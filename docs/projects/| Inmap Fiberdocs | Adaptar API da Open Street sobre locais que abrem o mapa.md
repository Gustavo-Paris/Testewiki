### Wiki do InMaps - IXCSoft

---

## API de Localização e Mapas

### **Introdução**

Com o objetivo de melhorar a experiência de uso dos clientes, foi realizada a integração do InMaps com a API da Open Street Maps (OSM) devido à descontinuação da API da Bing e às limitações impostas pela API do Google Maps. A API do Google exige cartão de crédito para a geração de chaves, motivo pelo qual buscou-se uma alternativa viável e gratuita.

---

### **Configuração e Acesso**

#### **Caminho para Configuração da API de Mapas**

Para configurar a API de mapas no IXC Provedor, siga o caminho abaixo:

1. **IXC Provedor > Configurações > Parâmetros > Parâmetros gerais**: 
    - Vá até a aba **Mapas**.
    - Dentro desta aba, selecione **API dos Mapas**.
    - Adicione a opção “Open Street Maps”.

!image-20240903-194007.png|width=1809,height=913,alt="Configuração da API OSM em InMaps"!

#### **Atualização dos Locais que Utilizam Mapa**

Os locais no IXC Provedor que utilizam a API de mapa foram atualizados para suportar a Open Street Maps. Abaixo estão listados os locais que abrem mapas no IXC Provedor, divididos conforme a presença de barra de busca:

##### **Sem Barra de Busca**

- IXC Provedor > Sistema > Suporte > Ordem de serviço > Outras funções > Mostrar no mapa
- IXC Provedor > Sistema > Suporte > Atendimento > Ordens de serviço > Outras funções > Mostrar no mapa

##### **Com Barra de Busca**

- IXC Provedor > Sistema > Cadastros > Clientes > Localização
- IXC Provedor > Sistema > Cadastros > Contratos > Endereço > Marcar coordenadas
- IXC Provedor > Sistema > Cadastros > Estrutura > Estrutura
- IXC Provedor > Sistema > Provedor > Logins > Localização > Localização (mapa)
- IXC Provedor > Sistema > Provedor > Transmissores > POP - Ponto de transmissão > Localização
- IXC Provedor > Sistema > Provedor > Cliente Fibra (ONU) > Localização
- IXC Provedor > Sistema > Inmap > Elementos > Caixa de atendimento > Localização
- IXC Provedor > Sistema > Inmap > Elementos > Caixa Subterrânea > Localização
- IXC Provedor > Sistema > Inmap > Elementos > Postes > Localização
- IXC Provedor > Sistema > Inmap > Elementos > Projetos > Localização
- IXC Provedor > Sistema > Inmap > Configurações > Projeto de execução > Visualizar
- IXC Provedor > Sistema > CRM > Prospecções > Localização
- IXC Provedor > Sistema > CRM > Prospecções > Endereço > Marcar coordenadas
- IXC Provedor > Sistema > CRM > Leads > Localização

---

### **Implementação Técnica**

#### **Arquivo: `Localizacao.php`**

O arquivo `Localizacao.php` contém a função que define a API de mapa a ser usada, a qual foi modificada para aceitar a OSM.

```php
private function mostrarLocalizacaoTela() {
    $this->api = $this->getActiveApis();
    $searchApi = $this->api["maps_search_api"];
    
    $mapApi = 'OSM';
    $mapKey = $mapApi === 'BL' ? $this->api["maps_bing_key"] : $this->api["maps_google_key"];
    $searchKey = $searchApi === 'BL' ? $this->api["maps_bing_key"] : $this->api["maps_google_key"];
    $googleKey = $this->api["maps_google_key"];

    define('PATH_TO_WEBROOT', '../../');
    $randInt = random_int(1, 10000);
    $html = '<!DOCTYPE html>
    <html>
        <head>
            ...
            <script type="text/javascript" src="js/packages/provedor-dist/map-library.bundle.js?version='.IXC_VERSAO.'"></script>
        ...
    </html>';
}
```

#### **Arquivo: `MapaPadrao.js`**

Modificação da classe de inicialização do mapa para suportar a OSM.

```javascript
constructor(mapApi, mapKey, options = {}) {
    this.mapApi = mapApi;
    if (mapApi === 'BL') {
        this.mapApi = 'bing';
    } else if (mapApi === 'GP') {
        this.mapApi = 'google';
    } else {
        this.mapApi = mapApi;
    }
}
```

Renomeação de métodos para refletir o novo suporte:

- `isBingApi` renomeado para `isOpenLayers`.

```javascript
isOpenLayers() {
    return !(this.mapApi === 'GP' || this.mapApi === 'google');
}
```

- `buildBingMap` renomeado para `buildOpenLayersMap`.

```javascript
async buildOpenLayersMap() {
    this.mapController.initMap();
    this.mapController.carregaMapas();
    let layer = 'Road';
    if (this.mapApi == 'BL' || this.mapApi == 'bing') {
        layer = 'Road';
    } else {
        layer = 'OSM';
    }

    this.mapController.selectLayer(layer);
}
```

#### **Arquivo: `OpenLayersAdapter.js`**

Correção de condicional para suportar a API OSM.

```javascript
if (this.mapsHereKeyApp?.length < 23) {
    // ...
}
```

---

### **Considerações Finais**

A integração com a API da Open Street Maps (OSM) visou proporcionar aos clientes uma alternativa gratuita e eficiente para a visualização de mapas, substituindo as APIs da Bing e, opcionalmente, do Google. Esta mudança é significativa para evitar custos adicionais e dependências desnecessárias, mantendo a qualidade e a funcionalidade do sistema.

Qualquer dúvida ou necessidade de suporte, por favor, entre em contato com nossa equipe de atendimento.

---

#### **Referências**

Para mais detalhes sobre a configuração e utilização, consulte a [Wiki do InMaps](https://wiki-inmap.ixcsoft.com.br/pt-br/home).

---

Este documento foi elaborado com informações de integração e desenvolvimento da equipe do InMaps da IXCSoft.
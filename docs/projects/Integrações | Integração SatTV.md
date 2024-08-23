# Integração SatTV com IXC Provedor

## 1. Visão Geral
A integração SatTV com IXC Provedor permite que os provedores de internet e TV gerenciem suas operações de TV via satélite diretamente através do sistema IXC. Esta integração inclui funcionalidades como autenticação de usuários, configuração de canais, pacotes de TV e monitoramento de serviços.

## 2. Dados do Ambiente de Homologação

- **URL da Documentação da API**: [http://apidoc.sattvgo.com.br/index.html](http://apidoc.sattvgo.com.br/index.html)
- **Usuário**: ixchml@satlabs.com.br
- **Senha**: k2WwEViZyjBbGLE
- **Provider ID**: c11ba198-55a3-40b9-bd2a-bb6c8f27b4f7

> **Nota**: Não utilize essas credenciais em ambientes de produção.

## 3. Funcionalidades Principais

### 3.1 Autenticação

A integração permite a autenticação de usuários no sistema SatTV diretamente a partir do IXC Provedor. Isto é feito através da API disponibilizada pela SatTV, onde as credenciais são verificadas e os tokens de autenticação são gerados.

### 3.2 Configuração de Canais

Os provedores podem configurar e gerenciar os canais de TV que serão disponibilizados aos seus clientes. Isso inclui a adição e remoção de canais, bem como a criação de pacotes de canais.

### 3.3 Gerenciamento de Pacotes de TV

É possível criar pacotes de TV customizados que podem ser oferecidos aos clientes. Esses pacotes podem incluir diferentes combinações de canais e serviços adicionais.

### 3.4 Monitoramento de Serviços

A integração permite monitorar o status dos serviços de TV, garantindo que o serviço oferecido aos clientes esteja sempre operante. Isso inclui a verificação de disponibilidade de canais e a qualidade do sinal.

## 4. Configuração no IXC Provedor

Para configurar a integração no IXC Provedor, siga os passos abaixo:

### 4.1 Acesso às Configurações de Integração

1. Acesse o IXC Provedor.
2. Vá para `Configurações > Integrações`.
3. Selecione `SatTV`.
4. Insira as credenciais de acesso e o `Provider ID`.

### 4.2 Configuração de Canais

1. Navegue até `Cadastros > TV > Canais`.
2. Adicione novos canais ou modifique os existentes conforme necessário.
3. Salve as alterações.

### 4.3 Configuração de Pacotes

1. Vá para `Cadastros > TV > Pacotes de TV`.
2. Crie novos pacotes ou edite os existentes.
3. Adicione os canais desejados a cada pacote.
4. Salve as alterações.

### 4.4 Monitoramento de Serviços

O monitoramento dos serviços de TV pode ser feito através do módulo de monitoramento do IXC Provedor:

1. Acesse `Monitoramento > TV`.
2. Verifique o status dos canais e a qualidade do sinal.
3. Acompanhe logs e históricos de eventos para identificar e resolver problemas.

## 5. Referências e Materiais de Apoio

- [Documentação da API SatTV](http://apidoc.sattvgo.com.br/index.html)
- [Wiki IXC Provedor](https://wiki.ixcsoft.com.br/pt-br/home)

Para mais informações e guias detalhados sobre outras funcionalidades do IXC Provedor, visite a [Wiki IXC Soft](https://wiki.ixcsoft.com.br/pt-br/home)【6:0†Wiki IXC】.
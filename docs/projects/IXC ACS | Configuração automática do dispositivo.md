# IXC ACS - Configuração Automática do Dispositivo

## Visão Geral

O IXC ACS oferece uma solução eficiente para a configuração automática de dispositivos assim que conectados à rede ou apontados para o sistema ACS. Essa funcionalidade busca automatizar a aplicação de configurações básicas como criptografia Wi-Fi, dados do protocolo TR069 e credenciais de acesso web, acelerando o processo de ativação e minimizando erros manuais.

### Objetivo

O desenvolvimento de um MVP (Produto Mínimo Viável) para a configuração automática visa:

- Reduzir o tempo de ativação e configuração manual de dispositivos.
- Eliminar a necessidade de acesso individual a interfaces web para configuração.
- Diminuir a probabilidade de erro humano e inconsistências nas configurações.
- Evitar o carregamento repetitivo de arquivos de configuração, semelhante a firmwares.

### Justificativa

O processo manual atual é lento e subjetivo a erros, especialmente em escalas médias e grandes. A automação não só otimiza o tempo de configuração como também garante um padrão de qualidade nas aplicações das definições. A experiência de um novo cliente, que utiliza uma funcionalidade similar em um concorrente (MadeForIt), reforça a necessidade dessa automação dentro do IXC ACS.

## Funcionalidades do Sistema

### Acesso Web

Ao criar ou editar uma configuração, os usuários podem especificar dados de acesso web que serão aplicados automaticamente aos dispositivos conectados.

### Configuração de DNS

- **DNS WAN:** No modo automático, impede a entrada de dados manuais. No modo manual, o DNS primário se torna obrigatório.
- **DNS LAN:** Funciona como o DNS WAN, especificamente para endereços IPv4.

### Configurações de NTP

- Requer seleção de uma opção de servidor NTP para ativar o botão de salvar.
- O campo de texto para o servidor NTP é obrigatório para preenchimento.

### Domínio Regulatório

Atualmente, a única opção disponível é "Brasil", garantindo conformidade com normas locais.

### Layer Bind

Permite seleção de portas LAN para preenchimento automático, podendo ser desmarcadas conforme necessário.

## Como Funciona

1. **Inicialização Automática:** Dispositivos conectados são detectados e configurados conforme as regras preestabelecidas.
2. **Modal de Configuração:** Usando a estética dos novos filtros, o usuário pode criar novas configurações através de um modal interativo.
3. **Aplicação de Configurações:** As definições ficam registradas e são aplicadas automaticamente aos dispositivos quando conectados.
4. **Informação de Modelos:** Ao clicar em "Mais informações", o sistema alerta sobre quais modelos podem não suportar certos parâmetros.

## Recursos Visuais e Protótipos

Para melhor compreensão do funcionamento e uso da funcionalidade de configuração automática, acesse os recursos visuais disponibilizados:
- [Protótipo do Figma - Projeto de Configuração Automática](https://www.figma.com/proto/BwoQV2tvgIuPuFX4Mg4K7x/Projeto---Configura%C3%A7%C3%A3o-autom%C3%A1tica-do-dispositivo?node-id=158-2400&t=dFr30e07RbixTqnE-1)
- [Apresentação do Protótipo no Figma](https://www.figma.com/proto/BwoQV2tvgIuPuFX4Mg4K7x/Projeto---Configura%C3%A7%C3%A3o-autom%C3%A1tica-do-dispositivo?node-id=158-2400&t=dFr30e07RbixTqnE-1)

Estamos à disposição para qualquer dúvida ou esclarecimento adicional.
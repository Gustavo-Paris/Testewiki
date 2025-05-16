# Wiki do InMap Sales - Personalização de Campos no Kanban

Bem-vindo à Wiki do InMaps Sales! Nesta seção, iremos abordar a personalização de campos diretamente no Kanban, uma funcionalidade que visa atender às demandas de flexibilidade dos usuários quanto à exibição de dados em cards de leads e negociações.

## Visão Geral

### Contexto
Diante da crescente necessidade de personalizar os cards no CRM, esta funcionalidade foi desenvolvida para permitir que os usuários customizem quais campos devem aparecer em cada card no Kanban, além de definir a obrigatoriedade de preenchimento de certos campos.

### Objetivo
Capacitar os usuários a:
- Personalizar cards com campos escolhidos.
- Criar novos campos específicos para leads/negociações.
- Determinar quais campos serão obrigatórios.

## Funcionalidades Principais

### Adicionar Campos Existentes
Usuários podem selecionar quais campos, já existentes nas tabelas de clientes, leads ou negociações, devem ser exibidos nos cards do Kanban.

### Criar Novos Campos
Permite a criação e adição de novos campos. Os usuários podem decidir se estes campos serão específicos para leads/negociações ou se também aparecerão no cadastro de clientes.

### Campos Obrigatórios
Opcionalidade de tornar certos campos obrigatórios para garantir o preenchimento de informações essenciais.

## Controle de Permissões
Para personalizar os campos no Kanban, é necessário ter permissões de administrador. As configurações são acessadas através de **Configurações > Campos Personalizados no Quadro Kanban**.

## Uso da Interface

### Configuração de Layout
- **Layout de Leads**
- **Layout de Negociações**
- **Layout de Prospecções/Clientes**

A interface inicial oferece um layout padrão que os usuários podem customizar, criando novos layouts conforme necessário.

### Interações Possíveis

- Mover campos entre seções de "Exibidos" e "Ocultos".
- Editar as configurações de visibilidade e obrigatoriedade através do menu contextual.
- Adicionar novos campos personalizados.

### Campos Essenciais
Alguns campos são essenciais para o funcionamento do Kanban e não podem ser removidos, apenas reordenados. Um tooltip alerta os usuários sobre a essencialidade destes campos.

## Integração Técnica

### Implementação no Banco de Dados
Os campos personalizados são armazenados no banco de dados como JSON, permitindo flexibilidade e expansão futura.

### Componentes Técnicos
Um novo componente será desenvolvido no Synapse para suportar a adição e manipulação de campos personalizados. Este componente irá gerenciar a renderização e a lógica de exibição na interface do usuário.

## Análise e Prototipagem

- Confira a análise de UX e os protótipos no [Figma](https://www.figma.com/design/7bpmGzOu1ujl2N2b0gepxo/IMDK-5559%7C-Kanban---Campos-personalizados?node-id=133-650&t=D6jEgTNHa3BU4Gua-1).

## Dicas de Utilização

Certifique-se de revisar os campos essenciais antes de realizar personalizações e sempre confirme as alterações para garantir a consistência dos dados.

Se precisar de suporte adicional na navegação e configuração, acesse a [Wiki do InMaps - IXCSoft](https://wiki-inmap.ixcsoft.com.br/pt-br/home) para orientações e tutoriais detalhados.

---
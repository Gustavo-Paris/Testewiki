# Reestruturação do Módulo de Propostas - InMap Sales

## Visão Geral

Este documento delineia a reestruturação do módulo de criação e gerenciamento de propostas no InMap Sales, parte do IXCSoft, com o objetivo de aprimorar a eficiência do processo e aumentar a flexibilidade na personalização e gestão de propostas comerciais.

## Problemas Identificados

1. Processo manual e suscetível a erros na criação de propostas.
2. Poucas opções de personalização e gerenciamento das propostas existentes.
3. Impacto negativo na eficiência operacional e na capacidade de resposta às demandas dos clientes.

## Soluções Propostas

- Reformulação do módulo para tornar a criação e gerenciamento de propostas mais automatizados e flexíveis.
- Inclusão de variáveis dinâmicas, como tabelas de preços, descontos e condições de pagamento, para personalização mais eficaz das propostas.

## Análise de Requisitos

### Formulário de Negociação no Kanban

#### Seção Produtos/Serviços

- Visualização de novos produtos ou serviços diretamente na seção Produtos/Serviços.
- Ajuste na interface para incluir uma aba entre as abas de Endereço e Proposta.
- Card de Produto/Serviço com informações como nome, quantidade, valor total e origem.
- Ordenação dos cards do último para o primeiro inserido.

#### Adição de Produtos ou Serviços

- Inclusão de botões para Novo Produto, Novo Serviço, Editar e Deletar.
- Formulário para inclusão de novos produtos ou serviços existente no plano de venda.
- Restrição na edição e deleção limitada a produtos ou serviços inseridos na negociação.

### Campos de Valores e Cálculos

- Introdução de campos para valor de ativação fixo, valor recorrente e outros relacionados a ativação e porcentagem.
- Cálculo automático do valor de ativação com base em percentuais definidos.
- Vinculação dos valores calculados à aba de Taxas de Ativação no módulo de Contrato.

## Configuração de Propostas no InMap Sales

- Integração do formulário de Modelos de e-mail/proposta no menu de configurações do InMap Sales.
- Mudança no nome do formulário para melhorar a intuitividade.
- Criação, edição e exclusão de modelos de propostas.

### Campos do Formulário de Edição

- Inclusão de campos como ID, status ativo, logo, cor dos botões, título e aceites digitais, entre outros.
- Editor de texto para personalizar o conteúdo da proposta.

## Reformulação da Tela de Criação de Propostas

- Funções para criar, salvar e excluir propostas.
- Envio de proposta via e-mail ou WhatsApp com interação sofisticada com o Opa! Suite.

### Geração de Link de Proposta

- Formato de link seguro e referido ao UUID criptografado.
- Indicação clara sobre status da proposta (aceita, recusada, validade de expiração).

## Personalização do Corpo da Proposta

- Editor de texto para edição do corpo da proposta.
- Upload de logotipo e controle sobre cores relacionadas ao título e botões da proposta.
- Inclusão de informações relevantes como vendedor, validade e detalhes do cliente na proposta.

### Botões de Ação

- Botões específicos para aceitação ou recusa de proposta com funcionalidade de feedback ao vendedor.

## Criação de Variáveis para Personalização

- Introdução de variáveis específicas que refletem valores dinâmicos designados no módulo de propostas.

## Conclusão

Esta reforma busca otimizar o fluxo de trabalho no InMap Sales, ao mesmo tempo que amplia a capacidade de resposta a solicitações dos clientes, com uma abordagem moderna e integrada para a elaboração de propostas comerciais dentro do ambiente IXCSoft.
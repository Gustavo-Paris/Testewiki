# Wiki do IXC Provedor: Notas Fiscais de Comodato e Gestão de Estoque

## Introdução

Neste documento, abordaremos a funcionalidade de emissão de notas fiscais de comodato no sistema IXC Provedor. Este processo foi otimizado para melhorar a usabilidade, reduzir o tempo de execução e minimizar erros operacionais.

**Principais Objetivos:**
- Facilitar a emissão de notas fiscais de comodato.
- Eliminar erros relacionados a divergências de inventário.
- Melhorar a usabilidade do sistema para emissão de notas.

## Funcionalidades de Gestão de Comodato

### Registro de Movimentações de Comodato

1. **Menu de Registro:** 
   - O sistema apresenta um menu exclusivo para registrar movimentações de comodato que inclui devolução e saída de equipamentos.
   - Campos: ID, Data de emissão, Data de saída, Cliente, Filial, Status da nota, Movimentação, ID da OS, Tipo de documento, Contrato.

2. **Formulários Integrados:**
   - Contrato → Aba Comodato
   - Ordem de serviço → Aba Comodato

### Geração de Notas Fiscais

1. **Emissão Automatizada:**
   - As notas de comodato, tanto de devolução quanto de saída, são geradas automaticamente.
   - A Grid de Comodato permite selecionar múltiplos registros para emissão de nota, agrupando itens do mesmo contrato em uma venda ou compra.

2. **Processamento de Notas:**
   - Ao clicar em *Faturar* na grid de comodato, o sistema gera a venda ou compra e emite a nota diretamente.

### Parâmetros Gerais

1. **Configurações de Documentos:**
   - Nos parâmetros gerais de estoque, são configurados os tipos de documentos utilizados na emissão de notas de comodato.
   - Condições a cumprir: 
     - Financeiro: Não
     - Gerencial: Sim ou Não
     - Fiscal: Sim
     - Estoque: Não

## Procedimentos Operacionais

- **Alterações de Notas:** As modificações, cancelamentos ou emissões devem ser realizadas através dos formulários de Compra ou Venda.
- **Status de Movimentações:** Os status da grid de comodato devem seguir as compras ou vendas associadas, de modo que a saída de comodato siga o status da venda e a entrada siga o da compra.

## Recomendações Fiscais

- A emissão da nota de comodato deve ocorrer o mais próximo possível do momento da instalação para registros adequados e prevenção de possíveis complicações fiscais.

## Comunicação e Transição para a Nova Funcionalidade

- **Informação ao Cliente:**
  - Sistema exibirá um pop-up informando a mudança para os usuários ao acessarem a antiga grid de pedidos via OS.
  - Disponibilização de materiais didáticos, como artigos e vídeos, para garantir o entendimento dos usuários sobre o novo fluxo de trabalho【4:0†source】.

## Conclusão

As melhorias no sistema IXC Provedor visam facilitar o gerenciamento de comodatos e patrimônios, reduzindo a carga operacional e minimizando erros no inventário e no processo fiscal. Esta abordagem proporciona uma experiência de usuário mais coerente e eficiente, ao mesmo tempo em que atende aos requisitos regulatórios impostos【4:8†source】.
# IXC Provedor - Wiki de Estoque e Patrimônio

Esta seção da wiki é dedicada a fornecer informações abrangentes sobre a funcionalidade de Estoque e Patrimônio do sistema IXC Provedor, focando na listagem e movimentação de produtos. Esta documentação é projetada para ajudar os clientes a compreender melhor os conceitos e usabilidade dessas funcionalidades.

## Estrutura e Parâmetros

### Parâmetro `permite_transferencia_automatica`
Este parâmetro permite que o provedor escolha se deseja ou não realizar transferências automáticas de produtos. Quando ativado, o sistema processará automaticamente a transferência de produtos entre filiais, simplificando o gerenciamento de estoque e minimizando erros humanos.

### Parâmetro `permite_informar_filial`
Este parâmetro define se o campo 'Filial' ficará habilitado. Ele permite ao usuário escolher de qual filial deseja retirar o saldo do produto, promovendo um controle mais preciso sobre a origem dos produtos e seus saldos.

## Regras de Listagem de Produtos

Quando ambos os parâmetros `permite_transferencia_automatica` e `permite_informar_filial` estão desativados, o sistema não deve listar os produtos de outras filiais para evitar erros de saldo e transferência. A regra padrão de listagem de produtos deve focar em:

- **Filial**: Listar produtos de todas as filiais que o operador tem acesso.
- **Almoxarifado**: Listar produtos de todos os almoxarifados aos quais o usuário tem acesso.
- **Patrimônio**: Focar no status 'Disponível' ou 'Disponível técnico', retirando saldo da filial do patrimônio correspondente.

### Controle de Estoque

Nos casos em que o parâmetro `controle_estoque` é definido para 'Bloqueia', o sistema adicionará um filtro extra para listar somente produtos com saldo superior a zero e com controle de estoque ativo, evitando a movimentação incorreta de produtos sem saldo disponível.

## Movimentação e Transferência de Produtos

### Procedimentos Padrões

- **Transferência Automática**: Remove a necessidade de aceitação manual, automatizando a movimentação ao selecionar produtos com saldo em outra filial.
- **Ocultação de Campos**: Os campos de patrimônio são ocultados quando o parâmetro `controlar_patrimonio` está desativado.

### Requisitos de Sistema

- O sistema deve respeitar os filtros aplicados nos campos de dropdown e nas buscas avançadas para garantir que somente os produtos apropriados sejam selecionados para movimentação.

## Práticas de Implementação

Este projeto deve ser entregue através de um `cannary deploy`, assegurando que nenhuma modificação afete os clientes sem prévio aviso e validação exaustiva de procedimentos. 

Para mais informações detalhadas sobre a implementação dessas funcionalidades, consulte os materiais e manuais disponibilizados no canal do YouTube e na documentação completa do IXC Provedor【4:0†Wiki IXCProvedor】.
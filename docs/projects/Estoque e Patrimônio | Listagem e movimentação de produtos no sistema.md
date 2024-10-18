# IXC Provedor - Documento de Wiki para Listagem e Movimentação de Produtos

Bem-vindo à seção de nossa Wiki dedicada à funcionalidade de Estoque e Patrimônio no sistema IXC Provedor. Este documento detalha a listagem e movimentação de produtos, levando em consideração novos parâmetros implementados e melhores práticas para uma gestão eficaz de seu inventário.

## Parâmetros Implementados

### Permite Transferência Automática

Este parâmetro, `{{permite_transferencia_automatica}}`, permite que o provedor escolha entre utilizar ou não transferências automáticas de produtos. Quando ativado, o sistema automatiza a transferência conforme as regras definidas.

### Permite Informar Filial

O parâmetro `{{permite_informar_filial}}` controla se o campo de Filial deverá ser preenchido, permitindo ao usuário escolher a filial de onde será retirado o saldo do produto.

## Regras de Listagem e Movimentação

### Cadastro de Produtos

Na seção de Cadastros → Contratos → Edita Comodato, a configuração de produtos obedecerá às seguintes diretrizes:

| Permitir Informar Filial | Permitir Transferência Automática | Conceito | Ação do Sistema |
|--------------------------|-----------------------------------|----------|-----------------|
| Sim                      | Sim                               | Todas as filiais e almoxarifados acessíveis. Patrimônio disponível ou disponível técnico. | Gera transferência automática; movimenta produto conforme filial no formulário. |
| Sim                      | Não                               | Filial conforme formulário. | Movimenta produto conforme filial no formulário. |
| Não                      | Sim                               | Todas as filiais e almoxarifados acessíveis. | Gera transferência automática; movimenta produto conforme filial no formulário. |
| Não                      | Não                               | Filial conforme formulário. | Movimenta produto conforme filial no formulário. |

## Requisitos para UX

- Criar uma Wiki explicativa para documentar como a listagem deve funcionar sob as diversas combinações de parâmetros.
- Ativar o modo de ajuda em todas as grids e formulários para oferecer informações adicionais.
- Enviar uma notificação uma semana antes de qualquer atualização que envolva alterações nas combinações de parâmetros.

## Movimentação de Patrimônios

No caso da gestão de patrimônios, a tabela abaixo resume as ações necessárias dependendo dos parâmetros escolhidos:

| Conceito | Ação do Sistema |
|----------|-----------------|
| Todas as filiais e almoxarifados acessíveis. Patrimônio disponível. | Retira o saldo e etiqueta da filial do patrimônio e insere na estrutura. |

## Considerações Finais

Para todas as operações de estoque e patrimônios, atente-se ao estado do parâmetro {{controle_estoque}}. Quando definido como *Bloqueia*, o sistema automaticamente aplicará um filtro durante a listagem, exibindo apenas produtos com saldo maior que zero e com controle de estoque ativado.

Este documento deve servir como um guia para maximizar a eficiência na gestão de estoques e patrimônios no IXC Provedor. Para mais detalhes, consulte nossas [páginas na Wiki IXC](https://wiki.ixcsoft.com.br) e vídeos no [canal IXC Soft no YouTube](https://youtube.com/@ixcsoft).
# Wiki de Emissão de Nota Fiscal de Transferência no IXC Provedor

## Introdução

A funcionalidade de **Emissão de Nota Fiscal de Transferência** no sistema IXC Provedor é essencial para empresas que necessitam transferir produtos entre suas filiais. Essa documentação foi desenvolvida para esclarecer o uso e a implementação dessa funcionalidade, garantindo conformidade com as obrigações fiscais de cada estabelecimento, de acordo com a Lei Complementar nº 87/1996 (Lei Kandir).

## CFOPs Utilizados

Os CFOPs (Código Fiscal de Operações e Prestações) mais freqüentes utilizados para emissão de notas fiscais no IXC Provedor são:

| ID no Sistema | CFOP | Descrição |
|---------------|------|-----------|
| 533           | 6552 | Transferência de bem do ativo imobilizado |
| 381           | 5552 | Transferência de bem do ativo imobilizado |
| 538           | 6557 | Transferência de material de uso ou consumo |
| 386           | 5557 | Transferência de material de uso ou consumo |
| 318           | 5152 | Transferência de mercadoria adquirida ou recebida de terceiros |
| 364           | 5409 | Transferência de mercadoria adquirida ou recebida de terceiros em operação com mercadoria sujeita ao |
| 518           | 6409 | Transferência de mercadoria adquirida ou recebida de terceiros, sujeita ao regime de substituição tributária |
| 317           | 5151 | Transferência de produção do estabelecimento |
| 517           | 6408 | Transferência de produção do estabelecimento quando o produto estiver sujeito ao regime de substituição |
| 363           | 5408 | Transferência de produção do estabelecimento quando o produto estiver sujeito ao regime de substituição |

## Objetivo

O objetivo principal da NF de Transferência é permitir que usuários possam emitir notas vinculadas às transferências previamente registradas, utilizando movimentações de produtos como base, assegurando conformidade e registro fiscal adequado entre diferentes filiais da mesma empresa.

## Escopo

### Funcionalidades e Requisitos

1. **Formulário de Transferência:** No módulo `transf_almox_top`, deve-se criar um botão "Emitir nota de saída".

2. **Coluna de Registro NF:** Adicionar uma nova coluna no menu de transferências entre almoxarifados para registro do número da NF, que deve buscar o número gerado pelo sistema.

3. **Parâmetro de Emissão da NF:** Implementar um parâmetro geral "Emitir nota fiscal de transferência: Sim/Não". Este parâmetro definirá se o botão deve estar disponível e habilitará a seleção obrigatória do tipo de documento, impedindo a escolha de documentos que gerem movimentações financeiras ou de estoque.

4. **Formulário de Venda:** Configurado para abertura ao clicar no botão "Emitir nota de saída", com preenchimento automático de:
   - **Filial Origem e Destino**;
   - **Datas de Emissão e Saída**;
   - **Valor Total dos Produtos**;
   - **Parâmetros de Frete, Comissão e Condições de Pagamento**;
   - **Filial Destino** identificando corretamente a transferência em questão.

5. **Validação de Transações:** Impedir a criação de novas vendas ou edição de dados de transferência, caso já exista uma venda derivada da transferência.

6. **Manutenção de Registros:** Deve-se ocultar botões e campos não necessários para o cenário de transferência e assegurar que movimentações financeiras não sejam duplicadas.

### Procedimentos de Cancelamento

Caso uma NF seja cancelada, deve ser desvinculado o campo `id_transf_almox_top` para permitir nova geração de NF referente àquela transferência.

## Observações Finais

A funcionalidade foi projetada respeitando as diretrizes fiscais e logísticas necessárias para uma implementação eficiente e segura, garantindo a rastreabilidade e compliance dos processos de transferência de mercadorias dentro do IXC Provedor.

---

Para mais informações e suporte, consulte a [documentação oficial do IXC Provedor](https://wiki.ixcsoft.com.br) ou entre em contato com nosso time de implementação .
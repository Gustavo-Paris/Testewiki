# Wiki para o Cliente sobre Pix Automático - modobank no ERP IXC Provedor

## Introdução ao Pix Automático - modobank

O *Pix Automático* é uma funcionalidade inovadora que está sendo integrada ao ERP IXC Provedor, com o objetivo de permitir pagamentos recorrentes e automatizados por meio do Pix. Essa solução visa facilitar o pagamento de compromissos financeiros, como mensalidades e assinaturas, diretamente entre o cliente e o recebedor, com a homologação do banco modobank e utilizando a API do Banco Central.

## Vantagens do Pix Automático

### Para a Empresa
- Ativação é feita imediatamente após autorização do cliente.
- Ideal para vendas tanto físicas quanto digitais, com potencial de reduzir inadimplência.
- Melhora a previsibilidade de fluxo de caixa.

### Para o Cliente
- Estabelece um limite máximo do valor da parcela debitada.
- Oferece a liberdade de encerrar o contrato sem multas.
- Automatiza os pagamentos, eliminando preocupações com datas de vencimento.

## Funcionamento e Configurações no IXC Provedor

### Configurações Necessárias
1. **Habilitação do Pix Recorrente**: Criação de um campo na carteira de cobrança para habilitar o Pix recorrente quando o gateway for modobank.
   - Display: "Utiliza PIX Recorrente".
   - Valores: Sim/Não (Padrão: Não).
   
2. **Parâmetros de Retentativas**: Permitirá configurar novas tentativas de débito, caso a primeira falhe.
   - Display: "Permite Retentativas PIX Recorrente".
   - Valores: Sim/Não (Padrão: Sim).

3. **Status de Recorrência PIX**: Adicionar campo no contrato com status como "Aguardando Aprovação", "Aceita", "Rejeitada", etc.

### Processo de Débito Automático
Uma vez autorizado:
- A empresa envia a cobrança ao PSP recebedor.
- O PSP do pagador é instruído a debitar na data prevista do vencimento ou no próximo dia útil.

## Jornadas de Autorização do Pagador

### Tipos de Jornada
1. **Solicitação Direta**: Requisição ao PSP do pagador que deve ser validada e aceita pelo cliente.
2. **QR Code Composto**: Lê-se um QR para configurar autorização recorrente.
3. **Open Finance**: Autorização via fluxos de Open Finance.

### FAQ - Perguntas Frequentes

- **O que é o Pix Automático?**: Permite que o pagador automatize pagamentos recorrentes.
- **Como Funciona a Autorização?**: Depende de permissão explícita pelo usuário, seguindo diferentes jornadas.

## Referências e Documentação

- [Manual de Padrões para Iniciação do Pix - Versão 2.8.1](#)
- API do Banco Central para o Pix: [Documentação API BACEN](https://bacen.github.io/pix-api/)

## Imagens e Diagramas

### Fluxo BPMN
![BPMN Diagram](#link-da-imagem) - Demonstra o processo de autorização e operação do Pix Automático.

Para mais informações e suporte, acesse nossa [Wiki IXC Provedor](https://wiki.ixcsoft.com.br/pt-br/home).

---

Este documento é feito para guiar o usuário do IXC Provedor, oferecendo detalhes e suporte técnico sobre a implementação e uso do Pix Automático com modobank.
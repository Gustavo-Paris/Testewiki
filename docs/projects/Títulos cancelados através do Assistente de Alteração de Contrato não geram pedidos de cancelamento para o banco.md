# Títulos Cancelados via Assistente de Alteração de Contrato - IXC Provedor

## Introdução
Nesta seção, abordaremos detalhadamente como o processo de cancelamento de títulos é gerenciado quando realizado através do Assistente de Alteração de Contrato no sistema IXC Provedor. Será descrito o que ocorre no backend do sistema quando há o cancelamento de boletos e como isso deve corresponder a ações disparadas automaticamente para os bancos ou integrações de cobrança.

---

## Sumário
- Introdução
- Relato de Situação
  - Problema Identificado
  - Caminho
- Análise Técnica
  - Metodologia de Cancelamento
  - Ajustes Necessários
- Procedimento de Correção
  - Definições Técnicas
  - Simulação de Ajustes
- Contato e Suporte

---

## Relato de Situação

### Problema Identificado
Ao realizar a troca de plano de venda de um contrato pelo Assistente de Alteração de Contrato com agrupamento de faturas, após o cancelamento dos boletos em aberto, os mesmos não são adicionados como pedido de baixa na remessa. Este problema é identificado pela ausência da geração automática de pedidos de cancelamento nos bancos para os tipos de carteira de cobrança PIX, Boleto, Débito em Conta e Gateway.

Esse problema é notado nas seguintes condições:
- Tipos de Cobrança: PIX, Boleto, Débito em Conta e Gateway
- Natureza do erro: O Sistema não está gerando pedidos de baixa nem enviando requisição de cancelamento para os bancos.

#### Caminho Para Reproduzir o Problema
```plaintext
1. Navegue até Sistema > Cadastros > Clientes > Financeiro
2. Utilize o Assistente de Alteração de Contrato para realizar alteração no plano de um contrato.
3. Gere boletos e realize cancelamento dos mesmos por meio do assistente.
4. Verifique se título cancelado entra como pedido de baixa na remessa.
```

---

## Análise Técnica

### Metodologia de Cancelamento
No sistema IXC Provedor, os métodos responsáveis pelo cancelamento de títulos dependem da natureza do tipo de cobrança. Abaixo está descrita a configuração padrão do sistema e onde devem ocorrer as modificações:
- **Para Carteiras do Tipo Boleto e Débito em Conta**:
  - Validar se pedido de baixa é gerado automaticamente para inclusão na próxima remessa.

- **Para Carteiras do Tipo PIX e Gateway**:
  - Enviar uma requisição de cancelamento para a integração associada (PIX, Gateway).

### Ajustes Necessários
Precisamos garantir que, ao cancelar boletos através do Assistente de Alteração de Contrato, o sistema chame os métodos corretos:
- **Boleto & Débito em Conta**: Adicionar movimentação de pedido de baixa para ser incluída na próxima remessa.
- **PIX & Gateway**: Enviar requisição de cancelamento para integração, atualizando o status para “Cancelado”.

---

## Procedimento de Correção

### Definições Técnicas
Devem ser replicados os métodos de cancelamento existentes no cancelamento manual para o processo do Assistente de Alteração de Contrato. As funções específicas a serem utilizadas são `FinalizarCobrancaPorAcao` para carteiras tipo Gateway ou Cartão e validação específica para PIX e boletos.

### Simulação de Ajustes
Simulação foi realizada nos seguintes clientes com diferentes carteiras de cobrança:
1. **Cliente ID 3 (Boleto)**:
   - Contrato ID 4
   - Boletos ID 61 à 72
   - Atualização da remessa e verificação da ausência de pedido de baixa.
2. **Cliente ID 6 (Débito em Conta)**:
3. **Cliente ID 4 (Gateway)**:
   - Contrato ID 5
   - Conta a Receber de IDs 73 à 84.
   - Falha na requisição de cancelamento, solicitada pela integração terceiro.
4. **Cliente ID 5 (PIX)**:

---

## Contato e Suporte

**Contato do Cliente**:
- naiara.carvalho@ampernet.com.br
- financeiro5@ampernet.com.br

Permissão para debug na base do cliente foi concedida. Cadastro de teste utilizado: `348088 - Teste IXC`.

**Acompanhamento e Suporte**:
Para mais informações, consulte a equipe técnica e desenvolvedores responsáveis na nossa base de conhecimento IXC Provedor utilizando os links abaixo:
- [Central de Notificações](https://wiki.ixcsoft.com.br/pt-br/home/central_notificacoes)
- [IXC Mobile](https://wiki.ixcsoft.com.br/pt-br/IXCMobile)
- [Primeiros Acessos](https://wiki.ixcsoft.com.br/pt-br/Primeiros_acessos_ao_sistema)
- [Parâmetros de Cobrança](https://wiki.ixcsoft.com.br/pt-br/CRM/Cobranca/Parametros_de_cobranca)

Para suporte adicional, acesse nossa página de suporte [Como chamar suporte ixcsoft](https://wiki.ixcsoft.com.br/pt-br/Como_chamar_suporte_ixcsoft)    .

---
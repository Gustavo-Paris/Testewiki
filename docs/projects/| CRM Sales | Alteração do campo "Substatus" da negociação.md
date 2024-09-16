### Wiki do Projeto: Alteração do Campo "Substatus" para "Motivo" nas Negociações - CRM Sales

#### Índice
1. [Introdução](#introdução)
2. [Objetivos](#objetivos)
3. [Descrição do Problema](#descrição-do-problema)
4. [Conceito da Funcionalidade](#conceito-da-funcionalidade)
5. [Caminho para Configuração](#caminho-para-configuração)
6. [Implementação da Mudança](#implementação-da-mudança)
7. [Motivação](#motivação)
8. [Timeline de Alterações](#timeline-de-alterações)
9. [Análise Técnica](#análise-técnica)
10. [Análise de UX](#análise-de-ux)
11. [Análise de Qualidade](#análise-de-qualidade)

---

### Introdução

Bem-vindo à Wiki do projeto CRM Sales, focado na alteração do campo "Substatus" para "Motivo" nas negociações. Este documento fornece uma visão detalhada das mudanças planejadas, instruções de configuração e análise de impacto.

---

### Objetivos

- **Melhorar a Usabilidade:** Alinhar a nomenclatura do campo com sua função real, facilitando o entendimento dos usuários.
- **Tornar o Campo Mais Assertivo:** Aprimorar a clareza e precisão das informações inseridas no sistema para melhor análise de dados.

---

### Descrição do Problema

Atualmente, o campo "Substatus" das negociações causa confusão entre os usuários devido ao seu nome impreciso. Esse campo especifica o motivo pelo qual uma negociação foi vencida ou perdida. A falta de clareza leva usuários a solicitar uma funcionalidade que já existe.

Além disso, quando se torna obrigatório o preenchimento do campo em negociações vencidas e perdidas, apenas no caso de negociação perdida é solicitado o motivo. Para negociações vencidas, o campo não é exibido, o que gera inconsistências nos dados coletados.

---

### Conceito da Funcionalidade

A funcionalidade serve para registrar o motivo que levou a vencer ou perder uma negociação. Isso permite à empresa agir com base em dados concretos, otimizando processos e estratégias comerciais.

**Vídeo Explicativo:** ![substatus melhoria.mp4](substatus_melhoria.mp4)

---

### Caminho para Configuração

Para configurar o campo "Motivo" no sistema, siga os passos abaixo:

**Configurações**
- Menu: Configurações > Parâmetros > Parâmetros Gerais > CRM > Substatus Obrigatório na Negociação > Ambos ou Vencemos

**Sistema**
- Menu: Sistema > CRM > Vencer/Perder Negociação
- Menu: Sistema > Inmap > Sales > Kanban > Negociações > Vencer/Perder Negociação

---

### Implementação da Mudança

1. **Renomear o Campo:** Alterar o nome do campo de “Substatus” para “Motivo” tanto nos parâmetros quanto no CRM.
2. **Apresentar Modal ao Vencer:** Apresentar um modal para preencher o motivo quando a venda for vencida via “Vencemos Simplificado”, semelhante ao procedimento atual de negociações perdidas.
3. **Adicionar Campo no Wizard:** Incluir um campo no Vencemos Wizard para preencher o motivo de vencer a negociação.

![Formulário Atualizado](image-20240730-194517.png)

---

### Motivação

A mudança visa tornar o uso do campo mais intuitivo e consistente com sua finalidade, melhorando a precisão dos dados coletados.

---

### Timeline de Alterações

- **Inmap Sales e CRM:** Alterado o nome do campo 'Substatus' para 'Motivo'.

---

### Análise Técnica

A análise técnica confirmou a viabilidade das alterações com as seguintes observações:

- Ambos os formulários, `crm_negociacoes_wiz` e `crm_negociacoes_simplificado`, estão associados à tabela `crm_negociacoes`, que contém o campo `substatus`. Portanto, podem ser ajustados conforme descrito nos itens 3.1 e 3.2.

---

### Análise de UX

Recomendações para a interface do usuário incluem:

1. **Separar os Parâmetros:** Mover parâmetros relacionados à prospecção para cima e os que não são, para baixo.
  
![Fieldset Organizado](image-20240806-165033.png)

2. **Renomear Parâmetros:** Alterar o nome do parâmetro: Configurações > Parâmetros > Parâmetros Gerais > CRM > Substatus Obrigatório na Negociação para Motivo Perdemos/Vencemos Obrigatório.
3. **Renomear Campo no Formulário:** Alterar o nome do campo substatus no formulário crm_negociacoes para Motivo Perdemos/Vencemos.

---

### Análise de Qualidade

#### O que está sendo entregue:

- Alteração do nome do campo `substatus` para `motivo`.
- Inclusão de campos para inserção de motivo em negociações vencidas.

#### O que foi feito no teste:

Procedimentos de validação foram realizados para garantir que a alteração do campo funcione conforme esperado, incluindo mensagens de erro apropriadas e validação ao tentar concluir uma negociação sem preencher o campo obrigatório.

---

Esperamos que esta Wiki ajude a entender as alterações feitas no sistema e facilite a adoção das novas funcionalidades. Para mais detalhes e suporte, consulte a [Wiki do InMaps - IXCSoft](https://wiki-inmap.ixcsoft.com.br/pt-br/home).
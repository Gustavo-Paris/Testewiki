# InMap Service | Dashboards Frotas

## Introdução

Este projeto visa a implementação de um painel de indicadores analíticos, chamado Dashboard de Frota no InMap Service. Este recurso é voltado para gestores operacionais e possibilita o acompanhamento em tempo real dos dados inseridos no módulo de Frotas. O dashboard transforma informações de campo, como abastecimento e quilometragem, em indicadores estratégicos de consumo e custo por veículo ou colaborador.

## Posicionamento

### Declaração do problema
Não existe atualmente um painel consolidado para a frota que permita o acompanhamento analítico dos indicadores de uso, consumo e custo, impactando gestores e diretores operacionais que necessitam monitorar a eficiência e o custo logístico.

### Solução Proposta
Implementar um dashboard de frota com dados de consumo, custos e manutenções programadas, alimentados automaticamente pelas informações inseridas no app e no sistema web.

## Pesquisa

O projeto evolui diretamente do "MVP Frotas e Rastreamento", utilizando dados estruturados de aplicativos e módulos do sistema web para construir indicadores gerenciais.

## Requisitos Funcionais

- **[RF-01] Criação de item no menu lateral "Dashboard"**: O sistema deve incluir um novo item "Dashboard" no menu lateral que direciona o usuário para a página de indicadores de frota.
  
- **[RF-02] Título geral do dashboard**: Centralizar o título "Dashboard de Frota" no topo da tela.

- **Cards com Indicadores**:
  - **[RF-03] KM Rodados**: Soma do KM final e inicial dos lançamentos válidos no período.
  - **[RF-04] Combustível Consumido**: Soma dos litros abastecidos.
  - **[RF-05] Custo Total**: Soma dos valores no campo "valor total" do formulário de abastecimento (exclui manutenções).
  - **[RF-06] Consumo Médio**: (KM Rodados) / (Litros abastecidos).
  - **[RF-07] Custo Médio por Litro**: (Valor Total Abastecido) / (Litros Abastecidos).
  - **[RF-08] Custo por KM Rodado**: (Valor Abastecido) / (KM Rodados).

- **[RF-09] Tabela Resumo de Veículos**: Exibir campos como Veículo, Próxima Revisão, Próxima Troca de Óleo e Consumo Médio.

## Requisitos Não Funcionais

- **[RNF-01] Tempo de Renderização**: Os dados do dashboard devem ser renderizados em menos de 3 segundos após seleção dos filtros.
- **[RNF-02] Responsividade**: Cards e tabelas devem ser responsivos em diferentes resoluções de tela.

## Requisitos de Integração

- **[RI-01] Integração de APIs**: O dashboard deve consumir dados de APIs de quilometragem e abastecimento do Service Mobile e do IXC Provedor.

## Casos de Uso

1. **Visualizar Indicadores Gerais**
   - Usuário acessa o menu "Dashboard" > "Frota"
   - O sistema exibe os dados do mês atual nos cards
   - Usuário ajusta filtros e o dashboard atualiza os dados

2. **Consultar Consumo de Veículo Específico**
   - Usuário filtra por veículo
   - Dashboard atualiza os dados, permitindo análise de manutenção necessária ou anomalias no consumo

## Restrições Adicionais

Apenas veículos com registros de abastecimento e quilometragem serão considerados nas métricas.

## Comitê de Aprovação

Os seguintes membros aprovam este projeto:

- Felipe Fussieger (Analista de Requisitos)
- Camila Mass (Líder de Suporte e Implantação)
- Eduardo Cardoso (Tech Lead)
- Pedro Riboli (Product Manager)
- Alexsandra Boita (UX)
- Junior Beluzzo (UX)
- Stéfanny da Rosa (Analista de Projetos)

## Protótipos de UX

Os protótipos estão disponíveis no [Figma](https://www.figma.com/design/tj3h48QMM3GMFZLeyXfGHe/Service---Rastreador?node-id=4038-4563&t=RzHLHgxHzLv5ZVxg-0).

## Análise de Qualidade

A qualidade será garantida por meio de testes abrangentes de funcionalidade, desempenho e segurança, com foco na usabilidade adequada conforme o design UX. As atualizações seguirão a abordagem de melhorias contínuas baseadas em feedbacks dos usuários.
### InMap Service | Roteirização/ Agendamento Automático

#### Descrição

A roteirização de agendamentos automatiza a organização de compromissos, maximizando eficiência e reduzindo tempos de deslocamento. Isso é possível através da integração com APIs do Google Maps e Bing Maps, que oferecem recursos robustos para calcular e otimizar rotas.

#### Ferramentas Utilizadas

**APIs do Google Maps:**

1. **Routes API:**
   - Evolução das APIs Directions e Distance Matrix, projetada para encontrar melhores rotas, calcular estimativas de tempo de chegada (ETAs) e distâncias.
   - [Documentação](https://developers.google.com/maps/documentation/routes)
   - [Exemplo prático de uso](https://developers.google.com/maps/documentation/routes/demo)

2. **API Distance Matrix:**
   - Calcula distâncias e durações de viagem entre múltiplos pontos de origem e destino.
   - [Detalhes sobre a API Distance Matrix](https://developers.google.com/maps/documentation/distance-matrix/overview?hl=pt-br)
   - [Demonstração da API Distance Matrix](https://developers.google.com/maps/documentation/javascript/examples/distance-matrix#maps_distance_matrix-javascript)

3. **API Directions:**
   - Visualiza rotas para diversos modos de transporte (carro, bicicleta, transporte público e caminhada), com instruções passo a passo.
   - [Guia para a API Directions](https://developers.google.com/maps/documentation/directions?hl=pt-br)
   - [Obtenção de instruções de direção](https://developers.google.com/maps/documentation/directions/get-directions?hl=pt-br)

**APIs do Bing Maps:**

1. **Create Driving Route:**
   - Calcula rotas de direção específicas para veículos.
   - [Documentação e Exemplos](https://www.bing.com/api/maps/sdk/mapcontrol/isdk/directionscreatedrivingroute)

#### Análise de UX

- **Organização do Fluxo:**
  - [Miro Board](https://miro.com/app/board/uXjVKfKbZjU=/)
- **Protótipo e Informações Gerais:**
  - [Figma Protótipo](https://www.figma.com/file/0YUzCfFnk2r9e0eUvAOnLm/Service---Roteiriza%C3%A7%C3%A3o?type=design&node-id=0%3A1&mode=design&t=1cbQ6LDjyWyNGnk3-1)
- **Estudo:**
  - [Notion Estudo](https://www.notion.so/alequesandra/2-Pesquisar-d8d5314dc836491e96e56c0d4f70dd5a?pvs=4)

#### Análise Técnica

**Estrutura Inicial de Cartões:**

1. **Pacote de Rotas**
   - Agnóstico a aplicação, utilizável por todo IXC provedor.
2. **API Google**
3. **API Bing**
4. **Estrutura de Adaptação para APIs de Roteirização**

**Roteirização Manual:**

- Mover acesso a roteirização manual ao novo menu.
- Uso da API na roteirização manual.
- Atualização do overlay e ajustes de front.
- Botão confirmar (módulo synapse para confirmação e mensagem de sucesso).

**Configurações:**

- **Configurações de Roteirização**:
  - Aba “Roteiro”, “Ordens de Serviço”, “Colaboradores”, “Colaborador”, “Assuntos”.
- **Módulo de Aviso sobre Custos.**

**Assistente de Roteirização:**

- Seleção das OS com desenho da região no mapa.
- **Assistente de Roteirização**:
  - Aba “Configurações”, “Colaboradores”, “Gerar Rota”.
- Implementação do algoritmo Sweep.
- Roteirizar por menor distância, prioridade, menor tempo.
- Estrutura do gerenciador das rotas/exibição dos colaboradores.
- Overlay das Ordens de Serviço (OSs).
- Ver e editar rota, ordenação das OSs, agendar rota/tudo, trocar colaborador.
- Atualizar notificação do aplicativo.

#### Imagens:

![Roteirização Google Maps](https://developers.google.com/maps/documentation/routes/images/screenshot-1.png)
![Roteirização Bing Maps](https://www.bing.com/api/maps/sdk/mapcontrol/isdk/directionscreateikingroute.png)

---

**Notas Finais:**
A integração com as ferramentas de roteirização do Google e Bing são fundamentais para aumentar a eficiência e otimização das rotas nos serviços prestados, beneficiando diretamente os colaboradores e clientes com maior precisão e redução de tempos de deslocamento.
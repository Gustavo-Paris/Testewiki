# InMap Service | Roteirização / Agendamento Automático

Bem-vindo à Wiki do InMap Service, onde iremos explorar o incrível mundo da roteirização e agendamento automático, utilizando as funcionalidades do InMaps da IXC Soft. Aqui você encontrará tudo o que precisa saber para maximizar a eficiência na organização de compromissos e otimização de tarefas. 

---

## Sumário

- [Introdução](#introdução)
- [Estudo de Ferramentas](#estudo-de-ferramentas)
  - [Google Maps APIs](#google-maps-apis)
  - [Bing Maps APIs](#bing-maps-apis)
- [Análise de UX](#análise-de-ux)
- [Análise Técnica](#análise-técnica)
  - [Estruturação Inicial](#estruturação-inicial)
  - [Configurações](#configurações)
  - [Assistente de Roteirização](#assistente-de-roteirização)
- [Recursos Adicionais](#recursos-adicionais)
- [Links Relevantes](#links-relevantes)

---

## Introdução

A roteirização de agendamentos é um processo essencial para qualquer serviço que busca maximizar a eficiência na organização de compromissos, otimizando a sequência de tarefas de acordo com critérios específicos. Neste guia, utilizaremos APIs renomadas como Google Maps e Bing Maps para alcançar esse objetivo.

---

## Estudo de Ferramentas

### Google Maps APIs

#### Routes API
A Routes API representa a evolução otimizada das APIs Directions e Distance Matrix. Desenvolvida para encontrar as melhores rotas de A a Z, calcular estimativas de tempo de chegada (ETAs) e distâncias entre várias localizações.
- **Documentação:** [Link para a documentação da API Routes](https://developers.google.com/maps/documentation/routes)
- **Demonstração:** [Exemplo prático de uso da API Routes](https://developers.google.com/maps/documentation/routes/demo)

#### Distance Matrix API
Calculate distâncias e durações de viagem entre uma matriz de origens e destinos para diversos modos de transporte.
- **Documentação:** [Detalhes sobre a API Distance Matrix](https://developers.google.com/maps/documentation/distance-matrix/overview?hl=pt-br)
- **Exemplo de Uso:** [Demonstração do uso da API Distance Matrix](https://developers.google.com/maps/documentation/javascript/examples/distance-matrix#maps_distance_matrix-javascript)

#### Directions API
Visualiza rotas para diversos modos de transporte, incluindo carro, bicicleta, transporte público e caminhadas.
- **Documentação:** [Guia para a API Directions](https://developers.google.com/maps/documentation/directions?hl=pt-br)
- **Instruções de Uso:** [Obtenção de instruções de direção](https://developers.google.com/maps/documentation/directions/get-directions?hl=pt-br)

---

### Bing Maps APIs

#### Create Driving Route
Permite o cálculo de rotas de direção específicas para veículos.
- **Documentação e Exemplos:** [Criando rotas de direção com Bing Maps](https://www.bing.com/api/maps/sdk/mapcontrol/isdk/directionscreatedrivingroute)

#### Exemplos Adicionais
- [Example 1](https://learn.microsoft.com/en-us/bingmaps/rest-services/examples/driving-route-example?source=recommendations)
- [Example 2](https://learn.microsoft.com/en-us/bingmaps/rest-services/routes/calculate-a-route#examples)

---

## Análise de UX

Organização do fluxo e protótipos desenvolvidos para a experiência do usuário.
- **Organização do Fluxo:** [Miro Board](https://miro.com/app/board/uXjVKfKbZjU=/)
- **Protótipo, Informações Gerais e Instruções:** [Figma File](https://www.figma.com/file/0YUzCfFnk2r9e0eUvAOnLm/Service---Roteiriza%C3%A7%C3%A3o?type=design&node-id=0%3A1&mode=design&t=1cbQ6LDjyWyNGnk3-1)
- **Estudo:** [Notion](https://www.notion.so/alequesandra/2-Pesquisar-d8d5314dc836491e96e56c0d4f70dd5a?pvs=4)

---

## Análise Técnica

A seguir uma análise técnica, determinando os recursos e tempo necessário para a implementação:

### Estruturação Inicial
- Criar pacote de rotas (agnóstico à aplicação, todo IXC provedor poderá usar)
- Integração com APIs Google e Bing
- Estrutura de adaptação para APIs de roteirização

### Configurações
- **Aba "Roteiro"**
- **Aba "Ordens de Serviço"**
- **Aba "Colaboradores"**
- **Aba "Assuntos"**
- Módulo de aviso sobre custos

### Assistente de Roteirização
- Seleção das OS com desenho da região no mapa
- Diversas configurações e execução de roteirização
- Implementação do algoritmo Sweep ([verificar artigo interessante](https://www.sciencedirect.com/science/article/abs/pii/S187449072030313X))
- Opções de roteirização por menor distância, tempo e prioridade
- Gerenciamento das rotas e colaboradores
- Agendamento de rotas

> Análise finalizada em 16/07, registrada hoje em 15/08

---

## Recursos Adicionais

- **Documentos PDF:** Consulte [documentos técnicos](https://docs.google.com/document/d/12dz7qBzKNwv6bBTwmHWrri4HssbFKpfn87tTCziz2yY/edit?usp=sharing) para obter mais detalhes sobre a visão do projeto.

---

## Links Relevantes

- [Wiki do InMaps - IXCSoft](https://wiki-inmap.ixcsoft.com.br/pt-br/home)
- [Canal IXC Soft no YouTube](https://youtube.com/@ixcsoft?si=ttPB4ZyUpmDKkwdx)

---

Espero que esta Wiki ajude você a entender e implementar a roteirização e agendamento automático com eficiência. Fique à vontade para explorar, e se tiver dúvidas, consulte a documentação fornecida. Feliz roteirização!
# Wiki do InMap Fiberdocs - Integração com Wispro

## Problema

O Fiberdocs atualmente depende do IXC Provedor, tanto em seu código quanto no banco de dados, o que dificulta a sua integração com outras plataformas e limita seu crescimento no mercado. Essa dependência impede que ele atenda clientes do Wispro, que necessitam de ferramentas para documentação de redes, restringindo seu alcance e reduzindo oportunidades de expansão.

---

## Como Vamos Resolver

Proposta a separação do Fiberdocs do IXC Provedor, criando uma integração direta com a plataforma Wispro. O usuário irá acessar o Fiberdocs diretamente via uma URL, interagindo através de pontos de interesse no mapa Wispro, sem precisar acessar o IXC Provedor. A sincronização de dados será automática e constante entre as plataformas, refletindo quaisquer alterações combinadamente.

Esta estratégia permitirá ao Fiberdocs adaptar-se às necessidades dos clientes Wispro que migram para redes de fibra, ampliando mercado e adaptabilidade.

---

## Critérios de Aceitação e Requisitos

1. **Independência do IXC Provedor**: Fiberdocs deve operar de forma independente, mantendo a estrutura do IXC Provedor somente localmente.
2. **Integração Direta com Wispro**: Facilitar redirecionamento automático através de URL, sem interrupções.
3. **Sincronização de Dados**: Assegurar atualização em tempo real entre Wispro e Fiberdocs.
4. **Interface de Usuário Intuitiva**: Manter acesso simples e direto.
5. **Suporte à Internacionalização**: Preparar Fiberdocs para diferentes mercados e clientes da Wispro.
6. **Estabilidade e Desempenho**: Garantir integração estável sem impacto negativo.

---

## Análise de Negócio

O projeto representa uma oportunidade estratégica de aumentar o alcance do Fiberdocs reduzindo a dependência do IXC Provedor, e suprimindo uma demanda crescente no mercado de provedores de internet.

---

## Análise Técnica

### Análise Inicial:

- **Infraestrutura Inicial**: Utilização do Apache Kafka, Consumer IXC, e Wispro Service para monitoramento, tratamento de dados e autenticação do usuário.

### Críticas e Ajustes Propostos:

1. **Identificação de Clientes**: Dificuldades na separação por filial.
2. **Segurança e Permissões**: Riscos na concessão de permissões de leitura e gravação.
3. **Conexão**: Instabilidade devido ao uso de túneis SSH.
4. **Configuração**: Necessidade de credenciais separadas do código-fonte.

### Solução Proposta:

- **Consumer IXC & Kafka**: Uso contínuo do monitoramento, agora com interações seguras via API.
- **Auth Service**: Responsável pela autenticação, identificação de cliente, e controle por filial.
- **Melhorias de Segurança**: Implementação de controle interno do túnel SSH e SQL Injection.

**Nota BÔNUS**: Implementar API adicional para facilitar integração futura.

---

## Análises Complementares

### U.X & Segurança

- **UX Simples**: Experiência do usuário fluida e sem complicações.
- **Segurança Reforçada**: Proteção de dados e autenticação robusta mediante ajustes nas conexões e permissões.

---

## Documentação Wiki

Confira este espaço para atualizações contínuas sobre a integração Fiberdocs-Wispro, exploração de funcionalidades e orientações a usuários.

[Para mais informações, acesse a Wiki oficial da IXCSoft](https://wiki-inmap.ixcsoft.com.br/pt-br/home)

---

Agradecemos a colaboração de todos os envolvidos no projeto para tornar esta integração possível e seu apoio contínuo no desenvolvimento de soluções para melhor atender nossos clientes.
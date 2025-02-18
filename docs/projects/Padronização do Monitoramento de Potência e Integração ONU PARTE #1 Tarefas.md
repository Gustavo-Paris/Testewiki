# Monitoramento de Potência e Integração de ONU na Plataforma IXC

> Este documento visa padronizar e melhorar o monitoramento de potência das ONUs no sistema IXC, proporcionando informações mais precisas para a gestão eficiente de redes.

---

## Visão Geral

### História do Usuário

**Cenário**:
- Como gerente de redes em um provedor de internet, a estabilidade e funcionalidade da conexão dos assinantes são primordiais.

**Objetivo**:
- Obtenção de dados precisos sobre o provisionamento, sinal e tempo conectado de clientes, atualmente dificultados pela forma inadequada de validação dos dados das ONUs (equipamentos de fibra).

**Motivo**:
- Melhorar a tomada de decisões, corrigir problemas rapidamente, e identificar irregularidades com agilidade, visando eficiência no atendimento e redução do tempo de resolução de problemas.

**Solução**:
- Aperfeiçoar a tarefa de monitoramento e implementar a funcionalidade "potência/resumo ONU".
- Utilizar o *MAC/Serial* para identificação de ONUs autorizadas, evitando a dependência do *número/pon/slot*.
- Criar um fluxo que facilite a identificação de inconsistências nos dados.

---

## Solução Proposta

### Ações Planejadas

**1. Padronização e Botão "Potência/Resumo ONU"**:
- Ajustar tarefas relacionadas ao monitoramento e potência/resumo das ONUs para garantir dados consistentes.

#### Tarefa de Monitoramento
- Validar ONU usando *MAC/Serial*.
- Verificar e registrar dados como potência do sinal, última atualização, voltagem e temperatura.
- Atualizar status das ONUs (online/offline/autorizada/desautorizada) conforme validação.

#### Botão Potência
- Implementar validação precisa usando *MAC/Serial*.
- Atualizar ONU com dados corretos em caso de inconsistências.
- Gerar status indicativo quando a ONU não for encontrada.

### Comportamento de Atualização de Dados
- **ONU Online**: Mostrar status 'online', atualizar potência e data, e status para autorizada.
- **ONU Offline**: Mostrar status 'offline', sinal zerado, atualizar data, e status para autorizada.
- **ONU Não Encontrada**: Indicar situação, sinal zerado, atualização de data, e alterar status para desautorizada.

---

## Critérios de Aceitação e Requisitos
- As implementações devem atender aos requisitos funcionais para garantir precisão e eficiência no monitoramento e atualização de cada ONU.

## Análise Técnica
- *Analista Técnico*: Cruzar ONUs dos equipamentos com o sistema antes do monitoramento.
- Validar dados de PONID e números das ONUs em buscas manuais para evitar potenciais erros.

## Análise U.X
- Indicar visualmente quando a ONU não está autorizada através de interfaces claras e intuitivas.

---

## Documentação e Recursos Adicionais

Para maiores detalhes, consulte:
- [Documentação Wiki IXC](https://wiki.ixcsoft.com.br)【4:0†source】.
- [Figma Design Interface](https://www.figma.com/design/f16rothuu5faWyc3hOCDb7/IR-4985?node-id=11-14&t=qqK9Bvmy023CmXSQ-1)

---

Este conteúdo foi organizado para proporcionar uma visão abrangente e detalhada sobre as melhorias propostas no monitoramento das ONUs, assegurando que o sistema IXC Provedor atenda às necessidades de precisão e funcionalidade crítica dos gerentes de rede.
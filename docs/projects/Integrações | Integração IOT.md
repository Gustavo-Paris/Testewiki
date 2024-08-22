# Documentação da Funcionalidade: Integração IoT

## Introdução à Funcionalidade

A funcionalidade de Integração IoT foi desenvolvida para facilitar a conexão entre o sistema IXCProvedor e a plataforma de IoT. O propósito desta integração é otimizar o gerenciamento de clientes, assinaturas e licenças de dispositivos, proporcionando uma experiência mais fluida e eficiente para os usuários finais. Os benefícios incluem um registro centralizado de clientes, a possibilidade de acompanhar as assinaturas e a gestão de novos dispositivos de forma simplificada.

## Visão Geral

Esta documentação descreve a integração entre o IXCProvedor e o sistema de IoT, detalhando os objetivos principais e requisitos necessários para a implementação. Os principais objetivos incluem:
- Criação de registros de integração no sistema.
- Geração de tabelas específicas para gerenciar clientes e licenças.
- Vinculação de produtos do IXCProvedor ao IoT para uma gestão mais eficiente.

### Requisitos da Funcionalidade
- Necessidade de autenticação para acessar a API.
- Definição de novas tabelas no banco de dados, incluindo Licença IoT.
- Mecanismo para busca e criação de clientes no sistema de IoT.

## Instruções de Uso

Para utilizar a funcionalidade de Integração IoT, siga os passos abaixo:

1. **Autenticação na API:**
   Para realizar requisições à API do IoT, você precisa autenticar sua aplicação. Utilize o seguinte formato para o corpo da requisição:

   ```json
   {
       "grant_type": "client_credentials",
       "client_id": "olli.oa2-client.0b76205e9431aafa975765ff350a1cfb",
       "client_secret": "2e2c0e7be83025d88969eb5efe39b67c4cb8de4c3055dd27c88ea52ed5f38dd2"
   }
   ```

2. **Criação do Registro de Integração:**
   Depois de se autenticar, você pode criar um registro de integração no sistema utilizando o formulário `sva_configuracoes`.

3. **Gerenciamento de Licenças:**
   No contrato do cliente, adicione uma nova tabela chamada "Licença IoT". Quando um cliente for criado ou já existir, você precisará gerar a assinatura e a licença apropriadas.

4. **Busca de Produtos:**
   Busque os itens disponíveis através do FN (Faturamento Nacional) e vincule esses itens na tabela de produtos do IXCProvedor.

## Cenários de Uso

### Cenário 1: Criação de Um Novo Cliente
1. Um novo cliente solicita um serviço de IoT.
2. O usuário se autentica na API e cria o registro de cliente no sistema.
3. O sistema gera a assinatura e licença para o novo cliente.

### Cenário 2: Integração de Dispositivos Existentes
1. Um cliente já existente decide adicionar novos dispositivos.
2. O usuário busca o cliente pelo FN.
3. Os novos dispositivos são vinculados ao contrato existente e as licenças são geradas.

## Dicas e Melhores Práticas

- **Validação de Dados:** Sempre valide os dados do cliente antes de realizar a criação ou atualização para evitar inconsistências.
- **Auditoria:** Mantenha um registro de todas as requisições realizadas para facilitar a solução de problemas e auditorias futuras.
- **Teste a API:** Realize testes regulares na API para garantir que as integrações funcionam conforme esperado.

## Perguntas Frequentes (FAQ)

### Como sei se um cliente já está cadastrado no sistema?
Utilize a rota específica para buscar clientes no sistema IoT antes de tentar criar um novo registro.

### O que faço se ocorrer um erro na autenticação da API?
Verifique se as credenciais utilizadas estão corretas e se a conta de cliente tem permissões adequadas.

### Quais documentos são necessários para configurar a Licença IoT?
As informações básicas do cliente e a lista de produtos a serem vinculados devem estar disponíveis para configuração.

## Recursos Adicionais

- [Documentação da API](https://documenter.getpostman.com/view/32140489/2s9YsKhY32#d38c2ce0-6b26-4db9-aabb-0f94880523b6)
- [Portal de Acesso](https://partner.olli.digital/)
- [Planilha de Integração](https://docs.google.com/spreadsheets/d/1HYHJE2kLceH_i8peCcL3faeRPQkYWMkOs5Tn-V5pX1g/edit#gid=0)

Para maior entendimento e orientação, confira os links e documentos adicionais relacionados à funcionalidade de Integração IoT.
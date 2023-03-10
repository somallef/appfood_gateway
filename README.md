# appfood [API Gateway]

Projeto criado como acompanhamento do treinamento [Microsserviços na prática: implementando com Java e Spring](https://www.alura.com.br/curso-online-microsservicos-implementando-java-spring)

Em uma arquitetura de microsserviços o gateway fornece um **ponto único de entrada**. Através da porta definida na propriedade `server.port` todos os microsserviços registrados no discovery poderão ser acessados:

`http://localhost:8082/pedidos-ms/pedidos`

`http://localhost:8082/pagamentos-ms/pagamentos`

Além disso, o Spring Cloud Gateway obtém a lista de endereços de todos os serviços registrados no Eureka Server, configura uma rota dinâmica para esses serviços e já faz o balanceamento de carga nas requisições (distribui as requisições vindas do cliente para as várias instâncias disponíveis de um serviço). 
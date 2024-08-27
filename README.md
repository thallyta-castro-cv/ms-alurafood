# Microserviço de pedidos e pagamentos com Spring Cloud

<b> Este projeto foi criado com Spring e Spring Cloud e se trata de um monorepo de dois microserviços: pedidos e pagamentos, bem como os
recursos necessários para sua implementação e integração.</b>

# Sobre o projeto
Este projeto foi desenvolvido como parte do curso da Alura sobre implementação de microserviços com Spring Cloud, com o propósito de criar um sistema eficiente e escalável para gerenciar pedidos e pagamentos em uma arquitetura de microserviços. O projeto utiliza tecnologias como Eureka, Gateway, OpenFeign e Load Balancer para oferecer uma solução completa.

# Objetivo
O objetivo principal deste microserviço é fornecer uma base sólida para consultas futuras e servir como referência para a 
implementação de funcionalidades e arquitetura de microserviços em projetos semelhantes. 

# Tecnologias Utilizadas

# Tecnologias Utilizadas

| Tecnologia     | Função                          | Descrição                                                                                                                                                                                                                              | Implementação     |
|----------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| Eureka         | Serviço de Registro e Descoberta | Eureka é utilizado para registrar e descobrir microserviços na arquitetura, facilitando a comunicação entre eles. Cada microserviço se registra no servidor Eureka, permitindo que outros serviços descubram e se comuniquem de maneira eficiente. | Projeto `server`  |
| Gateway        | Roteamento e Agregação          | O Gateway atua como um ponto de entrada único para a arquitetura de microserviços. Ele roteia as requisições do cliente para os microserviços apropriados e pode realizar a agregação de dados provenientes de diferentes serviços.         | Projeto `gateway` |
| OpenFeign      | Cliente HTTP Declarativo        | OpenFeign simplifica as chamadas de serviço HTTP entre microserviços. Ele permite que as chamadas sejam feitas de forma declarativa, reduzindo a complexidade do código e facilitando a integração entre os serviços. Neste projeto, o microserviço de pagamentos se comunica com pedidos para informar que o pedido foi pago. | Projeto `pagamentos` |
| Load Balancer  | Distribuição de Carga           | O Load Balancer distribui o tráfego entre várias instâncias dos microserviços, garantindo que a carga seja distribuída de maneira equitativa. Isso melhora a escalabilidade e a confiabilidade do sistema. Neste projeto, o gateway registra todas as instâncias de auto scaling e distribui a carga entre elas. | Projeto `gateway` |
| Resilience4j + Spring AOP | Circuit Breaker               | O *Resilience4j* é utilizado para implementar a estratégia de *Circuit Breaker* no microserviço de pagamentos. Combinado com *Spring AOP*, ele ajuda a proteger o sistema contra falhas temporárias, evitando sobrecarga e degradação de serviços quando outro serviço está indisponível. | Projeto `pagamentos` |



# Organização dos projetos

| Projeto    | Descrição                                                                            |
|------------|--------------------------------------------------------------------------------------|
| pagamentos | Microserviço de pagamento.                                                          |
| pedidos    | Microserviço de pedidos.                                                            |
| server     | Projeto com serviço de descoberta Eureka Server usando Spring Cloud Netflix.         |
| gateway    | Projeto com implementação de endereço que faz as requisições e delega para o microsserviço certo e faz o balanceamento de carga automaticamente em instâncias que são escaladas. |


# Autor
<b>Thallyta Macedo Carvalho de Castro</b>

Linkedin: https://www.linkedin.com/in/thallyta-castro/

Medium: https://medium.com/@thallyta-castro-cv

email: thallytacastro.dev@gmail.com

# Microserviço de pedidos e pagamentos com Spring Cloud

<b> Este projeto foi criado com Spring e Spring Cloud e se trata de um monorepo de dois microserviços: pedidos e pagamentos, bem como os
recursos necessários para sua implementação e integração.</b>

# Sobre o projeto
Este projeto foi desenvolvido como parte do curso da Alura sobre implementação de microserviços com Spring Cloud, com o propósito de criar um sistema eficiente e escalável para gerenciar pedidos e pagamentos em uma arquitetura de microserviços. O projeto utiliza tecnologias como Eureka, Gateway, OpenFeign e Load Balancer para oferecer uma solução completa.

# Objetivo
O objetivo principal deste microserviço é fornecer uma base sólida para consultas futuras e servir como referência para a 
implementação de funcionalidades e arquitetura de microserviços em projetos semelhantes. 

# Tecnologias Utilizadas

| Tecnologia   | Função                        | Descrição                                                                                                                                                  | Implementação     |
|--------------|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| Eureka       | Serviço de Registro e Descoberta | Eureka é utilizado para registrar e descobrir microserviços na arquitetura, facilitando a comunicação entre eles. Cada microserviço se registra no servidor Eureka, permitindo que outros serviços descubram e se comuniquem de maneira eficiente. | Projeto `server`  |
| Gateway      | Roteamento e Agregação        | O Gateway atua como um ponto de entrada único para a arquitetura de microserviços. Ele roteia as requisições do cliente para os microserviços apropriados e pode realizar a agregação de dados provenientes de diferentes serviços. | Projeto `gateway` |
| OpenFeign    | Cliente HTTP Declarativo      | OpenFeign simplifica as chamadas de serviço HTTP entre microserviços. Ele permite que as chamadas sejam feitas de forma declarativa, reduzindo a complexidade do código e facilitando a integração entre os serviços. | -                 |
| Load Balancer| Distribuição de Carga         | O Load Balancer distribui o tráfego entre várias instâncias dos microserviços, garantindo que a carga seja distribuída de maneira equitativa. Isso melhora a escalabilidade e a confiabilidade do sistema. | Projeto `gateway`                 |


# Organização dos projetos

| Projeto    | Descrição                                                                            |
|------------|--------------------------------------------------------------------------------------|
| pagamentos | Microserviço de pagamento.                                                          |
| pedidos    | Microserviço de pedidos.                                                            |
| server     | Projeto com serviço de descoberta Eureka Server usando Spring Cloud Netflix.         |
| gateway    | Projeto com implementação de endereço que faz as requisições e delega para o microsserviço certo. |


# Autor
<b>Thallyta Macedo Carvalho de Castro</b>

Linkedin: https://www.linkedin.com/in/thallyta-castro/

Medium: https://medium.com/@thallyta-castro-cv

email: thallytacastro.dev@gmail.com

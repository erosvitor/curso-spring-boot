## Sobre
O projeto é um curso que ensina os fundamentos do Spring Boot.

## Conteúdo do curso
* Implementando uma aplicação web
* Criando uma API Rest
* Conhecendo o Actuator
* Múltiplos servidores embutidos
* Desenvolvendo um microserviço
    * Comunicação com Feign Client
    * Discovery Register
    * API Gateway

## Tecnologias
As seguintes tecnologias foram utilizadas neste projeto:

* [Java Oracle](https://www.oracle.com/java/)
* [Apache Maven](https://maven.apache.org/)
* [Spring Boot](https://spring.io/projects/spring-boot)
* [Spring Cloud OpenFeign](https://spring.io/projects/spring-cloud-openfeign)
* [Spring Cloud Netflix Eureka](https://spring.io/projects/spring-cloud-netflix)
* [Spring Cloud Gateway](https://spring.io/projects/spring-cloud-gateway)
* [Spring Tools Suite](https://spring.io/tools)

### Testando o projeto
**Passo 1:** Iniciar os serviços usando o STS ou pelo Maven na linha de comando
* eurekaserver
* gatewayserver
* employee
* payslip
* payroll

**Passo 2:** Verificar os serviços usando o dashboard do Eureka

```
http://localhost:8761
```

**Passo 3:** Inserindo um funcionário

```
curl --location --request POST 'http://localhost:8888/employee' \
--header 'Content-Type: application/json' \
--data-raw '{
    "name": "Fulano da Silva",
    "email": "fulano@yahoo.com.br",
    "salary": 3000.00
}'
```

**Passo 4:** Calculando a folha de pagamento

```
curl --location --request GET 'http://localhost:8888/payroll'
```

## Licença
Este projeto está sob licença do MIT. Para mais detalhes, ver o arquivo LICENSE.

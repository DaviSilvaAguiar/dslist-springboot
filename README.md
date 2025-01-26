DSList is a backend project developed during the Spring Boot intensive course by Professor Nélio Alves. This project aims to list games, store them in a database, and provide an API for data queries and manipulation.

Technologies Used

Java: Main language of the project.

Spring Boot: Framework for building Java applications.

PostgreSQL: Database used for storage.

Docker: Tool for containerizing the database.

Postman: Tool for API testing.

Features

Listing games.

Storing game information in the database.

Querying games through REST endpoints.

Organizing games into lists.

How to Run the Project

Prerequisites

Before starting, make sure you have installed on your machine:

Java JDK 17 or higher.

Maven for dependency management.

Docker to run the PostgreSQL database.

Postman or another tool for API testing (optional).

Steps to Execute

Clone the repository:

git clone https://github.com/DaviSilvaAguiar/dslist-springboot
cd dslist

Start the PostgreSQL database using Docker:

docker run --name dslist-postgres -e POSTGRES_USER=your_user -e POSTGRES_PASSWORD=your_password -e POSTGRES_DB=dslist -p 5432:5432 -d postgres

Configure the application.properties file:
In the src/main/resources directory, set the PostgreSQL credentials:

spring.datasource.url=jdbc:postgresql://localhost:5432/dslist
spring.datasource.username=your_user
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

Build and run the project:

./mvnw spring-boot:run

Test the API endpoints:
Use Postman or another tool to send requests to the project endpoints.

Project Structure

src/main/java: Contains the main source code of the project.

src/main/resources: Configuration files and scripts.

docker-compose.yml (if applicable): File for automating Docker services.

Available Endpoints

GET /games: Returns the list of games.

GET /games/{id}: Returns details of a specific game.

POST /games: Adds a new game.

PUT /games/{id}: Updates game information.

DELETE /games/{id}: Removes a game.

Author

Developed by Davi Aguiar da Silva.

License

This project is licensed under the MIT License. See the LICENSE file for more details.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

DSList é um projeto backend desenvolvido durante o intensivo de Spring Boot do professor Nélio Alves. Este projeto tem como objetivo listar jogos, armazená-los em um banco de dados e disponibilizar uma API para consultas e manipulação de dados.

Tecnologias Utilizadas

Java: Linguagem principal do projeto.

Spring Boot: Framework para criação de aplicações Java.

PostgreSQL: Banco de dados utilizado para armazenamento.

Docker: Ferramenta para conteinerização do banco de dados.

Postman: Ferramenta para testes da API.

Funcionalidades

Listagem de jogos.

Armazenamento de informações sobre jogos no banco de dados.

Consulta de jogos através de endpoints REST.

Organização de jogos em listas.

Como Executar o Projeto

Pré-requisitos

Antes de iniciar, certifique-se de ter instalado em sua máquina:

Java JDK 17 ou superior.

Maven para gerenciamento de dependências.

Docker para executar o banco de dados PostgreSQL.

Postman ou outra ferramenta para testes de API (opcional).

Passos para Executar

Clone o repositório:

git clone https://github.com/DaviSilvaAguiar/dslist-springboot
cd dslist

Suba o banco de dados PostgreSQL usando Docker:

docker run --name dslist-postgres -e POSTGRES_USER=seu_usuario -e POSTGRES_PASSWORD=sua_senha -e POSTGRES_DB=dslist -p 5432:5432 -d postgres

Configure o arquivo application.properties:
No diretório src/main/resources, configure as credenciais do PostgreSQL:

spring.datasource.url=jdbc:postgresql://localhost:5432/dslist
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

Compile e execute o projeto:

./mvnw spring-boot:run

Teste os endpoints da API:
Utilize o Postman ou outra ferramenta para enviar requisições para os endpoints do projeto.

Estrutura do Projeto

src/main/java: Contém o código fonte principal do projeto.

src/main/resources: Arquivos de configuração e scripts.

docker-compose.yml (se aplicável): Arquivo para automação de serviços Docker.

Endpoints Disponíveis

GET /games: Retorna a lista de jogos.

GET /games/{id}: Retorna detalhes de um jogo específico.

POST /games: Adiciona um novo jogo.

PUT /games/{id}: Atualiza informações de um jogo.

DELETE /games/{id}: Remove um jogo.

Autor

Desenvolvido por Seu Nome.

Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo LICENSE para mais informações.


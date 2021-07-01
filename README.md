:spiral_calendar: Atualizado em 27 de Maio de 2021 

<img align="right" alt="GIF" height="160px" src="https://github.com/rdeconti/rdeconti-resources/blob/main/Digital%20Innovation%20One%20-%20Logotipo.png" />

# Projeto Digital Innovation One Java
# Desenvolvimento de testes unitários para validar uma API REST de gerenciamento estoques de cerveja
- Este projeto foi proposto pela Digital Innovation One - Link do código original: https://github.com/rpeleias/beer_api_digital_innovation_one
- Professor: Rodrigo Peleias 
- Aulas: https://web.digitalinnovation.one/lab/desenvolvimento-de-testes-unitarios-para-validar-uma-api-rest-de-gerenciamento-estoques-de-cerveja/learning/d00f891f-65bb-4149-85f0-57d771116214

# Descrição
Nesta live coding, vamos aprender a testar, unitariamente, uma API REST para o gerenciamento de estoques de cerveja. Vamos desenvolver testes unitários para validar o nosso sistema de gerenciamento de estoques de cerveja, e também apresentar os principais conceitos e vantagens de criar testes unitários com JUnit e Mockito. Além disso, vamos também mostrar como desenvolver funcionalidades da nossa API através da prática do TDD. Durante a sessão, serão abordados os seguintes tópicos:

- Baixar um projeto através do Git para desenolver nossos testes unitários
- Apresentação conceitual sobre testes: a pirâmide dos tipos de testes, e também a importância de cada tipo de teste durante o ciclo de desenvolvimento.
- Foco nos testes unitários: mostrar o porque é importante o desenvolvimento destes tipos de testes como parte do ciclo de desenvolvimento de software.
- Principais frameworks para testes unitários em Java: JUnit, Mockito e Hamcrest
- Desenvolvimento de testes unitários para validação de funcionalides básicas: criação, listagem, consulta por nome e exclusão de cervejas.
- TDD: apresentação e exemplo prático em 2 funcionaliades importantes: incremento e decremento do número de cervejas no estoque.

# Detalhes obtidos nas aulas
- Projeto criado com Spring Boot
- Tem arquivo porn.xml que tem todas as dependências do projeto
- Utiliza Swager para documentar a API
- Utiliza Lombok
- Entity: Beer com classe e atributos, anotações do Lombok gerando automaticamente os gets and sets
- Enums: Tem os tipos de cerveja possíveis
- Repository: Tem o DAO - trabalha com BD e tem interface que procura cervejas por nome

# Para executar o projeto
- Para executar o projeto no terminal, digite o seguinte comando:

        ```shell script
        mvn spring-boot:run 
        ```

        Para executar a suíte de testes desenvolvida durante a live coding, basta executar o seguinte comando:

        ```shell script
        mvn clean test
        ```

        Após executar o comando acima, basta apenas abrir o seguinte endereço e visualizar a execução do projeto:

        ```
        http://localhost:8080/api/v1/beers
        ```

# Dados da API
| Method | URI                          | Description                          |
| :------|:-----------------------------|:-------------------------------------|
| GET    | /api/v1/beers                | List all beers                       |
| POST   | /api/v1/beers                | Create a beer                        |
| PUT    | /api/v1/beers/{id}           | Update a beer                        |
| GET    | /api/v1/beers/{id}           | Return a beer by the given id        |
| DELETE | /api/v1/beers/{id}           | Delete a beer by the given id        |
| PATCH  | /api/v1/beers/{id}/decrement | Decrement the beer quantity in stock |
| PATCH  | /api/v1/beers/{id}/increment | Increment the beer quantity in stock |
| GET    | /api/v1/beers/name/{name}    | Return a beer by the given name      |
| DELETE | /api/v1/beers/name/{name}    | Delete a beer by the given name      |

# Configurações padrão
- Porta padrão `8080`, para alterar:
  - modificar `application.yml` or
  - adicionar:
    `-Dserver.port=8083` ou `--server.port=8083`
- acessar `/swagger-ui` para visualização ou testes manuais.
- acessar `/h2` para base de dados via console.

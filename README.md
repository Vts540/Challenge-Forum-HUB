# Challenge-Forum-HUB
Forum Hub API
Este projeto é uma aplicação REST desenvolvida em Java utilizando Spring Boot. O Forum Hub simula a funcionalidade de um fórum educacional para a conclusão do Challenge Alura de um Fórum onde usuários podem criar tópicos para tirar dúvidas e interagir em um ambiente organizado por cursos.
Funcionalidades
1.	Gerenciamento de Usuários:
o	Cadastro de usuários.
o	Autenticação e segurança utilizando tokens JWT.
2.	Gerenciamento de Cursos:
o	Registro de cursos associados a tópicos.
3.	Gerenciamento de Tópicos:
o	Criação de tópicos vinculados a cursos e usuários.
o	Atualização e exclusão de tópicos com base em permissões.
o	Listagem de todos os tópicos ou tópicos específicos por ID.
Tecnologias Utilizadas
•	Java 17
•	Spring Boot 3
o	Spring Data JPA
o	Spring Security
o	Spring Web
•	Banco de Dados H2 (para desenvolvimento e testes)
•	Maven
•	Lombok (para redução de boilerplate code)
Estrutura do Projeto
A aplicação está organizada nos seguintes pacotes principais:
1.	com.vts540.forum.domain: Entidades principais como User, Course e Topic.
2.	com.vts540.forum.controller: Controladores REST para gerenciar endpoints.
3.	com.vts540.forum.infra.exception: Manipuladores de exceções personalizados.
Como Executar
Requisitos:
•	Java 17 ou superior.
•	Maven.
Passos:
1.	Clone o repositório:
git clone https://github.com/vts540/forum-hub.git
2.	Navegue até o diretório do projeto:
cd forum-hub
3.	Compile e inicie a aplicação:
mvn spring-boot:run
4.	Acesse a API via http://localhost:8080.
Endpoints Principais
Autenticação
•	POST /auth/login
o	Autentica um usuário e retorna um token JWT.
Usuários
•	POST /users
o	Cria um novo usuário.
Cursos
•	GET /courses
o	Lista todos os cursos.
•	POST /courses
o	Cria um novo curso.
Tópicos
•	GET /topics
o	Lista todos os tópicos.
•	GET /topics/{id}
o	Busca um tópico pelo ID.
•	POST /topics
o	Cria um novo tópico (necessita autenticação).
•	PUT /topics/{id}
o	Atualiza um tópico existente (autenticado como autor).
•	DELETE /topics/{id}
o	Exclui um tópico existente (autenticado como autor).
Configuração de Banco de Dados
Por padrão, a aplicação utiliza o banco de dados H2 em memória. Você pode acessar o console do H2 em http://localhost:8080/h2-console com as seguintes credenciais:
•	JDBC URL: jdbc:h2:mem:testdb
•	Usuário: sa
•	Senha: (vazia)
Testes
A aplicação inclui testes unitários e de integração utilizando o JUnit e o Spring Boot Test. Para executar os testes:
mvn test
Licença
Este projeto está licenciado sob a MIT License.

Caso tenham alguma sugestão de melhoria ou possam me ajudar, ficarei extremamente grato. 

# json-server-base

### URL BASE : https://hopebr.herokuapp.com


Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Projetos Front-end.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.


### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### ROTAS QUE NECESSITAM DE AUTORIZAÇÃO!

 ### Listar Todos os Usuarios/Posts/Donations:

GET /users?_embed=donations&_embed=posts - RETORNA TODOS OS USUARIOS COM SEUS POSTS E DOAÇÕES

GET /donations?_expand=user - RETORNA TODAS AS DOAÇÕES COM O DONO DAQUELA DOAÇÃO

GET /posts?_expand=user - RETORNA TODAS OS POSTS COM O DONO DAQUELE POST

### Listar um Usuario/Posts/Donations especifico:

GET /users/id?_embed=donations&_embed=posts - RETORNA UM USUARIO ESPECIFICO

GET /donations/id?_expand=user - RETORNA UMA DOAÇÃO ESPECIFICA

GET /posts/id?_expand=user - RETORNA UM POST ESPECIFICO





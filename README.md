#  Spring JWT
## Exemplo de Aplicação REST com Spring - JWT - HSQLDB - Swagger
- Se preferir mude os dados de conexão no banco no arquivo **application.properties**
- Execute a classe **WebApiApplication**;
- Para exibir a documentação com Swagger, no navegador digite [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html) 
- Com o Swagger cadastre duas roles (ADMIN e USER) e em seguida um Usuario, pois as consultas precisam de autenticação com usuario com role ADMIN

- Se estiver usando o banco H2 em modo console http://localhost:8080/h2-console. Cadastre as roles e usuarios ADMIN e USER
>INSERT INTO TB_ROLE VALUES('ADMIN');
INSERT INTO TB_ROLE VALUES('USER');
INSERT INTO TB_USUARIO (LOGIN,EMAIL,NOME,SENHA) VALUES('admin','admin@admin.com.br','ADMINISTRADOR','$2a$10$HN3O4beErqfsQhZHp/nqYuGXd0yLvP2ffy0BgMTs6f4GKbdhL4QCm');
INSERT INTO TB_USUARIO (LOGIN,EMAIL,NOME,SENHA) VALUES('user','user@user.com.br','USUARIO','$2a$10$vgFCnsBOTdYAZaO4u.Iq6.u869NriIYAznjv4XORIi0CyceDfjQmS');
INSERT INTO TB_USER_ROLES (LOGIN,NOME) VALUES('admin','ADMIN');
INSERT INTO TB_USER_ROLES (LOGIN,NOME) VALUES('user','USER');

* USUARIO ADMIN

> {
  "email": "admin@admin.com.br",
  "login": "admin",
  "nome": "ADMINISTRADOR",
  "roles": [
    {
      "nome": "ADMIN"
    }
  ],
  "senha": "admin"
}

* USUARIO USER
> {
  "email": "user@user.com.br",
  "login": "user",
  "nome": "USUARIO",
  "roles": [
    {
      "nome": "USER"
    }
  ],
  "senha": "user"
}

![Swagger](https://github.com/digytal/spring-jwt-db-rest-api/blob/master/src/main/resources/api.JPG)


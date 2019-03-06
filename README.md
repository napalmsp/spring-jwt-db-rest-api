#  Spring JWT
## Exemplo de Aplicação REST com Spring - JWT - HSQLDB - Swagger
- Se preferir muda os dados de conexão no banco no arquivo **application.properties**
- Execute a classe **WebApiApplication**;
- Para exibir a documentação com Swagger, no navegador digite [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html) 
- Com o Swagger cadastre duas roles (ADMIN e USER) e em seguida um Usuario, pois as consultas precisam de autenticação com usuario com role ADMIN
{
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


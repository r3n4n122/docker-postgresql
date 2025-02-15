# DOCKER COM POSTGRES

> Este projeto tem como objetivo estudar postgresql utilizando docker compose.

### Conectando no pgAdmin:

Depois de clonar o projeto, basta dar um docker compose up para buildar e subir as imagens.

Após o docker baixar e subir a imagem, você consegue acessar a pagina do PGadmin, basta utilizar a seguinte url ```http://localhost:8000```.

No nosso arquivo ```docker-compose.yml``` temos as configurações de acesso do PGadmin e do nosso banco Postgres:

### Acessando PGadmin

Ao acessar a URL ```http://localhost:8000```, você visualizará o campo email e senha e preencherá com as seguintes credenciais:

```
PGADMIN_DEFAULT_EMAIL: user@postgres.com
PGADMIN_DEFAULT_PASSWORD: postgres
```

### Acessando PostgresSQL

Após se logar no pgadmin, você deve localizar no canto superior esquerdo um arquivo chamado ```service```
- Clicar com lado direto do mouse
- Register > Server
- Adiconar o nome do DB que no ```docker-compose.yml``` especifica. No caso seria: ```POSTGRES_DB: postgres```
- Acessar a aba ```connection```
- Campo ```Host``` é preenchido com o ip da internet.
- UserName e Password você localiza no ```docker-compose.yml```. No caso seria:
```
POSTGRES_USER: postgres
POSTGRES_PASSWORD: postgres
```

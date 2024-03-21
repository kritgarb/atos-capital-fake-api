# JSONServer + JWT Auth

Uma API REST fake usando json-server com autenticação JWT.

End-points implementados: login, register

## Install

```bash
$ npm install
$ npm run start-auth
```

Pode ser necessário rodar
```
npm audit fix
```

## Rodando a API no modo restrito

Execute o comando
```
node server.js
```

## Como fazer login/registrar?

Você pode fazer login/registrar enviando uma solicitação POST para

```
POST http://localhost:8000/auth/login
POST http://localhost:8000/auth/register
```
com os seguintes dados 

```
{
  "email": "seuemail@email.com",
  "password":"bestPassword"
}
```

Você deverá receber um token de acesso com o seguinte formato

```
{
   "access_token": "<ACCESS_TOKEN>"
}
```


Você deve enviar esta autorização com qualquer solicitação aos endpoints protegidos

```
Authorization: Bearer <ACCESS_TOKEN>
```

API baseada na API do techiediaries.
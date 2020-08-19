# konzertmeister-api
Public API documentation of the Konzertmeister platform

## Authentication and General Headers

After a succesful login call the access-token has to be sent as Authorization Header

> Authorization: Bearer token_value

> KM_CLIENT_VERSION: V_3_1

> KM_CLIENT_TYPE: 3RD_PARTY


## Login

> `POST /api/v2/login`


Input Content-Type `application/json`
----

```json
{
  "locale": "string",
  "mail": "string",
  "password": "string", -- Hash of the password SHA-1
  "timezoneId": "string"
}
```

Repsonse

Headers:

> X-AUTH-TOKEN: the access-token that has to get passed to all call as Authorization Header


----

```json
{
  "id": 0,
  "locale": "string",
  "mail": "string",
  "name": "string",
  "timezoneId": "string",
}
```


# User API Spec

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "wahyudi",
  "password": "password",
  "name": "Adi Wahyudi"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "wahyudi",
    "name": "Adi Wahyudi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username must not blank, ..."
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "wahyudi",
  "password": "password"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "wahyudi",
    "name": "Adi Wahyudi",
    "token": "uuid"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username or password wrong, ..."
}
```

## Get User

Endpoint : GET /api/users/current

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "username": "wahyudi",
    "name": "Adi Wahyudi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

## Update User

Endpoint : PATCH /api/users/current

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "password": "password", // optional
  "name": "Adi Wahyudi" // optional
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "wahyudi",
    "name": "Adi Wahyudi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

## Logout User

Endpoint : DELETE /api/users/current

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": "OK"
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

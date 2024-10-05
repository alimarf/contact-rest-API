# User API Spec

## Register User

Endpoint : POST /api/users

Request Body:

```json
{
  "username": "john",
  "password": "secret",
  "name": "john doe"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "john",
    "name": "john doe"
  }
}
```

Response Body (Success):

```json
{
  "errors": "Username already registered"
}
```

## Login User

Endpoint : POST /api/users/login

Request Body:

```json
{
  "username": "john",
  "password": "secret",
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "john",
    "name": "john doe",
    "token": "bearer token"
  }
}
```

Response Body (Success):

```json
{
  "errors": "Username or password is wrong"
}
```

## Get User

Endpoint : POST /api/users/current


## Update User

## Logout User

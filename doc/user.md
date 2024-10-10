User

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

Response Body (Failed):

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

Response Body (Failed):

```json
{
  "errors": "Username or password is wrong"
}
```

## Get User

Endpoint : GET /api/users/current

Headers :
- authorization: token

Response Body (Success):

```json
{
  "data": {
    "username": "john",
    "name": "john doe",
  }
}
```

Response Body (Failed):

```json
{
  "errors": "Unauthorized"
}
```

## Update User

Endpoint : PATCH /api/users/current

Headers :
- Authorization: token

Request Body:

```json
{
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

## Logout User

Endpoint : DELETE /api/users/current

Headers :
- Authorization: token

Response Body (Success):

```json
{
  "data": true
}
```


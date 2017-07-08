# Users

## Get Users
> Sample JSON structured response:

```javascript
{
    "users": [
        {
            "id": 1,
            "username": "income",
            "name": "Ignatius Ukwuoma",
            "email": "ignatius@andela.com",
            "roleId": 1
        },
        {
            "id": 2,
            "username": "moe",
            "name": "Mark Edomwande",
            "email": "moe@andela.com",
            "roleId": 2
        },
        {
            "id": 3,
            "username": "haroun",
            "name": "Haruna Popoola",
            "email": "haroun@andela.com",
            "roleId": 3
        },
    ],
    "pageData": {
        "count": 3,
        "pageSize": 3,
        "pageNumber": 1,
        "totalPages": 1
    }
}
```

### Request
- Endpoint: GET: `/users`
- Requires: Authentication

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
limit | 9 | Sets the limit.
offset | 0 | Sets the offset.

### Response
- Status: `200: OK`
- Body `(application/json)`



## Create User

> Request:

```javascript
{
    "username": "neji",
    "name": "Adebayo Adesanya",
    "email": "bayo@andela.com",
    "password": "password"
}
```

> Response:

```javascript
{
    "message": "User is successfully created",
    "user": {
        "id": 39,
        "username": "neji",
        "name": "Adebayo Adesanya",
        "email": "bayo@andela.com",
        "roleId": 3
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7ImlkIjozOSwibmFtZSI6IkFkZWJheW8gQWRlc2FueWEiLCJ1c2VybmFtZSI6Im5lamkiLCJlbWFpbCI6ImJheW9AYW5kZWxhLmNvbSIsInJvbGVJZCI6M30sImlhdCI6MTQ5ODI0MTE3MywiZXhwIjoxNDk4NDEzOTczfQ.rgEJhwIGZvP-C1KTZpDwDKkMbvdR3e29djWphG4XgQA"
}
```

### Request
- Endpoint: POST: `/users`
- Body `(application/json)`


### Response
- Status: `201: Created`
- Body `(application/json)`


## Get User

> Response:

```javascript
{
    "id": 39,
    "name": "Adebayo Adesanya",
    "username": "neji",
    "email": "bayo@andela.com",
    "roleId": 3
}
```

### Request
- Endpoint: GET: `/users/:id`
- Requires: Authentication by User or Admin

### Response
- Status: `200: OK`
- Body `(application/json)`


## Update User

> Request:

```javascript
{
  "username": "nejie",
}
```

> Response:

```javascript
{
    "id": 39,
    "name": "Adebayo Adesanya",
    "username": "nejie",
    "email": "bayo@andela.com",
    "roleId": 3
}
```

### Request
- Endpoint: PUT: `/users/:id`
- Requires: Authentication by User or Superadmin
- Body `(application/json)`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Delete User

> Response:

```javascript
{
    message: 'Deleted successfully'
}
```

### Request
- Endpoint: DELETE: `/users/:id`
- Requires: Authentication by User or Superadmin

### Response
- Status: `200: OK`
- Body `(application/json)`



## Login User

> Request:

```javascript
{
  "username": "moe",
  "password": "password"
}
```

> Response:

```javascript
{
    "message": "Login successful",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7ImlkIjozNCwibmFtZSI6Ikdvb2RuZXNzIE9yamkiLCJ1c2VybmFtZSI6Imdvb2RuZXNzIiwiZW1haWwiOiJnb29kbmVzc0BnbWFpbC5jb20iLCJyb2xlSWQiOjN9LCJpYXQiOjE0OTgyNDMwNDcsImV4cCI6MTQ5ODQxNTg0N30.OXtkoe9SG_IjJzoMUxCMw1Ecfd41ctKrX4o9W16_WcQ"
}
```

### Request
- Endpoint: POST: `/users/login`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Logout User

> Response:

```javascript
{
    "message": "You have signed out"
}
```

### Request
- Endpoint: POST: `/users/logout`

### Response
- Status: `200: OK`
- Body `(application/json)`



## Get User Documents

> Response:

```javascript
{
    "message": "1 document found",
    "documents": [
        {
            "id": 2,
            "title": "A write up about my country",
            "content": "Nigeria is immensely blessed but",
            "access": "public",
            "createdAt": "2017-06-06T17:14:24.386Z",
            "updatedAt": "2017-06-06T17:14:24.386Z",
            "userId": 2,
            "User": {
                "username": "moe",
                "roleId": 2
            }
        }
    ],
    "pageData": {
        "count": 1,
        "pageSize": 1,
        "pageNumber": 1,
        "totalPages": 1
    }
}
```

### Request
- Endpoint: GET: `/users/:id/documents`
- Requires: Authentication

### Response
- Status: `200: OK`
- Body `(application/json)`

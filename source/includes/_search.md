# Search

## Search Users

> Response:

```javascript
{
    "users": [
        {
            "id": 16,
            "username": "jeddy",
            "name": "Jedidiah Andelanosia",
            "email": "jeddy@andela.com",
            "roleId": 3
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
- Endpoint: GET: `/search/users`
- Requires: Authentication


### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
q | "" | Search query.

### Response
- Status: `200: OK`
- Body `(application/json)`

## Search Documents

> Response:

```javascript
{
    "documents": [
        {
            "id": 1,
            "title": "What I love about Andela Nigeria",
            "content": "Everything... especially the code. So cool.",
            "access": "public",
            "createdAt": "2017-06-06T17:04:54.254Z",
            "updatedAt": "2017-06-06T17:04:54.254Z",
            "userId": 1,
            "User": {
                "username": "income",
                "roleId": 1
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
- Endpoint: GET: `/search/documents`

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
q | "" | Search query.

### Response
- Status: `200: OK`
- Body `(application/json)`
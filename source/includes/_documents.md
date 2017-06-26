# Documents

## Get Documents
> Response:

```javascript
{
    "documents": [
        {
            "id": 5,
            "title": "Lyrics to go",
            "content": "How many times do I have to tell you, even when you crying you're beautiful too",
            "access": "public",
            "createdAt": "2017-06-07T05:08:03.001Z",
            "updatedAt": "2017-06-07T05:08:03.001Z",
            "userId": 4,
            "User": {
                "username": "mai",
                "roleId": 4
            }
        },
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
        },
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
        "count": 3,
        "pageSize": 3,
        "pageNumber": 1,
        "totalPages": 1
    }
}
```

### Request
- Endpoint: GET: `/documents`

### Query Parameters
Parameter | Default | Description
--------- | ------- | -----------
limit | 9 | Sets the limit.
offset | 0 | Sets the offset.

### Response
- Status: `200: OK`
- Body `(application/json)`



## Create Document

> Request:

```javascript
{
  "title": "Hello",
  "content": "Is it me you are looking for?",
  "access": "private"
}
```

> Response:

```javascript
{
    "message": "New document was successfully created",
    "document": {
        "id": 29,
        "title": "Hello",
        "content": "Is it me you are looking for?",
        "access": "private",
        "userId": 34,
        "updatedAt": "2017-06-23T19:15:44.172Z",
        "createdAt": "2017-06-23T19:15:44.172Z"
    }
}
```

### Request
- Endpoint: POST: `/documents`
- Requires: Authentication
- Body `(application/json)`


### Response
- Status: `201: Created`
- Body `(application/json)`


## Get Document

> Response:

```javascript
{
    "id": 29,
    "title": "Hello",
    "content": "Is it me you are looking for?",
    "access": "private",
    "createdAt": "2017-06-23T19:15:44.172Z",
    "updatedAt": "2017-06-23T19:15:44.172Z",
    "userId": 34,
    "User": {
        "username": "goodness",
        "roleId": 3
    }
}
```

### Request
- Endpoint: GET: `/documents/:id`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Edit Document

> Request:

```javascript
{
  "content": "Is it me you are looking for? Hello, how are you doing?"
}
```

> Response:

```javascript
{
    "message": "Document has been updated",
    "updatedDocument": {
        "id": 29,
        "title": "Hello",
        "content": "Is it me you are looking for? Hello, how are you doing?",
        "access": "private",
        "createdAt": "2017-06-23T19:15:44.172Z",
        "updatedAt": "2017-06-23T19:20:07.770Z",
        "userId": 34
    }
}
```

### Request
- Endpoint: PUT: `/documents/:id`
- Requires: Authentication
- Body `(application/json)`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Delete Document

> Response:

```javascript

```

### Request
- Endpoint: DELETE: `/documents/:id`
- Requires: Authentication

### Response
- Status: `204: No Content`
- Body `(application/json)`

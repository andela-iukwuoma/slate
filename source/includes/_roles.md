# Roles

## Get Roles
> Response:

```javascript
[
    {
        "id": 1,
        "title": "superadmin",
        "createdAt": "2017-06-06T17:03:34.384Z",
        "updatedAt": "2017-06-06T17:03:34.384Z"
    },
    {
        "id": 2,
        "title": "admin",
        "createdAt": "2017-06-06T17:07:52.412Z",
        "updatedAt": "2017-06-06T17:07:52.412Z"
    },
    {
        "id": 3,
        "title": "author",
        "createdAt": "2017-06-06T17:08:23.115Z",
        "updatedAt": "2017-06-06T17:08:23.115Z"
    }
]
```

### Request
- Endpoint: GET: `/roles`
- Requires: Superadmin credentials

### Response
- Status: `200: OK`
- Body `(application/json)`



## Create Role

> Request:

```javascript
{
  "title": "editor",
}
```

> Response:

```javascript
{
    "message": "New role successfully created",
    "role": {
        "id": 21,
        "title": "editor",
        "updatedAt": "2017-06-23T19:32:55.127Z",
        "createdAt": "2017-06-23T19:32:55.127Z"
    }
}
```

### Request
- Endpoint: POST: `/roles`
- Requires: Superadmin credentials
- Body `(application/json)`


### Response
- Status: `201: Created`
- Body `(application/json)`


## Update Role

> Request:

```javascript
{
  "title": "writer"
}
```

> Response:

```javascript
{   
    "message": "Role is successfully updated",
    "role": {
        "id": 21,
        "title": "writer",
        "createdAt": "2017-06-23T19:32:55.127Z",
        "updatedAt": "2017-06-23T19:36:02.227Z"
    }
}
```

### Request
- Endpoint: PUT: `/roles/:id`
- Requires: Superadmin credentials
- Body `(application/json)`

### Response
- Status: `200: OK`
- Body `(application/json)`


## Delete Role

> Response:

```javascript
{
    message: 'Deleted successfully'
}
```

### Request
- Endpoint: DELETE: `/roles/:id`
- Requires: Superadmin credentials

### Response
- Status: `200: OK`
- Body `(application/json)`
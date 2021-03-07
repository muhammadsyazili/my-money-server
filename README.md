# API Spec
---
## Transaction
### Create Transaction
Request :
- Method : POST
- Endpoint : `/transaction`
- Authorization : Bearer Token
- Header : 
    - Content-Type : application/json
    - Accept : application/json
- Body :
```json
{
    "title" : "string|required|max_length=255",
    "amount" : "numeric|required",
    "type" : "required|in:expense,revenue"
}
```

Response :
```json
{
    "status" : "integer",
    "message" : "string",
    "data" : {
        "id" : "integer",
        "title" : "string",
        "amount" : "numeric",
        "type" : "string"
    }
}
```

### Get Transaction
Request :
- Method : GET
- Endpoint : `/transaction/{transaction_id}`
- Authorization : Bearer Token
- Header : 
    - Accept : application/json

Response :
```json
{
    "status" : "integer",
    "message" : "string",
    "data" : {
        "id" : "integer",
        "title" : "string",
        "amount" : "numeric",
        "type" : "string"
    }
}
```

### Update Transaction
Request :
- Method : PUT
- Endpoint : `/transaction/{transaction_id}`
- Authorization : Bearer Token
- Header : 
    - Content-Type : application/json
    - Accept : application/json
- Body :
```json
{
    "title" : "string|required|max_length=255",
    "amount" : "numeric|required",
    "type" : "required|in:expense,revenue"
}
```

Response :
```json
{
    "status" : "integer",
    "message" : "string",
    "data" : {
        "id" : "integer",
        "title" : "string",
        "amount" : "numeric",
        "type" : "string"
    }
}
```

### List Transaction
Request :
- Method : GET
- Endpoint : `/transaction`
- Authorization : Bearer Token
- Header : 
    - Accept : application/json

Response :
```json
{
    "status" : "integer",
    "message" : "string",
    "data" : [
        {
            "status" : "integer",
            "message" : "string",
            "data" : {
                "id" : "integer",
                "title" : "string",
                "amount" : "numeric",
                "type" : "string"
            }
        }
    ]
}
```

### Delete Transaction
Request :
- Method : DELETE
- Endpoint : `/transaction/{transaction_id}`
- Authorization : Bearer Token
- Header : 
    - Accept : application/json

Response :
```json
{
    "status" : "integer",
    "message" : "string"
}
```

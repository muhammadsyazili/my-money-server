# API Spec
---
## Transaction
### Create Transaction
Request :
- Method : POST
- Endpoint : `/api/transaction`
- Authorization : Bearer Token
- Header : 
    - Content-Type : application/json
    - Accept : application/json
- Body :
```json
{
    "user_id" : "required|integer",
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
        "user_id" : "integer",
        "title" : "string",
        "amount" : "numeric",
        "type" : "string"
    }
}
```

### Get Transaction
Request :
- Method : GET
- Endpoint : `/api/transaction/{transaction_id}`
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
        "user_id" : "integer",
        "title" : "string",
        "amount" : "numeric",
        "type" : "string"
    }
}
```

### Update Transaction
Request :
- Method : PUT
- Endpoint : `/api/transaction/{transaction_id}`
- Authorization : Bearer Token
- Header : 
    - Content-Type : application/json
    - Accept : application/json
- Body :
```json
{
    "user_id" : "required|integer",
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
        "user_id" : "integer",
        "title" : "string",
        "amount" : "numeric",
        "type" : "string"
    }
}
```

### List Transaction
Request :
- Method : GET
- Endpoint : `/api/transaction`
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
            "id" : "integer",
            "user_id" : "integer",
            "title" : "string",
            "amount" : "numeric",
            "type" : "string"
        }
    ]
}
```

### Delete Transaction
Request :
- Method : DELETE
- Endpoint : `/api/transaction/{transaction_id}`
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

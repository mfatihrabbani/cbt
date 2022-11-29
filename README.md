
## Spesifikasi Api

### Users

#### Register Users

Request :
- Method : POST
- Endpoint : "/api/users/signup"
- Headers : 
    - Content-Type : application/json
    - Accept : application/json

- Body :

```json
{
    "email": "string",
    "password": "string",
    "confirmPassword": "string"
}
```

Response: 
```json
{
    "code": "number",
    "status": "string",
    "data": {
        "message": "string"
    }
}
```

#### Login Users

Request :
- Method : POST
- Endpoint : "/api/users/signin"
- Headers : 
    - Content-Type : application/json
    - Accept : application/json

- Body :

```json
{
    "email": "string",
    "password": "string",
}
```

Response: 
```json
{
    "code": "number",
    "status": "string",
    "data": {
        "token": "string"
    }
}
```



### Ujian Soal

#### POST Ujian Soal

Request :
- Method : POST
- Endpoint : "/api/exam"
- Headers : 
    - Content-Type : application/json
    - Accept : application/json

- Body :

```json
{
    "nameExam": "string",
    "gradeExam": "int",
    "majorExam": "string",
}
```

Response: 
```json
{
    "code": "number",
    "status": "string",
    "data": {
        "nameExam": "string",
        "gradeExam": "int",
        "majorExam": "string",
    }
}
```

#### GET Ujian Soal

Request :
- Method : GET
- Endpoint : "/api/exam/:id"
- Headers :
    - Accept : application/json

Response: 
```json
{
    "code": "number",
    "status": "string",
    "data": {
        "idExam": "string",
        "nameExam": "string",
        "gradeExam": "int",
        "majorExam": "string",
        "question": {
            
        }
    }
}
```
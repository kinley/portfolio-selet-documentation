Phone authorization API description for *portfolio-selet*:

### Endpoint
```
POST
https://api.portfolio-selet.ru/api/v1/login.json
```

### Reques Headers
```
Accept: application/json
Content-Type: application/json
```

### Request Body
```
{
  "phone":"79997771234",
  "pass":"123456"
}
```

#### Params description
`phone` - user phone number with leading 7 and without '+' symbol: `79997771234`  
`pass` - user passwors

### Successful authorization (status `200`)
```
{
  "token":"c25da44eef5c1be725702aa560d49dba0f2c17a0",
  "user": {
    "id": 341,
    "email": "email@domain.com",
    "phone": "79997771234",
    "first_name": "Timur",
    "last_name": "Platonov",
    "patronymic": "Sergeevich",
    "tat_first_name": "",
    "tat_last_name": "",
    "tat_patronymic": "",
    "gender": "M",
    "birthday": "1995-08-19T00:00:00Z",
    "year": "2016",
    "avatar": {
      "url": "https://api.portfolio-selet.ru/uploads/user/avatar/341/12c167ac-95fa-4ce3-8f5a-19e0499a636c.jpg",
      "thumb_url": "https://api.portfolio-selet.ru/uploads/user/avatar/341/thumb_12c167ac-95fa-4ce3-8f5a-19e0499a636c.jpg"
    }, 
    "places": [
      {
        "id": 3,
        "place_name": "KFU"
      }
    ]
  }
}
```

### Errors
```
{
  "error":"error message"
}
```

- Any request param is required. If any param is absent: status `400`
- Phone number format is wrong: status `400`
- Wrong phone or pass: status `401`

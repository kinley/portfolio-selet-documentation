User show API:

### Endpoint
```
GET
https://api.portfolio-selet.ru/api/v1/users/[:id].json
```

### Request Headers
```
Accept: application/json
Auth-Token: 221f39dfaedea2ee8e0512696ffd2a9b4bf5d620
```

`Auth-Token` - токен аутентификации, который можно получить, выполнив вход в платформу *portfolio-selet*  
`Auth-Token` - authentication token, received while authentication on *portfolio-selet*  

### User show success response (status `200`)
```
{
  "user": {
    "id": 341,
    "first_name": "Timur",
    "last_name": "Platonov",
    "gender": "M",
    "year": 2016,
    "avatar": {
      "url": "https://api.portfolio-selet.ru/uploads/user/avatar/341/12c167ac-95fa-4ce3-8f5a-19e0499a636c.jpg",
      "thumb_url": "https://api.portfolio-selet.ru/uploads/user/avatar/341/thumb_12c167ac-95fa-4ce3-8f5a-19e0499a636c.jpg"
    }
  }
}
```

### Errors
```
{
  "error":"error message"
}
```

- Token is wrong or absent: status `401`
- User not found: status `404`     


# USERS API ENDPOINTS

## User Registration


### Creating a user.

### Request : 

```json
  { 
  "user" : {
    "email":"rajeev@gmail.com",
    "password":"vBh12##",
    "password_confirmation" : "vBh12##",
    "username": "rShetty"
    }
  }
```

### Response :

```json
  {
  "status": "success",
  "data": {
    "user": {
    "id": 32,
    "auth_token": "c687865a26c83fbb0d030058e432852336d004c8"
    }
   }
  }
```

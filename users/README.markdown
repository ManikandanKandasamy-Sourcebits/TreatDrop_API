# USERS API ENDPOINTS

## 1. User Registration

##### Endpoint :   /api/v1/users
##### Method   :   POST
##### Description: Creating a user.

### Request : 

```json
  { 
  "user" : {
    "email":"rajeev@gmail.com",
    "password":"vBh12##@",
    "password_confirmation" : "vBh12##@",
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

## 2. User Sign In

##### Endpoint :   /api/v1/users/sign_in
##### Method   :   POST
##### Description: Signing in a user.

### Request : 

```json
  {
  "user" : {
    "email":"rajeev@gmail.com",
    "password":"vBh12##@"
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
        "auth_token": "dadee8f52aec2b8cff3e9fb67bebcc8d77edfe1f"
        }
      }
  }
```

## 3. Follow a User

##### Endpoint :   api/v1/users/follow?auth_token=
##### Method   :   POST
##### Description: Follow a User.

### Request :

```json
  {
    "follow_id" : 29
  }
```

### Response :

```json
    {
    "status": "success",
    "data": {
        "follow": {
            "id": 12,
            "followable_id": 29,
            "follower_id": 32,
            "followable_type": "User",
            "follower_type": "User"
        }
      }
    }
```






   



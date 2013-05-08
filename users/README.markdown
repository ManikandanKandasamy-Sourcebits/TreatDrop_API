# USERS API ENDPOINTS

## 1. User Registration

##### Endpoint :  `/api/v1/users`
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

##### Endpoint :   `/api/v1/users/sign_in`
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

##### Endpoint :   `api/v1/users/follow?auth_token=`
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

## 4. UnFollow a User

##### Endpoint :   `api/v1/users/unfollow?auth_token=`
##### Method   :   POST
##### Description: UnFollow a User.

### Request :

```json
  {
    "unfollow_id" : 29
  }
```

### Response :

```json
    {
    "status": "success",
    "data": {
        "unfollow": {
            "id": 12,
            "followable_id": 29,
            "follower_id": 32,
            "followable_type": "User",
            "follower_type": "User"
        }
      }
    }
```

## 5. Get the Followers of User

##### Endpoint :   `api/v1/users/followers?auth_token=`
##### Method   :   POST
##### Description: Get the Followers of a User.

### Request : 

```json
  {
    "user_id" : 29
  }
```

### Response :

```json

    {
    "status": "success",
    "data": {
        "users": [
            {
                "id": 32,
                "username": "rajeev",
                "email": "teja@gmail.com"
            },
            {
                "id": 36,
                "username": "sanjeev",
                "email": "roja@gmail.com"
            }
          ]
        }
     }
```

## 6. Get the Followings of a User

##### Endpoint :   `api/v1/users/following?auth_token=`
##### Method   :   POST
##### Description: Get the Followings of a User.

### Request : 

```json
  {
    "user_id" : 32
  }
```

### Response :

```json
    {
    "status": "success",
    "data": {
        "follows": [
            {
                "id": 13,
                "followable_id": 29,
                "followable_type": "User",
                "follower_id": 32,
                "follower_type": "User"
            },
            {
                "id": 14,
                "followable_id": 28,
                "followable_type": "User",
                "follower_id": 32,
                "follower_type": "User"
            }
         ]
      }
    } 
```

## 6. Block a User

##### Endpoint :   `/api/v1/users/block?auth_token=`
##### Method   :   POST
##### Description: Block a User.

### Request :

```json
  {
    "user_id" : 32
  }
```

### Response :

```json 
   {
    "status": "success",
    "data": {
        "user": {}
     }
   } 
```

## 7. Get the User Information

##### Endpoint :   `/api/v1/users/:id?auth_token=`
##### Method   :   GET
##### Description: Get the Information of a User.

### Request : `/api/v1/users/1?auth_token=`

### Response : 

```json
    {
    "status": "success",
    "data": {
        "user": {
            "id": 29,
            "email": "rajeev@gmail.com",
            "first_name" : "Rajeev"
            "last_name": "Bharshetty",
            "username": "rShetty"
        }
      }
    }
```
















   



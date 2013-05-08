# Brands API EndPoints


## 1. List All Brands

##### Endpoint :  `/api/v1/brands?auth_token=`
##### Method   :   GET
##### Description: Get a List of all brands.

### Request : `{BASE_URL}/api/v1/brands?auth_token=`

### Response : 

```json
    {
    "status": "success",
    "data": {
        "brands": [
            {
                "id": 73,
                "name": "Cocacola"
            },
            {
                "id": 74,
                "name": "Pepsi"
            }
          ]
        }
    }
```


## 2. Follow a Brand

##### Endpoint :   `api/v1/brands/follow?auth_token=`
##### Method   :   POST
##### Description: Follow a Brand.

### Request :

```json
  {
    "follow_id" : 89
  }
```

### Response :

```json
   {
    "status": "success",
    "data": {
        "follow": {
            "id": 17,
            "followable_id": 89,
            "follower_id": 32,
            "followable_type": "Brand",
            "follower_type": "User"
        }
     }
   }
```

## 3. UnFollow a Venue

##### Endpoint :   `api/v1/brands/unfollow?auth_token=`
##### Method   :   POST
##### Description: UnFollow a Brand.

### Request :

```json
  {
    "unfollow_id" : 89
  }
```

### Response :

```json
   {
    "status": "success",
    "data": {
        "unfollow": {
            "id": 17,
            "followable_id": 89,
            "follower_id": 32,
            "followable_type": "Brand",
            "follower_type": "User"
        }
     }
   }
```

## 4. Get the Followers of a Brand

##### Endpoint :   `api/v1/brands/followers?auth_token=`
##### Method   :   POST
##### Description: Get the Followers of a Brand.

### Request : 

```json
  {
    "brand_id" : 29
  }
```

### Response :

```json

   {
    "status": "success",
    "data": {
        "users": [
            {
                "id": 28,
                "username": "suraj0589",
                "email": "suraj0589@gmail.com"
            },
            {
                "id": 26,
                "username": "rShetty",
                "email": "rajeevrv@gmail.com"
            },
            {
                "id": 32,
                "username": "rajeev",
                "email": "race@gmail.com"
            }
         ]
       }
    }
```

## 5. Information of a Brand

##### Endpoint :   `/api/v1/brands/:id?auth_token=`
##### Method   :   GET
##### Description: Get the Information of a Venue.

### Request : `{BASE_URL}/api/v1/brands/89?auth_token=`

### Response :

```json
    {
    "status": "success",
    "data": {
        "brand": {
            "id": 89,
            "name": "Coca-Cola"
        }
      }
    }
```











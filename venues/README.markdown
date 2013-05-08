# Venues API EndPoints


## 1. List All Venues

##### Endpoint :  `/api/v1/venues?auth_token=`
##### Method   :   GET
##### Description: Get a List of all venues.

### Request : `{BASE_URL}/api/v1/venues?auth_token=`

### Response : 

```json

    {
    "status": "success",
    "data": {
        "venues": [
            {
                "id": 2,
                "venue_name": "ATest",
                "venue_address": "das"
            },
            {
                "id": 14,
                "venue_name": "S",
                "venue_address": "AAA"
            }
          ]
       }
    }
```


## 2. Get Venues within a Radius (miles)

##### Endpoint :  `/api/v1/venues/search?auth_token=`
##### Method   :   GET
##### Description: Get a List of all venues.

### Request : 
##### `{BASE_URL}/api/v1/venues/search?lat=51.2&lng=-0.0013&dist=100?auth_token=`

### Response : 

```json

    {
    "status": "success",
    "data": {
        "venues": [
            {
                "id": 2,
                "venue_name": "ATest",
                "venue_address": "das"
            },
            {
                "id": 14,
                "venue_name": "S",
                "venue_address": "AAA"
            }
          ]
       }
    }
```

## 3. Follow a Venue

##### Endpoint :   `api/v1/venues/follow?auth_token=`
##### Method   :   POST
##### Description: Follow a Venue.

### Request :

```json
  {
    "follow_id" : 163
  }
```

### Response :

```json
   {
    "status": "success",
    "data": {
        "follow": {
            "id": 15,
            "followable_id": 163,
            "follower_id": 32,
            "followable_type": "Venue",
            "follower_type": "User"
        }
     }
   }
```

## 4. UnFollow a Venue

##### Endpoint :   `api/v1/venues/unfollow?auth_token=`
##### Method   :   POST
##### Description: UnFollow a Venue.

### Request :

```json
  {
    "unfollow_id" : 163
  }
```

### Response :

```json
    {
    "status": "success",
    "data": {
        "unfollow": {
            "id": 15,
            "followable_id": 163,
            "follower_id": 32,
            "followable_type": "Venue",
            "follower_type": "User"
        }
      }
    }
```

## 5. Get the Followers of a Venue

##### Endpoint :   `api/v1/venues/followers?auth_token=`
##### Method   :   POST
##### Description: Get the Followers of a User.

### Request : 

```json
  {
    "venue_id" : 29
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









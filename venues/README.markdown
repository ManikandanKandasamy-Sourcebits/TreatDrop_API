# Venues API EndPoints


## 1. List All Venues

##### Endpoint :  `{BASE_URL}/api/v1/venues?auth_token=`
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

##### Endpoint :  `{BASE_URL}/api/v1/venues/search?auth_token=`
##### Method   :   GET
##### Description: Get a List of all venues.

### Request : `{BASE_URL}/api/v1/venues/search?lat=51.2&lng=-0.0013&dist=100?auth_token=`

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







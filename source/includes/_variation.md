# Variation
## Variation List

> To get the variation list for a shop, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/variation"
```

```javascript
// to be added
```

```php
<?php
//to be added
```

> A successful response will look like the following

```json
{
  "data": [
    {
      "id": 62,
      "name": "Color",
      "for": "Shirt",
      "variation": [
        {
          "id": 234,
          "name": "white"
        },
        {
          "id": 233,
          "name": "green"
        },
        {
          "id": 232,
          "name": "black"
        },
        {
          "id": 231,
          "name": "red"
        }
      ]
    },
    {
      "id": 61,
      "name": "Size",
      "for": "Pant",
      "variation": [
        {
          "id": 230,
          "name": "xxl"
        },
        {
          "id": 229,
          "name": "xl"
        },
        {
          "id": 228,
          "name": "l"
        },
        {
          "id": 227,
          "name": "m"
        },
        {
          "id": 226,
          "name": "s"
        }
      ]
    },
    {
      "id": 60,
      "name": "Size",
      "for": "Shirt",
      "variation": [
        {
          "id": 225,
          "name": "xxl"
        },
        {
          "id": 224,
          "name": "xl"
        },
        {
          "id": 223,
          "name": "l"
        },
        {
          "id": 222,
          "name": "m"
        },
        {
          "id": 221,
          "name": "s"
        }
      ]
    }
  ]
}
```

Retrive the varation list for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/variation`

### Request Method
`GET`

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Content-Type` | `application/json`
`Accept` | `application/json`

### Request Parameter
none

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Varation Info

> To get a variation info, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/variation/{variation_id}"
```

```javascript
// to be added
```

```php
<?php
//to be added
```
> A successful response will look like the following

```json
{
  "data": {
    "id": 62,
    "name": "Color",
    "for": "Shirt",
    "variation": [
      {
        "id": 234,
        "name": "white"
      },
      {
        "id": 233,
        "name": "green"
      },
      {
        "id": 232,
        "name": "black"
      },
      {
        "id": 231,
        "name": "red"
      }
    ]
  }
}
```

Retrive info for a variation

### End point
`https://apis.avana.asia/v1/mobile/variation/{variation_id}`

### Request Method
`GET`

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Content-Type` | `application/json`
`Accept` | `application/json`

### Request Parameter
none

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
404 | Variation not found | No variation found for the specified variation_id 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Create Variation

> To create a variation, use the following:

```shell
curl -X POST -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/variation"
```

```javascript
// to be added
```

```php
<?php
//to be added
```

> A successful response will look like the following

```json
{
  "data": {
    "id": 62,
    "name": "Color",
    "for": "Shirt",
    "variation": [
      {
        "id": 234,
        "name": "white"
      },
      {
        "id": 233,
        "name": "green"
      },
      {
        "id": 232,
        "name": "black"
      },
      {
        "id": 231,
        "name": "red"
      }
    ]
  }
}
```

Create a variation for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/variation`

### Request Method
`POST`

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Content-Type` | `application/json`
`Accept` | `application/json`

### Request Parameter
Name | Value
--- | ---
`name` | name. Ex: Color
`for` | for. Ex: Shirt
`variation` | comma seperated value. Ex: s,m,l,xl,xxl

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
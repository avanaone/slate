#Shop

## Shop List
> To get shop list of current logged in user, use the following:

```shell
curl -X GET -H "Authorization: Bearer access_token"\
-H "Content-Type: application/json" -H "Accept: application/json"\
"https://apis.avana.asia/v1/mobile/shop"
```

```javascript
// to be added
```

```php
<?php
//to be added
```
> A successful response will look like the following

> With data

```json
{
  "data": [
    {
      "id": 1,
      "name": "Shop name one"
    },
    {
      "id": 2,
      "name": "Shop name two"
    },

  ]
}
```

> Without data

```json
{
  "data": []
}
```

Retrive the shop list for currently logged in user

### End point
`https://apis.avana.asia/v1/mobile/shop`
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

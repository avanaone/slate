#Label

## Label List

> To get label list for a specific shop, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/label"
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
      "name": "New Arrival"
  },
  {
      "id": 2,
      "name": "On Sale"
  }
  ]
}
```

> Without data

```json
{
  "data": []
}
```

Retrive the label list for a specific shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/label`

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

## Label Info

> To get a label info, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/label/{label_id}"
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
      "id": 1,
      "name": "New Arrival"
  }
}
```

Retrive info for a label

### End point
`https://apis.avana.asia/v1/mobile/label/{label_id}`

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
403 | Forbidden | label_id does not belong to current user 
404 | Label not found | No label found for the specified label_id 

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


## Create Label

> To create a label, use the following:

```shell
curl -X POST -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/label"
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
      "id": 3,
      "name": "New label"
  }
}
```

Create a label for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/label`

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
`name` | tax name

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Update Label

> To update a label, use the following:

```shell
curl -X PATCH -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/label/{label_id}"
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
      "id": 3,
      "name": "Updated label"
  }
}
```

Update info for a tax

### End point
`https://apis.avana.asia/v1/mobile/label/{label_id}`

### Request Method
`PATCH`

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Content-Type` | `application/json`
`Accept` | `application/json`

### Request Parameter
Name | Value
--- | ---
`name` | labal name

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
403 | Forbidden | label_id does not belong to current user 
500 | Input cannot be empty, accepted input: {valid_inputs} | Request cannot be empty, needs atleast one input
500 | Invalid input({invalid_inputs}), accepted input: {valid_inputs} | Request needs a valid input

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


## Delete Label

> To delete a labale, use the following:

```shell
curl -X DELETE -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/label/{label_id}"
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
      "delete": true
  }
}
```

Delete a label

### End point
`https://apis.avana.asia/v1/mobile/label/{label_id}`

### Request Method
`DELETE`

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
403 | Forbidden | label_id does not belong to current user 
404 | Label not found | No label found for the specified label_id 

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
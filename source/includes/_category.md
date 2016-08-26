# Category
## Category List

> To get the category list for a shop, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/category"
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
      "id": 1,
      "name": "Baby Hat"
    },
    {
      "id": 2,
      "name": "Baby Shirt"
    }
  ]
}
```

Retrive the category for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/category`

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

## Category Info

> To get a category info, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/category/{category_id}"
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
  "data":{
      "id": 1,
      "name": "Baby Hat"
    }
}
```

Retrive info for a category

### End point
`https://apis.avana.asia/v1/mobile/category/{category_id}`

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
404 | Category not found | No category found for the specified category_id 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Create Category

> To create a category, use the following:

```shell
curl -X POST -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/category"
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
  "data":{
      "id": 1,
      "name": "Baby Hat"
    }
}
```

Create a category for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/category`

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
`name` | category name

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Update Category

> To update a category, use the following:

```shell
curl -X PATCH -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/category/{category_id}"
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
  "data":{
      "id": 1,
      "name": "Baby Hat Updated"
    }
}
```

Update info for a category

### End point
`https://apis.avana.asia/v1/mobile/category/{category_id}`

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
`name` | Category name

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
403 | Forbidden | category_id does not belong to current user 
500 | Input cannot be empty, accepted input: {valid_inputs} | Request cannot be empty, needs atleast one input
500 | Invalid input({invalid_inputs}), accepted input: {valid_inputs} | Request needs a valid input

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Delete Category

> To delete a category, use the following:

```shell
curl -X DELETE -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/category/{category_id}"
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

Delete a category

### End point
`https://apis.avana.asia/v1/mobile/category/{category_id}`

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
404 | Category not found | No category found for the specified category_id 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
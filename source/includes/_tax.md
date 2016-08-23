# Tax
## Tax List

> To get the tax list for a shop, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/tax"
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
      "name": "GST",
      "value": "6.0000"
    },
    {
      "id": 1,
      "name": "Sales",
      "value": "10.0000"
    }
  ]
}
```

Retrive the tax list for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/tax`

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

## Tax Info

> To get a tax info, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/tax/{tax_id}"
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
      "name": "GST",
      "value": "6.0000"
    }
}
```

Retrive info for a tax

### End point
`https://apis.avana.asia/v1/mobile/tax/{tax_id}`

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
404 | Tax not found | No tax found for the specified tax_id 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Create Tax

> To create a tax, use the following:

```shell
curl -X POST -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/tax?name={tax_name}&value={tax_value}"
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
      "name": "GST",
      "value": "6.0000"
    }
}
```

Create a tax for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/tax`

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
`value` | tax value

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Update Tax

> To update a tax, use the following:

```shell
curl -X PATCH -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/tax/{tax_id}?name={new_name}&value={new_value}"
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
      "name": "GST",
      "value": "6.0000"
    }
}
```

Update info for a tax

### End point
`https://apis.avana.asia/v1/mobile/tax/{tax_id}`

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
`name` | tax name
`value` | tax value

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
500 | Input cannot be empty, accepted input: {valid_inputs} | Request cannot be empty, needs atleast one input
500 | Invalid input({invalid_inputs}), accepted input: {valid_inputs} | Request needs a valid input

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Delete Tax

> To delete a tax, use the following:

```shell
curl -X DELETE -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/tax/{tax_id}"
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

Delete a tax

### End point
`https://apis.avana.asia/v1/mobile/tax/{tax_id}`

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
404 | Tax not found | No tax found for the specified tax_id 
<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
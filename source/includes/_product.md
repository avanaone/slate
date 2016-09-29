# Product
## Product List

> To get the product list for a shop, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/product"
```

```javascript
// to be added
```

```php
<?php
//to be added
```

> A successful response will look like the following for product without variant

```json
{
  "data": [
  {
    "id": 397,
    "name": "Product name",
    "description": "Product description",
    "model": "Product model",
    "quantity": 12,
    "price": 120,
    "sale": false,
    "sale_price": 0,
    "weight": 1,
    "estimated_delivery_time": "",
    "estimated_delivery_time_shopbased": true,
    "category": {
      "id": 104,
      "name": "Product Category"
    },
    "tax": {
      "id": 30,
      "name": "GST",
      "value": "6.0000"
    },
    "image": {
      "primary": 401,
      "items": [
        {
          "id": 400,
          "path": "https://apis.avana.asia/uploads/0474194d-387a-57ab-b67d-ba3109a1d8f7.png"
        },
        {
          "id": 401,
          "path": "https://apis.avana.asia/uploads/23a4d39c-8294-5cd6-8cf5-bcaaa23d0335.png"
        }
      ]
    }
  }
  ]
}
```

> A successful response will look like the following for product with variant

```json
{
  "data": [
  {
    "id": 397,
    "name": "Product name",
    "description": "Product description",
    "model": "Product model",
    "price": 120,
    "sale": false,
    "sale_price": 0,
    "weight": 1,
    "estimated_delivery_time": "",
    "estimated_delivery_time_shopbased": true,
    "category": {
      "id": 104,
      "name": "Product Category"
    },
    "tax": {
      "id": 30,
      "name": "GST",
      "value": "6.0000"
    },
    ,
    "image": {
      "primary": 401,
      "items": [
        {
          "id": 400,
          "path": "https://apis.avana.asia/uploads/0474194d-387a-57ab-b67d-ba3109a1d8f7.png"
        },
        {
          "id": 401,
          "path": "https://apis.avana.asia/uploads/23a4d39c-8294-5cd6-8cf5-bcaaa23d0335.png"
        }
      ]
    },
    "variant": [
    {
      "id": 1,
      "name": "s",
      "quantity": 14
    },
    {
      "id": 2,
      "name": "m",
      "quantity": 14
    },
    {
      "id": 3,
      "name": "l",
      "quantity": 14
    }
    ]
  }
  ]
}
```

Retrive the product list for a shop. **For product without image, `image` key will not exist**, do your checking accordingly.

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/product`

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

## Product Info

> To get a product info, use the following:

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/product/{product_id}"
```

```javascript
// to be added
```

```php
<?php
//to be added
```

> A successful response will look like the following for product without variant

```json
{
  "data": {
    "id": 397,
    "name": "Product name",
    "description": "Product description",
    "model": "Product model",
    "quantity": 12,
    "price": 120,
    "sale": false,
    "sale_price": 0,
    "weight": 1,
    "estimated_delivery_time": "",
    "estimated_delivery_time_shopbased": true,
    "category": {
      "id": 104,
      "name": "Product Category"
    },
    "tax": {
      "id": 30,
      "name": "GST",
      "value": "6.0000"
    }
  }
}
```

> A successful response will look like the following for product with variant

```json
{
  "data": {
    "id": 397,
    "name": "Product name",
    "description": "Product description",
    "model": "Product model",
    "price": 120,
    "sale": false,
    "sale_price": 0,
    "weight": 1,
    "estimated_delivery_time": "",
    "estimated_delivery_time_shopbased": true,
    "category": {
      "id": 104,
      "name": "Product Category"
    },
    "tax": {
      "id": 30,
      "name": "GST",
      "value": "6.0000"
    },
    "variant": [
    {
      "id": 1,
      "name": "s",
      "quantity": 14
    },
    {
      "id": 2,
      "name": "m",
      "quantity": 14
    },
    {
      "id": 3,
      "name": "l",
      "quantity": 14
    }
    ]
  }
}
```

Retrive info for a product

### End point
`https://apis.avana.asia/v1/mobile/product/{product_id}`

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
404 | Product not found | No product found for the specified product_id 

<aside class="notice">
  You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


## Create Product

> To create a category, use the following:

```shell
curl -X POST -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/{shop_id}/product"
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
    "id": 1
  }
}
```

Create a product for a shop

### End point
`https://apis.avana.asia/v1/mobile/{shop_id}/product`

### Request Method
`POST`

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Content-Type` | `application/json`
`Accept` | `application/json`

### Request Parameter
Name | Value | Required
--- | --- | ---
`name` | Product name | `Yes`
`description` | Product description | `No`
`price` | Product price | `Yes`
`category` | Category ID | `Yes`
`tax` | Tax ID | `Yes`
`weight` | Weight in KG | `Yes`
`quantity` | Product quamtity | `Yes` without `variation`
`sale` | Is product on sale?( 1 or 0) | `No`
`sale_price` | The price of product if its on sale | `Yes` if `sale` is true 
`estimated_delivery_time` | Estimated delivery time | `Yes` if `global_estimated_delivery_time` is not specified
`global_estimated_delivery_time` | User global estimated delivery time (1 or 0) | `Yes` if `estimated_delivery_time` is not specified
`variation_id` | The variant_id | `Yes` without `quantity`
`variation_value` | The variant values(json object, `{ id:quantity}`). | `Yes` without `quantity` and with `variation_id`

#### `variation_value` example

Consider the following [variation](#varation-info)

`variation_value` value should look like the following:

`variation_value: { 234: 5, 233:5, 232:5, 231: 5}`


### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
422 | Validation error | If there is any validation error
422 | Variant values not complete | Variant values not complete, missing or exceed the required value 
422 | Variants data does not match the variant_id | The `varaint value id` does not belong to `varaint_id`

<aside class="notice">
  You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


## Product Image

> To add a image to a product, use the following:

```shell
curl -X POST -H "Authorization: Bearer access_token" -F "image=@image.jpg"\
"http://apis.avana.asia/v1/mobile/product/{product_id}}/image"
```

```javascript
// to be added
```

```php
<?php
//to be added
```

> A successful response will look like the following for product without variant

```json
{
  "data": {
    "upload": true,
    "path": "https://apis.avana.asia/uploads/96ccf48e-c64f-598d-bb01-fd724e11dd27.png"
  }
}
```

Add image to a product. One product can have a maximum of 4 images. This is a **multipart form request**

### End point
`http://apis.avana.asia/v1/mobile/product/{product_id}}/image`

### Request Method
`POST` 

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Accept` | `application/json`

### Request Parameter
Name | Value
--- | ---
`image` |  the image file
`primary` | `1` or `0` . Set image as primary

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
403 | Forbidden | 403 | Forbidden | product_id does not belong to current user
404 | Product not found | No product found for the specified product_id 
422 | Validation Error | Validation error
422 | Minimum image width must be {width}px' | Minimum image width not met
500 | Image limit reached for this product | Image limit reached for this product
<aside class="notice">
  You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Delete Product

> To delete a product, use the following:

```shell
curl -X DELETE -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/product/{product_id}"
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
`https://apis.avana.asia/v1/mobile/product/{product_id}`

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
403 | Forbidden | product_id does not belong to current user 
404 | Product not found | No product found for the specified product_id 

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

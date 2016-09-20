# Product
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
      "id": 1,
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

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
422 | Validation error | If there is any validation error

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
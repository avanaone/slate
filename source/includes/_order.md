# Order
## Order List

> To get the order list for a shop, use the following:

```shell
curl -X GET -H "Authorization: Bearer access_token"\
-H "Content-Type: application/json" -H "Accept: application/json"\
"https://apis.avana.asia/v1/mobile/shop/{shop_id}/order"
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
      "status": "Processing",
      "customer_name": "Customer Name",
      "date": "2016-04-18 12:07:53"
    },
    {
      "id": 2,
      "status": "Processing",
      "customer_name": "Another Customer Name",
      "date": "2016-04-18 11:07:53"
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

Retrive the order list for a shop

### End point
`https://apis.avana.asia/v1/mobile/shop/{shop_id}/order`
### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`
`Content-Type` | `application/json`
`Accept` | `application/json`

### Request Parameter
Name | Value
--- | ---
`status` | `Processing` ,`Shipped` ,`Refunded` ,`Pending` ,`Paid` ,`Cancelled`

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


## Order Info

> To get the info of a specific order, use the following:

```shell
curl -X GET -H "Authorization: Bearer access_token"\
-H "Content-Type: application/json" -H "Accept: application/json"\
"https://apis.avana.asia/v1/mobile/order/{order_id}"
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
    "id": 779,
    "sub_total": 20,
    "shipping": 8,
    "tax": 0,
    "coupon": 0,
    "total": 28,
    "order_date": "2016-04-18 12:07:53",
    "status": "Shipped",
    "billing_name": "Avana",
    "billing_company": "Avana.asia",
    "billing_address1": "B-3-3A, Pacific Place Commercial Center",
    "billing_address2": "Jalan PJU 1A/4, Ara Damansara",
    "billing_city": "Petaling Jaya",
    "billing_postcode": "47301",
    "billing_state": "Selangor",
    "billing_country": "Malaysia",
    "billing_phone": "0122444444",
    "billing_email": "iifasazuani@gmail.com",
    "shipping_name": "Avana",
    "shipping_company": "Avana.asia",
    "shipping_address1": "B-3-3A, Pacific Place Commercial Center",
    "shipping_address2": "Jalan PJU 1A/4, Ara Damansara",
    "shipping_city": "Petaling Jaya",
    "shipping_postcode": "47301",
    "shipping_state": "Selangor",
    "shipping_country": "Malaysia",
    "shipping_phone": "0122444444",
    "shipping_email": "dummyemail@gmail.com",
    "merchant_notes": "Completed",
    "products": [
      {
        "id": 284,
        "name": "Baby Booties",
        "model": "Booties",
        "quantity": 1,
        "images": [
          {
            "path": "https://placekitten.com/500/300"
          }
        ]
      }
    ]
  }
}
```

Retrive info of a specific order

### End point
`https://apis.avana.asia/v1/mobile/order/{order_id}`

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
404 | Order not found | The requested order does not exist

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


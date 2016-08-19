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


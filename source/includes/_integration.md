# Third Party Integration

In order for a third party to push product to **AVANA** platform, they will have to have the shop's valid ***INTEGRATION_KEY***, **AVANA** user must be able to add the ***INTEGRATION_KEY*** on third party's platform.



## Validating Integration Key

> To validate `INTEGRATION_KEY`, use the following:

```shell
curl -X POST  "https://apis.avana.asia/v1/vendor/vendor?integration_key=INTEGRATION_KEY -H "Authorization: Bearer access_token"
```
```javascript
//to be added
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
      "secure_key" : "SECURE_KEY",
      "validity": true,
      "shop_id": 1
    }
  ]
}
```

> A failed response will look like the following

```json
{
  "error": {
    "message": "No shop is associated with this key: INTEGRATION_KEY",
    "code": 500
  }
}
```

All ***INTEGRATION_KEY*** that is being added must be validated against **AVANA** to make sure the ***INTEGRATION_KEY*** is a valid key. Upon successful validation, AVANA will respond with a `shop_id` and `SECURE_KEY`. This `shop_id` can be used to keep track of activities that involes **AVANA**.

In order to push product to **AVANA**, the push product request must be accompined with the received `SECURE_KEY` in `Avana-Secure-Key` header.

### Request Header
Name | Value
--- | ---
`Authorization` | `Bearer access_token`

### Request Parameter
Name | Value
--- | ---
`integration_key` | `INTEGRATION_KEY`

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>


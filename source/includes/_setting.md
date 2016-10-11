#Setting

## Basic Setting
> To get shop's basic setting, use the following

```shell
curl -X GET -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token"\
"https://apis.avana.asia/v1/mobile/shop/{shop_id}/setting"
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
    "shop_information": {
      "basic_information": {
        "name": "Shop name",
        "description": "Shop description",
        "shop_email": "shop@email.com",
        "phone_number": "123456789",
        "company_reg_no.": "123456789"
      },
      "address": {
        "country": "Malaysia",
        "state": "Perak,
        "post_code": "31900"
      },
      "reporting": {
        "google_analytic_account_id": "",
        "facebook_pixel_id": ""
      }
    },
    "checkout": {
      "payment_information": {
        "currency": "MYR",
        "paypal_email_address": "shop_paypal@email.com",
        "molpay_merchant_admin": "",
        "molpay_verification_code": "",
        "enable_molpay": 0
      }
    },
    "others": {
      "enable_comment_on_product_page": 0
    },
    "invoicing": {
      "logo": "https://apis.avana.asia/188.logo.png"
    }
  }
}
```


Retrive the shop setting

### End point
`https://apis.avana.asia/v1/mobile/shop/{shop_id}/setting`

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

## Update Basic Setting

> To update a shop setting, use the following:

```shell
curl -X PATCH -H "Content-Type: application/json" -H "Accept: application/json"\
-H "Authorization: Bearer access_token" \
"https://apis.avana.asia/v1/mobile/shop/{shop_id}/setting"
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
    "shop_information": {
      "basic_information": {
        "name": "Shop name",
        "description": "Shop description",
        "shop_email": "shop@email.com",
        "phone_number": "123456789",
        "company_reg_no.": "123456789"
      },
      "address": {
        "country": "Malaysia",
        "state": "Perak,
        "post_code": "31900"
      },
      "reporting": {
        "google_analytic_account_id": "",
        "facebook_pixel_id": ""
      }
    },
    "checkout": {
      "payment_information": {
        "currency": "MYR",
        "paypal_email_address": "shop_paypal@email.com",
        "molpay_merchant_admin": "",
        "molpay_verification_code": "",
        "enable_molpay": 0
      }
    },
    "others": {
      "enable_comment_on_product_page": 0
    },
    "invoicing": {
      "logo": "https://apis.avana.asia/188.logo.png"
    }
  }
}

```

Update a shop setting

### End point
`https://apis.avana.asia/v1/mobile/shop/{shop_id}/setting`

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
`name` | shop name 
`description` | shop description
`shop_email` | shop email
`phone_number` | phone number
`company_reg_no.` | company registeration number
`post_code` | post code
`google_analytic_account_id` | GA code
`facebook_pixel_id` | Pixel code
`paypal_email_address` | paypal email address
`molpay_merchant_admin` | molpay merchant admin
`molpay_verification_code` |  molpay verification code
`enable_molpay` |  enable molpay. Boolean
`enable_comment_on_product_page` | enable comment on product page. Boolean
`country` | Country (iso_3166_2)
`state` | State
`currency` | Currency code. Ex: MYR

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
500 | Input cannot be empty, accepted input: {valid_inputs} | Request cannot be empty, needs atleast one input
500 | Invalid input({invalid_inputs}), accepted input: {valid_inputs} | Request needs a valid input

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>

## Invoice Image

> To add invoice image, use the following:

```shell
curl -X POST -H "Authorization: Bearer access_token" -F "image=@image.png"\
"http://apis.avana.asia/v1/mobile/shop/{shop_id}/setting/invoice"
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
    "shop_information": {
      "basic_information": {
        "name": "Shop name",
        "description": "Shop description",
        "shop_email": "shop@email.com",
        "phone_number": "123456789",
        "company_reg_no.": "123456789"
      },
      "address": {
        "country": "Malaysia",
        "state": "Perak,
        "post_code": "31900"
      },
      "reporting": {
        "google_analytic_account_id": "",
        "facebook_pixel_id": ""
      }
    },
    "checkout": {
      "payment_information": {
        "currency": "MYR",
        "paypal_email_address": "shop_paypal@email.com",
        "molpay_merchant_admin": "",
        "molpay_verification_code": "",
        "enable_molpay": 0
      }
    },
    "others": {
      "enable_comment_on_product_page": 0
    },
    "invoicing": {
      "logo": "https://apis.avana.asia/188.logo.png"
    }
  }
}
```

Add invoice image. This is a **multipart form request**

### End point
`http://apis.avana.asia/v1/mobile/shop/{shop_id}/setting/invoice`

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

### Possible error
Code | Error Message | Explanation
--- | --- | ---
401 | Please login to continue | There is no user authenticated for the supplied `access_token` 
422 | Validation Error | Validation error

<aside class="notice">
  You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
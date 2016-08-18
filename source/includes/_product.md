# Product
## Add Product

> To add product, use the following:

```shell
curl -X POST -H "Avana-Secure-Key: secure_key" -H "Content-Type: application/json" -H "Accept: application/json" -H "Authorization: Bearer access_token"
-d '{
    "name": "Product name",
    "model": "Product model",
    "category": "Product Category",
    "option": {
        "name": "Size",
        "for": "Shirt",
        "variation" : ["s","m","l"],
        "quantity": {
            "s" : 10,
            "m" : 10,
            "l" : 10
        }
    },
    "quantity": 10,
    "price": 12,
    "description": "Product description",
    "weight":{
        "value" : 1,
        "unit": "kg"
    },
    "primary_image": "http://example.org/images/image_1.png",
    "images": ["http://example.org/images/image_2.png"],
    "EDT": "1-2 Days",
    "label" : ["label_1", "label_2", "label_3"],
    "tax" : {
        "value": 6,
        "name": "GST"
    },
    "published": true
}' "https://apis.avana.asia/v1/vendor/product"
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
      "product_id": 1
    }
  ]
}
```

> A failed response will look like the following

```json
{
  "error": {
    "message": "Adding product failed",
    "code": 500
  }
}
```

## Edit Product

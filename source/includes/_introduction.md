# Introduction

> Success Response (Single resource)

```
{
    "data" : {
        "key" : "value"
    }
}
```


> Success Response (Multiple resource)

```
{
    "data" : [
        {
            "key" : "value"
        },
        {
            "key" : "value"
        }
    ]
}
```


> Error Response

```
{
    "error" : {
        "message" : "Relevant error message",
        "code" : "500"
    }
}
```
Some fancy intro

For testing purpose, please use `http://apis.sandbox.avana.asia/`

### Response
All response from the API is enveloped in a common envelope


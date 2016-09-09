# Registeration

## Email

```shell

```

```javascript
//to be added
```

```php
<?php
//to be added
```

### End point
`https://apis.avana.asia/v1/oauth/register`

### Request Method
`POST`

### Request Header
Name | Value
--- | ---
`Content-Type` | `application/x-www-form-urlencoded`
`Accept` | `application/json`

### Request Parameter
Name | Value
--- | ---
`email` => email,
`password` => password,
`client_id` => `CLIENT_ID`,
`client_secret` => `CLIENT_SECRET`,
`grant_type` => `register`

### Possible error
*to be added*

<aside class="notice">
    Replace <code>CLIENT_ID</code> and <code>CLIENT_SECRET</code> with the one that you recieved while registering for an app
</aside>

## Facebook

```shell

```

```javascript
//to be added
```

```php
<?php
//to be added
```

### End point
`https://apis.avana.asia/v1/facebook/signon`

### Request Method
`POST`

### Request Header
Name | Value
--- | ---
`Content-Type` | `application/x-www-form-urlencoded`
`Accept` | `application/json`

### Request Parameter
Name | Value
--- | ---
`access_token` | facebook access_token
`client_id` | `CLIENT_ID`,
`client_secret` | `CLIENT_SECRET`,
`grant_type` | `facebook`

### Possible error
*to be added*

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
<aside class="notice">
    Replace <code>CLIENT_ID</code> and <code>CLIENT_SECRET</code> with the one that you recieved while registering for an app
</aside>
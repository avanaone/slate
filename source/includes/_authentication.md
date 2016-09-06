# Authentication

> To authenticate using `client_credentials` grant, use the following:

```shell
curl -X POST -H "Content-Type: application/x-www-form-urlencoded"\
-d 'grant_type=client_credentials&client_id=CLIENT_ID&client_secret=CLIENT_SECRET'\
"https://apis.avana.asia/v1/oauth/access_token"

```
```javascript
//to be added
```

```php
<?php
//to be added
```

> To authenticate using `auth_code` grant, use the following following

```shell
# to be added
```
```javascript
// to be added
```

```php
<?php

//to be added
```


> To authenticate using `password` grant, use the following following

```shell
curl -X POST -H "Content-Type: application/x-www-form-urlencoded"\
-d 'grant_type=password&client_id=CLIENT_ID&client_secret=CLIENT_SECRET&username=USERNAME&password=PASSWORD' \
"https://apis.avana.asia/v1/oauth/access_token"
```
```javascript
// to be added
```

```php
<?php

//to be added
```

**AVANA** uses OAuth2 to allow access to the API and supports the following grants:

- Client Credentials (Trusted Third Party Platform)
- Authorization Code 
- Resource Owner Password Credentials

### Authentication Flow

#### Client Credentials

Plese refer to RFC6749 [Section-4.4](https://tools.ietf.org/html/rfc6749#section-4.4)

#### Authorization Code 

Plese refer to RFC6749 [Section-4.1](https://tools.ietf.org/html/rfc6749#section-4.1)

#### Resource Owner Password Credentials

Plese refer to RFC6749 [Section-4.1](https://tools.ietf.org/html/rfc6749#section-4.3)

**AVANA** expects for the access_token to be included in all API requests to the server in a header that looks like the following:

`Authorization : Bearer access_token`

<aside class="notice">
    You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
<aside class="notice">
    Replace <code>CLIENT_ID</code> and <code>CLIENT_SECRET</code> with the one that you recieved while registering for an app
</aside>
<aside class="notice">
    Replace <code>USERNAME</code> and <code>PASSWORD</code> with the one entered by the user
</aside>
# Authentication

> To authenticate using `client_credentials` grant, use the following:

```shell
curl -X GET  "https://apis.avana.asia/v1/oauth/access_token?client_id=CLIENT_ID&client_secret=CLIENT_SECRET&grant_type=client_credentials"
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

> A successfull response will look like the following

```json
{
    "data" : {
	    "access_token": "access_token_string",
	    "token_type": "Bearer",
	    "expires_in": 5184000
    }
}
```
**AVANA** uses OAuth2 to allow access to the API and supports the following grants:

 - Client Credentials (Trusted Third Party Platform)
 - Authorization Code 

### Authentication Flow

#### Client Credentials

Plese refer to RFC6749 [Section-4.4](https://tools.ietf.org/html/rfc6749#section-4.4)

#### Authorization Code 

Plese refer to RFC6749 [Section-4.1](https://tools.ietf.org/html/rfc6749#section-4.1)

**AVANA** expects for the access_token to be included in all API requests to the server in a header that looks like the following:

`Authorization : Bearer access_token`

<aside class="notice">
You must replace <code>access_token</code> with your access token recieved upon authorization.
</aside>
<aside class="notice">
Replace <code>CLIENT_ID</code> and <code>CLIENT_SECRET</code> with the one that you recieved while registering for an app
</aside>
All requests to the API should be signed as OAuth 1.0a requests. To sign a request you'll need a client key, a client secret,
an access token and an access token secret. For the client key and secret please get in contact with us at
`api@alpinereplay.com` to register. To get your access token and secret you'll need to implement the 3-legged
OAuth authorization flow.

Lets go through this process with some examples in PHP.<br /><br />

## 3-legged OAuth authorization<br />

From the client's point of view (your app) this process consists of three steps:

1. The initial connection between client and API server.
1. A redirect to our servers (the API server) where the user will grant access to the client (your app).
1. A rederect back to the client with passed access token and secret.<br /><br />

### 1. Initial connection<br />

In this phase you'll send a request to `https://www.alpinereplay.com/api/oauth_init`. This request should be signed with
your client tokens. You'll also need to give a return URL (the URL you'll want the user to return to after authorization;
this should be a URL running on your app).

The server returns with a request token and request token secret. You'll want to save the request token and the request
token secret because you'll need them to make other calls on this API.

Let's take a look at what an example in PHP would look like:<br /><br />

```php
$oauth = new OAuth(
    'your client token here',
    'your client token secret here',
    OAUTH_SIG_METHOD_HMACSHA1,
    OAUTH_AUTH_TYPE_AUTHORIZATION);

$requestToken = $oauth->getRequestToken(
    'https://www.alpinereplay.com/api/oauth_init',
    'your callback URL here');

$_SESSION['oauth_request_token']        = $requestToken['oauth_token'];
$_SESSION['oauth_request_token_secret'] = $requestToken['oauth_token_secret'];
```
<br /><br />

### 2. User redirection

Now redirect the user to `https://www.alpinereplay.com/api/oauth_login`. The URL string should contain
`oauth_token` as a GET parameter. This will allow us to grant access once the user has entered her email
and password.

Using the eample above, here's what the next step would look like:<br /><br />

```php
header("Location: https://www.alpinereplay.com/api/oauth_login?oauth_token={$requestToken['oauth_token']}");
```

In practice these first two steps may be combined into a single script.

Here is a full example in PHP:<br /><br />

```php
session_start();

try {

    $oauth = new OAuth(
        'your client token here',
        'your client token secret here',
        OAUTH_SIG_METHOD_HMACSHA1,
        OAUTH_AUTH_TYPE_AUTHORIZATION);

    $requestToken = $oauth->getRequestToken(
        'https://www.alpinereplay.com/api/oauth_init',
        'your callback URL here');

    $_SESSION['oauth_request_token']        = $requestToken['oauth_token'];
    $_SESSION['oauth_request_token_secret'] = $requestToken['oauth_token_secret'];

    header("Location: https://www.alpinereplay.com/api/oauth_login?oauth_token={$requestToken['oauth_token']}");

} catch (OAuthException $e) {
    // handle errors here
}
```
<br /><br />

### 3. Getting access tokens

After the user grants access to your client she'll be redirected to the URL that is passed as a callback URL. The Trace server
will add two GET parameters `oauth_verifier` and `oauth_token`. These two parameters will give you the user's access
token and access token secret respectively.

Uses these to send a request to `https://www.alpinereplay.com/api/oauth_access_token` signed with your client tokens and
request tokens from first phase. In response you will get an access tokens.

Here is an example with PHP:<br /><br />

```php
session_start();

try {

    $verifierToken = $_GET['oauth_verifier'];
    $requestToken  = $_GET['oauth_token'];

    $oauthToken       = $_SESSION['oauth_request_token'];
    $oauthTokenSecret = $_SESSION['oauth_request_token_secret'];

    if ($oauthToken != $requestToken) {
        throw new Exception('Request tokens mismatch');
    }

    $oauth = new OAuth(
        'your client token here',
        'your client token secret here',
        OAUTH_SIG_METHOD_HMACSHA1,
        OAUTH_AUTH_TYPE_AUTHORIZATION);
    $oauth->setToken($oauthToken, $oauthTokenSecret);

    $accessToken = $oauth->getAccessToken(
        'https://www.alpinereplay.com/api/oauth_access_token',
        null,
        $verifierToken
    );

    // save $accessToken['oauth_token'] and $accessToken['oauth_token_secret'] for further requests to API

} catch (Exception $e) {
    // handle errors here
}
```
<br /><br />

Great! You've now been authenticated! You can start requesting select endpoints from the API. Let's take a look at requests and responses first.<br /><br />

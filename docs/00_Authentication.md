All requests to the API should be signed OAuth 1.0a requests. To sign a request you need client key, client secret,
access token and access token secret. Client key and secret you will get after API user registration. To get access
token and secret you need to implement 3-legged OAuth authorization flow.

Further we will see this process in details with code examples in PHP.

## 3-legged OAuth authorization

From client point of view this process consists of three steps:

1. initial connection between client and API server,
1. user redirection to API server to let user grant access to client,
1. request access tokens when user returned to client.

### 1. Initial connection

On this phase you send a request to `https://www.alpinereplay.com/api/oauth_init`. This request should be signed with
your client tokens. Also you provide a return URL. On this URL user is redirected after he grants access to his account
to your application.

Server returns request token and request token secret. These tokens are used in further process so you need to save them
for example in session.

Here is a PHP example code for this phase:

```php
$oauth = new OAuth(
    'your client token here',
    'your client token secret here',
    OAUTH_SIG_METHOD_HMACSHA1,
    OAUTH_AUTH_TYPE_AUTHORIZATION);

$requestToken = $oauth->getRequestToken(
    'https://www.alpinereplay.com/api/oauth_init',
    'your callback URL here');

$_SESSION['oauth_request_token'] = $requestToken['oauth_token'];
$_SESSION['oauth_request_token_secret'] = $requestToken['oauth_token_secret'];
```

### 2. User redirection

Then you redirect a user to `https://www.alpinereplay.com/api/oauth_login` with request token as `oauth_token` GET
parameter where he can log in (if he was not logged in) and grant access to your client.

```php
header("Location: https://www.alpinereplay.com/api/oauth_login?oauth_token={$requestToken['oauth_token']}");
```

In practice first two steps may be combined in one action that is performed when user presses a control to give access
to his account to your client.

Here is a full example for such action in PHP:

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

    $_SESSION['oauth_request_token'] = $requestToken['oauth_token'];
    $_SESSION['oauth_request_token_secret'] = $requestToken['oauth_token_secret'];

    header("Location: https://www.alpinereplay.com/api/oauth_login?oauth_token={$requestToken['oauth_token']}");

} catch (OAuthException $e) {
    // handle errors here
}
```

### 3. Getting access tokens

After user grants access to your client he is redirected to URL that is passed as callback URL on first phase. Also API
server adds GET parameters `oauth_verifier` and `oauth_token`. You should use them to get user's access token and access
token secret.

To do it send request to `https://www.alpinereplay.com/api/oauth_access_token` signed with your client tokens and
request tokens from first phase. In response you will get an access tokens.

Here is an example code:
```php
session_start();

try {

    $verifierToken = $_GET['oauth_verifier'];
    $requestToken = $_GET['oauth_token'];

    $oauthToken = $_SESSION['oauth_request_token'];
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

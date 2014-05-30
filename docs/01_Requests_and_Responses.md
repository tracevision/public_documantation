### Requests to API

To make calls you need to send HTTP GET or POST request to API endpoint with required and optional parameters. This call
also should be signed with OAuth.

Each sport type supported by API server has its own domain for API calls. Also API version number is included to
address. There are two supported sports and base API URL looks like this:

* Skiing and snowboarding: https://www.alpinereplay.com/api/v1
* Surfing: https://surf.activereplay.com/api/v1

Further in this documentation you will see a list of API methods that look like this: "GET /users/self". This means
that you can send HTTP GET request to https://www.alpinereplay.com/api/v1/users/self or to
https://surf.activereplay.com/api/v1/users/self. Sport related data inside response depends on URL domain.

### API responses

API uses JSON format in response. It always contains boolean `success` property which represents status of request.

If request was successful response will contain `success` equals to `true` and `data` property with response data. Also
HTTP code 200 for response.

Example of response data with array:
```javascript
{
   "success":true,
   "data":[
      {
         "prop1":"val1"
      },
      {
         "prop2":"val2"
      }
   ]
}
```

Successful response with dictionary for data:
```javascript
{
   "success":true,
   "data":{
      "prop1":"val1",
      "prop2":"val2"
   }
}
```

If request was not successful response contains `success` equals to `false` and `error` property with `id` and `message`
properties with information about error. Also response HTTP code 4xx, 5xx.
```javascript
{
   "success":false,
   "error":{
      "id":"oauth_authentication_failed",
      "message":"OAuth authentication failed"
   }
}
```

### API call example

Here is an example of API request to users search method in PHP:
```php
try {

    $oauth = new OAuth(
        'your client token here',
        'your client token secret here',
        OAUTH_SIG_METHOD_HMACSHA1,
        OAUTH_AUTH_TYPE_AUTHORIZATION);

    $oauth->setToken('user access token here', 'user access token secret here');

    $oauth->setRequestEngine(OAUTH_REQENGINE_CURL);

    $oauth->fetch(
        "https://www.alpinereplay.com/api/v1/users/search",
        array('term' => 'john smith'),
        OAUTH_HTTP_METHOD_POST);

    $responseJson = $oauth->getLastResponse();
    echo $responseJson;

} catch (Exception $e) {
    // handle errors here
}
```

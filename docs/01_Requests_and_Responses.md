### Requests to API

To make calls you'll need to send an HTTPS GET or POST request to an API endpoint with required and optional parameters.
This call should also be signed with OAuth.

Each sport type supported by the API server has its own domain for API calls. An API version number is also included in
the address. There are two supported sports and base API URLs:

* Skiing and snowboarding: https://www.alpinereplay.com/api/v1
* Surfing: https://surf.activereplay.com/api/v1

Further in this documentation you will see a list of API methods that look like this: "GET /users/self". This means
that you can send an HTTPS GET request to https://www.alpinereplay.com/api/v1/users/self or to
https://surf.activereplay.com/api/v1/users/self. Sport related data inside the response depends on URL domain.

### API responses

The Trace API uses the JSON format in responses because JSON is made from awesomesauce.
The response will always contain boolean `success` property which represents status of request.

If request was successful response will contain `success` equals to `true` and `data` property with response data.
There will also be an HTTP code 200 for the response.<br /><br />

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

<br /><br />
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

<br /><br />
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
<br /><br />

### API call example

Here is an example of an API request to the users search method in PHP:
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

### Requests to API

To make calls you'll need to send an HTTPS GET or POST request to an API endpoint with required and optional parameters.
This call should also be signed with OAuth.

Each sport type supported by the API server has its own domain for API calls. An API version number is also included in
the address. There are two supported sports and base API URLs:

* Trace Snow: https://www.alpinereplay.com/api/v1 or https://snow.traceup.com/api/v1
* Trace Surf: https://surf.activereplay.com/api/v1 or https://surf.traceup.com/api/v1

Further in this documentation you will see a list of API methods that look like this: "GET /users/self". This means
that you can send an HTTPS GET request to https://www.alpinereplay.com/api/v1/users/self or to
https://surf.activereplay.com/api/v1/users/self. Sport related data inside the response depends on URL domain.


### Support of sport subtypes
Each sport has subtypes. If an API call has **sport** parameter it means that it may have one of these values depending on sport:

Trace Snow: skier, snowboarder.

Trace Surf: surfing, windkite, wind, kite, sup_surf, sup_race, wake, other, wakesurf.

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

### Response filter
Some endpoints may produce a big JSON response which may be difficult to handle especially on mobile. Meanwhile only part of response is needed for application. To reduce amount of data in response and get only required properties a developer can use **filter** parameter. It's GET or POST parameter according to API call. **filter** is a JSON string with following structure:
```javascript
{
    "type":< filter type >,
    "properties":< filter properties >
}
```

**< filter type >** can have values **"show"** or **"hide"**. With **"show"** value properties listed in **< filter properties >** will be saved and all other will be deleted from response. And with **"hide"** value properties listed in **< filter properties >** will be deleted and all other will be saved.

**< filter properties >** is a structure that reflects response structure with two differences: 

1. for array of elements create only one array item,
1. set properties values to **true** for that properties which is needed to be shown or hidden depending on **< filter type >**.

Let's take "GET users/self" endpoint for example. Let's assume that in response a developers wants: user_id, Dropbox credentials, all resorts data and list of user groups ids. It this case **filter** will have value:

```javascript
{
    "type":"show",
    "properties":{
        "user_id":true,
        "credentials":{
            "dropbox":true
        },
        "resorts":true,
        "groups":[
            {
                "group_id":true
            }
        ]
    }
}
```

And response will be:
```javascript
{
    "success":true,
    "data":{
        "user_id":73799,
        "resorts":[
            {
                "resort_id":3208,
                "title":"Val d'Isere"
            }
        ],
        "groups":[
            {
                "group_id":11
            }
        ],
        "credentials":{
            "dropbox":{
                "access_token":"QABs48Iu...",
                "user_name":"Vadim I.",
                "dropbox_id":"27370"
            }
        }
    }
}
```


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

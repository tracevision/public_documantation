### General notes on Authentication <br /><br />

**Authentication** <br />
All requests to the API should be signed with OAuth 1.0a requests. There are two types of signature types: API client and API user. API client request uses only client id and client secret to sign the request. API user signs requests with client id, client secret, access token and access token secret.

**Authorization** <br />
Each API method defines a list of authorization groups required to execute this method. This list is verified against a list of enabled groups for request which consists of groups from API client and API user (if last is present). List of defined groups:
* users - group of site users, this group is given to access tokens after 3-legged OAuth authentication.
* native_apps - this group is given to API clients with extended rights, such as possibility to create new users. <br /><br />

### Session Endpoint <br /><br />
#### POST session/login<br />
Authentication: API client<br />
Authorization: native_apps<br /><br />

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
email | ✓ | |
password | ✓ |  |
application |  | ar_native | Application code for `user_sessions`. `application_id` value. If not set, value 1 will be used (“ar_native” application).
<br />
Success response:
```javascript
{
   "success":true,
   "data":{
      "api_token":{
         "oauth_token":"6ab237...",
         "oauth_token_secret":"8cd97f..."
      }
   }
}
```
<br /><br />

#### **POST session/register**<br /><br />
Authentication: API client<br />
Authorization: native_apps<br /><br />

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
email | ✓ | |
password | ✓ | |
password_confirm | ✓ | |
first_name | ✓ | |
last_name | | [empty string] |
weight | | | In grams
sport | | |
sex | | |
birth_date | | |
country | | |
application | | ar_native | Application code for `user_sessions`. `application_id` value. If not set, value 1 will be used (“ar_native” application).
<br />
Success response:
```javascript
{
   "success":true,
   "data":{
      "api_token":{
         "oauth_token":"6ab237...",
         "oauth_token_secret":"8cd97f..."
      }
   }
}
```
<br /><br />

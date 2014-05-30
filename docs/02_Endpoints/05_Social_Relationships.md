
#### **GET users/[user_id]/following**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "user_id":66222,
         "first_name":"Ben",
         "last_name":"Sandle",
         "pic_url":"...inereplay.com\/images\/userpics\/200x200.jpg",
         "sport":"snowboarder",
         "home_resort_title":"Turoa",
         "following":false,
         "premium":false
      },
      {
         "user_id":68135,
         "first_name":"Laura",
         "last_name":"Binns",
         "pic_url":"...inereplay.com\/images\/userpics\/200x200.jpg",
         "sport":"skier",
         "home_resort_title":"Whakapapa",
         "following":false,
         "premium":false
      }
   ]
}
```


#### GET **users/[user_id]/followed-by**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "user_id":109,
         "first_name":"David",
         "last_name":"Lokshin",
         "pic_url":"...inereplay.com\/images\/userpics\/200x200.jpg",
         "sport":"snowboarder",
         "home_resort_title":"Snow Summit",
         "following":true,
         "premium":false
      },
      {
         "user_id":68135,
         "first_name":"Laura",
         "last_name":"Binns",
         "pic_url":"...inereplay.com\/images\/userpics\/200x200.jpg",
         "sport":"skier",
         "home_resort_title":"Whakapapa",
         "following":false,
         "premium":false
      }
   ]
}
```


#### **POST users/[user_id]/follow**

No request params (except user_id in URL).

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```


#### **POST users/[user_id]/unfollow**

No request params (except user_id in URL).

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```


#### **POST users/search**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
term | ✓ | |

Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "user_id":40825,
         "name":"Adam Foote",
         "home_resort_title":"Blue Mountain Ontario",
         "following":false,
         "pic_url":"...inereplay.com\/images\/userpics\/100x100.jpg"
      },
      {
         "user_id":39393,
         "name":"Alan Fooks",
         "home_resort_title":"",
         "following":false,
         "pic_url":"...inereplay.com\/images\/userpics\/100x100.jpg"
      }
   ]
}
```


#### **POST users/self/follow-suggestions**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "user_id":4587,
         "first_name":"Nate",
         "last_name":"Holland",
         "pic_url":"...inereplay.com\/images\/userpics\/200x200.jpg",
         "sport":"",
         "home_resort_title":"Telluride",
         "following":false,
         "premium":false,
         "session_sheets":[
            "...alpinereplay.com\/stats\/get_stats_image?iId=76500",
            "...alpinereplay.com\/stats\/get_stats_image?iId=76501",
            "...alpinereplay.com\/stats\/get_stats_image?iId=76502",
            "...alpinereplay.com\/stats\/get_stats_image?iId=76503",
            "...alpinereplay.com\/stats\/get_stats_image?iId=76504"
         ]
      }
   ]
}
```



#### **POST users/invite**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
name | ✓ | |
email | ✓ | |

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```

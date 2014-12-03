#### **GET users/self**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":{
      "user_id":72653,
      "first_name":"Test The Second",
      "last_name":"Name The Good",
      "pic_url":"...r_photo\/get?user_id=72653&width=200&height=200",
      "birth_date":"1983-10-12",
      "weight":87500,
      "gender":"male",
      "units":"metric",
      "challenges_count":0,
      "runs_count":13,
      "resorts":[
         {
            "resort_id":2424,
            "title":"Sugarloaf"
         },
         {
            "resort_id":2362,
            "title":"Copper Mountain"
         }
      ],
      "bio":"Kupchino rules!",
      "equipment":"Arms and legs",
      "sport":"skier",
      "home_resort_id":2423,
      "premium":true,
      "groups":[
         {
            "group_id":34,
            "name":"Test Group"
         },
         {
            "group_id":42,
            "name":"mt snow"
         }
      ],
      "credentials":{
         "twitter":{
            "oauth_token":"901490...",
            "oauth_token_secret":"vYKM3s...",
            "country":"en"
         },
         "facebook":{
            "access_token":"CAABus...",
            "facebook_id":"100001043710814",
            "permission":true
         }
      },
      "email":"foo@bar8.com",
      "invite_id":"4xDdSqI8",
      "android_notifications":true,
      "iphone_notifications":true,
      "android_version":"2.2.0",
      "iphone_version":"2.2.1"
   }
}
```


#### **POST users/self**

Request Parameter | Mandatory | Default value | Comments
---|:---:|---|---
first_name | ✓ | |
last_name | | [empty string] | |
weight | | | In grams
sport | | |
sex | | |
home_resort_id | | |
birth_year | | |
birth_month | | |
birth_day | | |
units | | | ‘metric’ or ‘imperial’
equipment | | |
bio | | |
profile_picture | | | File with new user image

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```


#### **GET users/self/medals**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | --- 
season | | | Season (e.g. 2013) or empty to get medals for all seasons

Success response:
```javascript
{
   "success":true,
   "data":[
         {
            "count":2,
            "thumb":"\/images\/badges\/premium\/large\/pr.png",
            "desc":"You set a new personal record",
            "first":"2013-05-13 09:46:14",
            "title":"PR",
            "img" :"/images/badges/ar-large/pr.png"
         },
         {
            "count":1,
            "thumb":"\/images\/badges\/premium\/large\/casual.png",
            "desc":"10 runs in 1 day",
            "first":"2013-05-13 09:46:14",
            "title":"Casual"
            "img" :"/images/badges/ar-large/casual.png"
         }
      ]
   }
}
```


#### **GET users/[user_id]**

No request parameters (except user_id in URL).

Success response:
```javascript
{
   "success":true,
   "data":{
      "user_id":72653,
      "first_name":"Test The Second",
      "last_name":"Name The Good",
      "pic_url":"...r_photo\/get?user_id=72653&width=200&height=200",
      "birth_date":"1983-10-12",
      "weight":87500,
      "gender":"male",
      "units":"metric",
      "challenges_count":0,
      "runs_count":13,
      "resorts":[
         {
            "resort_id":2424,
            "title":"Sugarloaf"
         },
         {
            "resort_id":2362,
            "title":"Copper Mountain"
         }
      ],
      "bio":"Kupchino rules!",
      "equipment":"Arms and legs",
      "sport":"skier",
      "home_resort_id":2423,
      "premium":true,
      "groups":[
         {
            "group_id":34,
            "name":"Test Group"
         },
         {
            "group_id":42,
            "name":"mt snow"
         }
      ],
      "is_followed":false,
      "followers":1,
      "followed":5,
      "visit_counts":[
         {
            "month":"2014-02",
            "count":1
         },
         {
            "month":"2013-04",
            "count":5
         },
         {
            "month":"2013-02",
            "count":2
         }
      ]
   }
}
```


#### **GET users/[user_id]/medals**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | --- 
season | | | Season (e.g. 2013) or empty to get medals for all seasons

Success response:
```javascript
{
   "success":true,
   "data":[
         {
            "count":2,
            "thumb":"\/images\/badges\/premium\/large\/pr.png",
            "desc":"You set a new personal record",
            "first":"2013-05-13 09:46:14",
            "title":"PR",
            "img" :"/images/badges/ar-large/pr.png"
         },
         {
            "count":1,
            "thumb":"\/images\/badges\/premium\/large\/casual.png",
            "desc":"10 runs in 1 day",
            "first":"2013-05-13 09:46:14",
            "title":"Casual"
            "img" :"/images/badges/ar-large/casual.png"
         }
      ]
   }
}
```

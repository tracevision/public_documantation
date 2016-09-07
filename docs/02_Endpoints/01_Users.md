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
      "has_trace":true,      
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
      "iphone_version":"2.2.1",
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
      "has_trace":true,      
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

#### POST users/self/stats/compare

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats| ✓ | | json array of stat type strings
sport | | |

Success response:
```javascript
{
   "success":true,
   "data":
   {
      "stats":[
         {
            "stat_type":"jumps",
            "users":[
               {
                  "user_name":"Test51c38a857d Testself890649b380",
                  "user_id":260377,
                  "pic_url":"https://...",
                  "value":106925
               },
               {
                  "user_name":"John Smith",
                  "user_id":259957,
                  "pic_url":"https://...",
                  "value":82
               }
            ]
         },
         {
            "stat_type":"total_distance",
            "users":[...]
         }
      ]
   }
}
```

#### POST users/[user_id]/stats/compare

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats| ✓ | | json array of stat type strings

Success response:
The same form as for users/self/stats/compare

#### POST users/self/stats/progression

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats| ✓ | | json array of stat type strings
time_scale| | | "day", "month", or "year" (optional, defaults to "day")
start_date| | | "YYYY-MM-DD" date minimum time stamp for any stat values in response (optional, defaults to 30 days ago)
end_date| | | "YYYY-MM-DD" date maximum time stamp for any stat values in response (optional defaults to now)
sport | | | 


Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "stat_type":"jumps",
         "average":11.135593220339,
         "personalRecord":
         {
            "value":63,
            "visit_id":470385,
            "date":"2015-06-21T00:00:00+00:00"
         },
         "base":655,
         "values":[
            {
               "date":"2015-08-27T00:00:00+00:00",
               "value":2
            }
         ]
      },
      {
         "stat_type":"total_distance",
         "average":15886.528677267,
         "personalRecord":
         {
            "value":74996.918263752,
            "visit_id":470390,
            "date":"2015-06-21T00:00:00+00:00"
         },
         "base":922563.05826918,
         "values":[
            {
               "date":"2015-08-27T00:00:00+00:00",
               "value":1523.9569520155
            },
            {
               "date":"2015-08-28T00:00:00+00:00",
               "value":12769.563560985
            }
         ]
      }
   ]
}
```

#### POST users/[user_id]/stats/progression

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats| ✓ | | json array of stat type strings
time_scale| | | "day", "month", or "year" (optional, defaults to "day")
start_date| | | "YYYY-MM-DD" date minimum time stamp for any stat values in response (optional, defaults to 30 days ago)
end_date| | | "YYYY-MM-DD" date maximum time stamp for any stat values in response (optional defaults to now)
sport | | | 

Success response:
The same form as for /users/self/stats/progression



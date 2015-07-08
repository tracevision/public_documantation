
#### **GET users/self/events**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
min_timestamp | | | Minimum UTC timestamp of visits update time (in seconds in epoch)
max_timestamp | | | Maximum UTC timestamp of visits update time (in seconds in epoch)
limit | | 10 |

Success response:
```javascript
{
   "success":true,
   "data":[ <array of event items> ]
}
```

The event item contains general information and information specific to event. General information:
```javascript
         "event_id":141185,
         "event_name":"user_visit_add",
         "context":{
            "badges":[
               {
                  "id":4,
                  "title":"Explorer"
               }
            ],
            "comment":"hello world!"
         },
         "user":{
            "user_id":72653,
            "userpic_100":"...\/userpics\/100x100.jpg?ts=1373631023",
            "short_name":"Test The Fourth N."
         },
         "days_passed":"38 days ago",
         "time":"2013-06-04 13:33:03",
         "comments":[
            {
               "user_event_comment_id":1285,
               "can_delete":true,
               "post_time":"2013-06-05 12:10:43",
               "time":"now",
               "is_like":false,
               "message":"hello world!",
               "author":{
                  "user_id":72653,
                  "userpic_100":"...pics\/100x100.jpg?ts=1373631023",
                  "short_name":"Test The Fourth N."
               }
            }
         ],
         "likes":{
            "is_liked":true,
            "like_authors":[
               {
                  "first_name":"Test The Fourth",
                  "user_id":72653
               }
            ],
            "count":1
         }
```
context contains a visit’s medals and user’s comment for the visit.

Properties for a new follower:
```javascript
         "follower":{
            "user_id":10796,
            "short_name":"A S.",
            "userpic_100":"...lay.com\/images\/userpics\/100x100.jpg"
         }
```


Properties for new visit:
```javascript
         "visit":{
            "visit_id":129304,
            "resort_title":"Sugarloaf",
            "resort_name":"sugarloaf",
            "image":"...inereplay.com\/stats\/get_stats_image?iId=45",
            "stats":{
               "total_distance":3395.2783795707,
               "max_speed":16.361573885174,
               "avg_speed":9.0108148191514,
               "calories":59.473302995155,
               "jumps":0,
               "air_time":0,
               "calories_per_lb":0.0010912532659662,
               "max_slope":0.488109859999,
               "slope_time":398.59999990463,
               "lift_time":567.20000004768,
               "rest_time":57.200000047684,
               "vertical_drop":683.40430540792,
               "avg_slope":0.19186970055397,
               "sustained_speed":14.935487939803,
               "lunch_time":0
            }
         }
```


Properties for new video:
```javascript
         "video":{
            "video_id":139,
            "start_time":"2014-03-02 17:08:03",
            "link":"http:\/\/www.youtube.com\/watch?v=_ShlXyCT1A0"
         }
```



#### **POST events/[event_id]/like**

No request parameters (except event_id in the URL).

Success response:
```javascript
{
   "success":true,
   "data":{
      "show_facebook_like":true,
      "likes_count":1
   }
}
```
Note: show_facebook_like may be omitted if a task for a Facebook like was not created.

#### **POST events/[event_id]/unlike**

No request parameters (except event_id in URL).

Success response:
```javascript
{
   "success":true,
   "data":{
      "likes_count":0
   }
}
```

Failure response
```javascript
{
    "success": "false",
    "error": {
        "id": “like_not_found”,
        "message": “Like not found”
    }
}
```

#### **POST events/[event_id]/comment**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
message | ✓ | | Comment text

Success response:
```javascript
{
   "success":true,
   "data":{
       "comment":{
           "user_event_comment_id":102,
           "can_delete":true,
           "post_time":"2013-06-05 12:10:43",
           "time":"now",
           "is_like":false,
           "message":"776820dc79067591e4228d48f694aa3f",
           "author":{
               "user_id":260116,
               "userpic_100":"http:\/\/snow.traceup.com\/images\/userpics\/100x100.jpg",
               "userpic_40":"http:\/\/snow.traceup.com\/images\/userpics\/40x40.jpg",
               "short_name":"Testf3d5806c5e"
           }
       }
    }
}
```



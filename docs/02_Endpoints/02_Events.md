
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
               "time":"06\/05\/2013 12:10:43",
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
            "image":"...inereplay.com\/stats\/get_stats_image?iId=45"
         }
```


Properties for new video:
```javascript
         "video":{
            "video_id":139,
            "resort_titile":"Sugarloaf",
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




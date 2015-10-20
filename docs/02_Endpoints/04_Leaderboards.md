
#### **GET users/[user_id]/leaderboards/total**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stat | ✓ | | |
resort_id | | |
sport | | |
gender | | |
age | | |
season | | |
following | | |


Success response:
```javascript
{
   "success":true,
   "data":{
      "user_result":{
         "user_id":72653,
         "name":"Test The Fourth N.",
         "sport":"snowboarder",
         "value":6720.3525619054,
         "pic_url":"...\/72653\/userpics\/100x100.jpg?ts=1370343007",
         "rank":2,
         "visit_id":129300,
         "date":"Nov 18 2011",
         "resort_title":"Copper Mountain"
      },
      "lb_data":[
         {
            "user_id":109,
            "name":"David L.",
            "value":196231.70645749,
            "sport":"snowboarder",
            "pic_url":"...replay.com\/images\/userpics\/100x100.jpg",
            "rank":1,
            "following":true,
            "visit_id":101284,
            "date":"Mar 17 2012",
            "resort_title":"Big Sky"
         },
         {
            "user_id":72653,
            "name":"Test The Fourth N.",
            "value":6720.3525619054,
            "sport":"snowboarder",
            "pic_url":"...2653\/userpics\/100x100.jpg?ts=1370343007",
            "rank":2,
            "following":true,
            "visit_id":129300,
            "date":"Nov 18 2011",
            "resort_title":"Copper Mountain"
         }
      ]
   }
}
```

#### **GET users/[user_id]/leaderboards/weekly**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stat | ✓ | | |
resort_id | | |
season | | |
week | | |
sport | | |

Stat types for surf:
total_distance, jumps, air_time, avg_speed, calories, turns_num, longest_ride

Stat types for snow:
total_distance, jumps, air_time, avg_speed, calories, vertical_drop, sustained_speed, slope_time, max_slope

Success response:
```javascript
{
   "success":true,
   "data":{
      "user_result":{
         "user_id":72653,
         "name":"Test The Fourth N.",
         "sport":"snowboarder",
         "value":6720.3525619054,
         "pic_url":"...\/72653\/userpics\/100x100.jpg?ts=1370343007",
         "rank":2,
      },
      "lb_data":[
         {
            "user_id":109,
            "name":"David L.",
            "value":196231.70645749,
            "sport":"snowboarder",
            "pic_url":"...replay.com\/images\/userpics\/100x100.jpg",
            "rank":1,
            "following":true,
         },
         {
            "user_id":72653,
            "name":"Test The Fourth N.",
            "value":6720.3525619054,
            "sport":"snowboarder",
            "pic_url":"...2653\/userpics\/100x100.jpg?ts=1370343007",
            "rank":2,
            "following":true,
         }
      ]
   }
}
```

#### **GET users/[user_id]/leaderboards/daily**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stat | ✓ | |
date | ✓ | | yyyy-mm-dd
resort_id | |
sport | | |

Success response:
```javascript
{
   "success":true,
   "data":{
      "user_result":{
         "user_id":72653,
         "name":"Test The Fourth N.",
         "sport":"snowboarder",
         "value":6720.3525619054,
         "pic_url":"...\/72653\/userpics\/100x100.jpg?ts=1370343007",
         "rank":1
      },
      "lb_data":[
         {
            "user_id":72653,
            "name":"Test The Fourth N.",
            "value":31829.223305705,
            "sport":"snowboarder",
            "pic_url":"...2653\/userpics\/100x100.jpg?ts=1370343007",
            "rank":1,
            "following":true
         },
         {
            "user_id":109,
            "name":"David L.",
            "value":31829.223305705,
            "sport":"snowboarder",
            "pic_url":"...replay.com\/images\/userpics\/100x100.jpg",
            "rank":2,
            "following":true
         }
      ]
   }
}
```


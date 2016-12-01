
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

#### **GET users/[user_id]/leaderboards/monthly**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stat | ✓ | | |
resort_id | | |
season | | |
month | | | Number of month from 1 to 12
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
         "user_id":73799,
         "name":"Vadim I.",
         "sport":"skier",
         "value":"-",
         "pic_url":"https:\/\/s3.amazonaws.com\/dev7.xsportsw.com\/public\/users\/73000\/73799\/userpics\/100x100.jpg?ts=1464970577",
         "rank":"-",
         "visit_id":0,
         "date":"-",
         "resort_title":"-"
      },
      "lb_data":[
         {
            "user_id":73300,
            "name":"Andy A.",
            "value":"19730.870482308001",
            "sport":"",
            "pic_url":"http:\/\/tracesnow.dev7.alpinereplay.com\/images\/userpics\/100x100.jpg",
            "rank":1,
            "following":false,
            "visit_id":470708,
            "date":"Jun 04 2015",
            "resort_title":"Arapahoe Basin"
         },
         {
            "user_id":70000,
            "name":"john k.",
            "value":"5.2949999999999999",
            "sport":"skier",
            "pic_url":"http:\/\/tracesnow.dev7.alpinereplay.com\/images\/userpics\/100x100.jpg",
            "rank":2,
            "following":false,
            "visit_id":470854,
            "date":"Jun 02 2015",
            "resort_title":"Bolton Valley Resort "
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
         "user_id":73799,
         "name":"Vadim I.",
         "sport":"skier",
         "value":"-",
         "pic_url":"https:\/\/s3.amazonaws.com\/dev7.xsportsw.com\/public\/users\/73000\/73799\/userpics\/100x100.jpg?ts=1464970577",
         "rank":"-",
         "visit_id":0,
         "date":"-",
         "resort_title":"-"
      },
      "lb_data":[
         {
            "user_id":73300,
            "name":"Andy A.",
            "value":"19730.870482308001",
            "sport":"",
            "pic_url":"http:\/\/tracesnow.dev7.alpinereplay.com\/images\/userpics\/100x100.jpg",
            "rank":1,
            "following":false,
            "visit_id":470708,
            "date":"Jun 04 2015",
            "resort_title":"Arapahoe Basin"
         },
         {
            "user_id":70000,
            "name":"john k.",
            "value":"5.2949999999999999",
            "sport":"skier",
            "pic_url":"http:\/\/tracesnow.dev7.alpinereplay.com\/images\/userpics\/100x100.jpg",
            "rank":2,
            "following":false,
            "visit_id":470854,
            "date":"Jun 02 2015",
            "resort_title":"Bolton Valley Resort "
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
         "user_id":73799,
         "name":"Vadim I.",
         "sport":"skier",
         "value":"123979.62194683999",
         "pic_url":"https:\/\/s3.amazonaws.com\/dev7.xsportsw.com\/public\/users\/73000\/73799\/userpics\/100x100.jpg?ts=1464970577",
         "rank":0,
         "visit_id":471094,
         "date":"Apr 01 2016",
         "resort_title":"Val d'Isere"
      },
      "lb_data":[
         {
            "user_id":70000,
            "name":"john k.",
            "value":"5.2949999999999999",
            "sport":"skier",
            "pic_url":"http:\/\/tracesnow.dev7.alpinereplay.com\/images\/userpics\/100x100.jpg",
            "rank":1,
            "following":false,
            "visit_id":470854,
            "date":"Jun 02 2015",
            "resort_title":"Bolton Valley Resort "
         }
      ]
   }
}
```


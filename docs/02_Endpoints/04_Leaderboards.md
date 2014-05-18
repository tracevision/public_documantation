<br />
#### **GET users/[user_id]/leaderboards/total**<br />
Authorization: **users**  <br />
Authentication: **API user**  <br /><br />

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stat | ✓ | | |
resort_id | | |
sport | | |
gender | | |
age | | |
season | | |
following | | |
<br />

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
<br /><br />

#### **GET users/[user_id]/leaderboards/daily**
Authentication: **API user**<br />
Authorization: **users**<br /><br />

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stat | ✓ | |
date | ✓ | | yyyy-mm-dd
resort_id | |
<br />

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


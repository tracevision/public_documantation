#### **POST resorts/search**

Request Parameter| Mandatory | Default value | Comments
--- |:---:| --- | ---
term | ✓ | | First letter of resorts to search. For example, request for “term”=”sugar” will return resorts Sugarloaf, Sugarbush and Sugar Bowl.
limit | | 20 | must be passed as an int and not string


Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "resort_id":2422,
         "title":"Sugar Bowl",
         "name":"sugar_bowl",
         "state":"California",
         "origin":"[39.299893769169,-120.33278632768,2280.8200683594]"
      },
      {
         "resort_id":2423,
         "title":"Sugarbush",
         "name":"sugarbush",
         "state":"Vermont",
         "origin":"[44.148588670556,-72.910809861836,758.59155273438]"
      },
      {
         "resort_id":2424,
         "title":"Sugarloaf",
         "name":"sugarloaf",
         "state":"Maine",
         "origin":"[45.044323209955,-70.314274837269,753.3115234375]"
      }
   ]
}
```


#### **POST resorts/search/by-location**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
longitude | ✓ | |
latitude | ✓ | |
limit | | 10 |


Success response (array of resorts sorted by distance to given point and popularity, highest ranked goes first):
```javascript
{
   "success":true,
   "data":[
      {
         "resort_id":2755,
         "title":"Kavgolovo-Toksovo",
         "name":"kavgolovo_toksovo",
         "state":"Leningrad Oblast",
         "origin":"[60.155555555556,30.525,73.331901550293]"
      }
   ]
}
```


#### **GET resorts/[resort_name]/explore**

No request parameters (except resort name in URL).

Success response:
```javascript
{
   "success":true,
   "data":{
      "session_sheets":[
         {
            "url":"...ereplay.com\/stats\/get_stats_image?iId=10809",
            "visit_id":129248,
            "user_id":72674,
            "event_id":141130,
            "user_name":"Test Name",
            "start_time":"2011-12-20 07:12:38",
            "likes":11,
            "self_liked":true,
            "liked_by":[
               {
                  "user_id":72653,
                  "user_name":"Test The Fourth Name The Good"
               }
            ]
         }
      ],
      "videos":[
         {
            "url":"http:\/\/www.youtube.com\/watch?v=i_aKxORmtL8",
            "visit_id":28430,
            "user_id":3412,
            "event_id":103079,
            "user_name":"Sherri  Carey",
            "creation_time":"2012-01-31 16:46:17",
            "likes":0,
            "self_liked":false,
            "liked_by":[
            ]
         },
      ],
      "avg_run_drop":400.23535185969,
      "avg_run_drop_rating":4,
      "avg_run_dist":1877.2842034987,
      "avg_run_dist_rating":3,
      "avg_visit_cal":637.77654816732,
      "avg_visit_cal_rating":1,
      "sustained_speed":29.78,
      "max_speed":39.35,
      "lift_climb":0.76707660907782,
      "lift_climb_rating":1,
      "week_activity":{
         "Mon":38,
         "Tue":37,
         "Wed":36,
         "Thu":32,
         "Fri":51,
         "Sat":100,
         "Sun":92
      },
      "day_activity":{
         "7:00":3,
         "8:00":22,
         "9:00":83,
         "10:00":100,
         "11:00":100,
         "12:00":81,
         "13:00":75,
         "14:00":59,
         "15:00":31,
         "16:00":2
      },
      "sport_percent":{
         "skier":81,
         "snowboarder":19
      },
      "lifts":[
         {
            "lift_id":4934,
            "title":"Sugarloaf Superquad",
            "drop":513.103515625,
            "distance":1976.6782050408,
            "avg_time":850.4406779661,
            "avg_run_distance":2083.9077636788,
            "climb_rating":1,
            "speed_rating":2,
            "pop_rating":2
         }
      ],
      "lifts_popularity":{
         "Skyline":100,
         "Sugarloaf Superquad":39,
         "King Pine":6,
         "Timberline":3,
         "Bateau":1
      },
      "following_at_resort":[
         {
            "user_id":109,
            "first_name":"David",
            "last_name":"Lokshin",
            "pic_url":"...replay.com\/images\/userpics\/200x200.jpg",
            "sport":"snowboarder",
            "home_resort_title":"Snow Summit",
            "following":true,
            "premium":false
         }
      ],
      "promotions":[
         {
            "title":"Visit new planet",
            "description":"New planets every day",
            "price":0,
            "type":"image",
            "url":"http:\/\/wikipedia.org",
            "image_url":"...t_promotions\/0000\/8\/pics\/140x105.jpg"
         },
         {
            "title":"Super waffle!",
            "description":"With chocolate syrup!",
            "price":1.99,
            "type":"price",
            "url":"http:\/\/yandex.ru",
            "image_url":""
         }
      ]
   }
}
```
Notice: start_time in session sheets section is local time of visit and creation_time in videos section is in the resort's timezone.

#### GET resorts/[resort_name]/weather/forecast
Controller and action style: **{android,iphone}/get_resort_weather_forecast**
Authentication: **API user**
Authorization: **users**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
resort_name | ✓ | |
visit_id | | | |
time | | |

Success response:
```javascript
{
    "success":true,
    "data":[
        {
            "time":1385319075,
            "resort_id":2376,
            "temperature":27.0688,
            "temperature_min":25,
            "temperature_max":30,
            "humidity":96,
            "pressure":2722,
            "conditions":'FEW',
            "conditions_full":'Partly Cloudy',
            "icon":"weather-partly-cloudy",
            "sunrise":1385474377,
            "sunset":1385509389,
            "wind_speed":10,
            "wind_bearing":90,
            "wind_chill":0,
            "freeze_level":0,
            "precip_type":'snow',
            "precip_amount":1,
            "precip_probability":40,
            "precip_depth":10,
            "num_lifts":0,
            "num_lifts_open":0,
            "num_runs":0,
            "num_trails_open":0
        },
        {
            "time":1385405475,
            "resort_id":2376,
            "temperature":27.0688,
            "temperature_min":25,
            "temperature_max":30,
            "humidity":96,
            "pressure":2722,
            "conditions":'FEW',
            "conditions_full":'Partly Cloudy',
            "icon":"weather-partly-cloudy",
            "sunrise":1385474377,
            "sunset":1385509389,
            "wind_speed":10,
            "wind_bearing":90,
            "wind_chill":0,
            "freeze_level":0,
            "precip_type":'snow',
            "precip_amount":1,
            "precip_probability":40,
            "precip_depth":10,
            "num_lifts":0,
            "num_lifts_open":0,
            "num_runs":0,
            "num_trails_open":0
        },
        {
            "time":1385491875,
            "resort_id":2376,
            "temperature":27.0688,
            "temperature_min":25,
            "temperature_max":30,
            "humidity":96,
            "pressure":2722,
            "conditions":'FEW',
            "conditions_full":'Partly Cloudy',
            "icon":"weather-partly-cloudy",
            "sunrise":1385474377,
            "sunset":1385509389,
            "wind_speed":10,
            "wind_bearing":90,
            "wind_chill":0,
            "freeze_level":0,
            "precip_type":'snow',
            "precip_amount":1,
            "precip_probability":40,
            "precip_depth":10,
            "num_lifts":0,
            "num_lifts_open":0,
            "num_runs":0,
            "num_trails_open":0
        }
    ]
}
```
#### GET resorts/[resort_name]/weather/report
Controller and action style: **{android,iphone}/get_resort_weather_report**
Authentication: **API user**
Authorization: **users**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
resort_name | ✓ | |
visit_id | | | |
time | | |

Success response:
```javascript
{
    "success":true,
    "data":[
        {
            "time":1385319075,
            "resort_id":2376,
            "temperature":27.0688,
            "temperature_min":25,
            "temperature_max":30,
            "humidity":96,
            "pressure":2722,
            "conditions":'FEW',
            "conditions_full":'Partly Cloudy',
            "icon":"weather-partly-cloudy",
            "sunrise":1385474377,
            "sunset":1385509389,
            "wind_speed":10,
            "wind_bearing":90,
            "wind_chill":0,
            "freeze_level":0,
            "precip_type":'snow',
            "precip_amount":1,
            "precip_probability":40,
            "precip_depth":10,
            "num_lifts":0,
            "num_lifts_open":0,
            "num_runs":0,
            "num_trails_open":0
        },
        {
            "time":1385405475,
            "resort_id":2376,
            "temperature":27.0688,
            "temperature_min":25,
            "temperature_max":30,
            "humidity":96,
            "pressure":2722,
            "conditions":'FEW',
            "conditions_full":'Partly Cloudy',
            "icon":"weather-partly-cloudy",
            "sunrise":1385474377,
            "sunset":1385509389,
            "wind_speed":10,
            "wind_bearing":90,
            "wind_chill":0,
            "freeze_level":0,
            "precip_type":'snow',
            "precip_amount":1,
            "precip_probability":40,
            "precip_depth":10,
            "num_lifts":0,
            "num_lifts_open":0,
            "num_runs":0,
            "num_trails_open":0
        },
        {
            "time":1385491875,
            "resort_id":2376,
            "temperature":27.0688,
            "temperature_min":25,
            "temperature_max":30,
            "humidity":96,
            "pressure":2722,
            "conditions":'FEW',
            "conditions_full":'Partly Cloudy',
            "icon":"weather-partly-cloudy",
            "sunrise":1385474377,
            "sunset":1385509389,
            "wind_speed":10,
            "wind_bearing":90,
            "wind_chill":0,
            "freeze_level":0,
            "precip_type":'snow',
            "precip_amount":1,
            "precip_probability":40,
            "precip_depth":10,
            "num_lifts":0,
            "num_lifts_open":0,
            "num_runs":0,
            "num_trails_open":0
        }
    ]
}

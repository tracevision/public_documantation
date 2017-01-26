
#### **GET users/[user_id]/visits**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
min_timestamp | | | Minimum UTC timestamp of visits update time
max_timestamp | | | Maximum UTC timestamp of visits update time
limit | | 50 |
visit_ids | | | json array of visit ids

Success Snow response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":471094,
         "single_run_mode":false,
         "update_time":"2017-01-26 14:16:23",
         "resort_title":"Val d'Isere",
         "runs":[
            {
               "run_id":4850356,
               "start_time":"2016-04-01 14:30:36",
               "resources":{
                  "jumps":[
                     {
                        "distance":2.4419995494634,
                        "duration":0.33300185203552,
                        "gforce":5.3709035319675,
                        "height":0.59593895736977,
                        "offset":1459521071.6496,
                        "speed":7.1196980273042,
                        "trick":{
                           "axis1":0.039645864460457,
                           "axis2":-0.35850088643961,
                           "axis3":0.93268715004185,
                           "rot_around_long":-0.51210683233678,
                           "rot_of_long":0.5241298343699,
                           "type":"no_trick"
                        }
                     },
                     {
                        "distance":2.8534357116959,
                        "duration":0.42500233650208,
                        "gforce":5.13740127473,
                        "height":0.92645835983842,
                        "offset":1459521580.6645,
                        "speed":6.4432445243061,
                        "trick":{
                           "axis1":0.11285327393817,
                           "axis2":-0.085716007304787,
                           "axis3":-0.98990752328344,
                           "rot_around_long":0.342419678682,
                           "rot_of_long":0.064446826579728,
                           "type":"no_trick"
                        }
                     },
                     {
                        "distance":1.4074998564738,
                        "duration":0.26400136947632,
                        "gforce":3.9077935180073,
                        "height":0.45582686637596,
                        "offset":1459521622.4897,
                        "speed":4.6299136061054,
                        "trick":{
                           "axis1":0.061205891092834,
                           "axis2":0.093237572179222,
                           "axis3":-0.99376083341499,
                           "rot_around_long":0.30311141533697,
                           "rot_of_long":0.093445807590609,
                           "type":"no_trick"
                        }
                     },
                     {
                        "distance":1.3797151085931,
                        "duration":0.35400199890137,
                        "gforce":4.1089065727429,
                        "height":0.67138307290254,
                        "offset":1459521693.8731,
                        "speed":3.853128598944,
                        "trick":{
                           "axis1":-0.019150636575317,
                           "axis2":-0.46252343973468,
                           "axis3":0.88640020352816,
                           "rot_around_long":0.56270289007265,
                           "rot_of_long":0.65504050488073,
                           "type":"no_trick"
                        }
                     }
                  ],
                  "trails":[
                     {
                        "key":"col$green#0",
                        "location":"val_d_is_re",
                        "name":"Col",
                        "time_end":1459521086.2,
                        "time_start":1459521084.2,
                        "type":"green"
                     },
                     {
                        "key":"pr_chemin$green#0",
                        "location":"val_d_is_re",
                        "name":"Pr\u00e9 Chemin",
                        "time_end":1459521145.2,
                        "time_start":1459521086.2,
                        "type":"green"
                     },
                     {
                        "key":"pont_abatte$green#0",
                        "location":"val_d_is_re",
                        "name":"Pont Abatte",
                        "time_end":1459521155.8,
                        "time_start":1459521145.2,
                        "type":"green"
                     },
                     {
                        "key":"vallon$green#0",
                        "location":"val_d_is_re",
                        "name":"Vallon",
                        "time_end":1459521190,
                        "time_start":1459521155.8,
                        "type":"green"
                     },
                     {
                        "key":"table_d_orientation$blue#0",
                        "location":"val_d_is_re",
                        "name":"Table d'Orientation",
                        "time_end":1459521317.8,
                        "time_start":1459521299.6,
                        "type":"blue"
                     },
                     {
                        "key":"pyramides$green#0",
                        "location":"val_d_is_re",
                        "name":"Pyramides",
                        "time_end":1459521379.8,
                        "time_start":1459521317.8,
                        "type":"green"
                     },
                     {
                        "key":"mangard$green#0",
                        "location":"val_d_is_re",
                        "name":"Mangard",
                        "time_end":1459521860.8,
                        "time_start":1459521379.8,
                        "type":"green"
                     }
                  ],
                  "lift_line":[
                     {
                        "lat":45.4425256,
                        "lon":7.0178029,
                        "alt":2316.6748046875
                     },
                     {
                        "lat":45.4208585,
                        "lon":7.0333155,
                        "alt":2772.5805664062
                     }
                  ],
                  "lift_name":"Vallon de l'Iseran",
                  "lo_res_track_id":"2a71d747c13ab111",
                  "hi_res_track_id":"23601071c5035a8e"
               },
               "total_distance":5188.7279469112,
               "max_speed":18.404461415646,
               "avg_speed":7.6339718031697,
               "sustained_speed":15.539868081808,
               "calories":124.85040312481,
               "jumps":4,
               "air_time":1.3760075569153,
               "calories_per_lb":0.0013872267013868,
               "slope_time":689.20000004768,
               "lift_time":583.20000004768,
               "rest_time":119,
               "vertical_drop":864.37202875439,
               "max_slope":0.77823395720266,
               "avg_slope":0.16593337251357,
               "lunch_time":0,
               "air_height":2.6496072564867,
               "max_air_height":0.92645835983842,
               "max_air_time":0.42500233650208,
               "max_air_distance":2.8534357116959
            }
         ],
         "date":"2016-04-01",
         "season":2015,
         "session_sheet":"...lic\/users\/73000\/73799\/visits\/471094\/session_sheet_472700.jpg?h=f02495ef",
         "track_lo_res":"...rs\/73000\/73799\/visits\/471094\/visit.trk",
         "track_hi_res":"...rs\/73000\/73799\/visits\/471094\/23601071c5035a8e.trk",
         "device_type":"trace",
         "resources":{
            "equipment":[
               "\"Head Adapt Edge 100 Mens Ski Boots\"",
               "\"Giro G10 Ski Helmet\"",
               "\"Jet Ski\""
            ]
         },
         "hide_resort":false,
         "total_distance":5188.7279469112,
         "max_speed":18.404461415646,
         "avg_speed":7.6339718031697,
         "sustained_speed":15.539868081808,
         "calories":0,
         "jumps":4,
         "air_time":1.3760075569153,
         "calories_per_lb":0.0020149677276796,
         "max_slope":0.77823395720266,
         "slope_time":689.20000004768,
         "lift_time":583.20000004768,
         "rest_time":1065.5999996662,
         "vertical_drop":864.37202875439,
         "avg_slope":0.16593337251357,
         "lunch_time":0,
         "air_height":2.6496072564867,
         "max_air_height":0.92645835983842,
         "max_air_time":0.42500233650208,
         "max_air_distance":2.8534357116959,
         "num_runs":1
      }
   ]
}
```

Success Surf response for 'surfing' or 'sup_surf' sport subtype:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":1376,
         "single_run_mode":false,
         "update_time":"2017-01-26 13:39:38",
         "resort_title":"Soup Bowl",
         "runs":[
            {
               "run_id":15664,
               "start_time":"2017-01-25 19:41:12",
               "resources":{
                  "jumps":[
                     {
                        "bottom_turn":{
                           "angle":1.8699396778068,
                           "duration":1.175999879837,
                           "initial_speed":8.7295263195981,
                           "offset":1485373280.459,
                           "roll_angle":0.51276703108477,
                           "speed_gain":0.113328907107,
                           "vertical":0.99539294943257
                        },
                        "duration":0.5460000038147,
                        "height":0.64989288908112,
                        "offset":1485373281.774
                     }
                  ],
                  "cutbacks":[
                     {
                        "angle":1.5937639062672,
                        "bottom_turn":{
                           "angle":1.4360453440163,
                           "duration":0.70600008964539,
                           "initial_speed":6.994177087394,
                           "offset":1485373275.69,
                           "roll_angle":0.63726825816211,
                           "speed_gain":0,
                           "vertical":0.72137138406873
                        },
                        "duration":0.65199995040894,
                        "offset":1485373276.396,
                        "pitch_angle":0.72583530618141,
                        "power":1.3395083656816,
                        "relaxed":true,
                        "roll_angle":1.2914429694268,
                        "speed":6.2930058100068
                     }
                  ],
                  "turns":[

                  ],
                  "lo_res_track_id":"954737de3394555f",
                  "hi_res_track_id":"7d048fb72f190c58",
                  "paddle_tracks_ids":[
                     "77fc3729c4cacf40"
                  ]
               },
               "total_distance":93.942272680377,
               "max_speed":9.0647890212624,
               "avg_speed":6.0007839573338,
               "sustained_speed":0,
               "calories":27.974939874186,
               "jumps":1,
               "air_time":0.5460000038147,
               "calories_per_lb":0.00051330164906763,
               "ride_time":15.65499997139,
               "paddle_time":235.40799999237,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":140.18704956339,
               "turns_num":1,
               "sharpest_turn":1.5937639062672,
               "distance_stroke":0,
               "speed_gain_stroke":0,
               "stroke_rate":0,
               "strokes_side":0,
               "air_height":0.64989288908112,
               "max_air_height":0.64989288908112,
               "max_air_time":0.5460000038147,
               "max_air_distance":0
            }
         ],
         "date":"2017-01-25",
         "season":2016,
         "session_sheet":"...surf_sessions\/1376\/session_sheet_473425.jpg?h=6ba832d8",
         "track_lo_res":"...lic\/users\/0000\/339\/surf_sessions\/1376\/visit.trk",
         "track_hi_res":"...lic\/users\/0000\/339\/surf_sessions\/1376\/7d048fb72f190c58.trk",
         "track_paddle":"...lic\/users\/0000\/339\/surf_sessions\/1376\/paddle.trk",
         "device_type":"trace",
         "sport":"surfing",
         "resources":{
            "equipment":[

            ]
         },
         "hide_resort":false,
         "total_distance":93.942272680377,
         "max_speed":9.0647890212624,
         "avg_speed":6.0007839573338,
         "sustained_speed":0,
         "calories":27.974939874186,
         "jumps":1,
         "air_time":0.5460000038147,
         "calories_per_lb":0.00051330164906763,
         "ride_time":15.65499997139,
         "paddle_time":235.40799999237,
         "wait_time":1080.9989998341,
         "waves_missed":0,
         "paddle_distance":140.18704956339,
         "longest_ride":93.942272680377,
         "turns_num":1,
         "sharpest_turn":1.5937639062672,
         "distance_stroke":0,
         "speed_gain_stroke":0,
         "stroke_rate":0,
         "strokes_side":0,
         "air_height":0.64989288908112,
         "max_air_height":0.64989288908112,
         "max_air_time":0.5460000038147,
         "max_air_distance":0,
         "num_waves":1
      }
   ]
}
```

Success Surf response for 'windkite', 'wind' and 'kite' sport subtype:

```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":1376,
         "single_run_mode":false,
         "update_time":"2017-01-26 14:02:19",
         "resort_title":"Soup Bowl",
         "runs":[
            {
               "run_id":15667,
               "start_time":"2017-01-25 19:41:07",
               "resources":{
                  "jumps":[
                     {
                        "distance":11.875275717818,
                        "duration":1.1619999408722,
                        "gforce":0.63277215978198,
                        "height":0.52396747081169,
                        "offset":1485373273.276,
                        "speed":3.6951454639838,
                        "trick":{
                           "axis1":-0.026244240116052,
                           "axis2":-0.75335668956904,
                           "axis3":0.65708822706111,
                           "rot_around_long":0.32764904880755,
                           "rot_of_long":-0.10861446021706,
                           "type":"no_trick"
                        }
                     },
                     {
                        "distance":15.098997228737,
                        "duration":1.9740002155304,
                        "gforce":1.6881989215141,
                        "height":1.2789474495229,
                        "offset":1485373276.701,
                        "speed":6.6266884640822,
                        "trick":{
                           "axis1":-0.98744687212582,
                           "axis2":-0.14484549308018,
                           "axis3":-0.062995697180859,
                           "rot_around_long":0.51285727869438,
                           "rot_of_long":9.8267814422558,
                           "type":"unknown_trick"
                        }
                     }
                  ],
                  "cutbacks":[

                  ],
                  "turns":[

                  ],
                  "lo_res_track_id":"472217babbd8121b",
                  "hi_res_track_id":"85791012197062f6"
               },
               "total_distance":127.10190040387,
               "max_speed":9.3785340005781,
               "avg_speed":3.3613794791456,
               "sustained_speed":5.2974805332346,
               "calories":2.7255856384104,
               "jumps":2,
               "air_time":3.1360001564026,
               "calories_per_lb":"0.000050010745658907",
               "ride_time":37.799999952316,
               "paddle_time":0,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":0,
               "turns_num":0,
               "sharpest_turn":0,
               "distance_stroke":0,
               "speed_gain_stroke":0,
               "stroke_rate":0,
               "strokes_side":0,
               "air_height":1.8029149203346,
               "max_air_height":1.2789474495229,
               "max_air_time":1.9740002155304,
               "max_air_distance":15.098997228737
            }
         ],
         "date":"2017-01-25",
         "season":2016,
         "session_sheet":"...lic\/users\/0000\/339\/surf_sessions\/1376\/session_sheet_473425.jpg?h=6ba832d8",
         "track_lo_res":"...lic\/users\/0000\/339\/surf_sessions\/1376\/visit.trk",
         "track_hi_res":"...lic\/users\/0000\/339\/surf_sessions\/1376\/85791012197062f6.trk",
         "device_type":"trace",
         "sport":"kite",
         "resources":{
            "equipment":[

            ]
         },
         "hide_resort":false,
         "total_distance":127.10190040387,
         "max_speed":9.3785340005781,
         "avg_speed":3.3613794791456,
         "sustained_speed":5.2974805332346,
         "calories":2.7255856384104,
         "jumps":2,
         "air_time":3.1360001564026,
         "calories_per_lb":5.0010745658907e-5,
         "ride_time":37.799999952316,
         "paddle_time":0,
         "wait_time":0,
         "waves_missed":0,
         "paddle_distance":0,
         "longest_ride":127.10190040387,
         "turns_num":0,
         "sharpest_turn":0,
         "distance_stroke":0,
         "speed_gain_stroke":0,
         "stroke_rate":0,
         "strokes_side":0,
         "air_height":1.8029149203346,
         "max_air_height":1.2789474495229,
         "max_air_time":1.9740002155304,
         "max_air_distance":15.098997228737,
         "num_waves":1
      }
   ]
}
```

#### **GET users/self/visits**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
min_timestamp | | | Minimum UTC timestamp of visits update time
max_timestamp | | | Maximum UTC timestamp of visits update time
limit | | 50 |
visit_ids | | | json array of visit ids

Response format is the same as for **GET users/[user_id]/visits**.

#### **GET users/[user_id]/visits/list**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":390930,
         "update_time":"2013-03-15 18:08:55",
         "session_sheet":"https:\/\/...com\/public\/users\/73000\/73799\/visits\/390930\/session_sheet.jpg?h=82fc3a31",
         "date":"2013-03-15",
         "resort_title":"Unknown resort"
      },
      {
         "visit_id":469706,
         "update_time":"2014-10-06 14:20:48",
         "session_sheet":"http:\/\/...com\/stats\/get_stats_image?iId=469396",
         "date":"2014-01-15",
         "resort_title":"Killington"
      }
   ]
}
```

#### **GET users/self/visits/list**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":390930,
         "update_time":"2013-03-15 18:08:55",
         "session_sheet":"https:\/\/...com\/public\/users\/73000\/73799\/visits\/390930\/session_sheet.jpg?h=82fc3a31",
         "date":"2013-03-15",
         "resort_title":"Unknown resort"
      },
      {
         "visit_id":469706,
         "update_time":"2014-10-06 14:20:48",
         "session_sheet":"http:\/\/...com\/stats\/get_stats_image?iId=469396",
         "date":"2014-01-15",
         "resort_title":"Killington"
      }
   ]
}
```


#### **POST users/self/visit-overlay**
Description: With this call you can upload a track file with data in it (our usual track files either from Trace or from the phone app) and we'll create our video overlay in 1080p with stats like speed, altitude drop, jump information, etc. The overlay has a transparent alpha channel, so you can then use this file in your favorite video editor to create the stats overlay that you want. The link for the resultant video file will be sent to the user's email in the database.

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
data | ✓ | | Track file
client[version] | | |

Success response:
```javascript
{
   "success":true,
   "data":{
      "visit_id":129308,
      "upload_id":239888,
      "session_sheet":{
         "max_speed":24.64,
         "max_speed_rank":1,
         "vertical_drop":8264.7516557993,
         "vertical_drop_rank":2,
         "calories":1519.5797170011,
         "calories_rank":2,
         "air_time":0.39900302886963,
         "air_time_rank":12,
         "jumps":1,
         "jumps_rank":10,
         "total_distance":31829.223305705,
         "total_distance_rank":6,
         "runs":19
      }
   }
}
```




#### **POST visits/[visit_id]/comment**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
facebook | | | Create post in Facebook
twitter | | | Create post in Twitter
photo | | | Photo file
hide_resort_name | | 0 | [0,1] If resort name must be shown as a 'Secret Spot'
comment | | |
equipment | | |  comma-separated values string, up to 1000 characters in total


Success response:
```javascript
{
   "success":true,
   "data":[]
}
```


#### **POST visits/[visit_id]/photo**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
photo | ✓ | | Photo file

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```


#### **POST visits/[visit_id]/share**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats | ✓ | | JSON array of stat names
comment | | |
photo | | | Photo file
facebook | | | Create post on Facebook
twitter | | | Create post in Twitter

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```


#### **POST visits/[visit_id]/export**

No request parameters.

Success response:
```javascript
{
   "success":true,
   "data":{
        "gpx_link": "http://.../visit.gpx"
   }
}
```

#### **GET visits/[visit_id]/weather**

No request parameters (except visit_id in URL).

Success Ski response:
```javascript
{
   "success":true,
   "data":{
       "time":1428660000,
       "wind_strength":0,
       "resort_id":3880,
       "temperature":-27.921,
       "temperature_min":0,
       "temperature_max":0,
       "humidity":13,
       "pressure":1166,
       "reported_snow_fall":0,
       "reported_snow_fall_48":0,
       "reported_snow_fall_72":0,
       "num_lifts":0,
       "num_lifts_open":0,
       "num_runs":0,
       "num_trails_open":0,
       "base_depth":0,
       "icon":"weather-partly-cloudy",
       "wind_speed":0,
       "sunrise":1428640029,
       "sunset":1428688168,
       "precip_depth":0
   }
}
```

Success Surf response:
```javascript
{
   "success":true,
   "data":{
       "time":1431403200,
       "wind_strength":0,
       "beach_id":26208,
       "icon":"weather-partly-cloudy",
       "wind_speed":0,
       "sunrise":1431376450,
       "sunset":1431414361
   }
}
```
Note: data part might be empty if no resort is bound to the visit or no weather for resort is available at the visit date.

#### **GET visits/[visit_id]/equipment**

No request parameters (except visit_id in URL).

Success response:
```javascript
{
   "success":true,
   "data":{
       "equipment":["GNARLOO FLOUNDER POUNDER FISH 5'6\"","QUIKSILVER SYNCRO 3/2MM BZ"]
   }
}
```

#### **POST visits/[visit_id]/equipment**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
equipment | | |  comma-separated values string, up to 1000 characters in total

Success response:
```javascript
{
   "success":true,
   "data":[]
}
```

#### POST visits/[visit_id]/stats/compare

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats| | | json array of stat type strings

Success response:
```javascript
{
   "success":true,
   "data":
   {
      "jumps":
      {
         "users":[
            {
               "user_name":"John Smith",
               "user_id":259957,
               "pic_url":"https://...",
               "value":0,
               "source":"user"
            }
         ]
      },
      "total_distance":
      {
         "users":[
            {
               "user_name":"John Smith",
               "user_id":259957,
               "pic_url":"https://...",
               "value":0,
               "source":"user"
            }
         ]
      }
   }
}
```

#### POST visits/[visit_id]/stats/progression

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
stats| ✓ | | json array of stat type strings
time_scale| | | "day", "month", or "year" (optional, defaults to "day")
start_date| | | "YYYY-MM-DD" date minimum time stamp for any stat values in response (optional, defaults to 30 days ago)
end_date| | | "YYYY-MM-DD" date maximum time stamp for any stat values in response (optional defaults to now)
sport | | | 

Success response:
The same form as for users/self/stats/progression


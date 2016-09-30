
#### **GET users/[user_id]/visits**

Request Parameter | Mandatory | Default value | Comments
--- |:---:| --- | ---
min_timestamp | | | Minimum UTC timestamp of visits update time
max_timestamp | | | Maximum UTC timestamp of visits update time
limit | | 50 |
visit_ids | | | json array of visit ids

Success AlpineReplay response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":1455404,
         "single_run_mode":false,
         "update_time":"2015-11-15 06:00:47",
         "resort_title":"Lake Louise",
         "runs":[
            {
               "run_id":15287795,
               "start_time":"2015-11-14 18:28:35",
               "resources":{
                  "jumps":[
                     {
                        "distance":4.6933734661423,
                        "duration":0.59797406196594,
                        "height":1.5119494078036,
                        "offset":1447525787.8578,
                        "speed":7.86,
                        "trick":{
                           "axis1":0,
                           "axis2":0,
                           "axis3":0,
                           "rot_around_long":0,
                           "rot_of_long":0
                        }
                     },
                     {
                        "distance":3.9940184565235,
                        "duration":0.49497866630554,
                        "height":1.1419289122829,
                        "offset":1447526803.1611,
                        "speed":8.56,
                        "trick":{
                           "axis1":0,
                           "axis2":0,
                           "axis3":0,
                           "rot_around_long":0,
                           "rot_of_long":0
                        }
                     }
                  ],
                  "trails":[
                     {
                        "key":"home_run$blue#0",
                        "location":"lake_louise",
                        "name":"Home Run",
                        "time_end":1447525841.995,
                        "time_start":1447525163.999,
                        "type":"blue"
                     },
                     {
                        "key":"charlie_s_choice$blue#0",
                        "location":"lake_louise",
                        "name":"Charlie's Choice",
                        "time_end":1447525855.995,
                        "time_start":1447525841.995,
                        "type":"blue"
                     },
                     {
                        "key":"gully$blue#0",
                        "location":"lake_louise",
                        "name":"Gully",
                        "time_end":1447526522.999,
                        "time_start":1447526168.999,
                        "type":"blue"
                     }
                  ],
                  "lift_line":[
                     {
                        "lat":51.4530698,
                        "lon":-116.141247,
                        "alt":2131.5107421875
                     },
                     {
                        "lat":51.4623423,
                        "lon":-116.1352671,
                        "alt":2448.9736328125
                     }
                  ],
                  "lift_name":"Top of the World Express",
                  "lo_res_track_id":"615a92f684591e75",
                  "hi_res_track_id":"690a2031411bd31a"
               },
               "total_distance":4001.0007059669,
               "max_speed":14.12,
               "avg_speed":5.7636141853206,
               "calories":91.903624849708,
               "jumps":2,
               "air_time":1.0929527282715,
               "calories_per_lb":0.0017019189786983,
               "slope_time":735.99500012398,
               "lift_time":1025.0000002384,
               "rest_time":475.0039999485,
               "vertical_drop":849.9924137931,
               "max_slope":0.42261614853455,
               "avg_slope":0.17017029463648,
               "sustained_speed":12.73,
               "lunch_time":0
            }
         ],
         "date":"2015-11-14",
         "season":2015,
         "session_sheet":".../users\/522000\/522521\/visits\/1455404\/session_sheet_1510713.jpg?h=5e76bb52",
         "track_lo_res":".../users\/522000\/522521\/visits\/1455404\/visit.trk",
         "track_hi_res":".../users\/522000\/522521\/visits\/1455404\/690a2031411bd31a.trk",
         "device_type":"phone",
         "resources":{
            "equipment":[
               "Head Adapt Edge 100 Mens Ski Boots",
               "Giro G10 Ski Helmet"
            ]
         },
         "hide_resort":false,
         "total_distance":4001.0007059669,
         "max_speed":14.12,
         "avg_speed":5.7636141853206,
         "calories":153.50441426301,
         "jumps":2,
         "air_time":1.0929527282715,
         "calories_per_lb":0.0028426743382038,
         "max_slope":0.42261614853455,
         "slope_time":735.99500012398,
         "lift_time":1025.0000002384,
         "rest_time":979.3639998436,
         "vertical_drop":849.9924137931,
         "avg_slope":0.17017029463648,
         "sustained_speed":12.73,
         "lunch_time":0
      }
   ]
}
```

Success SurfReplay response for 'surfing' or 'sup_surf' sport subtype:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":1306,
         "single_run_mode":false,
         "update_time":"2016-09-30 12:41:01",
         "resort_title":"Mission Beach",
         "runs":[
            {
               "run_id":14859,
               "start_time":"2016-08-10 17:14:51",
               "resources":{
                  "jumps":[
                     {
                        "bottom_turn":{
                           "angle":1.063141039714,
                           "duration":0.56400585174561,
                           "initial_speed":5.5531547348587,
                           "offset":1470849324.2438,
                           "roll_angle":0.5662238709555,
                           "speed_gain":0,
                           "vertical":1.1053572864652
                        },
                        "duration":0.4450044631958,
                        "height":0.43170315953592,
                        "offset":1470849325.1778
                     }
                  ],
                  "cutbacks":[
                     {
                        "angle":3.8860248941471,
                        "bottom_turn":{
                           "angle":1.063141039714,
                           "duration":0.56400585174561,
                           "initial_speed":5.5531547348587,
                           "offset":1470849324.2438,
                           "roll_angle":0.5662238709555,
                           "speed_gain":0,
                           "vertical":1.1053572864652
                        },
                        "duration":1.7160172462463,
                        "offset":1470849324.8078,
                        "pitch_angle":1.1237543427608,
                        "power":8.582133845308,
                        "relaxed":false,
                        "roll_angle":1.6302825681822,
                        "speed":5.578005072276
                     }
                  ],
                  "turns":[

                  ],
                  "lo_res_track_id":"36d68ca4efd02c80",
                  "hi_res_track_id":"95d0780c6ff5599b",
                  "paddle_tracks_ids":[
                     "6336d6541741eb99",
                     "17d2129ec32247b4",
                     "aa77b48f1b25014e"
                  ]
               },
               "total_distance":274.29820677809,
               "max_speed":6.2411841466674,
               "avg_speed":4.4851795013269,
               "sustained_speed":0,
               "calories":12.56680380362,
               "jumps":1,
               "air_time":0.4450044631958,
               "calories_per_lb":0.00023058355602972,
               "ride_time":61.156572818756,
               "paddle_time":23.457236766815,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":15.030122374055,
               "turns_num":1,
               "sharpest_turn":3.8860248941471,
               "distance_stroke":0,
               "speed_gain_stroke":0,
               "stroke_rate":0,
               "strokes_side":0
            }
         ],
         "date":"2016-08-10",
         "season":2016,
         "session_sheet":"http:\/\/...\/stats\/get_stats_image?iId=473226",
         "track_lo_res":"http:\/\/...\/users\/0000\/300\/surf_sessions\/1306\/visit.trk",
         "track_hi_res":"http:\/\/...\/users\/0000\/300\/surf_sessions\/1306\/95d0780c6ff5599b.trk",
         "track_paddle":"http:\/\/...\/users\/0000\/300\/surf_sessions\/1306\/paddle.trk",
         "device_type":"trace",
         "sport":"surfing",
         "resources":{
            "equipment":[

            ]
         },
         "hide_resort":false,
         "total_distance":274.29820677809,
         "max_speed":6.2411841466674,
         "avg_speed":4.4851795013269,
         "sustained_speed":0,
         "calories":12.56680380362,
         "jumps":1,
         "air_time":0.4450044631958,
         "calories_per_lb":0.00023058355602972,
         "ride_time":61.156572818756,
         "paddle_time":23.457236766815,
         "wait_time":15.400000095367,
         "waves_missed":0,
         "paddle_distance":15.030122374055,
         "longest_ride":274.29820677809,
         "turns_num":1,
         "sharpest_turn":3.8860248941471,
         "distance_stroke":0,
         "speed_gain_stroke":0,
         "stroke_rate":0,
         "strokes_side":0
      }
   ]
}
```

Success SurfReplay response for 'windkite', 'wind' and 'kite' sport subtype (12 waves is cut to shorten example:

```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":1308,
         "single_run_mode":false,
         "update_time":"2016-09-30 12:49:03",
         "resort_title":"Figure Eight and Shell Islands",
         "runs":[
            {
               "run_id":14868,
               "start_time":"2016-09-11 21:21:28",
               "resources":{
                  "jumps":[
                     {
                        "distance":11.917648278056,
                        "duration":2.0500130653381,
                        "gforce":0.52660864281948,
                        "height":1.3856917561109,
                        "offset":1473629143.5796,
                        "speed":6.0952768599958,
                        "trick":{
                           "axis1":-0.12687104266097,
                           "axis2":-0.6951409494157,
                           "axis3":-0.70758942825593,
                           "rot_around_long":-0.59072666166167,
                           "rot_of_long":1.6008627487356,
                           "type":"no_trick"
                        }
                     },
                     {
                        "distance":7.521914399517,
                        "duration":1.0540065765381,
                        "gforce":1.65177683067,
                        "height":0.40207357458691,
                        "offset":1473629395.1092,
                        "speed":7.7214765427346,
                        "trick":{
                           "axis1":0.094959658036419,
                           "axis2":-0.53799943634845,
                           "axis3":-0.83757941106164,
                           "rot_around_long":-0.53709817089488,
                           "rot_of_long":0.74015373083628,
                           "type":"no_trick"
                        }
                     }
                  ],
                  "cutbacks":[

                  ],
                  "turns":[

                  ],
                  "lo_res_track_id":"e5d110df7c2e8941",
                  "hi_res_track_id":"d71fa39417166d4f"
               },
               "total_distance":5127.2168550269,
               "max_speed":9.6862841172454,
               "avg_speed":5.9358993427024,
               "sustained_speed":6.8935114419286,
               "calories":88.631080766341,
               "jumps":2,
               "air_time":3.1040196418762,
               "calories_per_lb":0.0016262583626852,
               "ride_time":863.59999990463,
               "paddle_time":0,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":0,
               "turns_num":0,
               "sharpest_turn":0,
               "distance_stroke":0,
               "speed_gain_stroke":0,
               "stroke_rate":0,
               "strokes_side":0
            }
         ],
         "date":"2016-09-11",
         "season":2016,
         "session_sheet":"http:\/\/...\/stats\/get_stats_image?iId=473228",
         "track_lo_res":"http:\/\/...\/users\/0000\/302\/surf_sessions\/1308\/visit.trk",
         "track_hi_res":"http:\/\/...\/users\/0000\/302\/surf_sessions\/1308\/d71fa39417166d4f.trk",
         "device_type":"trace",
         "sport":"kite",
         "resources":{
            "equipment":[

            ]
         },
         "hide_resort":false,
         "total_distance":5127.2168550269,
         "max_speed":9.6862841172454,
         "avg_speed":5.9358993427024,
         "sustained_speed":6.8935114419286,
         "calories":88.631080766341,
         "jumps":2,
         "air_time":3.1040196418762,
         "calories_per_lb":0.0016262583626852,
         "ride_time":863.59999990463,
         "paddle_time":0,
         "wait_time":0,
         "waves_missed":0,
         "paddle_distance":0,
         "longest_ride":5127.2168550269,
         "turns_num":0,
         "sharpest_turn":0,
         "distance_stroke":0,
         "speed_gain_stroke":0,
         "stroke_rate":0,
         "strokes_side":0
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


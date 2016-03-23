
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
         "visit_id":971,
         "single_run_mode":false,
         "update_time":"2015-02-03 15:55:48",
         "resort_title":"Unknown beach",
         "runs":[
            {
               "run_id":14717,
               "start_time":"2015-01-16 22:52:10",
               "resources":{
                  "jumps":[
                     {
                        "duration":0.23737764358521,
                        "height":0.12283895756946,
                        "offset":1421448732.6146
                     },
                     {
                        "duration":0.17272996902466,
                        "height":0.065041699994385,
                        "offset":1421448733.1318
                     },
                     {
                        "duration":0.10808253288269,
                        "height":0.025466397933257,
                        "offset":1421448733.4328
                     }
                  ],
                  "turns":[

                  ],
                  "cutbacks":[
                     {
                        "angle":3.1975215476702,
                        "duration":0.79698204994202,
                        "offset":1421448731.0752,
                        "pitch_angle":1.3019902427897,
                        "roll_angle":1.4972622387144,
                        "speed":0
                     },
                     {
                        "angle":2.9496673447171,
                        "duration":0.57071566581726,
                        "offset":1421448734.6399,
                        "pitch_angle":1.1120858958012,
                        "roll_angle":1.5147551703502,
                        "speed":0
                     }
                  ],
                  "lo_res_track_id":"6336d6541741eb99",
                  "hi_res_track_id":"05f49d77d2557f54"
               },
               "total_distance":0,
               "max_speed":0,
               "avg_speed":0,
               "calories":0,
               "jumps":3,
               "air_time":0.51819014549256,
               "calories_per_lb":0,
               "ride_time":4.3828964233398,
               "paddle_time":0,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":0,
               "turns_num":2,
               "sharpest_turn":3.1975215476702,
               "distance_stroke":0,
               "speed_gain_stroke":0,
               "stroke_rate":0,
               "strokes_side":0
            }
         ],
         "date":"2015-01-16",
         "season":2014,
         "session_sheet":".../users\/429000\/429174\/surf_sessions\/971\/session_sheet_1081111.jpg?h=6c41251c",
         "track_lo_res":".../users\/429000\/429174\/surf_sessions\/971\/visit.trk",
         "track_hi_res":".../users\/429000\/429174\/surf_sessions\/971\/05f49d77d2557f54.trk",
         "device_type":"trace",
         "sport":"surfing",
         "resources":{
            "equipment":[
               "GNARLOO FLOUNDER POUNDER FISH 5'6\"",
               "QUIKSILVER SYNCRO 3/2MM BZ"
            ]
         },
         "hide_resort":false,
         "total_distance":0,
         "max_speed":0,
         "avg_speed":0,
         "calories":1.0359803475684,
         "jumps":3,
         "air_time":0.51819014549256,
         "calories_per_lb":"0.000019008813716852",
         "ride_time":4.3828964233398,
         "paddle_time":0,
         "wait_time":0.20000290870667,
         "waves_missed":0,
         "paddle_distance":0,
         "longest_ride":0,
         "turns_num":2,
         "sharpest_turn":3.1975215476702,
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
         "visit_id":7256,
         "single_run_mode":false,
         "update_time":"2015-11-14 15:04:48",
         "resort_title":"Kijkduin",
         "runs":[
            {
               "run_id":235563,
               "start_time":"2015-11-10 15:45:25",
               "resources":{
                  "jumps":[
                     {
                        "distance":0,
                        "duration":1.3040120601654,
                        "height":0,
                        "offset":1447170378.6222,
                        "speed":8.0176368089357,
                        "trick":{
                           "axis1":0.71281006205366,
                           "axis2":0.18001321046891,
                           "axis3":0.67786212424927,
                           "rot_around_long":4.2752394938352,
                           "rot_of_long":6.8749633674519
                        }
                     }
                  ],
                  "cutbacks":[

                  ],
                  "turns":[
                     {
                        "duration":0.19999980926514,
                        "offset":1447170387.4,
                        "speed":2.5538362231201,
                        "time_upsidedown":0,
                        "turn_upsidedown":false
                     }
                  ],
                  "lo_res_track_id":"46f2e8b497ea6fad",
                  "hi_res_track_id":"bb80b5fcb951017d"
               },
               "total_distance":351.30687837396,
               "max_speed":10.215674231298,
               "avg_speed":6.1506674600359,
               "calories":8416.590646966,
               "jumps":1,
               "air_time":1.3040120601654,
               "calories_per_lb":0.12948600995332,
               "ride_time":62.200000047684,
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
         "date":"2015-11-10",
         "season":2015,
         "session_sheet":".../users\/397000\/397760\/surf_sessions\/7256\/session_sheet_1509266.jpg?h=f4e8af4c",
         "track_lo_res":".../users\/397000\/397760\/surf_sessions\/7256\/visit.trk",
         "track_hi_res":".../users\/397000\/397760\/surf_sessions\/7256\/4e6a209eb430c83f.trk",
         "device_type":"trace",
         "sport":"windkite",
         "resources":{
            "equipment":[
               "GNARLOO FLOUNDER POUNDER FISH 5'6\"",
               "QUIKSILVER SYNCRO 3/2MM BZ"
            ]
         },
         "hide_resort":false,
         "total_distance":2625.1763708054,
         "max_speed":11.092384775151,
         "avg_speed":5.6100173655587,
         "calories":68539.638970828,
         "jumps":5,
         "air_time":8.0380740165711,
         "calories_per_lb":1.0544559841666,
         "ride_time":463.99999976158,
         "paddle_time":0,
         "wait_time":0,
         "waves_missed":0,
         "paddle_distance":0,
         "longest_ride":366.74450006541,
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
       "wave_height":1.9584,
       "wave_bearing":213,
       "wave_period":10.2,
       "tide":1.083135,
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

Success response:
The same form as for users/self/stats/progression


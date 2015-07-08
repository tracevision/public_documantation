
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
         "visit_id":129593,
         "single_run_mode":false,
         "update_time":"2014-07-24 08:17:36",
         "resort_title":"Sugarloaf",
         "runs":{
            {
               "run_id":1451367,
               "start_time":"2014-03-02 17:08:03",
               "resources":{
                  "jumps":[
                     {
                        "duration":0.62702536582947,
                        "offset":1393782999.9713,
                        "speed":0.14173210109706
                     }
                  ],
                  "trails":[
                     {
                        "key":"upper_narrow_gauge$black#0",
                        "location":"sugarloaf",
                        "name":"Upper Narrow Gauge",
                        "time_end":1393782729,
                        "time_start":1393782640,
                        "type":"black"
                     },
                     {
                        "key":"lower_narrow_gauge$green#0",
                        "location":"sugarloaf",
                        "name":"Lower Narrow Gauge",
                        "time_end":1393782939,
                        "time_start":1393782869,
                        "type":"green"
                     }
                  ],
                  "lift_line":[
                     {
                        "lat":45.04465,
                        "lon":-70.31224,
                        "alt":731.75048828125
                     },
                     {
                        "lat":45.03491,
                        "lon":-70.31679,
                        "alt":1165.6518554688
                     }
                  ],
                  "lift_name":"Skyline",
                  "lo_res_track_id":"89e7effd25ea3dd0"
                  "hi_res_track_id":"993c67f2f7f03b01"
               },
               "total_distance":2412.25,
               "max_speed":21.5,
               "avg_speed":13.195355191257,
               "calories":31.962116868798,
               "jumps":1,
               "air_time":0.62702536582947,
               "calories_per_lb":0.00058646085997795,
               "slope_time":182,
               "lift_time":525,
               "rest_time":170,
               "vertical_drop":625,
               "max_slope":0.5114716783443,
               "avg_slope":0.24140107846186,
               "sustained_speed":18.5,
               "lunch_time":0
            }
         },
         "date":"2014-03-02",
         "season":2013,
         "session_sheet":"http:\/\/...com\/users\/72000\/72027\/visits\/129593\/session_sheet_129119.jpg?h=9b446842",
         "track_lo_res":"http:\/\/...com\/users\/72000\/72027\/visits\/129593\/visit.trk",
         "track_hi_res":"http:\/\/...com\/users\/72000\/72027\/visits\/129593\/993c67f2f7f03b01.trk",
         "device_type":"trace",
         "total_distance":28817.274209236,
         "max_speed":24,
         "avg_speed":9.1546521597203,
         "calories":1098.2559027617,
         "jumps":9,
         "air_time":4.7254085540771,
         "calories_per_lb":0.020151484454343,
         "max_slope":0.84268901530484,
         "slope_time":3428,
         "lift_time":9635,
         "rest_time":3335.4760000706,
         "vertical_drop":6653.4101745876,
         "avg_slope":0.20432066521036,
         "sustained_speed":19.75,
         "lunch_time":0
      }
   ]
}
```

Success SurfReplay response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":710,
         "single_run_mode":false,
         "update_time":"2015-06-18 13:58:05",
         "resort_title":"Lower Trestles",
         "runs":[
            {
               "run_id":6728,
               "start_time":"2015-06-11 15:12:49",
               "resources":{
                  "jumps":[
                     {
                        "bottom_turn":{
                           "angle":2.0449782177287,
                           "duration":0.91000270843506,
                           "initial_speed":9.8748835109338,
                           "offset":1434035574.4419,
                           "roll_angle":0.77971739233362,
                           "speed_gain":0.99871869878497,
                           "vertical":66.932779820941
                        },
                        "duration":0.38100099563599,
                        "height":0.31645263391284,
                        "offset":1434035575.4309
                     }
                  ],
                  "cutbacks":[
                     {
                        "angle":4.2269022388381,
                        "bottom_turn":{
                           "angle":2.3531268564004,
                           "duration":1.0000030994415,
                           "initial_speed":8.3040393283667,
                           "offset":1434035577.4849,
                           "roll_angle":1.1135685537327,
                           "speed_gain":0.72827139422401,
                           "vertical":50.387893062057
                        },
                        "duration":1.4480042457581,
                        "offset":1434035578.4849,
                        "pitch_angle":0.88292636603308,
                        "power":9.1181047180415,
                        "roll_angle":1.395900988425,
                        "speed":7.0556366238778
                     }
                  ],
                  "lo_res_track_id":"f62821216756647f",
                  "hi_res_track_id":"17b4d701f0581475"
               },
               "total_distance":92.069442184946,
               "max_speed":11.026549777696,
               "avg_speed":6.4487753557003,
               "calories":8.7360104541531,
               "jumps":1,
               "air_time":0.38100099563599,
               "calories_per_lb":0.00034944041816612,
               "ride_time":14.277042865753,
               "paddle_time":147.60544347763,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":145.0574779941,
               "turns_num":1,
               "sharpest_turn":4.2269022388381
            }
         ],
         "date":"2015-06-11",
         "season":2015,
         "session_sheet":"...com\/stats\/get_stats_image?iId=471787",
         "track_lo_res":"...com\/users\/71000\/71202\/surf_sessions\/710\/visit.trk",
         "track_hi_res":"...com\/users\/71000\/71202\/surf_sessions\/710\/17b4d701f0581475.trk",
         "device_type":"trace",
         "total_distance":92.069442184946,
         "max_speed":11.026549777696,
         "avg_speed":6.4487753557003,
         "calories":8.736010454153,
         "jumps":1,
         "air_time":0.38100099563599,
         "calories_per_lb":0.00034944041816612,
         "ride_time":14.277042865753,
         "paddle_time":147.60544347763,
         "wait_time":69.401000499725,
         "waves_missed":0,
         "paddle_distance":145.0574779941,
         "longest_ride":92.069442184946,
         "turns_num":1,
         "sharpest_turn":4.2269022388381
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

Success AlpineReplay response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":129593,
         "single_run_mode":false,
         "update_time":"2014-07-24 08:17:36",
         "resort_title":"Sugarloaf",
         "runs":{
            {
               "run_id":1451367,
               "start_time":"2014-03-02 17:08:03",
               "resources":{
                  "jumps":[
                     {
                        "duration":0.62702536582947,
                        "offset":1393782999.9713,
                        "speed":0.14173210109706
                     }
                  ],
                  "trails":[
                     {
                        "key":"upper_narrow_gauge$black#0",
                        "location":"sugarloaf",
                        "name":"Upper Narrow Gauge",
                        "time_end":1393782729,
                        "time_start":1393782640,
                        "type":"black"
                     },
                     {
                        "key":"lower_narrow_gauge$green#0",
                        "location":"sugarloaf",
                        "name":"Lower Narrow Gauge",
                        "time_end":1393782939,
                        "time_start":1393782869,
                        "type":"green"
                     }
                  ],
                  "lift_line":[
                     {
                        "lat":45.04465,
                        "lon":-70.31224,
                        "alt":731.75048828125
                     },
                     {
                        "lat":45.03491,
                        "lon":-70.31679,
                        "alt":1165.6518554688
                     }
                  ],
                  "lift_name":"Skyline",
                  "lo_res_track_id":"89e7effd25ea3dd0"
                  "hi_res_track_id":"993c67f2f7f03b01"
               },
               "total_distance":2412.25,
               "max_speed":21.5,
               "avg_speed":13.195355191257,
               "calories":31.962116868798,
               "jumps":1,
               "air_time":0.62702536582947,
               "calories_per_lb":0.00058646085997795,
               "slope_time":182,
               "lift_time":525,
               "rest_time":170,
               "vertical_drop":625,
               "max_slope":0.5114716783443,
               "avg_slope":0.24140107846186,
               "sustained_speed":18.5,
               "lunch_time":0
            }
         },
         "date":"2014-03-02",
         "season":2013,
         "session_sheet":"http:\/\/...com\/users\/72000\/72027\/visits\/129593\/session_sheet_129119.jpg?h=9b446842",
         "track_lo_res":"http:\/\/...com\/users\/72000\/72027\/visits\/129593\/visit.trk",
         "track_hi_res":"http:\/\/...com\/users\/72000\/72027\/visits\/129593\/993c67f2f7f03b01.trk",
         "device_type":"trace",
         "total_distance":28817.274209236,
         "max_speed":24,
         "avg_speed":9.1546521597203,
         "calories":1098.2559027617,
         "jumps":9,
         "air_time":4.7254085540771,
         "calories_per_lb":0.020151484454343,
         "max_slope":0.84268901530484,
         "slope_time":3428,
         "lift_time":9635,
         "rest_time":3335.4760000706,
         "vertical_drop":6653.4101745876,
         "avg_slope":0.20432066521036,
         "sustained_speed":19.75,
         "lunch_time":0
      }
   ]
}
```

Success SurfReplay response:
```javascript
{
   "success":true,
   "data":[
      {
         "visit_id":710,
         "single_run_mode":false,
         "update_time":"2015-06-18 13:58:05",
         "resort_title":"Lower Trestles",
         "runs":[
            {
               "run_id":6728,
               "start_time":"2015-06-11 15:12:49",
               "resources":{
                  "jumps":[
                     {
                        "bottom_turn":{
                           "angle":2.0449782177287,
                           "duration":0.91000270843506,
                           "initial_speed":9.8748835109338,
                           "offset":1434035574.4419,
                           "roll_angle":0.77971739233362,
                           "speed_gain":0.99871869878497,
                           "vertical":66.932779820941
                        },
                        "duration":0.38100099563599,
                        "height":0.31645263391284,
                        "offset":1434035575.4309
                     }
                  ],
                  "cutbacks":[
                     {
                        "angle":4.2269022388381,
                        "bottom_turn":{
                           "angle":2.3531268564004,
                           "duration":1.0000030994415,
                           "initial_speed":8.3040393283667,
                           "offset":1434035577.4849,
                           "roll_angle":1.1135685537327,
                           "speed_gain":0.72827139422401,
                           "vertical":50.387893062057
                        },
                        "duration":1.4480042457581,
                        "offset":1434035578.4849,
                        "pitch_angle":0.88292636603308,
                        "power":9.1181047180415,
                        "roll_angle":1.395900988425,
                        "speed":7.0556366238778
                     }
                  ],
                  "lo_res_track_id":"f62821216756647f",
                  "hi_res_track_id":"17b4d701f0581475"
               },
               "total_distance":92.069442184946,
               "max_speed":11.026549777696,
               "avg_speed":6.4487753557003,
               "calories":8.7360104541531,
               "jumps":1,
               "air_time":0.38100099563599,
               "calories_per_lb":0.00034944041816612,
               "ride_time":14.277042865753,
               "paddle_time":147.60544347763,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":145.0574779941,
               "turns_num":1,
               "sharpest_turn":4.2269022388381
            }
         ],
         "date":"2015-06-11",
         "season":2015,
         "session_sheet":"...com\/stats\/get_stats_image?iId=471787",
         "track_lo_res":"...com\/users\/71000\/71202\/surf_sessions\/710\/visit.trk",
         "track_hi_res":"...com\/users\/71000\/71202\/surf_sessions\/710\/17b4d701f0581475.trk",
         "device_type":"trace",
         "total_distance":92.069442184946,
         "max_speed":11.026549777696,
         "avg_speed":6.4487753557003,
         "calories":8.736010454153,
         "jumps":1,
         "air_time":0.38100099563599,
         "calories_per_lb":0.00034944041816612,
         "ride_time":14.277042865753,
         "paddle_time":147.60544347763,
         "wait_time":69.401000499725,
         "waves_missed":0,
         "paddle_distance":145.0574779941,
         "longest_ride":92.069442184946,
         "turns_num":1,
         "sharpest_turn":4.2269022388381
      }
   ]
}
```

#### **GET users/[user_id]/visits/list**
Controller and action style:  **new method**  
Authentication: **API user**  
Authorization: **users**  

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
Controller and action style:  **new method**  
Authentication: **API user**  
Authorization: **users**  

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

Authentication: **API user**
Authorization: **users**

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
Controller and action style:  **new method**
Authentication: **API user**
Authorization: **users**

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

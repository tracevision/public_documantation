
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
         "session_sheet":"http:\/\/dev7.alpinereplay.com\/users\/72000\/72027\/visits\/129593\/session_sheet_129119.jpg?h=9b446842",
         "track_lo_res":"http:\/\/dev7.alpinereplay.com\/users\/72000\/72027\/visits\/129593\/visit.trk",
         "track_hi_res":"http:\/\/dev7.alpinereplay.com\/users\/72000\/72027\/visits\/129593\/993c67f2f7f03b01.trk",
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
   "data":{
      {
         "visit_id":51,
         "single_run_mode":false,
         "update_time":"2014-07-24 08:17:36",
         "resort_title":"Huntington Pier",
         "runs":{
            {
               "run_id":535,
               "start_time":"2013-10-27 17:08:03",
               "resources":{
                  "jumps":[

                  ],
                  "turns":[
                     {
                        "angle":1.8399137376356,
                        "duration":0.80200004577637,
                        "offset":1382904248.451,
                        "pitch_angle":0.33291302989604,
                        "roll_angle":0.3687552612955
                     },
                     {
                        "angle":2.0093690798478,
                        "duration":1.6949999332428,
                        "offset":1382904249.253,
                        "pitch_angle":0.33291302989604,
                        "roll_angle":0.3687552612955
                     }
                  ],
                  "cutbacks":[
                     {
                        "angle":1.8399137376356,
                        "duration":2.4969999790192,
                        "offset":1382904248.451,
                        "pitch_angle":1.3288775025193,
                        "roll_angle":3.1314442313886,
                        "speed":3.5368231661251
                     }
                  ],
                  "air_reverses":[
                     {
                        "duration":0.39891743659973,
                        "height":0.3469145642668,
                        "offset":1411235084.1628
                     }
                  ],
                  "lo_res_track_id":"cc6e05cb41388ab9"
                  "hi_res_track_id":"ce28f9c95ae28ee3"
               },
               "total_distance":44.250139416349,
               "max_speed":7.1978108427489,
               "avg_speed":4.0964765070197,
               "calories":0,
               "jumps":0,
               "air_time":0,
               "calories_per_lb":0,
               "ride_time":10.802000045776,
               "paddle_time":0,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":0
            }
         },
         "date":"2013-10-27",
         "season":2013,
         "session_sheet":"https:\/\/dev7.xsportsw.com-surf.s3.amazonaws.com\/public\/users\/72000\/72024\/surf_sessions\/51\/session_sheet_129089.jpg?h=0e4d87fd",
         "track_lo_res":"http:\/\/dev7.alpinereplay.com\/surf\/users\/72000\/72024\/surf_sessions\/51\/visit.trk",
         "track_hi_res":"http:\/\/dev7.alpinereplay.com\/surf\/users\/72000\/72024\/surf_sessions\/51\/d98b1c6e93353ff8.trk",
         "total_distance":234.28361776096,
         "max_speed":7.1978108427489,
         "avg_speed":3.6395096190365,
         "calories":71.87498335435,
         "jumps":0,
         "air_time":0,
         "calories_per_lb":0.0013188070340248,
         "ride_time":62.178000211716,
         "paddle_time":672.69100022316,
         "wait_time":2466.0700006485,
         "waves_missed":0,
         "paddle_distance":650.63030354383,
         "longest_ride":62.324761436524
      }
   }
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
         "session_sheet":"http:\/\/dev7.alpinereplay.com\/users\/72000\/72027\/visits\/129593\/session_sheet_129119.jpg?h=9b446842",
         "track_lo_res":"http:\/\/dev7.alpinereplay.com\/users\/72000\/72027\/visits\/129593\/visit.trk",
         "track_hi_res":"http:\/\/dev7.alpinereplay.com\/users\/72000\/72027\/visits\/129593\/993c67f2f7f03b01.trk",
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
   "data":{
      {
         "visit_id":51,
         "single_run_mode":false,
         "update_time":"2014-07-24 08:17:36",
         "resort_title":"Huntington Pier",
         "runs":{
            {
               "run_id":535,
               "start_time":"2013-10-27 17:08:03",
               "resources":{
                  "jumps":[

                  ],
                  "turns":[
                     {
                        "angle":1.8399137376356,
                        "duration":0.80200004577637,
                        "offset":1382904248.451,
                        "pitch_angle":0.33291302989604,
                        "roll_angle":0.3687552612955
                     },
                     {
                        "angle":2.0093690798478,
                        "duration":1.6949999332428,
                        "offset":1382904249.253,
                        "pitch_angle":0.33291302989604,
                        "roll_angle":0.3687552612955
                     }
                  ],
                  "cutbacks":[
                     {
                        "angle":1.8399137376356,
                        "duration":2.4969999790192,
                        "offset":1382904248.451,
                        "pitch_angle":1.3288775025193,
                        "roll_angle":3.1314442313886,
                        "speed":3.5368231661251
                     }
                  ],
                  "air_reverses":[
                     {
                        "duration":0.39891743659973,
                        "height":0.3469145642668,
                        "offset":1411235084.1628
                     }
                  ],
                  "lo_res_track_id":"cc6e05cb41388ab9"
                  "hi_res_track_id":"ce28f9c95ae28ee3"
               },
               "total_distance":44.250139416349,
               "max_speed":7.1978108427489,
               "avg_speed":4.0964765070197,
               "calories":0,
               "jumps":0,
               "air_time":0,
               "calories_per_lb":0,
               "ride_time":10.802000045776,
               "paddle_time":0,
               "wait_time":0,
               "waves_missed":0,
               "paddle_distance":0
            }
         },
         "date":"2013-10-27",
         "season":2013,
         "session_sheet":"https:\/\/dev7.xsportsw.com-surf.s3.amazonaws.com\/public\/users\/72000\/72024\/surf_sessions\/51\/session_sheet_129089.jpg?h=0e4d87fd",
         "track_lo_res":"http:\/\/dev7.alpinereplay.com\/surf\/users\/72000\/72024\/surf_sessions\/51\/visit.trk",
         "track_hi_res":"http:\/\/dev7.alpinereplay.com\/surf\/users\/72000\/72024\/surf_sessions\/51\/d98b1c6e93353ff8.trk",
         "total_distance":234.28361776096,
         "max_speed":7.1978108427489,
         "avg_speed":3.6395096190365,
         "calories":71.87498335435,
         "jumps":0,
         "air_time":0,
         "calories_per_lb":0.0013188070340248,
         "ride_time":62.178000211716,
         "paddle_time":672.69100022316,
         "wait_time":2466.0700006485,
         "waves_missed":0,
         "paddle_distance":650.63030354383,
         "longest_ride":62.324761436524
      }
   }
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
         "session_sheet":"https:\/\/dev7.xsportsw.com.s3.amazonaws.com\/public\/users\/73000\/73799\/visits\/390930\/session_sheet.jpg?h=82fc3a31",
         "date":"2013-03-15",
         "resort_title":"Unknown resort"
      },
      {
         "visit_id":469706,
         "update_time":"2014-10-06 14:20:48",
         "session_sheet":"http:\/\/tracesnow.dev7.alpinereplay.com\/stats\/get_stats_image?iId=469396",
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
         "session_sheet":"https:\/\/dev7.xsportsw.com.s3.amazonaws.com\/public\/users\/73000\/73799\/visits\/390930\/session_sheet.jpg?h=82fc3a31",
         "date":"2013-03-15",
         "resort_title":"Unknown resort"
      },
      {
         "visit_id":469706,
         "update_time":"2014-10-06 14:20:48",
         "session_sheet":"http:\/\/tracesnow.dev7.alpinereplay.com\/stats\/get_stats_image?iId=469396",
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

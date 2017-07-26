# Historical wireless usage statistics

```
GET /wireless/usage.{format}
```

## Description

> This method returns historical wireless usage statistics, by building.

## Summary

<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Value</b></td>
    <td><b><b>Name</b></b></td>
    <td><b>Value</b></td>
  </tr>
  <tr>
    <td><b>Request Protocol</b></td>
    <td>GET</td>
    <td><b>Requires API Key</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Method ID</b></td>
    <td>10000</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>wireless</td>
    <td><b>Service ID</b></td>
    <td>1000</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Information Systems & Technology</td>
    <td><b>Data Type</b></td>
    <td>Database</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every 15 minutes</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Historical data is only avaialble for the past 2 months
- Any value can be `null`


### Sources

- https://uwaterloo.ca/information-systems-technology/statistics/wifi-charts


## Parameters

```
GET /wireless/usage.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>key</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Valid API key</td>
  </tr>
  <tr>
    <td><b>callback</b></td>
    <td>filter</td>
    <td><i>no</i></td>
    <td>JSONP callback format</td>
  </tr>
  <tr>
    <td><b>from</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Timestamp of starting point (in ISO 8601 format)</td>
  </tr>
</table>

**Output Formats**

- json
- xml


## Examples

```
GET /wireless/usage.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/historical/usage.json?from=2017-06-28T160000-0040&to=2017-06-28T161500-0400**
- **https://api.uwaterloo.ca/v2/wireless/historical/usage.xml**
- **https://api.uwaterloo.ca/v2/wireless/historical/usage.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>building_code</b></td>
    <td>string</td>
    <td>Building code</td>
  </tr>
  <tr>
    <td><b>clients</b></td>
    <td>string</td>
    <td>Number of wireless clients</td>
  </tr>
  <tr>
    <td><b>rates</b></td>
    <td>object</td>
    <td>Current usage rates<br><table>
  <tr>
    <td><b>download</b></td>
    <td>integer</td>
    <td>Curent download rate, in bps</td>
  </tr>
  <tr>
    <td><b>upload</b></td>
    <td>integer</td>
    <td>Current upload rate, in bps</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>last_updated</b></td>
    <td>string</td>
    <td>Timestamp of collection</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
    "meta": {
        "requests": 1016365,
        "timestamp": 1501095136,
        "status": 200,
        "message": "Request successful",
        "method_id": 10005,
        "method": []
    },
    "data": [
        {
            "building_code": "ACW",
            "clients": 14,
            "rates": {
                "download": 665464,
                "upload": 123708
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 6,
            "rates": {
                "download": 264645,
                "upload": 40578
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 203,
            "rates": {
                "download": 32514842,
                "upload": 4290696
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 116,
            "rates": {
                "download": 24695331,
                "upload": 2040341
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 81,
            "rates": {
                "download": 14522119,
                "upload": 850370
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 143,
            "rates": {
                "download": 13127682,
                "upload": 1115158
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 106,
            "rates": {
                "download": 5762882,
                "upload": 353590
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 71,
            "rates": {
                "download": 4042428,
                "upload": 416503
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 174,
            "rates": {
                "download": 51674382,
                "upload": 3605184
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 116,
            "rates": {
                "download": 8430086,
                "upload": 3876791
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 16,
            "rates": {
                "download": 1052648,
                "upload": 115279
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 302,
            "rates": {
                "download": 58129181,
                "upload": 5483692
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 145,
            "rates": {
                "download": 36121947,
                "upload": 2636022
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 31,
            "rates": {
                "download": 3631084,
                "upload": 358664
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 122,
            "rates": {
                "download": 22879631,
                "upload": 13674990
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 103,
            "rates": {
                "download": 8502659,
                "upload": 668825
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 17,
            "rates": {
                "download": 2338156,
                "upload": 136599
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 9,
            "rates": {
                "download": 183136,
                "upload": 237798
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 13,
            "rates": {
                "download": 648638,
                "upload": 64668
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 5,
            "rates": {
                "download": 74887,
                "upload": 14876
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 2,
            "rates": {
                "download": 835230,
                "upload": 50268
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1387,
                "upload": 482
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 13,
            "rates": {
                "download": 3512695,
                "upload": 2638554
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 10,
            "rates": {
                "download": 4073335,
                "upload": 153797
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 1734326,
                "upload": 50581
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 17,
            "rates": {
                "download": 10595400,
                "upload": 484890
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 4,
            "rates": {
                "download": 68408,
                "upload": 3074
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 59227,
                "upload": 22907
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 1,
            "rates": {
                "download": 411,
                "upload": 6
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 12,
            "rates": {
                "download": 601793,
                "upload": 313531
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 1,
            "rates": {
                "download": 104,
                "upload": 80
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 10,
            "rates": {
                "download": 2053397,
                "upload": 160450
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 26,
            "rates": {
                "download": 933311,
                "upload": 77161
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 317,
            "rates": {
                "download": 39279274,
                "upload": 5237179
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 2650,
                "upload": 992
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1222,
            "rates": {
                "download": 180973586,
                "upload": 25910365
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 40,
            "rates": {
                "download": 3276176,
                "upload": 291489
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 372,
            "rates": {
                "download": 28113432,
                "upload": 3825024
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 415,
            "rates": {
                "download": 93414525,
                "upload": 39753042
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 207,
            "rates": {
                "download": 19839493,
                "upload": 19909522
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 690,
            "rates": {
                "download": 92840390,
                "upload": 15681309
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 355,
            "rates": {
                "download": 60194340,
                "upload": 5424380
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 13,
            "rates": {
                "download": 1801067,
                "upload": 105252
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 44,
            "rates": {
                "download": 2389930,
                "upload": 123833
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 387,
            "rates": {
                "download": 60394489,
                "upload": 5233440
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 45,
            "rates": {
                "download": 4393488,
                "upload": 1609839
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 162,
            "rates": {
                "download": 35099562,
                "upload": 2234466
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 175,
            "rates": {
                "download": 42416655,
                "upload": 5424324
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 78,
            "rates": {
                "download": 14905195,
                "upload": 1485397
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 183,
            "rates": {
                "download": 25031535,
                "upload": 4943207
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 11,
            "rates": {
                "download": 102833,
                "upload": 13507
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 5,
            "rates": {
                "download": 109944,
                "upload": 59051
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 21,
            "rates": {
                "download": 2988215,
                "upload": 159745
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 52,
            "rates": {
                "download": 639890,
                "upload": 107985
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 871,
            "rates": {
                "download": 101237498,
                "upload": 14756090
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 37,
            "rates": {
                "download": 1240464,
                "upload": 499795
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 54,
            "rates": {
                "download": 3863205,
                "upload": 426548
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 598,
            "rates": {
                "download": 131509249,
                "upload": 14821691
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 244,
            "rates": {
                "download": 33031074,
                "upload": 10490589
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1285,
            "rates": {
                "download": 154000328,
                "upload": 14345870
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 27,
            "rates": {
                "download": 15755303,
                "upload": 2374899
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 69,
            "rates": {
                "download": 10203409,
                "upload": 666542
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 82,
            "rates": {
                "download": 14186718,
                "upload": 20920638
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 182,
            "rates": {
                "download": 23628157,
                "upload": 3568472
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 191,
            "rates": {
                "download": 19460351,
                "upload": 6984838
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 33,
            "rates": {
                "download": 538405,
                "upload": 92766
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 26,
            "rates": {
                "download": 1138009,
                "upload": 377697
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 239,
            "rates": {
                "download": 31046832,
                "upload": 4905985
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 327,
            "rates": {
                "download": 63459932,
                "upload": 5645428
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 223,
            "rates": {
                "download": 20699706,
                "upload": 3571431
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 741,
            "rates": {
                "download": 76595212,
                "upload": 7808364
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 41,
            "rates": {
                "download": 588630,
                "upload": 205280
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 52,
            "rates": {
                "download": 20681033,
                "upload": 1526845
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 528,
            "rates": {
                "download": 79325482,
                "upload": 17169292
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 344,
            "rates": {
                "download": 48178659,
                "upload": 3552917
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 3,
            "rates": {
                "download": 1181,
                "upload": 198
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 4,
            "rates": {
                "download": 93480,
                "upload": 10973
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 21,
            "rates": {
                "download": 869757,
                "upload": 45964
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 4,
            "rates": {
                "download": 5058625,
                "upload": 124777
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 6,
            "rates": {
                "download": 5234317,
                "upload": 165679
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 13,
            "rates": {
                "download": 4126763,
                "upload": 147086
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 12,
            "rates": {
                "download": 1426417,
                "upload": 112134
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 256,
            "rates": {
                "download": 27301906,
                "upload": 2796487
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 683,
            "rates": {
                "download": 77444844,
                "upload": 12441451
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 597,
            "rates": {
                "download": 81761939,
                "upload": 8681365
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 185,
            "rates": {
                "download": 16011217,
                "upload": 2172315
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 76,
            "rates": {
                "download": 4362973,
                "upload": 494312
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 121,
            "rates": {
                "download": 21459124,
                "upload": 1121430
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 8,
            "rates": {
                "download": 4436,
                "upload": 2626
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 65,
            "rates": {
                "download": 3577779,
                "upload": 279577
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 38,
            "rates": {
                "download": 1088087,
                "upload": 150988
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 97,
            "rates": {
                "download": 8039672,
                "upload": 1112750
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 1,
            "rates": {
                "download": 661,
                "upload": 104
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 1,
            "rates": {
                "download": 41334,
                "upload": 25999
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 1,
            "rates": {
                "download": 3031,
                "upload": 1706
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 24,
            "rates": {
                "download": 1811297,
                "upload": 157279
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 20,
            "rates": {
                "download": 3252573,
                "upload": 163169
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 15,
            "rates": {
                "download": 6839455,
                "upload": 258031
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 30,
            "rates": {
                "download": 4478175,
                "upload": 218832
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 18,
            "rates": {
                "download": 2121571,
                "upload": 189996
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 24,
            "rates": {
                "download": 7978966,
                "upload": 473617
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 1,
            "rates": {
                "download": 428,
                "upload": 280
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 318,
                "upload": 143
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 91,
            "rates": {
                "download": 15612470,
                "upload": 1766320
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 10,
            "rates": {
                "download": 17939,
                "upload": 14987
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 147,
            "rates": {
                "download": 27058676,
                "upload": 2477506
            },
            "last_updated": "2017-06-28T12:45:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 13,
            "rates": {
                "download": 1151130,
                "upload": 110857
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 12,
            "rates": {
                "download": 1593008,
                "upload": 212927
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 207,
            "rates": {
                "download": 32286485,
                "upload": 3022753
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 141,
            "rates": {
                "download": 13298333,
                "upload": 1746553
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 93,
            "rates": {
                "download": 6084469,
                "upload": 403958
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 161,
            "rates": {
                "download": 13797915,
                "upload": 1075450
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 119,
            "rates": {
                "download": 9328459,
                "upload": 421808
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 68,
            "rates": {
                "download": 1114731,
                "upload": 356948
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 172,
            "rates": {
                "download": 11560477,
                "upload": 1336786
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 118,
            "rates": {
                "download": 6072875,
                "upload": 1439748
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 17,
            "rates": {
                "download": 723618,
                "upload": 94011
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 301,
            "rates": {
                "download": 30258809,
                "upload": 2653287
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 147,
            "rates": {
                "download": 26458240,
                "upload": 1760855
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 33,
            "rates": {
                "download": 3478251,
                "upload": 199639
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 108,
            "rates": {
                "download": 36917392,
                "upload": 28880708
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 93,
            "rates": {
                "download": 6291569,
                "upload": 443957
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 18,
            "rates": {
                "download": 2741056,
                "upload": 228372
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 11,
            "rates": {
                "download": 351968,
                "upload": 325346
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 14,
            "rates": {
                "download": 2830628,
                "upload": 121852
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 5,
            "rates": {
                "download": 82796,
                "upload": 21445
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 608997,
                "upload": 33780
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 911,
                "upload": 208
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 14,
            "rates": {
                "download": 5705293,
                "upload": 2698927
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 9,
            "rates": {
                "download": 5840099,
                "upload": 478010
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 349721,
                "upload": 11936
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 17,
            "rates": {
                "download": 11293718,
                "upload": 423896
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 5,
            "rates": {
                "download": 161298,
                "upload": 44130
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 52545,
                "upload": 23538
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 1,
            "rates": {
                "download": 421,
                "upload": 6
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 13,
            "rates": {
                "download": 2442839,
                "upload": 728733
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 9,
            "rates": {
                "download": 5884737,
                "upload": 279606
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 24,
            "rates": {
                "download": 3212976,
                "upload": 186939
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 295,
            "rates": {
                "download": 46856972,
                "upload": 3962643
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 1,
            "rates": {
                "download": 464,
                "upload": 38
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1262,
            "rates": {
                "download": 205628882,
                "upload": 25746938
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 42,
            "rates": {
                "download": 1664982,
                "upload": 214403
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 348,
            "rates": {
                "download": 27167395,
                "upload": 5167397
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 446,
            "rates": {
                "download": 47698171,
                "upload": 4710112
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 232,
            "rates": {
                "download": 20026130,
                "upload": 2396669
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 713,
            "rates": {
                "download": 73523217,
                "upload": 28183199
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 351,
            "rates": {
                "download": 65642459,
                "upload": 4828980
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 9,
            "rates": {
                "download": 1937558,
                "upload": 59553
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 50,
            "rates": {
                "download": 2039181,
                "upload": 151398
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 406,
            "rates": {
                "download": 65649075,
                "upload": 13188438
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 52,
            "rates": {
                "download": 7644249,
                "upload": 1119777
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 195,
            "rates": {
                "download": 33055973,
                "upload": 2348145
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 200,
            "rates": {
                "download": 28034168,
                "upload": 10695729
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 78,
            "rates": {
                "download": 8646466,
                "upload": 959436
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 211,
            "rates": {
                "download": 20825085,
                "upload": 8340293
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 12,
            "rates": {
                "download": 1303446,
                "upload": 83233
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 65891,
                "upload": 37991
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 27,
            "rates": {
                "download": 1601351,
                "upload": 150899
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 67,
            "rates": {
                "download": 7912097,
                "upload": 314308
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 728,
            "rates": {
                "download": 88578990,
                "upload": 10427074
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 43,
            "rates": {
                "download": 1713684,
                "upload": 189012
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 61,
            "rates": {
                "download": 3228409,
                "upload": 380658
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 635,
            "rates": {
                "download": 143491102,
                "upload": 15578400
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 271,
            "rates": {
                "download": 48676485,
                "upload": 4757729
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1358,
            "rates": {
                "download": 170829663,
                "upload": 20053554
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 28,
            "rates": {
                "download": 5462190,
                "upload": 2580413
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 66,
            "rates": {
                "download": 10250115,
                "upload": 843435
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 103,
            "rates": {
                "download": 17061363,
                "upload": 1725298
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 211,
            "rates": {
                "download": 16559824,
                "upload": 3446076
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 190,
            "rates": {
                "download": 20270228,
                "upload": 2660663
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 48,
            "rates": {
                "download": 216216,
                "upload": 76538
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 32,
            "rates": {
                "download": 557043,
                "upload": 70785
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 239,
            "rates": {
                "download": 31796856,
                "upload": 5445323
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 426,
            "rates": {
                "download": 35079176,
                "upload": 3881566
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 245,
            "rates": {
                "download": 48987413,
                "upload": 7362735
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 731,
            "rates": {
                "download": 101002113,
                "upload": 7829844
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 36,
            "rates": {
                "download": 2261314,
                "upload": 707066
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 51,
            "rates": {
                "download": 15977788,
                "upload": 709598
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 572,
            "rates": {
                "download": 81105647,
                "upload": 23014623
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 307,
            "rates": {
                "download": 36566264,
                "upload": 4708978
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 2,
            "rates": {
                "download": 2974,
                "upload": 1120
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 5,
            "rates": {
                "download": 263034,
                "upload": 17280
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 32,
            "rates": {
                "download": 2315440,
                "upload": 155177
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 3,
            "rates": {
                "download": 6680089,
                "upload": 158721
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 5,
            "rates": {
                "download": 2735217,
                "upload": 85341
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 12,
            "rates": {
                "download": 3409475,
                "upload": 128741
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 14,
            "rates": {
                "download": 1954005,
                "upload": 770141
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 261,
            "rates": {
                "download": 17317840,
                "upload": 2533231
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 650,
            "rates": {
                "download": 119102924,
                "upload": 17277897
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 403,
            "rates": {
                "download": 77279215,
                "upload": 30697726
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 209,
            "rates": {
                "download": 25207997,
                "upload": 2051831
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 73,
            "rates": {
                "download": 7998893,
                "upload": 685407
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 142,
            "rates": {
                "download": 16417222,
                "upload": 1230955
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 7,
            "rates": {
                "download": 415760,
                "upload": 30479
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 70,
            "rates": {
                "download": 4832462,
                "upload": 326237
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 37,
            "rates": {
                "download": 993328,
                "upload": 126402
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 7,
            "rates": {
                "download": 2429057,
                "upload": 183791
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 65,
            "rates": {
                "download": 10511649,
                "upload": 969815
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 1,
            "rates": {
                "download": 430,
                "upload": 68
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 2,
            "rates": {
                "download": 2379,
                "upload": 2546
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 4,
            "rates": {
                "download": 573,
                "upload": 447
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 29,
            "rates": {
                "download": 3719749,
                "upload": 420930
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 24,
            "rates": {
                "download": 2568788,
                "upload": 205116
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 20,
            "rates": {
                "download": 6380824,
                "upload": 353476
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 31,
            "rates": {
                "download": 26294104,
                "upload": 834089
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 18,
            "rates": {
                "download": 3884389,
                "upload": 199597
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 27,
            "rates": {
                "download": 18509986,
                "upload": 790935
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 2,
            "rates": {
                "download": 100225,
                "upload": 21859
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 1,
            "rates": {
                "download": 2194,
                "upload": 1591
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 3,
            "rates": {
                "download": 286770,
                "upload": 81594
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 97,
            "rates": {
                "download": 22412298,
                "upload": 3727057
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 9,
            "rates": {
                "download": 70642,
                "upload": 14113
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 162,
            "rates": {
                "download": 47322926,
                "upload": 2407244
            },
            "last_updated": "2017-06-28T13:00:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 16,
            "rates": {
                "download": 4614046,
                "upload": 284548
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 5,
            "rates": {
                "download": 4351,
                "upload": 4096
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 202,
            "rates": {
                "download": 23235946,
                "upload": 7571440
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 163,
            "rates": {
                "download": 25655948,
                "upload": 1947815
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 99,
            "rates": {
                "download": 7574588,
                "upload": 815733
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 206,
            "rates": {
                "download": 22016646,
                "upload": 1931660
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 131,
            "rates": {
                "download": 7066186,
                "upload": 849977
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 71,
            "rates": {
                "download": 2196228,
                "upload": 757320
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 186,
            "rates": {
                "download": 49043245,
                "upload": 2512098
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 121,
            "rates": {
                "download": 6867267,
                "upload": 1202393
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 17,
            "rates": {
                "download": 2050635,
                "upload": 117152
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 322,
            "rates": {
                "download": 44445102,
                "upload": 4351275
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 144,
            "rates": {
                "download": 42610099,
                "upload": 3186195
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 34,
            "rates": {
                "download": 1451280,
                "upload": 121564
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 111,
            "rates": {
                "download": 24552823,
                "upload": 27445832
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 89,
            "rates": {
                "download": 8826338,
                "upload": 485266
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 18,
            "rates": {
                "download": 5645234,
                "upload": 305947
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 8,
            "rates": {
                "download": 314714,
                "upload": 102186
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 13,
            "rates": {
                "download": 567861,
                "upload": 18042
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 5,
            "rates": {
                "download": 82578,
                "upload": 18230
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 181665,
                "upload": 7194
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1708,
                "upload": 684
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 13,
            "rates": {
                "download": 5872995,
                "upload": 2943141
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 11,
            "rates": {
                "download": 5253989,
                "upload": 197115
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 99218,
                "upload": 880369
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 15,
            "rates": {
                "download": 8388272,
                "upload": 303719
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 3,
            "rates": {
                "download": 466926,
                "upload": 56215
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 84971,
                "upload": 14725
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 1,
            "rates": {
                "download": 406,
                "upload": 6
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 14,
            "rates": {
                "download": 1397929,
                "upload": 694161
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 7,
            "rates": {
                "download": 22647,
                "upload": 12275
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 24,
            "rates": {
                "download": 2467265,
                "upload": 158905
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 303,
            "rates": {
                "download": 35817049,
                "upload": 11790257
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 3,
            "rates": {
                "download": 425,
                "upload": 16
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1344,
            "rates": {
                "download": 269663281,
                "upload": 30904687
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 50,
            "rates": {
                "download": 2076841,
                "upload": 281164
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 293,
            "rates": {
                "download": 22809138,
                "upload": 2498112
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 494,
            "rates": {
                "download": 96898120,
                "upload": 6837516
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 238,
            "rates": {
                "download": 23565798,
                "upload": 2588927
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 721,
            "rates": {
                "download": 62679020,
                "upload": 22907237
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 353,
            "rates": {
                "download": 47506615,
                "upload": 14220170
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 13,
            "rates": {
                "download": 892062,
                "upload": 42172
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 51,
            "rates": {
                "download": 2426798,
                "upload": 201311
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 438,
            "rates": {
                "download": 56673224,
                "upload": 4303094
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 48,
            "rates": {
                "download": 2604585,
                "upload": 430203
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 200,
            "rates": {
                "download": 46118258,
                "upload": 3516131
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 183,
            "rates": {
                "download": 27669499,
                "upload": 14401228
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 86,
            "rates": {
                "download": 10793441,
                "upload": 927340
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 222,
            "rates": {
                "download": 27305699,
                "upload": 9931704
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 14,
            "rates": {
                "download": 179606,
                "upload": 17625
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 4,
            "rates": {
                "download": 501834,
                "upload": 57482
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 24,
            "rates": {
                "download": 622431,
                "upload": 70231
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 58,
            "rates": {
                "download": 3205272,
                "upload": 188787
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 779,
            "rates": {
                "download": 152846960,
                "upload": 36838787
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 47,
            "rates": {
                "download": 3522775,
                "upload": 308757
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 67,
            "rates": {
                "download": 2020507,
                "upload": 348420
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 620,
            "rates": {
                "download": 165250166,
                "upload": 17154943
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 282,
            "rates": {
                "download": 35642861,
                "upload": 3813232
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1394,
            "rates": {
                "download": 155239879,
                "upload": 19658992
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 29,
            "rates": {
                "download": 1761846,
                "upload": 1668658
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 64,
            "rates": {
                "download": 10070183,
                "upload": 706564
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 82,
            "rates": {
                "download": 17011938,
                "upload": 1445522
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 217,
            "rates": {
                "download": 26410580,
                "upload": 4654753
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 199,
            "rates": {
                "download": 26961566,
                "upload": 7978853
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 18,
            "rates": {
                "download": 109039,
                "upload": 28274
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 50,
            "rates": {
                "download": 622355,
                "upload": 84532
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 240,
            "rates": {
                "download": 24252007,
                "upload": 4808100
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 376,
            "rates": {
                "download": 19373855,
                "upload": 2120910
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 254,
            "rates": {
                "download": 45183507,
                "upload": 7591525
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 755,
            "rates": {
                "download": 109555489,
                "upload": 10455325
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 38,
            "rates": {
                "download": 5049548,
                "upload": 671256
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 53,
            "rates": {
                "download": 5994149,
                "upload": 868781
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 589,
            "rates": {
                "download": 103368005,
                "upload": 26296597
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 326,
            "rates": {
                "download": 25506733,
                "upload": 3418619
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 2,
            "rates": {
                "download": 853,
                "upload": 38
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 5,
            "rates": {
                "download": 4357,
                "upload": 2628
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 42,
            "rates": {
                "download": 16538605,
                "upload": 820103
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 6,
            "rates": {
                "download": 1245422,
                "upload": 49216
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 4,
            "rates": {
                "download": 2847998,
                "upload": 737917
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 9,
            "rates": {
                "download": 3771763,
                "upload": 149636
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 11,
            "rates": {
                "download": 819521,
                "upload": 54759
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 246,
            "rates": {
                "download": 15088972,
                "upload": 2066557
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 644,
            "rates": {
                "download": 105285666,
                "upload": 9596831
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 392,
            "rates": {
                "download": 49057893,
                "upload": 25532847
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 179,
            "rates": {
                "download": 25395275,
                "upload": 2301945
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 74,
            "rates": {
                "download": 9945720,
                "upload": 1029100
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 126,
            "rates": {
                "download": 13579394,
                "upload": 1195289
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 7,
            "rates": {
                "download": 7301,
                "upload": 5294
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 74,
            "rates": {
                "download": 6464186,
                "upload": 728854
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 34,
            "rates": {
                "download": 662971,
                "upload": 55145
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 9,
            "rates": {
                "download": 1158335,
                "upload": 98747
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 57,
            "rates": {
                "download": 6352994,
                "upload": 357577
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 2,
            "rates": {
                "download": 5077,
                "upload": 2272
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 2,
            "rates": {
                "download": 114,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 25,
            "rates": {
                "download": 11549629,
                "upload": 764727
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 22,
            "rates": {
                "download": 2988828,
                "upload": 129618
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 19,
            "rates": {
                "download": 8348307,
                "upload": 396936
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 33,
            "rates": {
                "download": 4844602,
                "upload": 627162
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 16,
            "rates": {
                "download": 2993706,
                "upload": 181807
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 22,
            "rates": {
                "download": 8533076,
                "upload": 414588
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 3,
            "rates": {
                "download": 963,
                "upload": 553
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 547,
                "upload": 267
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 98,
            "rates": {
                "download": 16908786,
                "upload": 3881671
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 7,
            "rates": {
                "download": 320395,
                "upload": 27765
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 3,
            "rates": {
                "download": 113,
                "upload": 29
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 158,
            "rates": {
                "download": 44038641,
                "upload": 3178795
            },
            "last_updated": "2017-06-28T13:15:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 16,
            "rates": {
                "download": 781641,
                "upload": 73253
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 2,
            "rates": {
                "download": 406740,
                "upload": 19680
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 208,
            "rates": {
                "download": 46867452,
                "upload": 8261538
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 221,
            "rates": {
                "download": 29136791,
                "upload": 3446876
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 103,
            "rates": {
                "download": 8278193,
                "upload": 783828
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 220,
            "rates": {
                "download": 19897372,
                "upload": 2071207
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 153,
            "rates": {
                "download": 20041733,
                "upload": 1181469
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 76,
            "rates": {
                "download": 3178133,
                "upload": 477864
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 185,
            "rates": {
                "download": 48002635,
                "upload": 3682270
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 124,
            "rates": {
                "download": 7525426,
                "upload": 1195058
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 14,
            "rates": {
                "download": 305317,
                "upload": 45659
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 314,
            "rates": {
                "download": 39403175,
                "upload": 15766007
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 226,
            "rates": {
                "download": 33082608,
                "upload": 3021235
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 32,
            "rates": {
                "download": 1238327,
                "upload": 178325
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 111,
            "rates": {
                "download": 9432092,
                "upload": 970100
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 102,
            "rates": {
                "download": 7024332,
                "upload": 559608
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 18,
            "rates": {
                "download": 7347501,
                "upload": 299688
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 8,
            "rates": {
                "download": 193026,
                "upload": 3319
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 12,
            "rates": {
                "download": 2328899,
                "upload": 120870
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 66212,
                "upload": 17138
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 12209,
                "upload": 2700
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 981,
                "upload": 202
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 15,
            "rates": {
                "download": 2197655,
                "upload": 2199162
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 9,
            "rates": {
                "download": 6790397,
                "upload": 303176
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 2338225,
                "upload": 47951
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 15,
            "rates": {
                "download": 5805891,
                "upload": 197270
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 3,
            "rates": {
                "download": 584625,
                "upload": 94699
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 272177,
                "upload": 49635
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 1,
            "rates": {
                "download": 438,
                "upload": 294
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 14,
            "rates": {
                "download": 769518,
                "upload": 1557066
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 6,
            "rates": {
                "download": 3988,
                "upload": 1013
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 29,
            "rates": {
                "download": 1568937,
                "upload": 154653
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 356,
            "rates": {
                "download": 34675489,
                "upload": 3251567
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 1038,
                "upload": 663
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1494,
            "rates": {
                "download": 249505448,
                "upload": 34090194
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 45,
            "rates": {
                "download": 9320022,
                "upload": 423727
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 357,
            "rates": {
                "download": 40104947,
                "upload": 4029341
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 579,
            "rates": {
                "download": 64382901,
                "upload": 6936910
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 306,
            "rates": {
                "download": 12671039,
                "upload": 3354755
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 663,
            "rates": {
                "download": 69702094,
                "upload": 20402390
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 339,
            "rates": {
                "download": 58789535,
                "upload": 4835244
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 21,
            "rates": {
                "download": 234355,
                "upload": 37183
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 48,
            "rates": {
                "download": 2188025,
                "upload": 117983
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 447,
            "rates": {
                "download": 45265747,
                "upload": 6681782
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 49,
            "rates": {
                "download": 3475460,
                "upload": 1058155
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 225,
            "rates": {
                "download": 29342596,
                "upload": 2247236
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 179,
            "rates": {
                "download": 26201724,
                "upload": 2615742
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 88,
            "rates": {
                "download": 16583635,
                "upload": 842684
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 240,
            "rates": {
                "download": 27845718,
                "upload": 10536565
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 11,
            "rates": {
                "download": 187415,
                "upload": 16497
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 2,
            "rates": {
                "download": 664648,
                "upload": 104853
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 23,
            "rates": {
                "download": 798583,
                "upload": 78229
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 59,
            "rates": {
                "download": 1838152,
                "upload": 199416
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 812,
            "rates": {
                "download": 120704295,
                "upload": 28036563
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 58,
            "rates": {
                "download": 3456255,
                "upload": 341915
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 68,
            "rates": {
                "download": 1694098,
                "upload": 366240
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 618,
            "rates": {
                "download": 106095795,
                "upload": 12737446
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 308,
            "rates": {
                "download": 49007818,
                "upload": 4499547
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1475,
            "rates": {
                "download": 160138608,
                "upload": 22597433
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 25,
            "rates": {
                "download": 1048133,
                "upload": 167661
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 58,
            "rates": {
                "download": 14513397,
                "upload": 648885
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 75,
            "rates": {
                "download": 8021709,
                "upload": 1079035
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 221,
            "rates": {
                "download": 18762714,
                "upload": 2519552
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 196,
            "rates": {
                "download": 31096998,
                "upload": 5155320
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 24,
            "rates": {
                "download": 205657,
                "upload": 34877
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 34,
            "rates": {
                "download": 2353451,
                "upload": 223641
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 256,
            "rates": {
                "download": 15497166,
                "upload": 2104258
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 362,
            "rates": {
                "download": 15813028,
                "upload": 1735391
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 260,
            "rates": {
                "download": 60436598,
                "upload": 23302002
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 697,
            "rates": {
                "download": 103343794,
                "upload": 14965539
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 39,
            "rates": {
                "download": 2716407,
                "upload": 1242995
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 52,
            "rates": {
                "download": 24360223,
                "upload": 1252369
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 624,
            "rates": {
                "download": 55635409,
                "upload": 6869265
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 325,
            "rates": {
                "download": 31128699,
                "upload": 4836525
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 2,
            "rates": {
                "download": 599,
                "upload": 38
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 5,
            "rates": {
                "download": 3132,
                "upload": 2536
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 45,
            "rates": {
                "download": 13301959,
                "upload": 828485
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 10,
            "rates": {
                "download": 107232,
                "upload": 13205
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 7,
            "rates": {
                "download": 5888858,
                "upload": 2074452
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 15,
            "rates": {
                "download": 3425434,
                "upload": 690326
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 12,
            "rates": {
                "download": 461969,
                "upload": 44125
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 197,
            "rates": {
                "download": 8282429,
                "upload": 1132005
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 589,
            "rates": {
                "download": 131150060,
                "upload": 11342430
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 297,
            "rates": {
                "download": 34825740,
                "upload": 13926219
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 178,
            "rates": {
                "download": 39396027,
                "upload": 2696513
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 66,
            "rates": {
                "download": 6104519,
                "upload": 465289
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 123,
            "rates": {
                "download": 13002273,
                "upload": 906576
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 9,
            "rates": {
                "download": 2830157,
                "upload": 109981
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 74,
            "rates": {
                "download": 12784576,
                "upload": 822953
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 30,
            "rates": {
                "download": 1739377,
                "upload": 108382
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 10,
            "rates": {
                "download": 187403,
                "upload": 41938
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 64,
            "rates": {
                "download": 2483131,
                "upload": 206202
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 2,
            "rates": {
                "download": 8658,
                "upload": 4528
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 5,
            "rates": {
                "download": 5112,
                "upload": 3704
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 2,
            "rates": {
                "download": 1086046,
                "upload": 40590
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 2,
            "rates": {
                "download": 34921,
                "upload": 2418
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 22,
            "rates": {
                "download": 7031468,
                "upload": 623693
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 20,
            "rates": {
                "download": 5978395,
                "upload": 217211
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 16,
            "rates": {
                "download": 6183756,
                "upload": 252750
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 29,
            "rates": {
                "download": 3152045,
                "upload": 365359
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 19,
            "rates": {
                "download": 6256587,
                "upload": 379535
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 27,
            "rates": {
                "download": 9979526,
                "upload": 553280
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 5,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 1,
            "rates": {
                "download": 21883,
                "upload": 1268
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 1,
            "rates": {
                "download": 404,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 367,
                "upload": 119
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 98,
            "rates": {
                "download": 19475857,
                "upload": 3870344
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 5,
            "rates": {
                "download": 7758,
                "upload": 4413
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 12,
            "rates": {
                "download": 12136,
                "upload": 5619
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 136,
            "rates": {
                "download": 39941376,
                "upload": 3086838
            },
            "last_updated": "2017-06-28T13:30:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 19,
            "rates": {
                "download": 1518166,
                "upload": 198805
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 5,
            "rates": {
                "download": 1361,
                "upload": 1604
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 206,
            "rates": {
                "download": 29016199,
                "upload": 3368336
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 221,
            "rates": {
                "download": 39567756,
                "upload": 4076848
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 98,
            "rates": {
                "download": 6785636,
                "upload": 688697
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 228,
            "rates": {
                "download": 45363435,
                "upload": 7547107
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 139,
            "rates": {
                "download": 14425800,
                "upload": 893224
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 76,
            "rates": {
                "download": 3378911,
                "upload": 698302
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 173,
            "rates": {
                "download": 10675553,
                "upload": 1252858
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 120,
            "rates": {
                "download": 6495198,
                "upload": 1031439
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 17,
            "rates": {
                "download": 2911240,
                "upload": 89442
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 338,
            "rates": {
                "download": 59800996,
                "upload": 4088474
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 185,
            "rates": {
                "download": 29933258,
                "upload": 1920518
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 31,
            "rates": {
                "download": 1466046,
                "upload": 209826
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 115,
            "rates": {
                "download": 13271525,
                "upload": 32155317
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 95,
            "rates": {
                "download": 11536573,
                "upload": 990960
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 18,
            "rates": {
                "download": 8884662,
                "upload": 355454
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 9,
            "rates": {
                "download": 218996,
                "upload": 4549
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 11,
            "rates": {
                "download": 2492079,
                "upload": 127140
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 45280,
                "upload": 16306
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 5,
            "rates": {
                "download": 460227,
                "upload": 34400
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1811,
                "upload": 724
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 12,
            "rates": {
                "download": 3472883,
                "upload": 2764334
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 8,
            "rates": {
                "download": 4507784,
                "upload": 59812
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 2631104,
                "upload": 74209
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 12,
            "rates": {
                "download": 3248100,
                "upload": 123711
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 275,
                "upload": 223
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 5447,
                "upload": 10970
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 1572,
                "upload": 1155
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 2,
            "rates": {
                "download": 395,
                "upload": 6
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 13,
            "rates": {
                "download": 1061254,
                "upload": 207468
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 5,
            "rates": {
                "download": 253466,
                "upload": 24431
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 29,
            "rates": {
                "download": 1191513,
                "upload": 92093
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 350,
            "rates": {
                "download": 23499549,
                "upload": 4167645
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 1,
            "rates": {
                "download": 513,
                "upload": 33
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1535,
            "rates": {
                "download": 244279824,
                "upload": 40295671
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 44,
            "rates": {
                "download": 2226538,
                "upload": 268472
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 379,
            "rates": {
                "download": 44981652,
                "upload": 9962288
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 646,
            "rates": {
                "download": 59579863,
                "upload": 7591609
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 300,
            "rates": {
                "download": 20566869,
                "upload": 4384835
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 655,
            "rates": {
                "download": 67073149,
                "upload": 6220677
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 356,
            "rates": {
                "download": 60031148,
                "upload": 4839093
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 11,
            "rates": {
                "download": 706083,
                "upload": 121093
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 52,
            "rates": {
                "download": 2744023,
                "upload": 174241
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 423,
            "rates": {
                "download": 48025006,
                "upload": 6405709
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 56,
            "rates": {
                "download": 6994683,
                "upload": 672502
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 205,
            "rates": {
                "download": 26607212,
                "upload": 1598866
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 192,
            "rates": {
                "download": 31670573,
                "upload": 19066323
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 93,
            "rates": {
                "download": 14849409,
                "upload": 957946
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 250,
            "rates": {
                "download": 26220596,
                "upload": 11803689
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 10,
            "rates": {
                "download": 77680,
                "upload": 28613
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 47016,
                "upload": 40775
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 22,
            "rates": {
                "download": 1421752,
                "upload": 120215
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 51,
            "rates": {
                "download": 760534,
                "upload": 163730
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 827,
            "rates": {
                "download": 139019788,
                "upload": 13672136
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 60,
            "rates": {
                "download": 9566494,
                "upload": 524584
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 62,
            "rates": {
                "download": 826156,
                "upload": 167758
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 636,
            "rates": {
                "download": 179304354,
                "upload": 19287824
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 338,
            "rates": {
                "download": 55408621,
                "upload": 4905648
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1503,
            "rates": {
                "download": 209389958,
                "upload": 46749262
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 26,
            "rates": {
                "download": 1758022,
                "upload": 347482
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 58,
            "rates": {
                "download": 20523564,
                "upload": 825739
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 63,
            "rates": {
                "download": 7388541,
                "upload": 1294931
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 222,
            "rates": {
                "download": 12998366,
                "upload": 2138498
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 213,
            "rates": {
                "download": 38087107,
                "upload": 6869914
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 30,
            "rates": {
                "download": 146872,
                "upload": 39190
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 49,
            "rates": {
                "download": 5419181,
                "upload": 696977
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 266,
            "rates": {
                "download": 25124905,
                "upload": 4604462
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 371,
            "rates": {
                "download": 25795175,
                "upload": 2682201
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 242,
            "rates": {
                "download": 28394992,
                "upload": 9386036
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 730,
            "rates": {
                "download": 105864489,
                "upload": 12306965
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 41,
            "rates": {
                "download": 4055813,
                "upload": 3224159
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 50,
            "rates": {
                "download": 2613380,
                "upload": 836587
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 690,
            "rates": {
                "download": 54506213,
                "upload": 26080736
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 336,
            "rates": {
                "download": 28705190,
                "upload": 3185920
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 2,
            "rates": {
                "download": 1010,
                "upload": 226
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 5,
            "rates": {
                "download": 301527,
                "upload": 113779
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 31,
            "rates": {
                "download": 4651512,
                "upload": 351338
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 8,
            "rates": {
                "download": 53943,
                "upload": 512144
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 5,
            "rates": {
                "download": 1835307,
                "upload": 253991
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 16,
            "rates": {
                "download": 2139124,
                "upload": 218821
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 11,
            "rates": {
                "download": 1076970,
                "upload": 98906
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 173,
            "rates": {
                "download": 21793279,
                "upload": 2884996
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 531,
            "rates": {
                "download": 92373819,
                "upload": 12251683
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 301,
            "rates": {
                "download": 43116233,
                "upload": 8888077
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 183,
            "rates": {
                "download": 27865403,
                "upload": 2160389
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 70,
            "rates": {
                "download": 8486941,
                "upload": 585604
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 130,
            "rates": {
                "download": 14958097,
                "upload": 1383955
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 10,
            "rates": {
                "download": 3170962,
                "upload": 127592
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 73,
            "rates": {
                "download": 19050151,
                "upload": 1029980
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 16,
            "rates": {
                "download": 583607,
                "upload": 27104
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 16,
            "rates": {
                "download": 2317778,
                "upload": 299011
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 55,
            "rates": {
                "download": 16550997,
                "upload": 593619
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 2,
            "rates": {
                "download": 162,
                "upload": 49
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 5,
            "rates": {
                "download": 5134,
                "upload": 4717
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 3,
            "rates": {
                "download": 4271,
                "upload": 4187
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 16,
            "rates": {
                "download": 1092930,
                "upload": 179175
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 19,
            "rates": {
                "download": 4099030,
                "upload": 198108
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 17,
            "rates": {
                "download": 8158910,
                "upload": 216152
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 29,
            "rates": {
                "download": 7671456,
                "upload": 436335
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 19,
            "rates": {
                "download": 3201488,
                "upload": 243677
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 27,
            "rates": {
                "download": 16123585,
                "upload": 803119
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 2,
            "rates": {
                "download": 540,
                "upload": 262
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 100,
            "rates": {
                "download": 14267985,
                "upload": 2026557
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 4,
            "rates": {
                "download": 4164,
                "upload": 6233
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 1,
            "rates": {
                "download": 397,
                "upload": 9
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 131,
            "rates": {
                "download": 48985767,
                "upload": 4065963
            },
            "last_updated": "2017-06-28T13:45:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 17,
            "rates": {
                "download": 15059177,
                "upload": 696356
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 6,
            "rates": {
                "download": 150160,
                "upload": 24561
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 213,
            "rates": {
                "download": 25031466,
                "upload": 2501057
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 220,
            "rates": {
                "download": 20548031,
                "upload": 1905788
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 91,
            "rates": {
                "download": 13547423,
                "upload": 2227604
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 223,
            "rates": {
                "download": 18125027,
                "upload": 6740774
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 142,
            "rates": {
                "download": 6362192,
                "upload": 951751
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 75,
            "rates": {
                "download": 21078004,
                "upload": 638956
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 170,
            "rates": {
                "download": 40466498,
                "upload": 2357928
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 131,
            "rates": {
                "download": 5185046,
                "upload": 1406996
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 13,
            "rates": {
                "download": 738388,
                "upload": 53075
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 312,
            "rates": {
                "download": 57533821,
                "upload": 4789177
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 177,
            "rates": {
                "download": 29395505,
                "upload": 1976662
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 33,
            "rates": {
                "download": 259757,
                "upload": 57447
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 111,
            "rates": {
                "download": 30799990,
                "upload": 31381926
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 102,
            "rates": {
                "download": 7235778,
                "upload": 577368
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 19,
            "rates": {
                "download": 9121947,
                "upload": 373479
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 8,
            "rates": {
                "download": 210757,
                "upload": 2914
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 11,
            "rates": {
                "download": 2449959,
                "upload": 120296
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 47005,
                "upload": 20378
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 1382,
                "upload": 794
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 2244,
                "upload": 812
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 13,
            "rates": {
                "download": 2965531,
                "upload": 2706669
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 8,
            "rates": {
                "download": 4405507,
                "upload": 39757
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 1080712,
                "upload": 28753
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 12,
            "rates": {
                "download": 5441787,
                "upload": 186016
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 61625,
                "upload": 1769
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 854,
                "upload": 219
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 194,
                "upload": 20
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 2,
            "rates": {
                "download": 6056,
                "upload": 25057
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 12,
            "rates": {
                "download": 530147,
                "upload": 86348
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 6,
            "rates": {
                "download": 6293,
                "upload": 2709
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 29,
            "rates": {
                "download": 2989162,
                "upload": 205035
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 330,
            "rates": {
                "download": 36148569,
                "upload": 7028280
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 938,
                "upload": 252
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1591,
            "rates": {
                "download": 272470614,
                "upload": 49527037
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 47,
            "rates": {
                "download": 2076677,
                "upload": 267761
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 367,
            "rates": {
                "download": 36973740,
                "upload": 4823663
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 649,
            "rates": {
                "download": 57724236,
                "upload": 7592003
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 275,
            "rates": {
                "download": 15016394,
                "upload": 3304852
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 651,
            "rates": {
                "download": 68752041,
                "upload": 33569377
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 367,
            "rates": {
                "download": 54317075,
                "upload": 4422656
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 17,
            "rates": {
                "download": 6732234,
                "upload": 203000
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 66,
            "rates": {
                "download": 2040997,
                "upload": 156415
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 432,
            "rates": {
                "download": 37990774,
                "upload": 3790391
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 58,
            "rates": {
                "download": 4243058,
                "upload": 563252
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 200,
            "rates": {
                "download": 24583646,
                "upload": 2328921
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 196,
            "rates": {
                "download": 23644094,
                "upload": 4972528
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 89,
            "rates": {
                "download": 8908937,
                "upload": 4308737
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 263,
            "rates": {
                "download": 35500474,
                "upload": 7591031
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 12,
            "rates": {
                "download": 1464895,
                "upload": 58860
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 60055,
                "upload": 35762
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 21,
            "rates": {
                "download": 548518,
                "upload": 75199
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 70,
            "rates": {
                "download": 601479,
                "upload": 298755
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 826,
            "rates": {
                "download": 107592901,
                "upload": 13989450
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 59,
            "rates": {
                "download": 9186048,
                "upload": 546274
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 60,
            "rates": {
                "download": 4471869,
                "upload": 320992
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 674,
            "rates": {
                "download": 152057201,
                "upload": 16556917
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 346,
            "rates": {
                "download": 42800545,
                "upload": 3595519
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1548,
            "rates": {
                "download": 161765246,
                "upload": 31930050
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 28,
            "rates": {
                "download": 5139527,
                "upload": 328930
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 63,
            "rates": {
                "download": 24227122,
                "upload": 1139352
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 63,
            "rates": {
                "download": 9033679,
                "upload": 1588939
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 225,
            "rates": {
                "download": 13939838,
                "upload": 3588413
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 207,
            "rates": {
                "download": 30186957,
                "upload": 10367408
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 20,
            "rates": {
                "download": 293811,
                "upload": 94153
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 55,
            "rates": {
                "download": 2495578,
                "upload": 347651
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 285,
            "rates": {
                "download": 22410020,
                "upload": 7321590
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 373,
            "rates": {
                "download": 28876066,
                "upload": 3183786
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 262,
            "rates": {
                "download": 17991994,
                "upload": 9431156
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 723,
            "rates": {
                "download": 112006970,
                "upload": 10313691
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 38,
            "rates": {
                "download": 6666293,
                "upload": 3616745
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 50,
            "rates": {
                "download": 6302729,
                "upload": 601815
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 729,
            "rates": {
                "download": 64434572,
                "upload": 25154780
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 333,
            "rates": {
                "download": 29605655,
                "upload": 11680288
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 2,
            "rates": {
                "download": 755,
                "upload": 392
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 4,
            "rates": {
                "download": 339791,
                "upload": 17568
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 30,
            "rates": {
                "download": 17356785,
                "upload": 515020
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 5,
            "rates": {
                "download": 458034,
                "upload": 24106
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 6,
            "rates": {
                "download": 2843970,
                "upload": 126741
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 15,
            "rates": {
                "download": 1899072,
                "upload": 302660
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 10,
            "rates": {
                "download": 1961692,
                "upload": 160769
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 159,
            "rates": {
                "download": 10778688,
                "upload": 1592658
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 523,
            "rates": {
                "download": 79421972,
                "upload": 9882657
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 325,
            "rates": {
                "download": 62670770,
                "upload": 9797677
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 172,
            "rates": {
                "download": 26611052,
                "upload": 2896550
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 68,
            "rates": {
                "download": 7075589,
                "upload": 537376
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 151,
            "rates": {
                "download": 18940906,
                "upload": 1667322
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 9,
            "rates": {
                "download": 1331964,
                "upload": 120414
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 69,
            "rates": {
                "download": 5847263,
                "upload": 566497
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 10,
            "rates": {
                "download": 1185750,
                "upload": 88542
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 12,
            "rates": {
                "download": 5269895,
                "upload": 392068
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 53,
            "rates": {
                "download": 1423533,
                "upload": 190113
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 1,
            "rates": {
                "download": 80075,
                "upload": 1063677
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 1,
            "rates": {
                "download": 262,
                "upload": 35
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 19,
            "rates": {
                "download": 23714,
                "upload": 24335
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 21,
            "rates": {
                "download": 2703375,
                "upload": 168231
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 15,
            "rates": {
                "download": 9587852,
                "upload": 364317
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 32,
            "rates": {
                "download": 10134394,
                "upload": 464029
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 21,
            "rates": {
                "download": 398031,
                "upload": 136879
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 25,
            "rates": {
                "download": 19803749,
                "upload": 898260
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 1,
            "rates": {
                "download": 1421,
                "upload": 1293
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 1090,
                "upload": 683
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 99,
            "rates": {
                "download": 29181281,
                "upload": 1579444
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 6,
            "rates": {
                "download": 1789,
                "upload": 1333
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 1,
            "rates": {
                "download": 394,
                "upload": 15
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 136,
            "rates": {
                "download": 38760389,
                "upload": 2480043
            },
            "last_updated": "2017-06-28T14:00:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 22,
            "rates": {
                "download": 1275233,
                "upload": 163680
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 7,
            "rates": {
                "download": 46084,
                "upload": 12025
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 205,
            "rates": {
                "download": 46955926,
                "upload": 5763937
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 227,
            "rates": {
                "download": 22934507,
                "upload": 2661334
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 94,
            "rates": {
                "download": 8363336,
                "upload": 920331
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 227,
            "rates": {
                "download": 9359652,
                "upload": 2134333
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 137,
            "rates": {
                "download": 3090366,
                "upload": 1134926
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 79,
            "rates": {
                "download": 3906261,
                "upload": 517761
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 175,
            "rates": {
                "download": 58269412,
                "upload": 4621414
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 130,
            "rates": {
                "download": 8085029,
                "upload": 1775016
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 12,
            "rates": {
                "download": 941624,
                "upload": 63457
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 325,
            "rates": {
                "download": 47416118,
                "upload": 4040131
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 188,
            "rates": {
                "download": 32146127,
                "upload": 2456336
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 32,
            "rates": {
                "download": 442214,
                "upload": 75153
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 120,
            "rates": {
                "download": 20058582,
                "upload": 24625951
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 94,
            "rates": {
                "download": 12321788,
                "upload": 860621
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 20,
            "rates": {
                "download": 9577268,
                "upload": 396359
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 8,
            "rates": {
                "download": 208661,
                "upload": 6184
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 9,
            "rates": {
                "download": 425721,
                "upload": 19120
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 48372,
                "upload": 22097
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 352439,
                "upload": 32115
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1381,
                "upload": 383
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 14,
            "rates": {
                "download": 2818020,
                "upload": 2738533
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 9,
            "rates": {
                "download": 6320492,
                "upload": 71426
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 819960,
                "upload": 41260
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 12,
            "rates": {
                "download": 9496691,
                "upload": 314427
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 7766,
                "upload": 1251
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 58493,
                "upload": 72383
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 1433,
                "upload": 670
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 2,
            "rates": {
                "download": 2189,
                "upload": 3997
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 12,
            "rates": {
                "download": 2223929,
                "upload": 178815
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 5,
            "rates": {
                "download": 13597,
                "upload": 5861
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 26,
            "rates": {
                "download": 400634,
                "upload": 127954
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 345,
            "rates": {
                "download": 20795668,
                "upload": 4129083
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 3,
            "rates": {
                "download": 874,
                "upload": 302
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1611,
            "rates": {
                "download": 234832959,
                "upload": 46094468
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 48,
            "rates": {
                "download": 3144968,
                "upload": 665184
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 385,
            "rates": {
                "download": 27497469,
                "upload": 9907129
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 673,
            "rates": {
                "download": 102775005,
                "upload": 8864559
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 282,
            "rates": {
                "download": 20742901,
                "upload": 2632455
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 640,
            "rates": {
                "download": 76763440,
                "upload": 19686793
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 316,
            "rates": {
                "download": 66781059,
                "upload": 4668503
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 19,
            "rates": {
                "download": 9946294,
                "upload": 498421
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 63,
            "rates": {
                "download": 5144036,
                "upload": 319477
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 455,
            "rates": {
                "download": 31874750,
                "upload": 9068184
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 57,
            "rates": {
                "download": 8651761,
                "upload": 4393410
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 202,
            "rates": {
                "download": 18312086,
                "upload": 1915770
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 190,
            "rates": {
                "download": 24091723,
                "upload": 6513365
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 100,
            "rates": {
                "download": 14381138,
                "upload": 1172188
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 260,
            "rates": {
                "download": 49356556,
                "upload": 11834950
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 11,
            "rates": {
                "download": 15748,
                "upload": 177853
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 94898,
                "upload": 49833
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 17,
            "rates": {
                "download": 192649,
                "upload": 39603
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 63,
            "rates": {
                "download": 5122473,
                "upload": 330648
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 833,
            "rates": {
                "download": 149596677,
                "upload": 14424381
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 55,
            "rates": {
                "download": 6946649,
                "upload": 410580
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 67,
            "rates": {
                "download": 4238722,
                "upload": 2857939
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 682,
            "rates": {
                "download": 130980448,
                "upload": 18247322
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 335,
            "rates": {
                "download": 47119971,
                "upload": 3840243
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1589,
            "rates": {
                "download": 212138600,
                "upload": 47082100
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 27,
            "rates": {
                "download": 3442475,
                "upload": 239759
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 65,
            "rates": {
                "download": 9500996,
                "upload": 909964
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 66,
            "rates": {
                "download": 29905913,
                "upload": 2017850
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 229,
            "rates": {
                "download": 10109957,
                "upload": 1920938
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 221,
            "rates": {
                "download": 20508036,
                "upload": 17377111
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 21,
            "rates": {
                "download": 264796,
                "upload": 121569
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 59,
            "rates": {
                "download": 4481549,
                "upload": 501790
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 309,
            "rates": {
                "download": 23959732,
                "upload": 3602326
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 351,
            "rates": {
                "download": 31782862,
                "upload": 3804925
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 281,
            "rates": {
                "download": 34264700,
                "upload": 10513205
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 781,
            "rates": {
                "download": 91987179,
                "upload": 14843273
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 45,
            "rates": {
                "download": 3149175,
                "upload": 807186
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 54,
            "rates": {
                "download": 3297381,
                "upload": 548743
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 646,
            "rates": {
                "download": 71254301,
                "upload": 25619573
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 311,
            "rates": {
                "download": 31282181,
                "upload": 9207428
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 1,
            "rates": {
                "download": 553,
                "upload": 236
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 4,
            "rates": {
                "download": 21105,
                "upload": 8399
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 35,
            "rates": {
                "download": 14617470,
                "upload": 655019
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 11,
            "rates": {
                "download": 859060,
                "upload": 25481
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 4,
            "rates": {
                "download": 96896,
                "upload": 17230
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 16,
            "rates": {
                "download": 2931243,
                "upload": 289397
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 10,
            "rates": {
                "download": 782389,
                "upload": 93951
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 173,
            "rates": {
                "download": 17069842,
                "upload": 9945059
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 504,
            "rates": {
                "download": 75833934,
                "upload": 12087975
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 290,
            "rates": {
                "download": 90486548,
                "upload": 10004752
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 204,
            "rates": {
                "download": 21990705,
                "upload": 2029530
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 65,
            "rates": {
                "download": 11424696,
                "upload": 1011670
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 134,
            "rates": {
                "download": 13184096,
                "upload": 1383335
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 9,
            "rates": {
                "download": 7045,
                "upload": 6163
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 70,
            "rates": {
                "download": 5750224,
                "upload": 458931
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 5,
            "rates": {
                "download": 512231,
                "upload": 15573
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 17,
            "rates": {
                "download": 8330671,
                "upload": 397747
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 49,
            "rates": {
                "download": 707857,
                "upload": 153084
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 1,
            "rates": {
                "download": 124,
                "upload": 20
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 2,
            "rates": {
                "download": 51,
                "upload": 165
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 18,
            "rates": {
                "download": 5058886,
                "upload": 261791
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 19,
            "rates": {
                "download": 7445743,
                "upload": 429308
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 15,
            "rates": {
                "download": 10440860,
                "upload": 270252
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 35,
            "rates": {
                "download": 7989478,
                "upload": 449495
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 23,
            "rates": {
                "download": 11888988,
                "upload": 518292
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 27,
            "rates": {
                "download": 10377595,
                "upload": 3426949
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 104,
            "rates": {
                "download": 43159965,
                "upload": 2152210
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 5,
            "rates": {
                "download": 432,
                "upload": 13
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 3,
            "rates": {
                "download": 1667,
                "upload": 1735
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 126,
            "rates": {
                "download": 57347432,
                "upload": 4027840
            },
            "last_updated": "2017-06-28T14:15:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 21,
            "rates": {
                "download": 2302183,
                "upload": 593335
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 15,
            "rates": {
                "download": 248699,
                "upload": 22903
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 210,
            "rates": {
                "download": 22464267,
                "upload": 5572257
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 163,
            "rates": {
                "download": 9951205,
                "upload": 2240589
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 125,
            "rates": {
                "download": 6370001,
                "upload": 655001
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 203,
            "rates": {
                "download": 8457792,
                "upload": 1273968
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 167,
            "rates": {
                "download": 2817560,
                "upload": 504068
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 75,
            "rates": {
                "download": 1527574,
                "upload": 441088
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 201,
            "rates": {
                "download": 21496740,
                "upload": 3307111
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 126,
            "rates": {
                "download": 4387337,
                "upload": 898083
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 19,
            "rates": {
                "download": 35672,
                "upload": 16484
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 341,
            "rates": {
                "download": 44803818,
                "upload": 4335500
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 234,
            "rates": {
                "download": 34849813,
                "upload": 2647903
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 33,
            "rates": {
                "download": 848951,
                "upload": 144425
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 112,
            "rates": {
                "download": 14472293,
                "upload": 1286676
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 96,
            "rates": {
                "download": 19818736,
                "upload": 961810
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 20,
            "rates": {
                "download": 8505718,
                "upload": 352577
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 7,
            "rates": {
                "download": 242633,
                "upload": 2389
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 10,
            "rates": {
                "download": 1059122,
                "upload": 120860
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 56906,
                "upload": 13193
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 4,
            "rates": {
                "download": 396014,
                "upload": 75567
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1018,
                "upload": 257
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 14,
            "rates": {
                "download": 2624166,
                "upload": 2599210
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 8,
            "rates": {
                "download": 7040772,
                "upload": 65561
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 665372,
                "upload": 44269
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 12,
            "rates": {
                "download": 6246726,
                "upload": 212472
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 23081,
                "upload": 4191
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 939,
                "upload": 436
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 412,
                "upload": 8
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 2,
            "rates": {
                "download": 269993,
                "upload": 19126
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 13,
            "rates": {
                "download": 409619,
                "upload": 93445
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 5,
            "rates": {
                "download": 11637,
                "upload": 2253
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 27,
            "rates": {
                "download": 110001,
                "upload": 31525
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 357,
            "rates": {
                "download": 25148639,
                "upload": 3615863
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 4,
            "rates": {
                "download": 30031,
                "upload": 9879
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1581,
            "rates": {
                "download": 214283638,
                "upload": 49242830
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 47,
            "rates": {
                "download": 2302424,
                "upload": 365503
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 350,
            "rates": {
                "download": 31320674,
                "upload": 7206616
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 711,
            "rates": {
                "download": 41017390,
                "upload": 5916699
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 352,
            "rates": {
                "download": 22272437,
                "upload": 2799584
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 649,
            "rates": {
                "download": 73794526,
                "upload": 14526295
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 311,
            "rates": {
                "download": 67526616,
                "upload": 8759885
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 12,
            "rates": {
                "download": 2015339,
                "upload": 394453
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 59,
            "rates": {
                "download": 3869260,
                "upload": 372058
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 439,
            "rates": {
                "download": 49635884,
                "upload": 5162080
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 61,
            "rates": {
                "download": 5939459,
                "upload": 4437371
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 234,
            "rates": {
                "download": 31020615,
                "upload": 2102820
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 174,
            "rates": {
                "download": 35333151,
                "upload": 5698488
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 116,
            "rates": {
                "download": 10596959,
                "upload": 2736821
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 236,
            "rates": {
                "download": 26626644,
                "upload": 5151241
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 10,
            "rates": {
                "download": 6295,
                "upload": 3163
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 5,
            "rates": {
                "download": 335624,
                "upload": 80176
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 18,
            "rates": {
                "download": 1247744,
                "upload": 168895
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 72,
            "rates": {
                "download": 600133,
                "upload": 147844
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 745,
            "rates": {
                "download": 88104728,
                "upload": 11387268
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 68,
            "rates": {
                "download": 11399132,
                "upload": 590358
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 71,
            "rates": {
                "download": 2530997,
                "upload": 242127
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 670,
            "rates": {
                "download": 125785992,
                "upload": 14741189
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 283,
            "rates": {
                "download": 88486530,
                "upload": 4227860
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1539,
            "rates": {
                "download": 163249302,
                "upload": 30800043
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 30,
            "rates": {
                "download": 5150171,
                "upload": 489961
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 51,
            "rates": {
                "download": 5932239,
                "upload": 806662
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 92,
            "rates": {
                "download": 20011869,
                "upload": 11410637
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 226,
            "rates": {
                "download": 12010514,
                "upload": 2467142
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 259,
            "rates": {
                "download": 20047467,
                "upload": 16876904
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 46,
            "rates": {
                "download": 426871,
                "upload": 76741
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 59,
            "rates": {
                "download": 3738923,
                "upload": 763513
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 356,
            "rates": {
                "download": 28194748,
                "upload": 2669364
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 282,
            "rates": {
                "download": 21991565,
                "upload": 3159103
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 294,
            "rates": {
                "download": 21979586,
                "upload": 8875290
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 816,
            "rates": {
                "download": 77082290,
                "upload": 9586877
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 48,
            "rates": {
                "download": 5478187,
                "upload": 4178766
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 48,
            "rates": {
                "download": 18323644,
                "upload": 1022878
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 524,
            "rates": {
                "download": 47107303,
                "upload": 10433489
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 288,
            "rates": {
                "download": 21311814,
                "upload": 6256601
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 4,
            "rates": {
                "download": 14483,
                "upload": 38149
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 4,
            "rates": {
                "download": 604265,
                "upload": 30159
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 18,
            "rates": {
                "download": 1948585,
                "upload": 121407
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 8,
            "rates": {
                "download": 3966,
                "upload": 2881
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 3,
            "rates": {
                "download": 1086,
                "upload": 592
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 11,
            "rates": {
                "download": 5972224,
                "upload": 352352
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 11,
            "rates": {
                "download": 378163,
                "upload": 172902
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 202,
            "rates": {
                "download": 22103088,
                "upload": 1889426
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 508,
            "rates": {
                "download": 74898204,
                "upload": 13319927
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 256,
            "rates": {
                "download": 44991576,
                "upload": 3654434
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 172,
            "rates": {
                "download": 33632413,
                "upload": 1996580
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 74,
            "rates": {
                "download": 6490049,
                "upload": 676479
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 156,
            "rates": {
                "download": 19544403,
                "upload": 1917661
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 9,
            "rates": {
                "download": 1151575,
                "upload": 128525
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 71,
            "rates": {
                "download": 9710799,
                "upload": 923719
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 11,
            "rates": {
                "download": 42588,
                "upload": 4232
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 16,
            "rates": {
                "download": 18037628,
                "upload": 896103
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 44,
            "rates": {
                "download": 1971021,
                "upload": 152789
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 2,
            "rates": {
                "download": 270627,
                "upload": 13258
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 1,
            "rates": {
                "download": 28,
                "upload": 22
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 17,
            "rates": {
                "download": 23785,
                "upload": 13765
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 20,
            "rates": {
                "download": 3987860,
                "upload": 234257
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 14,
            "rates": {
                "download": 3760237,
                "upload": 123095
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 28,
            "rates": {
                "download": 13527726,
                "upload": 757510
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 24,
            "rates": {
                "download": 12333019,
                "upload": 513529
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 28,
            "rates": {
                "download": 9228648,
                "upload": 536239
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 15,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 93,
            "rates": {
                "download": 18991836,
                "upload": 1035433
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 6,
            "rates": {
                "download": 3243,
                "upload": 2394
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 7,
            "rates": {
                "download": 1095,
                "upload": 339
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 115,
            "rates": {
                "download": 26449132,
                "upload": 1434006
            },
            "last_updated": "2017-06-28T14:30:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 22,
            "rates": {
                "download": 4186542,
                "upload": 305604
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 4,
            "rates": {
                "download": 42156,
                "upload": 5651
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 218,
            "rates": {
                "download": 33540087,
                "upload": 4748218
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 135,
            "rates": {
                "download": 6485587,
                "upload": 654565
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 114,
            "rates": {
                "download": 3324322,
                "upload": 2028672
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 209,
            "rates": {
                "download": 6980748,
                "upload": 900494
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 146,
            "rates": {
                "download": 9093046,
                "upload": 793673
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 73,
            "rates": {
                "download": 2320767,
                "upload": 392375
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 187,
            "rates": {
                "download": 39690986,
                "upload": 3302801
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 129,
            "rates": {
                "download": 4423107,
                "upload": 869969
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 17,
            "rates": {
                "download": 96684,
                "upload": 12318
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 304,
            "rates": {
                "download": 56699178,
                "upload": 5191726
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 208,
            "rates": {
                "download": 34559558,
                "upload": 2187575
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 31,
            "rates": {
                "download": 55804,
                "upload": 37889
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 129,
            "rates": {
                "download": 22614173,
                "upload": 30345956
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 112,
            "rates": {
                "download": 21660899,
                "upload": 1060007
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 20,
            "rates": {
                "download": 6617107,
                "upload": 271384
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 8,
            "rates": {
                "download": 3886035,
                "upload": 112808
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 10,
            "rates": {
                "download": 821491,
                "upload": 20786
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 58487,
                "upload": 12906
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 2,
            "rates": {
                "download": 34687,
                "upload": 5513
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1750,
                "upload": 370
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 13,
            "rates": {
                "download": 4787020,
                "upload": 2597320
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 9,
            "rates": {
                "download": 59058,
                "upload": 9192
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 788005,
                "upload": 39259
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 13,
            "rates": {
                "download": 6335967,
                "upload": 213896
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 39581,
                "upload": 2550
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 22934,
                "upload": 15228
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 76,
                "upload": 23
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 1,
            "rates": {
                "download": 420,
                "upload": 103
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 12,
            "rates": {
                "download": 491434,
                "upload": 51332
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 6,
            "rates": {
                "download": 6370,
                "upload": 2754
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 24,
            "rates": {
                "download": 2747542,
                "upload": 466057
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 361,
            "rates": {
                "download": 32124635,
                "upload": 4235008
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 3,
            "rates": {
                "download": 801,
                "upload": 107
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1464,
            "rates": {
                "download": 218090391,
                "upload": 38607340
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 43,
            "rates": {
                "download": 2386676,
                "upload": 293344
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 304,
            "rates": {
                "download": 34199940,
                "upload": 3723099
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 661,
            "rates": {
                "download": 43750713,
                "upload": 41427895
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 327,
            "rates": {
                "download": 38792074,
                "upload": 3633648
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 609,
            "rates": {
                "download": 70048810,
                "upload": 7096865
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 296,
            "rates": {
                "download": 57091591,
                "upload": 8950520
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 10,
            "rates": {
                "download": 106754,
                "upload": 18480
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 62,
            "rates": {
                "download": 4328164,
                "upload": 207713
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 449,
            "rates": {
                "download": 53248716,
                "upload": 10722648
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 57,
            "rates": {
                "download": 9080189,
                "upload": 7592797
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 198,
            "rates": {
                "download": 35312002,
                "upload": 2942984
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 181,
            "rates": {
                "download": 38011374,
                "upload": 2961870
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 105,
            "rates": {
                "download": 8222287,
                "upload": 1810627
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 297,
            "rates": {
                "download": 60909787,
                "upload": 9616377
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 9,
            "rates": {
                "download": 3708,
                "upload": 2073
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 299018,
                "upload": 76117
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 19,
            "rates": {
                "download": 258642,
                "upload": 47445
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 71,
            "rates": {
                "download": 2207823,
                "upload": 1304498
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 753,
            "rates": {
                "download": 124788611,
                "upload": 14712211
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 57,
            "rates": {
                "download": 2347468,
                "upload": 279401
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 70,
            "rates": {
                "download": 6555716,
                "upload": 11441762
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 709,
            "rates": {
                "download": 146967243,
                "upload": 20365340
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 305,
            "rates": {
                "download": 65010329,
                "upload": 3584966
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1573,
            "rates": {
                "download": 254795270,
                "upload": 28108057
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 30,
            "rates": {
                "download": 4765071,
                "upload": 363891
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 61,
            "rates": {
                "download": 9293595,
                "upload": 863614
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 62,
            "rates": {
                "download": 8627824,
                "upload": 1127265
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 230,
            "rates": {
                "download": 10283836,
                "upload": 2017047
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 306,
            "rates": {
                "download": 18332841,
                "upload": 16594496
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 25,
            "rates": {
                "download": 612614,
                "upload": 82162
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 70,
            "rates": {
                "download": 2078789,
                "upload": 167686
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 404,
            "rates": {
                "download": 47393265,
                "upload": 5432585
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 176,
            "rates": {
                "download": 25366532,
                "upload": 2166066
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 263,
            "rates": {
                "download": 21177583,
                "upload": 6774197
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 817,
            "rates": {
                "download": 81736301,
                "upload": 9415954
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 49,
            "rates": {
                "download": 5726713,
                "upload": 2250973
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 50,
            "rates": {
                "download": 24172035,
                "upload": 1106314
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 546,
            "rates": {
                "download": 49840407,
                "upload": 6139337
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 331,
            "rates": {
                "download": 35204449,
                "upload": 4523837
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 1,
            "rates": {
                "download": 789,
                "upload": 221
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 6,
            "rates": {
                "download": 6836,
                "upload": 3394
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 17,
            "rates": {
                "download": 1374013,
                "upload": 75920
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 6,
            "rates": {
                "download": 1169,
                "upload": 475
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 3,
            "rates": {
                "download": 386784,
                "upload": 50971
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 11,
            "rates": {
                "download": 3362250,
                "upload": 737662
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 10,
            "rates": {
                "download": 662976,
                "upload": 65630
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 159,
            "rates": {
                "download": 12016859,
                "upload": 5514014
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 493,
            "rates": {
                "download": 82244169,
                "upload": 8983896
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 237,
            "rates": {
                "download": 39687189,
                "upload": 3092866
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 152,
            "rates": {
                "download": 50089943,
                "upload": 5677058
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 67,
            "rates": {
                "download": 18038692,
                "upload": 1173818
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 147,
            "rates": {
                "download": 41598649,
                "upload": 2375712
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 9,
            "rates": {
                "download": 91805,
                "upload": 19911
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 68,
            "rates": {
                "download": 12853266,
                "upload": 972136
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 7,
            "rates": {
                "download": 1732191,
                "upload": 100194
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 15,
            "rates": {
                "download": 3042553,
                "upload": 267720
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 49,
            "rates": {
                "download": 1491700,
                "upload": 255381
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 2,
            "rates": {
                "download": 400,
                "upload": 6
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 1,
            "rates": {
                "download": 2811,
                "upload": 2459
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 19,
            "rates": {
                "download": 1341014,
                "upload": 73003
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 18,
            "rates": {
                "download": 1287147,
                "upload": 148406
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 15,
            "rates": {
                "download": 1173365,
                "upload": 69471
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 29,
            "rates": {
                "download": 5333019,
                "upload": 3766674
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 26,
            "rates": {
                "download": 7162729,
                "upload": 360681
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 30,
            "rates": {
                "download": 12664982,
                "upload": 585543
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 2,
            "rates": {
                "download": 354,
                "upload": 350
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 2,
            "rates": {
                "download": 9837,
                "upload": 5625
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 99,
            "rates": {
                "download": 22070716,
                "upload": 1615815
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 5,
            "rates": {
                "download": 47814,
                "upload": 25783
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 2,
            "rates": {
                "download": 1370,
                "upload": 1393
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 120,
            "rates": {
                "download": 41833569,
                "upload": 1774094
            },
            "last_updated": "2017-06-28T14:45:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 23,
            "rates": {
                "download": 2932094,
                "upload": 249196
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 2,
            "rates": {
                "download": 3707,
                "upload": 1327
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 212,
            "rates": {
                "download": 23911306,
                "upload": 2201523
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 127,
            "rates": {
                "download": 6068288,
                "upload": 623322
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 114,
            "rates": {
                "download": 5084724,
                "upload": 3900893
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 205,
            "rates": {
                "download": 6803166,
                "upload": 1023634
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 123,
            "rates": {
                "download": 6546949,
                "upload": 548698
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 103,
            "rates": {
                "download": 3362613,
                "upload": 1139909
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 182,
            "rates": {
                "download": 12668399,
                "upload": 1124048
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 120,
            "rates": {
                "download": 3884443,
                "upload": 744843
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 16,
            "rates": {
                "download": 965990,
                "upload": 57353
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 298,
            "rates": {
                "download": 28463150,
                "upload": 2761386
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 202,
            "rates": {
                "download": 43432336,
                "upload": 3383527
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 34,
            "rates": {
                "download": 1336726,
                "upload": 163896
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 132,
            "rates": {
                "download": 19642733,
                "upload": 3318673
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 112,
            "rates": {
                "download": 39271659,
                "upload": 1923181
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 20,
            "rates": {
                "download": 9225689,
                "upload": 480343
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 8,
            "rates": {
                "download": 2722521,
                "upload": 97158
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 10,
            "rates": {
                "download": 995453,
                "upload": 499161
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 68302,
                "upload": 24464
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 496961,
                "upload": 28170
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1069,
                "upload": 324
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 12,
            "rates": {
                "download": 263286,
                "upload": 35204
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 9,
            "rates": {
                "download": 7218370,
                "upload": 99706
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 1173438,
                "upload": 40197
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 14,
            "rates": {
                "download": 6341256,
                "upload": 221768
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 7170,
                "upload": 407
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 24032,
                "upload": 15880
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 1,
            "rates": {
                "download": 402,
                "upload": 6
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 13,
            "rates": {
                "download": 2164973,
                "upload": 605918
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 6,
            "rates": {
                "download": 3757,
                "upload": 3159
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 27,
            "rates": {
                "download": 3006842,
                "upload": 210393
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 339,
            "rates": {
                "download": 32032789,
                "upload": 3812814
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 3,
            "rates": {
                "download": 1659,
                "upload": 859
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1437,
            "rates": {
                "download": 220392044,
                "upload": 30199153
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 44,
            "rates": {
                "download": 1697251,
                "upload": 267978
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 307,
            "rates": {
                "download": 34928890,
                "upload": 4601541
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 654,
            "rates": {
                "download": 43351938,
                "upload": 5274290
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 343,
            "rates": {
                "download": 39009934,
                "upload": 3157298
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 631,
            "rates": {
                "download": 59986361,
                "upload": 29729155
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 291,
            "rates": {
                "download": 44102364,
                "upload": 8447369
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 9,
            "rates": {
                "download": 153504,
                "upload": 27034
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 53,
            "rates": {
                "download": 2773329,
                "upload": 253564
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 438,
            "rates": {
                "download": 43462072,
                "upload": 5218086
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 64,
            "rates": {
                "download": 11295492,
                "upload": 8014097
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 198,
            "rates": {
                "download": 34852777,
                "upload": 2340431
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 167,
            "rates": {
                "download": 17667334,
                "upload": 2184150
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 107,
            "rates": {
                "download": 9277223,
                "upload": 4609819
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 334,
            "rates": {
                "download": 68472943,
                "upload": 9508539
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 7,
            "rates": {
                "download": 4335,
                "upload": 2250
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 119367,
                "upload": 43808
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 17,
            "rates": {
                "download": 3576167,
                "upload": 276893
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 60,
            "rates": {
                "download": 1818390,
                "upload": 2541895
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 745,
            "rates": {
                "download": 100713998,
                "upload": 12882622
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 57,
            "rates": {
                "download": 7874746,
                "upload": 564248
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 76,
            "rates": {
                "download": 1563663,
                "upload": 261238
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 740,
            "rates": {
                "download": 154850674,
                "upload": 15017211
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 311,
            "rates": {
                "download": 73864259,
                "upload": 11274971
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1587,
            "rates": {
                "download": 202572603,
                "upload": 31468419
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 30,
            "rates": {
                "download": 5818823,
                "upload": 519659
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 78,
            "rates": {
                "download": 23446140,
                "upload": 2315845
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 64,
            "rates": {
                "download": 13390066,
                "upload": 1366519
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 215,
            "rates": {
                "download": 9844989,
                "upload": 1442112
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 307,
            "rates": {
                "download": 26751615,
                "upload": 3155098
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 18,
            "rates": {
                "download": 764573,
                "upload": 84728
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 67,
            "rates": {
                "download": 3925921,
                "upload": 266027
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 400,
            "rates": {
                "download": 51487432,
                "upload": 5415567
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 162,
            "rates": {
                "download": 32008075,
                "upload": 2514204
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 263,
            "rates": {
                "download": 22659026,
                "upload": 4286554
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 831,
            "rates": {
                "download": 82088923,
                "upload": 11587604
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 52,
            "rates": {
                "download": 4721849,
                "upload": 2543686
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 50,
            "rates": {
                "download": 3958051,
                "upload": 585684
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 569,
            "rates": {
                "download": 48464066,
                "upload": 5477623
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 327,
            "rates": {
                "download": 42948325,
                "upload": 5219139
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 1,
            "rates": {
                "download": 621,
                "upload": 214
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 5,
            "rates": {
                "download": 17737,
                "upload": 8328
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 18,
            "rates": {
                "download": 2658982,
                "upload": 119402
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 7,
            "rates": {
                "download": 1584018,
                "upload": 124528
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 12,
            "rates": {
                "download": 4894883,
                "upload": 250982
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 11,
            "rates": {
                "download": 1883041,
                "upload": 144687
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 130,
            "rates": {
                "download": 31862333,
                "upload": 3041610
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 484,
            "rates": {
                "download": 87992095,
                "upload": 9422239
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 249,
            "rates": {
                "download": 35724106,
                "upload": 2435520
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 144,
            "rates": {
                "download": 16282341,
                "upload": 3205399
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 70,
            "rates": {
                "download": 11903537,
                "upload": 743204
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 145,
            "rates": {
                "download": 22976734,
                "upload": 2094042
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 6,
            "rates": {
                "download": 9345,
                "upload": 6054
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 74,
            "rates": {
                "download": 12864577,
                "upload": 656583
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 5,
            "rates": {
                "download": 4325,
                "upload": 1731
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 18,
            "rates": {
                "download": 3648975,
                "upload": 244292
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 46,
            "rates": {
                "download": 1582968,
                "upload": 223204
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 3,
            "rates": {
                "download": 2659,
                "upload": 2192
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 2,
            "rates": {
                "download": 88,
                "upload": 577
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 20,
            "rates": {
                "download": 386465,
                "upload": 42817
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 28,
            "rates": {
                "download": 5115550,
                "upload": 426386
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 16,
            "rates": {
                "download": 3450410,
                "upload": 202155
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 30,
            "rates": {
                "download": 5743812,
                "upload": 554970
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 25,
            "rates": {
                "download": 14685738,
                "upload": 807438
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 31,
            "rates": {
                "download": 11124884,
                "upload": 617010
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 1,
            "rates": {
                "download": 29,
                "upload": 23
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 3,
            "rates": {
                "download": 4871,
                "upload": 1713
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 2,
            "rates": {
                "download": 6052,
                "upload": 5155
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 111,
            "rates": {
                "download": 36914071,
                "upload": 2084480
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 5,
            "rates": {
                "download": 1342,
                "upload": 852
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 4,
            "rates": {
                "download": 95,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 128,
            "rates": {
                "download": 45995261,
                "upload": 2590869
            },
            "last_updated": "2017-06-28T15:00:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 23,
            "rates": {
                "download": 2577454,
                "upload": 536638
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 3,
            "rates": {
                "download": 261293,
                "upload": 16252
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 210,
            "rates": {
                "download": 35615177,
                "upload": 4244695
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 127,
            "rates": {
                "download": 51418808,
                "upload": 3067463
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 107,
            "rates": {
                "download": 9870376,
                "upload": 1954740
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 182,
            "rates": {
                "download": 10907257,
                "upload": 997749
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 141,
            "rates": {
                "download": 23353916,
                "upload": 1131391
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 82,
            "rates": {
                "download": 13559424,
                "upload": 1231826
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 180,
            "rates": {
                "download": 16812507,
                "upload": 1885899
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 125,
            "rates": {
                "download": 6014803,
                "upload": 618890
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 16,
            "rates": {
                "download": 307452,
                "upload": 19910
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 294,
            "rates": {
                "download": 55568637,
                "upload": 4300129
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 191,
            "rates": {
                "download": 32796535,
                "upload": 2795810
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 34,
            "rates": {
                "download": 743733,
                "upload": 637658
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 130,
            "rates": {
                "download": 20122122,
                "upload": 1203113
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 111,
            "rates": {
                "download": 23465864,
                "upload": 1348452
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 19,
            "rates": {
                "download": 5329373,
                "upload": 247421
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 9,
            "rates": {
                "download": 3007857,
                "upload": 63594
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 10,
            "rates": {
                "download": 650962,
                "upload": 338481
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 61433,
                "upload": 20467
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 2,
            "rates": {
                "download": 122261,
                "upload": 8795
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1140,
                "upload": 327
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 11,
            "rates": {
                "download": 693552,
                "upload": 61182
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 10,
            "rates": {
                "download": 6978945,
                "upload": 78074
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 551374,
                "upload": 45189
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 13,
            "rates": {
                "download": 14885278,
                "upload": 392545
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 1046,
                "upload": 329
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 3,
            "rates": {
                "download": 679679,
                "upload": 45453
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 1064,
                "upload": 624
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 2,
            "rates": {
                "download": 3303,
                "upload": 979
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 11,
            "rates": {
                "download": 791301,
                "upload": 86219
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 7,
            "rates": {
                "download": 484463,
                "upload": 28661
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 25,
            "rates": {
                "download": 1817055,
                "upload": 149633
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 344,
            "rates": {
                "download": 37287503,
                "upload": 5460834
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 178,
                "upload": 81
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1473,
            "rates": {
                "download": 279816545,
                "upload": 45902687
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 43,
            "rates": {
                "download": 1698286,
                "upload": 227910
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 302,
            "rates": {
                "download": 38642904,
                "upload": 5424758
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 626,
            "rates": {
                "download": 71530660,
                "upload": 7779833
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 323,
            "rates": {
                "download": 28949215,
                "upload": 3477631
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 630,
            "rates": {
                "download": 106801586,
                "upload": 15756383
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 292,
            "rates": {
                "download": 43907224,
                "upload": 5582294
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 10,
            "rates": {
                "download": 90184,
                "upload": 16124
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 61,
            "rates": {
                "download": 1980733,
                "upload": 230055
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 446,
            "rates": {
                "download": 36759903,
                "upload": 3725826
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 66,
            "rates": {
                "download": 9815372,
                "upload": 5232577
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 204,
            "rates": {
                "download": 19576276,
                "upload": 1339944
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 170,
            "rates": {
                "download": 23236093,
                "upload": 2837421
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 105,
            "rates": {
                "download": 15062391,
                "upload": 4470098
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 336,
            "rates": {
                "download": 72441393,
                "upload": 12602210
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 9,
            "rates": {
                "download": 11308,
                "upload": 8923
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 69380,
                "upload": 41213
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 19,
            "rates": {
                "download": 1298514,
                "upload": 114243
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 66,
            "rates": {
                "download": 2126872,
                "upload": 495279
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 737,
            "rates": {
                "download": 77284125,
                "upload": 9581092
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 48,
            "rates": {
                "download": 914966,
                "upload": 118627
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 66,
            "rates": {
                "download": 8860070,
                "upload": 1267106
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 785,
            "rates": {
                "download": 157404432,
                "upload": 12735598
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 307,
            "rates": {
                "download": 39259898,
                "upload": 3219326
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1588,
            "rates": {
                "download": 255767814,
                "upload": 35931642
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 32,
            "rates": {
                "download": 9428212,
                "upload": 1180878
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 78,
            "rates": {
                "download": 45814555,
                "upload": 2425178
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 60,
            "rates": {
                "download": 6258689,
                "upload": 1839506
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 224,
            "rates": {
                "download": 16362184,
                "upload": 3342180
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 301,
            "rates": {
                "download": 35416788,
                "upload": 4916122
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 22,
            "rates": {
                "download": 471041,
                "upload": 60122
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 67,
            "rates": {
                "download": 2603301,
                "upload": 237546
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 387,
            "rates": {
                "download": 50425736,
                "upload": 5343471
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 151,
            "rates": {
                "download": 16590931,
                "upload": 1161392
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 266,
            "rates": {
                "download": 46120542,
                "upload": 3386259
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 821,
            "rates": {
                "download": 78484539,
                "upload": 9115715
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 48,
            "rates": {
                "download": 4104426,
                "upload": 1369206
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 50,
            "rates": {
                "download": 32950418,
                "upload": 2500432
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 566,
            "rates": {
                "download": 55454784,
                "upload": 9550187
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 321,
            "rates": {
                "download": 19744456,
                "upload": 11228915
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 1,
            "rates": {
                "download": 667,
                "upload": 265
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 13,
            "rates": {
                "download": 18823,
                "upload": 6393
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 15,
            "rates": {
                "download": 4123896,
                "upload": 117896
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 5,
            "rates": {
                "download": 2027129,
                "upload": 127033
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 3,
            "rates": {
                "download": 1119,
                "upload": 2667
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 15,
            "rates": {
                "download": 8070717,
                "upload": 459696
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 11,
            "rates": {
                "download": 2326832,
                "upload": 171007
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 138,
            "rates": {
                "download": 13794570,
                "upload": 1515372
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 477,
            "rates": {
                "download": 71820505,
                "upload": 8417800
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 248,
            "rates": {
                "download": 34643296,
                "upload": 4972239
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 138,
            "rates": {
                "download": 31295775,
                "upload": 1979829
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 74,
            "rates": {
                "download": 15330958,
                "upload": 839838
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 142,
            "rates": {
                "download": 24195721,
                "upload": 1504047
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 8,
            "rates": {
                "download": 19840,
                "upload": 3493
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 78,
            "rates": {
                "download": 8977539,
                "upload": 622536
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 5,
            "rates": {
                "download": 5843,
                "upload": 3148
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 15,
            "rates": {
                "download": 2816151,
                "upload": 243861
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 43,
            "rates": {
                "download": 3133832,
                "upload": 259428
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 1,
            "rates": {
                "download": 61,
                "upload": 8
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 1,
            "rates": {
                "download": 16268,
                "upload": 4886
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 19,
            "rates": {
                "download": 3445474,
                "upload": 152809
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 33,
            "rates": {
                "download": 5533386,
                "upload": 422071
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 20,
            "rates": {
                "download": 5327299,
                "upload": 295835
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 31,
            "rates": {
                "download": 12372501,
                "upload": 637121
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 29,
            "rates": {
                "download": 12131934,
                "upload": 816666
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 31,
            "rates": {
                "download": 9094286,
                "upload": 667836
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 1,
            "rates": {
                "download": 638,
                "upload": 359
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 1,
            "rates": {
                "download": 1814,
                "upload": 1465
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 4,
            "rates": {
                "download": 72252,
                "upload": 22070
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 1,
            "rates": {
                "download": 519,
                "upload": 83
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 1,
            "rates": {
                "download": 3,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 19,
                "upload": 2
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 113,
            "rates": {
                "download": 34793806,
                "upload": 1791056
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 3,
            "rates": {
                "download": 64937,
                "upload": 6029
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 3,
            "rates": {
                "download": 648,
                "upload": 130
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 129,
            "rates": {
                "download": 55378144,
                "upload": 2866362
            },
            "last_updated": "2017-06-28T15:15:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 23,
            "rates": {
                "download": 1245318,
                "upload": 149397
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 4,
            "rates": {
                "download": 109186,
                "upload": 10067
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 215,
            "rates": {
                "download": 19623526,
                "upload": 1726632
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 123,
            "rates": {
                "download": 13541636,
                "upload": 1852376
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 116,
            "rates": {
                "download": 11026608,
                "upload": 915226
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 191,
            "rates": {
                "download": 16501485,
                "upload": 24111826
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 146,
            "rates": {
                "download": 10094122,
                "upload": 917450
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 80,
            "rates": {
                "download": 5548454,
                "upload": 4155809
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 169,
            "rates": {
                "download": 14318441,
                "upload": 1594712
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 121,
            "rates": {
                "download": 5008536,
                "upload": 3373494
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 11,
            "rates": {
                "download": 671060,
                "upload": 131683
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 308,
            "rates": {
                "download": 33699464,
                "upload": 3784927
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 213,
            "rates": {
                "download": 25302503,
                "upload": 2407389
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 33,
            "rates": {
                "download": 1395485,
                "upload": 1431131
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 131,
            "rates": {
                "download": 19243074,
                "upload": 1415196
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 114,
            "rates": {
                "download": 12583507,
                "upload": 2030634
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 15,
            "rates": {
                "download": 4208736,
                "upload": 131770
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 7,
            "rates": {
                "download": 272221,
                "upload": 10213
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 10,
            "rates": {
                "download": 545770,
                "upload": 611881
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 68408,
                "upload": 25186
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 4,
            "rates": {
                "download": 845340,
                "upload": 53694
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 920,
                "upload": 159
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 10,
            "rates": {
                "download": 249477,
                "upload": 43275
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 8,
            "rates": {
                "download": 294701,
                "upload": 68711
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 490682,
                "upload": 28272
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 14,
            "rates": {
                "download": 5750978,
                "upload": 219871
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 88202,
                "upload": 2087
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 833828,
                "upload": 51450
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 2,
            "rates": {
                "download": 190,
                "upload": 177
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 11,
            "rates": {
                "download": 726851,
                "upload": 100586
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 6,
            "rates": {
                "download": 626181,
                "upload": 77550
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 26,
            "rates": {
                "download": 2190320,
                "upload": 144166
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 373,
            "rates": {
                "download": 40217047,
                "upload": 4094281
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 707,
                "upload": 427
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1602,
            "rates": {
                "download": 252944997,
                "upload": 39382850
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 41,
            "rates": {
                "download": 1468969,
                "upload": 208820
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 238,
            "rates": {
                "download": 15376907,
                "upload": 3950305
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 638,
            "rates": {
                "download": 60862499,
                "upload": 15909924
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 340,
            "rates": {
                "download": 24154222,
                "upload": 6320624
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 599,
            "rates": {
                "download": 56274320,
                "upload": 25699590
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 292,
            "rates": {
                "download": 36547008,
                "upload": 5752043
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 18,
            "rates": {
                "download": 1797566,
                "upload": 156831
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 58,
            "rates": {
                "download": 594963,
                "upload": 148818
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 371,
            "rates": {
                "download": 44541346,
                "upload": 3954295
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 65,
            "rates": {
                "download": 15467906,
                "upload": 5279664
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 219,
            "rates": {
                "download": 15865728,
                "upload": 1258200
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 161,
            "rates": {
                "download": 32452560,
                "upload": 3157747
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 106,
            "rates": {
                "download": 11546884,
                "upload": 12136372
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 341,
            "rates": {
                "download": 48868704,
                "upload": 8809748
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 11,
            "rates": {
                "download": 8725,
                "upload": 4586
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 2,
            "rates": {
                "download": 11733,
                "upload": 11168
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 17,
            "rates": {
                "download": 16337,
                "upload": 7876
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 85,
            "rates": {
                "download": 2464192,
                "upload": 545636
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 724,
            "rates": {
                "download": 86607439,
                "upload": 11656539
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 57,
            "rates": {
                "download": 4922220,
                "upload": 279499
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 67,
            "rates": {
                "download": 6322618,
                "upload": 1127653
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 786,
            "rates": {
                "download": 153277875,
                "upload": 13575458
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 360,
            "rates": {
                "download": 70071767,
                "upload": 4112947
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1330,
            "rates": {
                "download": 137138790,
                "upload": 15574832
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 28,
            "rates": {
                "download": 17022061,
                "upload": 527413
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 87,
            "rates": {
                "download": 38927741,
                "upload": 1618706
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 61,
            "rates": {
                "download": 7042001,
                "upload": 544313
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 227,
            "rates": {
                "download": 19036810,
                "upload": 2980116
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 291,
            "rates": {
                "download": 44228536,
                "upload": 3250049
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 24,
            "rates": {
                "download": 290484,
                "upload": 57369
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 64,
            "rates": {
                "download": 2566756,
                "upload": 154958
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 382,
            "rates": {
                "download": 65654554,
                "upload": 5103111
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 153,
            "rates": {
                "download": 20683148,
                "upload": 3061662
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 284,
            "rates": {
                "download": 21576903,
                "upload": 3510280
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 785,
            "rates": {
                "download": 91889568,
                "upload": 10287652
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 46,
            "rates": {
                "download": 5296603,
                "upload": 1337842
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 51,
            "rates": {
                "download": 13789081,
                "upload": 845060
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 515,
            "rates": {
                "download": 51917228,
                "upload": 4927030
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 318,
            "rates": {
                "download": 16802688,
                "upload": 2699045
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 2,
            "rates": {
                "download": 427,
                "upload": 10
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 10,
            "rates": {
                "download": 11466,
                "upload": 5335
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 18,
            "rates": {
                "download": 5410157,
                "upload": 258402
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 5,
            "rates": {
                "download": 2229614,
                "upload": 70735
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 3,
            "rates": {
                "download": 124641,
                "upload": 5960
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 15,
            "rates": {
                "download": 17452176,
                "upload": 550794
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 10,
            "rates": {
                "download": 639437,
                "upload": 52318
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 154,
            "rates": {
                "download": 11792015,
                "upload": 1164311
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 470,
            "rates": {
                "download": 65308961,
                "upload": 12982920
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 299,
            "rates": {
                "download": 38186162,
                "upload": 3384554
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 143,
            "rates": {
                "download": 29713980,
                "upload": 1599472
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 83,
            "rates": {
                "download": 12688819,
                "upload": 1211223
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 145,
            "rates": {
                "download": 4769010,
                "upload": 735671
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 5,
            "rates": {
                "download": 61415,
                "upload": 10839
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 74,
            "rates": {
                "download": 4121009,
                "upload": 423224
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 5,
            "rates": {
                "download": 2131,
                "upload": 453
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 20,
            "rates": {
                "download": 2658038,
                "upload": 272887
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 47,
            "rates": {
                "download": 4334264,
                "upload": 344114
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 2,
            "rates": {
                "download": 204,
                "upload": 82
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 550,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 20,
            "rates": {
                "download": 2449862,
                "upload": 144792
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 32,
            "rates": {
                "download": 5748305,
                "upload": 327427
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 22,
            "rates": {
                "download": 4203062,
                "upload": 239220
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 32,
            "rates": {
                "download": 14238512,
                "upload": 642319
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 29,
            "rates": {
                "download": 13008730,
                "upload": 579432
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 30,
            "rates": {
                "download": 13727461,
                "upload": 1376029
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 1,
            "rates": {
                "download": 407,
                "upload": 6
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 2,
            "rates": {
                "download": 377,
                "upload": 757
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 2,
            "rates": {
                "download": 194017,
                "upload": 11481
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 117,
            "rates": {
                "download": 33718355,
                "upload": 1882206
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 2,
            "rates": {
                "download": 128,
                "upload": 8
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 133,
            "rates": {
                "download": 33530817,
                "upload": 2319267
            },
            "last_updated": "2017-06-28T15:30:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 22,
            "rates": {
                "download": 431190,
                "upload": 152569
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 1,
            "rates": {
                "download": 84391,
                "upload": 4943
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 228,
            "rates": {
                "download": 20972022,
                "upload": 1925632
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 135,
            "rates": {
                "download": 9306792,
                "upload": 1767320
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 93,
            "rates": {
                "download": 10848872,
                "upload": 1951390
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 200,
            "rates": {
                "download": 11899669,
                "upload": 1634048
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 137,
            "rates": {
                "download": 4047702,
                "upload": 791565
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 72,
            "rates": {
                "download": 2843843,
                "upload": 537499
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 168,
            "rates": {
                "download": 21289531,
                "upload": 1380573
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 104,
            "rates": {
                "download": 2838346,
                "upload": 514987
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 10,
            "rates": {
                "download": 58044,
                "upload": 12594
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 290,
            "rates": {
                "download": 44304819,
                "upload": 15289460
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 186,
            "rates": {
                "download": 26976596,
                "upload": 2071534
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 34,
            "rates": {
                "download": 263018,
                "upload": 172604
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 132,
            "rates": {
                "download": 26827063,
                "upload": 1687046
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 116,
            "rates": {
                "download": 19063649,
                "upload": 902307
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 17,
            "rates": {
                "download": 6253428,
                "upload": 247035
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 7,
            "rates": {
                "download": 320741,
                "upload": 9300
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 11,
            "rates": {
                "download": 416376,
                "upload": 84187
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 65951,
                "upload": 14645
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 5,
            "rates": {
                "download": 98755,
                "upload": 49614
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 2909,
                "upload": 581
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 11,
            "rates": {
                "download": 1409859,
                "upload": 69174
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 7,
            "rates": {
                "download": 7938897,
                "upload": 130080
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 3793013,
                "upload": 136648
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 13,
            "rates": {
                "download": 5145964,
                "upload": 210967
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 62931,
                "upload": 1775
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 321289,
                "upload": 41459
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 11,
            "rates": {
                "download": 448314,
                "upload": 106179
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 5,
            "rates": {
                "download": 79608,
                "upload": 33546
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 25,
            "rates": {
                "download": 168193,
                "upload": 31545
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 348,
            "rates": {
                "download": 37674808,
                "upload": 5019502
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 2333,
                "upload": 1235
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1576,
            "rates": {
                "download": 288149946,
                "upload": 39373911
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 42,
            "rates": {
                "download": 2783081,
                "upload": 221509
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 199,
            "rates": {
                "download": 21869472,
                "upload": 2519198
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 593,
            "rates": {
                "download": 82074377,
                "upload": 6962199
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 301,
            "rates": {
                "download": 34262396,
                "upload": 6411162
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 605,
            "rates": {
                "download": 73170748,
                "upload": 23885139
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 292,
            "rates": {
                "download": 57487301,
                "upload": 5668451
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 14,
            "rates": {
                "download": 1256342,
                "upload": 115502
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 59,
            "rates": {
                "download": 1613317,
                "upload": 165013
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 328,
            "rates": {
                "download": 32737042,
                "upload": 2292633
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 60,
            "rates": {
                "download": 6274658,
                "upload": 5365407
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 196,
            "rates": {
                "download": 19503130,
                "upload": 1665405
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 153,
            "rates": {
                "download": 30955718,
                "upload": 3388306
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 98,
            "rates": {
                "download": 12472724,
                "upload": 4551034
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 330,
            "rates": {
                "download": 64168616,
                "upload": 6247766
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 12,
            "rates": {
                "download": 2483261,
                "upload": 151148
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 3,
            "rates": {
                "download": 282750,
                "upload": 54372
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 19,
            "rates": {
                "download": 1571508,
                "upload": 179236
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 77,
            "rates": {
                "download": 2875690,
                "upload": 537822
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 697,
            "rates": {
                "download": 77964513,
                "upload": 15869819
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 43,
            "rates": {
                "download": 9427060,
                "upload": 781048
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 64,
            "rates": {
                "download": 2294543,
                "upload": 1075433
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 796,
            "rates": {
                "download": 140698864,
                "upload": 24073066
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 387,
            "rates": {
                "download": 81932031,
                "upload": 5611805
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1290,
            "rates": {
                "download": 169277717,
                "upload": 20518333
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 30,
            "rates": {
                "download": 12343998,
                "upload": 371079
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 96,
            "rates": {
                "download": 35542676,
                "upload": 1878202
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 62,
            "rates": {
                "download": 6951441,
                "upload": 574402
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 235,
            "rates": {
                "download": 6878087,
                "upload": 2239929
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 288,
            "rates": {
                "download": 41178691,
                "upload": 9593101
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 29,
            "rates": {
                "download": 172123,
                "upload": 59074
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 63,
            "rates": {
                "download": 5896308,
                "upload": 238849
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 366,
            "rates": {
                "download": 56658518,
                "upload": 6085366
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 143,
            "rates": {
                "download": 12889108,
                "upload": 2119650
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 264,
            "rates": {
                "download": 41484716,
                "upload": 3666352
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 792,
            "rates": {
                "download": 96133113,
                "upload": 11080093
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 41,
            "rates": {
                "download": 4453934,
                "upload": 3089390
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 49,
            "rates": {
                "download": 3040068,
                "upload": 358258
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 506,
            "rates": {
                "download": 36533513,
                "upload": 5572578
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 291,
            "rates": {
                "download": 34703729,
                "upload": 13707984
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 4,
            "rates": {
                "download": 2076,
                "upload": 782
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 7,
            "rates": {
                "download": 9286,
                "upload": 4573
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 13,
            "rates": {
                "download": 7076,
                "upload": 4676
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 10,
            "rates": {
                "download": 2144299,
                "upload": 137632
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 1,
            "rates": {
                "download": 65180,
                "upload": 10603
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 17,
            "rates": {
                "download": 8401926,
                "upload": 968754
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 16,
            "rates": {
                "download": 5431051,
                "upload": 365125
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 150,
            "rates": {
                "download": 16052109,
                "upload": 1819723
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 483,
            "rates": {
                "download": 87213418,
                "upload": 9293919
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 331,
            "rates": {
                "download": 30279136,
                "upload": 4387716
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 143,
            "rates": {
                "download": 37494719,
                "upload": 2475858
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 84,
            "rates": {
                "download": 13148692,
                "upload": 1100239
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 142,
            "rates": {
                "download": 34682840,
                "upload": 2027053
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 6,
            "rates": {
                "download": 7741,
                "upload": 3760
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 77,
            "rates": {
                "download": 5418179,
                "upload": 352201
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 3,
            "rates": {
                "download": 3981,
                "upload": 2910
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 20,
            "rates": {
                "download": 2704434,
                "upload": 348669
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 52,
            "rates": {
                "download": 1341339,
                "upload": 212821
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 3,
            "rates": {
                "download": 2221,
                "upload": 2321
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 2,
            "rates": {
                "download": 160309,
                "upload": 12782
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 23,
            "rates": {
                "download": 1777994,
                "upload": 235849
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 35,
            "rates": {
                "download": 4951803,
                "upload": 375255
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 25,
            "rates": {
                "download": 3339569,
                "upload": 253091
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 31,
            "rates": {
                "download": 10773790,
                "upload": 547198
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 26,
            "rates": {
                "download": 9400013,
                "upload": 456120
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 31,
            "rates": {
                "download": 21184237,
                "upload": 1595313
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 2,
            "rates": {
                "download": 377,
                "upload": 289
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 1,
            "rates": {
                "download": 802,
                "upload": 238
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 1,
            "rates": {
                "download": 1584,
                "upload": 837
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 386,
                "upload": 316
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 120,
            "rates": {
                "download": 42054051,
                "upload": 2135412
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 2,
            "rates": {
                "download": 810,
                "upload": 452
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 144,
            "rates": {
                "download": 36668793,
                "upload": 2147438
            },
            "last_updated": "2017-06-28T15:45:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 25,
            "rates": {
                "download": 536091,
                "upload": 201832
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 1,
            "rates": {
                "download": 1152,
                "upload": 41
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 230,
            "rates": {
                "download": 27934696,
                "upload": 5471998
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 122,
            "rates": {
                "download": 7870993,
                "upload": 950920
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 85,
            "rates": {
                "download": 8188277,
                "upload": 754857
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 196,
            "rates": {
                "download": 14513254,
                "upload": 1787172
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 132,
            "rates": {
                "download": 5023377,
                "upload": 530205
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 67,
            "rates": {
                "download": 6262832,
                "upload": 3734332
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 167,
            "rates": {
                "download": 18346356,
                "upload": 3585829
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 101,
            "rates": {
                "download": 4210860,
                "upload": 712971
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 6,
            "rates": {
                "download": 116464,
                "upload": 14619
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 287,
            "rates": {
                "download": 59400963,
                "upload": 4197051
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 203,
            "rates": {
                "download": 33094694,
                "upload": 3164952
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 32,
            "rates": {
                "download": 296898,
                "upload": 36337
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 147,
            "rates": {
                "download": 42290868,
                "upload": 2591776
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 109,
            "rates": {
                "download": 11086557,
                "upload": 727571
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 18,
            "rates": {
                "download": 7615101,
                "upload": 341575
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 6,
            "rates": {
                "download": 250647,
                "upload": 1716
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 12,
            "rates": {
                "download": 3742445,
                "upload": 207872
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 73495,
                "upload": 15384
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 6,
            "rates": {
                "download": 315631,
                "upload": 42510
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 865,
                "upload": 174
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 11,
            "rates": {
                "download": 322060,
                "upload": 33489
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 8,
            "rates": {
                "download": 8823410,
                "upload": 185381
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 1939544,
                "upload": 49768
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 14,
            "rates": {
                "download": 5364927,
                "upload": 228381
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 67188,
                "upload": 2049
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 1,
            "rates": {
                "download": 268634,
                "upload": 20835
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 9,
            "rates": {
                "download": 2396576,
                "upload": 144223
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 5,
            "rates": {
                "download": 5911,
                "upload": 2119
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 19,
            "rates": {
                "download": 291008,
                "upload": 582646
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 339,
            "rates": {
                "download": 32626473,
                "upload": 4957843
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 3,
            "rates": {
                "download": 10764,
                "upload": 6921
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1529,
            "rates": {
                "download": 244436531,
                "upload": 60175591
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 43,
            "rates": {
                "download": 4581248,
                "upload": 560520
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 205,
            "rates": {
                "download": 31051837,
                "upload": 2992614
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 582,
            "rates": {
                "download": 83632544,
                "upload": 8277431
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 327,
            "rates": {
                "download": 27688231,
                "upload": 7256429
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 570,
            "rates": {
                "download": 56411041,
                "upload": 8016895
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 283,
            "rates": {
                "download": 30553786,
                "upload": 6041126
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 1,
            "rates": {
                "download": 404,
                "upload": 8
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 50,
            "rates": {
                "download": 1922032,
                "upload": 173742
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 317,
            "rates": {
                "download": 29937012,
                "upload": 2680420
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 62,
            "rates": {
                "download": 12094874,
                "upload": 5083370
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 176,
            "rates": {
                "download": 23006334,
                "upload": 3874473
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 163,
            "rates": {
                "download": 18956336,
                "upload": 2819783
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 102,
            "rates": {
                "download": 13018607,
                "upload": 4754210
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 275,
            "rates": {
                "download": 27247556,
                "upload": 36921228
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 12,
            "rates": {
                "download": 1552906,
                "upload": 112082
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 5,
            "rates": {
                "download": 99884,
                "upload": 64047
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 22,
            "rates": {
                "download": 947153,
                "upload": 139381
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 119,
            "rates": {
                "download": 7027236,
                "upload": 646549
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 728,
            "rates": {
                "download": 78739573,
                "upload": 8525680
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 54,
            "rates": {
                "download": 2238960,
                "upload": 271869
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 59,
            "rates": {
                "download": 2126012,
                "upload": 762377
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 769,
            "rates": {
                "download": 168201563,
                "upload": 13262057
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 388,
            "rates": {
                "download": 86006148,
                "upload": 11068953
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1210,
            "rates": {
                "download": 143013023,
                "upload": 15099758
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 32,
            "rates": {
                "download": 14203871,
                "upload": 551929
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 95,
            "rates": {
                "download": 30882082,
                "upload": 3118581
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 58,
            "rates": {
                "download": 7679661,
                "upload": 980526
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 220,
            "rates": {
                "download": 11024829,
                "upload": 1343197
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 171,
            "rates": {
                "download": 7555147,
                "upload": 1201496
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 44,
            "rates": {
                "download": 490739,
                "upload": 126550
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 68,
            "rates": {
                "download": 539355,
                "upload": 1409403
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 352,
            "rates": {
                "download": 38218196,
                "upload": 4077008
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 136,
            "rates": {
                "download": 15305665,
                "upload": 2466036
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 227,
            "rates": {
                "download": 20431176,
                "upload": 4083076
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 793,
            "rates": {
                "download": 110242646,
                "upload": 14901756
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 41,
            "rates": {
                "download": 3988724,
                "upload": 2947530
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 47,
            "rates": {
                "download": 4009406,
                "upload": 480953
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 525,
            "rates": {
                "download": 53133116,
                "upload": 5767318
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 245,
            "rates": {
                "download": 20027831,
                "upload": 16934429
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 3,
            "rates": {
                "download": 1583,
                "upload": 241
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 8,
            "rates": {
                "download": 5778,
                "upload": 3648
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 13,
            "rates": {
                "download": 4108,
                "upload": 2626
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 6,
            "rates": {
                "download": 2126217,
                "upload": 143252
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 2,
            "rates": {
                "download": 8974,
                "upload": 6773
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 17,
            "rates": {
                "download": 11234181,
                "upload": 358312
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 15,
            "rates": {
                "download": 802744,
                "upload": 138921
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 125,
            "rates": {
                "download": 11516649,
                "upload": 1781254
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 476,
            "rates": {
                "download": 76260463,
                "upload": 11565412
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 337,
            "rates": {
                "download": 44241735,
                "upload": 3747530
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 150,
            "rates": {
                "download": 42909314,
                "upload": 2730099
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 91,
            "rates": {
                "download": 16678536,
                "upload": 982752
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 153,
            "rates": {
                "download": 24991986,
                "upload": 1882270
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 9,
            "rates": {
                "download": 4526991,
                "upload": 92376
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 72,
            "rates": {
                "download": 10725854,
                "upload": 674663
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 4,
            "rates": {
                "download": 1229,
                "upload": 1175
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 21,
            "rates": {
                "download": 1197625,
                "upload": 88561
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 59,
            "rates": {
                "download": 2182858,
                "upload": 325610
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 1,
            "rates": {
                "download": 6104,
                "upload": 2758
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 24,
            "rates": {
                "download": 15126014,
                "upload": 1241800
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 35,
            "rates": {
                "download": 4403744,
                "upload": 940950
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 23,
            "rates": {
                "download": 5189943,
                "upload": 364320
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 26,
            "rates": {
                "download": 13077983,
                "upload": 722998
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 26,
            "rates": {
                "download": 9584370,
                "upload": 529721
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 32,
            "rates": {
                "download": 18046854,
                "upload": 1615211
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 1,
            "rates": {
                "download": 776,
                "upload": 488
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 2,
            "rates": {
                "download": 49,
                "upload": 20
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 38,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 123,
            "rates": {
                "download": 48624762,
                "upload": 2764557
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 1,
            "rates": {
                "download": 427,
                "upload": 83
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 4,
            "rates": {
                "download": 1420,
                "upload": 548
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 144,
            "rates": {
                "download": 40309500,
                "upload": 2363279
            },
            "last_updated": "2017-06-28T16:00:00-04:00"
        },
        {
            "building_code": "ACW",
            "clients": 26,
            "rates": {
                "download": 8562371,
                "upload": 3508474
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 2,
            "rates": {
                "download": 3861,
                "upload": 1970
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 215,
            "rates": {
                "download": 24209554,
                "upload": 3777304
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 121,
            "rates": {
                "download": 5418629,
                "upload": 1198145
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 79,
            "rates": {
                "download": 3372978,
                "upload": 416168
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 186,
            "rates": {
                "download": 9830362,
                "upload": 2127474
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 116,
            "rates": {
                "download": 3546813,
                "upload": 385765
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 60,
            "rates": {
                "download": 5964846,
                "upload": 5105786
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 157,
            "rates": {
                "download": 11810377,
                "upload": 3257521
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 105,
            "rates": {
                "download": 5796790,
                "upload": 1340223
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 5,
            "rates": {
                "download": 90974,
                "upload": 10275
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 247,
            "rates": {
                "download": 48173550,
                "upload": 3316790
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 178,
            "rates": {
                "download": 46550642,
                "upload": 2538096
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 29,
            "rates": {
                "download": 19817,
                "upload": 9878
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 147,
            "rates": {
                "download": 50692819,
                "upload": 3184812
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 114,
            "rates": {
                "download": 9956978,
                "upload": 661820
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 16,
            "rates": {
                "download": 5705592,
                "upload": 250457
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 12,
            "rates": {
                "download": 743007,
                "upload": 76850
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 12,
            "rates": {
                "download": 1435508,
                "upload": 836665
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 4,
            "rates": {
                "download": 61609,
                "upload": 14796
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 6,
            "rates": {
                "download": 3215949,
                "upload": 75241
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 1118,
                "upload": 291
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 14,
            "rates": {
                "download": 1126150,
                "upload": 1253022
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 7,
            "rates": {
                "download": 8779718,
                "upload": 103904
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 3,
            "rates": {
                "download": 2500090,
                "upload": 107576
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 17,
            "rates": {
                "download": 2674236,
                "upload": 144579
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 219535,
                "upload": 12624
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 2,
            "rates": {
                "download": 506,
                "upload": 82
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 10,
            "rates": {
                "download": 2344443,
                "upload": 93326
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 6,
            "rates": {
                "download": 12507,
                "upload": 1739
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 21,
            "rates": {
                "download": 121621,
                "upload": 160796
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 359,
            "rates": {
                "download": 38679395,
                "upload": 8451500
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 53,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1533,
            "rates": {
                "download": 276329194,
                "upload": 45869978
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 40,
            "rates": {
                "download": 7790178,
                "upload": 449821
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 195,
            "rates": {
                "download": 37073372,
                "upload": 3588171
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 534,
            "rates": {
                "download": 42514625,
                "upload": 5772389
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 320,
            "rates": {
                "download": 31720871,
                "upload": 6171926
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 547,
            "rates": {
                "download": 82326185,
                "upload": 10604087
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 288,
            "rates": {
                "download": 36090781,
                "upload": 9361812
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 2,
            "rates": {
                "download": 2426,
                "upload": 1794
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 28,
            "rates": {
                "download": 33754,
                "upload": 21576
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 304,
            "rates": {
                "download": 32121132,
                "upload": 3923833
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 63,
            "rates": {
                "download": 13353838,
                "upload": 815518
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 167,
            "rates": {
                "download": 14402995,
                "upload": 1349087
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 150,
            "rates": {
                "download": 22785209,
                "upload": 3739364
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 87,
            "rates": {
                "download": 13820251,
                "upload": 792929
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 241,
            "rates": {
                "download": 41549824,
                "upload": 42355492
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 13,
            "rates": {
                "download": 2400473,
                "upload": 128479
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 5,
            "rates": {
                "download": 39658,
                "upload": 32531
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 17,
            "rates": {
                "download": 286034,
                "upload": 79457
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 53,
            "rates": {
                "download": 4059026,
                "upload": 225395
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 713,
            "rates": {
                "download": 116452016,
                "upload": 11658835
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 48,
            "rates": {
                "download": 4205279,
                "upload": 164001
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 49,
            "rates": {
                "download": 3274114,
                "upload": 1040136
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 755,
            "rates": {
                "download": 169215603,
                "upload": 16450719
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 384,
            "rates": {
                "download": 58141131,
                "upload": 7327488
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1167,
            "rates": {
                "download": 148025373,
                "upload": 16182193
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 32,
            "rates": {
                "download": 11084704,
                "upload": 323546
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 105,
            "rates": {
                "download": 19965375,
                "upload": 2595851
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 51,
            "rates": {
                "download": 6144073,
                "upload": 528379
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 171,
            "rates": {
                "download": 4091497,
                "upload": 3597531
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 150,
            "rates": {
                "download": 3550797,
                "upload": 6466023
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 49,
            "rates": {
                "download": 213513,
                "upload": 53540
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 71,
            "rates": {
                "download": 680375,
                "upload": 4872815
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 321,
            "rates": {
                "download": 40491482,
                "upload": 4518116
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 106,
            "rates": {
                "download": 10542808,
                "upload": 707033
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 208,
            "rates": {
                "download": 40594759,
                "upload": 3552636
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 742,
            "rates": {
                "download": 66127193,
                "upload": 9411825
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 39,
            "rates": {
                "download": 4027079,
                "upload": 3930450
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 47,
            "rates": {
                "download": 5763463,
                "upload": 579539
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 499,
            "rates": {
                "download": 43649368,
                "upload": 5902561
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 196,
            "rates": {
                "download": 22932098,
                "upload": 6347396
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 3,
            "rates": {
                "download": 1371,
                "upload": 199
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 8,
            "rates": {
                "download": 18509,
                "upload": 7052
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 13,
            "rates": {
                "download": 5016,
                "upload": 4362
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 6,
            "rates": {
                "download": 7350,
                "upload": 4136
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 2,
            "rates": {
                "download": 931,
                "upload": 746
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 25,
            "rates": {
                "download": 9226094,
                "upload": 346689
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 11,
            "rates": {
                "download": 663639,
                "upload": 64411
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 128,
            "rates": {
                "download": 5969189,
                "upload": 715574
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 516,
            "rates": {
                "download": 87708345,
                "upload": 39627928
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 325,
            "rates": {
                "download": 44163578,
                "upload": 6710393
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 144,
            "rates": {
                "download": 32044397,
                "upload": 1697534
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 106,
            "rates": {
                "download": 15084396,
                "upload": 1298455
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 125,
            "rates": {
                "download": 31720778,
                "upload": 1308013
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 12,
            "rates": {
                "download": 3526548,
                "upload": 40086
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 63,
            "rates": {
                "download": 8927979,
                "upload": 463940
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 3,
            "rates": {
                "download": 8066,
                "upload": 1581
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 22,
            "rates": {
                "download": 5741285,
                "upload": 393418
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 61,
            "rates": {
                "download": 15836094,
                "upload": 1138042
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 1,
            "rates": {
                "download": 753937,
                "upload": 38210
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 27,
            "rates": {
                "download": 7050568,
                "upload": 972605
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 41,
            "rates": {
                "download": 9718354,
                "upload": 568700
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 21,
            "rates": {
                "download": 8911318,
                "upload": 472578
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 26,
            "rates": {
                "download": 11269094,
                "upload": 552058
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 29,
            "rates": {
                "download": 13016355,
                "upload": 524989
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 34,
            "rates": {
                "download": 29840978,
                "upload": 1176616
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 1,
            "rates": {
                "download": 661,
                "upload": 434
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 133,
            "rates": {
                "download": 43483805,
                "upload": 3233372
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 3,
            "rates": {
                "download": 2277,
                "upload": 2113
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 3,
            "rates": {
                "download": 2117,
                "upload": 1225
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 157,
            "rates": {
                "download": 42911120,
                "upload": 9374575
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        }
    ]
}
```


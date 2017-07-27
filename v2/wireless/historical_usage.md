# Historical wireless usage statistics

```
GET /wireless/historical/usage.{format}
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
    <td>10005</td>
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

- Historical data is only available for the past 2 months
- Any value can be `null`


### Sources

- https://uwaterloo.ca/information-systems-technology/statistics/wifi-charts


## Parameters

```
GET /wireless/historical/usage.{format}
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
    <td>Timestamp of start time (in ISO 8601 format)</td>
  </tr>
  <tr>
    <td><b>to</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Timestamp of end time (in ISO 8601 format)</td>
  </tr>
</table>

**Output Formats**

- json
- xml


## Examples

```
GET /wireless/historical/usage.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/historical/usage.json?from=2017-06-28T160000-0400&to=2017-06-28T161500-0400**
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
        "requests": 1016649,
        "timestamp": 1501171197,
        "status": 200,
        "message": "Request successful",
        "method_id": 10005,
        "method": []
    },
    "data": [
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


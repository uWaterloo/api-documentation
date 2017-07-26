# Current wireless usage statistics

```
GET /wireless/usage.{format}
```

## Description

> This method returns current wireless usage statistics, by building.

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
</table>

**Output Formats**

- json
- xml


## Examples

```
GET /wireless/usage.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/usage.json**
- **https://api.uwaterloo.ca/v2/wireless/usage.xml**
- **https://api.uwaterloo.ca/v2/wireless/usage.json?callback=myResponse**


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
    <td>Timestamp of last collection</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
    "meta": {
        "requests": 1016345,
        "timestamp": 1501093729,
        "status": 200,
        "message": "Request successful",
        "method_id": 10000,
        "method": []
    },
    "data": [
        {
            "building_code": "ACW",
            "clients": 25,
            "rates": {
                "download": 17436782,
                "upload": 957810
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "AL",
            "clients": 8,
            "rates": {
                "download": 569,
                "upload": 177
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "ARC",
            "clients": 262,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "B1",
            "clients": 104,
            "rates": {
                "download": 894676,
                "upload": 118024
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "B2",
            "clients": 64,
            "rates": {
                "download": 93442,
                "upload": 11768
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EC1",
            "clients": 200,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EC2",
            "clients": 167,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EC3",
            "clients": 94,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EC4",
            "clients": 166,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EC5",
            "clients": 189,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UET",
            "clients": 19,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "BMH",
            "clients": 482,
            "rates": {
                "download": 13572457,
                "upload": 4030202
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "C2",
            "clients": 189,
            "rates": {
                "download": 14141973,
                "upload": 835789
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "BSC",
            "clients": 34,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CGR",
            "clients": 169,
            "rates": {
                "download": 180006,
                "upload": 75434
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CIF",
            "clients": 111,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "L03",
            "clients": 14,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "L09",
            "clients": 18,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "L15",
            "clients": 7,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "L27",
            "clients": 7,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTA",
            "clients": 3,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTB",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTC",
            "clients": 23,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTD",
            "clients": 9,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTE",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTG",
            "clients": 11,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTH",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTJ",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTK",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTL",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTM",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTN",
            "clients": 8,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTP",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CTQ",
            "clients": 11,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "COM",
            "clients": 27,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CPH",
            "clients": 370,
            "rates": {
                "download": 15887665,
                "upload": 3290107
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "CSB",
            "clients": 2,
            "rates": {
                "download": 405,
                "upload": 225
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "DC",
            "clients": 1524,
            "rates": {
                "download": 166792800,
                "upload": 25051565
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "DMS",
            "clients": 82,
            "rates": {
                "download": 587954,
                "upload": 96970
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "DWE",
            "clients": 318,
            "rates": {
                "download": 21081615,
                "upload": 1544042
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "E2",
            "clients": 687,
            "rates": {
                "download": 33839375,
                "upload": 5136514
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "E3",
            "clients": 338,
            "rates": {
                "download": 5805133,
                "upload": 1372191
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "E5",
            "clients": 540,
            "rates": {
                "download": 22936534,
                "upload": 1975124
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "E6",
            "clients": 356,
            "rates": {
                "download": 34217837,
                "upload": 6151382
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UWT",
            "clients": 23,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "ECH",
            "clients": 79,
            "rates": {
                "download": 2547688,
                "upload": 385164
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EIT",
            "clients": 387,
            "rates": {
                "download": 23397305,
                "upload": 1733845
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "ERC",
            "clients": 52,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "ESC",
            "clients": 212,
            "rates": {
                "download": 7125022,
                "upload": 508559
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EV1",
            "clients": 220,
            "rates": {
                "download": 169051025,
                "upload": 50601720
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EV2",
            "clients": 113,
            "rates": {
                "download": 3351163,
                "upload": 274783
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "EV3",
            "clients": 206,
            "rates": {
                "download": 21365644,
                "upload": 3239076
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "FED",
            "clients": 38,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "FRF",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "GSK",
            "clients": 9,
            "rates": {
                "download": 59789,
                "upload": 19493
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "GH",
            "clients": 28,
            "rates": {
                "download": 8876,
                "upload": 5913
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "GSC",
            "clients": 74,
            "rates": {
                "download": 4460,
                "upload": 1312
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "HH",
            "clients": 821,
            "rates": {
                "download": 82701055,
                "upload": 29223337
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "HS",
            "clients": 52,
            "rates": {
                "download": 47030,
                "upload": 6548
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "IHB",
            "clients": 43,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "LIB",
            "clients": 661,
            "rates": {
                "download": 83933673,
                "upload": 6868962
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "M3",
            "clients": 205,
            "rates": {
                "download": 15820243,
                "upload": 1878275
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "MC",
            "clients": 1836,
            "rates": {
                "download": 178577120,
                "upload": 30028834
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "MHR",
            "clients": 32,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "MKV",
            "clients": 99,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "ML",
            "clients": 75,
            "rates": {
                "download": 1293669,
                "upload": 156248
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "NH",
            "clients": 242,
            "rates": {
                "download": 4111808,
                "upload": 886856
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "OPT",
            "clients": 204,
            "rates": {
                "download": 1947276,
                "upload": 311653
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "Outdoors",
            "clients": 22,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "PAC",
            "clients": 31,
            "rates": {
                "download": 132354,
                "upload": 11810
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "PAS",
            "clients": 301,
            "rates": {
                "download": 19496709,
                "upload": 4035222
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "PHR",
            "clients": 557,
            "rates": {
                "download": 4020270,
                "upload": 332409
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "PHY",
            "clients": 250,
            "rates": {
                "download": 7059121,
                "upload": 649988
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "QNC",
            "clients": 666,
            "rates": {
                "download": 41759833,
                "upload": 5376212
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "RA2",
            "clients": 54,
            "rates": {
                "download": 2760586,
                "upload": 571110
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "RAC",
            "clients": 61,
            "rates": {
                "download": 76240,
                "upload": 50450
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "RCH",
            "clients": 450,
            "rates": {
                "download": 42319442,
                "upload": 9179267
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "REN",
            "clients": 378,
            "rates": {
                "download": 780691,
                "upload": 114401
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "REV",
            "clients": 3,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "REC",
            "clients": 25,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE",
            "clients": 5,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN",
            "clients": 132,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS",
            "clients": 16,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW",
            "clients": 22,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "RIA",
            "clients": 27,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "SCH",
            "clients": 189,
            "rates": {
                "download": 149797,
                "upload": 23759
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "SLC",
            "clients": 516,
            "rates": {
                "download": 47873720,
                "upload": 4918658
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "STC",
            "clients": 260,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "STJ",
            "clients": 222,
            "rates": {
                "download": 2547701,
                "upload": 177045
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "STP",
            "clients": 111,
            "rates": {
                "download": 13885551,
                "upload": 654778
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "TC",
            "clients": 165,
            "rates": {
                "download": 15693940,
                "upload": 1299267
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "TH",
            "clients": 7,
            "rates": {
                "download": 746,
                "upload": 878
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "TJB",
            "clients": 70,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UC",
            "clients": 5,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UCC",
            "clients": 13,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "V1C",
            "clients": 52,
            "rates": {
                "download": 273113,
                "upload": 34581
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE2",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE3",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE4",
            "clients": 3,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE5",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VE6",
            "clients": 3,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN1",
            "clients": 22,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN2",
            "clients": 31,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN3",
            "clients": 12,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN4",
            "clients": 24,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN5",
            "clients": 26,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VN6",
            "clients": 30,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS1",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS2",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS3",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS4",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS5",
            "clients": 5,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS6",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS7",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VS8",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW1",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW2",
            "clients": 1,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW3",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW4",
            "clients": 5,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW5",
            "clients": 2,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "VW6",
            "clients": 3,
            "rates": {
                "download": 1007,
                "upload": 1160
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "USC",
            "clients": 106,
            "rates": {
                "download": 2688675,
                "upload": 107412
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UNC",
            "clients": 9,
            "rates": {
                "download": 537,
                "upload": 327
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UWC",
            "clients": 0,
            "rates": {
                "download": 0,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        },
        {
            "building_code": "UEC",
            "clients": 146,
            "rates": {
                "download": 423,
                "upload": 0
            },
            "last_updated": "2017-07-20T15:30:00-04:00"
        }
    ]
}
```


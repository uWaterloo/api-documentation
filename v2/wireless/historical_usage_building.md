# Historical wireless building usage statistics

```
GET /wireless/usage/{building_code}.{format}
```

## Description

> This method returns historical wireless usage statistics for the requested building.

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

- Historical data is only available for the past 2 months
- Any value can be `null`


### Sources

- https://uwaterloo.ca/information-systems-technology/statistics/wifi-charts


## Parameters

```
GET /wireless/usage/{building_code}.{format}
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
GET /wireless/usage/{building_code}.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/historical/usage/MC.json?from=2017-06-28T160000-0400&to=2017-06-28T161500-0400**
- **https://api.uwaterloo.ca/v2/wireless/historical/usage/MC.xml**
- **https://api.uwaterloo.ca/v2/wireless/historical/usage/MC.json?callback=myResponse**


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
        "requests": 1016372,
        "timestamp": 1501095716,
        "status": 200,
        "message": "Request successful",
        "method_id": 10006,
        "method": []
    },
    "data": [
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
            "building_code": "MC",
            "clients": 1167,
            "rates": {
                "download": 148025373,
                "upload": 16182193
            },
            "last_updated": "2017-06-28T16:15:00-04:00"
        }
    ]
}
```


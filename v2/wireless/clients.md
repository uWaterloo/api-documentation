# Current wireless clients statistics

```
GET /wireless/clients.{format}
```

## Description

> This method returns wireless client information.

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
    <td>10002</td>
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
GET /wireless/clients.{format}
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
GET /wireless/clients.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/clients.json**
- **https://api.uwaterloo.ca/v2/wireless/clients.xml**
- **https://api.uwaterloo.ca/v2/wireless/clients.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>operating_system</b></td>
    <td>string</td>
    <td>Operating system</td>
  </tr>
  <tr>
    <td><b>radio_mode</b></td>
    <td>string</td>
    <td>Wireless radio mode</td>
  </tr>
  <tr>
    <td><b>count</b></td>
    <td>integer</td>
    <td>Number of clients with this Operating System/Radio Mode combination.</td>
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
        "requests": 1016357,
        "timestamp": 1501094463,
        "status": 200,
        "message": "Request successful",
        "method_id": 10002,
        "method": []
    },
    "data": [
        {
            "operating_system": "Android",
            "radio_mode": "a",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Android",
            "radio_mode": "ac",
            "count": 26,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Android",
            "radio_mode": "g",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Android",
            "radio_mode": "N",
            "count": 980,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "BlackBerry OS",
            "radio_mode": "n",
            "count": 5,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Chrome OS",
            "radio_mode": "N",
            "count": 6,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "iOS",
            "radio_mode": "ac",
            "count": 21,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "iOS",
            "radio_mode": "g",
            "count": 2,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "iOS",
            "radio_mode": "N",
            "count": 1110,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Linux",
            "radio_mode": "a",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Linux",
            "radio_mode": "ac",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Linux",
            "radio_mode": "g",
            "count": 2,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Linux",
            "radio_mode": "n",
            "count": 25,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Mac OS X",
            "radio_mode": "ac",
            "count": 42,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Mac OS X",
            "radio_mode": "g",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Mac OS X",
            "radio_mode": "N",
            "count": 683,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "PlayStation 3",
            "radio_mode": "g",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "RIM Tablet OS",
            "radio_mode": "N",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Unknown",
            "radio_mode": "a",
            "count": 19,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Unknown",
            "radio_mode": "ac",
            "count": 1149,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Unknown",
            "radio_mode": "ag",
            "count": 2,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Unknown",
            "radio_mode": "b",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Unknown",
            "radio_mode": "g",
            "count": 63,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Unknown",
            "radio_mode": "N",
            "count": 30302,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows",
            "radio_mode": "a",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows",
            "radio_mode": "ac",
            "count": 13,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows",
            "radio_mode": "g",
            "count": 7,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows",
            "radio_mode": "n",
            "count": 465,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 7",
            "radio_mode": "ac",
            "count": 11,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 7",
            "radio_mode": "g",
            "count": 11,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 7",
            "radio_mode": "n",
            "count": 298,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 8",
            "radio_mode": "a",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 8",
            "radio_mode": "ac",
            "count": 2,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 8",
            "radio_mode": "n",
            "count": 43,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows 98",
            "radio_mode": "n",
            "count": 3,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows CE",
            "radio_mode": "n",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows Mobile",
            "radio_mode": "g",
            "count": 7,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows Mobile",
            "radio_mode": "n",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows Mobile 8",
            "radio_mode": "n",
            "count": 4,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows Phone 8",
            "radio_mode": "n",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows XP",
            "radio_mode": "ac",
            "count": 1,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows XP",
            "radio_mode": "g",
            "count": 2,
            "last_updated": "2017-07-19T04:00:40-04:00"
        },
        {
            "operating_system": "Windows XP",
            "radio_mode": "n",
            "count": 32,
            "last_updated": "2017-07-19T04:00:40-04:00"
        }
    ]
}
```


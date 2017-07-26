# Current wireless auth statistics

```
GET /wireless/auth.{format}
```

## Description

> This method returns current wireless auth statistics.

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
    <td>10004</td>
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
GET /wireless/auth.{format}
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
GET /wireless/auth.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/auth.json**
- **https://api.uwaterloo.ca/v2/wireless/auth.xml**
- **https://api.uwaterloo.ca/v2/wireless/auth.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>issues</b></td>
    <td>object</td>
    <td>Authentication issues statistics<br><table>
  <tr>
    <td><b>count</b></td>
    <td>integer</td>
    <td>Number of authentication issues</td>
  </tr>
  <tr>
    <td><b>last_updated</b></td>
    <td>string</td>
    <td>Timestamp of last collection</td>
  </tr>
</table>
</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
    "meta": {
        "requests": 1016354,
        "timestamp": 1501094389,
        "status": 200,
        "message": "Request successful",
        "method_id": 10004,
        "method": []
    },
    "data": {
        "issues": {
            "count": 0,
            "last_updated": "1969-12-31T19:00:00-05:00"
        }
    }
}
```


# WATPark

```
GET /v2/parking/watpark.{format}
```

## Description

> This method returns real-time parking counts in select parking lots across campus.

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
    <td>1823</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>parking</td>
    <td><b>Service ID</b></td>
    <td>293</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>WATPark</td>
    <td><b>Data Type</b></td>
    <td>JSON Feed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every request (live)</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- We cannot modify the data from this method
- Any value can be `null`


### Sources

- http://watpark.com


## Parameters

```
GET /v2/parking/watpark.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>The format of the output</td>
  </tr>
  <tr>
    <td><b>key</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Your API key</td>
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
GET /v2/parking/watpark.{format}
```

- **https://api.uwaterloo.ca/v2/parking/watpark.json**
- **https://api.uwaterloo.ca/v2/parking/watpark.xml**
- **https://api.uwaterloo.ca/v2/parking/watpark.json.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>lot_name</b></td>
    <td>string</td>
    <td>Name of the parking lot</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Latitude of the parking lot</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Longitude of the parking lot</td>
  </tr>
  <tr>
    <td><b>capacity</b></td>
    <td>integer</td>
    <td>Capacity of the parking lot</td>
  </tr>
  <tr>
    <td><b>current_count</b></td>
    <td>integer</td>
    <td>Current count of the number of cars in the parking lot</td>
  </tr>
  <tr>
    <td><b>percent_filled</b></td>
    <td>integer</td>
    <td>Percentage of which the parking lot is filled, rounded to the nearest integer</td>
  </tr>
  <tr>
    <td><b>last_update</b></td>
    <td>string</td>
    <td>Time which the `current_count` was last updated</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":660143,
    "timestamp":1444252138,
    "status":200,
    "message":"Request successful",
    "method_id":1823,
    "method":{

    }
  },
  "data":[
    {
      "lot_name":"C",
      "latitude":43.467536,
      "longitude":-80.538379,
      "capacity":807,
      "current_count":401,
      "percent_filled":50,
      "last_updated":"2015-10-07T17:08:49-04:00"
    },
    {
      "lot_name":"N",
      "latitude":43.47491,
      "longitude":-80.544559,
      "capacity":252,
      "current_count":189,
      "percent_filled":75,
      "last_updated":"2015-10-07T17:08:39-04:00"
    },
    {
      "lot_name":"W",
      "latitude":43.474777,
      "longitude":-80.547579,
      "capacity":184,
      "current_count":135,
      "percent_filled":73,
      "last_updated":"2015-10-07T17:08:39-04:00"
    },
    {
      "lot_name":"X",
      "latitude":43.477526,
      "longitude":-80.545492,
      "capacity":630,
      "current_count":177,
      "percent_filled":28,
      "last_updated":"2015-10-07T17:08:18-04:00"
    }
  ]
}
```


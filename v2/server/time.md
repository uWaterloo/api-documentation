# Server Time

```
GET /server/time.{format}
```

## Description

> This method returns time information about the srver

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
    <td>No</td>
  </tr>
  <tr>
    <td><b>Method ID</b></td>
    <td>1087</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>server</td>
    <td><b>Service ID</b></td>
    <td>227</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>UW OpenData</td>
    <td><b>Data Type</b></td>
    <td>Language computed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every request (live)</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Calling this method does not affect usage
- Any value can be `null`


### Sources

- https://api.uwaterloo.ca


## Parameters

```
GET /server/time.{format}
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
GET /server/time.{format}
```

- **https://api.uwaterloo.ca/v2/server/time.json**
- **https://api.uwaterloo.ca/v2/server/time.xml**
- **https://api.uwaterloo.ca/v2/server/time.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>timestamp</b></td>
    <td>integer</td>
    <td>Current UNIX timestamp</td>
  </tr>
  <tr>
    <td><b>datetime</b></td>
    <td>string</td>
    <td>ISO8601 compatible current server timestamp</td>
  </tr>
  <tr>
    <td><b>timezone</b></td>
    <td>string</td>
    <td>Current server timezone</td>
  </tr>
  <tr>
    <td><b>key_reset_time</b></td>
    <td>integer</td>
    <td>UNIX timestamp of when the api call quota will reset</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":86,
    "timestamp":1381935632,
    "status":200,
    "message":"Request successful",
    "method_id":1087,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "timestamp":1381935632,
    "datetime":"2013-10-16T11:00:32-04:00",
    "timezone":"EDT",
    "key_reset_time":1384578000
  }
}
```


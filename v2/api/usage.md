# API Usage Stats

```
GET /api/usage.{format}
```

## Description

> This method returns user's api usage statistics

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
    <td>1097</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>api</td>
    <td><b>Service ID</b></td>
    <td>223</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>UW OpenData</td>
    <td><b>Data Type</b></td>
    <td>Direct DB Connection</td>
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
GET /api/usage.{format}
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
GET /api/usage.{format}
```

- **https://api.uwaterloo.ca/v2/api/usage.json**
- **https://api.uwaterloo.ca/v2/api/usage.xml**
- **https://api.uwaterloo.ca/v2/api/usage.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Developer's registered name</td>
  </tr>
  <tr>
    <td><b>api_key</b></td>
    <td>string</td>
    <td>Developer assigned API key</td>
  </tr>
  <tr>
    <td><b>monthly_calls</b></td>
    <td>integer</td>
    <td>Total calls made by the given key for the current month</td>
  </tr>
  <tr>
    <td><b>total_calls</b></td>
    <td>integer</td>
    <td>Total calls made by the given key</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":86,
    "timestamp":1381934735,
    "status":200,
    "message":"Request successful",
    "method_id":1097,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "name":"Kartik Talwar",
    "api_key":"853dfe5b299a7ab7f34d6a92b2339175",
    "monthly_calls":86,
    "total_calls":62
  }
}
```


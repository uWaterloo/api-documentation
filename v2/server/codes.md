# Server Error Codes

```
GET /server/codes.{format}
```

## Description

> This method returns a list of all possible API error codes

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
    <td>1091</td>
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
    <td>API computed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every request</td>
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
GET /server/codes.{format}
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
GET /server/codes.{format}
```

- **https://api.uwaterloo.ca/v2/server/codes.json**
- **https://api.uwaterloo.ca/v2/server/codes.xml**
- **https://api.uwaterloo.ca/v2/server/codes.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>code</b></td>
    <td>integer</td>
    <td>Numerical value of the Error code</td>
  </tr>
  <tr>
    <td><b>message</b></td>
    <td>string</td>
    <td>Accompanying error message</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":86,
    "timestamp":1381936008,
    "status":200,
    "message":"Request successful",
    "method_id":1091,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "code":200,
      "message":"Request successful"
    },
    {
      "code":204,
      "message":"No data returned"
    },
    {
      "code":401,
      "message":"Invalid API key"
    },
    {
      "code":403,
      "message":"The provided API key has been banned"
    },
    {
      "code":429,
      "message":"API request limit reached"
    },
    {
      "code":501,
      "message":"Invalid method"
    },
    {
      "code":511,
      "message":"API key is required (?key=)"
    }
  ]
}
```


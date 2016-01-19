# Lists information about GRT

```
GET /v2/transit/grt.{format}
```

## Description

> This method returns list of transit agencies that GRT connects to

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
    <td>1933</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>poi</td>
    <td><b>Service ID</b></td>
    <td>349</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>GTFS data from agency</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every day</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources



## Parameters

```
GET /v2/transit/grt.{format}
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
GET /v2/transit/grt.{format}
```

- **https://api.uwaterloo.ca/v2/transit/grt.json**
- **https://api.uwaterloo.ca/v2/transit/grt.xml**
- **https://api.uwaterloo.ca/v2/transit/grt.json?callback=myResponse**


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
    <td>Name of the agency</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>Agency website</td>
  </tr>
  <tr>
    <td><b>timezone</b></td>
    <td>string</td>
    <td>Agency stop data's timezone</td>
  </tr>
  <tr>
    <td><b>language</b></td>
    <td>string</td>
    <td>Stop data language</td>
  </tr>
  <tr>
    <td><b>phone</b></td>
    <td>string</td>
    <td>Agency phone number</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811694,
    "timestamp":1453161508,
    "status":200,
    "message":"Request successful",
    "method_id":1933,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Grand River Transit",
      "url":"http:\/\/www.grt.ca",
      "timezone":"America\/New_York",
      "language":null,
      "phone":"519-585-7555"
    }
  ]
}
```


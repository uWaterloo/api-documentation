# List of ATMs

```
GET /v2/poi/atms.{format}
```

## Description

> This method returns list of ATMs across campus.

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
    <td>1879</td>
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
    <td>Campus Map Team</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Upon pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- http://github.com/uWaterloo/datasets


## Parameters

```
GET /v2/poi/atms.{format}
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
- geojson
- xml


## Examples

```
GET /v2/poi/atms.{format}
```

- **https://api.uwaterloo.ca/v2/poi/atms.json**
- **https://api.uwaterloo.ca/v2/poi/atms.geojson**
- **https://api.uwaterloo.ca/v2/poi/atms.xml**
- **https://api.uwaterloo.ca/v2/poi/atms.json?callback=myResponse**


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
    <td>Name of the location</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Location description</td>
  </tr>
  <tr>
    <td><b>note</b></td>
    <td>string</td>
    <td>Any additional notes</td>
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
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811576,
    "timestamp":1453158945,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"CIBC",
      "description":null,
      "note":"Student Life Centre (SLC)",
      "latitude":43.471608889382,
      "longitude":-80.545644279658
    },
    {
      "name":"CIBC",
      "description":null,
      "note":"Student Life Centre (SLC)",
      "latitude":43.471581,
      "longitude":-80.545526
    },
    {
      "name":"CIBC",
      "description":null,
      "note":"William G. Davis Computer Research Centre (DC)",
      "latitude":43.472987666172,
      "longitude":-80.542651042342
    },
    {
      "name":"RBC",
      "description":null,
      "note":"Westmount Place Shopping Centre",
      "latitude":43.461585309973,
      "longitude":-80.537705822534
    },
    {
      "name":"Scotiabank",
      "description":null,
      "note":"St. Paul's University College (STP)",
      "latitude":43.467841,
      "longitude":-80.546304
    },
    {
      "name":"Scotiabank",
      "description":null,
      "note":"Campus Court Plaza",
      "latitude":43.47295085807,
      "longitude":-80.535225681961
    },
    {
      "name":"TD",
      "description":null,
      "note":"Laurelwood Shopping Centre",
      "latitude":43.467356151685,
      "longitude":-80.568387173116
    },
    {
      "name":"BMO",
      "description":null,
      "note":"University Plaza",
      "latitude":43.471548619399,
      "longitude":-80.5381533131
    }
  ]
}
```


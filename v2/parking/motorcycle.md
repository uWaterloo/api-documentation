# List of motorcycle allowed parking lots

```
GET /v2/parking/lots/motorcycle.{format}
```

## Description

> This method returns list of motorcycle allowed parking lots across campus.

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
    <td>1907</td>
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
    <td>Parking Services</td>
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
GET /v2/parking/lots/motorcycle.{format}
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
GET /v2/parking/lots/motorcycle.{format}
```

- **https://api.uwaterloo.ca/v2/parking/lots/motorcycle.json**
- **https://api.uwaterloo.ca/v2/parking/lots/motorcycle.geojson**
- **https://api.uwaterloo.ca/v2/parking/lots/motorcycle.xml**
- **https://api.uwaterloo.ca/v2/parking/lots/motorcycle.json?callback=myResponse**


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
    <td><b>description</b></td>
    <td>string</td>
    <td>Parking lot description</td>
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
    "requests":811532,
    "timestamp":1453157391,
    "status":200,
    "message":"Request successful",
    "method_id":1907,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"ML-EV3",
      "description":"Modern Languages (ML); Environment 3 (EV3)",
      "note":null,
      "latitude":43.468597619611,
      "longitude":-80.543191842735
    },
    {
      "name":"H",
      "description":"Psychology, Anthropology, Sociology (PAS)",
      "note":null,
      "latitude":43.466832595888,
      "longitude":-80.540616586804
    },
    {
      "name":"DWE-SCH",
      "description":"Douglas Wright Engineering Building (DWE); South Campus Hall (SCH)",
      "note":null,
      "latitude":43.469620169043,
      "longitude":-80.539586294297
    },
    {
      "name":"UWP",
      "description":"University of Waterloo Place (UWP)",
      "note":null,
      "latitude":43.470522215549,
      "longitude":-80.536178039293
    },
    {
      "name":"PAC-LHI-UC",
      "description":"Physical Activities Complex (PAC); Lyle S. Hallman Institute for Health Promotion (LHI); University Club (UC)",
      "note":null,
      "latitude":43.472745523991,
      "longitude":-80.546554997563
    },
    {
      "name":"V1-UC",
      "description":"Student Village 1 (V1); University Club (UC)",
      "note":null,
      "latitude":43.472316128251,
      "longitude":-80.548830851912
    },
    {
      "name":"N",
      "description":"Commissary (COM)",
      "note":null,
      "latitude":43.475101340233,
      "longitude":-80.543452415788
    },
    {
      "name":"E6-ECH",
      "description":"Engineering 6 (E6); East Campus Hall (ECH)",
      "note":null,
      "latitude":43.473501533583,
      "longitude":-80.539626851678
    }
  ]
}
```


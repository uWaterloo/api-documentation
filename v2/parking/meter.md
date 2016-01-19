# List of metered parking lots

```
GET /v2/parking/lots/meter.{format}
```

## Description

> This method returns list of metered parking lots across campus.

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
GET /v2/parking/lots/meter.{format}
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
GET /v2/parking/lots/meter.{format}
```

- **https://api.uwaterloo.ca/v2/parking/lots/meter.json**
- **https://api.uwaterloo.ca/v2/parking/lots/meter.geojson**
- **https://api.uwaterloo.ca/v2/parking/lots/meter.xml**
- **https://api.uwaterloo.ca/v2/parking/lots/meter.json?callback=myResponse**


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
    "requests":811534,
    "timestamp":1453157403,
    "status":200,
    "message":"Request successful",
    "method_id":1907,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"OPT",
      "description":"Optometry Building (OPT)",
      "note":null,
      "latitude":43.47584,
      "longitude":-80.54485
    },
    {
      "name":"DWE-SCH",
      "description":"Douglas Wright Engineering Building (DWE); South Campus Hall (SCH)",
      "note":null,
      "latitude":43.46966,
      "longitude":-80.53972
    },
    {
      "name":"E5-ECH",
      "description":"Engineering 5 (E5); East Campus Hall (ECH)",
      "note":null,
      "latitude":43.47317,
      "longitude":-80.53946
    },
    {
      "name":"PAC-SLC",
      "description":"Physical Activities Complex (PAC); Student Life Centre (SLC)",
      "note":null,
      "latitude":43.47164,
      "longitude":-80.54618
    },
    {
      "name":"V1-UC",
      "description":"Student Village 1 (V1); University Club (UC)",
      "note":null,
      "latitude":43.47218,
      "longitude":-80.54883
    },
    {
      "name":"MKV-V1",
      "description":"William Lyon Mackenzie King Village (MKV); Student Village 1 (V1)",
      "note":null,
      "latitude":43.47111,
      "longitude":-80.55115
    }
  ]
}
```


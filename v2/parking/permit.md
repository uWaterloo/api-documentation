# List of permit based parking lots

```
GET /v2/parking/lots/permit.{format}
```

## Description

> This method returns list of permit based parking lots across campus.

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
GET /v2/parking/lots/permit.{format}
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
GET /v2/parking/lots/permit.{format}
```

- **https://api.uwaterloo.ca/v2/parking/lots/permit.json**
- **https://api.uwaterloo.ca/v2/parking/lots/permit.geojson**
- **https://api.uwaterloo.ca/v2/parking/lots/permit.xml**
- **https://api.uwaterloo.ca/v2/parking/lots/permit.json?callback=myResponse**


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
    "requests":811535,
    "timestamp":1453157407,
    "status":200,
    "message":"Request successful",
    "method_id":1907,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"O",
      "description":"Optometry Building (OPT)",
      "note":null,
      "latitude":43.47656,
      "longitude":-80.54424
    },
    {
      "name":"K",
      "description":"William Lyon Mackenzie King Village (MKV); Student Village 1 (V1)",
      "note":null,
      "latitude":43.47231,
      "longitude":-80.55181
    },
    {
      "name":"R",
      "description":"B.C. Matthews Hall (BMH); Lyle S. Hallman Institute for Health Promotion (LHI); Federation Hall (FED)",
      "note":null,
      "latitude":43.47395,
      "longitude":-80.54704
    },
    {
      "name":"L",
      "description":"B.C. Matthews Hall (BMH); Energy Research Centre (ERC); Central Services Building (CSB); Commissary (COM)",
      "note":null,
      "latitude":43.47431,
      "longitude":-80.54412
    },
    {
      "name":"B",
      "description":"Engineering 5 (E5); William G. Davis Computer Research Centre (DC); East Campus Hall (ECH)",
      "note":null,
      "latitude":43.47373,
      "longitude":-80.5404
    },
    {
      "name":"T",
      "description":"Minota Hagey Residence (MHR)",
      "note":null,
      "latitude":43.46518,
      "longitude":-80.54225
    },
    {
      "name":"H",
      "description":"Psychology, Anthropology, Sociology (PAS); J.G. Hagey Hall of the Humanities (HH); William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "note":null,
      "latitude":43.46741,
      "longitude":-80.54036
    },
    {
      "name":"A",
      "description":"South Campus Hall (SCH); Douglas Wright Engineering Building (DWE)",
      "note":null,
      "latitude":43.46922,
      "longitude":-80.53739
    },
    {
      "name":"N",
      "description":"B.C. Matthews Hall (BMH)",
      "note":null,
      "latitude":43.47462,
      "longitude":-80.54516
    },
    {
      "name":"Q",
      "description":"East Campus 2 (EC2); East Campus 3 (EC3); General Services Complex (GSC)",
      "note":null,
      "latitude":43.47418,
      "longitude":-80.54114
    },
    {
      "name":"X",
      "description":"Optometry Building (OPT); Columbia Icefield (CIF)",
      "note":null,
      "latitude":43.47672,
      "longitude":-80.5471
    },
    {
      "name":"X",
      "description":"Optometry Building (OPT); Columbia Icefield (CIF)",
      "note":null,
      "latitude":43.47742,
      "longitude":-80.54593
    }
  ]
}
```


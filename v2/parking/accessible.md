# List of accessible parking lots

```
GET /v2/parking/lots/accessible.{format}
```

## Description

> This method returns list of accessible parking lots across campus.

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
GET /v2/parking/lots/accessible.{format}
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
GET /v2/parking/lots/accessible.{format}
```

- **https://api.uwaterloo.ca/v2/parking/lots/accessible.json**
- **https://api.uwaterloo.ca/v2/parking/lots/accessible.geojson**
- **https://api.uwaterloo.ca/v2/parking/lots/accessible.xml**
- **https://api.uwaterloo.ca/v2/parking/lots/accessible.json?callback=myResponse**


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
    "requests":811536,
    "timestamp":1453157421,
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
      "note":"Permit",
      "latitude":43.47582060866,
      "longitude":-80.545032106334
    },
    {
      "name":"V1-MKV",
      "description":"Student Village 1 (V1); William Lyon Mackenzie King Village (MKV)",
      "note":null,
      "latitude":43.471119689204,
      "longitude":-80.551042586209
    },
    {
      "name":"V1-UC",
      "description":"Student Village 1 (V1); University Club (UC)",
      "note":null,
      "latitude":43.472111492088,
      "longitude":-80.548738343836
    },
    {
      "name":"M",
      "description":"Lyle S. Hallman Institute for Health Promotion (LHI); B.C. Matthews Hall (BMH)",
      "note":"Visitor",
      "latitude":43.473397093956,
      "longitude":-80.546363005513
    },
    {
      "name":"PAC-SLC",
      "description":"Physical Activities Complex (PAC); Student Life Centre (SLC)",
      "note":null,
      "latitude":43.47168420989,
      "longitude":-80.545978098943
    },
    {
      "name":"BMH-ERC",
      "description":"B.C. Matthews Hall (BMH); Energy Research Centre (ERC)",
      "note":null,
      "latitude":43.473896296317,
      "longitude":-80.544718407338
    },
    {
      "name":"M3-MC",
      "description":"Mathematics 3 (M3); Mathematics & Computer Building (MC); William G. Davis Computer Research Centre (DC)",
      "note":null,
      "latitude":43.472883822692,
      "longitude":-80.543685186167
    },
    {
      "name":"Mc-M3",
      "description":"Mathematics & Computer Building (MC); Mathematics 3 (M3); William G. Davis Computer Research Centre (DC)",
      "note":null,
      "latitude":43.472660503165,
      "longitude":-80.543883083415
    },
    {
      "name":"COM-CSB",
      "description":"Commissary (COM); Central Services Building (CSB)",
      "note":null,
      "latitude":43.474351918111,
      "longitude":-80.542991396471
    },
    {
      "name":"DC-GSC",
      "description":"William G. Davis Computer Research Centre (DC); General Services Complex (GSC)",
      "note":null,
      "latitude":43.473076724244,
      "longitude":-80.54287815257
    },
    {
      "name":"E5",
      "description":"Engineering 5 (E5)",
      "note":null,
      "latitude":43.473344739338,
      "longitude":-80.540713809175
    },
    {
      "name":"E5",
      "description":"Engineering 5 (E5)",
      "note":null,
      "latitude":43.472432666171,
      "longitude":-80.539817155204
    },
    {
      "name":"E5-ECH",
      "description":"Engineering 6 (E6); East Campus Hall (ECH)",
      "note":null,
      "latitude":43.473078409799,
      "longitude":-80.539077554836
    },
    {
      "name":"B",
      "description":"Engineering 5 (E5); East Campus 2 (EC2)",
      "note":"Permit",
      "latitude":43.473754006652,
      "longitude":-80.541033438041
    },
    {
      "name":"UWC",
      "description":"University of Waterloo Place (UWP) Wilmot Court",
      "note":null,
      "latitude":43.470719990718,
      "longitude":-80.537153985226
    },
    {
      "name":"UWC-UWT",
      "description":"University of Waterloo Place (UWP) Wilmot Court, University of Waterloo Place (UWP) Eby Hall",
      "note":null,
      "latitude":43.470826236436,
      "longitude":-80.535927881616
    },
    {
      "name":"USC",
      "description":"University of Waterloo Place (UWP) Waterloo Court",
      "note":null,
      "latitude":43.469792441559,
      "longitude":-80.535543999339
    },
    {
      "name":"UNC-UET",
      "description":"University of Waterloo Place (UWP) Wellesley Court, University of Waterloo Place (UWP) Beck Hall",
      "note":null,
      "latitude":43.4711077397,
      "longitude":-80.534871245334
    },
    {
      "name":"UEC",
      "description":"University of Waterloo Place (UWP) Woolwich Court",
      "note":null,
      "latitude":43.47111135827,
      "longitude":-80.533982472349
    },
    {
      "name":"A",
      "description":"South Campus Hall (SCH)",
      "note":"Permit",
      "latitude":43.468956341497,
      "longitude":-80.538570469838
    },
    {
      "name":"C",
      "description":"South Campus Hall (SCH)",
      "note":"Visitor",
      "latitude":43.468384330828,
      "longitude":-80.538817508347
    },
    {
      "name":"TC-SCH",
      "description":"William M. Tatham Centre for Co-operative Education & Career Action (TC); South Campus Hall (SCH)",
      "note":null,
      "latitude":43.46884022055,
      "longitude":-80.54086581139
    },
    {
      "name":"PAS-HH",
      "description":"Psychology, Anthropology, Sociology (PAS); J.G. Hagey Hall of the Humanities (HH)",
      "note":null,
      "latitude":43.467388094618,
      "longitude":-80.541999182968
    },
    {
      "name":"T",
      "description":"Minota Hagey Residence (MHR)",
      "note":"Permit",
      "latitude":43.465372566484,
      "longitude":-80.541798353738
    },
    {
      "name":"H",
      "description":"Psychology, Anthropology, Sociology (PAS)",
      "note":"Permit",
      "latitude":43.466959897997,
      "longitude":-80.540573744598
    },
    {
      "name":"HV",
      "description":"South Campus Hall (SCH)",
      "note":"Visitor",
      "latitude":43.46857867934,
      "longitude":-80.5399130519
    },
    {
      "name":"DWE-SCH",
      "description":"Douglas Wright Engineering Building (DWE); South Campus Hall (SCH)",
      "note":null,
      "latitude":43.469630013084,
      "longitude":-80.539924801891
    },
    {
      "name":"LIB-ML",
      "description":"Dana Porter Library (LIB); Modern Languages (ML)",
      "note":null,
      "latitude":43.469335519496,
      "longitude":-80.542450074056
    },
    {
      "name":"LIB-NH",
      "description":"Dana Porter Library (LIB); Ira G. Needles Hall (NH)",
      "note":null,
      "latitude":43.469664186853,
      "longitude":-80.542708410111
    },
    {
      "name":"DC-C2",
      "description":"William G. Davis Computer Research Centre (DC); Chemistry 2 (C2)",
      "note":null,
      "latitude":43.472218254737,
      "longitude":-80.542412885408
    }
  ]
}
```


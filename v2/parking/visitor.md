# List of visitor parking lots

```
GET /v2/parking/lots/visitor.{format}
```

## Description

> This method returns list of visitor parking lots across campus.

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
GET /v2/parking/lots/visitor.{format}
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
GET /v2/parking/lots/visitor.{format}
```

- **https://api.uwaterloo.ca/v2/parking/lots/visitor.json**
- **https://api.uwaterloo.ca/v2/parking/lots/visitor.geojson**
- **https://api.uwaterloo.ca/v2/parking/lots/visitor.xml**
- **https://api.uwaterloo.ca/v2/parking/lots/visitor.json?callback=myResponse**


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
    "requests":811539,
    "timestamp":1453157505,
    "status":200,
    "message":"Request successful",
    "method_id":1907,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"X",
      "description":"Optometry Building (OPT); Columbia Icefield (CIF)",
      "note":"$5\/day - pay and display",
      "latitude":43.47693,
      "longitude":-80.54648
    },
    {
      "name":"X",
      "description":"Optometry Building (OPT); Columbia Icefield (CIF)",
      "note":"$5\/day - pay and display",
      "latitude":43.4778,
      "longitude":-80.54486
    },
    {
      "name":"W",
      "description":"Columbia Icefield (CIF)",
      "note":"$5\/day - pay and display",
      "latitude":43.47481,
      "longitude":-80.5476
    },
    {
      "name":"M",
      "description":"University Club (UC); Physical Activities Complex (PAC); Lyle S. Hallman Institute for Health Promotion (LHI)",
      "note":"$6 pay and display",
      "latitude":43.47323,
      "longitude":-80.54685
    },
    {
      "name":"D",
      "description":"Ira G. Needles Hall (NH)",
      "note":"Weekdays: $12\/hour up to $15 daily max. After 5 p.m. and weekends: $5 coin entry.",
      "latitude":43.46993,
      "longitude":-80.54351
    },
    {
      "name":"N",
      "description":"B.C. Matthews Hall (BMH); Energy Research Centre (ERC); Central Services Building (CSB); Commissary (CSB)",
      "note":"$5\/day - pay and display",
      "latitude":43.47507,
      "longitude":-80.54396
    },
    {
      "name":"J",
      "description":"Student Village 1 (V1)",
      "note":"$5 pay and display - pay in lot S",
      "latitude":43.47286,
      "longitude":-80.55022
    },
    {
      "name":"S",
      "description":"William Lyon Mackenzie King Village (MKV)",
      "note":"$5 pay and display",
      "latitude":43.47181,
      "longitude":-80.5532
    },
    {
      "name":"V",
      "description":"Ron Eydt Village (REV)",
      "note":"$5 pay and display - pay in lot S",
      "latitude":43.47134,
      "longitude":-80.55454
    },
    {
      "name":"CL",
      "description":"Columbia Lake Village (CLV); Columbia Lake Village North (CLN)",
      "note":"$5 pay and display",
      "latitude":43.47058,
      "longitude":-80.5631
    },
    {
      "name":"C",
      "description":"South Campus Hall (SCH); William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "note":"$5\/day - pay and display",
      "latitude":43.46733,
      "longitude":-80.53834
    },
    {
      "name":"HV",
      "description":"South Campus Hall (SCH); William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "note":"Weekdays: $2\/hour up to $15 daily max. After 5 p.m. and weekends: $5 coin entry.",
      "latitude":43.46836,
      "longitude":-80.53989
    },
    {
      "name":"UWP",
      "description":"University of Waterloo Place (UWP)",
      "note":"$5 pay and display",
      "latitude":43.47127,
      "longitude":-80.53371
    },
    {
      "name":"CGR",
      "description":"Conrad Grebel University College (CGR)",
      "note":"$1\/hour up to a $4 daily max",
      "latitude":43.4658,
      "longitude":-80.54427
    },
    {
      "name":"STP",
      "description":"St. Paul's University College (STP)",
      "note":"$5 coin entry",
      "latitude":43.46707,
      "longitude":-80.54617
    },
    {
      "name":"REN",
      "description":"Renison University College (REN)",
      "note":"$4 coin entry",
      "latitude":43.46891,
      "longitude":-80.54858
    },
    {
      "name":"STJ",
      "description":"St. Jerome's University (STJ)",
      "note":"$4 coin entry",
      "latitude":43.46959,
      "longitude":-80.54696
    },
    {
      "name":"OV",
      "description":"Optometry Building (OPT)",
      "note":"$5 coin exit",
      "latitude":43.4761,
      "longitude":-80.54387
    }
  ]
}
```


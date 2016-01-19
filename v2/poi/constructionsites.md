# List of construction sites

```
GET /v2/poi/constructionsites.{format}
```

## Description

> This method returns list of construction sites across campus.

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
GET /v2/poi/constructionsites.{format}
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
GET /v2/poi/constructionsites.{format}
```

- **https://api.uwaterloo.ca/v2/poi/constructionsites.json**
- **https://api.uwaterloo.ca/v2/poi/constructionsites.geojson**
- **https://api.uwaterloo.ca/v2/poi/constructionsites.xml**
- **https://api.uwaterloo.ca/v2/poi/constructionsites.json?callback=myResponse**


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
    "requests":811554,
    "timestamp":1453158035,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Needles Hall Expansion",
      "description":"An addition of 38,000 gross square feet of office and meeting space to the existing building.",
      "note":null,
      "latitude":43.470117058891,
      "longitude":-80.543861093073
    },
    {
      "name":"Science Teaching Complex",
      "description":null,
      "note":null,
      "latitude":43.47052512034,
      "longitude":-80.54339265232
    },
    {
      "name":"Federation Hall Expansion",
      "description":null,
      "note":null,
      "latitude":43.473291217367,
      "longitude":-80.548426198192
    },
    {
      "name":"Schlegel-University of Waterloo Research Institute for Aging (RIA)",
      "description":null,
      "note":null,
      "latitude":43.481022864069,
      "longitude":-80.549409813317
    },
    {
      "name":"Conrad Grebel University College - Academic Building Expansion",
      "description":null,
      "note":null,
      "latitude":43.466210751403,
      "longitude":-80.544980485367
    }
  ]
}
```


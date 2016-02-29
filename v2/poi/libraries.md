# List of libraries across the city

```
GET /v2/poi/libraries.{format}
```

## Description

> This method returns list of libraries across city.

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
GET /v2/poi/libraries.{format}
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
GET /v2/poi/libraries.{format}
```

- **https://api.uwaterloo.ca/v2/poi/libraries.json**
- **https://api.uwaterloo.ca/v2/poi/libraries.geojson**
- **https://api.uwaterloo.ca/v2/poi/libraries.xml**
- **https://api.uwaterloo.ca/v2/poi/libraries.json?callback=myResponse**


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
    "requests":811559,
    "timestamp":1453158165,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Dana Porter Library",
      "description":"Dana Porter Library (LIB)",
      "note":"http:\/\/www.lib.uwaterloo.ca\/tour\/MainET.html#porter",
      "latitude":43.469769479552,
      "longitude":-80.542372762749
    },
    {
      "name":"Davis Centre Library",
      "description":"William G. Davis Computer Research Centre (DC)",
      "note":"http:\/\/www.lib.uwaterloo.ca\/tour\/MainET.html#davis",
      "latitude":43.47258723304,
      "longitude":-80.542101736291
    },
    {
      "name":"St. Jerome's Library",
      "description":"St. Jerome's University (STJ)",
      "note":"http:\/\/sju.ca\/library.html",
      "latitude":43.468906050374,
      "longitude":-80.545792589556
    },
    {
      "name":"Lusi Wong Library",
      "description":"Renison University College (REN)",
      "note":"https:\/\/uwaterloo.ca\/renison\/lusi-wong-library",
      "latitude":43.469116903906,
      "longitude":-80.547391164016
    },
    {
      "name":"Milton Good Library",
      "description":"Conrad Grebel University College (CGR)",
      "note":"https:\/\/uwaterloo.ca\/grebel\/milton-good-library",
      "latitude":43.466208053962,
      "longitude":-80.544965770781
    },
    {
      "name":"The Centre for Teaching Excellence (CTE) Library",
      "description":"Environment 1 (EV1)",
      "note":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/research-teaching-and-learning\/cte-library",
      "latitude":43.468312138439,
      "longitude":-80.54281749708
    },
    {
      "name":"Centre for Career Action Library",
      "description":"William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "note":"https:\/\/uwaterloo.ca\/career-action\/resources-library\/library",
      "latitude":43.468749189392,
      "longitude":-80.541128946035
    },
    {
      "name":"Media Resources",
      "description":"Mathematics & Computer Building (MC)",
      "note":"https:\/\/uwaterloo.ca\/information-systems-technology\/services\/audio-visual-media-resources",
      "latitude":43.472154368956,
      "longitude":-80.543702408798
    },
    {
      "name":"Pharmacy Library",
      "description":"School of Pharmacy (PHR)",
      "note":"http:\/\/subjectguides.uwaterloo.ca\/content.php?pid=243188&sid=3626943",
      "latitude":43.45281373595,
      "longitude":-80.498933511151
    },
    {
      "name":"Musagetes Architecture Library",
      "description":"School of Architecture (ARC)",
      "note":"https:\/\/uwaterloo.ca\/library\/musagetes\/",
      "latitude":43.358112452575,
      "longitude":-80.316726223407
    },
    {
      "name":"Witer Learning Resource Centre",
      "description":"Optometry Building (OPT)",
      "note":"https:\/\/uwaterloo.ca\/witer-learning-resource-centre\/",
      "latitude":43.475815245449,
      "longitude":-80.545197882959
    }
  ]
}
```


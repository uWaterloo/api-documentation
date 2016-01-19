# List of emergency helplines

```
GET /v2/poi/helplines.{format}
```

## Description

> This method returns list of emergency helplines across campus.

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
GET /v2/poi/helplines.{format}
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
GET /v2/poi/helplines.{format}
```

- **https://api.uwaterloo.ca/v2/poi/helplines.json**
- **https://api.uwaterloo.ca/v2/poi/helplines.geojson**
- **https://api.uwaterloo.ca/v2/poi/helplines.xml**
- **https://api.uwaterloo.ca/v2/poi/helplines.json?callback=myResponse**


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
    "requests":811558,
    "timestamp":1453158124,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Columbia Icefield (CIF) Playing Fields",
      "description":"North Campus; east of Columbia Icefield (CIF) along the path between the playing fields 2 and 3.",
      "note":null,
      "latitude":43.474844436714,
      "longitude":-80.551531075133
    },
    {
      "name":"Visitor parking lot X",
      "description":"North Campus; visitor parking lot X near Hagey Boulevard.",
      "note":null,
      "latitude":43.476407083572,
      "longitude":-80.546808534201
    },
    {
      "name":"Visitor parking lot X",
      "description":"North Campus; visitor parking lot X near the Laurel Trail.",
      "note":null,
      "latitude":43.477507222197,
      "longitude":-80.544655088081
    },
    {
      "name":"Permit parking lot O",
      "description":"North Campus; permit parking lot O near the Laurel Trail.",
      "note":null,
      "latitude":43.477013075366,
      "longitude":-80.543949818088
    },
    {
      "name":null,
      "description":"South Campus; between Engineering 5 (E5) and East Campus Hall (ECH).",
      "note":null,
      "latitude":43.47314680517,
      "longitude":-80.539814132517
    },
    {
      "name":"Permit parking lot A",
      "description":"Permit parking lot A near intersection of University Avenue West and Seagram Drive.",
      "note":null,
      "latitude":43.468827302802,
      "longitude":-80.538146309938
    },
    {
      "name":"Permit parking lot A",
      "description":"Permit parking lot A away from intersection of University Avenue West and Seagram Drive.",
      "note":null,
      "latitude":43.469048672393,
      "longitude":-80.536916804837
    },
    {
      "name":"Visitor parking lot C",
      "description":"Visitor parking lot C away from University Avenue West.",
      "note":null,
      "latitude":43.467095282348,
      "longitude":-80.537979540992
    },
    {
      "name":"Visitor parking lot C",
      "description":"Visitor parking lot C in the centre.",
      "note":null,
      "latitude":43.467092951681,
      "longitude":-80.538625706632
    },
    {
      "name":"Visitor parking lot C",
      "description":"Visitor parking lot C near University Avenue West.",
      "note":null,
      "latitude":43.466848378051,
      "longitude":-80.539592171102
    },
    {
      "name":"Permit parking lot T",
      "description":"South Campus; permit parking lot T.",
      "note":null,
      "latitude":43.465380745314,
      "longitude":-80.541910766045
    },
    {
      "name":"St. Jerome's University (SJU)",
      "description":"South Campus; between St. Jerome's University (STJ) and Renison University College (REN).",
      "note":null,
      "latitude":43.469133116869,
      "longitude":-80.546401361915
    },
    {
      "name":"Westmount Road North",
      "description":"South Campus; along the path between Ron Eydt Village (REV) and Renison University College (REN) near Westmount Road North.",
      "note":null,
      "latitude":43.469470976,
      "longitude":-80.55125643196
    },
    {
      "name":"William Lyon Mackenzie King Village (MKV)",
      "description":"South Campus; along the path near Renison University College (REN), William Lyon Mackenzie King Village (MKV), and Student Village 1 (V1).",
      "note":null,
      "latitude":43.470426930683,
      "longitude":-80.552022336646
    }
  ]
}
```


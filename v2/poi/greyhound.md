# List of Greyhound bus stops

```
GET /v2/poi/greyhound.{format}
```

## Description

> This method returns list of Greyhound bus stops across city.

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
GET /v2/poi/greyhound.{format}
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
GET /v2/poi/greyhound.{format}
```

- **https://api.uwaterloo.ca/v2/poi/greyhound.json**
- **https://api.uwaterloo.ca/v2/poi/greyhound.geojson**
- **https://api.uwaterloo.ca/v2/poi/greyhound.xml**
- **https://api.uwaterloo.ca/v2/poi/greyhound.json?callback=myResponse**


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
  "meta": {
    "requests": 1328,
    "timestamp": 1476568844,
    "status": 200,
    "message": "Request successful",
    "method_id": 1889,
    "method": {
      
    }
  },
  "data": [
    {
      "name": "University of Waterloo",
      "description": "North of B.C. Matthews Hall (BMH)",
      "note": "Kitchener Charles St W; Kitchener Sportsworld;  Cambridge Glc, ON;  Guelph, Guelph U Gordon & College;  Guelph Univ Centre Loop;  Guelph Kortnight & Gor; Guelph Aberfoyle Brock Rd; Toronto U & Wellington; Toronto",
      "latitude": 43.473999090941,
      "longitude": -80.545923308322
    },
    {
      "name": "Wilfrid Laurier University",
      "description": null,
      "note": null,
      "latitude": 43.47510513598,
      "longitude": -80.527579188632
    },
    {
      "name": "Charles St. Transit Terminal",
      "description": null,
      "note": null,
      "latitude": 43.44943789805,
      "longitude": -80.492265104852
    },
    {
      "name": "Kitchener Sportsworld",
      "description": null,
      "note": null,
      "latitude": 43.409977,
      "longitude": -80.393938
    },
    {
      "name": "Cambridge",
      "description": null,
      "note": null,
      "latitude": 43.399403314036,
      "longitude": -80.330365309116
    }
  ]
}
```


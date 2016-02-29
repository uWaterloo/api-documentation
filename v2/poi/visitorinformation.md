# List of visitor information centers across Campus

```
GET /v2/poi/visitorinformation.{format}
```

## Description

> This method returns list of visitor information centers across campus.

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
GET /v2/poi/visitorinformation.{format}
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
GET /v2/poi/visitorinformation.{format}
```

- **https://api.uwaterloo.ca/v2/poi/visitorinformation.json**
- **https://api.uwaterloo.ca/v2/poi/visitorinformation.geojson**
- **https://api.uwaterloo.ca/v2/poi/visitorinformation.xml**
- **https://api.uwaterloo.ca/v2/poi/visitorinformation.json?callback=myResponse**


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
    "requests":811563,
    "timestamp":1453158282,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Turnkey Desk",
      "description":"Opens 24\/7 and knows just about everything around campus and the community. Get answers to questions, book a study room, and purchase Greyhound or GO Transit tickets.",
      "note":"Student Life Centre (SLC)",
      "opening_hours":"24\/7",
      "phone":"519-888-4434",
      "email":"turnkeys@uwaterloo.ca",
      "url":"https:\/\/uwaterloo.ca\/student-life-centre\/turnkey-desk",
      "latitude":43.47155,
      "longitude":-80.54565
    },
    {
      "name":"Police Services",
      "description":"Police Services serve to ensure a safe and secure campus environment. Report crime, aggressive behavior, suspicious activity, or other unusual situation. Register the serial number of bikes and electronics.",
      "note":"Commissary (COM)",
      "opening_hours":"24\/7",
      "phone":"519-888-4567, ext. 22222; 519-888-4911",
      "email":"uwpolice@uwaterloo.ca",
      "url":"https:\/\/uwaterloo.ca\/police\/",
      "latitude":43.47437,
      "longitude":-80.5428
    },
    {
      "name":"Parking Services",
      "description":"Parking Services manage campus lots and enforces parking regulations. Purchase parking permits, pay a ticket, or appeal an infraction.",
      "note":"Commissary (COM)",
      "opening_hours":"Mo-Fr 07:30-17:30",
      "phone":"519-888-4567, ext. 33100",
      "email":"uparking@uwaterloo.ca",
      "url":"https:\/\/uwaterloo.ca\/parking\/",
      "latitude":43.47438,
      "longitude":-80.54273
    },
    {
      "name":"Visitors Centre",
      "description":"Provides student-led campus tours, information for visitors, and tips for self-guided tours.",
      "note":"South Campus Hall (SCH)",
      "opening_hours":"Mo-Fr 08:30-16:30; Sa 10:00-16:00",
      "phone":"519-888-4567, ext. 33614",
      "email":"vcinfo@uwaterloo.ca",
      "url":"https:\/\/uwaterloo.ca\/find-out-more\/visit-waterloo\/visitors-centre",
      "latitude":43.46909,
      "longitude":-80.54026
    }
  ]
}
```


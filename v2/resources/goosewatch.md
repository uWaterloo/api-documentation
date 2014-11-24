# List of geese nests

```
GET /resources/goosewatch.{format}
```

## Description

> This method returns a list of geese nests during their spring mating season

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
    <td>1671</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>resources</td>
    <td><b>Service ID</b></td>
    <td>229</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Faculty of Environment - MAD Lab</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- This data is community curated on github in partnership with the Faculty of Environment's MAD Lab and http://goose-watch.uwaterloo.ca/
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/GooseWatch


## Parameters

```
GET /resources/goosewatch.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>key</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Your API key</td>
  </tr>
  <tr>
    <td><b>term</b></td>
    <td>filter</td>
    <td><i>no</i></td>
    <td>Four digit term representation</td>
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
- xml


## Examples

```
GET /resources/goosewatch.{format}
```

- **https://api.uwaterloo.ca/v2/resources/goosewatch.json**
- **https://api.uwaterloo.ca/v2/resources/goosewatch.xml**
- **https://api.uwaterloo.ca/v2/resources/goosewatch.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>string</td>
    <td>Goose Nest ID</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Human-readable description of goose nest location</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>number</td>
    <td>Latitude of goose nest location</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>number</td>
    <td>Longitude of goose nest location</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>string</td>
    <td>ISO 8601 time-stamp of last update</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":482,
    "timestamp":1396972619,
    "status":200,
    "message":"Request successful",
    "method_id":1671,
    "method":{
      "term_min":1141,
      "term_max":1141,
      "term_displaying":1141
    }
  },
  "data":[
    {
      "id":0,
      "location":"On top of CIF entrance",
      "latitude":43.475531375,
      "longitude":-80.5482428414,
      "updated":"2014-04-07T13:58:00-04:00"
    },
    {
      "id":1,
      "location":"REV Courtyard",
      "latitude":43.4697055374,
      "longitude":-80.5535603208,
      "updated":"2014-04-07T13:58:00-04:00"
    },
    {
      "id":2,
      "location":"Needles Hall roof by the main staircase",
      "latitude":43.4697707478,
      "longitude":-80.543146644,
      "updated":"2014-04-03T15:59:00-04:00"
    },
    {
      "id":3,
      "location":"Stairs next to RCH (south side between RCH and DWE) a goose has begun creating a nest.",
      "latitude":43.470051898,
      "longitude":-80.5406052517,
      "updated":"2014-04-07T13:58:00-04:00"
    },
    {
      "id":4,
      "location":"Ring Road side of PAS",
      "latitude":43.4673778167,
      "longitude":-80.5410052912,
      "updated":"2014-04-07T13:58:00-04:00"
    },
    {
      "id":5,
      "location":"In front of St.Paul's cafeteria window",
      "latitude":43.4675554604,
      "longitude":-80.5465653912,
      "updated":"2014-04-04T15:57:00-04:00"
    },
    {
      "id":6,
      "location":"Waterloo Court North Entrance",
      "latitude":43.4701785544,
      "longitude":-80.5354339524,
      "updated":"2014-04-07T13:58:00-04:00"
    },
    {
      "id":7,
      "location":"Arts Lecture Rooftop",
      "latitude":43.4689366324,
      "longitude":-80.5420160936,
      "updated":"2014-04-04T15:57:00-04:00"
    },
    {
      "id":8,
      "location":"On the side of the pond",
      "latitude":43.4656514503,
      "longitude":-80.543630783,
      "updated":"2014-04-07T13:58:00-04:00"
    },
    {
      "id":9,
      "location":"E2-E3 Courtyard outside of Lever Lab",
      "latitude":43.4711703427,
      "longitude":-80.5402366181,
      "updated":"2014-04-07T13:58:00-04:00"
    }
  ]
}
```


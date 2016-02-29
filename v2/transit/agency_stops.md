# List of GRT bus stops

```
GET /v2/transit/grt/stops.{format}
```

## Description

> This method returns list of all GRT bus stops

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
    <td>1913</td>
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
    <td>GTFS data from agency</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every day</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources



## Parameters

```
GET /v2/transit/grt/stops.{format}
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
GET /v2/transit/grt/stops.{format}
```

- **https://api.uwaterloo.ca/v2/transit/grt/stops.json**
- **https://api.uwaterloo.ca/v2/transit/grt/stops.geojson**
- **https://api.uwaterloo.ca/v2/transit/grt/stops.xml**
- **https://api.uwaterloo.ca/v2/transit/grt/stops.json?callback=myResponse**


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
    <td>Stop id</td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Stop name</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Stop description</td>
  </tr>
  <tr>
    <td><b>parent</b></td>
    <td>string</td>
    <td>Stop parent id</td>
  </tr>
  <tr>
    <td><b>zone_id</b></td>
    <td>string</td>
    <td>Stop zone id</td>
  </tr>
  <tr>
    <td><b>location_type</b></td>
    <td>string</td>
    <td>Location type (stop, etc)</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>Stop URL (if applicable)</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Stop latitude</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Stop longitude</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811672,
    "timestamp":1453160695,
    "status":200,
    "message":"Request successful",
    "method_id":1931,
    "method":{
      
    }
  },
  "data":[
    {
      "id":"1000",
      "name":"Frederick \/ King",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.449665,
      "longitude":-80.487205
    },
    {
      "id":"1001",
      "name":"Frederick \/ Irvin",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.452326,
      "longitude":-80.484192
    },
    {
      "id":"1002",
      "name":"Frederick \/ Otto",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.452995,
      "longitude":-80.482913
    },
    {
      "id":"1003",
      "name":"Frederick \/ Samuel",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.454826,
      "longitude":-80.479511
    },
    {
      "id":"1004",
      "name":"Frederick \/ Merner",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.45621,
      "longitude":-80.476903
    },
    {
      "id":"1005",
      "name":"Union \/ Dover",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.463995,
      "longitude":-80.509249
    },
    {
      "id":"1006",
      "name":"Frederick Street Mall",
      "description":null,
      "parent":null,
      "zone_id":null,
      "location_type":"stop",
      "url":null,
      "latitude":43.457923,
      "longitude":-80.473576
    }
  ]
}
```


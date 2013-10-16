# Building Details

```
GET /buildings/{building_code}.{format}
```

## Description

> This method returns the official building name, its unique number, and its lat/long coordinates given a building code.

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
    <td>1217</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>buildings</td>
    <td><b>Service ID</b></td>
    <td>257</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Institution of Analysis & Planning (IAP)</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by the steward/via github pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- This data is community curated on github.
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/Buildings/Buildings.csv


## Parameters

```
GET /buildings/{building_code}.{format}
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
GET /buildings/{building_code}.{format}
```

- **http://api.uwaterloo.ca/public/v2/buildings/MHR.json**
- **http://api.uwaterloo.ca/public/v2/buildings/MHR.xml**
- **http://api.uwaterloo.ca/public/v2/buildings/MHR.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>building_id</b></td>
    <td>integer</td>
    <td>Unique building number</td>
  </tr>
  <tr>
    <td><b>building_code</b></td>
    <td>string</td>
    <td>Official building name</td>
  </tr>
  <tr>
    <td><b>alternate_names</b></td>
    <td>array</td>
    <td>Alternate building names</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Latitude of building location</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Longitude of building location</td>
  </tr>
  <tr>
    <td><b>building_sections</b></td>
    <td>array</td>
    <td>List of building sections<br><table>
  <tr>
    <td><b>section_name</b></td>
    <td>array</td>
    <td>Name of section</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Latitude of building section location</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Longitude of building section location</td>
  </tr>
</table>
</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":121,
    "timestamp":1381957030,
    "status":200,
    "message":"Request successful",
    "method_id":2,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "building_id":23,
    "building_code":"MHR",
    "building_name":"Minota Hagey Residence",
    "alternate_names":[
      "Velocity"
    ],
    "latitude":43.46579535,
    "longitude":-80.54275113,
    "building_sections":[
      
    ],
    "building_outline":[
      
    ]
  }
}
```


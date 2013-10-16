# Buildings

```
GET /buildings/list.{format}
```

## Description

> This method returns a list of official building names, their unique number and their lat/long coordinates.

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
    <td>1213</td>
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
GET /buildings/list.{format}
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
    <td>Output format</td>
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
GET /buildings/list.{format}
```

- **https://api.uwaterloo.ca/v2/buildings/list.json**
- **https://api.uwaterloo.ca/v2/buildings/list.xml**
- **https://api.uwaterloo.ca/v2/buildings/list.json?callback=myResponse**


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
    "requests":96,
    "timestamp":1381939191,
    "status":200,
    "message":"Request successful",
    "method_id":2,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "building_id":0,
      "building_code":"AAC",
      "building_name":"Architecture Annex Cambridge",
      "alternate_names":[
        
      ],
      "latitude":43.35855,
      "longitude":-80.31684,
      "building_sections":[
        
      ]
    },
    {
      "building_id":0,
      "building_code":"AAR",
      "building_name":"Architecture Annex Rome",
      "alternate_names":[
        
      ],
      "latitude":41.889615,
      "longitude":12.470925,
      "building_sections":[
        
      ]
    },
    {
      "building_id":0,
      "building_code":"ACW",
      "building_name":"Accelerator Centre Waterloo",
      "alternate_names":[
        
      ],
      "latitude":43.47731,
      "longitude":-80.54896,
      "building_sections":[
        
      ]
    },
    {
      "building_id":44,
      "building_code":"MKV",
      "building_name":"William Lyon Mackenzie King Village",
      "alternate_names":[
        "Mackenzie King Village"
      ],
      "latitude":43.471509,
      "longitude":-80.552729,
      "building_sections":[
        {
          "section_name":"MKV East",
          "latitude":43.47132,
          "longitude":-80.551983
        },
        {
          "section_name":"MKV West",
          "latitude":43.471161,
          "longitude":-80.553056
        }
      ]
    },
    {
      "building_id":45,
      "building_code":"TC",
      "building_name":"William M. Tatham Centre for Co-operative Education & Career Action",
      "alternate_names":[
        "Tatham Centre"
      ],
      "latitude":43.469,
      "longitude":-80.541324,
      "building_sections":[
        
      ]
    }
  ]
}
```


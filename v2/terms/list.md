# Terms Listings

```
GET /terms/list.{format}
```

## Description

> This method returns the current, previous and next term's id along with a list of terms in the past year and the next year

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
    <td>1409</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>terms</td>
    <td><b>Service ID</b></td>
    <td>241</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>UW API</td>
    <td><b>Data Type</b></td>
    <td>Time computed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>On request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources



## Parameters

```
GET /terms/list.{format}
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
    <td>Valid API key</td>
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
GET /terms/list.{format}
```

- **https://api.uwaterloo.ca/v2/terms/list.json**
- **https://api.uwaterloo.ca/v2/terms/list.xml**
- **https://api.uwaterloo.ca/v2/terms/list.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>current_term</b></td>
    <td>integer</td>
    <td>Current Term's numerical value</td>
  </tr>
  <tr>
    <td><b>previous_term</b></td>
    <td>integer</td>
    <td>Previous term's numerical value</td>
  </tr>
  <tr>
    <td><b>next_term</b></td>
    <td>integer</td>
    <td>Upcoming term's numerical value</td>
  </tr>
  <tr>
    <td><b>listings</b></td>
    <td>object</td>
    <td>Term listings by year<br><table>
  <tr>
    <td><b>{year}</b></td>
    <td>list</td>
    <td>First item is previous year, second is current, last is next year<br><table>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Term's numeric ID</td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Parsed term name (human readable)</td>
  </tr>
</table>
</td>
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
    "requests":156,
    "timestamp":1383680452,
    "status":200,
    "message":"Request successful",
    "method_id":1409,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "current_term":1139,
    "previous_term":1135,
    "next_term":1141,
    "listings":{
      "2012":[
        {
          "id":1121,
          "name":"Winter 2012"
        },
        {
          "id":1125,
          "name":"Spring 2012"
        },
        {
          "id":1129,
          "name":"Fall 2012"
        }
      ],
      "2013":[
        {
          "id":1131,
          "name":"Winter 2013"
        },
        {
          "id":1135,
          "name":"Spring 2013"
        },
        {
          "id":1139,
          "name":"Fall 2013"
        }
      ],
      "2014":[
        {
          "id":1141,
          "name":"Winter 2014"
        },
        {
          "id":1145,
          "name":"Spring 2014"
        },
        {
          "id":1149,
          "name":"Fall 2014"
        }
      ]
    }
  }
}
```


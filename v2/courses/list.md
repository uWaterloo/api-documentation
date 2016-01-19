# List of all courses

```
GET /courses/list.{format}
```

## Description

> This method returns a list of all courses (currently offered, historically offered) from the opendata database

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
    <td>1471</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>courses</td>
    <td><b>Service ID</b></td>
    <td>239</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Registrar</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every term</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- This endpoint returns over 6000 courses!
- Any value can be `null`


### Sources

- http://ugradcalendar.uwaterloo.ca/
- http://gradcalendar.uwaterloo.ca/


## Parameters

```
GET /courses/list.{format}
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
GET /courses/list.{format}
```

- **https://api.uwaterloo.ca/v2/courses/list.json**
- **https://api.uwaterloo.ca/v2/courses/list.xml**
- **https://api.uwaterloo.ca/v2/courses/list.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>class_number</b></td>
    <td>integer</td>
    <td>Associated term specific class enrollment number</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>string</td>
    <td>Registrar assigned class number</td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>string</td>
    <td>Requested subject acronym</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Class name and title</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":796875,
    "timestamp":1452281864,
    "status":204,
    "message":"No data returned",
    "method_id":1439,
    "method":{
      
    }
  },
  "data":[
    {
      "course_id": "011672",
      "subject": "ACC",
      "catalog_number": "604",
      "title": "Statutory Interpretation"
    },
    {
      "course_id": "011673",
      "subject": "ACC",
      "catalog_number": "605",
      "title": "International Tax"
    },
    {
      "course_id": "011674",
      "subject": "ACC",
      "catalog_number": "606",
      "title": "Business Valuations"
    },
    {
      "course_id": "011675",
      "subject": "ACC",
      "catalog_number": "607",
      "title": "Tax Issues Integration"
    }
  ]
}
```


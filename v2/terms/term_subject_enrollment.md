# Course enrollment by subject term

```
GET /terms/{term}/{subject}/enrollment.{format}
```

## Description

> This method returns enrollment numbers for all courses in a subject for a single term

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
    <td>1873</td>
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
    <td>Registrar</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every hour</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- http://ugradcalendar.uwaterloo.ca/
- http://gradcalendar.uwaterloo.ca/


## Parameters

```
GET /terms/{term}/{subject}/enrollment.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>term</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Four digit term representation</td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid uWaterloo subject name</td>
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
GET /terms/{term}/{subject}/enrollment.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1159/ITAL/enrollment.json**
- **https://api.uwaterloo.ca/v2/terms/1159/ITAL/enrollment.xml**
- **https://api.uwaterloo.ca/v2/terms/1159/ITAL/enrollment.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>string</td>
    <td>Requested subject acronym</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>string</td>
    <td>Registrar assigned class number</td>
  </tr>
  <tr>
    <td><b>class_number</b></td>
    <td>integer</td>
    <td>Associated term specific class enrollment number</td>
  </tr>
  <tr>
    <td><b>section</b></td>
    <td>string</td>
    <td>Class instruction and number</td>
  </tr>
  <tr>
    <td><b>enrollment_capacity</b></td>
    <td>integer</td>
    <td>Class enrollment capacity</td>
  </tr>
  <tr>
    <td><b>enrollment_total</b></td>
    <td>integer</td>
    <td>Total current class enrollment</td>
  </tr>
  <tr>
    <td><b>waiting_capacity</b></td>
    <td>integer</td>
    <td>Class waiting capacity</td>
  </tr>
  <tr>
    <td><b>waiting_total</b></td>
    <td>string</td>
    <td>Total current waiting students</td>
  </tr>
  <tr>
    <td><b>last_updated</b></td>
    <td>string</td>
    <td>ISO8601 timestamp of when the data was last updated</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":723422,
    "timestamp":1447986463,
    "status":200,
    "message":"Request successful",
    "method_id":1873,
    "method":{
      
    }
  },
  "data":[
    {
      "subject":"ITAL",
      "catalog_number":"101",
      "class_number":7542,
      "section":"LAB 101",
      "enrollment_capacity":22,
      "enrollment_total":21,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"101",
      "class_number":7543,
      "section":"LAB 102",
      "enrollment_capacity":23,
      "enrollment_total":11,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"101",
      "class_number":7548,
      "section":"LAB 103",
      "enrollment_capacity":23,
      "enrollment_total":18,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"101",
      "class_number":7549,
      "section":"LAB 104",
      "enrollment_capacity":22,
      "enrollment_total":24,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"101",
      "class_number":7540,
      "section":"LEC 001",
      "enrollment_capacity":45,
      "enrollment_total":30,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"101",
      "class_number":7541,
      "section":"LEC 002",
      "enrollment_capacity":45,
      "enrollment_total":44,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"101W",
      "class_number":8727,
      "section":"LEC 002",
      "enrollment_capacity":999,
      "enrollment_total":1,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"155",
      "class_number":7555,
      "section":"LEC 001",
      "enrollment_capacity":20,
      "enrollment_total":12,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ITAL",
      "catalog_number":"155",
      "class_number":7555,
      "section":"LEC 001",
      "enrollment_capacity":20,
      "enrollment_total":12,
      "waiting_capacity":0,
      "waiting_total":0
    }
  ]
}
```


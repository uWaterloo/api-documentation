# Course enrollment by term

```
GET /terms/{term}/enrollment.{format}
```

## Description

> This method returns enrollment numbers for all classes in a term

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
    <td>1871</td>
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
GET /terms/{term}/enrollment.{format}
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
GET /terms/{term}/enrollment.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1159/enrollment.json**
- **https://api.uwaterloo.ca/v2/terms/1159/enrollment.xml**
- **https://api.uwaterloo.ca/v2/terms/1159/enrollment.json?callback=myResponse**


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

*The sample response has been trimmed and the endpoint will return data for an entire term.*

```json
{
  "meta":{
    "requests":723413,
    "timestamp":1447986011,
    "status":200,
    "message":"Request successful",
    "method_id":1871,
    "method":{

    }
  },
  "data":[
    {
      "subject":"ACC",
      "catalog_number":"770",
      "class_number":3901,
      "section":"LEC 001",
      "enrollment_capacity":8,
      "enrollment_total":0,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ACC",
      "catalog_number":"772",
      "class_number":3902,
      "section":"LEC 001",
      "enrollment_capacity":8,
      "enrollment_total":1,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ACC",
      "catalog_number":"781",
      "class_number":3903,
      "section":"SEM 001",
      "enrollment_capacity":5,
      "enrollment_total":4,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ACINTY",
      "catalog_number":"600",
      "class_number":2921,
      "section":"OLN 081",
      "enrollment_capacity":9999,
      "enrollment_total":219,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ACINTY",
      "catalog_number":"600",
      "class_number":2922,
      "section":"OLN 082",
      "enrollment_capacity":9999,
      "enrollment_total":22,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ACINTY",
      "catalog_number":"610",
      "class_number":2967,
      "section":"OLN 081",
      "enrollment_capacity":9999,
      "enrollment_total":275,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"ACINTY",
      "catalog_number":"610",
      "class_number":2968,
      "section":"OLN 082",
      "enrollment_capacity":9999,
      "enrollment_total":42,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"WS",
      "catalog_number":"325",
      "class_number":4354,
      "section":"LEC 001",
      "enrollment_capacity":5,
      "enrollment_total":4,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"WS",
      "catalog_number":"334",
      "class_number":7896,
      "section":"LEC 001",
      "enrollment_capacity":15,
      "enrollment_total":6,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"WS",
      "catalog_number":"475",
      "class_number":7898,
      "section":"RDG 001",
      "enrollment_capacity":1,
      "enrollment_total":0,
      "waiting_capacity":0,
      "waiting_total":0
    },
    {
      "subject":"WS",
      "catalog_number":"499A",
      "class_number":3886,
      "section":"RDG 001",
      "enrollment_capacity":1,
      "enrollment_total":2,
      "waiting_capacity":0,
      "waiting_total":0
    }
  ]
}
```


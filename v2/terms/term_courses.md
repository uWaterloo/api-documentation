# Course listings by term

```
GET /terms/{term_id}/courses.{format}
```

## Description

> This method returns a list of all courses offered for the given term from the opendata database

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
    <td>1511</td>
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
    <td>Every term</td>
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
GET /terms/{term_id}/courses.{format}
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
GET /terms/{term_id}/courses.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1161/courses.json**
- **https://api.uwaterloo.ca/v2/terms/1161/courses.xml**
- **https://api.uwaterloo.ca/v2/terms/1161/courses.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>units</b></td>
    <td>float</td>
    <td>Course credits/units</td>
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
    "requests":796933,
    "timestamp":1452284471,
    "status":200,
    "message":"Request successful",
    "method_id":1511,
    "method":{
      
    }
  },
  "data":[
    {
      "subject":"ACC",
      "catalog_number":"607",
      "units":0.5,
      "title":"Tax Issues Integration"
    },
    {
      "subject":"ACC",
      "catalog_number":"611",
      "units":0.5,
      "title":"External Reporting"
    },
    {
      "subject":"ACC",
      "catalog_number":"621",
      "units":0.5,
      "title":"System Reliability Principles and Criteria"
    },
    {
      "subject":"ACC",
      "catalog_number":"622",
      "units":0.5,
      "title":"Electronic Commerce"
    },
    {
      "subject":"ACC",
      "catalog_number":"650",
      "units":0.5,
      "title":"Assurance and Governance"
    },
    {
      "subject":"ACC",
      "catalog_number":"652",
      "units":0.5,
      "title":"Forensic Accounting"
    },
    {
      "subject":"ACC",
      "catalog_number":"680",
      "units":0.5,
      "title":"Performance Measurement and Control systems for Implementing Strategy"
    },
    {
      "subject":"ACC",
      "catalog_number":"685",
      "units":0.5,
      "title":"Performance Management"
    },
    {
      "subject":"ACC",
      "catalog_number":"690",
      "units":0.5,
      "title":"Topics in Accounting"
    },
    {
      "subject":"ACC",
      "catalog_number":"701",
      "units":0.5,
      "title":"Financial Accounting Research Seminar"
    },
    {
      "subject":"ACC",
      "catalog_number":"750",
      "units":0.5,
      "title":"Auditing Research Seminar"
    },
    {
      "subject":"ACC",
      "catalog_number":"760",
      "units":0.5,
      "title":"Taxation Research Seminar"
    },
    {
      "subject":"ACC",
      "catalog_number":"784",
      "units":0.5,
      "title":"Selected Topics in Research Methodology"
    },
    {
      "subject":"ACINTY",
      "catalog_number":"600",
      "units":0,
      "title":"Academic Integrity Module"
    }
  ]
}
```


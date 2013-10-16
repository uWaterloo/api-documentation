# Course Prerequisites

```
GET /courses/{subject}/{catalog_number}/prerequisites.{format}
```

## Description

> This method returns parsed and raw representation of prerequsites for a given course

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
    <td>1181</td>
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
    <td>Every request (live)</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Please see the following blog post on how to interpret the data. <br>http://hxhl95.github.io/course-prerequisites-string-parser/
- Any value can be `null`


### Sources

- http://ugradcalendar.uwaterloo.ca/
- http://gradcalendar.uwaterloo.ca/


## Parameters

```
GET /courses/{subject}/{catalog_number}/prerequisites.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid uWaterloo subject name</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid uWaterloo course number</td>
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
GET /courses/{subject}/{catalog_number}/prerequisites.{format}
```

- **https://api.uwaterloo.ca/v2/courses/PHYS/375/prerequisites.json**
- **https://api.uwaterloo.ca/v2/courses/CS/486/prerequisites.xml**
- **https://api.uwaterloo.ca/v2/courses/PHYS/375/prerequisites.json?callback=myResponse**


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
    <td><b>title</b></td>
    <td>string</td>
    <td>Class name and title</td>
  </tr>
  <tr>
    <td><b>prerequisites</b></td>
    <td>number</td>
    <td>Raw listing of course prerequisites</td>
  </tr>
  <tr>
    <td><b>prerequisites_parsed</b></td>
    <td>list</td>
    <td>Parsed prerequisites</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":117,
    "timestamp":1381955389,
    "status":200,
    "message":"Request successful",
    "method_id":1181,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "subject":"PHYS",
    "catalog_number":"375",
    "title":"Stars",
    "prerequisites":"Prereq: PHYS 112 or 122 and two of PHYS 234, 241, 242, 256, 258\/358, 263, 275",
    "prerequisites_parsed":[
      [
        1,
        "PHYS112",
        "PHYS122"
      ],
      [
        2,
        "PHYS234",
        "PHYS241",
        "PHYS242",
        "PHYS256",
        [
          1,
          "PHYS258",
          "PHYS358"
        ],
        "PHYS263",
        "PHYS275"
      ]
    ]
  }
}
```


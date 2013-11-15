# Course Information

```
GET /courses/{subject}/{catalog_number}.{format}
```

## Description

> This method returns all available information for a given course

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
    <td>1447</td>
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
    <td>Scraped/API DB</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every request (live)</td>
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
GET /courses/{subject}/{catalog_number}.{format}
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
GET /courses/{subject}/{catalog_number}.{format}
```

- **https://api.uwaterloo.ca/v2/courses/PHYS/234.json**
- **https://api.uwaterloo.ca/v2/courses/PHYS/234.xml**
- **https://api.uwaterloo.ca/v2/courses/CS/486.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>course_id</b></td>
    <td>string</td>
    <td>Registrar assigned course ID</td>
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
    <td><b>units</b></td>
    <td>number</td>
    <td>Credit count for the mentioned course</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Brief course description</td>
  </tr>
  <tr>
    <td><b>instructions</b></td>
    <td>list</td>
    <td>Instruction types for the course (LEC, TUT, LAB etc)</td>
  </tr>
  <tr>
    <td><b>prerequisites</b></td>
    <td>string</td>
    <td>Prerequisite listing for the course</td>
  </tr>
  <tr>
    <td><b>antirequisites</b></td>
    <td>string</td>
    <td>Antirequisite listing for the course</td>
  </tr>
  <tr>
    <td><b>corequisites</b></td>
    <td>string</td>
    <td>Corequisite listing for the course</td>
  </tr>
  <tr>
    <td><b>crosslistings</b></td>
    <td>string</td>
    <td>Crosslisted courses</td>
  </tr>
  <tr>
    <td><b>terms_offered</b></td>
    <td>list</td>
    <td>List of terms that the course is offered</td>
  </tr>
  <tr>
    <td><b>notes</b></td>
    <td>string</td>
    <td>Additional notes on the course</td>
  </tr>
  <tr>
    <td><b>offerings</b></td>
    <td>object</td>
    <td>Brief course description<br><table>
  <tr>
    <td><b>online</b></td>
    <td>boolean</td>
    <td>Is the course offered online</td>
  </tr>
  <tr>
    <td><b>online_only</b></td>
    <td>boolean</td>
    <td>Is the course only offered online</td>
  </tr>
  <tr>
    <td><b>st_jerome</b></td>
    <td>boolean</td>
    <td>Is the course offered at St. Jerome's</td>
  </tr>
  <tr>
    <td><b>st_jerome_only</b></td>
    <td>boolean</td>
    <td>Is the course only offered at St. Jerome's</td>
  </tr>
  <tr>
    <td><b>renison</b></td>
    <td>boolean</td>
    <td>Is the course offered at Renison</td>
  </tr>
  <tr>
    <td><b>renison_only</b></td>
    <td>boolean</td>
    <td>Is the course only offered at Renison</td>
  </tr>
  <tr>
    <td><b>conrad_grebel</b></td>
    <td>boolean</td>
    <td>Is the course offered at Conrad Grebel</td>
  </tr>
  <tr>
    <td><b>conrad_grebel_only</b></td>
    <td>boolean</td>
    <td>Is the course only offered at Conrad Grebel</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>needs_department_consent</b></td>
    <td>boolean</td>
    <td>Does enrollment require the department's permission</td>
  </tr>
  <tr>
    <td><b>needs_instructor_consent</b></td>
    <td>boolean</td>
    <td>Does enrollment require instructor's consent</td>
  </tr>
  <tr>
    <td><b>extra</b></td>
    <td>list</td>
    <td>Any additional information associated with the course</td>
  </tr>
  <tr>
    <td><b>calendar_year</b></td>
    <td>string</td>
    <td>Last active year the course was offered</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>Course URL on the course calendar</td>
  </tr>
  <tr>
    <td><b>academic_level</b></td>
    <td>string</td>
    <td>Undergraduate or graduate course classification</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":319,
    "timestamp":1384542748,
    "status":200,
    "message":"Request successful",
    "method_id":1447,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "course_id":"007407",
    "subject":"PHYS",
    "catalog_number":"234",
    "title":"Quantum Physics 1",
    "units":0.5,
    "description":"Background of quantum physics. Quantization, waves and particles. The uncertainty principle. The Schroedinger equation for one-dimensional problems: bound states in square wells. Harmonic oscillator; transmission through barriers.",
    "instructions":[
      "LEC",
      "TUT"
    ],
    "prerequisites":"PHYS 112 or 122; MATH 114 or 136; MATH 128 or 138 or 148; One of MATH 228, AMATH 250, AMATH 251.",
    "antirequisites":"CHEM 256\/356, NE 232",
    "corequisites":"MATH 228 or AMATH 250.",
    "crosslistings":null,
    "terms_offered":[
      "W",
      "S"
    ],
    "notes":"[Note: PHYS 236 or knowledge of computational methods recommended. Offered: W, S]",
    "offerings":{
      "online":false,
      "online_only":false,
      "st_jerome":false,
      "st_jerome_only":false,
      "renison":false,
      "renison_only":false,
      "conrad_grebel":false,
      "conrad_grebel_only":false
    },
    "needs_department_consent":false,
    "needs_instructor_consent":false,
    "extra":[
      
    ],
    "calendar_year":"1415",
    "url":"http:\/\/www.ucalendar.uwaterloo.ca\/1415\/COURSE\/course-PHYS.html#PHYS234",
    "academic_level":"undergraduate"
  }
}
```


# Employer Info Sessions by Term

```
GET /terms/{term}/infosessions.{format}
```

## Description

> This method returns the schedule for employer information sessions of a given term

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
    <td>1489</td>
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
    <td>CECA</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>???</td>
    <td><b>Cache Time</b></td>
    <td>???</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- http://www.ceca.uwaterloo.ca/students/sessions.php


## Parameters

```
GET /terms/{term}/infosessions.{format}
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
GET /terms/{term}/infosessions.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.json*
- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.xml**
- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Information session id</td>
  </tr>
  <tr>
    <td><b>employer</b></td>
    <td>string</td>
    <td>Name of employer hosting session</td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>string</td>
    <td>Date of session</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>Start time of session</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>End time of session</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Location of session</td>
  </tr>
  <tr>
    <td><b>website</b></td>
    <td>string</td>
    <td>Employer's website</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>string</td>
    <td>Employer's target audience for the session</td>
  </tr>
  <tr>
    <td><b>programs</b></td>
    <td>string</td>
    <td>Programs relevant to employer</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Description of employer</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":1567,
    "timestamp":1396574182,
    "status":200,
    "message":"Request successful",
    "method_id":1489,
    "method":{
      
    }
  },
  "data":[
    {
      "id":"2174",
      "employer":"Actv8 Marketing",
      "date":"January 7, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ALL - Business",
      "description":""
    },
    {
      "id":"2247",
      "employer":"Mozilla",
      "date":"January 7, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"careers.mozilla.org\/",
      "audience":"Co-op Students",
      "programs":"ENG - Software, MATH - Information Technology Management, MATH - Computer Science",
      "description":""
    },
    {
      "id":"2255",
      "employer":"Facebook",
      "date":"January 7, 2014",
      "start_time":"2:00 PM",
      "end_time":"4:00 PM",
      "location":"TC 2218",
      "website":"facebook.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2219",
      "employer":"Audatex Canada",
      "date":"January 7, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"MATH - Information Technology Management, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2307",
      "employer":"Amazon",
      "date":"January 7, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH - Festival Room",
      "website":"www.amazon.com\/college",
      "audience":"Co-op Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2248",
      "employer":"Enflick",
      "date":"January 8, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - MATH faculty, ENG - System Design, ENG - Architecture, ALL - ENG faculty, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical",
      "description":""
    },
    {
      "id":"2218",
      "employer":"Facebook",
      "date":"January 8, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"FACEBOOK.COM",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Computer, ENG - Electrical, ENG - Mechatronics, ENG - Software, ENG - System Design",
      "description":""
    },
    {
      "id":"2168",
      "employer":"Deloitte",
      "date":"January 8, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH - Festival Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Math & Business, MATH - Information Technology Management, MATH - Bioinformatics, ALL - MATH faculty, ENG - System Design, ENG - Software, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ALL - ENG faculty,  ALL - Info Tech",
      "description":""
    },
    {
      "id":"2216",
      "employer":"CPP Investment Board",
      "date":"January 9, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"CPPIB.COM",
      "audience":"Co-op Students",
      "programs":"SCI - Science & Business, MATH - Statistics, MATH - Pure Mathematics, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Math & Business, MATH - Financial Analysis & Risk Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Computational Mathematics, MATH - Combinatorics & Optimization, MATH - Business Administration, ALL - MATH faculty, MATH - Actuarial Science, ENG - System Design, ENG - Management, ENG - Computer, CA - Chartered Accounting, ARTS - Financial Management, ARTS - Economics, ARTS - Arts & Business,  ALL - Info Tech,  ALL - Business",
      "description":""
    }
  ]
}
```

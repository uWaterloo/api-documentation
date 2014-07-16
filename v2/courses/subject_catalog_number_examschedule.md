# Exam Schedule

```
GET /courses/{subject}/{catalog_number}/examschedule.{format}
```

## Description

> This method returns a given course's exam schedule

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
    <td>1367</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>cpirses</td>
    <td><b>Service ID</b></td>
    <td>239</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Registrar's Office</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Once a day</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- The CSV file on github is generated through the registrar's office
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/ExamSchedule/


## Parameters

```
GET /courses/{subject}/{catalog_number}/examschedule.{format}
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
    <td><b>term</b></td>
    <td>filter</td>
    <td><i>no</i></td>
    <td>Four digit term representation</td>
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
GET /courses/{subject}/{catalog_number}/examschedule.{format}
```

- **https://api.uwaterloo.ca/v2/courses/CS/486/examschedule.json**
- **https://api.uwaterloo.ca/v2/courses/CS/486/examschedule.xml**
- **https://api.uwaterloo.ca/v2/courses/CS/486/examschedule.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>course</b></td>
    <td>string</td>
    <td>Full course name (subject and catalog number)</td>
  </tr>
  <tr>
    <td><b>sections</b></td>
    <td>list</td>
    <td>Exam schedule for all sections of the course<br><table>
  <tr>
    <td><b>section</b></td>
    <td>string</td>
    <td>Exam section number</td>
  </tr>
  <tr>
    <td><b>day</b></td>
    <td>string</td>
    <td>Day of the exam</td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>string</td>
    <td>ISO8601 exam date representation</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>Exam starting time</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>Exam ending time</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Exam location</td>
  </tr>
  <tr>
    <td><b>notes</b></td>
    <td>string</td>
    <td>Additional notes regarding the section</td>
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
    "requests":150,
    "timestamp":1382376814,
    "status":200,
    "message":"Request successful",
    "method_id":1367,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "course":"CS 486",
    "sections":[
      {
        "section":"001",
        "day":"Tuesday",
        "date":"2013-12-10",
        "start_time":"7:30 PM",
        "end_time":"10:00 PM",
        "location":"MC 2017,2054",
        "notes":""
      }
    ]
  }
}
```


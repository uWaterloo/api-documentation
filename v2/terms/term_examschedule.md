# Exam Schedule

```
GET /terms/{term}/examschedule.{format}
```

## Description

> This method returns a given term's exam schedule

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
    <td>1187</td>
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

- https://github.com/uWaterloo/Datasets/tree/master/ExamSchedule


## Parameters

```
GET /terms/{term}/examschedule.{format}
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
    <td>Numeric representation of the term</td>
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
GET /terms/{term}/examschedule.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1139/examschedule.json**
- **https://api.uwaterloo.ca/v2/terms/1139/examschedule.xml**
- **https://api.uwaterloo.ca/v2/terms/1139/examschedule.json?callback=myResponse**


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
    "requests":149,
    "timestamp":1382375438,
    "status":200,
    "message":"Request successful",
    "method_id":1187,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "course":"ACTSC 221",
      "sections":[
        {
          "section":"001",
          "day":"Thursday",
          "date":"2013-12-19",
          "start_time":"12:30 PM",
          "end_time":"3:00 PM",
          "location":"PAC 1",
          "notes":""
        }
      ]
    },
    {
      "course":"ACTSC 231",
      "sections":[
        {
          "section":"001",
          "day":"Thursday",
          "date":"2013-12-19",
          "start_time":"9:00 AM",
          "end_time":"11:30 AM",
          "location":"PAC 4,5,6",
          "notes":""
        }
      ]
    },
    {
      "course":"ACTSC 232",
      "sections":[
        {
          "section":"001",
          "day":"Thursday",
          "date":"2013-12-05",
          "start_time":"9:00 AM",
          "end_time":"11:30 AM",
          "location":"MC 4059,4060,4061",
          "notes":""
        }
      ]
    },
    {
      "course":"ACTSC 331",
      "sections":[
        {
          "section":"001",
          "day":"Friday",
          "date":"2013-12-06",
          "start_time":"12:30 PM",
          "end_time":"3:00 PM",
          "location":"PAC 8",
          "notes":""
        }
      ]
    },
    {
      "course":"ACTSC 371",
      "sections":[
        {
          "section":"001",
          "day":"Friday",
          "date":"2013-12-13",
          "start_time":"9:00 AM",
          "end_time":"11:30 AM",
          "location":"M3 1006,MC 1056",
          "notes":""
        }
      ]
    },
    {
      "course":"ACTSC 372",
      "sections":[
        {
          "section":"001",
          "day":"Tuesday",
          "date":"2013-12-10",
          "start_time":"12:30 PM",
          "end_time":"3:00 PM",
          "location":"PAC 1,2",
          "notes":""
        }
      ]
    },
    {
      "course":"ACTSC 431",
      "sections":[
        {
          "section":"001",
          "day":"Wednesday",
          "date":"2013-12-11",
          "start_time":"4:00 PM",
          "end_time":"6:30 PM",
          "location":"MC 2034,2035,2038",
          "notes":""
        }
      ]
    }
}
```


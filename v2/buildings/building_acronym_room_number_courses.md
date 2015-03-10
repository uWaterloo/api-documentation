# Courses in a Classroom

```
GET /buildings/{building}/{room}/courses.{format}
```

## Description

> This method gives out the all the courses offered in a given classroom.

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
    <td>1223</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>buildings</td>
    <td><b>Service ID</b></td>
    <td>257</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>University Registrar</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every hour on weekdays</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- Information regarding description of parameters is available here: https://uwaterloo.ca/quest/undergraduate-students/schedule-of-classes-definitions
- Any value can be `null`


### Sources

- http://www.adm.uwaterloo.ca/infocour/CIR/SA/under.html


## Parameters

```
GET /buildings/{building}/{room}/courses.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>building</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Building code</td>
  </tr>
  <tr>
    <td><b>room</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Room number</td>
  </tr>
  <tr>
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Output format</td>
  </tr>
  <tr>
    <td><b>key</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Your API key</td>
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
GET /buildings/{building}/{room}/courses.{format}
```

- **https://api.uwaterloo.ca/v2/buildings/MC/2038/courses.json**
- **https://api.uwaterloo.ca/v2/buildings/MC/2038/courses.xml**
- **https://api.uwaterloo.ca/v2/buildings/MC/2038/courses.json?callback=myResponse**


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
    <td>Class Number</td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>string</td>
    <td>Course subject code</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>string</td>
    <td>Catalog number</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Course title</td>
  </tr>
  <tr>
    <td><b>section</b></td>
    <td>string</td>
    <td>Course section number</td>
  </tr>
  <tr>
    <td><b>weekdays</b></td>
    <td>string</td>
    <td>Course class days</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>Start time</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>End time</td>
  </tr>
  <tr>
    <td><b>start_date</b></td>
    <td>string</td>
    <td>Start date</td>
  </tr>
  <tr>
    <td><b>end_date</b></td>
    <td>string</td>
    <td>End date</td>
  </tr>
  <tr>
    <td><b>enrollment_total</b></td>
    <td>integer</td>
    <td>Number of students currently enrolled in the section</td>
  </tr>
  <tr>
    <td><b>instructors</b></td>
    <td>array</td>
    <td>List of instructors the individual meet</td>
  </tr>
  <tr>
    <td><b>building</b></td>
    <td>string</td>
    <td>Building code of building where the individual meet is held</td>
  </tr>
  <tr>
    <td><b>room</b></td>
    <td>string</td>
    <td>Room where the individual meet is held</td>
  </tr>
  <tr>
    <td><b>term</b></td>
    <td>integer</td>
    <td>Particular 4-month period within which sessions are defined</td>
  </tr>
  <tr>
    <td><b>last_updated</b></td>
    <td>string</td>
    <td>Server time at last update (in ISO 8601 format)</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":122,
    "timestamp":1381957387,
    "status":200,
    "message":"Request successful",
    "method_id":1223,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "class_number":6554,
      "subject":"BIOL",
      "catalog_number":"309",
      "title":"Analytical Methods in Molecular Biology",
      "section":"TUT 103",
      "weekdays":"Th",
      "start_time":"17:30",
      "end_time":"18:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":62,
      "instructors":[
        "Moffatt,Barbara A"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:18-04:00"
    },
    {
      "class_number":5282,
      "subject":"CO",
      "catalog_number":"342",
      "title":"Introduction to Graph Theory",
      "section":"LEC 001",
      "weekdays":"MWF",
      "start_time":"11:30",
      "end_time":"12:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":47,
      "instructors":[
        "Godsil,Christopher D"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:38-04:00"
    },
    {
      "class_number":5825,
      "subject":"CS",
      "catalog_number":"137",
      "title":"Programming Principles",
      "section":"TUT 202",
      "weekdays":"F",
      "start_time":"15:30",
      "end_time":"16:20",
      "start_date":"09\/20",
      "end_date":"11\/29",
      "enrollment_total":75,
      "instructors":[
        "Clarke,Charles L.A"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:42-04:00"
    },
    {
      "class_number":5363,
      "subject":"CS",
      "catalog_number":"241",
      "title":"Foundations of Sequential Programs",
      "section":"LEC 001",
      "weekdays":"MWF",
      "start_time":"08:30",
      "end_time":"09:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":70,
      "instructors":[
        "Naeem,Nomair Ahmed"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:42-04:00"
    },
    {
      "class_number":5746,
      "subject":"CS",
      "catalog_number":"246",
      "title":"Object-Oriented Software Development",
      "section":"LEC 002",
      "weekdays":"TTh",
      "start_time":"10:00",
      "end_time":"11:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":80,
      "instructors":[
        "Lushman,Bradley Michael"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:42-04:00"
    },
    {
      "class_number":5799,
      "subject":"CS",
      "catalog_number":"246",
      "title":"Object-Oriented Software Development",
      "section":"LEC 003",
      "weekdays":"TTh",
      "start_time":"11:30",
      "end_time":"12:50",
      "start_date":null,
      "end_date":null,
      "enrollment_total":83,
      "instructors":[
        "Prosser,Reuben Mark"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:42-04:00"
    },
    {
      "class_number":5365,
      "subject":"CS",
      "catalog_number":"251",
      "title":"Computer Organization and Design",
      "section":"LEC 001",
      "weekdays":"MWF",
      "start_time":"14:30",
      "end_time":"15:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":80,
      "instructors":[
        "Mann,Richard"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:42-04:00"
    },
    {
      "class_number":5703,
      "subject":"CS",
      "catalog_number":"341",
      "title":"Algorithms",
      "section":"LEC 002",
      "weekdays":"TTh",
      "start_time":"13:00",
      "end_time":"14:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":90,
      "instructors":[
        "Lopez-Ortiz,Alejandro"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:42-04:00"
    },
    {
      "class_number":5748,
      "subject":"CS",
      "catalog_number":"343",
      "title":"Concurrent and Parallel Programming",
      "section":"LEC 002",
      "weekdays":"TTh",
      "start_time":"14:30",
      "end_time":"15:50",
      "start_date":null,
      "end_date":null,
      "enrollment_total":89,
      "instructors":[
        "Wong,Bernard"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:43-04:00"
    },
    {
      "class_number":5704,
      "subject":"CS",
      "catalog_number":"458",
      "title":"Computer Security and Privacy",
      "section":"LEC 001",
      "weekdays":"TTh",
      "start_time":"08:30",
      "end_time":"09:50",
      "start_date":null,
      "end_date":null,
      "enrollment_total":77,
      "instructors":[
        "Stinson,Douglas R"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:00:43-04:00"
    },
    {
      "class_number":5613,
      "subject":"MATH",
      "catalog_number":"104",
      "title":"Introductory Calculus for Arts and Social Science",
      "section":"LEC 001",
      "weekdays":"MWF",
      "start_time":"09:30",
      "end_time":"10:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":75,
      "instructors":[
        "Ali Akbari,Shahla"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:41-04:00"
    },
    {
      "class_number":5554,
      "subject":"MATH",
      "catalog_number":"106",
      "title":"Applied Linear Algebra 1",
      "section":"LEC 001",
      "weekdays":"MWF",
      "start_time":"10:30",
      "end_time":"11:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":64,
      "instructors":[
        "Zhao,Yongqiang"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:41-04:00"
    },
    {
      "class_number":5627,
      "subject":"MATH",
      "catalog_number":"136",
      "title":"Linear Algebra 1 for Honours Mathematics",
      "section":"LEC 002",
      "weekdays":"MWF",
      "start_time":"13:30",
      "end_time":"14:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":96,
      "instructors":[
        "Farczadi,Linda"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5346,
      "subject":"MATH",
      "catalog_number":"136",
      "title":"Linear Algebra 1 for Honours Mathematics",
      "section":"TUT 101",
      "weekdays":"M",
      "start_time":"15:30",
      "end_time":"16:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":111,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5792,
      "subject":"MATH",
      "catalog_number":"136",
      "title":"Linear Algebra 1 for Honours Mathematics",
      "section":"TUT 103",
      "weekdays":"M",
      "start_time":"17:30",
      "end_time":"18:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":124,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5853,
      "subject":"MATH",
      "catalog_number":"137",
      "title":"Calculus 1 for Honours Mathematics",
      "section":"TUT 103",
      "weekdays":"Th",
      "start_time":"16:30",
      "end_time":"17:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":35,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5252,
      "subject":"MATH",
      "catalog_number":"138",
      "title":"Calculus 2 For Honours Mathematics",
      "section":"TUT 101",
      "weekdays":"W",
      "start_time":"15:30",
      "end_time":"16:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":93,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5576,
      "subject":"MATH",
      "catalog_number":"138",
      "title":"Calculus 2 For Honours Mathematics",
      "section":"TUT 102",
      "weekdays":"W",
      "start_time":"16:30",
      "end_time":"17:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":94,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5794,
      "subject":"MATH",
      "catalog_number":"138",
      "title":"Calculus 2 For Honours Mathematics",
      "section":"TUT 103",
      "weekdays":"W",
      "start_time":"17:30",
      "end_time":"18:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":91,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:42-04:00"
    },
    {
      "class_number":5409,
      "subject":"MATH",
      "catalog_number":"228",
      "title":"Differential Equations for Physics and Chemistry",
      "section":"TUT 101",
      "weekdays":"M",
      "start_time":"16:30",
      "end_time":"17:20",
      "start_date":null,
      "end_date":null,
      "enrollment_total":79,
      "instructors":[
        
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:01:43-04:00"
    },
    {
      "class_number":5720,
      "subject":"CS",
      "catalog_number":"658",
      "title":"Computer Security and Privacy",
      "section":"LEC 001",
      "weekdays":"TTh",
      "start_time":"08:30",
      "end_time":"09:50",
      "start_date":null,
      "end_date":null,
      "enrollment_total":2,
      "instructors":[
        "Stinson,Douglas R"
      ],
      "building":"MC",
      "room":"2038",
      "term":1139,
      "last_updated":"2013-10-16T08:02:47-04:00"
    }
  ]
}
```


# Course Schedule

```
GET /courses/{subject}/{catalog_number}/schedule.{format}
```

## Description

> This method returns the class schedule for a given course and term

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
    <td>1171</td>
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
    <td>Every hour</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- By default, only schedules for the current term will be returned if the [`term` parameter](#parameters) is not given
- Any value can be `null`


### Sources

- http://ugradcalendar.uwaterloo.ca/
- http://gradcalendar.uwaterloo.ca/


## Parameters

```
GET /courses/{subject}/{catalog_number}/schedule.{format}
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
    <td>Valid uWaterloo coure number</td>
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
GET /courses/{subject}/{catalog_number}/schedule.{format}
```

- **https://api.uwaterloo.ca/v2/courses/CS/486/schedule.json**
- **https://api.uwaterloo.ca/v2/courses/CS/486/schedule.xml**
- **https://api.uwaterloo.ca/v2/courses/CS/486/schedule.json?callback=myResponse**


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
    <td><b>units</b></td>
    <td>number</td>
    <td>Credit count for the mentioned course</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Class name and title</td>
  </tr>
  <tr>
    <td><b>note</b></td>
    <td>string</td>
    <td>Additional notes regarding enrollment for the given term</td>
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
    <td><b>campus</b></td>
    <td>string</td>
    <td>Name of the campus the course is being offered</td>
  </tr>
  <tr>
    <td><b>associated_class</b></td>
    <td>integer</td>
    <td>Associated class id</td>
  </tr>
  <tr>
    <td><b>related_component_1</b></td>
    <td>string</td>
    <td>Name of the related course component</td>
  </tr>
  <tr>
    <td><b>related_component_2</b></td>
    <td>string</td>
    <td>Name of the second related course component</td>
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
    <td><b>topic</b></td>
    <td>string</td>
    <td>Class discussion topic</td>
  </tr>
  <tr>
    <td><b>reserves</b></td>
    <td>object</td>
    <td>Course specific enrollemnt reserveation data<br><table>
  <tr>
    <td><b>reserve_group</b></td>
    <td>string</td>
    <td>Name of the reserved group</td>
  </tr>
  <tr>
    <td><b>enrollment_capacity</b></td>
    <td>integer</td>
    <td>Total enrollment capacity of the group</td>
  </tr>
  <tr>
    <td><b>enrollment_total</b></td>
    <td>integer</td>
    <td>Total reserve enrollment</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>classes</b></td>
    <td>object</td>
    <td>Schedule data<br><table>
  <tr>
    <td><b>date</b></td>
    <td>object</td>
    <td>Date object for course schedule<br><table>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>24 hour class starting time</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>24 hour class ending time</td>
  </tr>
  <tr>
    <td><b>weekdays</b></td>
    <td>string</td>
    <td>Weekdays the course is offered</td>
  </tr>
  <tr>
    <td><b>start_date</b></td>
    <td>string</td>
    <td>Additional starting date for course</td>
  </tr>
  <tr>
    <td><b>end_date</b></td>
    <td>string</td>
    <td>Additional ending date for course</td>
  </tr>
  <tr>
    <td><b>is_tba</b></td>
    <td>boolean</td>
    <td>If the course schedule is TBA</td>
  </tr>
  <tr>
    <td><b>is_cancelled</b></td>
    <td>boolean</td>
    <td>If the course is cancelled for the term</td>
  </tr>
  <tr>
    <td><b>is_closed</b></td>
    <td>boolean</td>
    <td>If the course is closed for the term</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>object</td>
    <td>Class location details<br><table>
  <tr>
    <td><b>building</b></td>
    <td>string</td>
    <td>Name of the building</td>
  </tr>
  <tr>
    <td><b>room</b></td>
    <td>string</td>
    <td>Room number from the building</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>instructors</b></td>
    <td>list</td>
    <td>Names of instructors teaching the course</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>held_with</b></td>
    <td>list</td>
    <td>A list of classes the course is held with</td>
  </tr>
  <tr>
    <td><b>term</b></td>
    <td>integer</td>
    <td>4 digit term representation</td>
  </tr>
  <tr>
    <td><b>academic_level</b></td>
    <td>string</td>
    <td>Undergraduate or graduate course classification</td>
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
    "requests":100,
    "timestamp":1381946930,
    "status":200,
    "message":"Request successful",
    "method_id":1171,
    "version":2.07,
    "method":{
      "disclaimer":"Review the 'No Warranty' section of the University of Waterloo Open Data License before using this data. If building services upon this data, please inform your users of the inherent risks (as a best practice)",
      "license":"https:\/\/uwaterloo.ca\/open-data\/university-waterloo-open-data-license-agreement-v1"
    }
  },
  "data":[
    {
      "subject":"CS",
      "catalog_number":"486",
      "units":0.5,
      "title":"Introduction to Artificial Intelligence",
      "note":null,
      "class_number":5377,
      "section":"LEC 001",
      "campus":"UW U",
      "associated_class":1,
      "related_component_1":null,
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":77,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"16:00",
            "end_time":"17:20",
            "weekdays":"TTh",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"4045"
          },
          "instructors":[
            "Larson,Kate"
          ]
        }
      ],
      "held_with":[
        "CS 686"
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-10-16T08:00:43-04:00"
    }
  ]
}
```


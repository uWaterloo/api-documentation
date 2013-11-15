# Course Schedule by Term

```
GET /terms/{term}/{subject}/{catalog_number}/schedule.{format}
```

## Description

> This method returns the class schedule for the given course of a given term

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
    <td>1193</td>
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
GET /terms/{term}/{subject}/{catalog_number}/schedule.{format}
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
    <td><b>catalog_number</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Course name</td>
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
GET /terms/{term}/{subject}/{catalog_number}/schedule.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1139/CS/115/schedule.json**
- **https://api.uwaterloo.ca/v2/terms/1141/CS/116/schedule.xml**
- **https://api.uwaterloo.ca/v2/terms/1141/MATH/128/schedule.json?callback=myResponse**


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
    <td>Course specific enrollment reservation data<br><table>
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
    "requests":311,
    "timestamp":1384538735,
    "status":200,
    "message":"Request successful",
    "method_id":1193,
    "version":2.07,
    "method":{
      "disclaimer":"Review the 'No Warranty' section of the University of Waterloo Open Data License before using this data. If building services upon this data, please inform your users of the inherent risks (as a best practice)",
      "license":"https:\/\/uwaterloo.ca\/open-data\/university-waterloo-open-data-license-agreement-v1"
    }
  },
  "data":[
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5682,
      "section":"LEC 001",
      "campus":"UW U",
      "associated_class":1,
      "related_component_1":null,
      "related_component_2":"201",
      "enrollment_capacity":250,
      "enrollment_total":248,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        {
          "reserve_group":"Year 1 students ",
          "enrollment_capacity":239,
          "enrollment_total":241
        }
      ],
      "classes":[
        {
          "dates":{
            "start_time":"12:30",
            "end_time":"13:50",
            "weekdays":"MW",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"OPT",
            "room":"347"
          },
          "instructors":[
            "Vasiga,Troy Michael John"
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5683,
      "section":"LEC 002",
      "campus":"UW U",
      "associated_class":2,
      "related_component_1":null,
      "related_component_2":"201",
      "enrollment_capacity":350,
      "enrollment_total":344,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        {
          "reserve_group":"Yr 1 Honours Geomatics ",
          "enrollment_capacity":47,
          "enrollment_total":37
        },
        {
          "reserve_group":"Year 1 students ",
          "enrollment_capacity":263,
          "enrollment_total":266
        }
      ],
      "classes":[
        {
          "dates":{
            "start_time":"14:30",
            "end_time":"15:50",
            "weekdays":"MW",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"RCH",
            "room":"101"
          },
          "instructors":[
            "Vasiga,Troy Michael John"
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5684,
      "section":"LEC 003",
      "campus":"STJ J",
      "associated_class":3,
      "related_component_1":"112",
      "related_component_2":"202",
      "enrollment_capacity":50,
      "enrollment_total":56,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        {
          "reserve_group":"Year 1 students ",
          "enrollment_capacity":50,
          "enrollment_total":53
        }
      ],
      "classes":[
        {
          "dates":{
            "start_time":"13:00",
            "end_time":"14:20",
            "weekdays":"TTh",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"STJ",
            "room":"3014"
          },
          "instructors":[
            "Case,Lori"
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5685,
      "section":"LEC 004",
      "campus":"UW U",
      "associated_class":4,
      "related_component_1":null,
      "related_component_2":"201",
      "enrollment_capacity":40,
      "enrollment_total":38,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        {
          "reserve_group":"2A GBDA students only ",
          "enrollment_capacity":40,
          "enrollment_total":33
        }
      ],
      "classes":[
        {
          "dates":{
            "start_time":"09:00",
            "end_time":"11:50",
            "weekdays":"Th",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"ECH",
            "room":"1205"
          },
          "instructors":[
            "Harrigan,Kevin"
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5686,
      "section":"LEC 005",
      "campus":"UW U",
      "associated_class":5,
      "related_component_1":null,
      "related_component_2":"201",
      "enrollment_capacity":350,
      "enrollment_total":337,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        {
          "reserve_group":"Year 1 students ",
          "enrollment_capacity":246,
          "enrollment_total":254
        }
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
            "building":"AL",
            "room":"116"
          },
          "instructors":[
            "Case,Lori"
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5689,
      "section":"LAB 101",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":69,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"10:00",
            "end_time":"11:20",
            "weekdays":"W",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5690,
      "section":"LAB 102",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":84,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"11:30",
            "end_time":"12:50",
            "weekdays":"W",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5691,
      "section":"LAB 103",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":84,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"13:00",
            "end_time":"14:20",
            "weekdays":"W",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5692,
      "section":"LAB 104",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":84,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"14:30",
            "end_time":"15:50",
            "weekdays":"W",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5693,
      "section":"LAB 105",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":89,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"10:00",
            "end_time":"11:20",
            "weekdays":"Th",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5694,
      "section":"LAB 106",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":85,
      "enrollment_total":92,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"11:30",
            "end_time":"12:50",
            "weekdays":"Th",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5695,
      "section":"LAB 107",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":80,
      "enrollment_total":87,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"13:00",
            "end_time":"14:20",
            "weekdays":"Th",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5696,
      "section":"LAB 108",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":80,
      "enrollment_total":88,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"14:30",
            "end_time":"15:50",
            "weekdays":"Th",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5721,
      "section":"LAB 109",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":80,
      "enrollment_total":57,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"08:30",
            "end_time":"09:50",
            "weekdays":"F",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5951,
      "section":"LAB 110",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":80,
      "enrollment_total":61,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"10:00",
            "end_time":"11:20",
            "weekdays":"F",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5952,
      "section":"LAB 111",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":80,
      "enrollment_total":84,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"11:30",
            "end_time":"12:50",
            "weekdays":"F",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5991,
      "section":"LAB 112",
      "campus":"STJ U",
      "associated_class":3,
      "related_component_1":null,
      "related_component_2":null,
      "enrollment_capacity":50,
      "enrollment_total":56,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"13:00",
            "end_time":"14:20",
            "weekdays":"F",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5992,
      "section":"LAB 113",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":80,
      "enrollment_total":88,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"14:30",
            "end_time":"15:50",
            "weekdays":"F",
            "start_date":null,
            "end_date":null,
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":"MC",
            "room":"3003"
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5717,
      "section":"TST 201",
      "campus":"UW U",
      "associated_class":99,
      "related_component_1":"99",
      "related_component_2":null,
      "enrollment_capacity":990,
      "enrollment_total":967,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"19:00",
            "end_time":"20:50",
            "weekdays":"M",
            "start_date":"10\/28",
            "end_date":"10\/28",
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":null,
            "room":null
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    },
    {
      "subject":"CS",
      "catalog_number":"115",
      "units":0.5,
      "title":"Introduction to Computer Science 1",
      "note":"LEC 001 & 002 and 004 to 007 choose LAB section for Related 1. LEC 003 is auto-enrolled.",
      "class_number":5905,
      "section":"TST 202",
      "campus":"STJ J",
      "associated_class":3,
      "related_component_1":null,
      "related_component_2":null,
      "enrollment_capacity":50,
      "enrollment_total":56,
      "waiting_capacity":0,
      "waiting_total":0,
      "topic":null,
      "reserves":[
        
      ],
      "classes":[
        {
          "dates":{
            "start_time":"19:00",
            "end_time":"20:50",
            "weekdays":"M",
            "start_date":"10\/28",
            "end_date":"10\/28",
            "is_tba":false,
            "is_cancelled":false,
            "is_closed":false
          },
          "location":{
            "building":null,
            "room":null
          },
          "instructors":[
            
          ]
        }
      ],
      "held_with":[
        
      ],
      "term":1139,
      "academic_level":"undergraduate",
      "last_updated":"2013-11-15T13:00:57-05:00"
    }
  ]
}
```


# Get Events from All Sites

```
GET /events.{format}
```

## Description

> This method returns a list of the upcoming 21 University of Waterloo events as crawled from all University WCMS sites

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
    <td>1693</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>events</td>
    <td><b>Service ID</b></td>
    <td>271</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Each individual site's data steward</td>
    <td><b>Data Type</b></td>
    <td>Database</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Realtime</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- This is a 'realtime' feed. An item will be available on the api the second its up using Webhooks
- Any value can be `null`


### Sources

- Crawled from all WMCS sites listed at https://api.uwaterloo.ca/v2/resources/sites.{format}


## Parameters

```
GET /events.{format}
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
GET /events.{format}
```

- **https://api.uwaterloo.ca/v2/events.json**
- **https://api.uwaterloo.ca/v2/events.xml**
- **https://api.uwaterloo.ca/v2/events.json?callback=myResponse**


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
    <td>Unique event id</td>
  </tr>
  <tr>
    <td><b>site</b></td>
    <td>string</td>
    <td>Site slug from /resources/sites</td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Full site name as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Event title</td>
  </tr>
  <tr>
    <td><b>times</b></td>
    <td>array</td>
    <td>The event's times<br><table>
  <tr>
    <td><b>start</b></td>
    <td>date</td>
    <td>ISO 8601 formatted start date</td>
  </tr>
  <tr>
    <td><b>end</b></td>
    <td>date</td>
    <td>ISO 8601 formatted end date</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>type</b></td>
    <td>array</td>
    <td>Type of event</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>URL of event link</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>date</td>
    <td>ISO 8601 formatted updated date</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":6983,
    "timestamp":1400010395,
    "status":200,
    "message":"Request successful",
    "method_id":1693,
    "method":{
      
    }
  },
  "data":[
    {
      "id":1270,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"CUT Research Projects Workshop (CTE146)",
      "times":[
        {
          "start":"2014-05-12T17:00:00-04:00",
          "end":"2014-05-12T19:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/cut-research-projects-workshop-cte146-2",
      "updated":"2014-04-21T15:06:05-04:00"
    },
    {
      "id":917,
      "site":"biology",
      "site_name":"Department of Biology",
      "title":"PhD Thesis Defense - Nataliya Melnyk-Lamont",
      "times":[
        {
          "start":"2014-05-12T17:30:00-04:00",
          "end":"2014-05-12T17:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/biology\/events\/phd-thesis-defense-nataliya-melnyk-lamont",
      "updated":"2014-04-25T14:32:01-04:00"
    },
    {
      "id":875,
      "site":"science",
      "site_name":"Science",
      "title":"Mini Town Hall Meeting: Academic Programming",
      "times":[
        {
          "start":"2014-05-12T18:00:00-04:00",
          "end":"2014-05-12T19:00:00-04:00"
        }
      ],
      "type":[
        "Information session"
      ],
      "link":"https:\/\/uwaterloo.ca\/science\/events\/mini-town-hall-meeting-academic-programming",
      "updated":"2014-05-05T13:00:02-04:00"
    },
    {
      "id":1827,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Mini Town Hall Session | Academic Programming",
      "times":[
        {
          "start":"2014-05-12T18:00:00-04:00",
          "end":"2014-05-12T19:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/mini-town-hall-session-academic-programming",
      "updated":"2014-05-12T09:24:55-04:00"
    },
    {
      "id":1822,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Omar Fawzi: achieving the limits of the bounded\/noisy quantum-storage model",
      "times":[
        {
          "start":"2014-05-12T18:30:00-04:00",
          "end":"2014-05-12T19:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/omar-fawzi-achieving-limits-boundednoisy-quantum-storage",
      "updated":"2014-05-08T11:47:08-04:00"
    },
    {
      "id":1011,
      "site":"electrical-computer-engineering",
      "site_name":"Electrical and Computer Engineering",
      "title":"PhD defence - Ehsan Nasr Azadani",
      "times":[
        {
          "start":"2014-05-13T13:00:00-04:00",
          "end":"2014-05-13T13:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/electrical-computer-engineering\/events\/phd-defence-ehsan-nasr-azadani",
      "updated":"2014-05-08T08:53:28-04:00"
    },
    {
      "id":1271,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-13T13:30:00-04:00",
          "end":"2014-05-13T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-87",
      "updated":"2014-04-22T15:56:18-04:00"
    },
    {
      "id":1784,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Careers 601 Workshop",
      "times":[
        {
          "start":"2014-05-13T14:30:00-04:00",
          "end":"2014-05-13T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/careers-601-workshop",
      "updated":"2014-05-05T14:26:50-04:00"
    },
    {
      "id":43,
      "site":"retirees-association",
      "site_name":"Retirees Association",
      "title":"UWRA Spring Luncheon",
      "times":[
        {
          "start":"2014-05-13T15:30:00-04:00",
          "end":"2014-05-13T18:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/retirees-association\/events\/uwra-spring-luncheon",
      "updated":"2014-03-20T19:29:12-04:00"
    },
    {
      "id":1802,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Zynga Employer Information Session",
      "times":[
        {
          "start":"2014-05-13T15:30:00-04:00",
          "end":"2014-05-13T17:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/zynga-employer-information-session",
      "updated":"2014-05-07T10:12:10-04:00"
    },
    {
      "id":1310,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Documenting Teaching in a Teaching Dossier (CTE914)",
      "times":[
        {
          "start":"2014-05-13T16:00:00-04:00",
          "end":"2014-05-13T18:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/documenting-teaching-teaching-dossier-cte914-0",
      "updated":"2014-05-07T09:47:57-04:00"
    },
    {
      "id":610,
      "site":"institute-nanotechnology",
      "site_name":"Waterloo Institute for Nanotechnology",
      "title":"WIN Nano Graduate Student Seminar Series",
      "times":[
        {
          "start":"2014-05-06T16:30:00-04:00",
          "end":"2014-05-06T17:30:00-04:00"
        },
        {
          "start":"2014-05-13T16:30:00-04:00",
          "end":"2014-05-13T17:30:00-04:00"
        },
        {
          "start":"2014-05-27T16:30:00-04:00",
          "end":"2014-05-27T17:30:00-04:00"
        },
        {
          "start":"2014-06-03T16:30:00-04:00",
          "end":"2014-06-03T17:30:00-04:00"
        },
        {
          "start":"2014-06-10T16:30:00-04:00",
          "end":"2014-06-10T17:30:00-04:00"
        },
        {
          "start":"2014-06-17T16:30:00-04:00",
          "end":"2014-06-17T17:30:00-04:00"
        },
        {
          "start":"2014-06-24T16:30:00-04:00",
          "end":"2014-06-24T17:30:00-04:00"
        },
        {
          "start":"2014-07-08T16:30:00-04:00",
          "end":"2014-07-08T17:30:00-04:00"
        },
        {
          "start":"2014-07-15T16:30:00-04:00",
          "end":"2014-07-15T17:30:00-04:00"
        },
        {
          "start":"2014-07-22T16:30:00-04:00",
          "end":"2014-07-22T17:30:00-04:00"
        },
        {
          "start":"2014-07-29T16:30:00-04:00",
          "end":"2014-07-29T17:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/institute-nanotechnology\/events\/win-nano-graduate-student-seminar-series",
      "updated":"2014-05-12T15:24:27-04:00"
    },
    {
      "id":543,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"WCMS Web Form Creation [SEW101]",
      "times":[
        {
          "start":"2014-05-13T17:30:00-04:00",
          "end":"2014-05-13T19:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/wcms-web-form-creation-sew101-11",
      "updated":"2014-04-29T14:21:00-04:00"
    },
    {
      "id":1272,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-13T18:00:00-04:00",
          "end":"2014-05-13T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-88",
      "updated":"2014-04-22T15:56:46-04:00"
    },
    {
      "id":214,
      "site":"international-students",
      "site_name":"International Student Experience",
      "title":"Post-Graduation Work Permit online application workshop",
      "times":[
        {
          "start":"2014-05-13T18:30:00-04:00",
          "end":"2014-05-13T20:00:00-04:00"
        },
        {
          "start":"2014-05-27T18:30:00-04:00",
          "end":"2014-05-27T20:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/international-students\/events\/post-graduation-work-permit-online-application-workshop",
      "updated":"2014-04-24T15:46:01-04:00"
    },
    {
      "id":1803,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Uken Games Employer Information Session",
      "times":[
        {
          "start":"2014-05-13T21:00:00-04:00",
          "end":"2014-05-13T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/uken-games-employer-information-session",
      "updated":"2014-05-07T10:12:08-04:00"
    },
    {
      "id":797,
      "site":"housing",
      "site_name":"Residences",
      "title":"CLV Meet, Greet and Enjoy Tacos!",
      "times":[
        {
          "start":"2014-05-13T23:00:00-04:00",
          "end":"2014-05-14T00:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/housing\/events\/clv-meet-greet-and-enjoy-tacos",
      "updated":"2014-05-01T10:54:30-04:00"
    },
    {
      "id":1804,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Palantir Technologies Employer Information Session",
      "times":[
        {
          "start":"2014-05-13T23:30:00-04:00",
          "end":"2014-05-14T01:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/palantir-technologies-employer-information-session",
      "updated":"2014-05-07T10:12:07-04:00"
    },
    {
      "id":1741,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Campus Life Fair",
      "times":[
        {
          "start":"2014-05-14T15:00:00-04:00",
          "end":"2014-05-14T18:00:00-04:00"
        }
      ],
      "type":[
        "Information session",
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/campus-life-fair",
      "updated":"2014-04-17T15:25:20-04:00"
    },
    {
      "id":1814,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Chemical Engineering Seminar by Beno\u00eet H. Lessard",
      "times":[
        {
          "start":"2014-05-14T15:30:00-04:00",
          "end":"2014-05-14T16:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/chemical-engineering-seminar-benoit-h-lessard",
      "updated":"2014-05-07T16:01:40-04:00"
    },
    {
      "id":297,
      "site":"chemical-engineering",
      "site_name":"Chemical Engineering",
      "title":"Seminar - \u201cControlling Microstructure: From the Synthesis of Novel Smart Polymers to the Crystal Engineering of Phthalocyanines for use in Organic Electronics\u201d by Beno\u00eet H. Lessard, PhD, NSERC Banting Post Doctoral Fellow, University of Toronto",
      "times":[
        {
          "start":"2014-05-14T15:30:00-04:00",
          "end":"2014-05-14T15:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/chemical-engineering\/events\/seminar-controlling-microstructure-synthesis-novel-smart",
      "updated":"2014-05-07T10:00:38-04:00"
    },
    {
      "id":1266,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Interactive Teaching Activities (CTE165)",
      "times":[
        {
          "start":"2014-05-14T17:00:00-04:00",
          "end":"2014-05-14T18:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/interactive-teaching-activities-cte165-2",
      "updated":"2014-04-15T10:10:25-04:00"
    },
    {
      "id":1785,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Writing CVs and Cover Letters",
      "times":[
        {
          "start":"2014-05-14T17:30:00-04:00",
          "end":"2014-05-14T19:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/writing-cvs-and-cover-letters-5",
      "updated":"2014-05-05T14:26:46-04:00"
    },
    {
      "id":872,
      "site":"science",
      "site_name":"Science",
      "title":"Writing CVs and Cover Letters (Graduate Students and Postdocs only)",
      "times":[
        {
          "start":"2014-05-14T17:30:00-04:00",
          "end":"2014-05-14T19:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/science\/events\/writing-cvs-and-cover-letters-graduate-students-and-postdocs",
      "updated":"2014-05-05T11:36:31-04:00"
    },
    {
      "id":540,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"Writing for the Web [SEW016]",
      "times":[
        {
          "start":"2014-05-14T17:30:00-04:00",
          "end":"2014-05-14T19:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/writing-web-sew016-11",
      "updated":"2014-04-29T14:06:15-04:00"
    },
    {
      "id":918,
      "site":"biology",
      "site_name":"Department of Biology",
      "title":"PhD Thesis Defense - Oana Birceanu",
      "times":[
        {
          "start":"2014-05-14T17:30:00-04:00",
          "end":"2014-05-14T17:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/biology\/events\/phd-thesis-defense-oana-birceanu",
      "updated":"2014-04-25T14:24:15-04:00"
    },
    {
      "id":1273,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-14T18:00:00-04:00",
          "end":"2014-05-14T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-89",
      "updated":"2014-04-22T15:56:59-04:00"
    },
    {
      "id":1786,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"David Sprott lecture by Art Owen, Stanford University",
      "times":[
        {
          "start":"2014-05-14T20:00:00-04:00",
          "end":"2014-05-14T21:00:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/david-sprott-lecture-art-owen-stanford-university",
      "updated":"2014-05-05T12:48:51-04:00"
    },
    {
      "id":107,
      "site":"counselling-services",
      "site_name":"Counselling Services",
      "title":"Mindfulness at Waterloo....for students",
      "times":[
        {
          "start":"2014-05-14T20:30:00-04:00",
          "end":"2014-05-14T22:30:00-04:00"
        },
        {
          "start":"2014-05-21T20:30:00-04:00",
          "end":"2014-05-21T22:30:00-04:00"
        },
        {
          "start":"2014-05-28T20:30:00-04:00",
          "end":"2014-05-28T22:30:00-04:00"
        },
        {
          "start":"2014-06-04T20:30:00-04:00",
          "end":"2014-06-04T22:30:00-04:00"
        },
        {
          "start":"2014-06-11T20:30:00-04:00",
          "end":"2014-06-11T22:30:00-04:00"
        },
        {
          "start":"2014-06-18T20:30:00-04:00",
          "end":"2014-06-18T22:30:00-04:00"
        },
        {
          "start":"2014-06-25T20:30:00-04:00",
          "end":"2014-06-25T22:30:00-04:00"
        },
        {
          "start":"2014-07-02T20:30:00-04:00",
          "end":"2014-07-02T22:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/counselling-services\/events\/mindfulness-waterloofor-students",
      "updated":"2014-04-09T10:54:51-04:00"
    },
    {
      "id":206,
      "site":"partnerships-in-dementia-care",
      "site_name":"Partnerships in Dementia Care",
      "title":"Cracked: New Light on Dementia play",
      "times":[
        {
          "start":"2014-05-14T20:30:00-04:00",
          "end":"2014-05-14T20:30:00-04:00"
        }
      ],
      "type":[
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/partnerships-in-dementia-care\/events\/cracked-new-light-dementia-play-2",
      "updated":"2014-04-15T10:11:34-04:00"
    },
    {
      "id":1782,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Project Management as a Career Option",
      "times":[
        {
          "start":"2014-05-14T21:00:00-04:00",
          "end":"2014-05-14T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/project-management-career-option",
      "updated":"2014-05-05T14:26:56-04:00"
    },
    {
      "id":1805,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Bazaarvoice Employer Information Session",
      "times":[
        {
          "start":"2014-05-14T21:00:00-04:00",
          "end":"2014-05-14T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/bazaarvoice-employer-information-session",
      "updated":"2014-05-07T10:12:05-04:00"
    },
    {
      "id":1806,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Twitter Employer Information Session",
      "times":[
        {
          "start":"2014-05-14T23:30:00-04:00",
          "end":"2014-05-15T01:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/twitter-employer-information-session",
      "updated":"2014-05-07T10:12:01-04:00"
    },
    {
      "id":1013,
      "site":"electrical-computer-engineering",
      "site_name":"Electrical and Computer Engineering",
      "title":"PhD seminar - Ahmed Gad",
      "times":[
        {
          "start":"2014-05-15T14:00:00-04:00",
          "end":"2014-05-15T14:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/electrical-computer-engineering\/events\/phd-seminar-ahmed-gad",
      "updated":"2014-05-09T09:00:01-04:00"
    },
    {
      "id":1807,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"DBRS Global Technology Employer Information Session",
      "times":[
        {
          "start":"2014-05-15T15:30:00-04:00",
          "end":"2014-05-15T17:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/dbrs-global-technology-employer-information-session",
      "updated":"2014-05-07T10:11:59-04:00"
    },
    {
      "id":1783,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"General Application Further Education Workshop",
      "times":[
        {
          "start":"2014-05-15T17:30:00-04:00",
          "end":"2014-05-15T19:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/general-application-further-education-workshop",
      "updated":"2014-05-05T14:26:53-04:00"
    },
    {
      "id":1012,
      "site":"electrical-computer-engineering",
      "site_name":"Electrical and Computer Engineering",
      "title":"MASc seminar - Forhad Hasnat",
      "times":[
        {
          "start":"2014-05-15T18:00:00-04:00",
          "end":"2014-05-15T18:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/electrical-computer-engineering\/events\/masc-seminar-forhad-hasnat",
      "updated":"2014-05-09T08:57:41-04:00"
    },
    {
      "id":798,
      "site":"housing",
      "site_name":"Residences",
      "title":"Youth Ping Pong Tournament",
      "times":[
        {
          "start":"2014-05-15T21:00:00-04:00",
          "end":"2014-05-15T22:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/housing\/events\/youth-ping-pong-tournament",
      "updated":"2014-05-01T11:03:31-04:00"
    },
    {
      "id":1808,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Amazon Employer Information Session",
      "times":[
        {
          "start":"2014-05-15T21:00:00-04:00",
          "end":"2014-05-15T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/amazon-employer-information-session-1",
      "updated":"2014-05-07T10:11:56-04:00"
    },
    {
      "id":1745,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Open Source Ecology: Towards the Open Source Economy",
      "times":[
        {
          "start":"2014-05-15T22:00:00-04:00",
          "end":"2014-05-16T00:00:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/open-source-ecology-towards-open-source-economy",
      "updated":"2014-04-23T09:26:11-04:00"
    },
    {
      "id":1809,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Bloomberg Employer Information Session",
      "times":[
        {
          "start":"2014-05-15T23:30:00-04:00",
          "end":"2014-05-16T01:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/bloomberg-employer-information-session",
      "updated":"2014-05-07T10:11:53-04:00"
    },
    {
      "id":205,
      "site":"partnerships-in-dementia-care",
      "site_name":"Partnerships in Dementia Care",
      "title":"Cracked: New Light on Dementia play",
      "times":[
        {
          "start":"2014-05-16T00:00:00-04:00",
          "end":"2014-05-16T00:00:00-04:00"
        }
      ],
      "type":[
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/partnerships-in-dementia-care\/events\/cracked-new-light-dementia-play-1",
      "updated":"2014-04-16T13:41:13-04:00"
    },
    {
      "id":1274,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-16T13:30:00-04:00",
          "end":"2014-05-16T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-90",
      "updated":"2014-04-22T15:57:11-04:00"
    },
    {
      "id":1294,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Classroom Delivery Skills (CTE226)",
      "times":[
        {
          "start":"2014-05-16T13:30:00-04:00",
          "end":"2014-05-16T15:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/classroom-delivery-skills-cte226-4",
      "updated":"2014-04-30T14:06:48-04:00"
    },
    {
      "id":1810,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Facebook Employer Information Session",
      "times":[
        {
          "start":"2014-05-16T15:30:00-04:00",
          "end":"2014-05-16T17:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/facebook-employer-information-session-2",
      "updated":"2014-05-07T10:11:34-04:00"
    },
    {
      "id":48,
      "site":"aviation",
      "site_name":"Aviation",
      "title":"WWFC Information Session",
      "times":[
        {
          "start":"2014-05-17T14:00:00-04:00",
          "end":"2014-05-17T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/aviation\/events\/wwfc-information-session-13",
      "updated":"2014-04-28T14:16:04-04:00"
    },
    {
      "id":507,
      "site":"murray-alzheimer-research-and-education-program",
      "site_name":"Murray Alzheimer Research and Education Program",
      "title":"Waterloo-Bordeaux &quot;Path to a privileged partnership&quot;",
      "times":[
        {
          "start":"2014-05-20T04:00:00-04:00",
          "end":"2014-05-21T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/murray-alzheimer-research-and-education-program\/events\/waterloo-bordeaux-path-privileged-partnership",
      "updated":"2014-05-12T15:40:22-04:00"
    },
    {
      "id":545,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"WCMS for Site Managers [SEW100]",
      "times":[
        {
          "start":"2014-05-20T13:00:00-04:00",
          "end":"2014-05-20T16:00:00-04:00"
        },
        {
          "start":"2014-05-28T13:00:00-04:00",
          "end":"2014-05-28T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/wcms-site-managers-sew100-8",
      "updated":"2014-04-29T14:30:15-04:00"
    },
    {
      "id":1826,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Waterloo-Bordeaux Path to Partnership | Opening Ceremony",
      "times":[
        {
          "start":"2014-05-20T13:00:00-04:00",
          "end":"2014-05-20T13:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/waterloo-bordeaux-path-partnership-opening-ceremony",
      "updated":"2014-05-09T17:11:48-04:00"
    },
    {
      "id":1267,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Teaching Dossiers (CTE113)",
      "times":[
        {
          "start":"2014-05-20T13:30:00-04:00",
          "end":"2014-05-20T15:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/teaching-dossiers-cte113-1",
      "updated":"2014-04-15T10:23:42-04:00"
    },
    {
      "id":323,
      "site":"international",
      "site_name":"Waterloo International",
      "title":"Campus France Day",
      "times":[
        {
          "start":"2014-05-20T14:00:00-04:00",
          "end":"2014-05-20T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/international\/events\/campus-france-day",
      "updated":"2014-05-12T11:47:11-04:00"
    },
    {
      "id":1825,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"PDT Partners Employer Information Session",
      "times":[
        {
          "start":"2014-05-20T15:30:00-04:00",
          "end":"2014-05-20T17:30:00-04:00"
        }
      ],
      "type":[
        "Information session"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/pdt-partners-employer-information-session",
      "updated":"2014-05-09T14:53:28-04:00"
    },
    {
      "id":1763,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Alpha Kickoff",
      "times":[
        {
          "start":"2014-05-20T16:30:00-04:00",
          "end":"2014-05-20T17:30:00-04:00"
        }
      ],
      "type":[
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-alpha-kickoff",
      "updated":"2014-05-01T09:31:56-04:00"
    },
    {
      "id":1790,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Alpha Kickoff",
      "times":[
        {
          "start":"2014-05-20T16:30:00-04:00",
          "end":"2014-05-20T17:30:00-04:00"
        }
      ],
      "type":[
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-alpha-kickoff-0",
      "updated":"2014-05-05T13:15:28-04:00"
    },
    {
      "id":116,
      "site":"counselling-services",
      "site_name":"Counselling Services",
      "title":"Dialectical Behavioural Therapy Group",
      "times":[
        {
          "start":"2014-05-20T17:15:00-04:00",
          "end":"2014-05-20T18:30:00-04:00"
        },
        {
          "start":"2014-05-27T17:15:00-04:00",
          "end":"2014-05-27T18:30:00-04:00"
        },
        {
          "start":"2014-06-03T17:15:00-04:00",
          "end":"2014-06-03T18:30:00-04:00"
        },
        {
          "start":"2014-06-17T17:15:00-04:00",
          "end":"2014-06-17T18:30:00-04:00"
        },
        {
          "start":"2014-06-24T17:15:00-04:00",
          "end":"2014-06-24T18:30:00-04:00"
        },
        {
          "start":"2014-07-08T17:15:00-04:00",
          "end":"2014-07-08T18:30:00-04:00"
        },
        {
          "start":"2014-07-15T17:15:00-04:00",
          "end":"2014-07-15T18:30:00-04:00"
        },
        {
          "start":"2014-07-22T17:15:00-04:00",
          "end":"2014-07-22T18:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/counselling-services\/events\/dialectical-behavioural-therapy-group-0",
      "updated":"2014-04-17T09:22:25-04:00"
    },
    {
      "id":1275,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-20T18:00:00-04:00",
          "end":"2014-05-20T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-91",
      "updated":"2014-04-22T15:57:24-04:00"
    },
    {
      "id":118,
      "site":"master-peace-conflict-studies",
      "site_name":"Master of Peace and Conflict Studies",
      "title":"Bertha Von Suttner: A Life of Peace Concert and Exhibit",
      "times":[
        {
          "start":"2014-05-20T23:30:00-04:00",
          "end":"2014-05-20T23:30:00-04:00"
        }
      ],
      "type":[
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/master-peace-conflict-studies\/events\/bertha-von-suttner-life-peace-concert-and-exhibit",
      "updated":"2014-04-15T10:00:39-04:00"
    },
    {
      "id":1899,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Bertha von Suttner; A life of Peace - Concert and Exhibit",
      "times":[
        {
          "start":"2014-05-20T23:30:00-04:00",
          "end":"2014-05-20T23:30:00-04:00"
        }
      ],
      "type":[
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/bertha-von-suttner-life-peace-concert-and-exhibit",
      "updated":"2014-04-23T14:01:45-04:00"
    },
    {
      "id":1736,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"1914-2014 Concert with Violin and Piano",
      "times":[
        {
          "start":"2014-05-20T23:30:00-04:00",
          "end":"2014-05-20T23:30:00-04:00"
        }
      ],
      "type":[
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/1914-2014-concert-violin-and-piano",
      "updated":"2014-04-17T15:26:56-04:00"
    },
    {
      "id":252,
      "site":"music",
      "site_name":"Music",
      "title":"Bertha von Suttner: A life of peace concert &amp; exhibit",
      "times":[
        {
          "start":"2014-05-20T23:30:00-04:00",
          "end":"2014-05-20T23:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/music\/events\/bertha-von-suttner-life-peace-concert-exhibit",
      "updated":"2014-04-16T14:18:00-04:00"
    },
    {
      "id":68,
      "site":"science-technology-society",
      "site_name":"Science and Technology in Society",
      "title":"Science-Policy Interface: International Comparisons Workshop",
      "times":[
        {
          "start":"2014-05-21T04:00:00-04:00",
          "end":"2014-05-23T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/science-technology-society\/events\/science-policy-interface-international-comparisons-workshop",
      "updated":"2014-03-06T16:31:32-05:00"
    },
    {
      "id":1268,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Assessing Student Learning (CTE020)",
      "times":[
        {
          "start":"2014-05-21T13:30:00-04:00",
          "end":"2014-05-21T15:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/assessing-student-learning-cte020-2",
      "updated":"2014-04-15T10:25:46-04:00"
    },
    {
      "id":1276,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-21T13:30:00-04:00",
          "end":"2014-05-21T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-92",
      "updated":"2014-04-22T15:57:35-04:00"
    },
    {
      "id":999,
      "site":"environment",
      "site_name":"uWaterloo - Faculty of Environment",
      "title":"Social Innovations Within Markets Workshops",
      "times":[
        {
          "start":"2014-05-21T13:30:00-04:00",
          "end":"2014-05-21T21:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/environment\/events\/social-innovations-within-markets-workshops",
      "updated":"2014-04-17T13:12:03-04:00"
    },
    {
      "id":1295,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Effective Lesson Plans (CTE202)",
      "times":[
        {
          "start":"2014-05-21T18:00:00-04:00",
          "end":"2014-05-21T20:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/effective-lesson-plans-cte202-8",
      "updated":"2014-04-30T14:19:30-04:00"
    },
    {
      "id":118,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Find Books and More",
      "times":[
        {
          "start":"2014-05-21T18:30:00-04:00",
          "end":"2014-05-21T19:30:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/find-books-and-more-0",
      "updated":"2014-05-02T16:42:37-04:00"
    },
    {
      "id":165,
      "site":"peace-conflict-studies",
      "site_name":"Peace and Conflict Studies",
      "title":"\u201cThe Loss of History: Memory, Humanity and Peace after 1971\u201d with Yasmin Saikia",
      "times":[
        {
          "start":"2014-05-21T20:00:00-04:00",
          "end":"2014-05-21T20:00:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/peace-conflict-studies\/events\/loss-history-memory-humanity-and-peace-after-1971-yasmin",
      "updated":"2014-04-09T13:31:38-04:00"
    },
    {
      "id":1198,
      "site":"arts",
      "site_name":"Arts",
      "title":"&quot;The Loss of History: Memory, Humanity and Peace after 1971\u201d with Yasmin Saikia",
      "times":[
        {
          "start":"2014-05-21T20:00:00-04:00",
          "end":"2014-05-21T20:00:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/arts\/events\/loss-history-memory-humanity-and-peace-after-1971-yasmin",
      "updated":"2014-04-10T16:16:01-04:00"
    },
    {
      "id":470,
      "site":"history",
      "site_name":"History",
      "title":"\u201cThe Loss of History: Memory, Humanity and Peace after 1971\u201d with Yasmin Saikia",
      "times":[
        {
          "start":"2014-05-21T20:00:00-04:00",
          "end":"2014-05-21T20:00:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/history\/events\/loss-history-memory-humanity-and-peace-after-1971-yasmin",
      "updated":"2014-04-10T15:55:04-04:00"
    },
    {
      "id":1732,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"&quot;The Loss of History: Memory, Humanity and Peace after 1971&quot; with Yasmin Saikia",
      "times":[
        {
          "start":"2014-05-21T20:00:00-04:00",
          "end":"2014-05-21T21:30:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/loss-history-memory-humanity-and-peace-after-1971-yasmin",
      "updated":"2014-04-16T19:49:28-04:00"
    },
    {
      "id":1898,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"\u201cThe Loss of History: Memory, Humanity and Peace after 1971\u201d with Yasmin Saikia",
      "times":[
        {
          "start":"2014-05-21T20:00:00-04:00",
          "end":"2014-05-21T20:00:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/loss-history-memory-humanity-and-peace-after-1971-yasmin",
      "updated":"2014-04-09T13:29:20-04:00"
    },
    {
      "id":1873,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"K-W &amp; Area Alumni Event",
      "times":[
        {
          "start":"2014-05-21T21:00:00-04:00",
          "end":"2014-05-21T21:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/k-w-area-alumni-event",
      "updated":"2014-03-25T11:06:26-04:00"
    },
    {
      "id":162,
      "site":"waterloo-summit-centre",
      "site_name":"Waterloo Summit Centre for the Environment",
      "title":"Environment Lecture Series",
      "times":[
        {
          "start":"2014-05-21T23:00:00-04:00",
          "end":"2014-05-21T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/waterloo-summit-centre\/events\/environment-lecture-series-0",
      "updated":"2014-03-20T10:34:21-04:00"
    },
    {
      "id":293,
      "site":"chemical-engineering",
      "site_name":"Chemical Engineering",
      "title":"Notice of PhD Comprehensive Examination - &quot;Fabrication and Characterizaton of Smart Biommimetic Micro\/Nano-Structured Adhesives&quot; by Hamed Shahsavan",
      "times":[
        {
          "start":"2014-05-22T14:00:00-04:00",
          "end":"2014-05-22T14:00:00-04:00"
        }
      ],
      "type":[
        "Thesis defence"
      ],
      "link":"https:\/\/uwaterloo.ca\/chemical-engineering\/events\/notice-phd-comprehensive-examination-fabrication-and",
      "updated":"2014-04-16T15:29:28-04:00"
    },
    {
      "id":1821,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"WISE public lecture series: microalgae for energy production between dream and reality",
      "times":[
        {
          "start":"2014-05-22T17:30:00-04:00",
          "end":"2014-05-22T18:30:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/wise-public-lecture-series-microalgae-energy-production",
      "updated":"2014-05-08T11:30:30-04:00"
    },
    {
      "id":213,
      "site":"international-students",
      "site_name":"International Student Experience",
      "title":"English Hour",
      "times":[
        {
          "start":"2014-05-22T19:00:00-04:00",
          "end":"2014-05-22T20:00:00-04:00"
        },
        {
          "start":"2014-05-29T19:00:00-04:00",
          "end":"2014-05-29T20:00:00-04:00"
        },
        {
          "start":"2014-06-05T19:00:00-04:00",
          "end":"2014-06-05T20:00:00-04:00"
        },
        {
          "start":"2014-06-12T19:00:00-04:00",
          "end":"2014-06-12T20:00:00-04:00"
        },
        {
          "start":"2014-06-19T19:00:00-04:00",
          "end":"2014-06-19T20:00:00-04:00"
        },
        {
          "start":"2014-06-26T19:00:00-04:00",
          "end":"2014-06-26T20:00:00-04:00"
        },
        {
          "start":"2014-07-03T19:00:00-04:00",
          "end":"2014-07-03T20:00:00-04:00"
        },
        {
          "start":"2014-07-10T19:00:00-04:00",
          "end":"2014-07-10T20:00:00-04:00"
        },
        {
          "start":"2014-07-17T19:00:00-04:00",
          "end":"2014-07-17T20:00:00-04:00"
        },
        {
          "start":"2014-07-24T19:00:00-04:00",
          "end":"2014-07-24T20:00:00-04:00"
        },
        {
          "start":"2014-07-31T19:00:00-04:00",
          "end":"2014-07-31T20:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/international-students\/events\/english-hour",
      "updated":"2014-04-24T14:35:48-04:00"
    },
    {
      "id":792,
      "site":"housing",
      "site_name":"Residences",
      "title":"Bike Tune Up Night",
      "times":[
        {
          "start":"2014-05-22T21:00:00-04:00",
          "end":"2014-05-22T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/housing\/events\/bike-tune-night-1",
      "updated":"2014-04-25T09:53:42-04:00"
    },
    {
      "id":1812,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Startup Community | University of Waterloo Screening",
      "times":[
        {
          "start":"2014-05-22T22:00:00-04:00",
          "end":"2014-05-23T00:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/startup-community-university-waterloo-screening",
      "updated":"2014-05-07T18:31:23-04:00"
    },
    {
      "id":1791,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Alpha Idea Generation",
      "times":[
        {
          "start":"2014-05-22T23:30:00-04:00",
          "end":"2014-05-23T01:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-alpha-idea-generation",
      "updated":"2014-05-05T13:28:17-04:00"
    },
    {
      "id":572,
      "site":"stratford-campus",
      "site_name":"Stratford Campus",
      "title":"SocDocs 2014 Film Festival",
      "times":[
        {
          "start":"2014-05-23T04:00:00-04:00",
          "end":"2014-05-23T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/stratford-campus\/events\/socdocs-2014-film-festival",
      "updated":"2014-04-22T09:14:13-04:00"
    },
    {
      "id":791,
      "site":"housing",
      "site_name":"Residences",
      "title":"Community Breakfast",
      "times":[
        {
          "start":"2014-05-09T12:00:00-04:00",
          "end":"2014-05-09T13:00:00-04:00"
        },
        {
          "start":"2014-05-23T12:00:00-04:00",
          "end":"2014-05-23T13:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/housing\/events\/community-breakfast-3",
      "updated":"2014-05-01T10:25:32-04:00"
    },
    {
      "id":1277,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-23T18:00:00-04:00",
          "end":"2014-05-23T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-93",
      "updated":"2014-04-22T15:57:46-04:00"
    },
    {
      "id":371,
      "site":"knowledge-integration",
      "site_name":"Knowledge Integration",
      "title":"You@Waterloo Day 2014",
      "times":[
        {
          "start":"2014-05-24T04:00:00-04:00",
          "end":"2014-05-24T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/knowledge-integration\/events\/youwaterloo-day-2014",
      "updated":"2014-04-21T17:22:29-04:00"
    },
    {
      "id":1742,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"You @ Waterloo Day",
      "times":[
        {
          "start":"2014-05-24T14:00:00-04:00",
          "end":"2014-05-24T18:00:00-04:00"
        }
      ],
      "type":[
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/you-waterloo-day-0",
      "updated":"2014-04-22T09:20:51-04:00"
    },
    {
      "id":856,
      "site":"science",
      "site_name":"Science",
      "title":"You @ Waterloo Day",
      "times":[
        {
          "start":"2014-05-24T14:00:00-04:00",
          "end":"2014-05-24T18:00:00-04:00"
        }
      ],
      "type":[
        "Information session",
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/science\/events\/you-waterloo-day-0",
      "updated":"2014-04-23T10:55:55-04:00"
    },
    {
      "id":1748,
      "site":"engineering",
      "site_name":"Engineering",
      "title":"You @ Waterloo Engineering",
      "times":[
        {
          "start":"2014-05-24T14:00:00-04:00",
          "end":"2014-05-24T18:00:00-04:00"
        }
      ],
      "type":[
        "Information session",
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/you-at-waterloo",
      "updated":"2014-05-07T12:25:14-04:00"
    },
    {
      "id":1364,
      "site":"renison",
      "site_name":"Renison University College",
      "title":"You @ Waterloo Day",
      "times":[
        {
          "start":"2014-05-24T14:00:00-04:00",
          "end":"2014-05-24T20:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/renison\/events\/you-waterloo-day",
      "updated":"2014-05-07T13:12:56-04:00"
    },
    {
      "id":579,
      "site":"stratford-campus",
      "site_name":"Stratford Campus",
      "title":"You @ Waterloo Day",
      "times":[
        {
          "start":"2014-05-24T14:00:00-04:00",
          "end":"2014-05-24T18:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/stratford-campus\/events\/you-waterloo-day",
      "updated":"2014-05-09T09:59:03-04:00"
    },
    {
      "id":88,
      "site":"women-in-engineering",
      "site_name":"Women in Engineering",
      "title":"WiE Welcomes You",
      "times":[
        {
          "start":"2014-05-24T18:00:00-04:00",
          "end":"2014-05-24T18:00:00-04:00"
        }
      ],
      "type":[
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/women-in-engineering\/events\/wie-welcomes-you-0",
      "updated":"2014-05-07T16:16:35-04:00"
    },
    {
      "id":1875,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Niagara Alumni Event",
      "times":[
        {
          "start":"2014-05-24T20:00:00-04:00",
          "end":"2014-05-24T20:00:00-04:00"
        }
      ],
      "type":[
        "Reunion"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/niagara-alumni-event",
      "updated":"2014-03-25T11:13:52-04:00"
    },
    {
      "id":248,
      "site":"earth-sciences-museum",
      "site_name":"Earth Sciences Museum",
      "title":"Waterloo Wellington Children&#039;s Groundwater Festival",
      "times":[
        {
          "start":"2014-05-26T12:00:00-04:00",
          "end":"2014-05-26T18:30:00-04:00"
        },
        {
          "start":"2014-05-27T12:00:00-04:00",
          "end":"2014-05-27T18:30:00-04:00"
        },
        {
          "start":"2014-05-28T12:00:00-04:00",
          "end":"2014-05-28T18:30:00-04:00"
        },
        {
          "start":"2014-05-29T12:00:00-04:00",
          "end":"2014-05-29T18:30:00-04:00"
        },
        {
          "start":"2014-05-30T12:00:00-04:00",
          "end":"2014-05-30T18:30:00-04:00"
        }
      ],
      "type":[
        "Reception"
      ],
      "link":"https:\/\/uwaterloo.ca\/earth-sciences-museum\/groundwater-festival",
      "updated":"2014-05-12T16:51:54-04:00"
    },
    {
      "id":1278,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-05-26T13:30:00-04:00",
          "end":"2014-05-26T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-94",
      "updated":"2014-04-22T15:57:56-04:00"
    },
    {
      "id":1296,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Giving and Receiving Feedback (CTE106)",
      "times":[
        {
          "start":"2014-05-26T17:00:00-04:00",
          "end":"2014-05-26T18:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/giving-and-receiving-feedback-cte106-2",
      "updated":"2014-04-30T14:24:40-04:00"
    },
    {
      "id":1348,
      "site":"institute-for-quantum-computing",
      "site_name":"Institute for Quantum Computing",
      "title":"Xiaodong Xu: Spin and pseudospins in 2D semiconductors",
      "times":[
        {
          "start":"2014-05-26T18:30:00-04:00",
          "end":"2014-05-26T19:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/institute-for-quantum-computing\/events\/xiaodong-xu-spin-and-pseudospins-2d-semiconductors",
      "updated":"2014-04-07T16:00:27-04:00"
    },
    {
      "id":1736,
      "site":"engineering",
      "site_name":"Engineering",
      "title":"Instructional Skills Workshop",
      "times":[
        {
          "start":"2014-05-27T04:00:00-04:00",
          "end":"2014-05-30T04:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/instructional-skills-workshop-0",
      "updated":"2014-04-24T12:47:40-04:00"
    },
    {
      "id":542,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"WCMS for Content Maintainers [SEW099]",
      "times":[
        {
          "start":"2014-05-27T13:00:00-04:00",
          "end":"2014-05-28T16:00:00-04:00"
        },
        {
          "start":"2014-06-10T13:00:00-04:00",
          "end":"2014-06-11T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/wcms-content-maintainers-sew099-15",
      "updated":"2014-04-29T14:18:04-04:00"
    },
    {
      "id":546,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"Understanding Information Architecture [SEW119]",
      "times":[
        {
          "start":"2014-05-27T14:00:00-04:00",
          "end":"2014-05-27T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/understanding-information-architecture-sew119-0",
      "updated":"2014-04-29T14:33:27-04:00"
    },
    {
      "id":1369,
      "site":"institute-for-quantum-computing",
      "site_name":"Institute for Quantum Computing",
      "title":"Sahel Ashhab",
      "times":[
        {
          "start":"2014-05-27T14:30:00-04:00",
          "end":"2014-05-27T15:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/institute-for-quantum-computing\/events\/sahel-ashhab",
      "updated":"2014-05-05T15:13:10-04:00"
    },
    {
      "id":1789,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Science Open Lab",
      "times":[
        {
          "start":"2014-05-27T15:30:00-04:00",
          "end":"2014-05-27T17:00:00-04:00"
        }
      ],
      "type":[
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-science-open-lab",
      "updated":"2014-05-05T13:09:47-04:00"
    },
    {
      "id":117,
      "site":"counselling-services",
      "site_name":"Counselling Services",
      "title":"Procrastination Workshop",
      "times":[
        {
          "start":"2014-05-27T18:00:00-04:00",
          "end":"2014-05-27T20:15:00-04:00"
        },
        {
          "start":"2014-06-03T18:00:00-04:00",
          "end":"2014-06-03T20:15:00-04:00"
        },
        {
          "start":"2014-06-10T18:00:00-04:00",
          "end":"2014-06-10T20:15:00-04:00"
        },
        {
          "start":"2014-06-17T18:00:00-04:00",
          "end":"2014-06-17T20:15:00-04:00"
        },
        {
          "start":"2014-06-24T18:00:00-04:00",
          "end":"2014-06-24T20:15:00-04:00"
        },
        {
          "start":"2014-07-08T18:00:00-04:00",
          "end":"2014-07-08T20:15:00-04:00"
        },
        {
          "start":"2014-07-15T18:00:00-04:00",
          "end":"2014-07-15T20:15:00-04:00"
        },
        {
          "start":"2014-07-22T18:00:00-04:00",
          "end":"2014-07-22T20:15:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/counselling-services\/events\/procrastination-workshop",
      "updated":"2014-04-22T13:20:49-04:00"
    },
    {
      "id":108,
      "site":"counselling-services",
      "site_name":"Counselling Services",
      "title":"Procrastination Solutions",
      "times":[
        {
          "start":"2014-05-27T18:00:00-04:00",
          "end":"2014-05-27T20:15:00-04:00"
        },
        {
          "start":"2014-06-03T18:00:00-04:00",
          "end":"2014-06-03T20:15:00-04:00"
        },
        {
          "start":"2014-06-10T18:00:00-04:00",
          "end":"2014-06-10T20:15:00-04:00"
        },
        {
          "start":"2014-06-17T18:00:00-04:00",
          "end":"2014-06-17T20:15:00-04:00"
        },
        {
          "start":"2014-06-24T18:00:00-04:00",
          "end":"2014-06-24T20:15:00-04:00"
        },
        {
          "start":"2014-07-08T18:00:00-04:00",
          "end":"2014-07-08T20:15:00-04:00"
        },
        {
          "start":"2014-07-15T18:00:00-04:00",
          "end":"2014-07-15T20:15:00-04:00"
        },
        {
          "start":"2014-07-22T18:00:00-04:00",
          "end":"2014-07-22T20:15:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/counselling-services\/events\/procrastination-solutions",
      "updated":"2014-04-09T10:56:14-04:00"
    },
    {
      "id":51,
      "site":"retirees-association",
      "site_name":"Retirees Association",
      "title":"UWRA Annual General Meeting",
      "times":[
        {
          "start":"2014-05-27T19:30:00-04:00",
          "end":"2014-05-27T21:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/retirees-association\/events\/uwra-annual-general-meeting",
      "updated":"2014-03-04T16:58:39-05:00"
    },
    {
      "id":796,
      "site":"housing",
      "site_name":"Residences",
      "title":"Round the World Cooking Class - France",
      "times":[
        {
          "start":"2014-05-27T21:00:00-04:00",
          "end":"2014-05-27T22:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/housing\/events\/round-world-cooking-class-france",
      "updated":"2014-05-01T10:45:10-04:00"
    },
    {
      "id":62,
      "site":"retirees-association",
      "site_name":"Retirees Association",
      "title":"Political Life and the Stops Along with Way with Elizabeth Witmer",
      "times":[
        {
          "start":"2014-05-27T23:00:00-04:00",
          "end":"2014-05-27T23:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/retirees-association\/events\/political-life-and-stops-along-way-elizabeth-witmer",
      "updated":"2014-04-29T16:20:41-04:00"
    },
    {
      "id":2398,
      "site":"alumni",
      "site_name":"Alumni",
      "title":"London, UK Alumni Chapter - Spring Networking Event",
      "times":[
        {
          "start":"2014-05-28T13:00:00-04:00",
          "end":"2014-05-28T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/alumni\/events\/london-uk-alumni-chapter-spring-networking-event",
      "updated":"2014-05-09T09:45:50-04:00"
    },
    {
      "id":121,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Citing Properly with RefWorks",
      "times":[
        {
          "start":"2014-05-28T17:00:00-04:00",
          "end":"2014-05-28T19:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/citing-properly-refworks-0",
      "updated":"2014-05-02T16:51:42-04:00"
    },
    {
      "id":1772,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Citing Properly with RefWorks",
      "times":[
        {
          "start":"2014-05-28T17:00:00-04:00",
          "end":"2014-05-28T19:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/citing-properly-refworks-8",
      "updated":"2014-05-02T09:25:45-04:00"
    },
    {
      "id":869,
      "site":"science",
      "site_name":"Science",
      "title":"How to Start Your Own Business",
      "times":[
        {
          "start":"2014-05-28T18:30:00-04:00",
          "end":"2014-05-28T20:00:00-04:00"
        }
      ],
      "type":[
        "Information session",
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/science\/events\/how-start-your-own-business",
      "updated":"2014-05-05T11:15:56-04:00"
    },
    {
      "id":1828,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Waterloo Women&#039;s Wednesdays",
      "times":[
        {
          "start":"2014-05-28T20:00:00-04:00",
          "end":"2014-05-28T22:00:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/waterloo-womens-wednesdays",
      "updated":"2014-05-13T10:55:22-04:00"
    },
    {
      "id":1817,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Mind \u00adperception versus conception",
      "times":[
        {
          "start":"2014-05-28T21:00:00-04:00",
          "end":"2014-05-28T22:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/mind-perception-versus-conception",
      "updated":"2014-05-08T11:10:42-04:00"
    },
    {
      "id":1788,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Alpha What&#039;s Your Problem?",
      "times":[
        {
          "start":"2014-05-28T23:30:00-04:00",
          "end":"2014-05-29T01:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-alpha-whats-your-problem",
      "updated":"2014-05-05T13:02:16-04:00"
    },
    {
      "id":119,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Keep Current with Research Alerts",
      "times":[
        {
          "start":"2014-05-29T14:00:00-04:00",
          "end":"2014-05-29T15:30:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/keep-current-research-alerts-0",
      "updated":"2014-05-02T16:46:31-04:00"
    },
    {
      "id":1770,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Keep Current with Research Alerts",
      "times":[
        {
          "start":"2014-05-29T14:00:00-04:00",
          "end":"2014-05-29T15:30:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/keep-current-research-alerts-6",
      "updated":"2014-05-02T09:25:50-04:00"
    },
    {
      "id":1197,
      "site":"arts",
      "site_name":"Arts",
      "title":"Status Quo Crisis: Global Financial Governance after the 2008 Meltdown",
      "times":[
        {
          "start":"2014-05-29T23:30:00-04:00",
          "end":"2014-05-29T23:30:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/arts\/events\/status-quo-crisis-global-financial-governance-after-2008",
      "updated":"2014-04-10T11:53:33-04:00"
    },
    {
      "id":95,
      "site":"women-in-engineering",
      "site_name":"Women in Engineering",
      "title":"Girls Club",
      "times":[
        {
          "start":"2014-05-30T04:00:00-04:00",
          "end":"2014-05-30T04:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/women-in-engineering\/events\/girls-club",
      "updated":"2014-04-22T14:50:33-04:00"
    },
    {
      "id":41,
      "site":"toronto-mennonite-theological-centre",
      "site_name":"Toronto Mennonite Theological Centre",
      "title":"TMTC Graduate Student Conference",
      "times":[
        {
          "start":"2014-05-30T23:00:00-04:00",
          "end":"2014-06-01T17:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/toronto-mennonite-theological-centre\/events\/tmtc-graduate-student-conference-0",
      "updated":"2014-05-02T15:56:46-04:00"
    },
    {
      "id":442,
      "site":"centre-automotive-research",
      "site_name":"WATCAR Waterloo Centre for Automotive Research",
      "title":"Toyota High School Electric Vehicle Challenge",
      "times":[
        {
          "start":"2014-05-31T04:00:00-04:00",
          "end":"2014-05-31T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-automotive-research\/events\/toyota-high-school-electric-vehicle-challenge",
      "updated":"2014-04-08T23:12:18-04:00"
    },
    {
      "id":81,
      "site":"sedra-student-design-centre",
      "site_name":"Sedra Student Design Centre",
      "title":"2014 Toyota High School EV Challenge",
      "times":[
        {
          "start":"2014-05-31T04:00:00-04:00",
          "end":"2014-05-31T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/sedra-student-design-centre\/events\/2014-toyota-high-school-ev-challenge",
      "updated":"2014-04-24T14:46:04-04:00"
    },
    {
      "id":1811,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"2014 Toyota High School Electric Vehicle Challenge",
      "times":[
        {
          "start":"2014-05-31T04:00:00-04:00",
          "end":"2014-05-31T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/2014-toyota-high-school-electric-vehicle-challenge",
      "updated":"2014-05-07T16:05:42-04:00"
    },
    {
      "id":1739,
      "site":"engineering",
      "site_name":"Engineering",
      "title":"2014 Toyota High School EV Challenge",
      "times":[
        {
          "start":"2014-05-31T04:00:00-04:00",
          "end":"2014-05-31T04:00:00-04:00"
        }
      ],
      "type":[
        "Open house"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/2014-toyota-high-school-ev-challenge",
      "updated":"2014-04-24T10:43:14-04:00"
    },
    {
      "id":1823,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"2014 Toyota High School EV Challenge",
      "times":[
        {
          "start":"2014-05-31T14:30:00-04:00",
          "end":"2014-05-31T20:00:00-04:00"
        }
      ],
      "type":[
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/2014-toyota-high-school-ev-challenge",
      "updated":"2014-05-08T11:56:10-04:00"
    },
    {
      "id":445,
      "site":"centre-automotive-research",
      "site_name":"WATCAR Waterloo Centre for Automotive Research",
      "title":"IST Canada Conference",
      "times":[
        {
          "start":"2014-06-01T04:00:00-04:00",
          "end":"2014-06-04T04:00:00-04:00"
        }
      ],
      "type":[
        "Conference"
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-automotive-research\/events\/ist-canada-conference",
      "updated":"2014-04-10T21:41:02-04:00"
    },
    {
      "id":86,
      "site":"leonenko-research-group",
      "site_name":"Leonenko Research Group",
      "title":"Canadian Chemistry Conference &amp; Exhibition 2014",
      "times":[
        {
          "start":"2014-06-01T04:00:00-04:00",
          "end":"2014-06-05T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/leonenko-research-group\/events\/canadian-chemistry-conference-exhibition-2014",
      "updated":"2014-01-16T12:03:23-05:00"
    },
    {
      "id":1297,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Teaching Methods (CTE217)",
      "times":[
        {
          "start":"2014-06-02T13:30:00-04:00",
          "end":"2014-06-02T15:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/teaching-methods-cte217-3",
      "updated":"2014-04-30T14:33:04-04:00"
    },
    {
      "id":915,
      "site":"biology",
      "site_name":"Department of Biology",
      "title":"MSc Thesis Proposal - Che Lu",
      "times":[
        {
          "start":"2014-06-02T18:00:00-04:00",
          "end":"2014-06-02T18:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/biology\/events\/msc-thesis-proposal-che-lu",
      "updated":"2014-04-25T14:20:57-04:00"
    },
    {
      "id":106,
      "site":"counselling-services",
      "site_name":"Counselling Services",
      "title":"Mindfulness Based Relapse Prevention",
      "times":[
        {
          "start":"2014-06-02T18:30:00-04:00",
          "end":"2014-06-02T20:30:00-04:00"
        },
        {
          "start":"2014-06-09T18:30:00-04:00",
          "end":"2014-06-09T20:30:00-04:00"
        },
        {
          "start":"2014-06-16T18:30:00-04:00",
          "end":"2014-06-16T20:30:00-04:00"
        },
        {
          "start":"2014-06-23T18:30:00-04:00",
          "end":"2014-06-23T20:30:00-04:00"
        },
        {
          "start":"2014-07-07T18:30:00-04:00",
          "end":"2014-07-07T20:30:00-04:00"
        },
        {
          "start":"2014-07-14T18:30:00-04:00",
          "end":"2014-07-14T20:30:00-04:00"
        },
        {
          "start":"2014-07-21T18:30:00-04:00",
          "end":"2014-07-21T20:30:00-04:00"
        },
        {
          "start":"2014-07-28T18:30:00-04:00",
          "end":"2014-07-28T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/counselling-services\/events\/mindfulness-based-relapse-prevention",
      "updated":"2014-04-11T15:41:56-04:00"
    },
    {
      "id":56,
      "site":"retirees-association",
      "site_name":"Retirees Association",
      "title":"Port Dover - A theatre of war &amp; comedy",
      "times":[
        {
          "start":"2014-06-03T04:00:00-04:00",
          "end":"2014-06-03T04:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/retirees-association\/events\/port-dover-theatre-war-comedy",
      "updated":"2014-04-02T15:43:55-04:00"
    },
    {
      "id":124,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Power Search",
      "times":[
        {
          "start":"2014-06-03T14:00:00-04:00",
          "end":"2014-06-03T16:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/power-search",
      "updated":"2014-05-02T16:58:48-04:00"
    },
    {
      "id":1775,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Power Search",
      "times":[
        {
          "start":"2014-06-03T14:00:00-04:00",
          "end":"2014-06-03T16:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/power-search-0",
      "updated":"2014-05-02T09:25:40-04:00"
    },
    {
      "id":120,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Better Searching - Better Marks",
      "times":[
        {
          "start":"2014-06-03T17:00:00-04:00",
          "end":"2014-06-03T18:30:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/better-searching-better-marks-0",
      "updated":"2014-05-02T16:48:59-04:00"
    },
    {
      "id":1771,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Better Searching - Better Marks",
      "times":[
        {
          "start":"2014-06-03T17:00:00-04:00",
          "end":"2014-06-03T18:30:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/better-searching-better-marks-13",
      "updated":"2014-05-02T09:25:47-04:00"
    },
    {
      "id":198,
      "site":"geriatric-health-systems-research-group",
      "site_name":"Geriatric Health Systems Research Group",
      "title":"Managing the Seams: Transitions in Health Care for Older Adults",
      "times":[
        {
          "start":"2014-06-03T17:00:00-04:00",
          "end":"2014-06-03T20:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/geriatric-health-systems-research-group\/events\/managing-seams-transitions-health-care-older-adults",
      "updated":"2014-05-07T15:38:20-04:00"
    },
    {
      "id":834,
      "site":"applied-health-sciences",
      "site_name":"Applied Health Sciences",
      "title":"Managing the Seams: Transitions in Health Care for Older Adults",
      "times":[
        {
          "start":"2014-06-03T17:00:00-04:00",
          "end":"2014-06-03T20:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/applied-health-sciences\/events\/managing-seams-transitions-health-care-older-adults",
      "updated":"2014-05-07T14:45:40-04:00"
    },
    {
      "id":1831,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Building Game Developers",
      "times":[
        {
          "start":"2014-06-03T19:30:00-04:00",
          "end":"2014-06-03T20:30:00-04:00"
        }
      ],
      "type":[
        "Lecture"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/building-game-developers",
      "updated":"2014-05-13T11:23:41-04:00"
    },
    {
      "id":446,
      "site":"centre-automotive-research",
      "site_name":"WATCAR Waterloo Centre for Automotive Research",
      "title":"APMA Annual Conference and Exhibition",
      "times":[
        {
          "start":"2014-06-04T04:00:00-04:00",
          "end":"2014-06-05T04:00:00-04:00"
        }
      ],
      "type":[
        "Conference"
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-automotive-research\/events\/apma-annual-conference-and-exhibition",
      "updated":"2014-04-10T22:01:13-04:00"
    },
    {
      "id":539,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"Accessible Word and PDF Files [SEW106]",
      "times":[
        {
          "start":"2014-06-04T14:00:00-04:00",
          "end":"2014-06-04T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/accessible-word-and-pdf-files-sew106-7",
      "updated":"2014-04-29T13:52:31-04:00"
    },
    {
      "id":874,
      "site":"science",
      "site_name":"Science",
      "title":"Writing Successful Grant Proposals (Graduate students and Postdocs only)",
      "times":[
        {
          "start":"2014-06-04T14:30:00-04:00",
          "end":"2014-06-04T16:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/science\/events\/writing-successful-grant-proposals-graduate-students-and",
      "updated":"2014-05-05T11:42:53-04:00"
    },
    {
      "id":538,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"Creating Accessible Tables [SEW112]",
      "times":[
        {
          "start":"2014-06-04T17:30:00-04:00",
          "end":"2014-06-04T19:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/creating-accessible-tables-sew112-1",
      "updated":"2014-04-29T13:49:42-04:00"
    },
    {
      "id":125,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Introduction to ArcGIS Desktop 10.2",
      "times":[
        {
          "start":"2014-06-04T18:00:00-04:00",
          "end":"2014-06-04T20:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/introduction-arcgis-desktop-102",
      "updated":"2014-05-02T17:01:41-04:00"
    },
    {
      "id":1776,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Introduction to ArcGIS Desktop 10.2",
      "times":[
        {
          "start":"2014-06-04T18:00:00-04:00",
          "end":"2014-06-04T20:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/introduction-arcgis-desktop-102",
      "updated":"2014-05-02T09:25:37-04:00"
    },
    {
      "id":1818,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Intelligence, quality versus quantity",
      "times":[
        {
          "start":"2014-06-04T21:00:00-04:00",
          "end":"2014-06-04T22:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/intelligence-quality-versus-quantity",
      "updated":"2014-05-08T11:16:15-04:00"
    },
    {
      "id":1787,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Alpha Business Model Generation",
      "times":[
        {
          "start":"2014-06-04T23:30:00-04:00",
          "end":"2014-06-05T01:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-alpha-business-model-generation",
      "updated":"2014-05-05T12:56:49-04:00"
    },
    {
      "id":865,
      "site":"science",
      "site_name":"Science",
      "title":"Career Exploration and Decision Making",
      "times":[
        {
          "start":"2014-06-05T18:30:00-04:00",
          "end":"2014-06-05T20:30:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/science\/events\/career-exploration-and-decision-making",
      "updated":"2014-05-05T11:16:50-04:00"
    },
    {
      "id":1953,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Mennofolk Concert",
      "times":[
        {
          "start":"2014-06-05T19:00:00-04:00",
          "end":"2014-06-05T19:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/mennofolk-concert",
      "updated":"2014-05-05T13:31:26-04:00"
    },
    {
      "id":256,
      "site":"music",
      "site_name":"Music",
      "title":"Mennofolk Concert",
      "times":[
        {
          "start":"2014-06-05T19:00:00-04:00",
          "end":"2014-06-05T19:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/music\/events\/mennofolk-concert",
      "updated":"2014-05-05T13:45:05-04:00"
    },
    {
      "id":1369,
      "site":"renison",
      "site_name":"Renison University College",
      "title":"Barbara J. Checketts Retirement Event",
      "times":[
        {
          "start":"2014-06-05T20:00:00-04:00",
          "end":"2014-06-05T22:30:00-04:00"
        }
      ],
      "type":[
        "Reception"
      ],
      "link":"https:\/\/uwaterloo.ca\/renison\/events\/barbara-j-checketts-retirement-event",
      "updated":"2014-05-05T12:58:11-04:00"
    },
    {
      "id":1820,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Barbara J. Checketts retirement",
      "times":[
        {
          "start":"2014-06-05T20:00:00-04:00",
          "end":"2014-06-05T22:30:00-04:00"
        }
      ],
      "type":[
        "Reception"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/barbara-j-checketts-retirement",
      "updated":"2014-05-08T11:25:40-04:00"
    },
    {
      "id":556,
      "site":"optometry-vision-science",
      "site_name":"Optometry &amp; Vision Science",
      "title":"June CE 2014",
      "times":[
        {
          "start":"2014-06-06T04:00:00-04:00",
          "end":"2014-06-08T04:00:00-04:00"
        }
      ],
      "type":[
        "Conference"
      ],
      "link":"https:\/\/uwaterloo.ca\/optometry-vision-science\/events\/june-ce-2014",
      "updated":"2014-03-05T16:37:34-05:00"
    },
    {
      "id":1738,
      "site":"engineering",
      "site_name":"Engineering",
      "title":"Pan IIT Conference - Toronto 2014",
      "times":[
        {
          "start":"2014-06-06T04:00:00-04:00",
          "end":"2014-06-08T04:00:00-04:00"
        }
      ],
      "type":[
        "Conference"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/pan-iit-conference-toronto-2014",
      "updated":"2014-04-24T11:06:15-04:00"
    },
    {
      "id":1298,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Facilitating Effective Discussions (Social Sciences &amp; Humanities) (CTE228)",
      "times":[
        {
          "start":"2014-06-06T13:30:00-04:00",
          "end":"2014-06-06T15:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/facilitating-effective-discussions-social-sciences-1",
      "updated":"2014-04-30T14:36:34-04:00"
    },
    {
      "id":1312,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-06-06T13:30:00-04:00",
          "end":"2014-06-06T16:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-95",
      "updated":"2014-05-09T14:00:13-04:00"
    },
    {
      "id":1737,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Sound in the Land 2014 Festival and Conference - Music and the Environment",
      "times":[
        {
          "start":"2014-06-06T17:00:00-04:00",
          "end":"2014-06-09T17:00:00-04:00"
        }
      ],
      "type":[
        "Conference"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/sound-land-2014-festival-and-conference-music-and",
      "updated":"2014-04-17T15:26:43-04:00"
    },
    {
      "id":982,
      "site":"environment",
      "site_name":"uWaterloo - Faculty of Environment",
      "title":"Class of &#039;74 Planning Reunion",
      "times":[
        {
          "start":"2014-06-06T23:00:00-04:00",
          "end":"2014-06-08T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/environment\/events\/class-74-planning-reunion",
      "updated":"2014-04-23T13:56:48-04:00"
    },
    {
      "id":1954,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Sonic Convergences",
      "times":[
        {
          "start":"2014-06-07T00:00:00-04:00",
          "end":"2014-06-07T00:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/sonic-convergences",
      "updated":"2014-05-01T13:36:54-04:00"
    },
    {
      "id":257,
      "site":"music",
      "site_name":"Music",
      "title":"Sonic Convergences",
      "times":[
        {
          "start":"2014-06-07T00:00:00-04:00",
          "end":"2014-06-07T00:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/music\/events\/sonic-convergences",
      "updated":"2014-05-05T11:31:17-04:00"
    },
    {
      "id":1955,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Kalahari Journey",
      "times":[
        {
          "start":"2014-06-08T00:00:00-04:00",
          "end":"2014-06-08T00:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/kalahari-journey",
      "updated":"2014-04-25T09:18:58-04:00"
    },
    {
      "id":258,
      "site":"music",
      "site_name":"Music",
      "title":"Kalahari Journey",
      "times":[
        {
          "start":"2014-06-08T00:00:00-04:00",
          "end":"2014-06-08T00:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/music\/events\/kalahari-journey",
      "updated":"2014-05-05T12:32:11-04:00"
    },
    {
      "id":1956,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Dawn Concert",
      "times":[
        {
          "start":"2014-06-08T11:00:00-04:00",
          "end":"2014-06-08T11:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/dawn-concert",
      "updated":"2014-04-24T14:57:17-04:00"
    },
    {
      "id":259,
      "site":"music",
      "site_name":"Music",
      "title":"Dawn Concert",
      "times":[
        {
          "start":"2014-06-08T11:00:00-04:00",
          "end":"2014-06-08T11:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/music\/events\/dawn-concert",
      "updated":"2014-05-05T12:36:18-04:00"
    },
    {
      "id":1957,
      "site":"grebel",
      "site_name":"Conrad Grebel University College",
      "title":"Choral Concert",
      "times":[
        {
          "start":"2014-06-08T23:00:00-04:00",
          "end":"2014-06-08T23:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/grebel\/events\/choral-concert",
      "updated":"2014-04-24T15:00:22-04:00"
    },
    {
      "id":260,
      "site":"music",
      "site_name":"Music",
      "title":"Choral Concert",
      "times":[
        {
          "start":"2014-06-08T23:00:00-04:00",
          "end":"2014-06-08T23:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Performance"
      ],
      "link":"https:\/\/uwaterloo.ca\/music\/events\/choral-concert",
      "updated":"2014-05-05T12:40:27-04:00"
    },
    {
      "id":1299,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Effective Lesson Plans (CTE202)",
      "times":[
        {
          "start":"2014-06-09T13:30:00-04:00",
          "end":"2014-06-09T15:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/effective-lesson-plans-cte202-9",
      "updated":"2014-04-30T14:39:22-04:00"
    },
    {
      "id":798,
      "site":"research",
      "site_name":"Research",
      "title":"Information session: CIHR\u2019s new foundation scheme",
      "times":[
        {
          "start":"2014-06-09T14:30:00-04:00",
          "end":"2014-06-09T14:30:00-04:00"
        }
      ],
      "type":[
        "Information session"
      ],
      "link":"https:\/\/uwaterloo.ca\/research\/events\/information-session-cihrs-new-foundation-scheme",
      "updated":"2014-05-08T09:09:02-04:00"
    },
    {
      "id":312,
      "site":"management-sciences",
      "site_name":"Management Sciences",
      "title":"Management Sciences Seminar Series: Kory W. Hedman",
      "times":[
        {
          "start":"2014-06-09T16:00:00-04:00",
          "end":"2014-06-09T17:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/management-sciences\/events\/management-sciences-seminar-series-kory-w-hedman",
      "updated":"2014-05-13T15:35:48-04:00"
    },
    {
      "id":1313,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-06-09T18:00:00-04:00",
          "end":"2014-06-09T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-96",
      "updated":"2014-05-09T14:00:36-04:00"
    },
    {
      "id":1314,
      "site":"centre-for-teaching-excellence",
      "site_name":"Centre for Teaching Excellence",
      "title":"Microteaching Session",
      "times":[
        {
          "start":"2014-06-10T13:30:00-04:00",
          "end":"2014-06-10T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/events\/microteaching-session-97",
      "updated":"2014-05-09T14:00:41-04:00"
    },
    {
      "id":122,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"Citing Properly with RefWorks",
      "times":[
        {
          "start":"2014-06-10T17:00:00-04:00",
          "end":"2014-06-10T19:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/citing-properly-refworks-1",
      "updated":"2014-05-02T16:53:51-04:00"
    },
    {
      "id":1773,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Citing Properly with RefWorks",
      "times":[
        {
          "start":"2014-06-10T17:00:00-04:00",
          "end":"2014-06-10T19:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/citing-properly-refworks-9",
      "updated":"2014-05-02T09:25:44-04:00"
    },
    {
      "id":215,
      "site":"international-students",
      "site_name":"International Student Experience",
      "title":"Study Permit online application workshop",
      "times":[
        {
          "start":"2014-06-10T18:30:00-04:00",
          "end":"2014-06-10T20:00:00-04:00"
        },
        {
          "start":"2014-07-08T18:30:00-04:00",
          "end":"2014-07-08T20:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/international-students\/events\/study-permit-online-application-workshop",
      "updated":"2014-04-24T15:48:26-04:00"
    },
    {
      "id":1003,
      "site":"environment",
      "site_name":"uWaterloo - Faculty of Environment",
      "title":"Spring 2014 Faculty of Environment Convocation Ceremony",
      "times":[
        {
          "start":"2014-06-10T18:30:00-04:00",
          "end":"2014-06-10T20:30:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/environment\/events\/spring-2014-faculty-environment-convocation-ceremony",
      "updated":"2014-04-23T14:46:21-04:00"
    },
    {
      "id":1002,
      "site":"environment",
      "site_name":"uWaterloo - Faculty of Environment",
      "title":"Spring 2014 Grad Receptions",
      "times":[
        {
          "start":"2014-06-10T20:30:00-04:00",
          "end":"2014-06-10T22:00:00-04:00"
        }
      ],
      "type":[
        "Reception"
      ],
      "link":"https:\/\/uwaterloo.ca\/environment\/events\/spring-2014-grad-receptions",
      "updated":"2014-04-23T14:31:27-04:00"
    },
    {
      "id":364,
      "site":"knowledge-integration",
      "site_name":"Knowledge Integration",
      "title":"Convocation",
      "times":[
        {
          "start":"2014-06-10T21:22:00-04:00",
          "end":"2014-06-10T21:22:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/knowledge-integration\/events\/convocation",
      "updated":"2014-03-03T17:25:45-05:00"
    },
    {
      "id":268,
      "site":"planning",
      "site_name":"School of Planning",
      "title":"School of Planning Graduation Ceremony",
      "times":[
        {
          "start":"2014-06-11T03:30:00-04:00",
          "end":"2014-06-11T03:30:00-04:00"
        }
      ],
      "type":[
        "Reception"
      ],
      "link":"https:\/\/uwaterloo.ca\/planning\/events\/school-planning-graduation-ceremony",
      "updated":"2014-05-07T15:20:50-04:00"
    },
    {
      "id":537,
      "site":"web-resources",
      "site_name":"Web Resources",
      "title":"Creating Accessible Web Graphics [SEW108]",
      "times":[
        {
          "start":"2014-06-11T14:30:00-04:00",
          "end":"2014-06-11T16:00:00-04:00"
        }
      ],
      "type":[
        
      ],
      "link":"https:\/\/uwaterloo.ca\/web-resources\/events\/creating-accessible-web-graphics-sew108-5",
      "updated":"2014-04-29T13:47:41-04:00"
    },
    {
      "id":126,
      "site":"library\/news",
      "site_name":"Library News",
      "title":"SketchUp: 3D Modeling Made Easy",
      "times":[
        {
          "start":"2014-06-11T18:00:00-04:00",
          "end":"2014-06-11T20:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/library\/news\/events\/sketchup-3d-modeling-made-easy",
      "updated":"2014-05-02T17:04:29-04:00"
    },
    {
      "id":1777,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"SketchUp: 3D Modeling Made Easy",
      "times":[
        {
          "start":"2014-06-11T18:00:00-04:00",
          "end":"2014-06-11T20:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/sketchup-3d-modeling-made-easy",
      "updated":"2014-05-02T09:25:34-04:00"
    },
    {
      "id":1819,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Wisdom, learning versus knowledge",
      "times":[
        {
          "start":"2014-06-11T21:00:00-04:00",
          "end":"2014-06-11T22:30:00-04:00"
        }
      ],
      "type":[
        "Seminar"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/wisdom-learning-versus-knowledge",
      "updated":"2014-05-08T11:19:39-04:00"
    },
    {
      "id":1767,
      "site":"events",
      "site_name":"Waterloo Events",
      "title":"Velocity Alpha: Do People Want Your Stuff",
      "times":[
        {
          "start":"2014-06-11T23:30:00-04:00",
          "end":"2014-06-12T01:00:00-04:00"
        }
      ],
      "type":[
        "Workshop"
      ],
      "link":"https:\/\/uwaterloo.ca\/events\/events\/velocity-alpha-do-people-want-your-stuff",
      "updated":"2014-05-01T12:55:11-04:00"
    }
  ]
}
```


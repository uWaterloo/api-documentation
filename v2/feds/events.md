# Get All FEDS Events

```
GET /feds/events.{format}
```

## Description

> This method returns a list of the upcoming events from the FEDS database

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
    <td>1723</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>feds</td>
    <td><b>Service ID</b></td>
    <td>311</td>
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



## Parameters

```
GET /feds/events.{format}
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
GET /feds/events.{format}
```

- **https://api.uwaterloo.ca/v2/feds/events.json**
- **https://api.uwaterloo.ca/v2/feds/events.xml**
- **https://api.uwaterloo.ca/v2/feds/events.json?callback=myResponse**


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
    <td><b>title</b></td>
    <td>string</td>
    <td>Event title</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Event location</td>
  </tr>
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
  <tr>
    <td><b>categories</b></td>
    <td>array</td>
    <td>Type of event</td>
  </tr>
  <tr>
    <td><b>url</b></td>
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
    "requests":811364,
    "timestamp":1453149684,
    "status":200,
    "message":"Request successful",
    "method_id":1723,
    "method":{
      
    }
  },
  "data":[
    {
      "id":300787,
      "title":"MFE@UWaterloo",
      "location":null,
      "start":"2016-01-11T17:30:00-05:00",
      "end":"2016-01-11T19:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-05T10:39:40-05:00",
      "url":"http:\/\/www.feds.ca\/event\/mfeuwaterloo\/"
    },
    {
      "id":301568,
      "title":"Sex Toy Bingo",
      "location":"200 University Ave, Waterloo, N2L3G1, Canada",
      "start":"2016-01-11T19:00:00-05:00",
      "end":"2016-01-11T23:55:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-08T17:20:11-05:00",
      "url":"http:\/\/www.feds.ca\/event\/sex-toy-bingo-5\/"
    },
    {
      "id":300607,
      "title":"Volunteer Fair",
      "location":null,
      "start":"2016-01-12T11:00:00-05:00",
      "end":"2016-01-12T14:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-04T17:10:44-05:00",
      "url":"http:\/\/www.feds.ca\/event\/volunteer-fair-2\/"
    },
    {
      "id":294962,
      "title":"Mandatory Presidents Meetings",
      "location":null,
      "start":"2016-01-12T15:30:00-05:00",
      "end":"2016-01-12T16:30:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-11T09:19:40-05:00",
      "url":"http:\/\/www.feds.ca\/event\/mandatory-presidents-meetings\/"
    },
    {
      "id":295778,
      "title":"Warriors on Ice",
      "location":null,
      "start":"2016-01-12T20:00:00-05:00",
      "end":"2016-01-12T23:00:00-05:00",
      "categories":[
        "Athletics",
        "Sports & Recreational,Events"
      ],
      "updated":"2015-12-15T13:41:02-05:00",
      "url":"http:\/\/www.feds.ca\/event\/warriors-ice\/"
    },
    {
      "id":301630,
      "title":"NYE 2.0",
      "location":null,
      "start":"2016-01-13T08:00:00-05:00",
      "end":"2016-01-13T17:00:00-05:00",
      "categories":[
        "Events,Pub Events"
      ],
      "updated":"2016-01-08T17:23:58-05:00",
      "url":"http:\/\/www.feds.ca\/event\/nye-2-0\/"
    },
    {
      "id":295779,
      "title":"Campus Life Fair",
      "location":null,
      "start":"2016-01-13T11:00:00-05:00",
      "end":"2016-01-13T14:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-15T13:46:57-05:00",
      "url":"http:\/\/www.feds.ca\/event\/campus-life-fair-5\/"
    },
    {
      "id":302347,
      "title":"University of Waterloo Dragon Boat Club Recruitment",
      "location":null,
      "start":"2016-01-14T09:00:00-05:00",
      "end":"2016-01-15T15:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-06T11:38:35-05:00",
      "url":"http:\/\/www.feds.ca\/event\/university-of-waterloo-dragon-boat-club-recruitment-2\/"
    },
    {
      "id":295780,
      "title":"Super Ball Scooping",
      "location":null,
      "start":"2016-01-14T10:00:00-05:00",
      "end":"2016-01-14T14:00:00-05:00",
      "categories":[
        "Athletics",
        "Sports & Recreational,Events"
      ],
      "updated":"2015-12-15T14:08:01-05:00",
      "url":"http:\/\/www.feds.ca\/event\/super-ball-scooping\/"
    },
    {
      "id":302349,
      "title":"Waterloo Chopstick Challenge",
      "location":null,
      "start":"2016-01-14T11:00:00-05:00",
      "end":"2016-01-14T14:00:00-05:00",
      "categories":[
        "Athletics",
        "Sports & Recreational,Events"
      ],
      "updated":"2016-01-08T17:11:52-05:00",
      "url":"http:\/\/www.feds.ca\/event\/waterloo-chopstick-challenge-2\/"
    },
    {
      "id":295781,
      "title":"Clubs and Societies Days",
      "location":null,
      "start":"2016-01-14T11:00:00-05:00",
      "end":"2016-01-14T18:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-15T13:54:45-05:00",
      "url":"http:\/\/www.feds.ca\/event\/clubs-societies-days-4\/"
    },
    {
      "id":294251,
      "title":"UW Mambo Club",
      "location":null,
      "start":"2016-01-14T20:00:00-05:00",
      "end":"2016-01-14T22:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-03T15:24:46-05:00",
      "url":"http:\/\/www.feds.ca\/event\/uw-mambo-club\/2016-01-14\/"
    },
    {
      "id":294885,
      "title":"Clubs & Societies Days",
      "location":null,
      "start":"2016-01-14T23:00:00-05:00",
      "end":"2016-01-14T23:00:00-05:00",
      "categories":[
        "Athletics",
        "Sports & Recreational,Business & Entrepreneurial Events,Careers,Charitable",
        "Community Service & International Development Events,Creative Arts",
        "Dance & Music Events,Cultural Clubs,Diversity Events,Health & Wellbeing Events,Spirit Building Events"
      ],
      "updated":"2015-12-10T21:14:44-05:00",
      "url":"http:\/\/www.feds.ca\/event\/clubs-societies-days-2\/"
    },
    {
      "id":302351,
      "title":"Clubs and Societies Days",
      "location":null,
      "start":"2016-01-15T10:00:00-05:00",
      "end":"2016-01-15T15:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-15T13:53:14-05:00",
      "url":"http:\/\/www.feds.ca\/event\/clubs-societies-days-5\/"
    },
    {
      "id":294890,
      "title":"Clubs & Societies Days",
      "location":null,
      "start":"2016-01-15T10:00:00-05:00",
      "end":"2016-01-15T15:00:00-05:00",
      "categories":[
        "Academic Events,Athletics",
        "Sports & Recreational,Business & Entrepreneurial Events,Cultural Clubs,Environmental & Sustainability Clubs & Initiatives,Spirit Building Events"
      ],
      "updated":"2015-12-10T21:16:07-05:00",
      "url":"http:\/\/www.feds.ca\/event\/clubs-societies-days-3\/"
    },
    {
      "id":302589,
      "title":"Ski Trip to Kissing Bridge",
      "location":null,
      "start":"2016-01-16T07:00:00-05:00",
      "end":"2016-01-16T23:30:00-05:00",
      "categories":[
        "Athletics",
        "Sports & Recreational,Events"
      ],
      "updated":"2015-12-15T14:05:09-05:00",
      "url":"http:\/\/www.feds.ca\/event\/ski-trip-kissing-bridge\/"
    },
    {
      "id":302590,
      "title":"Junior Executive Interviews",
      "location":null,
      "start":"2016-01-18T19:00:00-05:00",
      "end":"2016-01-18T21:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-12T12:38:52-05:00",
      "url":"http:\/\/www.feds.ca\/event\/junior-executive-interviews\/"
    },
    {
      "id":295179,
      "title":"Mandatory Exec Training",
      "location":null,
      "start":"2016-01-19T03:30:00-05:00",
      "end":"2016-01-19T16:30:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-11T09:18:14-05:00",
      "url":"http:\/\/www.feds.ca\/event\/mandatory-exec-training-3\/"
    },
    {
      "id":302830,
      "title":"Feds Open House",
      "location":null,
      "start":"2016-01-19T11:00:00-05:00",
      "end":"2016-01-19T14:00:00-05:00",
      "categories":[
        "Events,Motivational\/Inspirational,Spirit Building Events"
      ],
      "updated":"2016-01-13T16:49:40-05:00",
      "url":"http:\/\/www.feds.ca\/event\/feds-open-house-6\/"
    },
    {
      "id":302831,
      "title":"Winter Meeting",
      "location":null,
      "start":"2016-01-19T18:30:00-05:00",
      "end":"2016-01-19T20:30:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-12T09:54:22-05:00",
      "url":"http:\/\/www.feds.ca\/event\/winter-meeting\/"
    },
    {
      "id":303069,
      "title":"Bomber Blackout",
      "location":"200 University Ave, Waterloo, N2L3G1, Canada",
      "start":"2016-01-20T19:00:00-05:00",
      "end":"2016-01-20T23:55:00-05:00",
      "categories":[
        "Events,Pub Events"
      ],
      "updated":"2016-01-08T17:31:05-05:00",
      "url":"http:\/\/www.feds.ca\/event\/bomber-blackout\/"
    },
    {
      "id":303070,
      "title":"Mandatory Exec Training",
      "location":null,
      "start":"2016-01-21T10:00:00-05:00",
      "end":"2016-01-21T11:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-11T10:54:26-05:00",
      "url":"http:\/\/www.feds.ca\/event\/mandatory-exec-training-4\/"
    },
    {
      "id":295180,
      "title":"Mandatory Exec Training",
      "location":null,
      "start":"2016-01-21T10:30:00-05:00",
      "end":"2016-01-21T11:30:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-13T01:54:32-05:00",
      "url":"http:\/\/www.feds.ca\/event\/mandatory-exec-training-4\/"
    },
    {
      "id":303201,
      "title":"General Meeting",
      "location":null,
      "start":"2016-01-21T18:00:00-05:00",
      "end":"2016-01-21T19:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-15T12:57:51-05:00",
      "url":"http:\/\/www.feds.ca\/event\/general-meeting-2\/"
    },
    {
      "id":303071,
      "title":"UW Mambo Club",
      "location":null,
      "start":"2016-01-21T20:00:00-05:00",
      "end":"2016-01-21T22:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-03T15:23:52-05:00",
      "url":"http:\/\/www.feds.ca\/event\/uw-mambo-club\/2016-01-21\/"
    },
    {
      "id":303311,
      "title":"Sever Ties Referendum",
      "location":null,
      "start":"2016-01-25T10:00:00-05:00",
      "end":"2016-01-27T22:00:00-05:00",
      "categories":[
        "Events,Political & Social Awareness Events"
      ],
      "updated":"2016-01-08T17:17:17-05:00",
      "url":"http:\/\/www.feds.ca\/event\/sever-ties-referendum\/"
    },
    {
      "id":303551,
      "title":"Samosa Sale",
      "location":null,
      "start":"2016-01-27T09:00:00-05:00",
      "end":"2016-01-28T17:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2016-01-15T12:58:11-05:00",
      "url":"http:\/\/www.feds.ca\/event\/samosa-sale-2\/"
    },
    {
      "id":294966,
      "title":"Mandatory Presidents Meetings",
      "location":null,
      "start":"2016-02-01T12:00:00-05:00",
      "end":"2016-02-01T13:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-11T14:38:12-05:00",
      "url":"http:\/\/www.feds.ca\/event\/mandatory-presidents-meetings-2\/"
    },
    {
      "id":294252,
      "title":"Chilly Dog Run\/Walk",
      "location":null,
      "start":"2016-02-27T09:00:00-05:00",
      "end":"2016-02-27T15:00:00-05:00",
      "categories":[
        "Events"
      ],
      "updated":"2015-12-03T15:22:59-05:00",
      "url":"http:\/\/www.feds.ca\/event\/chilly-dog-runwalk\/"
    }
  ]
}
```


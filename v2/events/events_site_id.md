# Get Events for Site given id

```
GET events/{site}/{id}.{format}
```

## Description

> Array

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
    <td>1567</td>
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
GET events/{site}/{id}.{format}
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
    <td><b>site</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid site slug from /resources/sites</td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid event id</td>
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
GET events/{site}/{id}.{format}
```

- **https://api.uwaterloo.ca/v2/events/engineering/1701.json**
- **https://api.uwaterloo.ca/v2/events/engineering/1701.xml**
- **https://api.uwaterloo.ca/v2/events/engineering/1701.json?callback=myResponse**


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
    <td><b>description</b></td>
    <td>string</td>
    <td>Event description</td>
  </tr>
  <tr>
    <td><b>description_raw</b></td>
    <td>string</td>
    <td>Raw event description (includes HTML markup)</td>
  </tr>
  <tr>
    <td><b>times</b></td>
    <td>list</td>
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
  <tr>
    <td><b>start_day</b></td>
    <td>string</td>
    <td>Full name of day of week for start day</td>
  </tr>
  <tr>
    <td><b>start_date</b></td>
    <td>sate</td>
    <td>YYYY-MM-DD formatted start date</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>sate</td>
    <td>HH:MM:SS 24 formatted start time</td>
  </tr>
  <tr>
    <td><b>end_day</b></td>
    <td>string</td>
    <td>Full name of day of week for end day</td>
  </tr>
  <tr>
    <td><b>end_date</b></td>
    <td>string</td>
    <td>YYYY-MM-DD formatted end date</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>HH:MM:SS 24 formatted end time</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>cost</b></td>
    <td>string</td>
    <td>Cost of event</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>list</td>
    <td>Audience targeted by event</td>
  </tr>
  <tr>
    <td><b>tags</b></td>
    <td>list</td>
    <td>Tags related to event</td>
  </tr>
  <tr>
    <td><b>type</b></td>
    <td>list</td>
    <td>Type of event</td>
  </tr>
  <tr>
    <td><b>website</b></td>
    <td>object</td>
    <td>The event's website for more information<br><table>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Title of the link</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>URL of the link</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>host</b></td>
    <td>object</td>
    <td>The event's host<br><table>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Title of the link</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>URL of the link</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>image</b></td>
    <td>object</td>
    <td>Image representing the event<br><table>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Unique id of image</td>
  </tr>
  <tr>
    <td><b>file</b></td>
    <td>string</td>
    <td>Relative link to image file path in filename.{format}</td>
  </tr>
  <tr>
    <td><b>alt</b></td>
    <td>string</td>
    <td>Image alternate text</td>
  </tr>
  <tr>
    <td><b>mime</b></td>
    <td>string</td>
    <td>Image MIME type in "string/{format}"</td>
  </tr>
  <tr>
    <td><b>size</b></td>
    <td>integer</td>
    <td>Image file size in bytes</td>
  </tr>
  <tr>
    <td><b>width</b></td>
    <td>integer</td>
    <td>Image width in pixels</td>
  </tr>
  <tr>
    <td><b>height</b></td>
    <td>integer</td>
    <td>Image height in pixels</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>Full link to image resource</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>object</td>
    <td>Location of the event<br><table>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Unique id of location</td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Name of location</td>
  </tr>
  <tr>
    <td><b>street</b></td>
    <td>string</td>
    <td>Street address of location</td>
  </tr>
  <tr>
    <td><b>additional</b></td>
    <td>string</td>
    <td>Additional information regarding street address of location</td>
  </tr>
  <tr>
    <td><b>city</b></td>
    <td>string</td>
    <td>Name of city</td>
  </tr>
  <tr>
    <td><b>province</b></td>
    <td>string</td>
    <td>Name of province in two-letter short form</td>
  </tr>
  <tr>
    <td><b>postal_code</b></td>
    <td>string</td>
    <td>Postal code "in L#L #L#" format</td>
  </tr>
  <tr>
    <td><b>country</b></td>
    <td>string</td>
    <td>Full name of country</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>number</td>
    <td>Event location latitude</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>number</td>
    <td>Event location longitude</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Full site name as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>site_id</b></td>
    <td>string</td>
    <td>Site slug as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>revision_id</b></td>
    <td>integer</td>
    <td>Unique id of revision of event</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>URL of event link</td>
  </tr>
  <tr>
    <td><b>link_calendar</b></td>
    <td>string</td>
    <td>iCal feed of event</td>
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
    "requests":492,
    "timestamp":1399702009,
    "status":200,
    "message":"Request successful",
    "method_id":1567,
    "method":{
      
    }
  },
  "data":{
    "id":1701,
    "title":"Waterloo Engineering 5, 10, 15, 20, 30, 35, 40, and 45 Alumni Reunion",
    "description":"This alumni reunion in 2014 is for the classes of 1969, 1974, 1979, 1984, 1994, 1999, 2004 and 2008. We hope that you will be able to attend your reunion to reconnect with your classmates, your professors, your Faculty, and your University.There are various events happening all weekend long including an open house, lectures, tours of campus, a football game and a brunch the following day, just to name a few.",
    "description_raw":"<p><img alt=\"Engineering yearbook and jacket\" class=\"image-sidebar-220px-wide image-right\" height=\"225\" src=\"\/engineering\/sites\/ca.engineering\/files\/styles\/sidebar-220px-wide\/public\/uploads\/images\/2012-5-45Reunion_1.jpg?itok=dVf-g3gA\" width=\"220\" \/>This alumni reunion in 2014 is for the classes of 1969, 1974, 1979, 1984, 1994, 1999, 2004 and 2008. We hope that you will be able to attend your reunion to reconnect with your classmates, your professors, your Faculty, and your University.<\/p>\n<p>There are various events happening all weekend long including an open house, lectures, tours of campus, a football game and a brunch the following day, just to name a few.<\/p>",
    "times":[
      {
        "start":"2014-09-27T04:00:00-04:00",
        "end":"2014-09-27T04:00:00-04:00",
        "start_day":"Saturday",
        "start_date":"2014-09-27",
        "start_time":"04:00:00",
        "end_day":"Saturday",
        "end_date":"2014-09-27",
        "end_time":"04:00:00"
      }
    ],
    "cost":null,
    "audience":[
      "Faculty",
      "Alumni"
    ],
    "tags":[
      
    ],
    "type":[
      "Reunion"
    ],
    "website":{
      "title":"More reunion information",
      "url":"http:\/\/uwaterloo.ca\/engineering\/alumni\/reunions\/5-10-15-20-30-35-40-and-45"
    },
    "host":{
      "title":"Waterloo Engineering Alumni Affairs",
      "url":"https:\/\/uwaterloo.ca\/engineering\/alumni-and-friends"
    },
    "image":{
      "id":1323,
      "file":"2012-5-45Reunion.jpg",
      "alt":"Engineering yearbook and jacket",
      "mime":"image\/jpeg",
      "size":1253260,
      "width":2764,
      "height":2824,
      "url":"https:\/\/uwaterloo.ca\/engineering\/sites\/ca.engineering\/files\/uploads\/images\/2012-5-45Reunion.jpg"
    },
    "location":{
      "id":90,
      "name":"University of Waterloo",
      "street":"200 University Avenue West",
      "additional":null,
      "city":"Waterloo",
      "province":"ON",
      "postal_code":"N2L 3G1",
      "country":"Canada",
      "latitude":null,
      "longitude":null
    },
    "site_name":"Engineering",
    "site_id":"engineering",
    "revision_id":14587,
    "link":"https:\/\/uwaterloo.ca\/engineering\/events\/waterloo-engineering-5-10-15-20-30-35-40-and-45-alumni",
    "link_calendar":"https:\/\/uwaterloo.ca\/engineering\/events\/ical\/1701\/calendar.ics",
    "updated":"2014-04-09T12:48:32-04:00"
  }
}
```


# Get FEDS Events for given id

```
GET /feds/events/{site}/{id}.{format}
```

## Description

> This method returns a specific event's information given the unique id

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
    <td>1733</td>
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
GET /feds/events/{site}/{id}.{format}
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
GET /feds/events/{site}/{id}.{format}
```

- **https://api.uwaterloo.ca/v2/feds/events/300787.json**
- **https://api.uwaterloo.ca/v2/feds/events/300787.xml**
- **https://api.uwaterloo.ca/v2/feds/events/300787.json?callback=myResponse**


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
    <td>list</td>
    <td>Audience targeted by event</td>
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
    "requests":811369,
    "timestamp":1453149868,
    "status":200,
    "message":"Request successful",
    "method_id":1733,
    "method":{
      
    }
  },
  "data":{
    "id":300787,
    "title":"MFE@UWaterloo",
    "location":null,
    "start":"2016-01-11T17:30:00-05:00",
    "end":"2016-01-11T19:00:00-05:00",
    "description":"The UW Economics Society presents MFE@UWaterloo. The Master of Financial Economics (MFE) is a non-thesis degree. Students follow a three-term, 16-month program, consisting of 12 one-term courses and a four-month summer internship between terms two and three. Students follow a core program which includes elective courses offered by the Department of Economics and the Rotman School of Management. The Program is designed to equip students with the tools and skills required for successful careers in the financial sector. In 2015, full time employment was 100% with top organizations such as Blackrock, Goldman Sachs, Bank of Canada, BMO, OTPP and much more. More information can be found at: https:\/\/www.economics.utoronto.ca\/index.php\/index\/mfe\/home Please join us for a infomation and networking session with program coordinator Ayeha Alli and current MFE students on January 11th, 2016 from 5:30pm to 7:00pm in RCH 309. Free pizza will be provided for all attendants during the networking session. Present your free eventbrite ticket at the sign in desk or signup at the entrance. This is a great opportunity to learn more about getting into finance and an opportunity to increase your chances of getting into the program!",
    "description_raw":"The UW Economics Society presents MFE@UWaterloo. The Master of Financial Economics (MFE) is a non-thesis degree. Students follow a three-term, 16-month program, consisting of 12 one-term courses and a four-month summer internship between terms two and three. Students follow a core program which includes elective courses offered by the Department of Economics and the Rotman School of Management. The Program is designed to equip students with the tools and skills required for successful careers in the financial sector. In 2015, full time employment was 100% with top organizations such as Blackrock, Goldman Sachs, Bank of Canada, BMO, OTPP and much more. More information can be found at: https:\/\/www.economics.utoronto.ca\/index.php\/index\/mfe\/home     Please join us for a infomation and networking session with program coordinator Ayeha Alli and current MFE students on January 11th, 2016 from 5:30pm to 7:00pm in RCH 309. Free pizza will be provided for all attendants during the networking session. Present your free eventbrite ticket at the sign in desk or signup at the entrance. This is a great opportunity to learn more about getting into finance and an opportunity to increase your chances of getting into the program!",
    "categories":[
      "Events"
    ],
    "updated":"2016-01-05T10:39:40-05:00",
    "url":"http:\/\/www.feds.ca\/event\/mfeuwaterloo\/"
  }
}
```


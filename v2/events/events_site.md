# Get Events for Site

```
GET /events/{site}.{format}
```

## Description

> This method returns a list of the upcoming site events given a site slug

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
    <td>1559</td>
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
GET /events/{site}.{format}
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
GET /events/{site}.{format}
```

- **https://api.uwaterloo.ca/v2/events/engineering.json**
- **https://api.uwaterloo.ca/v2/events/science.xml**
- **https://api.uwaterloo.ca/v2/events/engineering.json.json?callback=myResponse**


## Response

### meta
<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Full site name as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
</table>

### data
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
    <td>event title</td>
  </tr>
  <tr>
    <td><b>times</b></td>
    <td>array</td>
    <td>The outlet menu list<br><table>
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
    "requests":6988,
    "timestamp":1400035710,
    "status":200,
    "message":"Request successful",
    "method_id":1559,
    "method":{
      "site_name":"Engineering"
    }
  },
  "data":[
    {
      "id":1759,
      "title":"Chamath Palihapitiya: The Unconventional Venture Capitalist",
      "times":[
        {
          "start":"2014-05-09T15:30:00-04:00",
          "end":"2014-05-09T17:30:00-04:00"
        }
      ],
      "type":[
        "Information session"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/chamath-palihapitiya-unconventional-venture-capitalist",
      "updated":"2014-05-09T09:50:42-04:00"
    },
    {
      "id":1740,
      "title":"OCE Discovery Conference",
      "times":[
        {
          "start":"2014-05-12T04:00:00-04:00",
          "end":"2014-05-13T04:00:00-04:00"
        }
      ],
      "type":[
        "Conference",
        "Information session"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/oce-discovery-conference",
      "updated":"2014-04-24T11:52:52-04:00"
    },
    {
      "id":1748,
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
      "id":1736,
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
      "id":1739,
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
      "id":1738,
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
      "id":1699,
      "title":"Waterloo Engineering 50th Alumni Reunion",
      "times":[
        {
          "start":"2014-09-27T04:00:00-04:00",
          "end":"2014-09-27T04:00:00-04:00"
        }
      ],
      "type":[
        "Reunion"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/waterloo-engineering-50th-alumni-reunion",
      "updated":"2014-03-20T23:33:02-04:00"
    },
    {
      "id":1701,
      "title":"Waterloo Engineering 5, 10, 15, 20, 30, 35, 40, and 45 Alumni Reunion",
      "times":[
        {
          "start":"2014-09-27T04:00:00-04:00",
          "end":"2014-09-27T04:00:00-04:00"
        }
      ],
      "type":[
        "Reunion"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/waterloo-engineering-5-10-15-20-30-35-40-and-45-alumni",
      "updated":"2014-04-09T12:48:32-04:00"
    },
    {
      "id":1700,
      "title":"Waterloo Engineering 25th Alumni Reunion",
      "times":[
        {
          "start":"2014-09-27T04:00:00-04:00",
          "end":"2014-09-27T04:00:00-04:00"
        }
      ],
      "type":[
        "Reunion"
      ],
      "link":"https:\/\/uwaterloo.ca\/engineering\/events\/waterloo-engineering-25th-alumni-reunion",
      "updated":"2014-04-09T12:46:13-04:00"
    }
  ]
}
```


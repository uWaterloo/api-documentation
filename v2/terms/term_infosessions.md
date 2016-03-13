# Employer Info Sessions by Term

```
GET /terms/{term}/infosessions.{format}
```

## Description

> This method returns the schedule for employer information sessions of a given term

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
    <td>1489</td>
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
    <td>CECA</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Weekly</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/tree/master/EmployerInfoSessions


## Parameters

```
GET /terms/{term}/infosessions.{format}
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
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>The format of the output</td>
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
GET /terms/{term}/infosessions.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.json**
- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.xml**
- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>string</td>
    <td>Session ID</td>
  </tr>
  <tr>
    <td><b>employer</b></td>
    <td>string</td>
    <td>Name of the company/employer</td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>string</td>
    <td>Session date in yyyy/mm/dd format</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>Session start time in hh:mm 24 hour format</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>Session end time in hh:mm 24 hour format</td>
  </tr>
    <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Information about the session</td>
  </tr>
  <tr>
    <td><b>website</b></td>
    <td>string</td>
    <td>Employer's website</td>
  </tr>
  <tr>
    <td><b>building</b></td>
    <td>object</td>
    <td>
      Infosession location data<br>
      <table>
        <tr>
          <td><b>code</b></td>
          <td>string</td>
          <td>Building code</td>
        </tr>
        <tr>
          <td><b>name</b></td>
          <td>string</td>
          <td>Name of building</td>
        </tr>
        <tr>
          <td><b>room</b></td>
          <td>string</td>
          <td>Room within building</td>
        </tr>
        <tr>
          <td><b>latitude</b></td>
          <td>float</td>
          <td>Location latitude coordinate</td>
        </tr>
        <tr>
          <td><b>longitude</b></td>
          <td>float</td>
          <td>Location longitude coordinate</td>
        </tr>
        <tr>
          <td><b>map_url</b></td>
          <td>string</td>
          <td>URL to uwaterloo map with infosession location</td>
        </tr>
      </table>
    </td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>list</td>
    <td>List of intended programs for student audience</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>Link to CECA's schedule of the info session</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":31454,
    "timestamp":1456706180,
    "status":200,
    "message":"Request successful",
    "method_id":1129,
    "method":{
      
    }
  },
  "data":[
    {
      "id":3681,
      "employer":"Google",
      "date":"2016-01-05",
      "day":"January",
      "start_time":"17:00",
      "end_time":"19:00",
      "description":"Info session to discuss options at Google for majors outside of Computer Science.",
      "website":"http:\/\/www.google.com\/careers\/students",
      "building":{
        "code":"FED",
        "name":"Federation Hall",
        "room":"Main Hall",
        "latitude":43.4732,
        "longitude":-80.5485,
        "map_url":"https:\/\/uwaterloo.ca\/map\/FED?basemap=D#map=17\/43.4732\/-80.5485"
      },
      "audience":[
        "ENG - Computer",
        "ENG - Electrical",
        "ENG - Mechatronics",
        "ENG - Software",
        "ENG - System Design",
        "MATH - Combinatorics & Optimization",
        "MATH - Computer Science",
        "MATH - Pure Mathematics"
      ],
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id=3681"
    },
    {
      "id":3739,
      "employer":"Mattermost Inc.",
      "date":"2016-01-05",
      "day":"January",
      "start_time":"11:30",
      "end_time":"13:30",
      "description":"Mattermost, Inc. is Y Combinator-funded company behind Mattermost, an open source messaging platform available from http:\/\/mattermost.org. Here you'll write thoughtful, high-quality, open source code that's seen, used, shared and extended around the world.",
      "website":"mattermost.org",
      "building":{
        "code":"DC",
        "name":"William G. Davis Computer Research Centre",
        "room":"Corporate Lounge 1301",
        "latitude":43.4727,
        "longitude":-80.5421,
        "map_url":"https:\/\/uwaterloo.ca\/map\/DC?basemap=D#map=17\/43.4727\/-80.5421"
      },
      "audience":[
        "ENG - Computer",
        "ENG - Nanotechnology",
        "ENG - Software",
        "ENG - System Design",
        "MATH - Applied Mathematics",
        "MATH - Computer Science",
        "MATH - Information Technology Management",
        "MATH - Statistics"
      ],
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id=3739"
    },
    {
      "id":3758,
      "employer":"Deloitte",
      "date":"2016-01-05",
      "day":"January",
      "start_time":"19:30",
      "end_time":"21:30",
      "description":"Want to know what makes Deloitte different? Join us at our upcoming campus information session to learn more about our firm, our work and our culture. You'll have the opportunity to ask your most pressing questions and to meet professionals who were once in your shoes. Find out how to launch your career and why so many people come to Deloitte for the big opportunities, but stay for the people.",
      "website":"deloitte.ca\/campus",
      "building":{
        "code":"FED",
        "name":"Federation Hall",
        "room":"Columbia Room A & B",
        "latitude":43.4732,
        "longitude":-80.5485,
        "map_url":"https:\/\/uwaterloo.ca\/map\/FED?basemap=D#map=17\/43.4732\/-80.5485"
      },
      "audience":[
        "ENG - Computer",
        "ENG - Software",
        "ENG - System Design",
        "MATH - Computational Mathematics",
        "MATH - Computer Science",
        "MATH - Computing & Financial Management",
        "MATH - Financial Analysis & Risk Management",
        "MATH - Information Technology Management"
      ],
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id=3758"
    }
   ]
  }
```


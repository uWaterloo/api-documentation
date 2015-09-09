# List of coop infosessions

```
GET /resources/infosessions.{format}
```

## Description

> This method returns a list of campus employer infosessions

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
    <td>1129</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>resources</td>
    <td><b>Service ID</b></td>
    <td>229</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>CECS</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- This data is community curated on github
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/tree/master/EmployerInfoSession


## Parameters

```
GET /resources/infosessions.{format}
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
GET /resources/infosessions.{format}
```

- **https://api.uwaterloo.ca/v2/resources/infosessions.json**
- **https://api.uwaterloo.ca/v2/resources/infosessions.xml**
- **https://api.uwaterloo.ca/v2/resources/infosessions.json?callback=myResponse**


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
    <td>Session date</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>Session start time</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>Session end time</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Session campus location</td>
  </tr>
  <tr>
    <td><b>website</b></td>
    <td>string</td>
    <td>Employer's website</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>string</td>
    <td>Intended student audience</td>
  </tr>
  <tr>
    <td><b>programs</b></td>
    <td>string</td>
    <td>Intended programs for student audience</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Information about the session</td>
  </tr>
    <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>Link to CECA's schedule about the info session</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":148,
    "timestamp":1382028148,
    "status":200,
    "message":"Request successful",
    "method_id":1129,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "id":"2116",
      "employer":"Accenture (Registration Needed to Attend)",
      "date":"September 5, 2013",
      "start_time":"09:30 AM",
      "end_time":"1:00 PM",
      "location":"TBD",
      "website":"",
      "audience":"3rd and 4th year Students",
      "programs":"Mathematics, Engineering, Computer Science",
      "description":"This event will be a preface to the fall information session.  We are offering you an opportunity to connect one-on-one with a Technology Consulting Analyst and the Executive Sponsor of the campus recruitment program.  You are welcome to ask questions pertaining to careers at Accenture, the day in the life of a Consulting Analyst, how to best prepare for a career with us, and any other questions you may have. Please register for a 15 minute session by contacting Andrew Davidson at abdavidson@uwaterloo.ca.",
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id2116"
    },
    {
      "id":"2093",
      "employer":"McKinsey & Company",
      "date":"September 5, 2013",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"http:\/\/mckinsey.com\/careers",
      "audience":"Co-op and Graduating Students",
      "programs":"MASTERS - Management Sciences, MASTERS - Civil Engineering, Info Tech , Engineering, Business",
      "description":"",
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id2093"
    },
    {
      "id":"2082",
      "employer":"Hulu",
      "date":"September 9, 2013",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"http:\/\/www.hulu.com",
      "audience":"Co-op and Graduating Students",
      "programs":"Applied Mathematics, Computer Engineering, Computer Science, Software Engineering, Systems Design Engineering",
      "description":"",
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id2082"
    },
    {
      "id":"2107",
      "employer":"FreshBooks",
      "date":"September 9, 2013",
      "start_time":"3:00 PM",
      "end_time":"4:30 PM",
      "location":"TC 2218",
      "website":"http:\/\/freshbooks.com\/careers",
      "audience":"Co-op and Graduating Students",
      "programs":"Mathematics, Engineering",
      "description":"",
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id2107"
    },
    {
      "id":"2006",
      "employer":"Wal-mart",
      "date":"September 9, 2013",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"http:\/\/walmartoncampus.ca",
      "audience":"Graduating Students",
      "programs":"Accounting and Financial Management, Business, Financial Management",
      "description":"",
      "link":"http:\/\/www.ceca.uwaterloo.ca\/students\/hiresessions_details.php?id2006"
    }
  ]
}
```


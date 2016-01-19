# List all open opportunities for a given id

```
GET /opportunities/{site}/{id}.{format}
```

## Description

> This method returns a the job description for a given opportunity

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
    <td>1811</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>opportunities</td>
    <td><b>Service ID</b></td>
    <td>347</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Each individual site's data steward</td>
    <td><b>Data Type</b></td>
    <td>Direct DB Connection</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Realtime</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources



## Parameters

```
GET /opportunities/{site}/{id}.{format}
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
    <td><b>site</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Site ID</td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Job ID</td>
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
GET /opportunities/{site}/{id}.{format}
```

- **https://api.uwaterloo.ca/v2/opportunities/planning/455.json**
- **https://api.uwaterloo.ca/v2/opportunities/planning/455.xml**
- **https://api.uwaterloo.ca/v2/opportunities/planning/455.json?callback=myResponse**


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
    <td>Post id</td>
  </tr>
  <tr>
    <td><b>site_id</b></td>
    <td>string</td>
    <td>Site id</td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Site name</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Position title</td>
  </tr>
  <tr>
    <td><b>job_id</b></td>
    <td>string</td>
    <td>Job ID (currently not implemented)</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Position title</td>
  </tr>
  <tr>
    <td><b>pay</b></td>
    <td>string</td>
    <td>Pay amount</td>
  </tr>
  <tr>
    <td><b>pay_type</b></td>
    <td>string</td>
    <td>Type of pay (salary, hourly etc)</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Job Description</td>
  </tr>
  <tr>
    <td><b>department</b></td>
    <td>string</td>
    <td>Hiring department</td>
  </tr>
  <tr>
    <td><b>description_raw</b></td>
    <td>string</td>
    <td>Position description with HTML</td>
  </tr>
  <tr>
    <td><b>type</b></td>
    <td>string</td>
    <td>Position type (fulltime/paid/volunteer etc)</td>
  </tr>
  <tr>
    <td><b>application_deadline</b></td>
    <td>date</td>
    <td>Deadline to apply</td>
  </tr>
  <tr>
    <td><b>start_date</b></td>
    <td>date</td>
    <td>Job start date</td>
  </tr>
  <tr>
    <td><b>end_date</b></td>
    <td>date</td>
    <td>Job end date</td>
  </tr>
  <tr>
    <td><b>number_of_positions</b></td>
    <td>string</td>
    <td>Number of positions available</td>
  </tr>
  <tr>
    <td><b>application_link</b></td>
    <td>string</td>
    <td>Link to directly apply for the job</td>
  </tr>
  <tr>
    <td><b>reports_to</b></td>
    <td>string</td>
    <td>Employee's direct report</td>
  </tr>
  <tr>
    <td><b>published_by</b></td>
    <td>string</td>
    <td>Watiam id of the publisher</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>Post URL</td>
  </tr>
  <tr>
    <td><b>posted</b></td>
    <td>datetime</td>
    <td>Date posted</td>
  </tr>
  <tr>
    <td><b>revision_id</b></td>
    <td>integer</td>
    <td>Job description revision id</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>datetime</td>
    <td>Last updated</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811498,
    "timestamp":1453156018,
    "status":200,
    "message":"Request successful",
    "method_id":1847,
    "method":{
      
    }
  },
  "data":{
    "id":455,
    "site_id":"planning",
    "site_name":"School of Planning",
    "title":"Municipal Land-Use Planner",
    "job_id":null,
    "pay":"TBD",
    "pay_type":"Salary",
    "type":"Paid",
    "department":"School of Planning",
    "description":"Oldman River Regional Services Commission has a position open for a Municipal Land-Use Planner. Please link for full details.",
    "description_raw":"<p>Oldman River Regional Services Commission has a position open for a Municipal Land-Use Planner. Please link for full details.<\/p>",
    "application_deadline":null,
    "start_date":null,
    "end_date":null,
    "number_of_positions":"1",
    "application_link":"http:\/\/www.albertaplanners.com\/sites\/default\/files\/career_opportunities\/attachments\/ORRSCPlannerJobAd.pdf",
    "reports_to":null,
    "published_by":"ssolomon",
    "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/municipal-land-use-planner",
    "revision_id":2460,
    "posted":"2015-12-23T00:00:00-05:00",
    "updated":"2015-12-23T12:22:26-05:00"
  }
}
```


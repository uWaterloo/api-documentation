# List all open opportunities for a given site/department

```
GET /opportunities/{site}.{format}
```

## Description

> This method returns a list of all opportunities available on campus

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

- The returned items are all UW admistered opportunities
- Any value can be `null`


### Sources



## Parameters

```
GET /opportunities/{site}.{format}
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
GET /opportunities/{site}.{format}
```

- **https://api.uwaterloo.ca/v2/opportunities/planning.json**
- **https://api.uwaterloo.ca/v2/opportunities/planning.xml**
- **https://api.uwaterloo.ca/v2/opportunities/planning.json?callback=myResponse**


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
    <td><b>title</b></td>
    <td>string</td>
    <td>Position title</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Job Description</td>
  </tr>
  <tr>
    <td><b>type</b></td>
    <td>string</td>
    <td>Position type (fulltime/paid/volunteer etc)</td>
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
    "requests":811485,
    "timestamp":1453155351,
    "status":200,
    "message":"Request successful",
    "method_id":1811,
    "method":{
      
    }
  },
  "data":[
    {
      "id":455,
      "title":"Municipal Land-Use Planner",
      "description":"Oldman River Regional Services Commission has a position open for a Municipal Land-Use Planner. Please link for full details.",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/municipal-land-use-planner",
      "posted":"2015-12-23T00:00:00-05:00",
      "updated":"2015-12-23T12:22:26-05:00"
    },
    {
      "id":454,
      "title":"Land Use Planner - Junior Intermediate",
      "description":"Junior\/Intermediate Land Use Planner\n\tB&amp;A is seeking a Junior to Intermediate land use planner to provide assistance on a variety of projects primarily focused land development in Calgary and surrounding municipalities. Working closely with partners and senior planners, the successful candidate will interface with clients and municipal staff on a\n\tregular basis.\n\nQUALIFICATIONS\n\n\u00a0Bachelor\u2019s or Master\u2019s degree in Urban Planning with up to 4 years of experience. Recent graduates are encouraged to apply\n\tInterpersonal and verbal\/written communication skills and ability to maintain professional working relationships\n\tKnowledge of Word, Excel, PowerPoint and InDesign programs\n\t\u00a0Eligibility for APPI membership\nIf you feel you meet these qualifications and are interested in applying, please submit a comprehensive resume via mail or email to address below.\n\n\n\tVal Culp, Office Manager\n\tBrown &amp; Associates Planning Group\n\tSuite 600, 940 - 6th Avenue SW\n\tCalgary, AB T2P 3T1\n\tvculp@bapg.ca\n\tDeadline to submit application is January 4, 2016",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/land-use-planner-junior-intermediate",
      "posted":"2015-12-23T00:00:00-05:00",
      "updated":"2015-12-23T12:15:24-05:00"
    },
    {
      "id":450,
      "title":"Planner I",
      "description":"The City of Edmonton is hiring a planner to help with the West Rossdale \/ River Crossing initiative. This is a complex project that would be fascinating and professionally rewarding to work on. The successful applicant will be working with a project manager who would be an excellent mentor. While the posting, which is up on the City web site and which is copied below, talks about applicants needing two years of experience, the hiring manager is willing to consider people with no work experience provided they are bright and effective.\n\n1 temporary full-time position lasting up to 11 months\n\nHelp implement the West Rossdale Urban Design Plan and as part of this participate in developing the \u201cRiver Crossing Initiative!\u201d \u00a0Take the challenge to nurture and maintain working relationships dealing with land planning and project development while advancing the interests of Edmonton.\u00a0 Consider this opportunity to showcase your professional planning expertise and relationship building skills in land use\/municipal planning as a Planner I with the Strategic Project Section of the Urban Planning and Environment Branch.\n\nWork closely with other planners in the section, other City Departments, and outside consultants to develop and implement the West Rossdale Urban Design Plan, River Crossing Initiatives, and support implementation of the River Valley Alliance Projects\n\tFormulate professional recommendations in dealing with land development activities\n\tProvide administrative and strategic support and advice in land, infrastructure, and planning policies associated with project implementation\n\tAdminister research or information searches related to land planning and development\n\tPrepare presentations for public meetings, council reports, and other clients and participate in the public engagement process\nQualifications\n\nBachelor degree in Urban Planning or a related field. Master\u2019s degree preferred\n\tMinimum 2 years planning experience, including working with high-profile, complex land development projects. \u00a0Those with less experience may be considered at the Opportunity Concept level\n\tExperience working with Aboriginal communities with a demonstrated ability to understand related cultural sensitivities\n\tExperience in public engagement, facilitation, and meeting management\n\tCanadian Institute of Planners (CIP) or Alberta Professional Planning Institute (APPI) membership is an asset\n\tStrong ability to focus on customer, stakeholder, and client needs based in creative problem solving\n\tValid Alberta Class 5 driver's licence (or provincial equivalent).\u00a0Obtaining and maintaining a City Driver's permit is a requirement of this position\nHours of Work:\u00a033.75 hours per week, Monday - Friday\n\nSalary:\u00a0$42.050 - $53.134 (Hourly). \u00a0Opportunity Concept:\u00a0$30.917 - $40.260 (Hourly)\n\nRecruitment Consultant:\u00a0CM\/JP",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/planner-i",
      "posted":"2015-11-16T00:00:00-05:00",
      "updated":"2015-11-23T13:43:10-05:00"
    }
  ]
}
```


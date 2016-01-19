# List all open opportunities on campus

```
GET /opportunities.{format}
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
    <td>1861</td>
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
GET /opportunities.{format}
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
GET /opportunities.{format}
```

- **https://api.uwaterloo.ca/v2/opportunities.json**
- **https://api.uwaterloo.ca/v2/opportunities.xml**
- **https://api.uwaterloo.ca/v2/opportunities.json?callback=myResponse**


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
    <td><b>site</b></td>
    <td>string</td>
    <td>Site/department/faculty name</td>
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
    "requests":811483,
    "timestamp":1453155251,
    "status":200,
    "message":"Request successful",
    "method_id":1861,
    "method":{
      
    }
  },
  "data":[
    {
      "id":455,
      "title":"Municipal Land-Use Planner",
      "site":"planning",
      "description":"Oldman River Regional Services Commission has a position open for a Municipal Land-Use Planner. Please link for full details.",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/municipal-land-use-planner",
      "posted":"2015-12-23T00:00:00-05:00",
      "updated":"2015-12-23T12:22:26-05:00"
    },
    {
      "id":454,
      "title":"Land Use Planner - Junior Intermediate",
      "site":"planning",
      "description":"Junior\/Intermediate Land Use Planner\n\tB&amp;A is seeking a Junior to Intermediate land use planner to provide assistance on a variety of projects primarily focused land development in Calgary and surrounding municipalities. Working closely with partners and senior planners, the successful candidate will interface with clients and municipal staff on a\n\tregular basis.\n\nQUALIFICATIONS\n\n\u00a0Bachelor\u2019s or Master\u2019s degree in Urban Planning with up to 4 years of experience. Recent graduates are encouraged to apply\n\tInterpersonal and verbal\/written communication skills and ability to maintain professional working relationships\n\tKnowledge of Word, Excel, PowerPoint and InDesign programs\n\t\u00a0Eligibility for APPI membership\nIf you feel you meet these qualifications and are interested in applying, please submit a comprehensive resume via mail or email to address below.\n\n\n\tVal Culp, Office Manager\n\tBrown &amp; Associates Planning Group\n\tSuite 600, 940 - 6th Avenue SW\n\tCalgary, AB T2P 3T1\n\tvculp@bapg.ca\n\tDeadline to submit application is January 4, 2016",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/land-use-planner-junior-intermediate",
      "posted":"2015-12-23T00:00:00-05:00",
      "updated":"2015-12-23T12:15:24-05:00"
    },
    {
      "id":244,
      "title":"AccessAbility Services Student Access Van Drivers",
      "site":"disability-services",
      "description":"Student Access Van\u00a0drivers are current University of Waterloo students who are hired to safely pick up and drop off student passengers, registered with AccessAbility Services at appropriate campus buildings and\/or departments. Occasionally, drivers may provide assistance with loading or unloading passengers.\u00a0Student Access\u00a0Van\u00a0drivers must have a valid, point free, Ontario driver\u2019s license. The overall objective of the position is to provide safe, reliable, and organized transportation services to students registered with AccessAbility Services.\n\t\u00a0\n\nResponsibilities\n\nAbility to safely operate a vehicle and adhere to Ontario Driving Regulations.\n\tWork closely with the Student Access Van coordinator, who oversees scheduling and operational management of the Student Access Van.\n\tMaintain driving logs, complete daily vehicle inspections, and report malfunctions immediately to the Student Access Van coordinator.\n\tAbility to provide professional and positive customer service and maintain respectful interactions with AccessAbility staff, coordinator, and students utilizing the service.\n\tUnderstand, follow, and execute verbal and\/or written instructions from the Student Access Van coordinator.\n\tRead and write in English, to help maintain daily route schedules and\/or records.\n\tMaintain a confidential environment.\nRequirements\n\nPossess a class \u201cG\u201d driver\u2019s license valid in the Province of Ontario with a point-free driving record. Interested candidates must bring a copy of their Ontario driving record to the interview. This can be obtained at your nearest Service Ontario.\n\tA Police Records Check is mandatory.\n\tPunctual, reliable, and able to demonstrate a professional attitude.\n\tKnowledge of University of Waterloo campus buildings and roadways.\n\tMust adhere to safety procedures, and Ontario Driving regulations.\n\tAble to work a flexible schedule, including morning, afternoon and evening shifts; Occasional weekend work may be required (i.e., during exams).\n\tA commitment of approximately 10\u00a0hours a week is required.",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/disability-services\/opportunities\/accessability-services-student-access-van-drivers",
      "posted":"2015-08-07T00:00:00-04:00",
      "updated":"2015-11-30T15:21:55-05:00"
    },
    {
      "id":951,
      "title":"Fun Police",
      "site":"math",
      "description":"Be a member of the fun police - it's a lot of fun!",
      "type":"Volunteer",
      "link":"https:\/\/uwaterloo.ca\/math\/opportunities\/fun-police",
      "posted":"2015-11-27T00:00:00-05:00",
      "updated":"2015-11-27T14:46:25-05:00"
    },
    {
      "id":450,
      "title":"Planner I",
      "site":"planning",
      "description":"The City of Edmonton is hiring a planner to help with the West Rossdale \/ River Crossing initiative. This is a complex project that would be fascinating and professionally rewarding to work on. The successful applicant will be working with a project manager who would be an excellent mentor. While the posting, which is up on the City web site and which is copied below, talks about applicants needing two years of experience, the hiring manager is willing to consider people with no work experience provided they are bright and effective.\n\n1 temporary full-time position lasting up to 11 months\n\nHelp implement the West Rossdale Urban Design Plan and as part of this participate in developing the \u201cRiver Crossing Initiative!\u201d \u00a0Take the challenge to nurture and maintain working relationships dealing with land planning and project development while advancing the interests of Edmonton.\u00a0 Consider this opportunity to showcase your professional planning expertise and relationship building skills in land use\/municipal planning as a Planner I with the Strategic Project Section of the Urban Planning and Environment Branch.\n\nWork closely with other planners in the section, other City Departments, and outside consultants to develop and implement the West Rossdale Urban Design Plan, River Crossing Initiatives, and support implementation of the River Valley Alliance Projects\n\tFormulate professional recommendations in dealing with land development activities\n\tProvide administrative and strategic support and advice in land, infrastructure, and planning policies associated with project implementation\n\tAdminister research or information searches related to land planning and development\n\tPrepare presentations for public meetings, council reports, and other clients and participate in the public engagement process\nQualifications\n\nBachelor degree in Urban Planning or a related field. Master\u2019s degree preferred\n\tMinimum 2 years planning experience, including working with high-profile, complex land development projects. \u00a0Those with less experience may be considered at the Opportunity Concept level\n\tExperience working with Aboriginal communities with a demonstrated ability to understand related cultural sensitivities\n\tExperience in public engagement, facilitation, and meeting management\n\tCanadian Institute of Planners (CIP) or Alberta Professional Planning Institute (APPI) membership is an asset\n\tStrong ability to focus on customer, stakeholder, and client needs based in creative problem solving\n\tValid Alberta Class 5 driver's licence (or provincial equivalent).\u00a0Obtaining and maintaining a City Driver's permit is a requirement of this position\nHours of Work:\u00a033.75 hours per week, Monday - Friday\n\nSalary:\u00a0$42.050 - $53.134 (Hourly). \u00a0Opportunity Concept:\u00a0$30.917 - $40.260 (Hourly)\n\nRecruitment Consultant:\u00a0CM\/JP",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/planning\/opportunities\/planner-i",
      "posted":"2015-11-16T00:00:00-05:00",
      "updated":"2015-11-23T13:43:10-05:00"
    },
    {
      "id":239,
      "title":"Volunteer Note-Taker",
      "site":"disability-services",
      "description":"AccessAbility Services\u00a0is looking for volunteer note-takers who are willing to share their class notes. In being a volunteer note-taker, you can contribute to academic success and make a difference in the lives of your fellow peers.\n\t\tThe volunteer note-taking position is a one term commitment (i.e., fall term, winter term, or spring term).\n\n\n\n\tAs a volunteer note taker, your\u00a0course notes will only be shared with students registered with AccessAbility Services, who have a documented disability and who have been approved for note-taking services by an AccessAbility Services advisor.\u00a0Volunteers can request to be removed from the program at any time. If you make changes to\u00a0your academic schedule (i.e., dropping a course), please notify AccessAbility Services of the change.\n\n\tInterested applicants, please complete the on-line note taker application form.\n\t\t\u00a0",
      "type":"Volunteer",
      "link":"https:\/\/uwaterloo.ca\/disability-services\/opportunities\/volunteer-note-taker",
      "posted":"2015-08-06T00:00:00-04:00",
      "updated":"2015-11-03T16:57:45-05:00"
    },
    {
      "id":538,
      "title":"Fall Open House volunteers",
      "site":"find-out-more",
      "description":"Volunteer at Fall Open House and share your Warrior pride with future Waterloo students and their families.\n\nWe are looking for more than 60 volunteers so be sure to submit your information today!",
      "type":"Volunteer",
      "link":"https:\/\/uwaterloo.ca\/find-out-more\/opportunities\/fall-open-house-volunteers",
      "posted":"2015-10-26T00:00:00-04:00",
      "updated":"2015-10-26T16:17:23-04:00"
    },
    {
      "id":243,
      "title":"AccessAbility Services Student Access Van Coordinator",
      "site":"disability-services",
      "description":"The incumbent is responsible for the day-to-day operations of the Student Access Van, operated and affiliated with the department of AccessAbility Services at the University of Waterloo. The Student Access Van is available for use by students registered with AccessAbility Services and for campus visitors. The overall objective of the position is to work closely and support AccessAbility Services and its students.\n\t\u00a0\n\nResponsibilities\n\nOversee and manage the Student Access Van drivers, who assist with campus transportation for students with accessibility needs.\n\tAccountable for scheduling the Student Access Van drivers (i.e., submitting driver hours, creating and distributing work schedules), and the operational management of the Student Access Van: scheduling and assigning students.\n\tMaintain proper communication with drivers, students, and staff at AccessAbility Services.\n\tPrimary contact for the Student Access Van drivers and students utilizing the service.\n\tLiaising with the AccessAbility office to coordinate services for newly registered students requiring the service.\n\tMaintain driving logs, complete vehicle inspections, and complete daily paperwork.\n\tCarrying out routine duties in an informed manner with minimal supervision.\n\tProviding friendly and positive customer service and maintaining respectful interactions with staff and students.\n\tAbility to understand, follow, and execute verbal and\/or written instructions from AccessAbility Service Coordinator.\n\tProvide coverage for vacation and other absences for the Student Access Van drivers, and assistance when required.\nRequirements\n\nCurrent University of Waterloo student or recent University of Waterloo graduate (within one year).\n\tPossess a class \u201cG\u201d driver\u2019s license valid in the Province of Ontario with a point-free driving record. Interested candidates must bring a copy of their Ontario driving record to the interview. This can be obtained at your nearest Service Ontario.\n\tA Police Records Check is mandatory.\n\tKnowledge of University of Waterloo campus buildings and roadways.\n\tAble to work a flexible schedule, including morning, afternoon and evening shifts; Occasional weekend work may be required (i.e., during exams).\n\tEffective listening, time management and organizational skills.\n\tExcellent problem solving abilities and good judgment.\n\t\t\u00a0",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/disability-services\/opportunities\/accessability-services-student-access-van-coordinator",
      "posted":"2015-08-07T00:00:00-04:00",
      "updated":"2015-09-11T11:00:57-04:00"
    },
    {
      "id":240,
      "title":"Tutor\/Editor Paid Position",
      "site":"disability-services",
      "description":"Share your passion for academic success, and register to become a tutor and\/or editor for students registered with AccessAbility Services.\n\nTutors and editors must be current UWaterloo students who have completed and received a grade of 70% or higher (or equivalent credentials) in the course(s) in which they are interested in tutoring and\/or editing.\u00a0Tutors\/Editors must include in their application an unofficial transcript.\n\nInterested applicants, please complete the on-line tutor\/editor application form.\u00a0",
      "type":"Paid",
      "link":"https:\/\/uwaterloo.ca\/disability-services\/opportunities\/tutoreditor-paid-position",
      "posted":"2015-08-06T00:00:00-04:00",
      "updated":"2015-08-19T08:46:16-04:00"
    }
  ]
}
```


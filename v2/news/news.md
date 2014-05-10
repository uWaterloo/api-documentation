# Get News from All Sites

```
GET /news.{format}
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
    <td>1697</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>news</td>
    <td><b>Service ID</b></td>
    <td>307</td>
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

- This is a 'realtime' feed. An item will be available on the api the second it is up using Webhooks
- Any value can be `null`


### Sources

- Crawled from all WMCS sites listed at https://api.uwaterloo.ca/v2/resources/sites.{format}


## Parameters

```
GET /news.{format}
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
GET /news.{format}
```

- **https://api.uwaterloo.ca/v2/news.json**
- **https://api.uwaterloo.ca/v2/news.xml**
- **https://api.uwaterloo.ca/v2/news.json?callback=myResponse**


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
    <td>Unique news id</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>News story title</td>
  </tr>
  <tr>
    <td><b>site</b></td>
    <td>string</td>
    <td>News site slug</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>URL of news link</td>
  </tr>
  <tr>
    <td><b>published</b></td>
    <td>date</td>
    <td>ISO 8601 formatted publish date</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>date</td>
    <td>ISO 8601 formatted update date</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":486,
    "timestamp":1399701919,
    "status":200,
    "message":"Request successful",
    "method_id":1697,
    "method":{
      
    }
  },
  "data":[
    {
      "id":9,
      "title":"Recruiting graduate students",
      "site":"wu-research-group",
      "link":"https:\/\/uwaterloo.ca\/wu-research-group\/news\/recruiting-graduate-students",
      "published":"2012-10-22T00:00:00-04:00",
      "updated":"2014-05-09T14:57:28-04:00"
    },
    {
      "id":702,
      "title":"Do you see what I see? The new frontier of astronomy",
      "site":"physics-astronomy",
      "link":"https:\/\/uwaterloo.ca\/physics-astronomy\/news\/do-you-see-what-i-see-new-frontier-astronomy",
      "published":"2014-05-09T00:00:00-04:00",
      "updated":"2014-05-09T13:52:54-04:00"
    },
    {
      "id":881,
      "title":"Do you see what I see? The new frontier of astronomy",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/do-you-see-what-i-see-new-frontier-astronomy",
      "published":"2014-05-09T00:00:00-04:00",
      "updated":"2014-05-09T13:51:36-04:00"
    },
    {
      "id":701,
      "title":"Minds in motion",
      "site":"physics-astronomy",
      "link":"https:\/\/uwaterloo.ca\/physics-astronomy\/news\/minds-motion",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-09T12:13:04-04:00"
    },
    {
      "id":878,
      "title":"Biology alumnus wins Jeopardy!",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/biology-alumnus-wins-jeopardy",
      "published":"2014-05-08T00:00:00-04:00",
      "updated":"2014-05-09T11:55:26-04:00"
    },
    {
      "id":30,
      "title":"GH Staff Team Meeting",
      "site":"graduate-house",
      "link":"https:\/\/uwaterloo.ca\/graduate-house\/news\/gh-staff-team-meeting",
      "published":"2014-01-13T00:00:00-05:00",
      "updated":"2014-05-09T11:39:10-04:00"
    },
    {
      "id":72,
      "title":"How Harper government funding cuts affect science research in Waterloo Region",
      "site":"science-technology-society",
      "link":"https:\/\/uwaterloo.ca\/science-technology-society\/news\/how-harper-government-funding-cuts-affect-science-research",
      "published":"2014-05-09T00:00:00-04:00",
      "updated":"2014-05-09T11:13:18-04:00"
    },
    {
      "id":1505,
      "title":"Mental health screening tool to be used by all frontline OPP officers",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/mental-health-screening-tool-be-used-all-frontline-opp",
      "published":"2014-05-08T00:00:00-04:00",
      "updated":"2014-05-08T17:00:31-04:00"
    },
    {
      "id":880,
      "title":"Water Institute Symposium 2014: The Future of Groundwater Research",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/water-institute-symposium-2014-future-groundwater-research",
      "published":"2014-05-08T00:00:00-04:00",
      "updated":"2014-05-08T16:10:10-04:00"
    },
    {
      "id":137,
      "title":"MPS students find success at Canadian Heritage",
      "site":"master-of-public-service",
      "link":"https:\/\/uwaterloo.ca\/master-of-public-service\/news\/mps-students-find-success-canadian-heritage",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-08T13:25:28-04:00"
    },
    {
      "id":1124,
      "title":"Congratulations!",
      "site":"earth-environmental-sciences",
      "link":"https:\/\/uwaterloo.ca\/earth-environmental-sciences\/news\/congratulations-2",
      "published":"2014-05-08T00:00:00-04:00",
      "updated":"2014-05-08T12:54:37-04:00"
    },
    {
      "id":307,
      "title":"Teaching undergraduates to examine the science-society interface",
      "site":"arts",
      "link":"https:\/\/uwaterloo.ca\/arts\/news\/teaching-undergraduates-examine-science-society-interface",
      "published":"2012-11-28T00:00:00-05:00",
      "updated":"2014-05-08T12:44:09-04:00"
    },
    {
      "id":500,
      "title":"Hippocampal sparing Alzheimer&#039;s disease misdiagnosed",
      "site":"murray-alzheimer-research-and-education-program",
      "link":"https:\/\/uwaterloo.ca\/murray-alzheimer-research-and-education-program\/news\/hippocampal-sparing-alzheimers-disease-misdiagnosed",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-08T11:12:03-04:00"
    },
    {
      "id":1760,
      "title":"ECE team advances in challenge to design the car of the future",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/ece-team-advances-challenge-design-car-future",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-07T16:22:48-04:00"
    },
    {
      "id":1756,
      "title":"Grad student wins hydrotechnical engineering award",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/grad-student-wins-hydrotechnical-engineering-award",
      "published":"2014-05-05T00:00:00-04:00",
      "updated":"2014-05-07T15:39:20-04:00"
    },
    {
      "id":877,
      "title":"Water Institute Symposium 2014: Tracking Microbial Communities of the Grand River Watershed",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/water-institute-symposium-2014-tracking-microbial",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-07T15:20:43-04:00"
    },
    {
      "id":925,
      "title":"Water Institute Symposium 2014: Tracking Microbial Communities of the Grand River Watershed",
      "site":"biology",
      "link":"https:\/\/uwaterloo.ca\/biology\/news\/water-institute-symposium-2014-tracking-microbial",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-07T15:19:48-04:00"
    },
    {
      "id":864,
      "title":"Water Institute Symposium 2014: Future challenges for the Great Lakes",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/water-institute-symposium-2014-future-challenges-great-lakes",
      "published":"2014-05-04T00:00:00-04:00",
      "updated":"2014-05-07T15:08:16-04:00"
    },
    {
      "id":1502,
      "title":"OPP to announce tool developed at Waterloo will be used by frontline officers",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/opp-announce-tool-developed-waterloo-will-be-used-frontline",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-07T12:32:32-04:00"
    },
    {
      "id":544,
      "title":"Fellowship Awarded to IQC Professor Andris Ambainis",
      "site":"institute-for-quantum-computing",
      "link":"https:\/\/uwaterloo.ca\/institute-for-quantum-computing\/news\/fellowship-awarded-iqc-professor-andris-ambainis",
      "published":"2008-02-24T19:00:00-05:00",
      "updated":"2014-05-07T12:28:41-04:00"
    },
    {
      "id":1501,
      "title":"Play shows dementia diagnosis in a new light",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/play-shows-dementia-diagnosis-new-light",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-07T12:04:59-04:00"
    },
    {
      "id":166,
      "title":"&quot;You Are Not a Banana&quot; Now Available on Desura",
      "site":"games-institute",
      "link":"https:\/\/uwaterloo.ca\/games-institute\/news\/you-are-not-banana-now-available-desura",
      "published":"2014-05-06T00:00:00-04:00",
      "updated":"2014-05-06T16:59:53-04:00"
    },
    {
      "id":355,
      "title":"Drama faculty member, Award Recipient",
      "site":"drama-speech-communication",
      "link":"https:\/\/uwaterloo.ca\/drama-speech-communication\/news\/drama-faculty-member-award-recipient",
      "published":"2014-05-06T00:00:00-04:00",
      "updated":"2014-05-06T14:23:57-04:00"
    },
    {
      "id":160,
      "title":"John Paul Lederach will recieve Grebel&#039;s first honorary doctorate",
      "site":"peace-conflict-studies",
      "link":"https:\/\/uwaterloo.ca\/peace-conflict-studies\/news\/john-paul-lederach-will-recieve-grebels-first-honorary",
      "published":"2014-03-18T00:00:00-04:00",
      "updated":"2014-05-06T09:33:46-04:00"
    },
    {
      "id":374,
      "title":"Brain, Chain, Gain with Margret Walton-Roberts",
      "site":"school-environment-enterprise-development",
      "link":"https:\/\/uwaterloo.ca\/school-environment-enterprise-development\/news\/brain-chain-gain-margret-walton-roberts",
      "published":"2014-05-04T20:00:00-04:00",
      "updated":"2014-05-06T08:17:41-04:00"
    },
    {
      "id":581,
      "title":"New faculty member: Dr. Ben Thompson",
      "site":"optometry-vision-science",
      "link":"https:\/\/uwaterloo.ca\/optometry-vision-science\/news\/new-faculty-member-dr-ben-thompson",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-05T13:25:42-04:00"
    },
    {
      "id":2205,
      "title":"E-classroom podium access for the spring term",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/e-classroom-podium-access-for-spring-term",
      "published":"2014-05-05T00:00:00-04:00",
      "updated":"2014-05-05T11:25:53-04:00"
    },
    {
      "id":2207,
      "title":"LEARN unavailable - May 11",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/learn-unavailable-may-11",
      "published":"2014-05-05T00:00:00-04:00",
      "updated":"2014-05-05T11:23:45-04:00"
    },
    {
      "id":1755,
      "title":"You charge your phone. Are you ready to charge your car?",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/you-charge-your-phone-are-you-ready-charge-your-car",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-05T11:20:27-04:00"
    },
    {
      "id":387,
      "title":"Why traffic congestion is driving Toronto crazy (The Globe and Mail)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/why-traffic-congestion-driving-toronto-crazy-globe-and-mail",
      "published":"2014-05-03T00:00:00-04:00",
      "updated":"2014-05-05T11:20:04-04:00"
    },
    {
      "id":2206,
      "title":"Exchange Server Maintenance - May 5-May 14",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/exchange-server-maintenance-may-5-may-14",
      "published":"2014-05-05T00:00:00-04:00",
      "updated":"2014-05-05T11:07:26-04:00"
    },
    {
      "id":471,
      "title":"Cory Scurr wins People&#039;s Choice Award at Ontario 3MT Competition",
      "site":"history",
      "link":"https:\/\/uwaterloo.ca\/history\/news\/cory-scurr-wins-peoples-choice-award-ontario-3mt-competition",
      "published":"2014-05-04T00:00:00-04:00",
      "updated":"2014-05-05T09:05:10-04:00"
    },
    {
      "id":472,
      "title":"Susan Roy wins prestigious Early Research Award",
      "site":"history",
      "link":"https:\/\/uwaterloo.ca\/history\/news\/susan-roy-wins-prestigious-early-research-award",
      "published":"2014-05-04T00:00:00-04:00",
      "updated":"2014-05-04T17:19:37-04:00"
    },
    {
      "id":923,
      "title":"Water Institute Symposium 2014: Future challenges for the Great Lakes",
      "site":"biology",
      "link":"https:\/\/uwaterloo.ca\/biology\/news\/water-institute-symposium-2014-future-challenges-great-lakes",
      "published":"2014-05-04T00:00:00-04:00",
      "updated":"2014-05-04T08:17:17-04:00"
    },
    {
      "id":70,
      "title":"E-Waste Report 2014",
      "site":"central-stores",
      "link":"https:\/\/uwaterloo.ca\/central-stores\/news\/e-waste-report-2014",
      "published":"2014-01-24T00:00:00-05:00",
      "updated":"2014-05-02T13:23:27-04:00"
    },
    {
      "id":2200,
      "title":"Microsoft Internet Explorer critical security flaw",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/microsoft-internet-explorer-critical-security-flaw",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-05-02T13:21:39-04:00"
    },
    {
      "id":2204,
      "title":"Update - Microsoft Internet Explorer critical security flaw",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/update-microsoft-internet-explorer-critical-security-flaw",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-02T13:19:06-04:00"
    },
    {
      "id":2203,
      "title":"Internet Explorer patch to fix critical security flaw \u2013 May 1",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/internet-explorer-patch-fix-critical-security-flaw-may-1",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-02T12:36:42-04:00"
    },
    {
      "id":791,
      "title":"Get ready to plug in your car",
      "site":"research",
      "link":"https:\/\/uwaterloo.ca\/research\/news\/get-ready-plug-your-car",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-02T11:42:18-04:00"
    },
    {
      "id":1481,
      "title":"You charge your phone - are you ready to charge your car?",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/you-charge-your-phone-are-you-ready-charge-your-car",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-02T09:44:35-04:00"
    },
    {
      "id":790,
      "title":"$25 million allotted to Waterloo\u2019s IQC over five years",
      "site":"research",
      "link":"https:\/\/uwaterloo.ca\/research\/news\/25-million-allotted-waterloos-iqc-over-five-years",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-02T09:29:56-04:00"
    },
    {
      "id":681,
      "title":"SAE Baja Competition",
      "site":"mechanical-mechatronics-engineering",
      "link":"https:\/\/uwaterloo.ca\/mechanical-mechatronics-engineering\/news\/sae-baja-competition",
      "published":"2014-05-02T00:00:00-04:00",
      "updated":"2014-05-02T09:03:51-04:00"
    },
    {
      "id":580,
      "title":"Researchers link age, health and antidepressant use with eye disorders",
      "site":"optometry-vision-science",
      "link":"https:\/\/uwaterloo.ca\/optometry-vision-science\/news\/researchers-link-age-health-and-antidepressant-use-eye",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T17:36:11-04:00"
    },
    {
      "id":863,
      "title":"Researchers link age, general health and antidepressant use with eye disorders",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/researchers-link-age-general-health-and-antidepressant-use",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T16:51:50-04:00"
    },
    {
      "id":837,
      "title":"Pharmacy students invest in their future",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/pharmacy-students-invest-their-future",
      "published":"2014-03-20T00:00:00-04:00",
      "updated":"2014-05-01T16:47:25-04:00"
    },
    {
      "id":853,
      "title":"Grand River watershed could be showcase for smart water management",
      "site":"science",
      "link":"https:\/\/uwaterloo.ca\/science\/news\/grand-river-watershed-could-be-showcase-smart-water",
      "published":"2014-04-11T00:00:00-04:00",
      "updated":"2014-05-01T16:37:06-04:00"
    },
    {
      "id":1368,
      "title":"Ontario budget supports quantum research at Waterloo",
      "site":"institute-for-quantum-computing",
      "link":"https:\/\/uwaterloo.ca\/institute-for-quantum-computing\/news\/ontario-budget-supports-quantum-research-waterloo",
      "published":"2014-04-30T20:00:00-04:00",
      "updated":"2014-05-01T16:31:59-04:00"
    },
    {
      "id":1482,
      "title":"Ontario budget supports quantum research at Waterloo",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/ontario-budget-supports-quantum-research-waterloo",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T16:26:41-04:00"
    },
    {
      "id":519,
      "title":"New 3D tech offers unique multi-tasking",
      "site":"mechanical-mechatronics-engineering",
      "link":"https:\/\/uwaterloo.ca\/mechanical-mechatronics-engineering\/news\/new-3d-tech-offers-unique-multi-tasking",
      "published":"2014-02-18T00:00:00-05:00",
      "updated":"2014-05-01T16:18:29-04:00"
    },
    {
      "id":678,
      "title":"Global entrepreneurs: the Waterloo-China connection",
      "site":"mechanical-mechatronics-engineering",
      "link":"https:\/\/uwaterloo.ca\/mechanical-mechatronics-engineering\/news\/global-entrepreneurs-waterloo-china-connection",
      "published":"2014-04-22T00:00:00-04:00",
      "updated":"2014-05-01T16:10:04-04:00"
    },
    {
      "id":386,
      "title":"Ontario Well-being Study Yields Contradictory Results (Epoch Times)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/ontario-well-being-study-yields-contradictory-results-epoch",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-05-01T16:04:58-04:00"
    },
    {
      "id":680,
      "title":"Engineering student one of Maclean&#039;s Future leaders under 25",
      "site":"mechanical-mechatronics-engineering",
      "link":"https:\/\/uwaterloo.ca\/mechanical-mechatronics-engineering\/news\/engineering-student-one-macleans-future-leaders-under-25",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T16:01:37-04:00"
    },
    {
      "id":789,
      "title":"Eye disorders linked to age, health, and antidepressant use",
      "site":"research",
      "link":"https:\/\/uwaterloo.ca\/research\/news\/eye-disorders-linked-age-health-and-antidepressant-use",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T14:54:07-04:00"
    },
    {
      "id":143,
      "title":"MPS team project published in international book",
      "site":"master-of-public-service",
      "link":"https:\/\/uwaterloo.ca\/master-of-public-service\/news\/mtp-published",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T14:53:28-04:00"
    },
    {
      "id":788,
      "title":"New Ontario index puts wellbeing at the forefront",
      "site":"research",
      "link":"https:\/\/uwaterloo.ca\/research\/news\/new-ontario-index-puts-wellbeing-forefront",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T14:53:04-04:00"
    },
    {
      "id":1476,
      "title":"Researchers link age, health and antidepressant use with eye disorders",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/researchers-link-age-health-and-antidepressant-use-eye",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T11:21:25-04:00"
    },
    {
      "id":112,
      "title":"Spring research skills workshops",
      "site":"library\/news",
      "link":"https:\/\/uwaterloo.ca\/library\/news\/news\/spring-research-skills-workshops",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T10:48:36-04:00"
    },
    {
      "id":2202,
      "title":"Skills for the Electronic Workplace (SEW) May-June courses",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/skills-electronic-workplace-sew-may-june-courses",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-01T09:03:36-04:00"
    },
    {
      "id":385,
      "title":"CBC Lang and O&#039;Leary Exchange co-host Amanda Lang speaks to CIW Director about latest report findings",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/cbc-lang-and-oleary-exchange-co-host-amanda-lang-speaks-ciw",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-30T14:29:03-04:00"
    },
    {
      "id":376,
      "title":"CBC Metro Morning&#039;s Matt Galloway speaks to CIW Director about latest report findings",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/cbc-metro-mornings-matt-galloway-speaks-ciw-director-about",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-30T14:27:25-04:00"
    },
    {
      "id":512,
      "title":"Professor Emeritus Tony Cullen awarded a Life Fellowship Award from the American Academy of Optometry",
      "site":"optometry-vision-science",
      "link":"https:\/\/uwaterloo.ca\/optometry-vision-science\/news\/professor-emeritus-tony-cullen-awarded-life-fellowship-award",
      "published":"2013-10-01T00:00:00-04:00",
      "updated":"2014-04-30T13:04:00-04:00"
    },
    {
      "id":500,
      "title":"George Woo honoured with Essilor Award for Outstanding International Contributions in Optometry",
      "site":"optometry-vision-science",
      "link":"https:\/\/uwaterloo.ca\/optometry-vision-science\/news\/george-woo-honoured-essilor-award-outstanding-international",
      "published":"2013-08-20T00:00:00-04:00",
      "updated":"2014-04-30T13:02:34-04:00"
    },
    {
      "id":167,
      "title":"Call For Nominations for the 2014 SWEC Equity and Inclusivity Award",
      "site":"faculty-association",
      "link":"https:\/\/uwaterloo.ca\/faculty-association\/news\/call-nominations-2014-swec-equity-and-inclusivity-award",
      "published":"2014-04-21T00:00:00-04:00",
      "updated":"2014-04-30T11:17:06-04:00"
    },
    {
      "id":1729,
      "title":"Duever to become Ryerson&#039;s dean of engineering",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/duever-become-ryersons-dean-engineering",
      "published":"2014-04-15T00:00:00-04:00",
      "updated":"2014-04-30T11:09:54-04:00"
    },
    {
      "id":1732,
      "title":"Entrepreneurial engineers discuss University&#039;s role on the international stage",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/entrepreneurial-engineers-discuss-universitys-role",
      "published":"2014-04-16T00:00:00-04:00",
      "updated":"2014-04-30T11:08:55-04:00"
    },
    {
      "id":1746,
      "title":"Civil engineering grad students awarded prestigious scholarships",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/civil-engineering-grad-students-awarded-prestigious",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T11:01:09-04:00"
    },
    {
      "id":387,
      "title":"Social Development Studies (SDS) research round table series: Dr. Hsiao dAilly",
      "site":"renison",
      "link":"https:\/\/uwaterloo.ca\/renison\/news\/social-development-studies-sds-research-round-table-series",
      "published":"2010-10-04T00:00:00-04:00",
      "updated":"2014-04-30T10:43:40-04:00"
    },
    {
      "id":407,
      "title":"Social Development Studies (SDS) research round table series: Dr. Tracy Peressini",
      "site":"renison",
      "link":"https:\/\/uwaterloo.ca\/renison\/news\/social-development-studies-sds-research-round-table-series-1",
      "published":"2010-05-19T00:00:00-04:00",
      "updated":"2014-04-30T10:43:35-04:00"
    },
    {
      "id":138,
      "title":"International symposium on Canadian Chinese and American Chinese literature in English",
      "site":"renison",
      "link":"https:\/\/uwaterloo.ca\/renison\/news\/international-symposium-canadian-chinese-and-american",
      "published":"2010-10-15T00:00:00-04:00",
      "updated":"2014-04-30T10:43:26-04:00"
    },
    {
      "id":2201,
      "title":"Exchange certificate upgrade \u2013 May 1",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/exchange-certificate-upgrade-may-1",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T10:33:02-04:00"
    },
    {
      "id":1468,
      "title":"Waterloo professor receives L.S. Rosen Outstanding Educator Award",
      "site":"news",
      "link":"https:\/\/uwaterloo.ca\/news\/news\/waterloo-professor-receives-ls-rosen-outstanding-educator",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T10:17:34-04:00"
    },
    {
      "id":383,
      "title":"After-effects of recession still linger, UW wellbeing study says (TheRecord.com)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/after-effects-recession-still-linger-uw-wellbeing-study-says-0",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T09:57:28-04:00"
    },
    {
      "id":108,
      "title":"Special Collections acquires new scanners",
      "site":"library\/news",
      "link":"https:\/\/uwaterloo.ca\/library\/news\/news\/special-collections-acquires-new-scanners",
      "published":"2014-04-22T00:00:00-04:00",
      "updated":"2014-04-30T09:54:14-04:00"
    },
    {
      "id":227,
      "title":"Waterloo LEARN upgrade",
      "site":"learn-help",
      "link":"https:\/\/uwaterloo.ca\/learn-help\/news\/waterloo-learn-upgrade-0",
      "published":"2014-04-28T00:00:00-04:00",
      "updated":"2014-04-30T09:25:02-04:00"
    },
    {
      "id":228,
      "title":"Internet Explorer Critical security flaw",
      "site":"learn-help",
      "link":"https:\/\/uwaterloo.ca\/learn-help\/news\/internet-explorer-critical-security-flaw",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T09:24:42-04:00"
    },
    {
      "id":156,
      "title":"Print services migrated to Nexus",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/print-services-migrated-nexus",
      "published":"2013-08-26T00:00:00-04:00",
      "updated":"2014-04-30T09:06:20-04:00"
    },
    {
      "id":161,
      "title":"Help desk closed at lunch Wed Sept 18",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/help-desk-closed-lunch-wed-sept-18",
      "published":"2013-09-18T00:00:00-04:00",
      "updated":"2014-04-30T09:04:56-04:00"
    },
    {
      "id":164,
      "title":"SPSS problems October 1, 2013",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/spss-problems-october-1-2013",
      "published":"2013-10-02T00:00:00-04:00",
      "updated":"2014-04-30T09:04:02-04:00"
    },
    {
      "id":177,
      "title":"Limited support Tuesday December 3",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/limited-support-tuesday-december-3",
      "published":"2013-11-29T00:00:00-05:00",
      "updated":"2014-04-30T09:00:56-04:00"
    },
    {
      "id":179,
      "title":"Network problems in HH 2xx area",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/network-problems-hh-2xx-area",
      "published":"2013-12-09T00:00:00-05:00",
      "updated":"2014-04-30T09:00:02-04:00"
    },
    {
      "id":190,
      "title":"Emails regarding wifi configuration",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/emails-regarding-wifi-configuration",
      "published":"2014-01-31T00:00:00-05:00",
      "updated":"2014-04-30T08:59:06-04:00"
    },
    {
      "id":201,
      "title":"Connect Email\/Calendar Service Outage",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/connect-emailcalendar-service-outage",
      "published":"2014-03-20T00:00:00-04:00",
      "updated":"2014-04-30T08:56:12-04:00"
    },
    {
      "id":203,
      "title":"Microsoft support for Windows XP is ending April 8, 2014",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/microsoft-support-windows-xp-ending-april-8-2014",
      "published":"2014-04-03T00:00:00-04:00",
      "updated":"2014-04-30T08:54:17-04:00"
    },
    {
      "id":209,
      "title":"Microsoft Internet Explorer critical security flaw",
      "site":"arts-computing",
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/news\/microsoft-internet-explorer-critical-security-flaw",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T08:44:04-04:00"
    },
    {
      "id":382,
      "title":"Well-being Lagging Behind GDP Growth, Report Says (BlackburnNews.com)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/well-being-lagging-behind-gdp-growth-report-says",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T22:21:38-04:00"
    },
    {
      "id":381,
      "title":"Ontario in 2014: Less work, but longer commutes (CTV Kitchener video: Marc Venema)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/ontario-2014-less-work-longer-commutes-ctv-kitchener-video",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T22:06:26-04:00"
    },
    {
      "id":380,
      "title":"Five Ways the Lives of Ontarians have Changed since the 1990s (George Stroumboulopoulos Tonight)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/five-ways-lives-ontarians-have-changed-1990s-george",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T21:33:13-04:00"
    },
    {
      "id":1223,
      "title":"Arts professors win prestigious Early Research Award \u2013 again",
      "site":"arts",
      "link":"https:\/\/uwaterloo.ca\/arts\/news\/arts-professors-win-prestigious-early-research-award-again",
      "published":"2014-04-21T00:00:00-04:00",
      "updated":"2014-04-29T17:28:40-04:00"
    },
    {
      "id":1356,
      "title":"E-commerce web server fortuna will be down for maintenance: May 22 7am-10am",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/e-commerce-web-server-fortuna-will-be-down-maintenance-may",
      "published":"2013-05-17T00:00:00-04:00",
      "updated":"2014-04-29T14:11:09-04:00"
    },
    {
      "id":481,
      "title":"Beware: new Mac malware disguises itself as Adobe Flash installer",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/beware-new-mac-malware-disguises-itself-adobe-flash",
      "published":"2011-08-02T00:00:00-04:00",
      "updated":"2014-04-29T13:29:56-04:00"
    },
    {
      "id":386,
      "title":"SharePoint \u2018confirm site use\u2019 notices",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/sharepoint-confirm-site-use-notices",
      "published":"2011-02-10T00:00:00-05:00",
      "updated":"2014-04-29T13:29:16-04:00"
    },
    {
      "id":318,
      "title":"Conrad startup finalists in GTAN|START competition",
      "site":"conrad-business-entrepreneurship-technology",
      "link":"https:\/\/uwaterloo.ca\/conrad-business-entrepreneurship-technology\/news\/conrad-startup-finalists-gtanstart-competition",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T13:28:41-04:00"
    },
    {
      "id":371,
      "title":"MSDN-AA Software Center is currently unavailable",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/msdn-aa-software-center-currently-unavailable",
      "published":"2008-11-17T00:00:00-05:00",
      "updated":"2014-04-29T13:28:38-04:00"
    },
    {
      "id":379,
      "title":"GTA residents have the longest commute times in Ontario, study shows (GlobalNews.ca)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/gta-residents-have-longest-commute-times-ontario-study-shows",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T13:18:49-04:00"
    },
    {
      "id":378,
      "title":"Longer commutes mean &#039;time crunch&#039; is getting worse study finds (CP24.com)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/longer-commutes-mean-time-crunch-getting-worse-study-finds",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T13:00:55-04:00"
    },
    {
      "id":1605,
      "title":"Adel Sedra receives Ontario&#039;s highest honour",
      "site":"engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/adel-sedra-receives-ontarios-highest-honour",
      "published":"2014-01-24T19:00:00-05:00",
      "updated":"2014-04-29T12:33:21-04:00"
    },
    {
      "id":374,
      "title":"New Ontario index puts wellbeing at the forefront",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/new-ontario-index-puts-wellbeing-forefront",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T12:16:41-04:00"
    },
    {
      "id":1393,
      "title":"Presentation Friday: NetID",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/presentation-friday-netid",
      "published":"2013-09-05T00:00:00-04:00",
      "updated":"2014-04-29T12:12:03-04:00"
    },
    {
      "id":1340,
      "title":"Internet Issues - resolved",
      "site":"information-systems-technology",
      "link":"https:\/\/uwaterloo.ca\/information-systems-technology\/news\/internet-issues-resolved",
      "published":"2013-03-27T00:00:00-04:00",
      "updated":"2014-04-29T12:10:45-04:00"
    },
    {
      "id":377,
      "title":"Ontarians\u2019 well-being lags behind GDP growth, report says (CBC News KW)",
      "site":"canadian-index-wellbeing",
      "link":"https:\/\/uwaterloo.ca\/canadian-index-wellbeing\/news\/ontarians-well-being-lags-behind-gdp-growth-report-says-cbc",
      "published":"2014-04-29T00:00:00-04:00",
      "updated":"2014-04-29T12:02:15-04:00"
    }
  ]
}
```


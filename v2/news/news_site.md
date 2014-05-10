# Get Events for Site

```
GET news/{site}.{format}
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
    <td>1699</td>
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

- This is a 'realtime' feed. An item will be available on the api the second its up using Webhooks
- Any value can be `null`


### Sources

- Crawled from all WMCS sites listed at https://api.uwaterloo.ca/v2/resources/sites.{format}


## Parameters

```
GET news/{site}.{format}
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
GET news/{site}.{format}
```

- **https://api.uwaterloo.ca/v2/news/engineering.json**
- **https://api.uwaterloo.ca/v2/news/science.xml**
- **https://api.uwaterloo.ca/v2/news/engineering.json?callback=myResponse**


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
    "requests":488,
    "timestamp":1399701932,
    "status":200,
    "message":"Request successful",
    "method_id":1699,
    "method":{
      
    }
  },
  "data":[
    {
      "id":1760,
      "title":"ECE team advances in challenge to design the car of the future",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/ece-team-advances-challenge-design-car-future",
      "published":"2014-05-07T00:00:00-04:00",
      "updated":"2014-05-07T16:22:48-04:00"
    },
    {
      "id":1756,
      "title":"Grad student wins hydrotechnical engineering award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/grad-student-wins-hydrotechnical-engineering-award",
      "published":"2014-05-05T00:00:00-04:00",
      "updated":"2014-05-07T15:39:20-04:00"
    },
    {
      "id":1755,
      "title":"You charge your phone. Are you ready to charge your car?",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/you-charge-your-phone-are-you-ready-charge-your-car",
      "published":"2014-05-01T00:00:00-04:00",
      "updated":"2014-05-05T11:20:27-04:00"
    },
    {
      "id":1746,
      "title":"Civil engineering grad students awarded prestigious scholarships",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/civil-engineering-grad-students-awarded-prestigious",
      "published":"2014-04-30T00:00:00-04:00",
      "updated":"2014-04-30T11:01:09-04:00"
    },
    {
      "id":1742,
      "title":"John Baker&#039;s D2L is Transforming Education",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/john-bakers-d2l-transforming-education",
      "published":"2014-04-23T20:00:00-04:00",
      "updated":"2014-04-24T13:21:44-04:00"
    },
    {
      "id":1732,
      "title":"Entrepreneurial engineers discuss University&#039;s role on the international stage",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/entrepreneurial-engineers-discuss-universitys-role",
      "published":"2014-04-16T00:00:00-04:00",
      "updated":"2014-04-30T11:08:55-04:00"
    },
    {
      "id":1729,
      "title":"Duever to become Ryerson&#039;s dean of engineering",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/duever-become-ryersons-dean-engineering",
      "published":"2014-04-15T00:00:00-04:00",
      "updated":"2014-04-30T11:09:54-04:00"
    },
    {
      "id":1727,
      "title":"Celebrating a leader in Architectural education",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/celebrating-leader-architectural-education",
      "published":"2013-11-12T19:00:00-05:00",
      "updated":"2014-04-15T15:25:20-04:00"
    },
    {
      "id":1726,
      "title":"New director sees School of Architecture at forefront of technological wave",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/new-director-sees-school-architecture-forefront",
      "published":"2014-04-13T20:00:00-04:00",
      "updated":"2014-04-15T15:23:43-04:00"
    },
    {
      "id":1724,
      "title":"Innovative Student Projects Receive Funding from the Engineer of the Future Trust",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/innovative-student-projects-receive-funding-engineer-future",
      "published":"2014-04-07T20:00:00-04:00",
      "updated":"2014-04-08T15:31:18-04:00"
    },
    {
      "id":1721,
      "title":"Inspiring the next generation of women engineers",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/inspiring-next-generation-women-engineers",
      "published":"2014-04-05T00:00:00-04:00",
      "updated":"2014-04-15T13:52:42-04:00"
    },
    {
      "id":1717,
      "title":"Best paper for chemical engineering researchers",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/best-paper-chemical-engineering-researchers",
      "published":"2014-04-01T00:00:00-04:00",
      "updated":"2014-04-02T14:03:14-04:00"
    },
    {
      "id":1716,
      "title":"Four professors named Canada Research Chairs",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/four-professors-named-canada-research-chairs",
      "published":"2014-03-27T20:00:00-04:00",
      "updated":"2014-04-04T11:33:02-04:00"
    },
    {
      "id":1715,
      "title":"Alumni appointed to business and academic leadership positions",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/alumni-appointed-business-and-academic-leadership-positions",
      "published":"2014-04-01T00:00:00-04:00",
      "updated":"2014-04-01T15:34:52-04:00"
    },
    {
      "id":1712,
      "title":"New funding for undergraduate research",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/new-funding-undergraduate-research",
      "published":"2014-03-31T00:00:00-04:00",
      "updated":"2014-04-15T11:22:17-04:00"
    },
    {
      "id":1711,
      "title":"Announcing the winners of the Esch Awards for Capstone Design",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/announcing-winners-esch-awards-capstone-design",
      "published":"2014-04-04T00:00:00-04:00",
      "updated":"2014-04-16T13:54:47-04:00"
    },
    {
      "id":1708,
      "title":"Bionic Bodies and Gold Nanostars: Engineering Graduate Students shine in Waterloo\u2019s 3MT Finals",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/bionic-bodies-and-gold-nanostars-engineering-graduate",
      "published":"2014-03-27T00:00:00-04:00",
      "updated":"2014-03-27T17:36:55-04:00"
    },
    {
      "id":1707,
      "title":"Four engineering startups take away $110,000 in funding at VeloCity Fund Finals",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/waterloo-engineers-dominate-velocity-fund-finals",
      "published":"2014-03-27T00:00:00-04:00",
      "updated":"2014-04-01T14:45:51-04:00"
    },
    {
      "id":1706,
      "title":"Student receives prestigious University teaching honour",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/student-receives-prestigious-university-teaching-honour",
      "published":"2014-03-26T00:00:00-04:00",
      "updated":"2014-04-16T15:06:51-04:00"
    },
    {
      "id":1705,
      "title":"Barry Wills remembered",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/barry-wills-remembered",
      "published":"2014-03-26T00:00:00-04:00",
      "updated":"2014-03-26T17:51:02-04:00"
    },
    {
      "id":1704,
      "title":"MBET grad&#039;s startup joins Silicon Valley\u2019s Y Combinator",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/mbet-grads-startup-joins-silicon-valleys-y-combinator",
      "published":"2014-03-25T00:00:00-04:00",
      "updated":"2014-03-26T17:52:44-04:00"
    },
    {
      "id":1697,
      "title":"FIRST Robotics Competition draws high school students from across the province",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/first-robotics-competition-draws-high-school-students-across",
      "published":"2014-03-19T20:00:00-04:00",
      "updated":"2014-04-28T16:45:22-04:00"
    },
    {
      "id":1695,
      "title":"Systems design student honoured with University&#039;s co-op award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/systems-design-student-honoured-universitys-co-op-award",
      "published":"2014-03-20T00:00:00-04:00",
      "updated":"2014-03-26T17:53:00-04:00"
    },
    {
      "id":1694,
      "title":"Women engineers recognized during National Engineering Month",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/women-engineers-recognized-during-national-engineering-month",
      "published":"2014-03-28T00:00:00-04:00",
      "updated":"2014-04-02T14:07:27-04:00"
    },
    {
      "id":1691,
      "title":"Student Innovation on Display at the 6th Annual Mechatronics Capstone Design Symposium",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/student-innovation-display-6th-annual-mechatronics-capstone",
      "published":"2014-03-14T00:00:00-04:00",
      "updated":"2014-03-20T14:46:06-04:00"
    },
    {
      "id":1690,
      "title":"Professor Adrian Gerlich named NSERC\/TransCanada Industrial Research Chair in Welding",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/professor-adrian-gerlich-named-nserctranscanada-industrial",
      "published":"2014-03-14T00:00:00-04:00",
      "updated":"2014-03-17T15:05:18-04:00"
    },
    {
      "id":1685,
      "title":"Norman Esch Entrepreneurship Awards for Capstone Design",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/norman-esch-entrepreneurship-awards-capstone-design",
      "published":"2014-03-10T00:00:00-04:00",
      "updated":"2014-03-12T16:54:28-04:00"
    },
    {
      "id":1682,
      "title":"Graduate student awarded prestigious Vale scholarship",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/graduate-student-awarded-prestigious-vale-scholarship",
      "published":"2014-03-12T00:00:00-04:00",
      "updated":"2014-03-14T12:44:52-04:00"
    },
    {
      "id":1681,
      "title":"Professors win Google Research Awards",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/professors-win-google-research-awards",
      "published":"2014-03-11T00:00:00-04:00",
      "updated":"2014-03-26T14:45:17-04:00"
    },
    {
      "id":1679,
      "title":"ECE researchers receive best transaction paper award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/ece-researchers-receive-best-transaction-paper-award",
      "published":"2014-03-11T00:00:00-04:00",
      "updated":"2014-03-11T09:37:17-04:00"
    },
    {
      "id":1675,
      "title":"Announcing the 90sC! A new award for Capstone Design",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/announcing-90sc-new-award-capstone-design",
      "published":"2014-03-05T00:00:00-05:00",
      "updated":"2014-03-12T14:01:32-04:00"
    },
    {
      "id":1670,
      "title":"Prestigious design magazine features School of Architecture",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/prestigious-design-magazine-features-school-architecture",
      "published":"2014-03-03T00:00:00-05:00",
      "updated":"2014-03-07T15:07:52-05:00"
    },
    {
      "id":1668,
      "title":"Former civil engineering grad student honoured  for thesis",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/former-civil-engineering-grad-student-honoured-thesis",
      "published":"2014-02-28T00:00:00-05:00",
      "updated":"2014-02-28T08:31:23-05:00"
    },
    {
      "id":1664,
      "title":"Register for the 2014 Teaching and Learning Conference",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/register-2014-teaching-and-learning-conference",
      "published":"2014-04-15T00:00:00-04:00",
      "updated":"2014-04-16T13:55:28-04:00"
    },
    {
      "id":1661,
      "title":"Mechatronics grad honoured by local Chamber of Commerce",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/mechatronics-grad-honoured-local-chamber-commerce",
      "published":"2014-02-24T00:00:00-05:00",
      "updated":"2014-02-25T16:03:43-05:00"
    },
    {
      "id":1655,
      "title":"New Technology magazine features Clearpath Robotics",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/new-technology-magazine-features-clearpath-robotics",
      "published":"2014-02-18T00:00:00-05:00",
      "updated":"2014-02-18T17:29:55-05:00"
    },
    {
      "id":1651,
      "title":"Tighe honoured with Bleeds Black Award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/tighe-honoured-bleeds-black-award",
      "published":"2014-02-01T00:00:00-05:00",
      "updated":"2014-02-12T14:15:00-05:00"
    },
    {
      "id":1650,
      "title":"Management Engineering students capture awards at national competition",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/management-engineering-students-capture-awards-national",
      "published":"2014-01-31T00:00:00-05:00",
      "updated":"2014-02-12T14:03:15-05:00"
    },
    {
      "id":1649,
      "title":"Architecture professor wins international award in creative achivement",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/architecture-professor-wins-international-award-creative",
      "published":"2014-02-11T00:00:00-05:00",
      "updated":"2014-02-12T14:25:55-05:00"
    },
    {
      "id":1648,
      "title":"Architecture graduate named one of Britian&#039;s most influential",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/architecture-graduate-named-one-britians-most-influential",
      "published":"2014-02-10T00:00:00-05:00",
      "updated":"2014-02-13T10:18:29-05:00"
    },
    {
      "id":1640,
      "title":"When would you lie?",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/when-would-you-lie",
      "published":"2014-02-10T00:00:00-05:00",
      "updated":"2014-02-19T14:29:32-05:00"
    },
    {
      "id":1638,
      "title":"Architecture grad Alison Brooks one of Britain\u2019s 500 most influential people",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/architecture-graduate-one-britians-most-influential",
      "published":"2014-02-13T00:00:00-05:00",
      "updated":"2014-02-21T12:49:44-05:00"
    },
    {
      "id":1637,
      "title":"Deadline Approaching for Amit and Meena Chakma Awards for Exceptional Teaching by a Student",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/deadline-approaching-amit-and-meena-chakma-awards",
      "published":"2014-02-06T00:00:00-05:00",
      "updated":"2014-02-06T10:47:02-05:00"
    },
    {
      "id":1632,
      "title":"Research partnership gives Canada competitive edge in hybrid vehicle design",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/research-partnership-gives-canada-competitive-edge-hybrid",
      "published":"2014-02-03T00:00:00-05:00",
      "updated":"2014-02-05T12:38:27-05:00"
    },
    {
      "id":1628,
      "title":"Engineering Image Processing Expert Awarded E.W.R. Steacie Memorial Fellowship",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineering-image-processing-expert-awarded-ewr-steacie",
      "published":"2014-02-03T00:00:00-05:00",
      "updated":"2014-02-03T09:38:42-05:00"
    },
    {
      "id":1620,
      "title":"MBET students win $5000 in RBC Challenge",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/mbet-students-win-5000-rbc-challenge",
      "published":"2014-01-28T00:00:00-05:00",
      "updated":"2014-01-30T14:44:21-05:00"
    },
    {
      "id":1605,
      "title":"Adel Sedra receives Ontario&#039;s highest honour",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/adel-sedra-receives-ontarios-highest-honour",
      "published":"2014-01-24T19:00:00-05:00",
      "updated":"2014-04-29T12:33:21-04:00"
    },
    {
      "id":1603,
      "title":"Two $40,000 prizes announced for Capstone Design",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/two-40000-prizes-announced-capstone-design",
      "published":"2014-01-24T00:00:00-05:00",
      "updated":"2014-03-11T11:54:21-04:00"
    },
    {
      "id":1590,
      "title":"MBET students to compete in RBC innovator finals",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/mbet-students-compete-rbc-innovator-finals",
      "published":"2014-01-14T00:00:00-05:00",
      "updated":"2014-01-15T11:03:03-05:00"
    },
    {
      "id":1588,
      "title":"Elementary students apply sci-tech skills at FIRST LEGO League championship",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/elementary-students-apply-sci-tech-skills-first-lego-league",
      "published":"2014-01-13T00:00:00-05:00",
      "updated":"2014-02-03T15:18:44-05:00"
    },
    {
      "id":1584,
      "title":"Alumni&#039;s startup puts a new spin on old technology",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/alumnis-startup-puts-new-spin-old-technology",
      "published":"2014-01-13T00:00:00-05:00",
      "updated":"2014-01-21T09:52:26-05:00"
    },
    {
      "id":1581,
      "title":"Work Ethic from ASEE Prism",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/work-ethic-asee-prism",
      "published":"2014-01-10T00:00:00-05:00",
      "updated":"2014-01-10T22:46:01-05:00"
    },
    {
      "id":1578,
      "title":"Three with Waterloo Engineering ties make Forbes&#039; list",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/three-waterloo-engineering-ties-make-forbes-list",
      "published":"2014-01-09T00:00:00-05:00",
      "updated":"2014-01-13T11:38:14-05:00"
    },
    {
      "id":1573,
      "title":"ECE professor receives CFI funding for quantum systems research",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/ece-professor-receives-cfi-funding-quantum-systems-research",
      "published":"2014-01-08T00:00:00-05:00",
      "updated":"2014-02-18T09:57:17-05:00"
    },
    {
      "id":1572,
      "title":"Professor emeritus receives Transportation Research Board&#039;s highest honour",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/professor-emeritus-receive-transportation-research-boards",
      "published":"2014-01-16T00:00:00-05:00",
      "updated":"2014-02-12T17:02:44-05:00"
    },
    {
      "id":1571,
      "title":"MappedIn launches from startup life at Velocity",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/mappedin-launches-startup-life-velocity",
      "published":"2014-01-07T00:00:00-05:00",
      "updated":"2014-01-08T14:44:00-05:00"
    },
    {
      "id":1568,
      "title":"Registration under way for 3 Minute Thesis Competition",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/registration-under-way-3-minute-thesis-competition",
      "published":"2014-01-08T00:00:00-05:00",
      "updated":"2014-02-18T10:09:40-05:00"
    },
    {
      "id":1565,
      "title":"Grad student takes a top award in international steel contest",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/grad-student-takes-top-award-international-steel-contest",
      "published":"2014-01-03T00:00:00-05:00",
      "updated":"2014-03-07T10:46:44-05:00"
    },
    {
      "id":1564,
      "title":"Choosing your engineering program",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/choosing-your-engineering-program",
      "published":"2014-01-02T00:00:00-05:00",
      "updated":"2014-01-02T17:16:45-05:00"
    },
    {
      "id":1562,
      "title":"Mechatronics Engineering to expand in 2014",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/mechatronics-engineering-expand-2014",
      "published":"2013-12-23T00:00:00-05:00",
      "updated":"2014-02-18T08:49:25-05:00"
    },
    {
      "id":1555,
      "title":"Startup creates spray to prevent frost on your windshield",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/startup-creates-spray-prevent-frost-your-windshield",
      "published":"2013-12-17T00:00:00-05:00",
      "updated":"2013-12-17T16:29:23-05:00"
    },
    {
      "id":1554,
      "title":"Student team works on next generation smart car",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/student-team-works-next-generation-smart-car",
      "published":"2013-12-17T00:00:00-05:00",
      "updated":"2013-12-17T16:09:36-05:00"
    },
    {
      "id":1544,
      "title":"Innovative research featured in new graduate marketing campaign",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/innovative-research-featured-new-grad-studies-marketing",
      "published":"2013-12-11T00:00:00-05:00",
      "updated":"2014-03-07T14:31:38-05:00"
    },
    {
      "id":1543,
      "title":"WatCAR managing director talks fuel cells on Lang O&#039;Leary Exchange",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/watcar-managing-director-talks-fuel-cells-lang-oleary",
      "published":"2013-11-21T00:00:00-05:00",
      "updated":"2013-12-11T17:11:57-05:00"
    },
    {
      "id":1542,
      "title":"Wind energy experts part of Globe series on northern infrastructure projects",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/wind-energy-experts-part-globe-series-northern",
      "published":"2013-12-11T00:00:00-05:00",
      "updated":"2014-01-09T10:19:57-05:00"
    },
    {
      "id":1541,
      "title":"Conrad Centre professor chosen to chair provincial expert panel",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/conrad-centre-professor-chosen-chair-provincial-expert-panel",
      "published":"2013-12-10T00:00:00-05:00",
      "updated":"2013-12-11T09:30:34-05:00"
    },
    {
      "id":1540,
      "title":"Memorial planned for CEE Professor Khal Soudki",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/memorial-planned-cee-professor-khal-soudki",
      "published":"2013-12-09T00:00:00-05:00",
      "updated":"2013-12-10T12:16:29-05:00"
    },
    {
      "id":1537,
      "title":"Waterloo Announces New Biomedical Engineering Degree",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/waterloo-announces-new-biomedical-engineering-degree",
      "published":"2013-12-09T00:00:00-05:00",
      "updated":"2013-12-10T21:15:28-05:00"
    },
    {
      "id":1536,
      "title":"ECE faculty and students win a top IBM conference award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/ece-faculty-and-students-win-top-ibm-conference-award",
      "published":"2013-12-04T00:00:00-05:00",
      "updated":"2013-12-04T15:13:18-05:00"
    },
    {
      "id":1535,
      "title":"Alexis Ohanian says &quot;Waterloo Engineering students will be tomorrow&#039;s global leaders&quot;",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/alexis-ohanian-says-waterloo-engineering-students-will-be",
      "published":"2013-12-04T00:00:00-05:00",
      "updated":"2014-02-13T09:27:20-05:00"
    },
    {
      "id":1533,
      "title":"Chris Hadfield at Waterloo for sold-out event",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/chris-hadfield-waterloo-sold-out-event",
      "published":"2013-12-03T00:00:00-05:00",
      "updated":"2014-02-14T09:45:17-05:00"
    },
    {
      "id":1531,
      "title":"Connecting Waterloo to Asia and Beyond",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/connecting-waterloo-asia-and-beyond",
      "published":"2013-12-02T00:00:00-05:00",
      "updated":"2013-12-09T16:14:50-05:00"
    },
    {
      "id":1528,
      "title":"Capstone design project now sought-after wearable technology",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/capstone-design-project-now-sought-after-wearable-technology",
      "published":"2013-11-27T00:00:00-05:00",
      "updated":"2014-01-21T14:58:57-05:00"
    },
    {
      "id":1527,
      "title":"Editorial touts value of engineering grad degree",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/editorial-touts-value-engineering-grad-degree",
      "published":"2013-11-26T00:00:00-05:00",
      "updated":"2013-11-27T14:40:45-05:00"
    },
    {
      "id":1525,
      "title":"Haas the only Canadian to receive membership into National Academy of Construction",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/haas-only-canadian-receive-membership-national-academy",
      "published":"2013-11-25T00:00:00-05:00",
      "updated":"2013-11-25T16:39:40-05:00"
    },
    {
      "id":1524,
      "title":"Professor honoured with engineering research and development medal",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/professor-honoured-engineering-research-and-development",
      "published":"2013-11-24T00:00:00-05:00",
      "updated":"2013-12-02T09:35:15-05:00"
    },
    {
      "id":1519,
      "title":"Engineering awards dinner celebrates students, staff, faculty and alumni",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineering-awards-dinner-celebrates-students-staff-faculty",
      "published":"2013-11-21T00:00:00-05:00",
      "updated":"2013-11-25T14:25:32-05:00"
    },
    {
      "id":1516,
      "title":"How the 21st Century will be made according to Alexis Ohanian",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/how-21st-century-will-be-made-according-alexis-ohanian",
      "published":"2013-11-20T00:00:00-05:00",
      "updated":"2014-02-13T09:24:32-05:00"
    },
    {
      "id":1515,
      "title":"Chemical engineering students take top awards",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/chemical-engineering-students-take-top-awards",
      "published":"2013-11-20T00:00:00-05:00",
      "updated":"2013-11-21T16:03:07-05:00"
    },
    {
      "id":1513,
      "title":"Software system co-founded by new faculty member receives startup funding",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/software-system-co-founded-new-faculty-member-receives",
      "published":"2013-11-19T00:00:00-05:00",
      "updated":"2013-11-20T14:20:53-05:00"
    },
    {
      "id":1511,
      "title":"ECE professor appointed chair of Orange Scientific Board",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/ece-professor-appointed-chair-orange-scientific-board",
      "published":"2013-11-19T00:00:00-05:00",
      "updated":"2013-11-20T13:14:38-05:00"
    },
    {
      "id":1505,
      "title":"Engineering professor to host Hawking&#039;s Brave New World",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineering-professor-host-hawkings-brave-new-world",
      "published":"2013-11-13T00:00:00-05:00",
      "updated":"2013-11-13T17:22:13-05:00"
    },
    {
      "id":1504,
      "title":"Waterloo Engineering showcases R&amp;D projects at WE INNOVATE",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/waterloo-engineering-showcases-rd-projects-we-innovate",
      "published":"2013-11-13T00:00:00-05:00",
      "updated":"2013-11-13T16:15:17-05:00"
    },
    {
      "id":1503,
      "title":"Architecture alumni win designing recovery contest",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/architecture-alumni-win-designing-recovery-contest",
      "published":"2013-11-13T00:00:00-05:00",
      "updated":"2013-11-13T15:32:49-05:00"
    },
    {
      "id":1502,
      "title":"Engineering entrepreneurs to compete for coveted spot in VeloCity garage",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineering-entrepreneurs-compete-coveted-spot-velocity",
      "published":"2013-11-13T00:00:00-05:00",
      "updated":"2013-11-18T18:39:13-05:00"
    },
    {
      "id":1501,
      "title":"WiE committee to be honoured with equity and inclusion award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/wie-committee-be-honoured-equity-and-inclusion-award",
      "published":"2013-11-13T00:00:00-05:00",
      "updated":"2013-11-15T09:35:06-05:00"
    },
    {
      "id":1499,
      "title":"Engineering 5&#039;s Computer Commons dedicated to Magna International",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineering-5s-computer-commons-dedicated-magna",
      "published":"2013-11-05T00:00:00-05:00",
      "updated":"2013-11-12T10:48:22-05:00"
    },
    {
      "id":1497,
      "title":"Bloomberg Businessweek calls University of Waterloo Canada&#039;s Stanford",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/bloomberg-businessweek-calls-university-waterloo-canadas",
      "published":"2013-11-05T00:00:00-05:00",
      "updated":"2014-02-14T09:21:18-05:00"
    },
    {
      "id":1496,
      "title":"Engineers convocate and receive honours",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineers-convocate-and-receive-honours",
      "published":"2013-10-26T00:00:00-04:00",
      "updated":"2013-11-05T11:11:43-05:00"
    },
    {
      "id":1495,
      "title":"Civil engineering grad wins best transportation paper award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/civil-engineering-grad-wins-best-transportation-paper-award",
      "published":"2013-11-04T00:00:00-05:00",
      "updated":"2013-11-05T10:15:02-05:00"
    },
    {
      "id":1493,
      "title":"CPATT hosts poster symposium and is featured in newsletter",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/cpatt-hosts-poster-symposium-and-featured-newsletter",
      "published":"2013-10-31T00:00:00-04:00",
      "updated":"2013-11-04T09:38:10-05:00"
    },
    {
      "id":1489,
      "title":"Waterloo again tops Maclean&#039;s list of most innovative universities",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/waterloo-again-tops-macleans-list-most-innovative",
      "published":"2013-10-31T00:00:00-04:00",
      "updated":"2013-10-31T15:51:13-04:00"
    },
    {
      "id":1485,
      "title":"Automotive research receives almost $5 million in funding",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/automotive-research-receives-almost-5-million-funding",
      "published":"2013-10-25T00:00:00-04:00",
      "updated":"2013-10-28T12:02:28-04:00"
    },
    {
      "id":1484,
      "title":"Engineering professors take guesswork out of railway crossing safety",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/engineering-professors-take-guesswork-out-railway-crossing",
      "published":"2013-10-28T00:00:00-04:00",
      "updated":"2013-11-13T16:44:03-05:00"
    },
    {
      "id":1482,
      "title":"Two Waterloo Engineering grads win Ontario Entrepreneur Awards",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/two-waterloo-engineering-grads-win-ontario-entrepreneur",
      "published":"2013-10-25T00:00:00-04:00",
      "updated":"2014-01-09T15:54:09-05:00"
    },
    {
      "id":1479,
      "title":"Management Engineering student swings to OUA title",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/management-engineering-student-swings-oua-title",
      "published":"2013-10-24T00:00:00-04:00",
      "updated":"2013-10-24T11:27:37-04:00"
    },
    {
      "id":1478,
      "title":"Waterloo Engineering Alumni are Finalists for prestigious Entrepreneur Award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/waterloo-engineering-alumni-are-finalists-prestigious",
      "published":"2013-10-24T00:00:00-04:00",
      "updated":"2014-01-09T15:50:59-05:00"
    },
    {
      "id":1476,
      "title":"Globe and Mail calls uWaterloo Canada&#039;s Silicon Valley",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/globe-and-mail-calls-uwaterloo-canadas-silicon-valley",
      "published":"2013-10-23T00:00:00-04:00",
      "updated":"2013-11-13T15:46:24-05:00"
    },
    {
      "id":1474,
      "title":"Innovative project using 3D printer wins top wind energy award",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/innovative-project-using-3d-printer-wins-top-wind-energy",
      "published":"2013-10-21T00:00:00-04:00",
      "updated":"2014-02-14T12:58:32-05:00"
    },
    {
      "id":1473,
      "title":"Student Design Centre named to honour former dean",
      "link":"https:\/\/uwaterloo.ca\/engineering\/news\/student-design-centre-named-honour-former-dean",
      "published":"2013-10-18T00:00:00-04:00",
      "updated":"2013-10-22T09:20:11-04:00"
    }
  ]
}
```


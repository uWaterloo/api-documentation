# List of all courses

```
GET /courses.{format}
```

## Description

> This method returns a list of all courses (currently and historically offered) from the opendata database

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
    <td>1471</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>courses</td>
    <td><b>Service ID</b></td>
    <td>239</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Registrar</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every term</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- This endpoint returns over 6000 courses!
- Any value can be `null`


### Sources

- http://ugradcalendar.uwaterloo.ca/
- http://gradcalendar.uwaterloo.ca/


## Parameters

```
GET /courses.{format}
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
GET /courses.{format}
```

- **https://api.uwaterloo.ca/v2/courses.json**
- **https://api.uwaterloo.ca/v2/courses.xml**
- **https://api.uwaterloo.ca/v2/courses.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>course_id</b></td>
    <td>string</td>
    <td>Registrar assigned course ID</td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>string</td>
    <td>Requested subject acronym</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>string</td>
    <td>Registrar assigned class number</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Class name and title</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":835287,
    "timestamp":1456502387,
    "status":200,
    "message":"Request successful",
    "method_id":1471,
    "method":{
      
    }
  },
  "data":[
    {
      "course_id":"011672",
      "subject":"ACC",
      "catalog_number":"604",
      "title":"Statutory Interpretation"
    },
    {
      "course_id":"011673",
      "subject":"ACC",
      "catalog_number":"605",
      "title":"International Tax"
    },
    {
      "course_id":"011674",
      "subject":"ACC",
      "catalog_number":"606",
      "title":"Business Valuations"
    },
    {
      "course_id":"011675",
      "subject":"ACC",
      "catalog_number":"607",
      "title":"Tax Issues Integration"
    },
    {
      "course_id":"011677",
      "subject":"ACC",
      "catalog_number":"609",
      "title":"Financial Statement Analysis"
    },
    {
      "course_id":"000003",
      "subject":"ACC",
      "catalog_number":"610",
      "title":"Public Accounting Practice"
    },
    {
      "course_id":"000004",
      "subject":"ACC",
      "catalog_number":"611",
      "title":"External Reporting"
    },
    {
      "course_id":"011484",
      "subject":"ACC",
      "catalog_number":"621",
      "title":"System Reliability Principles and Criteria"
    },
    {
      "course_id":"011478",
      "subject":"ACC",
      "catalog_number":"622",
      "title":"Electronic Commerce"
    },
    {
      "course_id":"011479",
      "subject":"ACC",
      "catalog_number":"623",
      "title":"Business Technology Law"
    },
    {
      "course_id":"000012",
      "subject":"ACC",
      "catalog_number":"626",
      "title":"IT Assurance and Computer-Assisted Audit Techniques"
    },
    {
      "course_id":"000013",
      "subject":"ACC",
      "catalog_number":"627",
      "title":"Business Process Enablement and Project Management"
    },
    {
      "course_id":"000020",
      "subject":"ACC",
      "catalog_number":"650",
      "title":"Assurance and Governance"
    },
    {
      "course_id":"013326",
      "subject":"ACC",
      "catalog_number":"652",
      "title":"Forensic Accounting"
    },
    {
      "course_id":"000024",
      "subject":"ACC",
      "catalog_number":"662",
      "title":"Tax Policy"
    },
    {
      "course_id":"000028",
      "subject":"ACC",
      "catalog_number":"680",
      "title":"Performance Measurement and Control systems for Implementing Strategy"
    },
    {
      "course_id":"000029",
      "subject":"ACC",
      "catalog_number":"681",
      "title":"Understanding and Managing Organizational Change"
    },
    {
      "course_id":"010147",
      "subject":"ACC",
      "catalog_number":"682",
      "title":"Measuring and Managing the Value Creation Process"
    },
    {
      "course_id":"012014",
      "subject":"ACC",
      "catalog_number":"683",
      "title":"Emerging Issues in Management and Marketing"
    },
    {
      "course_id":"013327",
      "subject":"ACC",
      "catalog_number":"684",
      "title":"Strategy and Business Models"
    },
    {
      "course_id":"013328",
      "subject":"ACC",
      "catalog_number":"685",
      "title":"Performance Management"
    },
    {
      "course_id":"000030",
      "subject":"ACC",
      "catalog_number":"690",
      "title":"Topics in Accounting"
    },
    {
      "course_id":"000040",
      "subject":"ACC",
      "catalog_number":"701",
      "title":"Financial Accounting Research Seminar"
    },
    {
      "course_id":"000041",
      "subject":"ACC",
      "catalog_number":"702",
      "title":"Management Accounting Research Seminar"
    },
    {
      "course_id":"000042",
      "subject":"ACC",
      "catalog_number":"750",
      "title":"Auditing Research Seminar"
    },
    {
      "course_id":"000043",
      "subject":"ACC",
      "catalog_number":"760",
      "title":"Taxation Research Seminar"
    },
    {
      "course_id":"000044",
      "subject":"ACC",
      "catalog_number":"770",
      "title":"Finance 1"
    },
    {
      "course_id":"000045",
      "subject":"ACC",
      "catalog_number":"771",
      "title":"Finance 2"
    },
    {
      "course_id":"000046",
      "subject":"ACC",
      "catalog_number":"772",
      "title":"Finance 3"
    },
    {
      "course_id":"000047",
      "subject":"ACC",
      "catalog_number":"781",
      "title":"Introduction to Research 1"
    },
    {
      "course_id":"000049",
      "subject":"ACC",
      "catalog_number":"784",
      "title":"Selected Topics in Research Methodology"
    },
    {
      "course_id":"003290",
      "subject":"ACTSC",
      "catalog_number":"221",
      "title":"Mathematics of Investment"
    },
    {
      "course_id":"003293",
      "subject":"ACTSC",
      "catalog_number":"231",
      "title":"Mathematics of Finance"
    },
    {
      "course_id":"003294",
      "subject":"ACTSC",
      "catalog_number":"232",
      "title":"Life Contingencies 1"
    },
    {
      "course_id":"011750",
      "subject":"ACTSC",
      "catalog_number":"291",
      "title":"Corporate Finance 1"
    },
    {
      "course_id":"003295",
      "subject":"ACTSC",
      "catalog_number":"331",
      "title":"Life Contingencies 2"
    },
    {
      "course_id":"011438",
      "subject":"ACTSC",
      "catalog_number":"371",
      "title":"Introduction to Investments"
    },
    {
      "course_id":"012044",
      "subject":"ACTSC",
      "catalog_number":"372",
      "title":"Corporate Finance"
    },
    {
      "course_id":"011751",
      "subject":"ACTSC",
      "catalog_number":"391",
      "title":"Corporate Finance 2"
    },
    {
      "course_id":"003300",
      "subject":"ACTSC",
      "catalog_number":"431",
      "title":"Loss Models 1"
    },
    {
      "course_id":"003301",
      "subject":"ACTSC",
      "catalog_number":"432",
      "title":"Loss Models 2"
    },
    {
      "course_id":"003302",
      "subject":"ACTSC",
      "catalog_number":"433",
      "title":"Analysis of Survival Data"
    },
    {
      "course_id":"009492",
      "subject":"ACTSC",
      "catalog_number":"445",
      "title":"Quantitative Risk Management"
    },
    {
      "course_id":"003305",
      "subject":"ACTSC",
      "catalog_number":"446",
      "title":"Mathematical Models in Finance"
    },
    {
      "course_id":"003308",
      "subject":"ACTSC",
      "catalog_number":"453",
      "title":"Basic Pension Mathematics"
    },
    {
      "course_id":"013318",
      "subject":"ACTSC",
      "catalog_number":"455",
      "title":"Advanced Life Insurance Practice"
    },
    {
      "course_id":"003312",
      "subject":"ACTSC",
      "catalog_number":"462",
      "title":"Introduction to Property and Casualty Pricing"
    },
    {
      "course_id":"003299",
      "subject":"ACTSC",
      "catalog_number":"463",
      "title":"Introduction to Property and Casualty Loss Reserving"
    },
    {
      "course_id":"014534",
      "subject":"ACTSC",
      "catalog_number":"468",
      "title":"Readings in Actuarial Science 1"
    },
    {
      "course_id":"014535",
      "subject":"ACTSC",
      "catalog_number":"469",
      "title":"Readings in Actuarial Science 2"
    },
    {
      "course_id":"011760",
      "subject":"ACTSC",
      "catalog_number":"471",
      "title":"Advanced Corporate Finance"
    },
    {
      "course_id":"013389",
      "subject":"ACTSC",
      "catalog_number":"611",
      "title":"Financial Mathematics I"
    },
    {
      "course_id":"013390",
      "subject":"ACTSC",
      "catalog_number":"612",
      "title":"Life Insurance Mathematics I"
    },
    {
      "course_id":"013391",
      "subject":"ACTSC",
      "catalog_number":"613",
      "title":"Statistics for Actuarial Science"
    },
    {
      "course_id":"013392",
      "subject":"ACTSC",
      "catalog_number":"614",
      "title":"Corporate Finance"
    },
    {
      "course_id":"013393",
      "subject":"ACTSC",
      "catalog_number":"615",
      "title":"Economics"
    },
    {
      "course_id":"013406",
      "subject":"ACTSC",
      "catalog_number":"621",
      "title":"Financial Mathematics II"
    },
    {
      "course_id":"013395",
      "subject":"ACTSC",
      "catalog_number":"622",
      "title":"Life Insurance Mathematics II"
    },
    {
      "course_id":"013396",
      "subject":"ACTSC",
      "catalog_number":"623",
      "title":"Applied Statistics"
    },
    {
      "course_id":"013397",
      "subject":"ACTSC",
      "catalog_number":"624",
      "title":"Stochastic Processes for Actuarial Science"
    },
    {
      "course_id":"013398",
      "subject":"ACTSC",
      "catalog_number":"625",
      "title":"Casualty and Health Insurance Mathematics"
    },
    {
      "course_id":"013399",
      "subject":"ACTSC",
      "catalog_number":"631",
      "title":"Financial Mathematics III"
    },
    {
      "course_id":"013400",
      "subject":"ACTSC",
      "catalog_number":"632",
      "title":"Life Insurance Mathematics III"
    },
    {
      "course_id":"013401",
      "subject":"ACTSC",
      "catalog_number":"633",
      "title":"Actuarial Risk Management"
    },
    {
      "course_id":"013402",
      "subject":"ACTSC",
      "catalog_number":"634",
      "title":"Quantitative Risk Management"
    },
    {
      "course_id":"013403",
      "subject":"ACTSC",
      "catalog_number":"635",
      "title":"Profession Communications in Actuarial Science"
    },
    {
      "course_id":"009455",
      "subject":"ACTSC",
      "catalog_number":"690",
      "title":"Literature & Research Studies"
    },
    {
      "course_id":"000071",
      "subject":"ACTSC",
      "catalog_number":"831",
      "title":"Loss Models 1"
    },
    {
      "course_id":"000072",
      "subject":"ACTSC",
      "catalog_number":"832",
      "title":"Loss Models 2"
    },
    {
      "course_id":"000073",
      "subject":"ACTSC",
      "catalog_number":"833",
      "title":"Analysis of Mortality Data"
    },
    {
      "course_id":"010064",
      "subject":"ACTSC",
      "catalog_number":"845",
      "title":"Quantitative Risk Management"
    },
    {
      "course_id":"011270",
      "subject":"ACTSC",
      "catalog_number":"846",
      "title":"Mathematical Models in Finance"
    },
    {
      "course_id":"000076",
      "subject":"ACTSC",
      "catalog_number":"853",
      "title":"Basic Pension Mathematics"
    },
    {
      "course_id":"000078",
      "subject":"ACTSC",
      "catalog_number":"855",
      "title":"Advanced Life Insurance Practice"
    },
    {
      "course_id":"011273",
      "subject":"ACTSC",
      "catalog_number":"862",
      "title":"Introduction to Property and Casualty Pricing"
    },
    {
      "course_id":"000080",
      "subject":"ACTSC",
      "catalog_number":"863",
      "title":"Introduction fo Property and Casuality Loss Reserving"
    },
    {
      "course_id":"013085",
      "subject":"ACTSC",
      "catalog_number":"936",
      "title":"Longitudinal Data Analysis"
    },
    {
      "course_id":"000082",
      "subject":"ACTSC",
      "catalog_number":"961",
      "title":"Mathematical Methods of Loss Reserving"
    },
    {
      "course_id":"011274",
      "subject":"ACTSC",
      "catalog_number":"963",
      "title":"Insurance Surplus Mathematics"
    },
    {
      "course_id":"011275",
      "subject":"ACTSC",
      "catalog_number":"964",
      "title":"Insurance Solvency"
    },
    {
      "course_id":"011276",
      "subject":"ACTSC",
      "catalog_number":"965",
      "title":"Extreme Value Theory"
    },
    {
      "course_id":"011686",
      "subject":"ACTSC",
      "catalog_number":"966",
      "title":"Aggregate Claims Models"
    },
    {
      "course_id":"000044",
      "subject":"ACTSC",
      "catalog_number":"970",
      "title":"Finance 1"
    },
    {
      "course_id":"000045",
      "subject":"ACTSC",
      "catalog_number":"971",
      "title":"Finance 2"
    },
    {
      "course_id":"000046",
      "subject":"ACTSC",
      "catalog_number":"972",
      "title":"Finance 3"
    },
    {
      "course_id":"011622",
      "subject":"ACTSC",
      "catalog_number":"973",
      "title":"Portfolio Optimization"
    },
    {
      "course_id":"014063",
      "subject":"ACTSC",
      "catalog_number":"974",
      "title":"Financial Econometrics"
    },
    {
      "course_id":"000083",
      "subject":"ACTSC",
      "catalog_number":"980",
      "title":"Social Insurance"
    },
    {
      "course_id":"000085",
      "subject":"ACTSC",
      "catalog_number":"991",
      "title":"Topics in Actuarial Science"
    },
    {
      "course_id":"013227",
      "subject":"ADMGT",
      "catalog_number":"601",
      "title":"Introduction to Financial and Managerial Accounting"
    },
    {
      "course_id":"000093",
      "subject":"ACTSC",
      "catalog_number":"992",
      "title":"Seminar in Actuarial Science"
    },
    {
      "course_id":"011404",
      "subject":"AFM",
      "catalog_number":"101",
      "title":"Introduction to Financial Accounting"
    },
    {
      "course_id":"011700",
      "subject":"AFM",
      "catalog_number":"102",
      "title":"Introduction to Managerial Accounting"
    },
    {
      "course_id":"013719",
      "subject":"AFM",
      "catalog_number":"121",
      "title":"Introduction to Global Financial Markets"
    },
    {
      "course_id":"003239",
      "subject":"AFM",
      "catalog_number":"123",
      "title":"Accounting Information for Managers"
    },
    {
      "course_id":"003243",
      "subject":"AFM",
      "catalog_number":"131",
      "title":"Introduction to Business in North America"
    },
    {
      "course_id":"011411",
      "subject":"AFM",
      "catalog_number":"201",
      "title":"Introduction to Professional Practice"
    },
    {
      "course_id":"013739",
      "subject":"AFM",
      "catalog_number":"202",
      "title":"Introduction to Public Practice"
    },
    {
      "course_id":"013740",
      "subject":"AFM",
      "catalog_number":"203",
      "title":"Introduction to Decision Support"
    },
    {
      "course_id":"013741",
      "subject":"AFM",
      "catalog_number":"204",
      "title":"Introduction to Applied Finance"
    },
    {
      "course_id":"013742",
      "subject":"AFM",
      "catalog_number":"211",
      "title":"Connections to Business Context"
    },
    {
      "course_id":"003247",
      "subject":"AFM",
      "catalog_number":"231",
      "title":"Business Law"
    },
    {
      "course_id":"010334",
      "subject":"AFM",
      "catalog_number":"241",
      "title":"Introduction to Business Information Technology"
    },
    {
      "course_id":"003257",
      "subject":"AFM",
      "catalog_number":"271",
      "title":"Managerial Finance 1"
    },
    {
      "course_id":"011750",
      "subject":"AFM",
      "catalog_number":"272",
      "title":"Corporate Finance 1"
    },
    {
      "course_id":"011413",
      "subject":"AFM",
      "catalog_number":"432",
      "title":"Legal Environment and Corporate Governance"
    },
    {
      "course_id":"003257",
      "subject":"AFM",
      "catalog_number":"273",
      "title":"Managerial Finance 1"
    },
    {
      "course_id":"003258",
      "subject":"AFM",
      "catalog_number":"274",
      "title":"Managerial Finance 2"
    },
    {
      "course_id":"013743",
      "subject":"AFM",
      "catalog_number":"280",
      "title":"Introduction to Organizational Behaviour"
    },
    {
      "course_id":"003253",
      "subject":"AFM",
      "catalog_number":"291",
      "title":"Intermediate Financial Accounting 1"
    },
    {
      "course_id":"013744",
      "subject":"AFM",
      "catalog_number":"311",
      "title":"Connections to Ethical Context"
    },
    {
      "course_id":"013726",
      "subject":"AFM",
      "catalog_number":"321",
      "title":"Personal Financial Planning"
    },
    {
      "course_id":"011702",
      "subject":"AFM",
      "catalog_number":"322",
      "title":"Derivative Securities"
    },
    {
      "course_id":"013727",
      "subject":"AFM",
      "catalog_number":"323",
      "title":"Quantitative Foundations for Finance"
    },
    {
      "course_id":"014473",
      "subject":"AFM",
      "catalog_number":"328",
      "title":"Investment Management - Junior Analyst"
    },
    {
      "course_id":"014474",
      "subject":"AFM",
      "catalog_number":"329",
      "title":"Investment Management - Senior Analyst"
    },
    {
      "course_id":"003269",
      "subject":"AFM",
      "catalog_number":"331",
      "title":"Business Strategy"
    },
    {
      "course_id":"011974",
      "subject":"AFM",
      "catalog_number":"332",
      "title":"Accounting, Assurance, and the Law"
    },
    {
      "course_id":"012769",
      "subject":"AFM",
      "catalog_number":"333",
      "title":"International Business"
    },
    {
      "course_id":"003273",
      "subject":"AFM",
      "catalog_number":"341",
      "title":"Accounting Information Systems"
    },
    {
      "course_id":"003275",
      "subject":"AFM",
      "catalog_number":"351",
      "title":"Audit Strategy"
    },
    {
      "course_id":"003278",
      "subject":"AFM",
      "catalog_number":"352",
      "title":"Comprehensive\/Operational Auditing"
    },
    {
      "course_id":"003279",
      "subject":"AFM",
      "catalog_number":"361",
      "title":"Taxation 1"
    },
    {
      "course_id":"013745",
      "subject":"AFM",
      "catalog_number":"362",
      "title":"Taxation 1 - Foundations"
    },
    {
      "course_id":"013913",
      "subject":"AFM",
      "catalog_number":"363",
      "title":"Taxation 2 - Integration"
    },
    {
      "course_id":"003258",
      "subject":"AFM",
      "catalog_number":"371",
      "title":"Managerial Finance 2"
    },
    {
      "course_id":"011751",
      "subject":"AFM",
      "catalog_number":"372",
      "title":"Corporate Finance 2"
    },
    {
      "course_id":"011414",
      "subject":"AFM",
      "catalog_number":"373",
      "title":"Cases and Applications in Corporate Finance"
    },
    {
      "course_id":"011415",
      "subject":"AFM",
      "catalog_number":"382",
      "title":"Performance Measurement and Organization Control"
    },
    {
      "course_id":"003261",
      "subject":"AFM",
      "catalog_number":"391",
      "title":"Intermediate Financial Accounting 2"
    },
    {
      "course_id":"003262",
      "subject":"AFM",
      "catalog_number":"401",
      "title":"Accounting Theory"
    },
    {
      "course_id":"013746",
      "subject":"AFM",
      "catalog_number":"411",
      "title":"Connections Across Competencies for Accounting Professionals"
    },
    {
      "course_id":"013747",
      "subject":"AFM",
      "catalog_number":"412",
      "title":"Connections Across Competencies for Finance Professionals"
    },
    {
      "course_id":"003265",
      "subject":"AFM",
      "catalog_number":"415",
      "title":"Special Topics"
    },
    {
      "course_id":"013729",
      "subject":"AFM",
      "catalog_number":"416",
      "title":"Special Topics in Finance"
    },
    {
      "course_id":"013728",
      "subject":"AFM",
      "catalog_number":"417",
      "title":"Special Topics in Accounting"
    },
    {
      "course_id":"014397",
      "subject":"AFM",
      "catalog_number":"418",
      "title":"Special Topics in Finance or Accounting"
    },
    {
      "course_id":"013732",
      "subject":"AFM",
      "catalog_number":"422",
      "title":"Management of Financial Institutions"
    },
    {
      "course_id":"014855",
      "subject":"AFM",
      "catalog_number":"423",
      "title":"Topics in Financial Econometrics"
    },
    {
      "course_id":"003284",
      "subject":"AFM",
      "catalog_number":"424",
      "title":"Equity Investments"
    },
    {
      "course_id":"011703",
      "subject":"AFM",
      "catalog_number":"425",
      "title":"Fixed Income Securities"
    },
    {
      "course_id":"014475",
      "subject":"AFM",
      "catalog_number":"428",
      "title":"Investment Management - Junior Portfolio Manager"
    },
    {
      "course_id":"014478",
      "subject":"AFM",
      "catalog_number":"429",
      "title":"Investment Management - Senior Portfolio Manager"
    },
    {
      "course_id":"003270",
      "subject":"AFM",
      "catalog_number":"431",
      "title":"Professional Ethics for Financial Managers"
    },
    {
      "course_id":"003269",
      "subject":"AFM",
      "catalog_number":"433",
      "title":"Business Strategy"
    },
    {
      "course_id":"013748",
      "subject":"AFM",
      "catalog_number":"434",
      "title":"Governance and Enterprise Risk Management for Global Organizations"
    },
    {
      "course_id":"011178",
      "subject":"AFM",
      "catalog_number":"442",
      "title":"E-business: Enterprise Systems"
    },
    {
      "course_id":"011179",
      "subject":"AFM",
      "catalog_number":"443",
      "title":"E-business: Introduction to Electronic Commerce"
    },
    {
      "course_id":"003275",
      "subject":"AFM",
      "catalog_number":"451",
      "title":"Audit Strategy"
    },
    {
      "course_id":"003278",
      "subject":"AFM",
      "catalog_number":"452",
      "title":"Comprehensive\/Operational Auditing"
    },
    {
      "course_id":"003280",
      "subject":"AFM",
      "catalog_number":"461",
      "title":"Taxation 2"
    },
    {
      "course_id":"013914",
      "subject":"AFM",
      "catalog_number":"462",
      "title":"Taxation 3 - Tax Planning Topics"
    },
    {
      "course_id":"011414",
      "subject":"AFM",
      "catalog_number":"471",
      "title":"Cases and Applications in Corporate Finance"
    },
    {
      "course_id":"003284",
      "subject":"AFM",
      "catalog_number":"472",
      "title":"Equity Investments"
    },
    {
      "course_id":"011701",
      "subject":"AFM",
      "catalog_number":"473",
      "title":"Advanced Topics in Corporate Finance"
    },
    {
      "course_id":"011702",
      "subject":"AFM",
      "catalog_number":"474",
      "title":"Derivative Securities"
    },
    {
      "course_id":"011703",
      "subject":"AFM",
      "catalog_number":"475",
      "title":"Fixed Income Securities"
    },
    {
      "course_id":"011760",
      "subject":"AFM",
      "catalog_number":"476",
      "title":"Advanced Corporate Finance"
    },
    {
      "course_id":"013730",
      "subject":"AFM",
      "catalog_number":"477",
      "title":"Mergers and Acquisitions"
    },
    {
      "course_id":"013749",
      "subject":"AFM",
      "catalog_number":"478",
      "title":"International Financial Management"
    },
    {
      "course_id":"003260",
      "subject":"AFM",
      "catalog_number":"481",
      "title":"Cost Management Systems"
    },
    {
      "course_id":"011415",
      "subject":"AFM",
      "catalog_number":"482",
      "title":"Performance Measurement and Organization Control"
    },
    {
      "course_id":"014229",
      "subject":"AFM",
      "catalog_number":"483",
      "title":"Applications of Analytics to Business"
    },
    {
      "course_id":"014230",
      "subject":"AFM",
      "catalog_number":"484",
      "title":"Advanced Management Control Systems"
    },
    {
      "course_id":"003285",
      "subject":"AFM",
      "catalog_number":"491",
      "title":"Advanced Financial Accounting"
    },
    {
      "course_id":"011704",
      "subject":"AFM",
      "catalog_number":"492",
      "title":"Financial Statement Analysis"
    },
    {
      "course_id":"003286",
      "subject":"AFM",
      "catalog_number":"501",
      "title":"Contemporary Issues in Assurance and Accounting"
    },
    {
      "course_id":"003287",
      "subject":"AFM",
      "catalog_number":"502",
      "title":"Control Systems in a Computer Environment"
    },
    {
      "course_id":"003288",
      "subject":"AFM",
      "catalog_number":"503",
      "title":"Issues and Problems in Accounting Practice"
    },
    {
      "course_id":"003289",
      "subject":"AFM",
      "catalog_number":"504",
      "title":"Issues and Problems in External Reporting"
    },
    {
      "course_id":"013580",
      "subject":"AHS",
      "catalog_number":"150",
      "title":"Foundations of Human Anatomy and Physiology"
    },
    {
      "course_id":"003320",
      "subject":"AMATH",
      "catalog_number":"261",
      "title":"Classical Mechanics and Special Relativity"
    },
    {
      "course_id":"013715",
      "subject":"AHS",
      "catalog_number":"782",
      "title":"Selected Topics in Applied Health Sciences"
    },
    {
      "course_id":"003316",
      "subject":"AMATH",
      "catalog_number":"231",
      "title":"Calculus 4"
    },
    {
      "course_id":"011363",
      "subject":"AMATH",
      "catalog_number":"242",
      "title":"Introduction to Computational Mathematics"
    },
    {
      "course_id":"003317",
      "subject":"AMATH",
      "catalog_number":"250",
      "title":"Introduction to Differential Equations"
    },
    {
      "course_id":"014120",
      "subject":"AMATH",
      "catalog_number":"251",
      "title":"Introduction to Differential Equations (Advanced level)"
    },
    {
      "course_id":"013864",
      "subject":"AMATH",
      "catalog_number":"271",
      "title":"Introduction to Theoretical Mechanics"
    },
    {
      "course_id":"013317",
      "subject":"AMATH",
      "catalog_number":"310",
      "title":"Environmental Informatics"
    },
    {
      "course_id":"003323",
      "subject":"AMATH",
      "catalog_number":"331",
      "title":"Applied Real Analysis"
    },
    {
      "course_id":"003324",
      "subject":"AMATH",
      "catalog_number":"332",
      "title":"Applied Complex Analysis"
    },
    {
      "course_id":"011451",
      "subject":"AMATH",
      "catalog_number":"342",
      "title":"Computational Methods for Differential Equations"
    },
    {
      "course_id":"003328",
      "subject":"AMATH",
      "catalog_number":"343",
      "title":"Discrete Models in Applied Mathematics"
    },
    {
      "course_id":"012744",
      "subject":"AMATH",
      "catalog_number":"350",
      "title":"Differential Equations for Business and Economics"
    },
    {
      "course_id":"003329",
      "subject":"AMATH",
      "catalog_number":"351",
      "title":"Ordinary Differential Equations 2"
    },
    {
      "course_id":"003330",
      "subject":"AMATH",
      "catalog_number":"353",
      "title":"Partial Differential Equations 1"
    },
    {
      "course_id":"003331",
      "subject":"AMATH",
      "catalog_number":"361",
      "title":"Continuum Mechanics"
    },
    {
      "course_id":"003338",
      "subject":"AMATH",
      "catalog_number":"373",
      "title":"Quantum Theory 1"
    },
    {
      "course_id":"011910",
      "subject":"AMATH",
      "catalog_number":"382",
      "title":"Computational Modelling of Cellular Systems"
    },
    {
      "course_id":"012282",
      "subject":"AMATH",
      "catalog_number":"391",
      "title":"From Fourier to Wavelets"
    },
    {
      "course_id":"011448",
      "subject":"AMATH",
      "catalog_number":"442",
      "title":"Computational Methods for Partial Differential Equations"
    },
    {
      "course_id":"011443",
      "subject":"AMATH",
      "catalog_number":"444",
      "title":"Applications of Computational Differential Equations"
    },
    {
      "course_id":"003354",
      "subject":"AMATH",
      "catalog_number":"451",
      "title":"Introduction to Dynamical Systems"
    },
    {
      "course_id":"003355",
      "subject":"AMATH",
      "catalog_number":"453",
      "title":"Partial Differential Equations 2"
    },
    {
      "course_id":"003356",
      "subject":"AMATH",
      "catalog_number":"455",
      "title":"Control Theory"
    },
    {
      "course_id":"003357",
      "subject":"AMATH",
      "catalog_number":"456",
      "title":"Calculus of Variations"
    },
    {
      "course_id":"003359",
      "subject":"AMATH",
      "catalog_number":"463",
      "title":"Fluid Mechanics"
    },
    {
      "course_id":"003369",
      "subject":"AMATH",
      "catalog_number":"473",
      "title":"Quantum Theory 2"
    },
    {
      "course_id":"003371",
      "subject":"AMATH",
      "catalog_number":"475",
      "title":"Introduction to General Relativity"
    },
    {
      "course_id":"003382",
      "subject":"AMATH",
      "catalog_number":"495",
      "title":"Reading Course"
    },
    {
      "course_id":"011278",
      "subject":"AMATH",
      "catalog_number":"655",
      "title":"Control Theory"
    },
    {
      "course_id":"011279",
      "subject":"AMATH",
      "catalog_number":"663",
      "title":"Fluid Mechanics"
    },
    {
      "course_id":"011280",
      "subject":"AMATH",
      "catalog_number":"673",
      "title":"Quantum Mechanics"
    },
    {
      "course_id":"011281",
      "subject":"AMATH",
      "catalog_number":"675",
      "title":"General Relativity"
    },
    {
      "course_id":"000116",
      "subject":"AMATH",
      "catalog_number":"731",
      "title":"Applied Functional Analysis"
    },
    {
      "course_id":"011283",
      "subject":"AMATH",
      "catalog_number":"732",
      "title":"Asymptotic Analysis and Perturbation Theory"
    },
    {
      "course_id":"012670",
      "subject":"AMATH",
      "catalog_number":"740",
      "title":"Numerical Analysis"
    },
    {
      "course_id":"000724",
      "subject":"AMATH",
      "catalog_number":"741",
      "title":"Numerical Solution of Partial Differential Equations"
    },
    {
      "course_id":"000118",
      "subject":"AMATH",
      "catalog_number":"751",
      "title":"Advanced Ordinary Differential Equations"
    },
    {
      "course_id":"000119",
      "subject":"AMATH",
      "catalog_number":"753",
      "title":"Advanced Partial Differential Equations"
    },
    {
      "course_id":"011284",
      "subject":"AMATH",
      "catalog_number":"777",
      "title":"Stochastic Processes in the Physical Sciences"
    },
    {
      "course_id":"011285",
      "subject":"AMATH",
      "catalog_number":"851",
      "title":"Stability Theory and Applications"
    },
    {
      "course_id":"000132",
      "subject":"AMATH",
      "catalog_number":"855",
      "title":"Advanced Systems Analysis and Control"
    },
    {
      "course_id":"000133",
      "subject":"AMATH",
      "catalog_number":"863",
      "title":"Hydrodynamic Stability and Turbulence"
    },
    {
      "course_id":"000134",
      "subject":"AMATH",
      "catalog_number":"867",
      "title":"Dispersive and Nonlinear Waves"
    },
    {
      "course_id":"011589",
      "subject":"AMATH",
      "catalog_number":"871",
      "title":"Quantum Information Processing"
    },
    {
      "course_id":"012151",
      "subject":"AMATH",
      "catalog_number":"872",
      "title":"Introduction to Quantum Field Theory for Cosmology"
    },
    {
      "course_id":"000135",
      "subject":"AMATH",
      "catalog_number":"873",
      "title":"Introduction to Quantum Field Theory"
    },
    {
      "course_id":"010439",
      "subject":"AMATH",
      "catalog_number":"874",
      "title":"Advanced techniques in General Relativity and Applications to Black Holes"
    },
    {
      "course_id":"011282",
      "subject":"AMATH",
      "catalog_number":"875",
      "title":"Introduction to General Relativity with Applications to Cosmology"
    },
    {
      "course_id":"012567",
      "subject":"AMATH",
      "catalog_number":"876",
      "title":"Open Quantum Systems"
    },
    {
      "course_id":"013468",
      "subject":"AMATH",
      "catalog_number":"881",
      "title":"Introduction to Mathematical Oncology"
    },
    {
      "course_id":"013469",
      "subject":"AMATH",
      "catalog_number":"882",
      "title":"Mathematical Cell Biology"
    },
    {
      "course_id":"011357",
      "subject":"AMATH",
      "catalog_number":"900",
      "title":"Topics in Applied Mathematics"
    },
    {
      "course_id":"011692",
      "subject":"BET",
      "catalog_number":"606",
      "title":"Entrepreneurial Applications of Digital Media"
    },
    {
      "course_id":"003389",
      "subject":"ANTH",
      "catalog_number":"101",
      "title":"Human and Cultural Evolution"
    },
    {
      "course_id":"003391",
      "subject":"ANTH",
      "catalog_number":"102",
      "title":"Introduction to Social and Cultural Anthropology"
    },
    {
      "course_id":"003396",
      "subject":"ANTH",
      "catalog_number":"201",
      "title":"Archaeological Anthropology"
    },
    {
      "course_id":"003399",
      "subject":"ANTH",
      "catalog_number":"202",
      "title":"Social and Cultural Anthropology"
    },
    {
      "course_id":"003422",
      "subject":"ANTH",
      "catalog_number":"233",
      "title":"Inuit and Eskimo Cultures"
    },
    {
      "course_id":"003426",
      "subject":"ANTH",
      "catalog_number":"260",
      "title":"Human Evolution"
    },
    {
      "course_id":"003427",
      "subject":"ANTH",
      "catalog_number":"261",
      "title":"Primate Behaviour"
    },
    {
      "course_id":"003432",
      "subject":"ANTH",
      "catalog_number":"290",
      "title":"Visual Anthropology"
    },
    {
      "course_id":"003433",
      "subject":"ANTH",
      "catalog_number":"300",
      "title":"Practicing Anthropology"
    },
    {
      "course_id":"013559",
      "subject":"ANTH",
      "catalog_number":"302",
      "title":"Anthropology of Violence: Political Conflict and Change"
    },
    {
      "course_id":"013560",
      "subject":"ANTH",
      "catalog_number":"303",
      "title":"Anthropology of Digital Media"
    },
    {
      "course_id":"014127",
      "subject":"ANTH",
      "catalog_number":"305",
      "title":"Paleopathology of Health and Disease"
    },
    {
      "course_id":"003445",
      "subject":"ANTH",
      "catalog_number":"320",
      "title":"Studies in Hunter-Gatherer Archaeology"
    },
    {
      "course_id":"003446",
      "subject":"ANTH",
      "catalog_number":"321",
      "title":"Archaeology of Complex Cultures"
    },
    {
      "course_id":"003448",
      "subject":"ANTH",
      "catalog_number":"322",
      "title":"The Archaeology of the Great Lakes Area"
    },
    {
      "course_id":"003452",
      "subject":"ANTH",
      "catalog_number":"330",
      "title":"Environmental Anthropology"
    },
    {
      "course_id":"003460",
      "subject":"ANTH",
      "catalog_number":"345",
      "title":"Directed Research in Anthropology"
    },
    {
      "course_id":"011871",
      "subject":"ANTH",
      "catalog_number":"347",
      "title":"Medical Anthropology"
    },
    {
      "course_id":"013324",
      "subject":"ANTH",
      "catalog_number":"348",
      "title":"Anthropology of Tourism"
    },
    {
      "course_id":"003462",
      "subject":"ANTH",
      "catalog_number":"351",
      "title":"Indigenous Practices & Relations: A Comparative Approach"
    },
    {
      "course_id":"003463",
      "subject":"ANTH",
      "catalog_number":"352",
      "title":"Anthropological Thought"
    },
    {
      "course_id":"009886",
      "subject":"ANTH",
      "catalog_number":"355",
      "title":"Human Osteology"
    },
    {
      "course_id":"014128",
      "subject":"ANTH",
      "catalog_number":"361",
      "title":"Biocultural Examination of Primate Conservation"
    },
    {
      "course_id":"003466",
      "subject":"ANTH",
      "catalog_number":"365",
      "title":"Human Evolution"
    },
    {
      "course_id":"003945",
      "subject":"ANTH",
      "catalog_number":"370",
      "title":"Issues in Contemporary Native Communities in Canada"
    },
    {
      "course_id":"012624",
      "subject":"ANTH",
      "catalog_number":"371",
      "title":"Anthropological Field Experience"
    },
    {
      "course_id":"003471",
      "subject":"ANTH",
      "catalog_number":"390A",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003472",
      "subject":"ANTH",
      "catalog_number":"390B",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003473",
      "subject":"ANTH",
      "catalog_number":"391",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003474",
      "subject":"ANTH",
      "catalog_number":"393",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"012749",
      "subject":"ANTH",
      "catalog_number":"395",
      "title":"Anthropological Study Abroad"
    },
    {
      "course_id":"003475",
      "subject":"ANTH",
      "catalog_number":"400",
      "title":"Special Topics in Anthropology"
    },
    {
      "course_id":"013561",
      "subject":"ANTH",
      "catalog_number":"402",
      "title":"Palestine\/Israel: Anthropological Perspectives"
    },
    {
      "course_id":"013991",
      "subject":"ANTH",
      "catalog_number":"403",
      "title":"Anthropological Inquiry into the Origin of Language and Cultural Behaviour"
    },
    {
      "course_id":"009885",
      "subject":"ANTH",
      "catalog_number":"440",
      "title":"Archaeological Analysis and Interpretation"
    },
    {
      "course_id":"011982",
      "subject":"ANTH",
      "catalog_number":"455",
      "title":"Skeletal Biology and Forensics"
    },
    {
      "course_id":"003482",
      "subject":"ANTH",
      "catalog_number":"460",
      "title":"Human Adaptation and Variation"
    },
    {
      "course_id":"009887",
      "subject":"ANTH",
      "catalog_number":"470",
      "title":"Archaeological Field Methods"
    },
    {
      "course_id":"003485",
      "subject":"ANTH",
      "catalog_number":"492A",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003486",
      "subject":"ANTH",
      "catalog_number":"492B",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003487",
      "subject":"ANTH",
      "catalog_number":"495",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003488",
      "subject":"ANTH",
      "catalog_number":"497",
      "title":"Reading in Anthropology"
    },
    {
      "course_id":"003489",
      "subject":"ANTH",
      "catalog_number":"499A",
      "title":"Honours Essay"
    },
    {
      "course_id":"003490",
      "subject":"ANTH",
      "catalog_number":"499B",
      "title":"Honours Essay"
    },
    {
      "course_id":"012727",
      "subject":"ANTH",
      "catalog_number":"600",
      "title":"Public Issues Anthropology"
    },
    {
      "course_id":"012968",
      "subject":"ANTH",
      "catalog_number":"604",
      "title":"Human Development in a Cross-Cultural Perspective"
    },
    {
      "course_id":"012732",
      "subject":"ANTH",
      "catalog_number":"605",
      "title":"Selected Topics in Theory and Research"
    },
    {
      "course_id":"012729",
      "subject":"ANTH",
      "catalog_number":"608",
      "title":"Anthropological Theory"
    },
    {
      "course_id":"012728",
      "subject":"ANTH",
      "catalog_number":"614",
      "title":"Research Methods"
    },
    {
      "course_id":"012730",
      "subject":"ANTH",
      "catalog_number":"655",
      "title":"Skeletal Biology and Forensics"
    },
    {
      "course_id":"013815",
      "subject":"ANTH",
      "catalog_number":"659",
      "title":"Conservation, Communities and Globalization"
    },
    {
      "course_id":"012737",
      "subject":"ANTH",
      "catalog_number":"660",
      "title":"Reading Course"
    },
    {
      "course_id":"013807",
      "subject":"ANTH",
      "catalog_number":"661",
      "title":"Research Seminar in Public Issues Anthropology"
    },
    {
      "course_id":"012731",
      "subject":"ANTH",
      "catalog_number":"662",
      "title":"Human Adaptation and Evolution"
    },
    {
      "course_id":"012198",
      "subject":"APPLS",
      "catalog_number":"205R",
      "title":"Second Language Acquisition"
    },
    {
      "course_id":"012718",
      "subject":"APPLS",
      "catalog_number":"301",
      "title":"Language, Culture, and Identity"
    },
    {
      "course_id":"011980",
      "subject":"APPLS",
      "catalog_number":"304R",
      "title":"Second Language Teaching Methodology"
    },
    {
      "course_id":"012356",
      "subject":"APPLS",
      "catalog_number":"306R",
      "title":"Second Language Assessment and Testing"
    },
    {
      "course_id":"013720",
      "subject":"ARBUS",
      "catalog_number":"100",
      "title":"Introduction to Arts and Business"
    },
    {
      "course_id":"003243",
      "subject":"ARBUS",
      "catalog_number":"101",
      "title":"Introduction to Business in North America"
    },
    {
      "course_id":"003239",
      "subject":"ARBUS",
      "catalog_number":"102",
      "title":"Accounting Information for Managers"
    },
    {
      "course_id":"014241",
      "subject":"ARBUS",
      "catalog_number":"200",
      "title":"Entrepreneurship Principles and Practices"
    },
    {
      "course_id":"007266",
      "subject":"ARBUS",
      "catalog_number":"202",
      "title":"Professional and Business Ethics"
    },
    {
      "course_id":"013722",
      "subject":"ARBUS",
      "catalog_number":"300",
      "title":"Practical Business Skills"
    },
    {
      "course_id":"012769",
      "subject":"ARBUS",
      "catalog_number":"301",
      "title":"International Business"
    },
    {
      "course_id":"004936",
      "subject":"ARBUS",
      "catalog_number":"302",
      "title":"Marketing: Principles of Marketing and Consumer Economics"
    },
    {
      "course_id":"013721",
      "subject":"ARBUS",
      "catalog_number":"400",
      "title":"Strategy and Program Integration"
    },
    {
      "course_id":"003491",
      "subject":"ARCH",
      "catalog_number":"100",
      "title":"An Introduction to Architecture"
    },
    {
      "course_id":"003492",
      "subject":"ARCH",
      "catalog_number":"110",
      "title":"Visual and Digital Media 1"
    },
    {
      "course_id":"003494",
      "subject":"ARCH",
      "catalog_number":"113",
      "title":"Visual and Digital Media 2"
    },
    {
      "course_id":"010395",
      "subject":"ARCH",
      "catalog_number":"125",
      "title":"Principles of Environmental Design"
    },
    {
      "course_id":"003496",
      "subject":"ARCH",
      "catalog_number":"142",
      "title":"Introduction to Cultural History"
    },
    {
      "course_id":"003497",
      "subject":"ARCH",
      "catalog_number":"143",
      "title":"The Ancient World and Foundations of Europe"
    },
    {
      "course_id":"003500",
      "subject":"ARCH",
      "catalog_number":"172",
      "title":"Building Construction 1"
    },
    {
      "course_id":"003520",
      "subject":"ARCH",
      "catalog_number":"173",
      "title":"Building Construction 2"
    },
    {
      "course_id":"015006",
      "subject":"ARCH",
      "catalog_number":"212",
      "title":"Digital Fabrication"
    },
    {
      "course_id":"003501",
      "subject":"ARCH",
      "catalog_number":"174",
      "title":"Experimental Courses"
    },
    {
      "course_id":"010127",
      "subject":"ARCH",
      "catalog_number":"175",
      "title":"Experimental Courses"
    },
    {
      "course_id":"003502",
      "subject":"ARCH",
      "catalog_number":"192",
      "title":"Design Studio"
    },
    {
      "course_id":"003503",
      "subject":"ARCH",
      "catalog_number":"193",
      "title":"Design Studio"
    },
    {
      "course_id":"012948",
      "subject":"ARCH",
      "catalog_number":"215",
      "title":"Communication Design"
    },
    {
      "course_id":"003541",
      "subject":"ARCH",
      "catalog_number":"226",
      "title":"Environmental Building Design"
    },
    {
      "course_id":"003515",
      "subject":"ARCH",
      "catalog_number":"246",
      "title":"Pre-Renaissance to Reformation"
    },
    {
      "course_id":"003516",
      "subject":"ARCH",
      "catalog_number":"247",
      "title":"Cultural History 4: Renaissance to Revolution"
    },
    {
      "course_id":"003518",
      "subject":"ARCH",
      "catalog_number":"252",
      "title":"Creative Problem Solving"
    },
    {
      "course_id":"012286",
      "subject":"ARCH",
      "catalog_number":"256",
      "title":"Introduction to Photography"
    },
    {
      "course_id":"003498",
      "subject":"ARCH",
      "catalog_number":"260",
      "title":"Principles of Structures"
    },
    {
      "course_id":"003544",
      "subject":"ARCH",
      "catalog_number":"272",
      "title":"Interior Environments: Acoustics and Lighting"
    },
    {
      "course_id":"010396",
      "subject":"ARCH",
      "catalog_number":"273",
      "title":"Environmental Systems"
    },
    {
      "course_id":"003521",
      "subject":"ARCH",
      "catalog_number":"274",
      "title":"Experimental Course"
    },
    {
      "course_id":"010175",
      "subject":"ARCH",
      "catalog_number":"275",
      "title":"Experimental Courses"
    },
    {
      "course_id":"003529",
      "subject":"ARCH",
      "catalog_number":"276",
      "title":"Timber: Design, Structure and Construction"
    },
    {
      "course_id":"014259",
      "subject":"ARCH",
      "catalog_number":"277",
      "title":"Timber: Design, Structure and Construction for Engineers"
    },
    {
      "course_id":"003530",
      "subject":"ARCH",
      "catalog_number":"284",
      "title":"Architectural Research"
    },
    {
      "course_id":"003531",
      "subject":"ARCH",
      "catalog_number":"285",
      "title":"Architectural Research"
    },
    {
      "course_id":"003532",
      "subject":"ARCH",
      "catalog_number":"292",
      "title":"Design Studio"
    },
    {
      "course_id":"003533",
      "subject":"ARCH",
      "catalog_number":"293",
      "title":"Design Studio"
    },
    {
      "course_id":"011139",
      "subject":"ARCH",
      "catalog_number":"314",
      "title":"Digital Design"
    },
    {
      "course_id":"003512",
      "subject":"ARCH",
      "catalog_number":"327",
      "title":"Architecture of the Urban Environment"
    },
    {
      "course_id":"014260",
      "subject":"ARCH",
      "catalog_number":"328",
      "title":"Approaches to Architecture and Urbanism"
    },
    {
      "course_id":"014261",
      "subject":"ARCH",
      "catalog_number":"331",
      "title":"Working with Wood"
    },
    {
      "course_id":"010398",
      "subject":"ARCH",
      "catalog_number":"332",
      "title":"Design\/Build Workshop"
    },
    {
      "course_id":"010399",
      "subject":"ARCH",
      "catalog_number":"342",
      "title":"Modern Architecture"
    },
    {
      "course_id":"003536",
      "subject":"ARCH",
      "catalog_number":"343",
      "title":"Enlightenment, Romanticism and the 19th Century"
    },
    {
      "course_id":"003535",
      "subject":"ARCH",
      "catalog_number":"345",
      "title":"Architectural Theory 1850-1990"
    },
    {
      "course_id":"014262",
      "subject":"ARCH",
      "catalog_number":"346",
      "title":"Competitions in Architecture"
    },
    {
      "course_id":"014263",
      "subject":"ARCH",
      "catalog_number":"347",
      "title":"Philosophy in Architecture"
    },
    {
      "course_id":"003539",
      "subject":"ARCH",
      "catalog_number":"362",
      "title":"Steel and Concrete: Design, Structure and Construction"
    },
    {
      "course_id":"011141",
      "subject":"ARCH",
      "catalog_number":"364",
      "title":"Building Science"
    },
    {
      "course_id":"012862",
      "subject":"ARCH",
      "catalog_number":"365",
      "title":"Structural Design Build Workshop"
    },
    {
      "course_id":"003545",
      "subject":"ARCH",
      "catalog_number":"374",
      "title":"Experimental Courses"
    },
    {
      "course_id":"003549",
      "subject":"ARCH",
      "catalog_number":"375",
      "title":"Experimental Courses"
    },
    {
      "course_id":"003554",
      "subject":"ARCH",
      "catalog_number":"384",
      "title":"Architectural Research"
    },
    {
      "course_id":"003555",
      "subject":"ARCH",
      "catalog_number":"385",
      "title":"Architectural Research"
    },
    {
      "course_id":"003556",
      "subject":"ARCH",
      "catalog_number":"392",
      "title":"Design Studio"
    },
    {
      "course_id":"003557",
      "subject":"ARCH",
      "catalog_number":"393",
      "title":"Option Design Studio"
    },
    {
      "course_id":"009510",
      "subject":"ARCH",
      "catalog_number":"425",
      "title":"Theory and Design of the Contemporary Landscape"
    },
    {
      "course_id":"011174",
      "subject":"ARCH",
      "catalog_number":"442",
      "title":"Contemporary Architectural Theory"
    },
    {
      "course_id":"011766",
      "subject":"ARCH",
      "catalog_number":"443",
      "title":"Architecture and Film"
    },
    {
      "course_id":"003559",
      "subject":"ARCH",
      "catalog_number":"446",
      "title":"Italian Urban History (Rome)"
    },
    {
      "course_id":"003561",
      "subject":"ARCH",
      "catalog_number":"448",
      "title":"Rome and the Campagna (Rome)"
    },
    {
      "course_id":"003562",
      "subject":"ARCH",
      "catalog_number":"449",
      "title":"The Development of Modern Italian Architecture (Rome)"
    },
    {
      "course_id":"010400",
      "subject":"ARCH",
      "catalog_number":"473",
      "title":"Technical Report"
    },
    {
      "course_id":"003567",
      "subject":"ARCH",
      "catalog_number":"474",
      "title":"Experimental Courses"
    },
    {
      "course_id":"003571",
      "subject":"ARCH",
      "catalog_number":"475",
      "title":"Experimental Courses"
    },
    {
      "course_id":"003575",
      "subject":"ARCH",
      "catalog_number":"484",
      "title":"Architectural Research"
    },
    {
      "course_id":"003577",
      "subject":"ARCH",
      "catalog_number":"485",
      "title":"Architectural Research"
    },
    {
      "course_id":"003579",
      "subject":"ARCH",
      "catalog_number":"492",
      "title":"Design Studio"
    },
    {
      "course_id":"003581",
      "subject":"ARCH",
      "catalog_number":"493",
      "title":"Design Studio\/Comprehensive Building Design"
    },
    {
      "course_id":"010627",
      "subject":"ARCH",
      "catalog_number":"611",
      "title":"Drawing, Representation and Practice"
    },
    {
      "course_id":"010628",
      "subject":"ARCH",
      "catalog_number":"612",
      "title":"Originality and Invention in Architecture"
    },
    {
      "course_id":"010629",
      "subject":"ARCH",
      "catalog_number":"613",
      "title":"Light, Colour and Darkness"
    },
    {
      "course_id":"013896",
      "subject":"ARCH",
      "catalog_number":"622",
      "title":"Urban Revitalization & Design"
    },
    {
      "course_id":"010643",
      "subject":"ARCH",
      "catalog_number":"623",
      "title":"Ecosystem Design for Urban Landscapes"
    },
    {
      "course_id":"010644",
      "subject":"ARCH",
      "catalog_number":"624",
      "title":"The Social Ecology of the Urban Periphery"
    },
    {
      "course_id":"013899",
      "subject":"ARCH",
      "catalog_number":"641",
      "title":"The Inner Studio"
    },
    {
      "course_id":"010636",
      "subject":"ARCH",
      "catalog_number":"642",
      "title":"Modern Architecture"
    },
    {
      "course_id":"010637",
      "subject":"ARCH",
      "catalog_number":"643",
      "title":"The Study and Design of Cultural Sites"
    },
    {
      "course_id":"010638",
      "subject":"ARCH",
      "catalog_number":"644",
      "title":"Architecture, Memory and Commemoration"
    },
    {
      "course_id":"010639",
      "subject":"ARCH",
      "catalog_number":"645",
      "title":"Architecture and the State"
    },
    {
      "course_id":"012034",
      "subject":"ARCH",
      "catalog_number":"646",
      "title":"Architecture and Film"
    },
    {
      "course_id":"010631",
      "subject":"ARCH",
      "catalog_number":"652",
      "title":"Specifications"
    },
    {
      "course_id":"010633",
      "subject":"ARCH",
      "catalog_number":"654",
      "title":"Acts and Codes"
    },
    {
      "course_id":"013117",
      "subject":"ARCH",
      "catalog_number":"655",
      "title":"Architectural Practice: Ethics, Professional Liability and Business"
    },
    {
      "course_id":"010640",
      "subject":"ARCH",
      "catalog_number":"672",
      "title":"Energy Effective Design"
    },
    {
      "course_id":"010641",
      "subject":"ARCH",
      "catalog_number":"673",
      "title":"The Science of the Building Envelope"
    },
    {
      "course_id":"010647",
      "subject":"ARCH",
      "catalog_number":"675",
      "title":"Sheltering Systems"
    },
    {
      "course_id":"010648",
      "subject":"ARCH",
      "catalog_number":"676",
      "title":"Lightweight Structures"
    },
    {
      "course_id":"011628",
      "subject":"ARCH",
      "catalog_number":"677",
      "title":"Survey of Digital Design Technologies for Architecture"
    },
    {
      "course_id":"011629",
      "subject":"ARCH",
      "catalog_number":"678",
      "title":"Digital Lighting Design for Architecture"
    },
    {
      "course_id":"010645",
      "subject":"ARCH",
      "catalog_number":"684",
      "title":"Special Topics in Architecture"
    },
    {
      "course_id":"010646",
      "subject":"ARCH",
      "catalog_number":"685",
      "title":"Readings and Seminars in Architecture"
    },
    {
      "course_id":"013900",
      "subject":"ARCH",
      "catalog_number":"686",
      "title":"Competitions in Architecture"
    },
    {
      "course_id":"010634",
      "subject":"ARCH",
      "catalog_number":"692",
      "title":"Graduate Design Studio and Seminar"
    },
    {
      "course_id":"011679",
      "subject":"ARTS",
      "catalog_number":"101",
      "title":"Foundations for Writing"
    },
    {
      "course_id":"011400",
      "subject":"ARTS",
      "catalog_number":"111",
      "title":"Career Development and Decision-Making"
    },
    {
      "course_id":"003610",
      "subject":"ARTS",
      "catalog_number":"122",
      "title":"Quest for Meaning in the Modern World"
    },
    {
      "course_id":"014276",
      "subject":"ARTS",
      "catalog_number":"125",
      "title":"Who are the Mennonites?"
    },
    {
      "course_id":"013857",
      "subject":"ARTS",
      "catalog_number":"190",
      "title":"First-Year Topics in Arts Disciplines"
    },
    {
      "course_id":"012283",
      "subject":"ARTS",
      "catalog_number":"280",
      "title":"Statistics for Arts Students"
    },
    {
      "course_id":"013858",
      "subject":"ARTS",
      "catalog_number":"290",
      "title":"Second-Year Topics in Arts Disciplines"
    },
    {
      "course_id":"003628",
      "subject":"ARTS",
      "catalog_number":"301",
      "title":"Studies in Ideas"
    },
    {
      "course_id":"010387",
      "subject":"ARTS",
      "catalog_number":"365",
      "title":"Arts Study Abroad"
    },
    {
      "course_id":"010730",
      "subject":"ARTS",
      "catalog_number":"366",
      "title":"Arts Study Abroad"
    },
    {
      "course_id":"010731",
      "subject":"ARTS",
      "catalog_number":"367",
      "title":"Arts Study Abroad"
    },
    {
      "course_id":"013856",
      "subject":"ARTS",
      "catalog_number":"390",
      "title":"Third-Year Topics in Arts Disciplines"
    },
    {
      "course_id":"013859",
      "subject":"ARTS",
      "catalog_number":"490",
      "title":"Fourth-Year Topics in Arts Disciplines"
    },
    {
      "course_id":"012851",
      "subject":"ARTS",
      "catalog_number":"600",
      "title":"Knowledge Mobilzation to Serve Society"
    },
    {
      "course_id":"012969",
      "subject":"ARTS",
      "catalog_number":"601",
      "title":"Building Community-University Research Alliances"
    },
    {
      "course_id":"013236",
      "subject":"AVIA",
      "catalog_number":"101",
      "title":"Professional Pilot Program Course I"
    },
    {
      "course_id":"013237",
      "subject":"AVIA",
      "catalog_number":"102",
      "title":"Professional Pilot Program Course II"
    },
    {
      "course_id":"013238",
      "subject":"AVIA",
      "catalog_number":"203",
      "title":"Professional Pilot Program Course III"
    },
    {
      "course_id":"013239",
      "subject":"AVIA",
      "catalog_number":"204",
      "title":"Professional Pilot Program Course IV"
    },
    {
      "course_id":"014522",
      "subject":"AVIA",
      "catalog_number":"205",
      "title":"Professional Pilot Program Course V"
    },
    {
      "course_id":"013242",
      "subject":"AVIA",
      "catalog_number":"306",
      "title":"Professional Pilot Program Course VI"
    },
    {
      "course_id":"014523",
      "subject":"AVIA",
      "catalog_number":"307",
      "title":"Professional Pilot Program Course VII"
    },
    {
      "course_id":"013302",
      "subject":"AVIA",
      "catalog_number":"310",
      "title":"Human Factors in Aviation"
    },
    {
      "course_id":"014524",
      "subject":"AVIA",
      "catalog_number":"408",
      "title":"Professional Pilot Program Course VIII"
    },
    {
      "course_id":"014107",
      "subject":"AVIA",
      "catalog_number":"474",
      "title":"Special Topics in Aviation"
    },
    {
      "course_id":"014108",
      "subject":"AVIA",
      "catalog_number":"475",
      "title":"Independent Studies of Selected Topics"
    },
    {
      "course_id":"014671",
      "subject":"BE",
      "catalog_number":"600",
      "title":"Management and Leadership"
    },
    {
      "course_id":"013227",
      "subject":"BE",
      "catalog_number":"601",
      "title":"Introduction to Financial and Managerial Accounting"
    },
    {
      "course_id":"013226",
      "subject":"BE",
      "catalog_number":"602",
      "title":"Data Analysis and Management"
    },
    {
      "course_id":"013225",
      "subject":"BE",
      "catalog_number":"603",
      "title":"Operations and Supply Chain Management"
    },
    {
      "course_id":"013224",
      "subject":"BE",
      "catalog_number":"604",
      "title":"Marketing Management"
    },
    {
      "course_id":"013223",
      "subject":"BE",
      "catalog_number":"605",
      "title":"Project Management"
    },
    {
      "course_id":"013222",
      "subject":"BE",
      "catalog_number":"606",
      "title":"Entrepreneurship and Innovation"
    },
    {
      "course_id":"014672",
      "subject":"BE",
      "catalog_number":"610",
      "title":"Special Topics in Business and Entrepreneurship"
    },
    {
      "course_id":"014055",
      "subject":"BET",
      "catalog_number":"300",
      "title":"Foundations of Venture Creation"
    },
    {
      "course_id":"014056",
      "subject":"BET",
      "catalog_number":"400",
      "title":"Growing Early-stage Ventures"
    },
    {
      "course_id":"013080",
      "subject":"BET",
      "catalog_number":"600",
      "title":"Applied Business Leadership Skills for Entrepreneurs"
    },
    {
      "course_id":"011687",
      "subject":"BET",
      "catalog_number":"601",
      "title":"Strategically Managing the Entrepreneurial Organization"
    },
    {
      "course_id":"011688",
      "subject":"BET",
      "catalog_number":"602",
      "title":"Marketing Strategies for New Technology-based Ventures"
    },
    {
      "course_id":"011689",
      "subject":"BET",
      "catalog_number":"603",
      "title":"Entrepreneurial Finance for the Technology-based Enterprise"
    },
    {
      "course_id":"011690",
      "subject":"BET",
      "catalog_number":"604",
      "title":"New Technology-based Venture Creation"
    },
    {
      "course_id":"011691",
      "subject":"BET",
      "catalog_number":"605",
      "title":"Essential Accounting for Entrepreneurs"
    },
    {
      "course_id":"011693",
      "subject":"BET",
      "catalog_number":"607",
      "title":"Managing Technological Innovation"
    },
    {
      "course_id":"011694",
      "subject":"BET",
      "catalog_number":"608",
      "title":"Entrepreneurial Application of Technology"
    },
    {
      "course_id":"013081",
      "subject":"BET",
      "catalog_number":"620",
      "title":"Social Entrepreneurship and Corporate Social Responsibility"
    },
    {
      "course_id":"013082",
      "subject":"BET",
      "catalog_number":"700",
      "title":"Topics in Business, Entrepreneurship and Technology"
    },
    {
      "course_id":"003654",
      "subject":"BIOL",
      "catalog_number":"110",
      "title":"Introductory Zoology"
    },
    {
      "course_id":"003650",
      "subject":"BIOL",
      "catalog_number":"112",
      "title":"Introductory Biology 2"
    },
    {
      "course_id":"003657",
      "subject":"BIOL",
      "catalog_number":"120",
      "title":"Introduction to Plant Structure and Function"
    },
    {
      "course_id":"011617",
      "subject":"BIOL",
      "catalog_number":"130",
      "title":"Introductory Cell Biology"
    },
    {
      "course_id":"011567",
      "subject":"BIOL",
      "catalog_number":"130L",
      "title":"Cell Biology Laboratory"
    },
    {
      "course_id":"003668",
      "subject":"BIOL",
      "catalog_number":"150",
      "title":"Organismal and Evolutionary Ecology"
    },
    {
      "course_id":"009491",
      "subject":"BIOL",
      "catalog_number":"165",
      "title":"Diversity of Life"
    },
    {
      "course_id":"003655",
      "subject":"BIOL",
      "catalog_number":"211",
      "title":"Introductory Vertebrate Zoology"
    },
    {
      "course_id":"014403",
      "subject":"BIOL",
      "catalog_number":"225",
      "title":"Plants and Civilization"
    },
    {
      "course_id":"003665",
      "subject":"BIOL",
      "catalog_number":"239",
      "title":"Genetics"
    },
    {
      "course_id":"011618",
      "subject":"BIOL",
      "catalog_number":"240",
      "title":"Fundamentals of Microbiology"
    },
    {
      "course_id":"011568",
      "subject":"BIOL",
      "catalog_number":"240L",
      "title":"Microbiology Laboratory"
    },
    {
      "course_id":"003667",
      "subject":"BIOL",
      "catalog_number":"241",
      "title":"Introduction to Applied Microbiology"
    },
    {
      "course_id":"003669",
      "subject":"BIOL",
      "catalog_number":"273",
      "title":"Principles of Human Physiology 1"
    },
    {
      "course_id":"011569",
      "subject":"BIOL",
      "catalog_number":"273L",
      "title":"Human Physiology 1 Laboratory"
    },
    {
      "course_id":"012773",
      "subject":"BIOL",
      "catalog_number":"280",
      "title":"Introduction to Biophysics"
    },
    {
      "course_id":"003651",
      "subject":"BIOL",
      "catalog_number":"301",
      "title":"Human Anatomy"
    },
    {
      "course_id":"004838",
      "subject":"BIOL",
      "catalog_number":"360",
      "title":"Evolution 2: Fossil Record"
    },
    {
      "course_id":"003673",
      "subject":"BIOL",
      "catalog_number":"302",
      "title":"Functional Histology"
    },
    {
      "course_id":"003674",
      "subject":"BIOL",
      "catalog_number":"303",
      "title":"Introductory Developmental Biology and Embryology"
    },
    {
      "course_id":"012246",
      "subject":"BIOL",
      "catalog_number":"308",
      "title":"Principles of Molecular Biology"
    },
    {
      "course_id":"012245",
      "subject":"BIOL",
      "catalog_number":"309",
      "title":"Analytical Methods in Molecular Biology"
    },
    {
      "course_id":"003675",
      "subject":"BIOL",
      "catalog_number":"310",
      "title":"Invertebrate Zoology"
    },
    {
      "course_id":"010002",
      "subject":"BIOL",
      "catalog_number":"321",
      "title":"Plant Anatomy and Morphogenesis"
    },
    {
      "course_id":"003680",
      "subject":"BIOL",
      "catalog_number":"323",
      "title":"Plant Physiology"
    },
    {
      "course_id":"010179",
      "subject":"BIOL",
      "catalog_number":"325",
      "title":"Flowering Plants"
    },
    {
      "course_id":"003685",
      "subject":"BIOL",
      "catalog_number":"331",
      "title":"Advanced Cell Biology"
    },
    {
      "course_id":"003724",
      "subject":"BIOL",
      "catalog_number":"335L",
      "title":"Molecular Biology Techniques"
    },
    {
      "course_id":"003691",
      "subject":"BIOL",
      "catalog_number":"342",
      "title":"Molecular Biotechnology 1"
    },
    {
      "course_id":"003734",
      "subject":"BIOL",
      "catalog_number":"345",
      "title":"Microorganisms in Foods"
    },
    {
      "course_id":"003735",
      "subject":"BIOL",
      "catalog_number":"346",
      "title":"Microbial Ecology and Diversity"
    },
    {
      "course_id":"011570",
      "subject":"BIOL",
      "catalog_number":"348L",
      "title":"Laboratory Methods in Microbiology"
    },
    {
      "course_id":"013110",
      "subject":"BIOL",
      "catalog_number":"349",
      "title":"Synthetic Biology Project Design"
    },
    {
      "course_id":"012918",
      "subject":"BIOL",
      "catalog_number":"350",
      "title":"Ecosystem Ecology"
    },
    {
      "course_id":"003740",
      "subject":"BIOL",
      "catalog_number":"351",
      "title":"Aquatic Ecology"
    },
    {
      "course_id":"003694",
      "subject":"BIOL",
      "catalog_number":"354",
      "title":"Environmental Toxicology 1"
    },
    {
      "course_id":"013897",
      "subject":"BIOL",
      "catalog_number":"355",
      "title":"Biology of Human Aging"
    },
    {
      "course_id":"003748",
      "subject":"BIOL",
      "catalog_number":"359",
      "title":"Evolution 1: Mechanisms"
    },
    {
      "course_id":"009500",
      "subject":"BIOL",
      "catalog_number":"361",
      "title":"Biostatistics and Experimental Design"
    },
    {
      "course_id":"013528",
      "subject":"BIOL",
      "catalog_number":"364",
      "title":"Mathematical Modelling in Biology"
    },
    {
      "course_id":"009501",
      "subject":"BIOL",
      "catalog_number":"365",
      "title":"Methods in Bioinformatics"
    },
    {
      "course_id":"011508",
      "subject":"BIOL",
      "catalog_number":"366",
      "title":"Introduction to Bioinformatics"
    },
    {
      "course_id":"003696",
      "subject":"BIOL",
      "catalog_number":"370",
      "title":"Comparative Animal Physiology 1"
    },
    {
      "course_id":"003697",
      "subject":"BIOL",
      "catalog_number":"371",
      "title":"Comparative Animal Physiology 2"
    },
    {
      "course_id":"010000",
      "subject":"BIOL",
      "catalog_number":"373",
      "title":"Principles of Human Physiology 2"
    },
    {
      "course_id":"010001",
      "subject":"BIOL",
      "catalog_number":"373L",
      "title":"Human Physiology 2 Laboratory"
    },
    {
      "course_id":"012976",
      "subject":"BIOL",
      "catalog_number":"376",
      "title":"Cellular Neurophysiology"
    },
    {
      "course_id":"013977",
      "subject":"BIOL",
      "catalog_number":"377",
      "title":"Systems Neuroscience: From Neurons to Behaviour"
    },
    {
      "course_id":"011910",
      "subject":"BIOL",
      "catalog_number":"382",
      "title":"Computational Modelling of Cellular Systems"
    },
    {
      "course_id":"012580",
      "subject":"BIOL",
      "catalog_number":"383",
      "title":"Tropical Ecosystems"
    },
    {
      "course_id":"003701",
      "subject":"BIOL",
      "catalog_number":"403",
      "title":"Advanced Topics in Developmental Biology"
    },
    {
      "course_id":"003705",
      "subject":"BIOL",
      "catalog_number":"412",
      "title":"Arthropod Zoology"
    },
    {
      "course_id":"003713",
      "subject":"BIOL",
      "catalog_number":"426",
      "title":"Phycology"
    },
    {
      "course_id":"003716",
      "subject":"BIOL",
      "catalog_number":"428",
      "title":"Plant Molecular Genetics"
    },
    {
      "course_id":"003718",
      "subject":"BIOL",
      "catalog_number":"431",
      "title":"Bacterial Molecular Genetics"
    },
    {
      "course_id":"003720",
      "subject":"BIOL",
      "catalog_number":"432",
      "title":"Molecular Biotechnology 2"
    },
    {
      "course_id":"003721",
      "subject":"BIOL",
      "catalog_number":"433",
      "title":"Plant Biotechnology"
    },
    {
      "course_id":"003722",
      "subject":"BIOL",
      "catalog_number":"434",
      "title":"Human Molecular Genetics"
    },
    {
      "course_id":"003727",
      "subject":"BIOL",
      "catalog_number":"438",
      "title":"Molecular Biology of Animal Development"
    },
    {
      "course_id":"003728",
      "subject":"BIOL",
      "catalog_number":"439",
      "title":"Environmental and Natural Products Biochemistry"
    },
    {
      "course_id":"003730",
      "subject":"BIOL",
      "catalog_number":"441",
      "title":"Advances in Immunology"
    },
    {
      "course_id":"003731",
      "subject":"BIOL",
      "catalog_number":"442",
      "title":"Virology"
    },
    {
      "course_id":"003732",
      "subject":"BIOL",
      "catalog_number":"443",
      "title":"Fermentation Biotechnology"
    },
    {
      "course_id":"003733",
      "subject":"BIOL",
      "catalog_number":"444",
      "title":"Microorganisms and Disease"
    },
    {
      "course_id":"003736",
      "subject":"BIOL",
      "catalog_number":"447",
      "title":"Environmental Microbiology"
    },
    {
      "course_id":"003737",
      "subject":"BIOL",
      "catalog_number":"448",
      "title":"Microbial Physiology and Biochemistry"
    },
    {
      "course_id":"012173",
      "subject":"BIOL",
      "catalog_number":"449",
      "title":"Public Health Microbiology"
    },
    {
      "course_id":"003739",
      "subject":"BIOL",
      "catalog_number":"450",
      "title":"Marine Biology"
    },
    {
      "course_id":"003741",
      "subject":"BIOL",
      "catalog_number":"452",
      "title":"Quantitative Fisheries Biology"
    },
    {
      "course_id":"003744",
      "subject":"BIOL",
      "catalog_number":"455",
      "title":"Ecological Risk Assessment and Management"
    },
    {
      "course_id":"003745",
      "subject":"BIOL",
      "catalog_number":"456",
      "title":"Population Biology"
    },
    {
      "course_id":"003746",
      "subject":"BIOL",
      "catalog_number":"457",
      "title":"Analysis of Communities"
    },
    {
      "course_id":"013953",
      "subject":"BIOL",
      "catalog_number":"458",
      "title":"Quantitative Ecology"
    },
    {
      "course_id":"003751",
      "subject":"BIOL",
      "catalog_number":"461",
      "title":"Advanced Biostatistics"
    },
    {
      "course_id":"012909",
      "subject":"BIOL",
      "catalog_number":"462",
      "title":"Applied Wetland Science"
    },
    {
      "course_id":"010003",
      "subject":"BIOL",
      "catalog_number":"465",
      "title":"Structural Bioinformatics"
    },
    {
      "course_id":"012916",
      "subject":"BIOL",
      "catalog_number":"466",
      "title":"Biogeochemical Microbiology"
    },
    {
      "course_id":"013532",
      "subject":"BIOL",
      "catalog_number":"467",
      "title":"Plant-Bacterial Interactions"
    },
    {
      "course_id":"003750",
      "subject":"BIOL",
      "catalog_number":"470",
      "title":"Methods of Aquatic Ecology"
    },
    {
      "course_id":"013530",
      "subject":"BIOL",
      "catalog_number":"472",
      "title":"Cell Biology of Human Disease"
    },
    {
      "course_id":"003756",
      "subject":"BIOL",
      "catalog_number":"473",
      "title":"Mammalian Reproduction"
    },
    {
      "course_id":"010354",
      "subject":"BIOL",
      "catalog_number":"474",
      "title":"Bioprocessing"
    },
    {
      "course_id":"011571",
      "subject":"BIOL",
      "catalog_number":"475",
      "title":"Current Topics in Applied Microbiology"
    },
    {
      "course_id":"012174",
      "subject":"BIOL",
      "catalog_number":"476",
      "title":"Cellular and Molecular Neuroscience"
    },
    {
      "course_id":"003698",
      "subject":"BIOL",
      "catalog_number":"477L",
      "title":"Techniques in Animal Physiology"
    },
    {
      "course_id":"012404",
      "subject":"BIOL",
      "catalog_number":"479",
      "title":"Population Genetics and Evolution"
    },
    {
      "course_id":"012427",
      "subject":"BIOL",
      "catalog_number":"480",
      "title":"Molecular Ecology"
    },
    {
      "course_id":"012166",
      "subject":"BIOL",
      "catalog_number":"483",
      "title":"Animal Cell Biotechnology"
    },
    {
      "course_id":"012330",
      "subject":"BIOL",
      "catalog_number":"484",
      "title":"Advanced Eukaryotic Genetics"
    },
    {
      "course_id":"014515",
      "subject":"BIOL",
      "catalog_number":"485",
      "title":"Conservation Biology"
    },
    {
      "course_id":"013531",
      "subject":"BIOL",
      "catalog_number":"486",
      "title":"Glycobiology"
    },
    {
      "course_id":"014290",
      "subject":"BIOL",
      "catalog_number":"487",
      "title":"Computational Neuroscience"
    },
    {
      "course_id":"012267",
      "subject":"BIOL",
      "catalog_number":"488",
      "title":"Ecotoxicology from a Watershed Perspective"
    },
    {
      "course_id":"014516",
      "subject":"BIOL",
      "catalog_number":"489",
      "title":"Arctic Ecology"
    },
    {
      "course_id":"003762",
      "subject":"BIOL",
      "catalog_number":"490A",
      "title":"Biology Field Course I"
    },
    {
      "course_id":"003763",
      "subject":"BIOL",
      "catalog_number":"490B",
      "title":"Biology Field Course II"
    },
    {
      "course_id":"003765",
      "subject":"BIOL",
      "catalog_number":"491A",
      "title":"Aquatic Field Biology"
    },
    {
      "course_id":"003765",
      "subject":"BIOL",
      "catalog_number":"490C",
      "title":"Biology Field Course III"
    },
    {
      "course_id":"003766",
      "subject":"BIOL",
      "catalog_number":"490D",
      "title":"Biology Field Course IV"
    },
    {
      "course_id":"003767",
      "subject":"BIOL",
      "catalog_number":"492",
      "title":"Marine Mammals and Seabirds"
    },
    {
      "course_id":"014281",
      "subject":"BIOL",
      "catalog_number":"496",
      "title":"Neuroscience Research Seminar"
    },
    {
      "course_id":"003770",
      "subject":"BIOL",
      "catalog_number":"498A",
      "title":"Short Biology Field Course 1"
    },
    {
      "course_id":"003779",
      "subject":"BUS",
      "catalog_number":"121W",
      "title":"Functional Areas of the Organization (WLU)"
    },
    {
      "course_id":"003771",
      "subject":"BIOL",
      "catalog_number":"498B",
      "title":"Short Biology Field Course 2"
    },
    {
      "course_id":"003776",
      "subject":"BUS",
      "catalog_number":"111W",
      "title":"Introduction to Business Organization (WLU)"
    },
    {
      "course_id":"003772",
      "subject":"BIOL",
      "catalog_number":"499A",
      "title":"Senior Honours Project"
    },
    {
      "course_id":"003773",
      "subject":"BIOL",
      "catalog_number":"499B",
      "title":"Senior Honours Project"
    },
    {
      "course_id":"000158",
      "subject":"BIOL",
      "catalog_number":"602",
      "title":"Fisheries Biology"
    },
    {
      "course_id":"000161",
      "subject":"BIOL",
      "catalog_number":"604",
      "title":"Animal Cells in Culture"
    },
    {
      "course_id":"000162",
      "subject":"BIOL",
      "catalog_number":"605",
      "title":"Environmental Animal Physiology"
    },
    {
      "course_id":"000163",
      "subject":"BIOL",
      "catalog_number":"606",
      "title":"Advanced Aquatic Ecology"
    },
    {
      "course_id":"000165",
      "subject":"BIOL",
      "catalog_number":"608",
      "title":"Advanced Molecular Genetics"
    },
    {
      "course_id":"000166",
      "subject":"BIOL",
      "catalog_number":"610",
      "title":"Biosystematics and Evolution"
    },
    {
      "course_id":"000167",
      "subject":"BIOL",
      "catalog_number":"611",
      "title":"Plant Growth Regulation I"
    },
    {
      "course_id":"000168",
      "subject":"BIOL",
      "catalog_number":"612",
      "title":"Phylogenetic Reconstruction and Analysis"
    },
    {
      "course_id":"000170",
      "subject":"BIOL",
      "catalog_number":"614",
      "title":"Bioinformatics Tools and Techniques"
    },
    {
      "course_id":"000173",
      "subject":"BIOL",
      "catalog_number":"617",
      "title":"Advanced Topics in Environmental Toxicology"
    },
    {
      "course_id":"000174",
      "subject":"BIOL",
      "catalog_number":"618",
      "title":"Advanced Microbial Physiology"
    },
    {
      "course_id":"000177",
      "subject":"BIOL",
      "catalog_number":"621",
      "title":"Transport Phenomena in Plants"
    },
    {
      "course_id":"000178",
      "subject":"BIOL",
      "catalog_number":"622",
      "title":"Selected Topics in Plant Physiology"
    },
    {
      "course_id":"000179",
      "subject":"BIOL",
      "catalog_number":"623",
      "title":"Floral Morphology and Taxonomy"
    },
    {
      "course_id":"000180",
      "subject":"BIOL",
      "catalog_number":"624",
      "title":"Environmental Biogeochemistry"
    },
    {
      "course_id":"000181",
      "subject":"BIOL",
      "catalog_number":"625",
      "title":"Applied  Limnology"
    },
    {
      "course_id":"000183",
      "subject":"BIOL",
      "catalog_number":"627",
      "title":"Topics in Applied and Industrial Microbiology"
    },
    {
      "course_id":"000184",
      "subject":"BIOL",
      "catalog_number":"628",
      "title":"Morphogenesis"
    },
    {
      "course_id":"000185",
      "subject":"BIOL",
      "catalog_number":"629",
      "title":"Cell Growth and Differentiation"
    },
    {
      "course_id":"000187",
      "subject":"BIOL",
      "catalog_number":"631",
      "title":"Multivariate Methods in Ecology"
    },
    {
      "course_id":"000192",
      "subject":"BIOL",
      "catalog_number":"636",
      "title":"Advanced Immunology"
    },
    {
      "course_id":"000197",
      "subject":"BIOL",
      "catalog_number":"642",
      "title":"Current Topics in Biotechnology"
    },
    {
      "course_id":"000198",
      "subject":"BIOL",
      "catalog_number":"645",
      "title":"Recent  Advances in Microbial Ecology"
    },
    {
      "course_id":"012794",
      "subject":"BIOL",
      "catalog_number":"646",
      "title":"Paleolimnology"
    },
    {
      "course_id":"000204",
      "subject":"BIOL",
      "catalog_number":"650",
      "title":"Bio-Molecular Tools"
    },
    {
      "course_id":"013757",
      "subject":"BIOL",
      "catalog_number":"651",
      "title":"Hydroecology for Freshwater Ecosystem Management"
    },
    {
      "course_id":"014059",
      "subject":"BIOL",
      "catalog_number":"652",
      "title":"Advanced Ecology"
    },
    {
      "course_id":"000206",
      "subject":"BIOL",
      "catalog_number":"667",
      "title":"Animal Molecular Biology"
    },
    {
      "course_id":"000207",
      "subject":"BIOL",
      "catalog_number":"669",
      "title":"Plant Molecular Biology"
    },
    {
      "course_id":"000208",
      "subject":"BIOL",
      "catalog_number":"670",
      "title":"Photobiology"
    },
    {
      "course_id":"000209",
      "subject":"BIOL",
      "catalog_number":"675",
      "title":"Advanced Topics in Animal Behaviour"
    },
    {
      "course_id":"012711",
      "subject":"BIOL",
      "catalog_number":"678",
      "title":"Current Topics in Neurophysiology"
    },
    {
      "course_id":"000210",
      "subject":"BIOL",
      "catalog_number":"680",
      "title":"Specialized Studies of Selected Research Procedures, Strategies or Topics"
    },
    {
      "course_id":"000224",
      "subject":"BIOL",
      "catalog_number":"681",
      "title":"Specialized Studies of Selected Research Procedures, Strategies or Topics"
    },
    {
      "course_id":"013049",
      "subject":"BIOL",
      "catalog_number":"690",
      "title":"Scientific Communication"
    },
    {
      "course_id":"014447",
      "subject":"BME",
      "catalog_number":"101",
      "title":"Introduction to Biomedical Engineering"
    },
    {
      "course_id":"014448",
      "subject":"BME",
      "catalog_number":"101L",
      "title":"Comupter-Aided Design"
    },
    {
      "course_id":"014449",
      "subject":"BME",
      "catalog_number":"121",
      "title":"Digital Computation"
    },
    {
      "course_id":"014452",
      "subject":"BME",
      "catalog_number":"122",
      "title":"Data Structures and Algorithms"
    },
    {
      "course_id":"014439",
      "subject":"BME",
      "catalog_number":"161",
      "title":"Introduction to Biomedical Design"
    },
    {
      "course_id":"014440",
      "subject":"BME",
      "catalog_number":"162",
      "title":"Human Factors in the Design of Biomedical and Health Systems"
    },
    {
      "course_id":"014453",
      "subject":"BME",
      "catalog_number":"181",
      "title":"Physics I - Statics"
    },
    {
      "course_id":"014458",
      "subject":"BME",
      "catalog_number":"182",
      "title":"Physics II - Dynamics"
    },
    {
      "course_id":"003971",
      "subject":"CHE",
      "catalog_number":"100",
      "title":"Chemical Engineering Concepts 1"
    },
    {
      "course_id":"003972",
      "subject":"CHE",
      "catalog_number":"101",
      "title":"Chemical Engineering Concepts 2"
    },
    {
      "course_id":"003973",
      "subject":"CHE",
      "catalog_number":"102",
      "title":"Chemistry for Engineers"
    },
    {
      "course_id":"011990",
      "subject":"CHE",
      "catalog_number":"121",
      "title":"Engineering Computation"
    },
    {
      "course_id":"011991",
      "subject":"CHE",
      "catalog_number":"161",
      "title":"Engineering Biology"
    },
    {
      "course_id":"003949",
      "subject":"CHE",
      "catalog_number":"200",
      "title":"Equilibrium Stage Operations"
    },
    {
      "course_id":"009212",
      "subject":"CHE",
      "catalog_number":"201",
      "title":"Seminar"
    },
    {
      "course_id":"009213",
      "subject":"CHE",
      "catalog_number":"202",
      "title":"Seminar"
    },
    {
      "course_id":"003952",
      "subject":"CHE",
      "catalog_number":"211",
      "title":"Fluid Mechanics"
    },
    {
      "course_id":"003950",
      "subject":"CHE",
      "catalog_number":"220",
      "title":"Process Data Analysis"
    },
    {
      "course_id":"003951",
      "subject":"CHE",
      "catalog_number":"230",
      "title":"Physical Chemistry 1"
    },
    {
      "course_id":"003953",
      "subject":"CHE",
      "catalog_number":"231",
      "title":"Physical Chemistry 2"
    },
    {
      "course_id":"012020",
      "subject":"CHE",
      "catalog_number":"241",
      "title":"Materials Science and Engineering"
    },
    {
      "course_id":"011992",
      "subject":"CHE",
      "catalog_number":"290",
      "title":"Chemical Engineering Lab 1"
    },
    {
      "course_id":"011993",
      "subject":"CHE",
      "catalog_number":"291",
      "title":"Chemical Engineering Lab 2"
    },
    {
      "course_id":"012004",
      "subject":"CHE",
      "catalog_number":"298",
      "title":"Directed Research Project"
    },
    {
      "course_id":"012005",
      "subject":"CHE",
      "catalog_number":"299",
      "title":"Directed Research Project"
    },
    {
      "course_id":"009214",
      "subject":"CHE",
      "catalog_number":"301",
      "title":"Seminar"
    },
    {
      "course_id":"009215",
      "subject":"CHE",
      "catalog_number":"302",
      "title":"Seminar"
    },
    {
      "course_id":"003960",
      "subject":"CHE",
      "catalog_number":"311",
      "title":"Chemical Reaction Engineering"
    },
    {
      "course_id":"013357",
      "subject":"CHE",
      "catalog_number":"312",
      "title":"Mathematics of Heat and Mass Transfer"
    },
    {
      "course_id":"013358",
      "subject":"CHE",
      "catalog_number":"313",
      "title":"Applications of Heat and Mass Transfer"
    },
    {
      "course_id":"011995",
      "subject":"CHE",
      "catalog_number":"322",
      "title":"Numerical Methods for Process Analysis and Design"
    },
    {
      "course_id":"012688",
      "subject":"CHEM",
      "catalog_number":"140L",
      "title":"Introductory Scientific Calculations Laboratory"
    },
    {
      "course_id":"011994",
      "subject":"CHE",
      "catalog_number":"325",
      "title":"Strategies for Process Improvement and Product Development"
    },
    {
      "course_id":"003957",
      "subject":"CHE",
      "catalog_number":"330",
      "title":"Chemical Engineering Thermodynamics"
    },
    {
      "course_id":"003962",
      "subject":"CHE",
      "catalog_number":"331",
      "title":"Electrochemical Engineering"
    },
    {
      "course_id":"003956",
      "subject":"CHE",
      "catalog_number":"360",
      "title":"Bioprocess Engineering"
    },
    {
      "course_id":"011996",
      "subject":"CHE",
      "catalog_number":"390",
      "title":"Chemical Engineering Lab 3"
    },
    {
      "course_id":"011997",
      "subject":"CHE",
      "catalog_number":"391",
      "title":"Chemical Engineering Lab 4"
    },
    {
      "course_id":"012006",
      "subject":"CHE",
      "catalog_number":"398",
      "title":"Directed Research Project"
    },
    {
      "course_id":"012007",
      "subject":"CHE",
      "catalog_number":"399",
      "title":"Directed Research Project"
    },
    {
      "course_id":"009216",
      "subject":"CHE",
      "catalog_number":"401",
      "title":"Seminar"
    },
    {
      "course_id":"009217",
      "subject":"CHE",
      "catalog_number":"402",
      "title":"Seminar"
    },
    {
      "course_id":"003964",
      "subject":"CHE",
      "catalog_number":"420",
      "title":"Introduction to Process Control"
    },
    {
      "course_id":"011999",
      "subject":"CHE",
      "catalog_number":"480",
      "title":"Process Analysis and Design"
    },
    {
      "course_id":"010016",
      "subject":"CHE",
      "catalog_number":"482",
      "title":"Chemical Engineering Design Workshop"
    },
    {
      "course_id":"003969",
      "subject":"CHE",
      "catalog_number":"483",
      "title":"Group Design Project"
    },
    {
      "course_id":"012000",
      "subject":"CHE",
      "catalog_number":"490",
      "title":"Chemical Engineering Lab 5"
    },
    {
      "course_id":"003966",
      "subject":"CHE",
      "catalog_number":"498",
      "title":"Directed Research Project"
    },
    {
      "course_id":"003970",
      "subject":"CHE",
      "catalog_number":"499",
      "title":"Elective Research Project"
    },
    {
      "course_id":"012726",
      "subject":"CHE",
      "catalog_number":"500",
      "title":"Special Topics in Chemical Engineering"
    },
    {
      "course_id":"003997",
      "subject":"CHE",
      "catalog_number":"514",
      "title":"Fundamentals of Petroleum Production"
    },
    {
      "course_id":"014525",
      "subject":"CHE",
      "catalog_number":"516",
      "title":"Energy Systems Engineering"
    },
    {
      "course_id":"004002",
      "subject":"CHE",
      "catalog_number":"522",
      "title":"Advanced Process Dynamics and Control"
    },
    {
      "course_id":"004004",
      "subject":"CHE",
      "catalog_number":"524",
      "title":"Process Control Laboratory"
    },
    {
      "course_id":"012001",
      "subject":"CHE",
      "catalog_number":"541",
      "title":"Introduction to Polymer Science and Properties"
    },
    {
      "course_id":"012002",
      "subject":"CHE",
      "catalog_number":"543",
      "title":"Polymer Production: Polymer Reaction Engineering"
    },
    {
      "course_id":"004016",
      "subject":"CHE",
      "catalog_number":"562",
      "title":"Advanced Bioprocess Engineering"
    },
    {
      "course_id":"004018",
      "subject":"CHE",
      "catalog_number":"564",
      "title":"Food Process Engineering"
    },
    {
      "course_id":"012003",
      "subject":"CHE",
      "catalog_number":"571",
      "title":"Industrial Ecology"
    },
    {
      "course_id":"004021",
      "subject":"CHE",
      "catalog_number":"572",
      "title":"Air Pollution Control"
    },
    {
      "course_id":"004023",
      "subject":"CHE",
      "catalog_number":"574",
      "title":"Industrial Wastewater Pollution Control"
    },
    {
      "course_id":"000333",
      "subject":"CHE",
      "catalog_number":"610",
      "title":"Theory and Application of Transport Phenomena"
    },
    {
      "course_id":"012789",
      "subject":"CHE",
      "catalog_number":"612",
      "title":"Interfacial Phenomena"
    },
    {
      "course_id":"010402",
      "subject":"CHE",
      "catalog_number":"614",
      "title":"Capillary and Transport Phenomena in Porous Media"
    },
    {
      "course_id":"014409",
      "subject":"CHE",
      "catalog_number":"620",
      "title":"Applied Engineering Mathematics"
    },
    {
      "course_id":"000337",
      "subject":"CHE",
      "catalog_number":"622",
      "title":"Statistics in Engineering"
    },
    {
      "course_id":"010415",
      "subject":"CHE",
      "catalog_number":"624",
      "title":"Advanced Process Dynamics and Control"
    },
    {
      "course_id":"000338",
      "subject":"CHE",
      "catalog_number":"630",
      "title":"Chemical Reactor Analysis"
    },
    {
      "course_id":"010445",
      "subject":"CHE",
      "catalog_number":"632",
      "title":"Introduction to Catalysis"
    },
    {
      "course_id":"000340",
      "subject":"CHE",
      "catalog_number":"640",
      "title":"Principles of Polymer Science"
    },
    {
      "course_id":"000341",
      "subject":"CHE",
      "catalog_number":"641",
      "title":"Physical Properties of Polymers"
    },
    {
      "course_id":"000345",
      "subject":"CHE",
      "catalog_number":"660",
      "title":"Principles of Biochemical Engineering"
    },
    {
      "course_id":"000346",
      "subject":"CHE",
      "catalog_number":"661",
      "title":"Advances in Biochemical Engineering"
    },
    {
      "course_id":"010447",
      "subject":"CHE",
      "catalog_number":"672",
      "title":"Air Pollution Control"
    },
    {
      "course_id":"010448",
      "subject":"CHE",
      "catalog_number":"674",
      "title":"Industrial Waste Treatment"
    },
    {
      "course_id":"000352",
      "subject":"CHE",
      "catalog_number":"710",
      "title":"Special Topics in Transport Phenomena"
    },
    {
      "course_id":"000355",
      "subject":"CHE",
      "catalog_number":"715",
      "title":"Research Topics in Transport Phenomena"
    },
    {
      "course_id":"000360",
      "subject":"CHE",
      "catalog_number":"720",
      "title":"Special Topics in Analysis of Chemical Processes"
    },
    {
      "course_id":"000366",
      "subject":"CHE",
      "catalog_number":"725",
      "title":"Research Topics in Analysis of Chemical Processes"
    },
    {
      "course_id":"000371",
      "subject":"CHE",
      "catalog_number":"730",
      "title":"Special Topics in Chemical Kinetics,Catalysis and Advanced Reactor Engineering"
    },
    {
      "course_id":"000376",
      "subject":"CHE",
      "catalog_number":"735",
      "title":"Research Topics in Chemical Kinetics, Catalysis and Advanced Reactor Engineering"
    },
    {
      "course_id":"000381",
      "subject":"CHE",
      "catalog_number":"740",
      "title":"Special Topics in Polymer Science and Engineering"
    },
    {
      "course_id":"000384",
      "subject":"CHE",
      "catalog_number":"745",
      "title":"Research Topics in Polymer Science and Engineering"
    },
    {
      "course_id":"000498",
      "subject":"CIVE",
      "catalog_number":"620",
      "title":"Advanced Construction Engineering and Project Management"
    },
    {
      "course_id":"000389",
      "subject":"CHE",
      "catalog_number":"750",
      "title":"Special Topics in Electrochemical Engineering, Interfacial Engineering & Materials Science"
    },
    {
      "course_id":"000392",
      "subject":"CHE",
      "catalog_number":"755",
      "title":"Res Topics in Electrochemical Engineering, Interfacial Eng &  Material Science"
    },
    {
      "course_id":"000393",
      "subject":"CHE",
      "catalog_number":"760",
      "title":"Special Topics in Biochemical Engineering"
    },
    {
      "course_id":"012159",
      "subject":"CHE",
      "catalog_number":"765",
      "title":"Research Topics in Biochemical Engineering"
    },
    {
      "course_id":"009372",
      "subject":"CHE",
      "catalog_number":"770",
      "title":"Special Topics in Environmental Engineering and Pollution Control"
    },
    {
      "course_id":"000404",
      "subject":"CHE",
      "catalog_number":"775",
      "title":"Research Topics in Environmental Engineering and Pollution Control"
    },
    {
      "course_id":"010181",
      "subject":"CHEM",
      "catalog_number":"1",
      "title":"Pre-University Chemistry"
    },
    {
      "course_id":"014633",
      "subject":"CHEM",
      "catalog_number":"100",
      "title":"Introduction to Chemical Sciences"
    },
    {
      "course_id":"004036",
      "subject":"CHEM",
      "catalog_number":"120",
      "title":"Physical and Chemical Properties of Matter"
    },
    {
      "course_id":"004037",
      "subject":"CHEM",
      "catalog_number":"120L",
      "title":"Chemical Reaction Laboratory 1"
    },
    {
      "course_id":"004040",
      "subject":"CHEM",
      "catalog_number":"123",
      "title":"Chemical Reactions, Equilibria and Kinetics"
    },
    {
      "course_id":"004041",
      "subject":"CHEM",
      "catalog_number":"123L",
      "title":"Chemical Reaction Laboratory 2"
    },
    {
      "course_id":"012688",
      "subject":"CHEM",
      "catalog_number":"140",
      "title":"Introduction to Scientific Calculations"
    },
    {
      "course_id":"012080",
      "subject":"CHEM",
      "catalog_number":"209",
      "title":"Introductory Spectroscopy and Structure"
    },
    {
      "course_id":"004048",
      "subject":"CHEM",
      "catalog_number":"212",
      "title":"Structure and Bonding"
    },
    {
      "course_id":"013241",
      "subject":"CHEM",
      "catalog_number":"217",
      "title":"Chemical Bonding"
    },
    {
      "course_id":"004052",
      "subject":"CHEM",
      "catalog_number":"220",
      "title":"Intro Analytical Chemistry"
    },
    {
      "course_id":"004053",
      "subject":"CHEM",
      "catalog_number":"220L",
      "title":"Analytical Chemistry Lab 1"
    },
    {
      "course_id":"004054",
      "subject":"CHEM",
      "catalog_number":"221",
      "title":"Multi-Component Analysis"
    },
    {
      "course_id":"004058",
      "subject":"CHEM",
      "catalog_number":"224L",
      "title":"Analytical Chemistry Laboratory 2"
    },
    {
      "course_id":"004059",
      "subject":"CHEM",
      "catalog_number":"228",
      "title":"Chemical Analysis"
    },
    {
      "course_id":"011729",
      "subject":"CHEM",
      "catalog_number":"228L",
      "title":"Analytical Chemistry Laboratory for Life Sciences"
    },
    {
      "course_id":"004060",
      "subject":"CHEM",
      "catalog_number":"233",
      "title":"Fundamentals of Biochemistry"
    },
    {
      "course_id":"004061",
      "subject":"CHEM",
      "catalog_number":"237",
      "title":"Introductory Biochemistry"
    },
    {
      "course_id":"004062",
      "subject":"CHEM",
      "catalog_number":"237L",
      "title":"Introductory Biochemistry Laboratory"
    },
    {
      "course_id":"012081",
      "subject":"CHEM",
      "catalog_number":"240",
      "title":"Mathematical Methods for Chemistry"
    },
    {
      "course_id":"004063",
      "subject":"CHEM",
      "catalog_number":"250L",
      "title":"Physical Chemistry Laboratory 1"
    },
    {
      "course_id":"004064",
      "subject":"CHEM",
      "catalog_number":"254",
      "title":"Introductory Chemical Thermodynamics"
    },
    {
      "course_id":"004029",
      "subject":"CHEM",
      "catalog_number":"262",
      "title":"Organic Chemistry for Engineering"
    },
    {
      "course_id":"004030",
      "subject":"CHEM",
      "catalog_number":"262L",
      "title":"Organic Chemistry Laboratory for Engineering Students"
    },
    {
      "course_id":"004068",
      "subject":"CHEM",
      "catalog_number":"264",
      "title":"Organic Chemistry 1"
    },
    {
      "course_id":"004069",
      "subject":"CHEM",
      "catalog_number":"265",
      "title":"Organic Chemistry 2"
    },
    {
      "course_id":"004070",
      "subject":"CHEM",
      "catalog_number":"265L",
      "title":"Organic Chemistry Laboratory 1"
    },
    {
      "course_id":"004071",
      "subject":"CHEM",
      "catalog_number":"266",
      "title":"Basic Organic Chemistry 1"
    },
    {
      "course_id":"004072",
      "subject":"CHEM",
      "catalog_number":"266L",
      "title":"Organic Chemistry Laboratory"
    },
    {
      "course_id":"004073",
      "subject":"CHEM",
      "catalog_number":"267",
      "title":"Basic Organic Chemistry 2"
    },
    {
      "course_id":"004074",
      "subject":"CHEM",
      "catalog_number":"267L",
      "title":"Organic Chemistry Laboratory"
    },
    {
      "course_id":"004078",
      "subject":"CHEM",
      "catalog_number":"310",
      "title":"Transition Element Compounds and Inorganic Materials"
    },
    {
      "course_id":"004079",
      "subject":"CHEM",
      "catalog_number":"310L",
      "title":"Inorganic Chemistry Laboratory 2"
    },
    {
      "course_id":"004083",
      "subject":"CHEM",
      "catalog_number":"313",
      "title":"Main Group and Solid State Chemistry"
    },
    {
      "course_id":"011572",
      "subject":"CHEM",
      "catalog_number":"313L",
      "title":"Inorganic Chemistry Laboratory 1"
    },
    {
      "course_id":"004089",
      "subject":"CHEM",
      "catalog_number":"323",
      "title":"Analytical Instrumentation"
    },
    {
      "course_id":"012194",
      "subject":"CHEM",
      "catalog_number":"331",
      "title":"Fundamentals of Metabolism 1"
    },
    {
      "course_id":"004091",
      "subject":"CHEM",
      "catalog_number":"333",
      "title":"Metabolism 1"
    },
    {
      "course_id":"004092",
      "subject":"CHEM",
      "catalog_number":"335L",
      "title":"Advanced Biochemistry Laboratory"
    },
    {
      "course_id":"012563",
      "subject":"CHEM",
      "catalog_number":"340",
      "title":"Introductory Computational Chemistry"
    },
    {
      "course_id":"004093",
      "subject":"CHEM",
      "catalog_number":"350",
      "title":"Chemical Kinetics"
    },
    {
      "course_id":"004094",
      "subject":"CHEM",
      "catalog_number":"350L",
      "title":"Physical Chemistry Laboratory 2"
    },
    {
      "course_id":"004067",
      "subject":"CHEM",
      "catalog_number":"356",
      "title":"Introductory Quantum Mechanics"
    },
    {
      "course_id":"004101",
      "subject":"CHEM",
      "catalog_number":"357",
      "title":"Physical Biochemistry"
    },
    {
      "course_id":"004107",
      "subject":"CHEM",
      "catalog_number":"360",
      "title":"Organic Chemistry 3"
    },
    {
      "course_id":"004108",
      "subject":"CHEM",
      "catalog_number":"360L",
      "title":"Senior Organic Chemistry Laboratory"
    },
    {
      "course_id":"004190",
      "subject":"CHEM",
      "catalog_number":"370",
      "title":"Introduction to Polymer Science"
    },
    {
      "course_id":"012199",
      "subject":"CHEM",
      "catalog_number":"381",
      "title":"Medicinal and Bioorganic Chemistry"
    },
    {
      "course_id":"012200",
      "subject":"CHEM",
      "catalog_number":"382L",
      "title":"Advanced Organic Synthesis Laboratory"
    },
    {
      "course_id":"004116",
      "subject":"CHEM",
      "catalog_number":"392A",
      "title":"Research Project 1"
    },
    {
      "course_id":"004117",
      "subject":"CHEM",
      "catalog_number":"392B",
      "title":"Research Project 2"
    },
    {
      "course_id":"004119",
      "subject":"CHEM",
      "catalog_number":"404",
      "title":"Physicochemical Aspects of Natural Waters"
    },
    {
      "course_id":"004126",
      "subject":"CHEM",
      "catalog_number":"410",
      "title":"Special Topics in Inorganic Chemistry"
    },
    {
      "course_id":"004139",
      "subject":"CHEM",
      "catalog_number":"420",
      "title":"Special Topics in Analytical Chem"
    },
    {
      "course_id":"004152",
      "subject":"CHEM",
      "catalog_number":"430",
      "title":"Special Topics in Biochemistry"
    },
    {
      "course_id":"004150",
      "subject":"CHEM",
      "catalog_number":"432",
      "title":"Metabolism 2"
    },
    {
      "course_id":"004151",
      "subject":"CHEM",
      "catalog_number":"433",
      "title":"Advanced Biochemistry"
    },
    {
      "course_id":"013002",
      "subject":"CHEM",
      "catalog_number":"440",
      "title":"Special Topics in Computational\/Theoretical Chemistry"
    },
    {
      "course_id":"004164",
      "subject":"CHEM",
      "catalog_number":"450",
      "title":"Special Topics in Physical Chemistry"
    },
    {
      "course_id":"004183",
      "subject":"CHEM",
      "catalog_number":"460",
      "title":"Special Topics in Organic Chemistry"
    },
    {
      "course_id":"004182",
      "subject":"CHEM",
      "catalog_number":"464",
      "title":"Spectroscopy in Organic Chemistry"
    },
    {
      "course_id":"013003",
      "subject":"CHEM",
      "catalog_number":"470",
      "title":"Special Topics in Polymer Chemistry"
    },
    {
      "course_id":"013360",
      "subject":"CHEM",
      "catalog_number":"481",
      "title":"Rational Design of Potential Drug Candidates"
    },
    {
      "course_id":"013361",
      "subject":"CHEM",
      "catalog_number":"482",
      "title":"Advanced Topics in Medicinal Chemistry"
    },
    {
      "course_id":"014757",
      "subject":"CHEM",
      "catalog_number":"491A",
      "title":"Biobased Chemistry Research Project 1"
    },
    {
      "course_id":"004194",
      "subject":"CHEM",
      "catalog_number":"494A",
      "title":"Research Project"
    },
    {
      "course_id":"009910",
      "subject":"CHEM",
      "catalog_number":"494B",
      "title":"Research Project"
    },
    {
      "course_id":"010356",
      "subject":"CHEM",
      "catalog_number":"495",
      "title":"Advanced Research Project"
    },
    {
      "course_id":"010357",
      "subject":"CHEM",
      "catalog_number":"496",
      "title":"Advanced Research Project"
    },
    {
      "course_id":"010358",
      "subject":"CHEM",
      "catalog_number":"497",
      "title":"Advanced Research Project"
    },
    {
      "course_id":"000423",
      "subject":"CHEM",
      "catalog_number":"710",
      "title":"Selected Topics in Inorganic Chemistry"
    },
    {
      "course_id":"000425",
      "subject":"CHEM",
      "catalog_number":"712",
      "title":"X-Ray Crystallography"
    },
    {
      "course_id":"000426",
      "subject":"CHEM",
      "catalog_number":"713",
      "title":"Chemistry of Inorganic Solid State Materials"
    },
    {
      "course_id":"000427",
      "subject":"CHEM",
      "catalog_number":"715",
      "title":"Structure & Bonding in Inorganic Chemistry"
    },
    {
      "course_id":"000429",
      "subject":"CHEM",
      "catalog_number":"717",
      "title":"Advanced Transition Metal Chemistry"
    },
    {
      "course_id":"000430",
      "subject":"CHEM",
      "catalog_number":"718",
      "title":"Advanced Organometallic Chemistry"
    },
    {
      "course_id":"000431",
      "subject":"CHEM",
      "catalog_number":"720",
      "title":"Selected Topics in Analytical Chemistry"
    },
    {
      "course_id":"000435",
      "subject":"CHEM",
      "catalog_number":"724",
      "title":"Chemical Instrumentation"
    },
    {
      "course_id":"000436",
      "subject":"CHEM",
      "catalog_number":"726",
      "title":"Topics in Analytical Spectroscopy"
    },
    {
      "course_id":"000437",
      "subject":"CHEM",
      "catalog_number":"727",
      "title":"Separations"
    },
    {
      "course_id":"000438",
      "subject":"CHEM",
      "catalog_number":"728",
      "title":"Electroanalytical Chemistry"
    },
    {
      "course_id":"000439",
      "subject":"CHEM",
      "catalog_number":"729",
      "title":"Surface Analysis"
    },
    {
      "course_id":"000440",
      "subject":"CHEM",
      "catalog_number":"730",
      "title":"Proteins and Nucleic Acids"
    },
    {
      "course_id":"000441",
      "subject":"CHEM",
      "catalog_number":"731",
      "title":"Selected Topics in Biochemistry"
    },
    {
      "course_id":"000497",
      "subject":"CIVE",
      "catalog_number":"615",
      "title":"Theories of Plates and Shells"
    },
    {
      "course_id":"000445",
      "subject":"CHEM",
      "catalog_number":"736",
      "title":"Regulations in Biological Systems"
    },
    {
      "course_id":"000446",
      "subject":"CHEM",
      "catalog_number":"737",
      "title":"Enzymes"
    },
    {
      "course_id":"000447",
      "subject":"CHEM",
      "catalog_number":"738",
      "title":"Cell Membranes and Cell Surfaces"
    },
    {
      "course_id":"000449",
      "subject":"CHEM",
      "catalog_number":"740",
      "title":"Selected Topics in Theoretical Chemistry"
    },
    {
      "course_id":"000453",
      "subject":"CHEM",
      "catalog_number":"745",
      "title":"Statistical Mechanics"
    },
    {
      "course_id":"000454",
      "subject":"CHEM",
      "catalog_number":"746",
      "title":"Quantum Chemistry"
    },
    {
      "course_id":"000455",
      "subject":"CHEM",
      "catalog_number":"750",
      "title":"Selected Topics in Physical Chemistry"
    },
    {
      "course_id":"000459",
      "subject":"CHEM",
      "catalog_number":"755",
      "title":"Kinetics - Dynamics"
    },
    {
      "course_id":"000460",
      "subject":"CHEM",
      "catalog_number":"756",
      "title":"Spectroscopy"
    },
    {
      "course_id":"000461",
      "subject":"CHEM",
      "catalog_number":"760",
      "title":"Selected Topics in Organic Chemistry"
    },
    {
      "course_id":"000465",
      "subject":"CHEM",
      "catalog_number":"764",
      "title":"Synthetic Organic Reactions"
    },
    {
      "course_id":"000466",
      "subject":"CHEM",
      "catalog_number":"765",
      "title":"Strategies in Organic Synthesis"
    },
    {
      "course_id":"000467",
      "subject":"CHEM",
      "catalog_number":"766",
      "title":"Organic Spectroscopy"
    },
    {
      "course_id":"000468",
      "subject":"CHEM",
      "catalog_number":"769",
      "title":"Physical Organic Chemistry"
    },
    {
      "course_id":"000469",
      "subject":"CHEM",
      "catalog_number":"770",
      "title":"Principles of Polymer Science"
    },
    {
      "course_id":"000341",
      "subject":"CHEM",
      "catalog_number":"771",
      "title":"Physical Properties of Polymers"
    },
    {
      "course_id":"000471",
      "subject":"CHEM",
      "catalog_number":"772",
      "title":"Polymerization and Polymer Reactions"
    },
    {
      "course_id":"000472",
      "subject":"CHEM",
      "catalog_number":"773",
      "title":"Selected Topics in Polymer Chemistry"
    },
    {
      "course_id":"000495",
      "subject":"CIVE",
      "catalog_number":"613",
      "title":"Structural Stability"
    },
    {
      "course_id":"000481",
      "subject":"CHEM",
      "catalog_number":"794",
      "title":"Master's Seminar"
    },
    {
      "course_id":"004201",
      "subject":"CHINA",
      "catalog_number":"101R",
      "title":"First-Year Chinese 1"
    },
    {
      "course_id":"004202",
      "subject":"CHINA",
      "catalog_number":"102R",
      "title":"First-Year Chinese 2"
    },
    {
      "course_id":"010373",
      "subject":"CHINA",
      "catalog_number":"120R",
      "title":"Advanced First-Year Chinese"
    },
    {
      "course_id":"013652",
      "subject":"CHINA",
      "catalog_number":"200R",
      "title":"Preliminary Second-Year Chinese"
    },
    {
      "course_id":"004203",
      "subject":"CHINA",
      "catalog_number":"201R",
      "title":"Second-Year Chinese 1"
    },
    {
      "course_id":"004204",
      "subject":"CHINA",
      "catalog_number":"202R",
      "title":"Second-Year Chinese 2"
    },
    {
      "course_id":"013999",
      "subject":"CHINA",
      "catalog_number":"272R",
      "title":"Chinese Culture and Society"
    },
    {
      "course_id":"012321",
      "subject":"CHINA",
      "catalog_number":"301R",
      "title":"Third-Year Chinese 1"
    },
    {
      "course_id":"012322",
      "subject":"CHINA",
      "catalog_number":"302R",
      "title":"Third-Year Chinese 2"
    },
    {
      "course_id":"012323",
      "subject":"CHINA",
      "catalog_number":"310R",
      "title":"Chinese for Business Settings"
    },
    {
      "course_id":"012324",
      "subject":"CHINA",
      "catalog_number":"320R",
      "title":"Chinese in Mass Media"
    },
    {
      "course_id":"014243",
      "subject":"CHINA",
      "catalog_number":"390R",
      "title":"Introduction to Professional Translation (Chinese to English)"
    },
    {
      "course_id":"010660",
      "subject":"CIVE",
      "catalog_number":"121",
      "title":"Computational Methods"
    },
    {
      "course_id":"004207",
      "subject":"CIVE",
      "catalog_number":"125",
      "title":"Civil Engineering Concepts 1"
    },
    {
      "course_id":"004209",
      "subject":"CIVE",
      "catalog_number":"127",
      "title":"Statics & Solid Mechanics 1"
    },
    {
      "course_id":"011496",
      "subject":"CIVE",
      "catalog_number":"153",
      "title":"Earth Engineering"
    },
    {
      "course_id":"013155",
      "subject":"CIVE",
      "catalog_number":"199",
      "title":"Seminar"
    },
    {
      "course_id":"004211",
      "subject":"CIVE",
      "catalog_number":"204",
      "title":"Statics and Solid Mechanics 2"
    },
    {
      "course_id":"004212",
      "subject":"CIVE",
      "catalog_number":"205",
      "title":"Mechanics of Solids 2"
    },
    {
      "course_id":"004214",
      "subject":"CIVE",
      "catalog_number":"221",
      "title":"Advanced Calculus"
    },
    {
      "course_id":"004215",
      "subject":"CIVE",
      "catalog_number":"222",
      "title":"Differential Equations"
    },
    {
      "course_id":"004219",
      "subject":"CIVE",
      "catalog_number":"224",
      "title":"Probability and Statistics"
    },
    {
      "course_id":"011493",
      "subject":"CIVE",
      "catalog_number":"240",
      "title":"Engineering and Sustainable Development"
    },
    {
      "course_id":"004221",
      "subject":"CIVE",
      "catalog_number":"265",
      "title":"Structure and Properties of Materials"
    },
    {
      "course_id":"004222",
      "subject":"CIVE",
      "catalog_number":"280",
      "title":"Fluid Mechanics and Thermal Sciences"
    },
    {
      "course_id":"004223",
      "subject":"CIVE",
      "catalog_number":"291",
      "title":"Survey Camp"
    },
    {
      "course_id":"004237",
      "subject":"CIVE",
      "catalog_number":"292",
      "title":"Engineering Economics"
    },
    {
      "course_id":"009219",
      "subject":"CIVE",
      "catalog_number":"298",
      "title":"Seminar"
    },
    {
      "course_id":"009220",
      "subject":"CIVE",
      "catalog_number":"299",
      "title":"Seminar"
    },
    {
      "course_id":"004227",
      "subject":"CIVE",
      "catalog_number":"303",
      "title":"Structural Analysis 1"
    },
    {
      "course_id":"004228",
      "subject":"CIVE",
      "catalog_number":"306",
      "title":"Mechanics of Solids 3"
    },
    {
      "course_id":"004229",
      "subject":"CIVE",
      "catalog_number":"313",
      "title":"Structural Concrete Design 1"
    },
    {
      "course_id":"011494",
      "subject":"CIVE",
      "catalog_number":"331",
      "title":"Advanced Mathematics for Civil Engineers"
    },
    {
      "course_id":"011495",
      "subject":"CIVE",
      "catalog_number":"332",
      "title":"Civil Engineering Systems"
    },
    {
      "course_id":"004230",
      "subject":"CIVE",
      "catalog_number":"342",
      "title":"Transport Principles and Applications"
    },
    {
      "course_id":"004251",
      "subject":"CIVE",
      "catalog_number":"343",
      "title":"Traffic Engineering"
    },
    {
      "course_id":"004233",
      "subject":"CIVE",
      "catalog_number":"353",
      "title":"Geotechnical Engineering 1"
    },
    {
      "course_id":"004234",
      "subject":"CIVE",
      "catalog_number":"354",
      "title":"Geotechnical Engineering 2"
    },
    {
      "course_id":"004235",
      "subject":"CIVE",
      "catalog_number":"375",
      "title":"Water Quality Engineering"
    },
    {
      "course_id":"004236",
      "subject":"CIVE",
      "catalog_number":"381",
      "title":"Hydraulics"
    },
    {
      "course_id":"009221",
      "subject":"CIVE",
      "catalog_number":"398",
      "title":"Seminar"
    },
    {
      "course_id":"009222",
      "subject":"CIVE",
      "catalog_number":"399",
      "title":"Seminar"
    },
    {
      "course_id":"004238",
      "subject":"CIVE",
      "catalog_number":"400",
      "title":"Civil Engineering Project 1"
    },
    {
      "course_id":"004239",
      "subject":"CIVE",
      "catalog_number":"401",
      "title":"Civil Engineering Project 2"
    },
    {
      "course_id":"004240",
      "subject":"CIVE",
      "catalog_number":"403",
      "title":"Structural Analysis 2"
    },
    {
      "course_id":"004242",
      "subject":"CIVE",
      "catalog_number":"405",
      "title":"Structural Dynamics"
    },
    {
      "course_id":"004244",
      "subject":"CIVE",
      "catalog_number":"413",
      "title":"Structural Steel Design"
    },
    {
      "course_id":"004245",
      "subject":"CIVE",
      "catalog_number":"414",
      "title":"Structural Concrete Design 2"
    },
    {
      "course_id":"004246",
      "subject":"CIVE",
      "catalog_number":"415",
      "title":"Structural Systems"
    },
    {
      "course_id":"004247",
      "subject":"CIVE",
      "catalog_number":"422",
      "title":"Finite Element Analysis"
    },
    {
      "course_id":"004249",
      "subject":"CIVE",
      "catalog_number":"440",
      "title":"Transit Planning and Operations"
    },
    {
      "course_id":"004232",
      "subject":"CIVE",
      "catalog_number":"444",
      "title":"Urban Transport Planning"
    },
    {
      "course_id":"004253",
      "subject":"CIVE",
      "catalog_number":"460",
      "title":"Engineering Biomechanics"
    },
    {
      "course_id":"004258",
      "subject":"CIVE",
      "catalog_number":"486",
      "title":"Hydrology"
    },
    {
      "course_id":"004259",
      "subject":"CIVE",
      "catalog_number":"491",
      "title":"Engineering Law and Ethics"
    },
    {
      "course_id":"010164",
      "subject":"CIVE",
      "catalog_number":"497",
      "title":"Special Topics in Civil Engineering"
    },
    {
      "course_id":"009223",
      "subject":"CIVE",
      "catalog_number":"498",
      "title":"Seminar"
    },
    {
      "course_id":"009224",
      "subject":"CIVE",
      "catalog_number":"499",
      "title":"Seminar"
    },
    {
      "course_id":"004243",
      "subject":"CIVE",
      "catalog_number":"507",
      "title":"Building Science and Technology"
    },
    {
      "course_id":"010038",
      "subject":"CIVE",
      "catalog_number":"512",
      "title":"Rehabilitation of Structures"
    },
    {
      "course_id":"004250",
      "subject":"CIVE",
      "catalog_number":"542",
      "title":"Pavement Structural Design"
    },
    {
      "course_id":"004252",
      "subject":"CIVE",
      "catalog_number":"554",
      "title":"Geotechnical Engineering 3"
    },
    {
      "course_id":"004254",
      "subject":"CIVE",
      "catalog_number":"572",
      "title":"Wastewater Treatment"
    },
    {
      "course_id":"004257",
      "subject":"CIVE",
      "catalog_number":"583",
      "title":"Design of Urban Water Systems"
    },
    {
      "course_id":"004261",
      "subject":"CIVE",
      "catalog_number":"596",
      "title":"Construction Engineering"
    },
    {
      "course_id":"000487",
      "subject":"CIVE",
      "catalog_number":"601",
      "title":"Engineering Risk and Reliability"
    },
    {
      "course_id":"000488",
      "subject":"CIVE",
      "catalog_number":"602",
      "title":"Prestressed Concrete"
    },
    {
      "course_id":"000489",
      "subject":"CIVE",
      "catalog_number":"603",
      "title":"Mechanics of Reinforced Concrete"
    },
    {
      "course_id":"000490",
      "subject":"CIVE",
      "catalog_number":"604",
      "title":"Advanced Structural Steel Design"
    },
    {
      "course_id":"000491",
      "subject":"CIVE",
      "catalog_number":"605",
      "title":"Computer-Aided Structural Design"
    },
    {
      "course_id":"000492",
      "subject":"CIVE",
      "catalog_number":"610",
      "title":"Elasticity"
    },
    {
      "course_id":"000493",
      "subject":"CIVE",
      "catalog_number":"611",
      "title":"Finite Element Analysis"
    },
    {
      "course_id":"000496",
      "subject":"CIVE",
      "catalog_number":"614",
      "title":"Structural Dynamics"
    },
    {
      "course_id":"000501",
      "subject":"CIVE",
      "catalog_number":"640",
      "title":"Urban Transportation Planning Models: Principles & Applications"
    },
    {
      "course_id":"000502",
      "subject":"CIVE",
      "catalog_number":"641",
      "title":"Advances in Public Transportation Planning, Operations & Control"
    },
    {
      "course_id":"000503",
      "subject":"CIVE",
      "catalog_number":"642",
      "title":"Pavement Design and Management I"
    },
    {
      "course_id":"000504",
      "subject":"CIVE",
      "catalog_number":"643",
      "title":"Fundamentals of Traffic Flow Theory"
    },
    {
      "course_id":"000506",
      "subject":"CIVE",
      "catalog_number":"650",
      "title":"Earth Structures Case Histories"
    },
    {
      "course_id":"000509",
      "subject":"CIVE",
      "catalog_number":"653",
      "title":"Numerical Methods in Geomechanics"
    },
    {
      "course_id":"000512",
      "subject":"CIVE",
      "catalog_number":"670",
      "title":"Physico-Chemical Processes of Water and Wastewater Treatment"
    },
    {
      "course_id":"000513",
      "subject":"CIVE",
      "catalog_number":"671",
      "title":"Aquatic Chemistry"
    },
    {
      "course_id":"000515",
      "subject":"CIVE",
      "catalog_number":"673",
      "title":"Mathematical Methods in Environmental Engineering"
    },
    {
      "course_id":"000517",
      "subject":"CIVE",
      "catalog_number":"676",
      "title":"Case Studies in Groundwater Management"
    },
    {
      "course_id":"000518",
      "subject":"CIVE",
      "catalog_number":"680",
      "title":"Water Management"
    },
    {
      "course_id":"000519",
      "subject":"CIVE",
      "catalog_number":"681",
      "title":"Surface Water: Theory and Modelling"
    },
    {
      "course_id":"000520",
      "subject":"CIVE",
      "catalog_number":"682",
      "title":"Free Surface Hydraulics"
    },
    {
      "course_id":"000527",
      "subject":"CIVE",
      "catalog_number":"700",
      "title":"Topics in Structural Engineering"
    },
    {
      "course_id":"000528",
      "subject":"CIVE",
      "catalog_number":"701",
      "title":"Topics in Mechanics"
    },
    {
      "course_id":"000532",
      "subject":"CIVE",
      "catalog_number":"705",
      "title":"Theories of Inelastic Structures"
    },
    {
      "course_id":"000529",
      "subject":"CIVE",
      "catalog_number":"702",
      "title":"Topics in Construction Engineering"
    },
    {
      "course_id":"000530",
      "subject":"CIVE",
      "catalog_number":"703",
      "title":"Cold Formed Steel Design"
    },
    {
      "course_id":"000531",
      "subject":"CIVE",
      "catalog_number":"704",
      "title":"Bridge Design"
    },
    {
      "course_id":"000534",
      "subject":"CIVE",
      "catalog_number":"707",
      "title":"Advanced Building Science"
    },
    {
      "course_id":"000535",
      "subject":"CIVE",
      "catalog_number":"708",
      "title":"Building Physics and Modelling"
    },
    {
      "course_id":"000536",
      "subject":"CIVE",
      "catalog_number":"709",
      "title":"Durability Design of New Concrete Infrastructure"
    },
    {
      "course_id":"000537",
      "subject":"CIVE",
      "catalog_number":"710",
      "title":"Advanced Project Management"
    },
    {
      "course_id":"000538",
      "subject":"CIVE",
      "catalog_number":"711",
      "title":"Computer-Aided Project Organization and Management"
    },
    {
      "course_id":"011047",
      "subject":"CIVE",
      "catalog_number":"712",
      "title":"Aspects of Structural Design"
    },
    {
      "course_id":"000544",
      "subject":"CIVE",
      "catalog_number":"720",
      "title":"Infrastructure Management"
    },
    {
      "course_id":"000549",
      "subject":"CIVE",
      "catalog_number":"740",
      "title":"Topics in Transportation Engineering"
    },
    {
      "course_id":"000552",
      "subject":"CIVE",
      "catalog_number":"743",
      "title":"Transport Risk Analysis"
    },
    {
      "course_id":"000550",
      "subject":"CIVE",
      "catalog_number":"741",
      "title":"Public Sector Economics and Finance"
    },
    {
      "course_id":"000551",
      "subject":"CIVE",
      "catalog_number":"742",
      "title":"Pavement Design and Management II"
    },
    {
      "course_id":"000553",
      "subject":"CIVE",
      "catalog_number":"744",
      "title":"Transportation Networks: Models, Algorithms and Computer Applications"
    },
    {
      "course_id":"000554",
      "subject":"CIVE",
      "catalog_number":"745",
      "title":"Intelligent Transportation Systems"
    },
    {
      "course_id":"000555",
      "subject":"CIVE",
      "catalog_number":"746",
      "title":"Contemporary Urban Travel Forecasting Methods"
    },
    {
      "course_id":"000558",
      "subject":"CIVE",
      "catalog_number":"750",
      "title":"Topics in Geotechnical Engineering"
    },
    {
      "course_id":"000559",
      "subject":"CIVE",
      "catalog_number":"751",
      "title":"Advanced Geotechnical Testing"
    },
    {
      "course_id":"000560",
      "subject":"CIVE",
      "catalog_number":"752",
      "title":"Trenchless Technologies"
    },
    {
      "course_id":"000561",
      "subject":"CIVE",
      "catalog_number":"753",
      "title":"Geotechnical Earthquake Engineering"
    },
    {
      "course_id":"000568",
      "subject":"CIVE",
      "catalog_number":"770",
      "title":"Topics in Environmental Engineering"
    },
    {
      "course_id":"000570",
      "subject":"CIVE",
      "catalog_number":"772",
      "title":"Environmental Health and Fate Engineering"
    },
    {
      "course_id":"000569",
      "subject":"CIVE",
      "catalog_number":"771",
      "title":"Biological Wastewater Treatment: Theory and Practice"
    },
    {
      "course_id":"000572",
      "subject":"CIVE",
      "catalog_number":"774",
      "title":"Advanced Numerical Methods for Environmental Applications"
    },
    {
      "course_id":"000574",
      "subject":"CIVE",
      "catalog_number":"776",
      "title":"Soil & Groundwater Remediation"
    },
    {
      "course_id":"000575",
      "subject":"CIVE",
      "catalog_number":"777",
      "title":"Biofilms in Engineered and Natural Systems"
    },
    {
      "course_id":"000577",
      "subject":"CIVE",
      "catalog_number":"779",
      "title":"Advanced Topics in Drinking Water Treatment"
    },
    {
      "course_id":"000578",
      "subject":"CIVE",
      "catalog_number":"780",
      "title":"Urban Water Systems"
    },
    {
      "course_id":"004262",
      "subject":"CLAS",
      "catalog_number":"100",
      "title":"An Introduction to Classical Studies"
    },
    {
      "course_id":"009519",
      "subject":"CLAS",
      "catalog_number":"103",
      "title":"Colossos - The Major Figures of Classical Antiquity"
    },
    {
      "course_id":"012910",
      "subject":"CLAS",
      "catalog_number":"104",
      "title":"Classical Mythology"
    },
    {
      "course_id":"011784",
      "subject":"CLAS",
      "catalog_number":"105",
      "title":"Introduction to Medieval Studies"
    },
    {
      "course_id":"004266",
      "subject":"CLAS",
      "catalog_number":"201",
      "title":"Ancient Greek Society"
    },
    {
      "course_id":"004267",
      "subject":"CLAS",
      "catalog_number":"202",
      "title":"Ancient Roman Society"
    },
    {
      "course_id":"004280",
      "subject":"CLAS",
      "catalog_number":"205",
      "title":"Medieval Society"
    },
    {
      "course_id":"006241",
      "subject":"CLAS",
      "catalog_number":"210",
      "title":"History of Ancient Law"
    },
    {
      "course_id":"003396",
      "subject":"CLAS",
      "catalog_number":"221",
      "title":"Archaeological Anthropology"
    },
    {
      "course_id":"009520",
      "subject":"CLAS",
      "catalog_number":"230",
      "title":"Classical Roots of English Vocabulary"
    },
    {
      "course_id":"011785",
      "subject":"CLAS",
      "catalog_number":"231",
      "title":"Survey of Greek Literature"
    },
    {
      "course_id":"011786",
      "subject":"CLAS",
      "catalog_number":"232",
      "title":"Survey of Roman Literature"
    },
    {
      "course_id":"006279",
      "subject":"CLAS",
      "catalog_number":"237",
      "title":"The Ancient Near East and Egypt"
    },
    {
      "course_id":"005478",
      "subject":"CLAS",
      "catalog_number":"241",
      "title":"Survey of Greek Art and Architecture"
    },
    {
      "course_id":"005480",
      "subject":"CLAS",
      "catalog_number":"242",
      "title":"Survey of Roman Art and Architecture"
    },
    {
      "course_id":"004278",
      "subject":"CLAS",
      "catalog_number":"251",
      "title":"Greek History"
    },
    {
      "course_id":"004279",
      "subject":"CLAS",
      "catalog_number":"252",
      "title":"Roman History"
    },
    {
      "course_id":"007248",
      "subject":"CLAS",
      "catalog_number":"261",
      "title":"Great Works: Ancient and Medieval"
    },
    {
      "course_id":"004287",
      "subject":"CLAS",
      "catalog_number":"311",
      "title":"Women in Classical Antiquity"
    },
    {
      "course_id":"003446",
      "subject":"CLAS",
      "catalog_number":"321",
      "title":"Archaeology of Complex Cultures"
    },
    {
      "course_id":"004290",
      "subject":"CLAS",
      "catalog_number":"325",
      "title":"Greek and Roman Religion"
    },
    {
      "course_id":"011787",
      "subject":"CLAS",
      "catalog_number":"327",
      "title":"Astrology and Magic"
    },
    {
      "course_id":"012911",
      "subject":"CLAS",
      "catalog_number":"331",
      "title":"Advanced Studies in Ancient Literature"
    },
    {
      "course_id":"012914",
      "subject":"CLAS",
      "catalog_number":"341",
      "title":"Advanced Studies in Greek Art and Architecture"
    },
    {
      "course_id":"012915",
      "subject":"CLAS",
      "catalog_number":"342",
      "title":"Advanced Studies in Roman Art and Architecture"
    },
    {
      "course_id":"012912",
      "subject":"CLAS",
      "catalog_number":"351",
      "title":"Advanced Studies in Greek History"
    },
    {
      "course_id":"012913",
      "subject":"CLAS",
      "catalog_number":"352",
      "title":"Advanced Studies in Roman History"
    },
    {
      "course_id":"007324",
      "subject":"CLAS",
      "catalog_number":"361",
      "title":"History of Ancient Philosophy"
    },
    {
      "course_id":"007325",
      "subject":"CLAS",
      "catalog_number":"362",
      "title":"History of Ancient Philosophy 2"
    },
    {
      "course_id":"004300",
      "subject":"CLAS",
      "catalog_number":"384",
      "title":"Science and Technology of Ancient Greece and Rome"
    },
    {
      "course_id":"004301",
      "subject":"CLAS",
      "catalog_number":"390",
      "title":"Classical Studies Abroad"
    },
    {
      "course_id":"013557",
      "subject":"CLAS",
      "catalog_number":"395",
      "title":"Research Skills Training"
    },
    {
      "course_id":"011189",
      "subject":"CLAS",
      "catalog_number":"461",
      "title":"Studies in Ancient Philosophy"
    },
    {
      "course_id":"004303",
      "subject":"CLAS",
      "catalog_number":"485",
      "title":"Greco-Roman Civilization and History"
    },
    {
      "course_id":"009523",
      "subject":"CLAS",
      "catalog_number":"486",
      "title":"Senior Seminar"
    },
    {
      "course_id":"004315",
      "subject":"CLAS",
      "catalog_number":"490A",
      "title":"Senior Honours Thesis"
    },
    {
      "course_id":"004316",
      "subject":"CLAS",
      "catalog_number":"490B",
      "title":"Senior Honours Thesis"
    },
    {
      "course_id":"004317",
      "subject":"CLAS",
      "catalog_number":"492",
      "title":"Directed Study"
    },
    {
      "course_id":"013021",
      "subject":"CLAS",
      "catalog_number":"600",
      "title":"Research Methods in Classical Studies"
    },
    {
      "course_id":"013033",
      "subject":"CLAS",
      "catalog_number":"601",
      "title":"The Integration of the Ancient Mediterranean World"
    },
    {
      "course_id":"014416",
      "subject":"CLAS",
      "catalog_number":"631",
      "title":"Studies in Greek Literature"
    },
    {
      "course_id":"013758",
      "subject":"CLAS",
      "catalog_number":"632",
      "title":"Studies in Latin Literature"
    },
    {
      "course_id":"013022",
      "subject":"CLAS",
      "catalog_number":"633",
      "title":"Studies in Ancient Literature"
    },
    {
      "course_id":"013037",
      "subject":"CLAS",
      "catalog_number":"641",
      "title":"Studies in Greek Art and Architecture"
    },
    {
      "course_id":"014417",
      "subject":"CLAS",
      "catalog_number":"642",
      "title":"Studies in Roman Art in Architecture"
    },
    {
      "course_id":"013024",
      "subject":"CLAS",
      "catalog_number":"643",
      "title":"Studies in Ancient Art and Architecture"
    },
    {
      "course_id":"014418",
      "subject":"CLAS",
      "catalog_number":"651",
      "title":"Topics in Greek History"
    },
    {
      "course_id":"014419",
      "subject":"CLAS",
      "catalog_number":"652",
      "title":"Topics in Roman History"
    },
    {
      "course_id":"013025",
      "subject":"CLAS",
      "catalog_number":"653",
      "title":"Topics in Ancient History"
    },
    {
      "course_id":"014420",
      "subject":"CLAS",
      "catalog_number":"695",
      "title":"Classical Studies Abroad"
    },
    {
      "course_id":"011431",
      "subject":"CM",
      "catalog_number":"361",
      "title":"Computational Statistics and Data Analysis"
    },
    {
      "course_id":"011444",
      "subject":"CM",
      "catalog_number":"375",
      "title":"Computational Linear Algebra"
    },
    {
      "course_id":"012670",
      "subject":"CM",
      "catalog_number":"670",
      "title":"Numerical Analysis"
    },
    {
      "course_id":"000626",
      "subject":"CM",
      "catalog_number":"730",
      "title":"Introduction to Symbolic Computation"
    },
    {
      "course_id":"012176",
      "subject":"CM",
      "catalog_number":"740",
      "title":"Fundamentals of Optimization"
    },
    {
      "course_id":"000724",
      "subject":"CM",
      "catalog_number":"750",
      "title":"Numerical Solution of Partial Differential Equations"
    },
    {
      "course_id":"003090",
      "subject":"CM",
      "catalog_number":"761",
      "title":"Computational Inference"
    },
    {
      "course_id":"012612",
      "subject":"CM",
      "catalog_number":"762",
      "title":"Data Visualization"
    },
    {
      "course_id":"003091",
      "subject":"CM",
      "catalog_number":"763",
      "title":"Statistical Learning - Classification"
    },
    {
      "course_id":"003092",
      "subject":"CM",
      "catalog_number":"764",
      "title":"Statistical Learning - Function Estimation"
    },
    {
      "course_id":"012289",
      "subject":"CMW",
      "catalog_number":"201",
      "title":"Worship Practicum 1"
    },
    {
      "course_id":"012290",
      "subject":"CMW",
      "catalog_number":"202",
      "title":"Worship Practicum 2"
    },
    {
      "course_id":"007051",
      "subject":"CMW",
      "catalog_number":"363",
      "title":"Christian Hymnody"
    },
    {
      "course_id":"007052",
      "subject":"CMW",
      "catalog_number":"364",
      "title":"Worship and Music"
    },
    {
      "course_id":"013525",
      "subject":"CMW",
      "catalog_number":"390",
      "title":"Special Topics in Church Music and Worship"
    },
    {
      "course_id":"003887",
      "subject":"CO",
      "catalog_number":"227",
      "title":"Introduction to Optimization (Non-Specialist Level)"
    },
    {
      "course_id":"003895",
      "subject":"CO",
      "catalog_number":"250",
      "title":"Introduction to Optimization"
    },
    {
      "course_id":"003897",
      "subject":"CO",
      "catalog_number":"255",
      "title":"Introduction to Optimization (Advanced Level)"
    },
    {
      "course_id":"003890",
      "subject":"CO",
      "catalog_number":"327",
      "title":"Deterministic OR Models (Non-Specialist Level)"
    },
    {
      "course_id":"003891",
      "subject":"CO",
      "catalog_number":"330",
      "title":"Combinatorial Enumeration"
    },
    {
      "course_id":"003892",
      "subject":"CO",
      "catalog_number":"331",
      "title":"Coding Theory"
    },
    {
      "course_id":"003893",
      "subject":"CO",
      "catalog_number":"342",
      "title":"Introduction to Graph Theory"
    },
    {
      "course_id":"003896",
      "subject":"CO",
      "catalog_number":"351",
      "title":"Network Flow Theory"
    },
    {
      "course_id":"011442",
      "subject":"CO",
      "catalog_number":"353",
      "title":"Computational Discrete Optimization"
    },
    {
      "course_id":"003898",
      "subject":"CO",
      "catalog_number":"367",
      "title":"Nonlinear Optimization"
    },
    {
      "course_id":"003899",
      "subject":"CO",
      "catalog_number":"370",
      "title":"Deterministic OR Models"
    },
    {
      "course_id":"011736",
      "subject":"CO",
      "catalog_number":"372",
      "title":"Portfolio Optimization Models"
    },
    {
      "course_id":"003901",
      "subject":"CO",
      "catalog_number":"380",
      "title":"Mathematical Discovery and Invention"
    },
    {
      "course_id":"003902",
      "subject":"CO",
      "catalog_number":"430",
      "title":"Algebraic Enumeration"
    },
    {
      "course_id":"003903",
      "subject":"CO",
      "catalog_number":"434",
      "title":"Combinatorial Designs"
    },
    {
      "course_id":"003906",
      "subject":"CO",
      "catalog_number":"439",
      "title":"Topics in Combinatorics"
    },
    {
      "course_id":"003907",
      "subject":"CO",
      "catalog_number":"440",
      "title":"Topics in Graph Theory"
    },
    {
      "course_id":"003908",
      "subject":"CO",
      "catalog_number":"442",
      "title":"Graph Theory"
    },
    {
      "course_id":"003909",
      "subject":"CO",
      "catalog_number":"444",
      "title":"Algebraic Graph Theory"
    },
    {
      "course_id":"013337",
      "subject":"CO",
      "catalog_number":"446",
      "title":"Matroid Theory"
    },
    {
      "course_id":"003910",
      "subject":"CO",
      "catalog_number":"450",
      "title":"Combinatorial Optimization"
    },
    {
      "course_id":"003911",
      "subject":"CO",
      "catalog_number":"452",
      "title":"Integer Programming"
    },
    {
      "course_id":"003912",
      "subject":"CO",
      "catalog_number":"453",
      "title":"Network Design"
    },
    {
      "course_id":"003913",
      "subject":"CO",
      "catalog_number":"454",
      "title":"Scheduling"
    },
    {
      "course_id":"003914",
      "subject":"CO",
      "catalog_number":"456",
      "title":"Introduction to Game Theory"
    },
    {
      "course_id":"010046",
      "subject":"CO",
      "catalog_number":"459",
      "title":"Topics in Optimization"
    },
    {
      "course_id":"010047",
      "subject":"CO",
      "catalog_number":"463",
      "title":"Convex Optimization and Analysis"
    },
    {
      "course_id":"014722",
      "subject":"COGSCI",
      "catalog_number":"300",
      "title":"Intelligence in Machines, Humans, and Other Animals"
    },
    {
      "course_id":"003917",
      "subject":"CO",
      "catalog_number":"466",
      "title":"Continuous Optimization"
    },
    {
      "course_id":"011364",
      "subject":"CO",
      "catalog_number":"471",
      "title":"Semidefinite Optimization"
    },
    {
      "course_id":"003918",
      "subject":"CO",
      "catalog_number":"480",
      "title":"History of Mathematics"
    },
    {
      "course_id":"011497",
      "subject":"CO",
      "catalog_number":"481",
      "title":"Introduction to Quantum Information Processing"
    },
    {
      "course_id":"010137",
      "subject":"CO",
      "catalog_number":"485",
      "title":"The Mathematics of Public-Key Cryptography"
    },
    {
      "course_id":"010136",
      "subject":"CO",
      "catalog_number":"487",
      "title":"Applied Cryptography"
    },
    {
      "course_id":"003920",
      "subject":"CO",
      "catalog_number":"499",
      "title":"Reading in Combinatorics and Optimization"
    },
    {
      "course_id":"012175",
      "subject":"CO",
      "catalog_number":"601",
      "title":"Fundamentals of Enumerative Combinatorics"
    },
    {
      "course_id":"012176",
      "subject":"CO",
      "catalog_number":"602",
      "title":"Fundamentals of Optimization"
    },
    {
      "course_id":"000232",
      "subject":"CO",
      "catalog_number":"630",
      "title":"Algebraic Enumeration"
    },
    {
      "course_id":"014211",
      "subject":"CO",
      "catalog_number":"631",
      "title":"Symmetric Functions"
    },
    {
      "course_id":"000233",
      "subject":"CO",
      "catalog_number":"634",
      "title":"Combinatorial Designs"
    },
    {
      "course_id":"010470",
      "subject":"CO",
      "catalog_number":"639",
      "title":"Topics in Combinatorics"
    },
    {
      "course_id":"000239",
      "subject":"CO",
      "catalog_number":"640",
      "title":"Topics in Graph Theory"
    },
    {
      "course_id":"000245",
      "subject":"CO",
      "catalog_number":"642",
      "title":"Graph Theory"
    },
    {
      "course_id":"000246",
      "subject":"CO",
      "catalog_number":"644",
      "title":"Algebraic Graph Theory"
    },
    {
      "course_id":"013351",
      "subject":"CO",
      "catalog_number":"646",
      "title":"Matroid Theory"
    },
    {
      "course_id":"000247",
      "subject":"CO",
      "catalog_number":"650",
      "title":"Combinatorial Optimization"
    },
    {
      "course_id":"000248",
      "subject":"CO",
      "catalog_number":"652",
      "title":"Integer Programming"
    },
    {
      "course_id":"000250",
      "subject":"CO",
      "catalog_number":"663",
      "title":"Convex Optimization and  Analysis"
    },
    {
      "course_id":"000251",
      "subject":"CO",
      "catalog_number":"664",
      "title":"Quadratic Programming"
    },
    {
      "course_id":"000252",
      "subject":"CO",
      "catalog_number":"666",
      "title":"Continuous Optimization"
    },
    {
      "course_id":"011371",
      "subject":"CO",
      "catalog_number":"671",
      "title":"Semidefinite Optimization"
    },
    {
      "course_id":"011589",
      "subject":"CO",
      "catalog_number":"681",
      "title":"Quantum Information Processing"
    },
    {
      "course_id":"010331",
      "subject":"CO",
      "catalog_number":"685",
      "title":"The Mathematics of Public-Key Cryptography"
    },
    {
      "course_id":"010471",
      "subject":"CO",
      "catalog_number":"687",
      "title":"Applied Cryptography"
    },
    {
      "course_id":"000253",
      "subject":"CO",
      "catalog_number":"690",
      "title":"Literature and Research Studies"
    },
    {
      "course_id":"000269",
      "subject":"CO",
      "catalog_number":"730",
      "title":"Asymptotic Enumeration"
    },
    {
      "course_id":"010473",
      "subject":"CO",
      "catalog_number":"734",
      "title":"Topics in Combinatorial Design"
    },
    {
      "course_id":"011796",
      "subject":"CO",
      "catalog_number":"738",
      "title":"Probabilistic Methods in Discrete Mathematics"
    },
    {
      "course_id":"000273",
      "subject":"CO",
      "catalog_number":"739",
      "title":"Topics in Combinatorics"
    },
    {
      "course_id":"000297",
      "subject":"CO",
      "catalog_number":"743",
      "title":"Directed Graphs and Applications"
    },
    {
      "course_id":"010474",
      "subject":"CO",
      "catalog_number":"745",
      "title":"Graph Theory Algorithms"
    },
    {
      "course_id":"000298",
      "subject":"CO",
      "catalog_number":"749",
      "title":"Topics in Graph Theory"
    },
    {
      "course_id":"000304",
      "subject":"CO",
      "catalog_number":"750",
      "title":"Topics in Combinatorial Optimization"
    },
    {
      "course_id":"000310",
      "subject":"CO",
      "catalog_number":"751",
      "title":"Topics in Matroid Theory"
    },
    {
      "course_id":"011797",
      "subject":"CO",
      "catalog_number":"754",
      "title":"Approximation Algorithms in Combinatorial Optimization"
    },
    {
      "course_id":"000311",
      "subject":"CO",
      "catalog_number":"759",
      "title":"Topics in Discrete Optimization"
    },
    {
      "course_id":"010475",
      "subject":"CO",
      "catalog_number":"765",
      "title":"Mathematical Programming"
    },
    {
      "course_id":"000317",
      "subject":"CO",
      "catalog_number":"769",
      "title":"Topics in Continuous Optimization"
    },
    {
      "course_id":"010476",
      "subject":"CO",
      "catalog_number":"771",
      "title":"Mathematical Operations Research"
    },
    {
      "course_id":"011622",
      "subject":"CO",
      "catalog_number":"778",
      "title":"Portfolio Optimization"
    },
    {
      "course_id":"010477",
      "subject":"CO",
      "catalog_number":"779",
      "title":"Topics in Operations Research"
    },
    {
      "course_id":"011847",
      "subject":"CO",
      "catalog_number":"781",
      "title":"Topics in Quantum Information"
    },
    {
      "course_id":"013602",
      "subject":"CS",
      "catalog_number":"640",
      "title":"Principles of Database Management and Use"
    },
    {
      "course_id":"011299",
      "subject":"CO",
      "catalog_number":"785",
      "title":"Algorithmic Number Theory"
    },
    {
      "course_id":"011277",
      "subject":"CO",
      "catalog_number":"789",
      "title":"Topics in Cryptography"
    },
    {
      "course_id":"000332",
      "subject":"CO",
      "catalog_number":"839",
      "title":"Seminar in Combinatorics"
    },
    {
      "course_id":"010479",
      "subject":"CO",
      "catalog_number":"849",
      "title":"Seminar in Graph Theory"
    },
    {
      "course_id":"010480",
      "subject":"CO",
      "catalog_number":"859",
      "title":"Seminar in Discrete Optimization"
    },
    {
      "course_id":"010481",
      "subject":"CO",
      "catalog_number":"869",
      "title":"Seminar in Continuous Optimization"
    },
    {
      "course_id":"010482",
      "subject":"CO",
      "catalog_number":"879",
      "title":"Seminar in Operations Research"
    },
    {
      "course_id":"011205",
      "subject":"COGSCI",
      "catalog_number":"600",
      "title":"Seminar in Cognitive Science"
    },
    {
      "course_id":"013541",
      "subject":"COMM",
      "catalog_number":"101",
      "title":"Introduction to Business 1"
    },
    {
      "course_id":"013542",
      "subject":"COMM",
      "catalog_number":"102",
      "title":"Introduction to Business 2"
    },
    {
      "course_id":"014062",
      "subject":"COMM",
      "catalog_number":"103",
      "title":"Principles of Economics"
    },
    {
      "course_id":"006938",
      "subject":"COMM",
      "catalog_number":"231",
      "title":"Commercial and Business Law for Mathematics Students"
    },
    {
      "course_id":"012745",
      "subject":"COMM",
      "catalog_number":"321",
      "title":"Intermediate Accounting for Finance"
    },
    {
      "course_id":"006943",
      "subject":"COMM",
      "catalog_number":"400",
      "title":"Entrepreneurship, Technology and the Emerging Information Economy"
    },
    {
      "course_id":"012747",
      "subject":"COMM",
      "catalog_number":"421",
      "title":"Financial Statement Analysis"
    },
    {
      "course_id":"012954",
      "subject":"COMM",
      "catalog_number":"431",
      "title":"Project Management"
    },
    {
      "course_id":"012955",
      "subject":"COMM",
      "catalog_number":"432",
      "title":"Electronic Business"
    },
    {
      "course_id":"011509",
      "subject":"COOP",
      "catalog_number":"1",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011510",
      "subject":"COOP",
      "catalog_number":"2",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011511",
      "subject":"COOP",
      "catalog_number":"3",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011512",
      "subject":"COOP",
      "catalog_number":"4",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011513",
      "subject":"COOP",
      "catalog_number":"5",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011514",
      "subject":"COOP",
      "catalog_number":"6",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011515",
      "subject":"COOP",
      "catalog_number":"7",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011516",
      "subject":"COOP",
      "catalog_number":"8",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011517",
      "subject":"COOP",
      "catalog_number":"9",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"011518",
      "subject":"COOP",
      "catalog_number":"10",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"012308",
      "subject":"COOP",
      "catalog_number":"11",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"012568",
      "subject":"COOP",
      "catalog_number":"12",
      "title":"Co-operative Work Term"
    },
    {
      "course_id":"009226",
      "subject":"COOP",
      "catalog_number":"101",
      "title":"Career Success Strategies"
    },
    {
      "course_id":"011503",
      "subject":"COOP",
      "catalog_number":"1G",
      "title":"Graduate Studies Co-operative Work Term 1"
    },
    {
      "course_id":"011504",
      "subject":"COOP",
      "catalog_number":"2G",
      "title":"Graduate Studies  Co-operative Work Term 2"
    },
    {
      "course_id":"012276",
      "subject":"COOP",
      "catalog_number":"3G",
      "title":"Graduate Studies Co-operative Work Term 3"
    },
    {
      "course_id":"012566",
      "subject":"COOP",
      "catalog_number":"601",
      "title":"Career Success Strategies"
    },
    {
      "course_id":"004344",
      "subject":"CROAT",
      "catalog_number":"101",
      "title":"Elementary Croatian 1"
    },
    {
      "course_id":"004346",
      "subject":"CROAT",
      "catalog_number":"102",
      "title":"Elementary Croatian II"
    },
    {
      "course_id":"004347",
      "subject":"CROAT",
      "catalog_number":"201",
      "title":"Intermediate Croatian I"
    },
    {
      "course_id":"004348",
      "subject":"CROAT",
      "catalog_number":"202",
      "title":"Intermediate Croatian II"
    },
    {
      "course_id":"004356",
      "subject":"CROAT",
      "catalog_number":"496",
      "title":"Special Topics in Croatian Studies"
    },
    {
      "course_id":"004360",
      "subject":"CS",
      "catalog_number":"100",
      "title":"Introduction to Computing through Applications"
    },
    {
      "course_id":"012765",
      "subject":"CS",
      "catalog_number":"115",
      "title":"Introduction to Computer Science 1"
    },
    {
      "course_id":"012766",
      "subject":"CS",
      "catalog_number":"116",
      "title":"Introduction to Computer Science 2"
    },
    {
      "course_id":"012040",
      "subject":"CS",
      "catalog_number":"135",
      "title":"Designing Functional Programs"
    },
    {
      "course_id":"012041",
      "subject":"CS",
      "catalog_number":"136",
      "title":"Elementary Algorithm Design and Data Abstraction"
    },
    {
      "course_id":"012886",
      "subject":"CS",
      "catalog_number":"137",
      "title":"Programming Principles"
    },
    {
      "course_id":"012887",
      "subject":"CS",
      "catalog_number":"138",
      "title":"Introduction to Data Abstraction and Implementation"
    },
    {
      "course_id":"012767",
      "subject":"CS",
      "catalog_number":"145",
      "title":"Designing Functional Programs (Advanced Level)"
    },
    {
      "course_id":"013657",
      "subject":"CS",
      "catalog_number":"146",
      "title":"Elementary Algorithm Design and Data Abstraction (Advanced Level)"
    },
    {
      "course_id":"004372",
      "subject":"CS",
      "catalog_number":"200",
      "title":"Concepts for Advanced Computer Usage"
    },
    {
      "course_id":"004374",
      "subject":"CS",
      "catalog_number":"230",
      "title":"Introduction to Computers and Computer Systems"
    },
    {
      "course_id":"004375",
      "subject":"CS",
      "catalog_number":"234",
      "title":"Data Types and Structures"
    },
    {
      "course_id":"004377",
      "subject":"CS",
      "catalog_number":"240",
      "title":"Data Structures and Data Management"
    },
    {
      "course_id":"004378",
      "subject":"CS",
      "catalog_number":"241",
      "title":"Foundations of Sequential Programs"
    },
    {
      "course_id":"011405",
      "subject":"CS",
      "catalog_number":"245",
      "title":"Logic and Computation"
    },
    {
      "course_id":"004380",
      "subject":"CS",
      "catalog_number":"246",
      "title":"Object-Oriented Software Development"
    },
    {
      "course_id":"013805",
      "subject":"CS",
      "catalog_number":"247",
      "title":"Software Engineering Principles"
    },
    {
      "course_id":"004382",
      "subject":"CS",
      "catalog_number":"251",
      "title":"Computer Organization and Design"
    },
    {
      "course_id":"004385",
      "subject":"CS",
      "catalog_number":"330",
      "title":"Management Information Systems"
    },
    {
      "course_id":"013658",
      "subject":"CS",
      "catalog_number":"335",
      "title":"Computational Methods in Business and Finance"
    },
    {
      "course_id":"004390",
      "subject":"CS",
      "catalog_number":"338",
      "title":"Computer Applications in Business: Databases"
    },
    {
      "course_id":"004392",
      "subject":"CS",
      "catalog_number":"341",
      "title":"Algorithms"
    },
    {
      "course_id":"011417",
      "subject":"CS",
      "catalog_number":"343",
      "title":"Concurrent and Parallel Programming"
    },
    {
      "course_id":"004417",
      "subject":"CS",
      "catalog_number":"348",
      "title":"Introduction to Database Management"
    },
    {
      "course_id":"011727",
      "subject":"CS",
      "catalog_number":"349",
      "title":"User Interfaces"
    },
    {
      "course_id":"011416",
      "subject":"CS",
      "catalog_number":"350",
      "title":"Operating Systems"
    },
    {
      "course_id":"004398",
      "subject":"CS",
      "catalog_number":"360",
      "title":"Introduction to the Theory of Computing"
    },
    {
      "course_id":"011347",
      "subject":"CS",
      "catalog_number":"365",
      "title":"Models of Computation"
    },
    {
      "course_id":"004400",
      "subject":"CS",
      "catalog_number":"370",
      "title":"Numerical Computation"
    },
    {
      "course_id":"011363",
      "subject":"CS",
      "catalog_number":"371",
      "title":"Introduction to Computational Mathematics"
    },
    {
      "course_id":"011409",
      "subject":"CS",
      "catalog_number":"398",
      "title":"Topics in Computer Science"
    },
    {
      "course_id":"011410",
      "subject":"CS",
      "catalog_number":"399",
      "title":"Readings in Computer Science"
    },
    {
      "course_id":"004404",
      "subject":"CS",
      "catalog_number":"430",
      "title":"Applications Software Engineering"
    },
    {
      "course_id":"004405",
      "subject":"CS",
      "catalog_number":"432",
      "title":"Business Systems Analysis"
    },
    {
      "course_id":"004407",
      "subject":"CS",
      "catalog_number":"436",
      "title":"Networks and Distributed Computer Systems"
    },
    {
      "course_id":"004410",
      "subject":"CS",
      "catalog_number":"442",
      "title":"Principles of Programming Languages"
    },
    {
      "course_id":"004412",
      "subject":"CS",
      "catalog_number":"444",
      "title":"Compiler Construction"
    },
    {
      "course_id":"004413",
      "subject":"CS",
      "catalog_number":"445",
      "title":"Software Requirements Specification and Analysis"
    },
    {
      "course_id":"004414",
      "subject":"CS",
      "catalog_number":"446",
      "title":"Software Design and Architectures"
    },
    {
      "course_id":"004416",
      "subject":"CS",
      "catalog_number":"447",
      "title":"Software Testing, Quality Assurance and Maintenance"
    },
    {
      "course_id":"012300",
      "subject":"CS",
      "catalog_number":"448",
      "title":"Database Systems Implementation"
    },
    {
      "course_id":"013910",
      "subject":"CS",
      "catalog_number":"449",
      "title":"Human-Computer Interaction"
    },
    {
      "course_id":"004418",
      "subject":"CS",
      "catalog_number":"450",
      "title":"Computer Architecture"
    },
    {
      "course_id":"004419",
      "subject":"CS",
      "catalog_number":"452",
      "title":"Real-time Programming"
    },
    {
      "course_id":"004420",
      "subject":"CS",
      "catalog_number":"454",
      "title":"Distributed Systems"
    },
    {
      "course_id":"010167",
      "subject":"CS",
      "catalog_number":"456",
      "title":"Computer Networks"
    },
    {
      "course_id":"004422",
      "subject":"CS",
      "catalog_number":"457",
      "title":"System Performance Evaluation"
    },
    {
      "course_id":"012980",
      "subject":"CS",
      "catalog_number":"458",
      "title":"Computer Security and Privacy"
    },
    {
      "course_id":"004424",
      "subject":"CS",
      "catalog_number":"462",
      "title":"Formal Languages and Parsing"
    },
    {
      "course_id":"004426",
      "subject":"CS",
      "catalog_number":"466",
      "title":"Algorithm Design and Analysis"
    },
    {
      "course_id":"011497",
      "subject":"CS",
      "catalog_number":"467",
      "title":"Introduction to Quantum Information Processing"
    },
    {
      "course_id":"011446",
      "subject":"CS",
      "catalog_number":"473",
      "title":"Medical Image Processing"
    },
    {
      "course_id":"011444",
      "subject":"CS",
      "catalog_number":"475",
      "title":"Computational Linear Algebra"
    },
    {
      "course_id":"003352",
      "subject":"CS",
      "catalog_number":"476",
      "title":"Numeric Computation for Financial Modeling"
    },
    {
      "course_id":"004434",
      "subject":"CS",
      "catalog_number":"482",
      "title":"Computational Techniques in Biological Sequence Analysis"
    },
    {
      "course_id":"010043",
      "subject":"CS",
      "catalog_number":"483",
      "title":"Computational Techniques in Structural Bioinformatics"
    },
    {
      "course_id":"013912",
      "subject":"CS",
      "catalog_number":"484",
      "title":"Computational Vision"
    },
    {
      "course_id":"013911",
      "subject":"CS",
      "catalog_number":"485",
      "title":"Machine Learning: Statistical and Computational Foundations"
    },
    {
      "course_id":"004435",
      "subject":"CS",
      "catalog_number":"486",
      "title":"Introduction to Artificial Intelligence"
    },
    {
      "course_id":"004436",
      "subject":"CS",
      "catalog_number":"487",
      "title":"Introduction to Symbolic Computation"
    },
    {
      "course_id":"004437",
      "subject":"CS",
      "catalog_number":"488",
      "title":"Introduction to Computer Graphics"
    },
    {
      "course_id":"010044",
      "subject":"CS",
      "catalog_number":"489",
      "title":"Advanced Topics in Computer Science"
    },
    {
      "course_id":"004433",
      "subject":"CS",
      "catalog_number":"490",
      "title":"Information Systems Management"
    },
    {
      "course_id":"004438",
      "subject":"CS",
      "catalog_number":"492",
      "title":"The Social Implications of Computing"
    },
    {
      "course_id":"012280",
      "subject":"CS",
      "catalog_number":"497",
      "title":"Multidisciplinary Studies in Computer Science"
    },
    {
      "course_id":"004444",
      "subject":"CS",
      "catalog_number":"499R",
      "title":"Readings in Computer Science"
    },
    {
      "course_id":"012560",
      "subject":"CS",
      "catalog_number":"499T",
      "title":"Honours Thesis"
    },
    {
      "course_id":"000599",
      "subject":"CS",
      "catalog_number":"642",
      "title":"Principles of Programming Languages"
    },
    {
      "course_id":"000601",
      "subject":"CS",
      "catalog_number":"644",
      "title":"Compiler Construction"
    },
    {
      "course_id":"000602",
      "subject":"CS",
      "catalog_number":"645",
      "title":"Software Requirements Specification and Analysis"
    },
    {
      "course_id":"000603",
      "subject":"CS",
      "catalog_number":"646",
      "title":"Software Design and  Architectures"
    },
    {
      "course_id":"000604",
      "subject":"CS",
      "catalog_number":"647",
      "title":"Software Testing, Quality Assurance and Maintenance"
    },
    {
      "course_id":"000605",
      "subject":"CS",
      "catalog_number":"648",
      "title":"Database Systems Implementation"
    },
    {
      "course_id":"014064",
      "subject":"CS",
      "catalog_number":"649",
      "title":"Human-Computer Interaction"
    },
    {
      "course_id":"000606",
      "subject":"CS",
      "catalog_number":"650",
      "title":"Computer Architecture"
    },
    {
      "course_id":"000607",
      "subject":"CS",
      "catalog_number":"652",
      "title":"Real-Time Programming"
    },
    {
      "course_id":"000608",
      "subject":"CS",
      "catalog_number":"654",
      "title":"Distributed Systems"
    },
    {
      "course_id":"000609",
      "subject":"CS",
      "catalog_number":"656",
      "title":"Computer Networks"
    },
    {
      "course_id":"000610",
      "subject":"CS",
      "catalog_number":"657",
      "title":"System Performance Evaluation"
    },
    {
      "course_id":"000611",
      "subject":"CS",
      "catalog_number":"658",
      "title":"Computer Security and Privacy"
    },
    {
      "course_id":"000612",
      "subject":"CS",
      "catalog_number":"662",
      "title":"Formal Languages and Parsing"
    },
    {
      "course_id":"000613",
      "subject":"CS",
      "catalog_number":"664",
      "title":"Computational Complexity Theory"
    },
    {
      "course_id":"000614",
      "subject":"CS",
      "catalog_number":"666",
      "title":"Algorithm Design and Analysis"
    },
    {
      "course_id":"011588",
      "subject":"CS",
      "catalog_number":"673",
      "title":"Medical Image Processing"
    },
    {
      "course_id":"014065",
      "subject":"CS",
      "catalog_number":"675",
      "title":"Computational Linear Algebra"
    },
    {
      "course_id":"000620",
      "subject":"CS",
      "catalog_number":"676",
      "title":"Numeric Computation for Financial Modelling"
    },
    {
      "course_id":"011302",
      "subject":"CS",
      "catalog_number":"682",
      "title":"Computational Techniques in Biological Sequence Analysis"
    },
    {
      "course_id":"011303",
      "subject":"CS",
      "catalog_number":"683",
      "title":"Computational Techniques in Structural Bioinformatics"
    },
    {
      "course_id":"000623",
      "subject":"CS",
      "catalog_number":"684",
      "title":"Computational Vision"
    },
    {
      "course_id":"000624",
      "subject":"CS",
      "catalog_number":"685",
      "title":"Machine Learning: Statistical and Computational Foundations"
    },
    {
      "course_id":"000625",
      "subject":"CS",
      "catalog_number":"686",
      "title":"Introduction to Artificial Intelligence"
    },
    {
      "course_id":"000626",
      "subject":"CS",
      "catalog_number":"687",
      "title":"Introduction to Symbolic Computation"
    },
    {
      "course_id":"000627",
      "subject":"CS",
      "catalog_number":"688",
      "title":"Introduction to Computer Graphics"
    },
    {
      "course_id":"000630",
      "subject":"CS",
      "catalog_number":"690A",
      "title":"Literature and Research Studies"
    },
    {
      "course_id":"000631",
      "subject":"CS",
      "catalog_number":"690B",
      "title":"Literature and Research Studies"
    },
    {
      "course_id":"000632",
      "subject":"CS",
      "catalog_number":"692",
      "title":"The Social Implications of Computing"
    },
    {
      "course_id":"009076",
      "subject":"CS",
      "catalog_number":"697",
      "title":"Graduate Research Skills Seminar"
    },
    {
      "course_id":"010461",
      "subject":"CS",
      "catalog_number":"698",
      "title":"Introductory Research Topics"
    },
    {
      "course_id":"011293",
      "subject":"CS",
      "catalog_number":"740",
      "title":"Database Engineering"
    },
    {
      "course_id":"011294",
      "subject":"CS",
      "catalog_number":"741",
      "title":"Non-Traditional Databases"
    },
    {
      "course_id":"000650",
      "subject":"CS",
      "catalog_number":"742",
      "title":"Parallel and Distributed Database Systems"
    },
    {
      "course_id":"013602",
      "subject":"CS",
      "catalog_number":"743",
      "title":"Principles of Database Management and Use"
    },
    {
      "course_id":"000655",
      "subject":"CS",
      "catalog_number":"744",
      "title":"Advanced Compiler Design"
    },
    {
      "course_id":"011295",
      "subject":"CS",
      "catalog_number":"745",
      "title":"Computer-Aided Verification"
    },
    {
      "course_id":"000656",
      "subject":"CS",
      "catalog_number":"746",
      "title":"Software Architecture"
    },
    {
      "course_id":"013603",
      "subject":"CS",
      "catalog_number":"755",
      "title":"System and Network Architectures and Implementation"
    },
    {
      "course_id":"011590",
      "subject":"CS",
      "catalog_number":"758",
      "title":"Cryptography\/Network Security"
    },
    {
      "course_id":"011296",
      "subject":"CS",
      "catalog_number":"761",
      "title":"Randomized Algorithms"
    },
    {
      "course_id":"000710",
      "subject":"CS",
      "catalog_number":"762",
      "title":"Graph-Theoretic Algorithms"
    },
    {
      "course_id":"011297",
      "subject":"CS",
      "catalog_number":"763",
      "title":"Computational Geometry"
    },
    {
      "course_id":"011298",
      "subject":"CS",
      "catalog_number":"764",
      "title":"Computational Complexity"
    },
    {
      "course_id":"011299",
      "subject":"CS",
      "catalog_number":"765",
      "title":"Algorithmic Number Theory"
    },
    {
      "course_id":"000711",
      "subject":"CS",
      "catalog_number":"766",
      "title":"Theory of Quantum Information"
    },
    {
      "course_id":"000712",
      "subject":"CS",
      "catalog_number":"767",
      "title":"Advanced Logic for Computer Science"
    },
    {
      "course_id":"011589",
      "subject":"CS",
      "catalog_number":"768",
      "title":"Quantum Information Processing"
    },
    {
      "course_id":"012670",
      "subject":"CS",
      "catalog_number":"770",
      "title":"Numerical Analysis"
    },
    {
      "course_id":"012994",
      "subject":"CS",
      "catalog_number":"774",
      "title":"Advanced Computational Finance"
    },
    {
      "course_id":"011300",
      "subject":"CS",
      "catalog_number":"775",
      "title":"Parallel Algorithm in Scientific Computing"
    },
    {
      "course_id":"000724",
      "subject":"CS",
      "catalog_number":"778",
      "title":"Numerical Solution of Partial Differential Equations"
    },
    {
      "course_id":"000725",
      "subject":"CS",
      "catalog_number":"779",
      "title":"Splines and Their Use in Computer Graphics"
    },
    {
      "course_id":"011501",
      "subject":"CS",
      "catalog_number":"780",
      "title":"Advanced Symbolic Computation"
    },
    {
      "course_id":"011467",
      "subject":"CS",
      "catalog_number":"781",
      "title":"Colour in Computer Graphics"
    },
    {
      "course_id":"011468",
      "subject":"CS",
      "catalog_number":"782",
      "title":"Pattern Discovery in Biomolecular Data"
    },
    {
      "course_id":"012995",
      "subject":"CS",
      "catalog_number":"783",
      "title":"Computer Modeling of Biophysical Phenomena"
    },
    {
      "course_id":"011288",
      "subject":"CS",
      "catalog_number":"784",
      "title":"Computational Linguistics"
    },
    {
      "course_id":"011289",
      "subject":"CS",
      "catalog_number":"785",
      "title":"Intelligent Computer Interfaces"
    },
    {
      "course_id":"000726",
      "subject":"CS",
      "catalog_number":"786",
      "title":"Probabilistic Inference and Machine Learning"
    },
    {
      "course_id":"000743",
      "subject":"CS",
      "catalog_number":"787",
      "title":"Computational Vision"
    },
    {
      "course_id":"000747",
      "subject":"CS",
      "catalog_number":"788",
      "title":"High-Performance Image Synthesis"
    },
    {
      "course_id":"011290",
      "subject":"CS",
      "catalog_number":"789",
      "title":"User Interface Tools"
    },
    {
      "course_id":"012996",
      "subject":"CS",
      "catalog_number":"791",
      "title":"Non-Photorealistic Rendering"
    },
    {
      "course_id":"013604",
      "subject":"CS",
      "catalog_number":"792",
      "title":"Data Structures and Standards in Health Informatics"
    },
    {
      "course_id":"013605",
      "subject":"CS",
      "catalog_number":"793",
      "title":"Health Informatics  - Applications Domains"
    },
    {
      "course_id":"000753",
      "subject":"CS",
      "catalog_number":"798",
      "title":"Advanced Research Topics"
    },
    {
      "course_id":"011084",
      "subject":"CS",
      "catalog_number":"840",
      "title":"Advanced Topics in Data Structures"
    },
    {
      "course_id":"011085",
      "subject":"CS",
      "catalog_number":"842",
      "title":"Advanced Topics in Language Design and Implementation"
    },
    {
      "course_id":"011086",
      "subject":"CS",
      "catalog_number":"846",
      "title":"Advanced Topics in Software Engineering"
    },
    {
      "course_id":"000781",
      "subject":"ECE",
      "catalog_number":"629",
      "title":"Computer Arithmetic"
    },
    {
      "course_id":"011087",
      "subject":"CS",
      "catalog_number":"848",
      "title":"Advanced Topics in Data Bases"
    },
    {
      "course_id":"011088",
      "subject":"CS",
      "catalog_number":"850",
      "title":"Advanced Topics  in Computer Architecture"
    },
    {
      "course_id":"011089",
      "subject":"CS",
      "catalog_number":"854",
      "title":"Advanced Topics in Computer Systems"
    },
    {
      "course_id":"011090",
      "subject":"CS",
      "catalog_number":"856",
      "title":"Advanced Topics  in Distributed Computing"
    },
    {
      "course_id":"012992",
      "subject":"CS",
      "catalog_number":"858",
      "title":"Advanced Topics in Cryptography, Security and Privacy"
    },
    {
      "course_id":"011091",
      "subject":"CS",
      "catalog_number":"860",
      "title":"Advanced Topics in Algorithms and Complexity"
    },
    {
      "course_id":"013470",
      "subject":"CS",
      "catalog_number":"867",
      "title":"Advanced Topics in Quantum Computing"
    },
    {
      "course_id":"011092",
      "subject":"CS",
      "catalog_number":"869",
      "title":"Advanced Topics in Logic Design"
    },
    {
      "course_id":"011093",
      "subject":"CS",
      "catalog_number":"870",
      "title":"Advanced Topics  in Scientific Computation"
    },
    {
      "course_id":"011304",
      "subject":"CS",
      "catalog_number":"882",
      "title":"Advanced Topics in Bioinformatics"
    },
    {
      "course_id":"011094",
      "subject":"CS",
      "catalog_number":"886",
      "title":"Advanced Topics in Artificial Intelligence"
    },
    {
      "course_id":"011095",
      "subject":"CS",
      "catalog_number":"887",
      "title":"Advanced Topics in Symbolic Computation"
    },
    {
      "course_id":"011096",
      "subject":"CS",
      "catalog_number":"888",
      "title":"Advanced Topics in Computer Graphics"
    },
    {
      "course_id":"000773",
      "subject":"ECE",
      "catalog_number":"616",
      "title":"Principles of Data Communication"
    },
    {
      "course_id":"012993",
      "subject":"CS",
      "catalog_number":"889",
      "title":"Advanced Topics in Human-Computer Interaction"
    },
    {
      "course_id":"011301",
      "subject":"CS",
      "catalog_number":"898",
      "title":"Advanced Special Topics in Computer Science"
    },
    {
      "course_id":"012640",
      "subject":"CT",
      "catalog_number":"601",
      "title":"The Books of Church"
    },
    {
      "course_id":"012641",
      "subject":"CT",
      "catalog_number":"602",
      "title":"The History of Catholicism"
    },
    {
      "course_id":"012642",
      "subject":"CT",
      "catalog_number":"603",
      "title":"Foundations of Theology"
    },
    {
      "course_id":"012643",
      "subject":"CT",
      "catalog_number":"604",
      "title":"Catholic Moral Life and Thought"
    },
    {
      "course_id":"012644",
      "subject":"CT",
      "catalog_number":"605",
      "title":"The Prayer of Church: Spirituality and Liturgy"
    },
    {
      "course_id":"013606",
      "subject":"CT",
      "catalog_number":"606A",
      "title":"Catholic Thought Research Paper or Project - Part I"
    },
    {
      "course_id":"013607",
      "subject":"CT",
      "catalog_number":"606B",
      "title":"Catholic Thought Research Paper or Project - Part II"
    },
    {
      "course_id":"012645",
      "subject":"CT",
      "catalog_number":"610",
      "title":"Catholic Sacramental Life"
    },
    {
      "course_id":"012646",
      "subject":"CT",
      "catalog_number":"611",
      "title":"Catholic Perspectives on Ecology"
    },
    {
      "course_id":"012647",
      "subject":"CT",
      "catalog_number":"612",
      "title":"Special Topics in Catholic Theology"
    },
    {
      "course_id":"012648",
      "subject":"CT",
      "catalog_number":"613",
      "title":"The Catholic Imagination in Art and Literature"
    },
    {
      "course_id":"012649",
      "subject":"CT",
      "catalog_number":"614",
      "title":"Catholicism and Education"
    },
    {
      "course_id":"012650",
      "subject":"CT",
      "catalog_number":"615",
      "title":"Catholic Social Ethics"
    },
    {
      "course_id":"012651",
      "subject":"CT",
      "catalog_number":"616",
      "title":"Gender Ethics in Roman Catholicism"
    },
    {
      "course_id":"012652",
      "subject":"CT",
      "catalog_number":"617",
      "title":"Contemporary Bioethics: Issues of Life and Death"
    },
    {
      "course_id":"012653",
      "subject":"CT",
      "catalog_number":"618",
      "title":"The Catholic Church in Canada"
    },
    {
      "course_id":"011680",
      "subject":"DAC",
      "catalog_number":"201",
      "title":"Designing Digital Images and Hypertext"
    },
    {
      "course_id":"011681",
      "subject":"DAC",
      "catalog_number":"202",
      "title":"Designing Digital Video"
    },
    {
      "course_id":"011682",
      "subject":"DAC",
      "catalog_number":"300",
      "title":"Special Topics in Digital Design"
    },
    {
      "course_id":"013106",
      "subject":"DAC",
      "catalog_number":"301",
      "title":"Designing with Digital Sound"
    },
    {
      "course_id":"014124",
      "subject":"DAC",
      "catalog_number":"302",
      "title":"Machinima as Digital Storytelling"
    },
    {
      "course_id":"013325",
      "subject":"DAC",
      "catalog_number":"305",
      "title":"Design for Interactive Games"
    },
    {
      "course_id":"014125",
      "subject":"DAC",
      "catalog_number":"307",
      "title":"Digital Display Systems"
    },
    {
      "course_id":"014126",
      "subject":"DAC",
      "catalog_number":"308",
      "title":"Cinematic Art and Practice"
    },
    {
      "course_id":"014521",
      "subject":"DAC",
      "catalog_number":"309",
      "title":"User Experience Design"
    },
    {
      "course_id":"012415",
      "subject":"DAC",
      "catalog_number":"329",
      "title":"Digital Presentations"
    },
    {
      "course_id":"012584",
      "subject":"DAC",
      "catalog_number":"403",
      "title":"Special Topics in Speech Communication and Technology"
    },
    {
      "course_id":"014085",
      "subject":"DEI",
      "catalog_number":"612",
      "title":"Working in Teams"
    },
    {
      "course_id":"014086",
      "subject":"DEI",
      "catalog_number":"613",
      "title":"Digital Media Solutions 1: Design Principles and Practice"
    },
    {
      "course_id":"014087",
      "subject":"DEI",
      "catalog_number":"614",
      "title":"Principles of Marketing in a Globalized World: Leveraging Digital Technology"
    },
    {
      "course_id":"014088",
      "subject":"DEI",
      "catalog_number":"615",
      "title":"New Perspectives: Media History and Analysis"
    },
    {
      "course_id":"014089",
      "subject":"DEI",
      "catalog_number":"622",
      "title":"Working in Teams 2"
    },
    {
      "course_id":"014090",
      "subject":"DEI",
      "catalog_number":"623",
      "title":"Digital Media Solutions 2: Project Management"
    },
    {
      "course_id":"014091",
      "subject":"DEI",
      "catalog_number":"624",
      "title":"Understanding the Consumer Universe: Market Research in Digital Media"
    },
    {
      "course_id":"014092",
      "subject":"DEI",
      "catalog_number":"625",
      "title":"Media Innovation and Impact"
    },
    {
      "course_id":"014302",
      "subject":"DEI",
      "catalog_number":"626",
      "title":"User Experience (UX) Fundamentals and User Research (UER)"
    },
    {
      "course_id":"009240",
      "subject":"EARTH",
      "catalog_number":"10",
      "title":"Enhancing Communications Skills for Earth Sciences Students"
    },
    {
      "course_id":"004838",
      "subject":"EARTH",
      "catalog_number":"336",
      "title":"Evolution 2: Fossil Record"
    },
    {
      "course_id":"014093",
      "subject":"DEI",
      "catalog_number":"631",
      "title":"Projects"
    },
    {
      "course_id":"011069",
      "subject":"DM",
      "catalog_number":"700",
      "title":"Numerical Simulation of Sheet Metal Forming"
    },
    {
      "course_id":"011070",
      "subject":"DM",
      "catalog_number":"701",
      "title":"Metal Forming"
    },
    {
      "course_id":"011071",
      "subject":"DM",
      "catalog_number":"702",
      "title":"Surface Machining"
    },
    {
      "course_id":"011072",
      "subject":"DM",
      "catalog_number":"712",
      "title":"Automation and Intelligent Manufacturing"
    },
    {
      "course_id":"011073",
      "subject":"DM",
      "catalog_number":"713",
      "title":"Life Extension"
    },
    {
      "course_id":"011074",
      "subject":"DM",
      "catalog_number":"714",
      "title":"Industrial Noise Analysis and Control"
    },
    {
      "course_id":"011075",
      "subject":"DM",
      "catalog_number":"720",
      "title":"Design: Materials Selection"
    },
    {
      "course_id":"011762",
      "subject":"DM",
      "catalog_number":"722",
      "title":"Mechatronics Engineering"
    },
    {
      "course_id":"012130",
      "subject":"DM",
      "catalog_number":"723",
      "title":"Sensors, Actuators & Interfacing"
    },
    {
      "course_id":"011076",
      "subject":"DM",
      "catalog_number":"730",
      "title":"Welding"
    },
    {
      "course_id":"011077",
      "subject":"DM",
      "catalog_number":"766",
      "title":"Strategic Management of Technology"
    },
    {
      "course_id":"011078",
      "subject":"DM",
      "catalog_number":"782",
      "title":"Integrating Product Development and Manufacturing"
    },
    {
      "course_id":"011079",
      "subject":"DM",
      "catalog_number":"784",
      "title":"Product Development Planning and Execution"
    },
    {
      "course_id":"011269",
      "subject":"DM",
      "catalog_number":"790",
      "title":"Logistics and Supply Chain Management"
    },
    {
      "course_id":"012021",
      "subject":"DM",
      "catalog_number":"791",
      "title":"Management of Quality"
    },
    {
      "course_id":"004660",
      "subject":"DRAMA",
      "catalog_number":"101A",
      "title":"Introduction to the Theatre 1"
    },
    {
      "course_id":"004661",
      "subject":"DRAMA",
      "catalog_number":"101B",
      "title":"Introduction to the Theatre 2"
    },
    {
      "course_id":"004662",
      "subject":"DRAMA",
      "catalog_number":"102",
      "title":"Introduction to Performance"
    },
    {
      "course_id":"004660",
      "subject":"DRAMA",
      "catalog_number":"200",
      "title":"Theatre and Performance in Context"
    },
    {
      "course_id":"012417",
      "subject":"DRAMA",
      "catalog_number":"220",
      "title":"Performance Studies"
    },
    {
      "course_id":"004663",
      "subject":"DRAMA",
      "catalog_number":"221",
      "title":"Performing Text"
    },
    {
      "course_id":"004664",
      "subject":"DRAMA",
      "catalog_number":"222",
      "title":"Performing the Body"
    },
    {
      "course_id":"004668",
      "subject":"DRAMA",
      "catalog_number":"243",
      "title":"Technical Production 1"
    },
    {
      "course_id":"004669",
      "subject":"DRAMA",
      "catalog_number":"244",
      "title":"Technical Production 2"
    },
    {
      "course_id":"004678",
      "subject":"DRAMA",
      "catalog_number":"301",
      "title":"Performance Creation"
    },
    {
      "course_id":"004680",
      "subject":"DRAMA",
      "catalog_number":"306",
      "title":"Production Participation 3"
    },
    {
      "course_id":"004681",
      "subject":"DRAMA",
      "catalog_number":"307",
      "title":"Production Participation 4"
    },
    {
      "course_id":"004682",
      "subject":"DRAMA",
      "catalog_number":"311",
      "title":"English Drama to 1642"
    },
    {
      "course_id":"004684",
      "subject":"DRAMA",
      "catalog_number":"314",
      "title":"Survey of Dramatic Literature and Theory 5"
    },
    {
      "course_id":"004685",
      "subject":"DRAMA",
      "catalog_number":"315",
      "title":"Survey of Dramatic Literature and Theory 6"
    },
    {
      "course_id":"004687",
      "subject":"DRAMA",
      "catalog_number":"318",
      "title":"Musical Theatre and Musical Film"
    },
    {
      "course_id":"010190",
      "subject":"DRAMA",
      "catalog_number":"319B",
      "title":"Tennessee Williams in Performance"
    },
    {
      "course_id":"012203",
      "subject":"DRAMA",
      "catalog_number":"319E",
      "title":"Beckett in Performance"
    },
    {
      "course_id":"004688",
      "subject":"DRAMA",
      "catalog_number":"321",
      "title":"Approaches to Acting with Text"
    },
    {
      "course_id":"004689",
      "subject":"DRAMA",
      "catalog_number":"322",
      "title":"Approaches to Acting with the Body"
    },
    {
      "course_id":"004692",
      "subject":"DRAMA",
      "catalog_number":"326",
      "title":"Performing the Voice"
    },
    {
      "course_id":"004694",
      "subject":"DRAMA",
      "catalog_number":"331",
      "title":"Design Theory and Practice"
    },
    {
      "course_id":"010103",
      "subject":"DRAMA",
      "catalog_number":"333",
      "title":"Costume Design"
    },
    {
      "course_id":"012204",
      "subject":"DRAMA",
      "catalog_number":"335",
      "title":"History of Costume"
    },
    {
      "course_id":"004696",
      "subject":"DRAMA",
      "catalog_number":"341",
      "title":"Lighting Design for the Theatre 1"
    },
    {
      "course_id":"004698",
      "subject":"DRAMA",
      "catalog_number":"343",
      "title":"Stage Management"
    },
    {
      "course_id":"014900",
      "subject":"DRAMA",
      "catalog_number":"366",
      "title":"Writing for Performance"
    },
    {
      "course_id":"005509",
      "subject":"DRAMA",
      "catalog_number":"351",
      "title":"Central and East European Film"
    },
    {
      "course_id":"005516",
      "subject":"DRAMA",
      "catalog_number":"359",
      "title":"Film and Television 1"
    },
    {
      "course_id":"005517",
      "subject":"DRAMA",
      "catalog_number":"360",
      "title":"Film and Television 2"
    },
    {
      "course_id":"004706",
      "subject":"DRAMA",
      "catalog_number":"361",
      "title":"Approaches to Directing"
    },
    {
      "course_id":"004707",
      "subject":"DRAMA",
      "catalog_number":"362",
      "title":"Directing 2"
    },
    {
      "course_id":"010088",
      "subject":"DRAMA",
      "catalog_number":"363",
      "title":"Stage Combat"
    },
    {
      "course_id":"004708",
      "subject":"DRAMA",
      "catalog_number":"371",
      "title":"Theatre History 1"
    },
    {
      "course_id":"004709",
      "subject":"DRAMA",
      "catalog_number":"372",
      "title":"Theatre History 2"
    },
    {
      "course_id":"005148",
      "subject":"DRAMA",
      "catalog_number":"380",
      "title":"Canadian Drama"
    },
    {
      "course_id":"008456",
      "subject":"DRAMA",
      "catalog_number":"381",
      "title":"Russian Drama before 1905"
    },
    {
      "course_id":"008457",
      "subject":"DRAMA",
      "catalog_number":"382",
      "title":"Russian Drama after 1905"
    },
    {
      "course_id":"005166",
      "subject":"DRAMA",
      "catalog_number":"386",
      "title":"Shakespeare 1"
    },
    {
      "course_id":"005167",
      "subject":"DRAMA",
      "catalog_number":"387",
      "title":"Shakespeare 2"
    },
    {
      "course_id":"011401",
      "subject":"DRAMA",
      "catalog_number":"392",
      "title":"American Film"
    },
    {
      "course_id":"011713",
      "subject":"DRAMA",
      "catalog_number":"394",
      "title":"The New Hollywood"
    },
    {
      "course_id":"011908",
      "subject":"DRAMA",
      "catalog_number":"396",
      "title":"Film Noir"
    },
    {
      "course_id":"010177",
      "subject":"DRAMA",
      "catalog_number":"397",
      "title":"Women and Film"
    },
    {
      "course_id":"011181",
      "subject":"DRAMA",
      "catalog_number":"401",
      "title":"Acting Styles"
    },
    {
      "course_id":"011182",
      "subject":"DRAMA",
      "catalog_number":"402",
      "title":"Political Theatre"
    },
    {
      "course_id":"011183",
      "subject":"DRAMA",
      "catalog_number":"403",
      "title":"Theories of the Modern Theatre"
    },
    {
      "course_id":"011184",
      "subject":"DRAMA",
      "catalog_number":"404",
      "title":"Genre"
    },
    {
      "course_id":"011907",
      "subject":"DRAMA",
      "catalog_number":"405",
      "title":"Theatre and the New Media"
    },
    {
      "course_id":"004715",
      "subject":"DRAMA",
      "catalog_number":"406",
      "title":"Production Participation 7"
    },
    {
      "course_id":"004716",
      "subject":"DRAMA",
      "catalog_number":"407",
      "title":"Production Participation 8"
    },
    {
      "course_id":"004717",
      "subject":"DRAMA",
      "catalog_number":"409",
      "title":"Theatre Criticism"
    },
    {
      "course_id":"004721",
      "subject":"DRAMA",
      "catalog_number":"443",
      "title":"Theatre Technology and Management Apprenticeship 1"
    },
    {
      "course_id":"004718",
      "subject":"DRAMA",
      "catalog_number":"421",
      "title":"Advanced Acting Workshop 1"
    },
    {
      "course_id":"004719",
      "subject":"DRAMA",
      "catalog_number":"422",
      "title":"Advanced Acting Workshop 2"
    },
    {
      "course_id":"004720",
      "subject":"DRAMA",
      "catalog_number":"425",
      "title":"Audition Technique and Professional Orientation"
    },
    {
      "course_id":"012960",
      "subject":"DRAMA",
      "catalog_number":"426",
      "title":"Advanced Voice Technique"
    },
    {
      "course_id":"011906",
      "subject":"DRAMA",
      "catalog_number":"440",
      "title":"Performative Inquiry and Practice"
    },
    {
      "course_id":"004723",
      "subject":"DRAMA",
      "catalog_number":"490",
      "title":"Selected Seminars in Drama & Theatre Arts"
    },
    {
      "course_id":"010105",
      "subject":"DRAMA",
      "catalog_number":"491",
      "title":"Selected Seminars in Drama & Theatre Arts"
    },
    {
      "course_id":"004740",
      "subject":"DRAMA",
      "catalog_number":"499A",
      "title":"Senior Seminar"
    },
    {
      "course_id":"004741",
      "subject":"DRAMA",
      "catalog_number":"499B",
      "title":"Senior Seminar"
    },
    {
      "course_id":"004742",
      "subject":"DUTCH",
      "catalog_number":"101",
      "title":"Elementary Dutch I"
    },
    {
      "course_id":"004743",
      "subject":"DUTCH",
      "catalog_number":"102",
      "title":"Elementary Dutch II"
    },
    {
      "course_id":"004744",
      "subject":"DUTCH",
      "catalog_number":"201",
      "title":"Intermediate Dutch I"
    },
    {
      "course_id":"004746",
      "subject":"DUTCH",
      "catalog_number":"202",
      "title":"Intermediate Dutch II"
    },
    {
      "course_id":"004819",
      "subject":"EARTH",
      "catalog_number":"121",
      "title":"Introductory Earth Sciences"
    },
    {
      "course_id":"004820",
      "subject":"EARTH",
      "catalog_number":"121L",
      "title":"Introductory Earth Sciences Laboratory"
    },
    {
      "course_id":"004821",
      "subject":"EARTH",
      "catalog_number":"122",
      "title":"Introductory Environmental Sciences"
    },
    {
      "course_id":"004822",
      "subject":"EARTH",
      "catalog_number":"122L",
      "title":"Introductory Environmental Sciences Laboratory"
    },
    {
      "course_id":"004823",
      "subject":"EARTH",
      "catalog_number":"123",
      "title":"Introductory Hydrology"
    },
    {
      "course_id":"004824",
      "subject":"EARTH",
      "catalog_number":"123L",
      "title":"Field Methods in Hydrology"
    },
    {
      "course_id":"011496",
      "subject":"EARTH",
      "catalog_number":"153",
      "title":"Earth Engineering"
    },
    {
      "course_id":"004826",
      "subject":"EARTH",
      "catalog_number":"221",
      "title":"Geochemistry 1"
    },
    {
      "course_id":"004827",
      "subject":"EARTH",
      "catalog_number":"223",
      "title":"Hydrology"
    },
    {
      "course_id":"004828",
      "subject":"EARTH",
      "catalog_number":"231",
      "title":"Mineralogy"
    },
    {
      "course_id":"004829",
      "subject":"EARTH",
      "catalog_number":"232",
      "title":"Petrography"
    },
    {
      "course_id":"004830",
      "subject":"EARTH",
      "catalog_number":"235",
      "title":"Stratigraphic Approaches to Understanding Earth's History"
    },
    {
      "course_id":"004831",
      "subject":"EARTH",
      "catalog_number":"236",
      "title":"Principles of Paleontology"
    },
    {
      "course_id":"004832",
      "subject":"EARTH",
      "catalog_number":"238",
      "title":"Introductory Structural Geology"
    },
    {
      "course_id":"004833",
      "subject":"EARTH",
      "catalog_number":"260",
      "title":"Applied Geophysics 1"
    },
    {
      "course_id":"012741",
      "subject":"EARTH",
      "catalog_number":"270",
      "title":"Disasters and Natural Hazards"
    },
    {
      "course_id":"011909",
      "subject":"EARTH",
      "catalog_number":"281",
      "title":"Geological Impacts on Human Health"
    },
    {
      "course_id":"013317",
      "subject":"EARTH",
      "catalog_number":"310",
      "title":"Environmental Informatics"
    },
    {
      "course_id":"004835",
      "subject":"EARTH",
      "catalog_number":"331",
      "title":"Volcanology and Igneous Petrology"
    },
    {
      "course_id":"004836",
      "subject":"EARTH",
      "catalog_number":"332",
      "title":"Metamorphic Petrology"
    },
    {
      "course_id":"004837",
      "subject":"EARTH",
      "catalog_number":"333",
      "title":"Introductory Sedimentology"
    },
    {
      "course_id":"004839",
      "subject":"EARTH",
      "catalog_number":"342",
      "title":"Geomorphology and GIS Applications"
    },
    {
      "course_id":"004842",
      "subject":"EARTH",
      "catalog_number":"358",
      "title":"Earth System Science"
    },
    {
      "course_id":"004843",
      "subject":"EARTH",
      "catalog_number":"359",
      "title":"Flow Through Porous Media"
    },
    {
      "course_id":"004848",
      "subject":"EARTH",
      "catalog_number":"390",
      "title":"Methods in Geological Mapping"
    },
    {
      "course_id":"004849",
      "subject":"EARTH",
      "catalog_number":"421",
      "title":"Geochemistry 2"
    },
    {
      "course_id":"004854",
      "subject":"EARTH",
      "catalog_number":"435",
      "title":"Advanced Structural Geology"
    },
    {
      "course_id":"004855",
      "subject":"EARTH",
      "catalog_number":"436A",
      "title":"Honours Thesis"
    },
    {
      "course_id":"004856",
      "subject":"EARTH",
      "catalog_number":"436B",
      "title":"Honours Thesis"
    },
    {
      "course_id":"004857",
      "subject":"EARTH",
      "catalog_number":"437",
      "title":"Rock Mechanics"
    },
    {
      "course_id":"004858",
      "subject":"EARTH",
      "catalog_number":"438",
      "title":"Engineering Geology"
    },
    {
      "course_id":"004860",
      "subject":"EARTH",
      "catalog_number":"440",
      "title":"Quaternary Geology"
    },
    {
      "course_id":"012909",
      "subject":"EARTH",
      "catalog_number":"444",
      "title":"Applied Wetland Science"
    },
    {
      "course_id":"004862",
      "subject":"EARTH",
      "catalog_number":"456",
      "title":"Numerical Methods in Hydrogeology"
    },
    {
      "course_id":"004749",
      "subject":"ECE",
      "catalog_number":"126",
      "title":"Introduction to Electrostatics, Magnetism and Electronics"
    },
    {
      "course_id":"004863",
      "subject":"EARTH",
      "catalog_number":"458",
      "title":"Physical Hydrogeology"
    },
    {
      "course_id":"013108",
      "subject":"EARTH",
      "catalog_number":"458L",
      "title":"Field Methods in Hydrogeology"
    },
    {
      "course_id":"004864",
      "subject":"EARTH",
      "catalog_number":"459",
      "title":"Chemical Hydrogeology"
    },
    {
      "course_id":"004865",
      "subject":"EARTH",
      "catalog_number":"460",
      "title":"Applied Geophysics 2"
    },
    {
      "course_id":"004866",
      "subject":"EARTH",
      "catalog_number":"461",
      "title":"Applied Geophysics 3"
    },
    {
      "course_id":"013109",
      "subject":"EARTH",
      "catalog_number":"461L",
      "title":"Field Methods in Applied Geophysics"
    },
    {
      "course_id":"004868",
      "subject":"EARTH",
      "catalog_number":"471",
      "title":"Mineral Deposits"
    },
    {
      "course_id":"004869",
      "subject":"EARTH",
      "catalog_number":"490",
      "title":"Field Course"
    },
    {
      "course_id":"014141",
      "subject":"EARTH",
      "catalog_number":"491",
      "title":"Special Topics in Earth and Environmental Sciences"
    },
    {
      "course_id":"013756",
      "subject":"EARTH",
      "catalog_number":"499",
      "title":"Research Project"
    },
    {
      "course_id":"000876",
      "subject":"EARTH",
      "catalog_number":"601",
      "title":"Stratigraphic Paleontology"
    },
    {
      "course_id":"000877",
      "subject":"EARTH",
      "catalog_number":"602",
      "title":"Paleontology"
    },
    {
      "course_id":"010449",
      "subject":"EARTH",
      "catalog_number":"603",
      "title":"Micropaleontology"
    },
    {
      "course_id":"000879",
      "subject":"EARTH",
      "catalog_number":"606",
      "title":"Principles of Palynology"
    },
    {
      "course_id":"000880",
      "subject":"EARTH",
      "catalog_number":"610",
      "title":"Sedimentology - Recent Sediments"
    },
    {
      "course_id":"000881",
      "subject":"EARTH",
      "catalog_number":"611",
      "title":"Sedimentology - Ancient Sediments"
    },
    {
      "course_id":"000882",
      "subject":"EARTH",
      "catalog_number":"612",
      "title":"Carbonate Sedimentology"
    },
    {
      "course_id":"000883",
      "subject":"EARTH",
      "catalog_number":"620",
      "title":"Metamorphic Tectonites"
    },
    {
      "course_id":"000884",
      "subject":"EARTH",
      "catalog_number":"621",
      "title":"Aqueous Geochemistry"
    },
    {
      "course_id":"000885",
      "subject":"EARTH",
      "catalog_number":"622",
      "title":"Environmental Isotope Hydrology and Geochemistry"
    },
    {
      "course_id":"000886",
      "subject":"EARTH",
      "catalog_number":"623",
      "title":"Geochemistry of Hydrothermal Ore Deposits"
    },
    {
      "course_id":"000180",
      "subject":"EARTH",
      "catalog_number":"624",
      "title":"Environmental Biogeochemistry"
    },
    {
      "course_id":"000888",
      "subject":"EARTH",
      "catalog_number":"625",
      "title":"Advanced Petrology"
    },
    {
      "course_id":"014365",
      "subject":"EARTH",
      "catalog_number":"626",
      "title":"Global Biogeochemical Cycles"
    },
    {
      "course_id":"000889",
      "subject":"EARTH",
      "catalog_number":"630",
      "title":"Genesis of Metalliferous Ore Deposits"
    },
    {
      "course_id":"000890",
      "subject":"EARTH",
      "catalog_number":"631",
      "title":"Field Methods in Soil and Rock Mechanics"
    },
    {
      "course_id":"010450",
      "subject":"EARTH",
      "catalog_number":"632",
      "title":"Geology of Industrial Minerals"
    },
    {
      "course_id":"000891",
      "subject":"EARTH",
      "catalog_number":"634",
      "title":"Geomechanics of In Situ Processes"
    },
    {
      "course_id":"000892",
      "subject":"EARTH",
      "catalog_number":"635",
      "title":"Clay Mineralogy"
    },
    {
      "course_id":"000893",
      "subject":"EARTH",
      "catalog_number":"638",
      "title":"Advanced Engineering Geology"
    },
    {
      "course_id":"000894",
      "subject":"EARTH",
      "catalog_number":"640",
      "title":"Quaternary Geology of North America"
    },
    {
      "course_id":"000895",
      "subject":"EARTH",
      "catalog_number":"641",
      "title":"Advanced Quaternary Ecology"
    },
    {
      "course_id":"000896",
      "subject":"EARTH",
      "catalog_number":"642",
      "title":"Geoliminology"
    },
    {
      "course_id":"014638",
      "subject":"EARTH",
      "catalog_number":"643",
      "title":"Nutrients in Watersheds"
    },
    {
      "course_id":"000897",
      "subject":"EARTH",
      "catalog_number":"644",
      "title":"Global Problems of Quaternary Geoglogy"
    },
    {
      "course_id":"000898",
      "subject":"EARTH",
      "catalog_number":"645",
      "title":"Geology of the Great Lakes Region"
    },
    {
      "course_id":"012794",
      "subject":"EARTH",
      "catalog_number":"646",
      "title":"Paleolimnology"
    },
    {
      "course_id":"000899",
      "subject":"EARTH",
      "catalog_number":"650",
      "title":"Physical Processes in Groundwater Systems"
    },
    {
      "course_id":"000900",
      "subject":"EARTH",
      "catalog_number":"651",
      "title":"Advanced Groundwater Modelling"
    },
    {
      "course_id":"000901",
      "subject":"EARTH",
      "catalog_number":"653",
      "title":"Contaminant Hydrogeology"
    },
    {
      "course_id":"000902",
      "subject":"EARTH",
      "catalog_number":"654",
      "title":"Groundwater Research Management"
    },
    {
      "course_id":"000903",
      "subject":"EARTH",
      "catalog_number":"656",
      "title":"Groundwater Modelling"
    },
    {
      "course_id":"000904",
      "subject":"EARTH",
      "catalog_number":"657",
      "title":"Organic Contaminants in the Subsurface"
    },
    {
      "course_id":"000905",
      "subject":"EARTH",
      "catalog_number":"658",
      "title":"Flow and Transport in Fractured Rock"
    },
    {
      "course_id":"000906",
      "subject":"EARTH",
      "catalog_number":"659",
      "title":"Chemical Hydrogeology"
    },
    {
      "course_id":"000907",
      "subject":"EARTH",
      "catalog_number":"661",
      "title":"Analytical Methods in Mathematical Geology"
    },
    {
      "course_id":"000908",
      "subject":"EARTH",
      "catalog_number":"668",
      "title":"Advanced Applied Geophysics"
    },
    {
      "course_id":"000909",
      "subject":"EARTH",
      "catalog_number":"671",
      "title":"Field Methods in Hydrogeology"
    },
    {
      "course_id":"000911",
      "subject":"EARTH",
      "catalog_number":"690",
      "title":"Current Problems in Geology"
    },
    {
      "course_id":"000912",
      "subject":"EARTH",
      "catalog_number":"691",
      "title":"Special Studies for MSc Students"
    },
    {
      "course_id":"000918",
      "subject":"EARTH",
      "catalog_number":"692",
      "title":"Special Studies for PhD Students"
    },
    {
      "course_id":"004871",
      "subject":"EASIA",
      "catalog_number":"201R",
      "title":"Introduction to East Asia"
    },
    {
      "course_id":"004872",
      "subject":"EASIA",
      "catalog_number":"205R",
      "title":"Religion in East Asia"
    },
    {
      "course_id":"012997",
      "subject":"EASIA",
      "catalog_number":"206R",
      "title":"Japanese Religions"
    },
    {
      "course_id":"012998",
      "subject":"EASIA",
      "catalog_number":"207R",
      "title":"Chinese Religions"
    },
    {
      "course_id":"010193",
      "subject":"EASIA",
      "catalog_number":"210R",
      "title":"Premodern Chinese Literature"
    },
    {
      "course_id":"011391",
      "subject":"EASIA",
      "catalog_number":"220R",
      "title":"The History of East Asian Communities in Canada"
    },
    {
      "course_id":"012075",
      "subject":"EASIA",
      "catalog_number":"250R",
      "title":"Study Abroad in East Asia"
    },
    {
      "course_id":"014245",
      "subject":"EASIA",
      "catalog_number":"275R",
      "title":"Religion and Japanese Film"
    },
    {
      "course_id":"013313",
      "subject":"EASIA",
      "catalog_number":"277R",
      "title":"International Relations of East Asia"
    },
    {
      "course_id":"012208",
      "subject":"EASIA",
      "catalog_number":"300R",
      "title":"Politics & Diplomacy of Contemporary Japan"
    },
    {
      "course_id":"012707",
      "subject":"EASIA",
      "catalog_number":"301R",
      "title":"The Political Economy of East Asia"
    },
    {
      "course_id":"012999",
      "subject":"EASIA",
      "catalog_number":"330R",
      "title":"Pure Land Buddhism"
    },
    {
      "course_id":"012154",
      "subject":"EASIA",
      "catalog_number":"375R",
      "title":"Special Topics in East Asian Studies"
    },
    {
      "course_id":"013156",
      "subject":"ECE",
      "catalog_number":"100A",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"013157",
      "subject":"ECE",
      "catalog_number":"100B",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"009889",
      "subject":"ECE",
      "catalog_number":"103",
      "title":"Discrete Mathematics"
    },
    {
      "course_id":"013166",
      "subject":"ECE",
      "catalog_number":"105",
      "title":"Physics of Electrical Engineering 1"
    },
    {
      "course_id":"013167",
      "subject":"ECE",
      "catalog_number":"106",
      "title":"Physics of Electrical Engineering 2"
    },
    {
      "course_id":"013168",
      "subject":"ECE",
      "catalog_number":"124",
      "title":"Digital Circuits and Systems"
    },
    {
      "course_id":"013169",
      "subject":"ECE",
      "catalog_number":"140",
      "title":"Linear Circuits"
    },
    {
      "course_id":"004750",
      "subject":"ECE",
      "catalog_number":"150",
      "title":"Fundamentals of Programming"
    },
    {
      "course_id":"013170",
      "subject":"ECE",
      "catalog_number":"155",
      "title":"Engineering Design with Embedded Systems"
    },
    {
      "course_id":"013159",
      "subject":"ECE",
      "catalog_number":"200A",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"013161",
      "subject":"ECE",
      "catalog_number":"200B",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"006891",
      "subject":"ECE",
      "catalog_number":"205",
      "title":"Advanced Calculus 1 for Electrical and Computer Engineers"
    },
    {
      "course_id":"006892",
      "subject":"ECE",
      "catalog_number":"206",
      "title":"Advanced Calculus 2 for Electrical Engineers"
    },
    {
      "course_id":"013171",
      "subject":"ECE",
      "catalog_number":"207",
      "title":"Signals and Systems"
    },
    {
      "course_id":"004754",
      "subject":"ECE",
      "catalog_number":"209",
      "title":"Electronic and Electrical Properties of Materials"
    },
    {
      "course_id":"004755",
      "subject":"ECE",
      "catalog_number":"222",
      "title":"Digital Computers"
    },
    {
      "course_id":"013172",
      "subject":"ECE",
      "catalog_number":"224",
      "title":"Embedded Microprocessor Systems"
    },
    {
      "course_id":"004757",
      "subject":"ECE",
      "catalog_number":"231",
      "title":"Electronic Devices"
    },
    {
      "course_id":"013173",
      "subject":"ECE",
      "catalog_number":"240",
      "title":"Electronic Circuits 1"
    },
    {
      "course_id":"013174",
      "subject":"ECE",
      "catalog_number":"242",
      "title":"Electronic Circuits 2"
    },
    {
      "course_id":"004759",
      "subject":"ECE",
      "catalog_number":"250",
      "title":"Algorithms and Data Structures"
    },
    {
      "course_id":"013175",
      "subject":"ECE",
      "catalog_number":"254",
      "title":"Operating Systems and Systems Programming"
    },
    {
      "course_id":"013176",
      "subject":"ECE",
      "catalog_number":"290",
      "title":"Engineering Profession, Ethics, and Law"
    },
    {
      "course_id":"013162",
      "subject":"ECE",
      "catalog_number":"300A",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"013163",
      "subject":"ECE",
      "catalog_number":"300B",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"004767",
      "subject":"ECE",
      "catalog_number":"309",
      "title":"Introduction to Thermodynamics and Heat Transfer"
    },
    {
      "course_id":"004768",
      "subject":"ECE",
      "catalog_number":"316",
      "title":"Probability Theory and Statistics"
    },
    {
      "course_id":"004769",
      "subject":"ECE",
      "catalog_number":"318",
      "title":"Analog and Digital Communications"
    },
    {
      "course_id":"011044",
      "subject":"ECE",
      "catalog_number":"325",
      "title":"Microprocessor Systems and Interfacing for Mechatronics Engineering"
    },
    {
      "course_id":"004786",
      "subject":"ECE",
      "catalog_number":"327",
      "title":"Digital Hardware Systems"
    },
    {
      "course_id":"013177",
      "subject":"ECE",
      "catalog_number":"331",
      "title":"Electronic Devices"
    },
    {
      "course_id":"013178",
      "subject":"ECE",
      "catalog_number":"351",
      "title":"Compilers"
    },
    {
      "course_id":"004774",
      "subject":"ECE",
      "catalog_number":"354",
      "title":"Real-time Operating Systems"
    },
    {
      "course_id":"013179",
      "subject":"ECE",
      "catalog_number":"356",
      "title":"Database Systems"
    },
    {
      "course_id":"013180",
      "subject":"ECE",
      "catalog_number":"358",
      "title":"Computer Networks"
    },
    {
      "course_id":"004776",
      "subject":"ECE",
      "catalog_number":"362",
      "title":"Modeling and Control of Electric Drives"
    },
    {
      "course_id":"013181",
      "subject":"ECE",
      "catalog_number":"361",
      "title":"Power Systems and Components"
    },
    {
      "course_id":"013187",
      "subject":"ECE",
      "catalog_number":"375",
      "title":"Electromagnetic Fields and Waves"
    },
    {
      "course_id":"004779",
      "subject":"ECE",
      "catalog_number":"380",
      "title":"Analog Control Systems"
    },
    {
      "course_id":"013182",
      "subject":"ECE",
      "catalog_number":"390",
      "title":"Engineering Design, Economics, and Impact on Society"
    },
    {
      "course_id":"013164",
      "subject":"ECE",
      "catalog_number":"400A",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"013165",
      "subject":"ECE",
      "catalog_number":"400B",
      "title":"Electrical and Computer Engineering Practice"
    },
    {
      "course_id":"007444",
      "subject":"ECE",
      "catalog_number":"403",
      "title":"Thermal Physics"
    },
    {
      "course_id":"007422",
      "subject":"ECE",
      "catalog_number":"404",
      "title":"Geometrical and Physical Optics"
    },
    {
      "course_id":"013969",
      "subject":"ECE",
      "catalog_number":"405",
      "title":"Introduction to Quantum Mechanics"
    },
    {
      "course_id":"010053",
      "subject":"ECE",
      "catalog_number":"406",
      "title":"Algorithm Design and Analysis"
    },
    {
      "course_id":"010055",
      "subject":"ECE",
      "catalog_number":"409",
      "title":"Cryptography and System Security"
    },
    {
      "course_id":"004782",
      "subject":"ECE",
      "catalog_number":"411",
      "title":"Digital Communications"
    },
    {
      "course_id":"004784",
      "subject":"ECE",
      "catalog_number":"413",
      "title":"Digital Signal and Image Processing"
    },
    {
      "course_id":"004785",
      "subject":"ECE",
      "catalog_number":"414",
      "title":"Wireless Communications"
    },
    {
      "course_id":"015126",
      "subject":"CHINA",
      "catalog_number":"391R",
      "title":"Special Topics"
    },
    {
      "course_id":"013431",
      "subject":"ECE",
      "catalog_number":"415",
      "title":"Multimedia Processing and Coding"
    },
    {
      "course_id":"013432",
      "subject":"ECE",
      "catalog_number":"416",
      "title":"Advanced Topics in Networking"
    },
    {
      "course_id":"013433",
      "subject":"ECE",
      "catalog_number":"417",
      "title":"Image Processing"
    },
    {
      "course_id":"010125",
      "subject":"ECE",
      "catalog_number":"418",
      "title":"Communications Networks"
    },
    {
      "course_id":"013434",
      "subject":"ECE",
      "catalog_number":"419",
      "title":"Communication System Security"
    },
    {
      "course_id":"013435",
      "subject":"ECE",
      "catalog_number":"423",
      "title":"Embedded Computer Systems"
    },
    {
      "course_id":"004788",
      "subject":"ECE",
      "catalog_number":"429",
      "title":"Computer Architecture"
    },
    {
      "course_id":"013436",
      "subject":"ECE",
      "catalog_number":"432",
      "title":"Radio Frequency Integrated Devices and Circuits"
    },
    {
      "course_id":"013437",
      "subject":"ECE",
      "catalog_number":"433",
      "title":"Fabrication Technologies for Micro and Nano Devices"
    },
    {
      "course_id":"013438",
      "subject":"ECE",
      "catalog_number":"444",
      "title":"Integrated Analog Electronics"
    },
    {
      "course_id":"013439",
      "subject":"ECE",
      "catalog_number":"445",
      "title":"Integrated Digital Electronics"
    },
    {
      "course_id":"004413",
      "subject":"ECE",
      "catalog_number":"451",
      "title":"Software Requirements Specification and Analysis"
    },
    {
      "course_id":"004414",
      "subject":"ECE",
      "catalog_number":"452",
      "title":"Software Design and Architectures"
    },
    {
      "course_id":"004416",
      "subject":"ECE",
      "catalog_number":"453",
      "title":"Software Testing, Quality Assurance and Maintenance"
    },
    {
      "course_id":"004801",
      "subject":"ECE",
      "catalog_number":"454",
      "title":"Distributed Computing"
    },
    {
      "course_id":"004803",
      "subject":"ECE",
      "catalog_number":"456",
      "title":"Database Systems"
    },
    {
      "course_id":"004802",
      "subject":"ECE",
      "catalog_number":"455",
      "title":"Embedded Software"
    },
    {
      "course_id":"013441",
      "subject":"ECE",
      "catalog_number":"457A",
      "title":"Cooperative and Adaptive Algorithms"
    },
    {
      "course_id":"013442",
      "subject":"ECE",
      "catalog_number":"457B",
      "title":"Fundamentals of Computational Intelligence"
    },
    {
      "course_id":"013443",
      "subject":"ECE",
      "catalog_number":"458",
      "title":"Computer Security"
    },
    {
      "course_id":"013471",
      "subject":"ECE",
      "catalog_number":"459",
      "title":"Programming for Performance"
    },
    {
      "course_id":"013445",
      "subject":"ECE",
      "catalog_number":"462",
      "title":"Electrical Distribution Systems"
    },
    {
      "course_id":"004806",
      "subject":"ECE",
      "catalog_number":"463",
      "title":"Design & Applications of Power Electronic Converters"
    },
    {
      "course_id":"004807",
      "subject":"ECE",
      "catalog_number":"464",
      "title":"High Voltage Engineering and Power System Protection"
    },
    {
      "course_id":"012581",
      "subject":"ECE",
      "catalog_number":"467",
      "title":"Power Systems Analysis, Operations and Markets"
    },
    {
      "course_id":"004810",
      "subject":"ECE",
      "catalog_number":"473",
      "title":"Radio Frequency and Microwave Circuits"
    },
    {
      "course_id":"004811",
      "subject":"ECE",
      "catalog_number":"474",
      "title":"Radio and Wireless Systems"
    },
    {
      "course_id":"013188",
      "subject":"ECE",
      "catalog_number":"475",
      "title":"Radio-Wave Systems"
    },
    {
      "course_id":"011045",
      "subject":"ECE",
      "catalog_number":"477",
      "title":"Photonic Devices and Systems"
    },
    {
      "course_id":"004813",
      "subject":"ECE",
      "catalog_number":"481",
      "title":"Digital Control Systems"
    },
    {
      "course_id":"010037",
      "subject":"ECE",
      "catalog_number":"492A",
      "title":"Engineering Design Project"
    },
    {
      "course_id":"011332",
      "subject":"ECE",
      "catalog_number":"484",
      "title":"Digital Control Applications"
    },
    {
      "course_id":"004816",
      "subject":"ECE",
      "catalog_number":"486",
      "title":"Robot Dynamics and Control"
    },
    {
      "course_id":"011333",
      "subject":"ECE",
      "catalog_number":"488",
      "title":"Multivariable Control Systems"
    },
    {
      "course_id":"010059",
      "subject":"ECE",
      "catalog_number":"493",
      "title":"Special Topics in Electrical and Computer Engineering"
    },
    {
      "course_id":"013183",
      "subject":"ECE",
      "catalog_number":"498A",
      "title":"Engineering Design Project"
    },
    {
      "course_id":"013184",
      "subject":"ECE",
      "catalog_number":"498B",
      "title":"Engineering Design Project"
    },
    {
      "course_id":"014714",
      "subject":"ECE",
      "catalog_number":"600",
      "title":"Analytical Methods for Electrical and Computer Engineering"
    },
    {
      "course_id":"010040",
      "subject":"ECE",
      "catalog_number":"499",
      "title":"Engineering Project"
    },
    {
      "course_id":"000764",
      "subject":"ECE",
      "catalog_number":"602",
      "title":"Introduction to Optimization"
    },
    {
      "course_id":"000771",
      "subject":"ECE",
      "catalog_number":"613",
      "title":"Digital Speech Processing"
    },
    {
      "course_id":"000765",
      "subject":"ECE",
      "catalog_number":"603",
      "title":"Statistical Signal Processing"
    },
    {
      "course_id":"000766",
      "subject":"ECE",
      "catalog_number":"604",
      "title":"Stochastic Processes"
    },
    {
      "course_id":"000767",
      "subject":"ECE",
      "catalog_number":"605",
      "title":"Queueing Systems"
    },
    {
      "course_id":"013906",
      "subject":"ECE",
      "catalog_number":"606",
      "title":"Algorithm Design and Analysis"
    },
    {
      "course_id":"014294",
      "subject":"ECE",
      "catalog_number":"607",
      "title":"Algebraic Fundamentals for Computation, Communication and Control"
    },
    {
      "course_id":"000768",
      "subject":"ECE",
      "catalog_number":"610",
      "title":"Broadband  Communication Networks"
    },
    {
      "course_id":"000769",
      "subject":"ECE",
      "catalog_number":"611",
      "title":"Digital Communications"
    },
    {
      "course_id":"000770",
      "subject":"ECE",
      "catalog_number":"612",
      "title":"Information Theory"
    },
    {
      "course_id":"000772",
      "subject":"ECE",
      "catalog_number":"614",
      "title":"Communications Over Fading Dispersive Channels"
    },
    {
      "course_id":"000774",
      "subject":"ECE",
      "catalog_number":"617",
      "title":"Data Compression with Applications to Speech and Image Coding"
    },
    {
      "course_id":"000777",
      "subject":"ECE",
      "catalog_number":"621",
      "title":"Computer Organization"
    },
    {
      "course_id":"014410",
      "subject":"ECE",
      "catalog_number":"627",
      "title":"Register-transfer-level Digital Systems"
    },
    {
      "course_id":"000780",
      "subject":"ECE",
      "catalog_number":"628",
      "title":"Computer Network Security"
    },
    {
      "course_id":"014299",
      "subject":"ECE",
      "catalog_number":"630",
      "title":"Physics and Models of Semiconductor Devices"
    },
    {
      "course_id":"000783",
      "subject":"ECE",
      "catalog_number":"631",
      "title":"Microelectronic Processing Technology"
    },
    {
      "course_id":"000784",
      "subject":"ECE",
      "catalog_number":"632",
      "title":"Photovoltaic Energy Conversion"
    },
    {
      "course_id":"000788",
      "subject":"ECE",
      "catalog_number":"636",
      "title":"Advanced Analog Integrated Circuits"
    },
    {
      "course_id":"000789",
      "subject":"ECE",
      "catalog_number":"637",
      "title":"Digital Integrated Circuits"
    },
    {
      "course_id":"010649",
      "subject":"ECE",
      "catalog_number":"638",
      "title":"Semiconductor Microtransducers"
    },
    {
      "course_id":"010650",
      "subject":"ECE",
      "catalog_number":"639",
      "title":"Characteristics & Applications of Amorphous Silicon"
    },
    {
      "course_id":"000790",
      "subject":"ECE",
      "catalog_number":"644",
      "title":"Computer Aided Circuit Analysis and Design"
    },
    {
      "course_id":"000792",
      "subject":"ECE",
      "catalog_number":"647",
      "title":"Algorithms for Physical Design of Digital Integrated Circuits"
    },
    {
      "course_id":"000813",
      "subject":"ECE",
      "catalog_number":"685",
      "title":"Stochastic Processes for Dynamical Systems"
    },
    {
      "course_id":"000794",
      "subject":"ECE",
      "catalog_number":"651",
      "title":"Foundations of Software Engineering"
    },
    {
      "course_id":"000795",
      "subject":"ECE",
      "catalog_number":"652",
      "title":"Parallel Programming"
    },
    {
      "course_id":"000796",
      "subject":"ECE",
      "catalog_number":"653",
      "title":"Software Testing, Quality Assurance and Maintenance"
    },
    {
      "course_id":"014295",
      "subject":"ECE",
      "catalog_number":"654",
      "title":"Software Reliability Engineering"
    },
    {
      "course_id":"014296",
      "subject":"ECE",
      "catalog_number":"655",
      "title":"Protocols, Software and Issues in Mobile Systems"
    },
    {
      "course_id":"014297",
      "subject":"ECE",
      "catalog_number":"656",
      "title":"Database Systems"
    },
    {
      "course_id":"014298",
      "subject":"ECE",
      "catalog_number":"657",
      "title":"Tools of Intelligent Systems Design"
    },
    {
      "course_id":"014300",
      "subject":"ECE",
      "catalog_number":"658",
      "title":"Component Based Software"
    },
    {
      "course_id":"000797",
      "subject":"ECE",
      "catalog_number":"661",
      "title":"HVDC and FACTS"
    },
    {
      "course_id":"000798",
      "subject":"ECE",
      "catalog_number":"662",
      "title":"Power Systems Analysis and Control"
    },
    {
      "course_id":"000808",
      "subject":"ECE",
      "catalog_number":"674",
      "title":"Analysis and Computation of Electric and Magnetic Fields"
    },
    {
      "course_id":"000799",
      "subject":"ECE",
      "catalog_number":"663",
      "title":"Energy Processing"
    },
    {
      "course_id":"000800",
      "subject":"ECE",
      "catalog_number":"664",
      "title":"Power System Components and Modeling"
    },
    {
      "course_id":"010651",
      "subject":"ECE",
      "catalog_number":"665",
      "title":"High Voltage Engineering Applications"
    },
    {
      "course_id":"000801",
      "subject":"ECE",
      "catalog_number":"666",
      "title":"Power Systems Operation"
    },
    {
      "course_id":"000802",
      "subject":"ECE",
      "catalog_number":"667",
      "title":"Sustainable Distributed Power Generation"
    },
    {
      "course_id":"000803",
      "subject":"ECE",
      "catalog_number":"668",
      "title":"Distribution System Engineering"
    },
    {
      "course_id":"000804",
      "subject":"ECE",
      "catalog_number":"669",
      "title":"Dielectric Materials"
    },
    {
      "course_id":"000805",
      "subject":"ECE",
      "catalog_number":"671",
      "title":"Microwave and RF Engineering"
    },
    {
      "course_id":"000806",
      "subject":"ECE",
      "catalog_number":"672",
      "title":"Optoelectronic Devices"
    },
    {
      "course_id":"000809",
      "subject":"ECE",
      "catalog_number":"675",
      "title":"Radiation & Propagation of Electromagnetic Fields"
    },
    {
      "course_id":"000810",
      "subject":"ECE",
      "catalog_number":"678",
      "title":"Fourier Optics and Optical Signal Processing"
    },
    {
      "course_id":"000811",
      "subject":"ECE",
      "catalog_number":"682",
      "title":"Multivariable Control Systems"
    },
    {
      "course_id":"000812",
      "subject":"ECE",
      "catalog_number":"683",
      "title":"System Identification"
    },
    {
      "course_id":"000814",
      "subject":"ECE",
      "catalog_number":"686",
      "title":"Filtering and Control of Stochastic Linear Systems"
    },
    {
      "course_id":"004816",
      "subject":"ECE",
      "catalog_number":"687",
      "title":"Robot Dynamics and Control"
    },
    {
      "course_id":"000815",
      "subject":"ECE",
      "catalog_number":"688",
      "title":"Nonlinear Systems"
    },
    {
      "course_id":"010652",
      "subject":"ECE",
      "catalog_number":"700",
      "title":"Special Topics in Electrical and Computer Engineering"
    },
    {
      "course_id":"010653",
      "subject":"ECE",
      "catalog_number":"710",
      "title":"Special Topics in Communications and Information Theory"
    },
    {
      "course_id":"011246",
      "subject":"ECE",
      "catalog_number":"711",
      "title":"Special Topics in Digital Communications"
    },
    {
      "course_id":"010654",
      "subject":"ECE",
      "catalog_number":"720",
      "title":"Special Topics in Computers and Digital Systems Software"
    },
    {
      "course_id":"011295",
      "subject":"ECE",
      "catalog_number":"725",
      "title":"Computer-Aided Verification"
    },
    {
      "course_id":"000827",
      "subject":"ECE",
      "catalog_number":"730",
      "title":"Special Topics in Solid State Devices"
    },
    {
      "course_id":"000829",
      "subject":"ECE",
      "catalog_number":"732",
      "title":"Simulation of Semiconductor Microtransducers"
    },
    {
      "course_id":"000828",
      "subject":"ECE",
      "catalog_number":"731",
      "title":"CCD Image Sensors"
    },
    {
      "course_id":"000836",
      "subject":"ECE",
      "catalog_number":"738",
      "title":"Low Power VLSI Circuits for Wireless Communication"
    },
    {
      "course_id":"000839",
      "subject":"ECE",
      "catalog_number":"740",
      "title":"Special Topics in Electronic Circuits"
    },
    {
      "course_id":"010300",
      "subject":"ECE",
      "catalog_number":"741",
      "title":"AHDL Modeling of Circuits and Systems"
    },
    {
      "course_id":"010655",
      "subject":"ECE",
      "catalog_number":"750",
      "title":"Special Topics in Computer Software"
    },
    {
      "course_id":"000844",
      "subject":"ECE",
      "catalog_number":"752",
      "title":"Software Architecture & Design"
    },
    {
      "course_id":"000845",
      "subject":"ECE",
      "catalog_number":"753",
      "title":"Parallel and Distributed Systems"
    },
    {
      "course_id":"014597",
      "subject":"ECE",
      "catalog_number":"754",
      "title":"Software Bug Detection and Tolerance"
    },
    {
      "course_id":"014598",
      "subject":"ECE",
      "catalog_number":"755",
      "title":"Safety-critical Real-time Embedded Software"
    },
    {
      "course_id":"000851",
      "subject":"ECE",
      "catalog_number":"761",
      "title":"Applied Nonlinear Systems Theory"
    },
    {
      "course_id":"010656",
      "subject":"ECE",
      "catalog_number":"760",
      "title":"Special Topics in Power Systems and High Voltage Engineering"
    },
    {
      "course_id":"013907",
      "subject":"ECE",
      "catalog_number":"768",
      "title":"Power System Quality"
    },
    {
      "course_id":"000856",
      "subject":"ECE",
      "catalog_number":"770",
      "title":"Special Topics in Antenna and Microwave Theory"
    },
    {
      "course_id":"013664",
      "subject":"ECON",
      "catalog_number":"622A",
      "title":"Applied Microeconometrics"
    },
    {
      "course_id":"010657",
      "subject":"ECE",
      "catalog_number":"780",
      "title":"Special Topics in Control"
    },
    {
      "course_id":"000865",
      "subject":"ECE",
      "catalog_number":"781",
      "title":"Adaptive Control"
    },
    {
      "course_id":"000868",
      "subject":"ECE",
      "catalog_number":"784",
      "title":"Introduction to Stochastic Calculus"
    },
    {
      "course_id":"012050",
      "subject":"ECE",
      "catalog_number":"6601PD",
      "title":"Power System Components and Modeling"
    },
    {
      "course_id":"012051",
      "subject":"ECE",
      "catalog_number":"6602PD",
      "title":"Power System Management & Electricity Markets"
    },
    {
      "course_id":"012052",
      "subject":"ECE",
      "catalog_number":"6603PD",
      "title":"Electromagnetic Compatibility and Power Quality"
    },
    {
      "course_id":"012053",
      "subject":"ECE",
      "catalog_number":"6604PD",
      "title":"Distributed Generation"
    },
    {
      "course_id":"012054",
      "subject":"ECE",
      "catalog_number":"6605PD",
      "title":"Power System Protection"
    },
    {
      "course_id":"012055",
      "subject":"ECE",
      "catalog_number":"6606PD",
      "title":"Distribution System Engineering"
    },
    {
      "course_id":"012056",
      "subject":"ECE",
      "catalog_number":"6607PD",
      "title":"Operation and Control of Resturctured Power Systems"
    },
    {
      "course_id":"012057",
      "subject":"ECE",
      "catalog_number":"6608PD",
      "title":"Dielectrics and Electrical Insulation"
    },
    {
      "course_id":"012058",
      "subject":"ECE",
      "catalog_number":"6609PD",
      "title":"High Voltage Engineering Applications"
    },
    {
      "course_id":"012059",
      "subject":"ECE",
      "catalog_number":"6610PD",
      "title":"Power Electronic Converters"
    },
    {
      "course_id":"012060",
      "subject":"ECE",
      "catalog_number":"6611PD",
      "title":"Electric Machines and Motor Drives"
    },
    {
      "course_id":"012061",
      "subject":"ECE",
      "catalog_number":"6612PD",
      "title":"FACTS: Models, Controls and Applications"
    },
    {
      "course_id":"013345",
      "subject":"ECE",
      "catalog_number":"6613PD",
      "title":"Power System Analysis"
    },
    {
      "course_id":"013346",
      "subject":"ECE",
      "catalog_number":"6614PD",
      "title":"Industrial Utilization of Electrical Energy"
    },
    {
      "course_id":"013347",
      "subject":"ECE",
      "catalog_number":"6615PD",
      "title":"Design and application of DC\/DC Converters"
    },
    {
      "course_id":"013348",
      "subject":"ECE",
      "catalog_number":"6616PD",
      "title":"Electric Safety and Grounding System Design"
    },
    {
      "course_id":"013349",
      "subject":"ECE",
      "catalog_number":"6617PD",
      "title":"Asset Management and Risk Assessment of Power Systems"
    },
    {
      "course_id":"013350",
      "subject":"ECE",
      "catalog_number":"6618PD",
      "title":"Medium and High Voltage Power Cables"
    },
    {
      "course_id":"004874",
      "subject":"ECON",
      "catalog_number":"101",
      "title":"Introduction to Microeconomics"
    },
    {
      "course_id":"004877",
      "subject":"ECON",
      "catalog_number":"102",
      "title":"Introduction to Macroeconomics"
    },
    {
      "course_id":"004885",
      "subject":"ECON",
      "catalog_number":"201",
      "title":"Microeconomic Theory 1"
    },
    {
      "course_id":"004886",
      "subject":"ECON",
      "catalog_number":"202",
      "title":"Macroeconomic Theory 1"
    },
    {
      "course_id":"004890",
      "subject":"ECON",
      "catalog_number":"211",
      "title":"Introduction to Mathematical Economics"
    },
    {
      "course_id":"004894",
      "subject":"ECON",
      "catalog_number":"220",
      "title":"The Principles of Entrepreneurship"
    },
    {
      "course_id":"004895",
      "subject":"ECON",
      "catalog_number":"221",
      "title":"Statistics for Economists"
    },
    {
      "course_id":"004899",
      "subject":"ECON",
      "catalog_number":"231",
      "title":"Introduction to International Economics"
    },
    {
      "course_id":"014129",
      "subject":"ECON",
      "catalog_number":"254",
      "title":"Economics of Sport"
    },
    {
      "course_id":"004911",
      "subject":"ECON",
      "catalog_number":"301",
      "title":"Microeconomic Theory 2"
    },
    {
      "course_id":"004913",
      "subject":"ECON",
      "catalog_number":"302",
      "title":"Macroeconomic Theory 2"
    },
    {
      "course_id":"004917",
      "subject":"ECON",
      "catalog_number":"304",
      "title":"Monetary Economics"
    },
    {
      "course_id":"004921",
      "subject":"ECON",
      "catalog_number":"311",
      "title":"Mathematical Economics"
    },
    {
      "course_id":"004923",
      "subject":"ECON",
      "catalog_number":"321",
      "title":"Introduction to Econometrics"
    },
    {
      "course_id":"004927",
      "subject":"ECON",
      "catalog_number":"332",
      "title":"International Finance"
    },
    {
      "course_id":"004932",
      "subject":"ECON",
      "catalog_number":"341",
      "title":"Public Economics: Expenditure"
    },
    {
      "course_id":"015191",
      "subject":"ECON",
      "catalog_number":"345",
      "title":"Marketing 2"
    },
    {
      "course_id":"004934",
      "subject":"ECON",
      "catalog_number":"342",
      "title":"Public Economics: Taxation"
    },
    {
      "course_id":"004936",
      "subject":"ECON",
      "catalog_number":"344",
      "title":"Marketing: Principles of Marketing and Consumer Economics"
    },
    {
      "course_id":"004939",
      "subject":"ECON",
      "catalog_number":"351",
      "title":"Labour Economics"
    },
    {
      "course_id":"004941",
      "subject":"ECON",
      "catalog_number":"355",
      "title":"Economics of Energy and Natural Resources"
    },
    {
      "course_id":"004942",
      "subject":"ECON",
      "catalog_number":"357",
      "title":"Environmental Economics"
    },
    {
      "course_id":"004943",
      "subject":"ECON",
      "catalog_number":"361",
      "title":"Cost-Benefit Analysis and Project Evaluation"
    },
    {
      "course_id":"004944",
      "subject":"ECON",
      "catalog_number":"363",
      "title":"Contemporary Canadian Problems"
    },
    {
      "course_id":"004945",
      "subject":"ECON",
      "catalog_number":"365",
      "title":"Economic Development of Modern Europe"
    },
    {
      "course_id":"004946",
      "subject":"ECON",
      "catalog_number":"371",
      "title":"Business Finance 1"
    },
    {
      "course_id":"004950",
      "subject":"ECON",
      "catalog_number":"383",
      "title":"Special Topics"
    },
    {
      "course_id":"004947",
      "subject":"ECON",
      "catalog_number":"372",
      "title":"Business Finance 2"
    },
    {
      "course_id":"009938",
      "subject":"ECON",
      "catalog_number":"381",
      "title":"Special Topics"
    },
    {
      "course_id":"004949",
      "subject":"ECON",
      "catalog_number":"382",
      "title":"Special Topics"
    },
    {
      "course_id":"004952",
      "subject":"ECON",
      "catalog_number":"401",
      "title":"Microeconomic Theory 3"
    },
    {
      "course_id":"004953",
      "subject":"ECON",
      "catalog_number":"402",
      "title":"Macroeconomic Theory 3"
    },
    {
      "course_id":"004954",
      "subject":"ECON",
      "catalog_number":"403",
      "title":"Topics in Economic Forecasting"
    },
    {
      "course_id":"004955",
      "subject":"ECON",
      "catalog_number":"404",
      "title":"Topics in Money and Finance"
    },
    {
      "course_id":"013754",
      "subject":"ECON",
      "catalog_number":"405",
      "title":"Topics in Financial Econometrics"
    },
    {
      "course_id":"004957",
      "subject":"ECON",
      "catalog_number":"410",
      "title":"Economic Thought"
    },
    {
      "course_id":"004958",
      "subject":"ECON",
      "catalog_number":"411",
      "title":"Advanced Mathematical Economics"
    },
    {
      "course_id":"004959",
      "subject":"ECON",
      "catalog_number":"421",
      "title":"Econometrics"
    },
    {
      "course_id":"004960",
      "subject":"ECON",
      "catalog_number":"422",
      "title":"Topics in Econometrics"
    },
    {
      "course_id":"011778",
      "subject":"ECON",
      "catalog_number":"436",
      "title":"International Trade"
    },
    {
      "course_id":"012408",
      "subject":"ECON",
      "catalog_number":"442",
      "title":"Economics of Taxation"
    },
    {
      "course_id":"009948",
      "subject":"ECON",
      "catalog_number":"445",
      "title":"Industrial Organization and Public Policy"
    },
    {
      "course_id":"013562",
      "subject":"ECON",
      "catalog_number":"451",
      "title":"Law and Economics"
    },
    {
      "course_id":"013884",
      "subject":"ECON",
      "catalog_number":"452",
      "title":"Topics in Labour Economics"
    },
    {
      "course_id":"012409",
      "subject":"ECON",
      "catalog_number":"456",
      "title":"Health Economics"
    },
    {
      "course_id":"012982",
      "subject":"ECON",
      "catalog_number":"465",
      "title":"Economics in History: Topics in European History 476-1800 AD"
    },
    {
      "course_id":"009949",
      "subject":"ECON",
      "catalog_number":"471",
      "title":"Computational Economics"
    },
    {
      "course_id":"004970",
      "subject":"ECON",
      "catalog_number":"472",
      "title":"Senior Honours Essay"
    },
    {
      "course_id":"009950",
      "subject":"ECON",
      "catalog_number":"483",
      "title":"Special Topics"
    },
    {
      "course_id":"009951",
      "subject":"ECON",
      "catalog_number":"484",
      "title":"Special Topics"
    },
    {
      "course_id":"009953",
      "subject":"ECON",
      "catalog_number":"487",
      "title":"Special Studies"
    },
    {
      "course_id":"004974",
      "subject":"ECON",
      "catalog_number":"488",
      "title":"Special Studies"
    },
    {
      "course_id":"004975",
      "subject":"ECON",
      "catalog_number":"489",
      "title":"Special Studies"
    },
    {
      "course_id":"000925",
      "subject":"ECON",
      "catalog_number":"601",
      "title":"Microeconomic Theory I"
    },
    {
      "course_id":"000926",
      "subject":"ECON",
      "catalog_number":"602",
      "title":"Macroeconomic Theory I"
    },
    {
      "course_id":"000928",
      "subject":"ECON",
      "catalog_number":"604",
      "title":"Monetary Theory and Banking"
    },
    {
      "course_id":"000929",
      "subject":"ECON",
      "catalog_number":"605",
      "title":"Computational  Economics"
    },
    {
      "course_id":"000930",
      "subject":"ECON",
      "catalog_number":"606",
      "title":"Research Methodology"
    },
    {
      "course_id":"000933",
      "subject":"ECON",
      "catalog_number":"621",
      "title":"Econometrics I"
    },
    {
      "course_id":"013664",
      "subject":"ECON",
      "catalog_number":"622",
      "title":"Applied Microeconometrics I"
    },
    {
      "course_id":"013665",
      "subject":"ECON",
      "catalog_number":"623",
      "title":"Applied Macroeconometrics I"
    },
    {
      "course_id":"011824",
      "subject":"ECON",
      "catalog_number":"624",
      "title":"Dynamic Optimization with Applications"
    },
    {
      "course_id":"000935",
      "subject":"ECON",
      "catalog_number":"631",
      "title":"International Trade"
    },
    {
      "course_id":"010498",
      "subject":"ECON",
      "catalog_number":"635",
      "title":"International Trade & Development"
    },
    {
      "course_id":"012850",
      "subject":"ECON",
      "catalog_number":"637",
      "title":"Economic Analysis and Global Governance"
    },
    {
      "course_id":"000938",
      "subject":"ECON",
      "catalog_number":"641",
      "title":"Public Economics: Expenditure"
    },
    {
      "course_id":"011825",
      "subject":"ECON",
      "catalog_number":"642",
      "title":"Public Economics: Taxation"
    },
    {
      "course_id":"011126",
      "subject":"ECON",
      "catalog_number":"643",
      "title":"Health Economics"
    },
    {
      "course_id":"000939",
      "subject":"ECON",
      "catalog_number":"645",
      "title":"Industrial Organization I"
    },
    {
      "course_id":"012016",
      "subject":"ECON",
      "catalog_number":"648",
      "title":"Industrial Organization II"
    },
    {
      "course_id":"010499",
      "subject":"ECON",
      "catalog_number":"651",
      "title":"Labour Economics"
    },
    {
      "course_id":"000941",
      "subject":"ECON",
      "catalog_number":"655",
      "title":"Resource Economics"
    },
    {
      "course_id":"011828",
      "subject":"ECON",
      "catalog_number":"657",
      "title":"Environmental Economics"
    },
    {
      "course_id":"012333",
      "subject":"ECON",
      "catalog_number":"659",
      "title":"Real Options and Investment under Uncertainty"
    },
    {
      "course_id":"000945",
      "subject":"ECON",
      "catalog_number":"672",
      "title":"Financial Economics"
    },
    {
      "course_id":"000946",
      "subject":"ECON",
      "catalog_number":"673",
      "title":"Special Topics in Economics"
    },
    {
      "course_id":"013553",
      "subject":"ENBUS",
      "catalog_number":"631",
      "title":"Stakeholder Engagement"
    },
    {
      "course_id":"011829",
      "subject":"ECON",
      "catalog_number":"701",
      "title":"Micro II"
    },
    {
      "course_id":"011830",
      "subject":"ECON",
      "catalog_number":"702",
      "title":"Macro II"
    },
    {
      "course_id":"014729",
      "subject":"ECON",
      "catalog_number":"704",
      "title":"Monetary Economics 2"
    },
    {
      "course_id":"000957",
      "subject":"ECON",
      "catalog_number":"721",
      "title":"Econometrics II"
    },
    {
      "course_id":"012334",
      "subject":"ECON",
      "catalog_number":"722",
      "title":"Applied Microeconometrics II"
    },
    {
      "course_id":"012335",
      "subject":"ECON",
      "catalog_number":"723",
      "title":"Applied Macroeconometrics II"
    },
    {
      "course_id":"012849",
      "subject":"ECON",
      "catalog_number":"727",
      "title":"Financial Econometrics"
    },
    {
      "course_id":"012337",
      "subject":"ECON",
      "catalog_number":"743",
      "title":"Topics in Health Economics"
    },
    {
      "course_id":"012336",
      "subject":"ECON",
      "catalog_number":"773",
      "title":"Special Topic in Economics"
    },
    {
      "course_id":"014667",
      "subject":"EFAS",
      "catalog_number":"32",
      "title":"Academic Skills"
    },
    {
      "course_id":"014668",
      "subject":"EFAS",
      "catalog_number":"34",
      "title":"Writing Skills"
    },
    {
      "course_id":"014669",
      "subject":"EFAS",
      "catalog_number":"36",
      "title":"Oral Skills"
    },
    {
      "course_id":"013850",
      "subject":"EFAS",
      "catalog_number":"42",
      "title":"Academic Skills"
    },
    {
      "course_id":"013851",
      "subject":"EFAS",
      "catalog_number":"44",
      "title":"Writing Skills"
    },
    {
      "course_id":"013852",
      "subject":"EFAS",
      "catalog_number":"46",
      "title":"Oral Skills"
    },
    {
      "course_id":"010089",
      "subject":"ENBUS",
      "catalog_number":"102",
      "title":"Introduction to Environment and Business"
    },
    {
      "course_id":"005265",
      "subject":"ENBUS",
      "catalog_number":"202",
      "title":"Environmental Management Systems"
    },
    {
      "course_id":"012894",
      "subject":"ENBUS",
      "catalog_number":"203",
      "title":"Green Entrepreneurship"
    },
    {
      "course_id":"012895",
      "subject":"ENBUS",
      "catalog_number":"204",
      "title":"Principles of Industrial Ecology"
    },
    {
      "course_id":"010090",
      "subject":"ENBUS",
      "catalog_number":"302",
      "title":"Strategies for Environment and Business"
    },
    {
      "course_id":"012896",
      "subject":"ENBUS",
      "catalog_number":"306",
      "title":"Research Design"
    },
    {
      "course_id":"012897",
      "subject":"ENBUS",
      "catalog_number":"307",
      "title":"Industrial Ecology: Life Cycle Assessment and Management in Business"
    },
    {
      "course_id":"012898",
      "subject":"ENBUS",
      "catalog_number":"308",
      "title":"Sustainability Management Standards and Auditing"
    },
    {
      "course_id":"014976",
      "subject":"ENBUS",
      "catalog_number":"309",
      "title":"Applied Social Marketing"
    },
    {
      "course_id":"012900",
      "subject":"ENBUS",
      "catalog_number":"310",
      "title":"Strategic Management for Sustainable Business"
    },
    {
      "course_id":"012901",
      "subject":"ENBUS",
      "catalog_number":"311",
      "title":"Green Marketing"
    },
    {
      "course_id":"012902",
      "subject":"ENBUS",
      "catalog_number":"312",
      "title":"Operationalizing Sustainable Development within Business"
    },
    {
      "course_id":"010154",
      "subject":"ENBUS",
      "catalog_number":"402A",
      "title":"Environment and Business Project"
    },
    {
      "course_id":"010155",
      "subject":"ENBUS",
      "catalog_number":"402B",
      "title":"Environment and Business Project"
    },
    {
      "course_id":"012903",
      "subject":"ENBUS",
      "catalog_number":"407",
      "title":"Corporate Sustainability Accounting and Reporting"
    },
    {
      "course_id":"012904",
      "subject":"ENBUS",
      "catalog_number":"408",
      "title":"Best Practices in Regulations"
    },
    {
      "course_id":"012905",
      "subject":"ENBUS",
      "catalog_number":"409",
      "title":"Special Topics in Environment and Business"
    },
    {
      "course_id":"012906",
      "subject":"ENBUS",
      "catalog_number":"410",
      "title":"Engaging Stakeholders"
    },
    {
      "course_id":"012907",
      "subject":"ENBUS",
      "catalog_number":"411",
      "title":"International Corporate Responsibility"
    },
    {
      "course_id":"013545",
      "subject":"ENBUS",
      "catalog_number":"601",
      "title":"Business and the Case for Sustainability"
    },
    {
      "course_id":"013546",
      "subject":"ENBUS",
      "catalog_number":"602",
      "title":"Introduction to Sustainability for Business"
    },
    {
      "course_id":"013547",
      "subject":"ENBUS",
      "catalog_number":"620",
      "title":"Business Operations and Sustainability"
    },
    {
      "course_id":"013551",
      "subject":"ENBUS",
      "catalog_number":"621",
      "title":"Enterprise Carbon Management"
    },
    {
      "course_id":"013552",
      "subject":"ENBUS",
      "catalog_number":"622",
      "title":"Product Life Cycle Assessment and Management"
    },
    {
      "course_id":"013548",
      "subject":"ENBUS",
      "catalog_number":"630",
      "title":"Enterprise Marketing and Social Accountability"
    },
    {
      "course_id":"013554",
      "subject":"ENBUS",
      "catalog_number":"632",
      "title":"Sustainability Reporting"
    },
    {
      "course_id":"013549",
      "subject":"ENBUS",
      "catalog_number":"640",
      "title":"Strategies for Sustainable Enterprises"
    },
    {
      "course_id":"013556",
      "subject":"ENBUS",
      "catalog_number":"642",
      "title":"Stakeholder Engagement, Collaborations and Partnerships"
    },
    {
      "course_id":"013550",
      "subject":"ENBUS",
      "catalog_number":"690",
      "title":"Enterprise Sustainability Project"
    },
    {
      "course_id":"013666",
      "subject":"ENBUS",
      "catalog_number":"650",
      "title":"Environmental Finance"
    },
    {
      "course_id":"014599",
      "subject":"ENBUS",
      "catalog_number":"690A",
      "title":"Enterprise Sustainability Project"
    },
    {
      "course_id":"014600",
      "subject":"ENBUS",
      "catalog_number":"690B",
      "title":"Enterprise Sustainability Project"
    },
    {
      "course_id":"014496",
      "subject":"ENGL",
      "catalog_number":"51",
      "title":"Pre-University English: Essentials of Composition"
    },
    {
      "course_id":"013477",
      "subject":"ENGL",
      "catalog_number":"100A",
      "title":"Fiction"
    },
    {
      "course_id":"013478",
      "subject":"ENGL",
      "catalog_number":"100B",
      "title":"Poetry"
    },
    {
      "course_id":"013479",
      "subject":"ENGL",
      "catalog_number":"100C",
      "title":"Drama"
    },
    {
      "course_id":"011580",
      "subject":"ENGL",
      "catalog_number":"101A",
      "title":"Introduction to Literary Studies"
    },
    {
      "course_id":"011581",
      "subject":"ENGL",
      "catalog_number":"101B",
      "title":"Introduction to Rhetorical Studies"
    },
    {
      "course_id":"005042",
      "subject":"ENGL",
      "catalog_number":"103B",
      "title":"Varieties of English"
    },
    {
      "course_id":"011395",
      "subject":"ENGL",
      "catalog_number":"104",
      "title":"Rhetoric in Popular Culture"
    },
    {
      "course_id":"013480",
      "subject":"ENGL",
      "catalog_number":"108A",
      "title":"The Superhero"
    },
    {
      "course_id":"013481",
      "subject":"ENGL",
      "catalog_number":"108B",
      "title":"Global English Literatures"
    },
    {
      "course_id":"013482",
      "subject":"ENGL",
      "catalog_number":"108C",
      "title":"Literature and the Environment"
    },
    {
      "course_id":"013483",
      "subject":"ENGL",
      "catalog_number":"108D",
      "title":"Digital Lives"
    },
    {
      "course_id":"005049",
      "subject":"ENGL",
      "catalog_number":"108E",
      "title":"Women in Literature"
    },
    {
      "course_id":"005050",
      "subject":"ENGL",
      "catalog_number":"108F",
      "title":"The Rebel"
    },
    {
      "course_id":"005051",
      "subject":"ENGL",
      "catalog_number":"108H",
      "title":"Isolation and Alienation"
    },
    {
      "course_id":"005052",
      "subject":"ENGL",
      "catalog_number":"108M",
      "title":"Youth and Adolescence"
    },
    {
      "course_id":"005054",
      "subject":"ENGL",
      "catalog_number":"109",
      "title":"Introduction to Academic Writing"
    },
    {
      "course_id":"011175",
      "subject":"ENGL",
      "catalog_number":"119",
      "title":"Communications in Mathematics & Computer Science"
    },
    {
      "course_id":"005061",
      "subject":"ENGL",
      "catalog_number":"129R",
      "title":"Written Academic English"
    },
    {
      "course_id":"005064",
      "subject":"ENGL",
      "catalog_number":"140R",
      "title":"The Use of English 1"
    },
    {
      "course_id":"005065",
      "subject":"ENGL",
      "catalog_number":"141R",
      "title":"The Use of English 2"
    },
    {
      "course_id":"005068",
      "subject":"ENGL",
      "catalog_number":"190",
      "title":"Shakespeare"
    },
    {
      "course_id":"005069",
      "subject":"ENGL",
      "catalog_number":"200A",
      "title":"Survey of British Literature 1"
    },
    {
      "course_id":"005070",
      "subject":"ENGL",
      "catalog_number":"200B",
      "title":"Survey of British Literature 2"
    },
    {
      "course_id":"005071",
      "subject":"ENGL",
      "catalog_number":"201",
      "title":"The Short Story"
    },
    {
      "course_id":"005072",
      "subject":"ENGL",
      "catalog_number":"202A",
      "title":"The Bible and Literature 1"
    },
    {
      "course_id":"005073",
      "subject":"ENGL",
      "catalog_number":"202B",
      "title":"The Bible and Literature 2"
    },
    {
      "course_id":"011680",
      "subject":"ENGL",
      "catalog_number":"203",
      "title":"Designing Digital Images and Hypertext"
    },
    {
      "course_id":"011681",
      "subject":"ENGL",
      "catalog_number":"204",
      "title":"Designing Digital Video"
    },
    {
      "course_id":"005078",
      "subject":"ENGL",
      "catalog_number":"205R",
      "title":"The Canadian Short Story"
    },
    {
      "course_id":"011769",
      "subject":"ENGL",
      "catalog_number":"206",
      "title":"Writing Lives"
    },
    {
      "course_id":"005081",
      "subject":"ENGL",
      "catalog_number":"208A",
      "title":"Forms of Fantasy"
    },
    {
      "course_id":"005082",
      "subject":"ENGL",
      "catalog_number":"208B",
      "title":"Science Fiction"
    },
    {
      "course_id":"005083",
      "subject":"ENGL",
      "catalog_number":"208C",
      "title":"Studies in Children's Literature"
    },
    {
      "course_id":"005084",
      "subject":"ENGL",
      "catalog_number":"208E",
      "title":"Women Writing since 1900"
    },
    {
      "course_id":"005086",
      "subject":"ENGL",
      "catalog_number":"208H",
      "title":"Arthurian Legend"
    },
    {
      "course_id":"005087",
      "subject":"ENGL",
      "catalog_number":"208K",
      "title":"Detective Fiction"
    },
    {
      "course_id":"009249",
      "subject":"ENGL",
      "catalog_number":"208L",
      "title":"Race and English Literature"
    },
    {
      "course_id":"010194",
      "subject":"ENGL",
      "catalog_number":"208M",
      "title":"Travel Literature"
    },
    {
      "course_id":"010335",
      "subject":"ENGL",
      "catalog_number":"208N",
      "title":"Sex and Marriage in Literature"
    },
    {
      "course_id":"005095",
      "subject":"ENGL",
      "catalog_number":"210E",
      "title":"Genres of Technical Communication"
    },
    {
      "course_id":"005096",
      "subject":"ENGL",
      "catalog_number":"210F",
      "title":"Genres of Business Communication"
    },
    {
      "course_id":"009890",
      "subject":"ENGL",
      "catalog_number":"210H",
      "title":"Arts Writing"
    },
    {
      "course_id":"010336",
      "subject":"ENGL",
      "catalog_number":"210I",
      "title":"Legal Writing"
    },
    {
      "course_id":"011770",
      "subject":"ENGL",
      "catalog_number":"212",
      "title":"Convict Literature"
    },
    {
      "course_id":"011771",
      "subject":"ENGL",
      "catalog_number":"213",
      "title":"Literature and the Law"
    },
    {
      "course_id":"005100",
      "subject":"ENGL",
      "catalog_number":"214",
      "title":"Themes in Canadian Literature"
    },
    {
      "course_id":"005101",
      "subject":"ENGL",
      "catalog_number":"215",
      "title":"Canadian Regional Literature"
    },
    {
      "course_id":"005102",
      "subject":"ENGL",
      "catalog_number":"216",
      "title":"Canadian Multicultural Literature"
    },
    {
      "course_id":"005104",
      "subject":"ENGL",
      "catalog_number":"217",
      "title":"Canadian Children's Literature"
    },
    {
      "course_id":"005106",
      "subject":"ENGL",
      "catalog_number":"218",
      "title":"Mennonite Literature"
    },
    {
      "course_id":"013008",
      "subject":"ENGL",
      "catalog_number":"220A",
      "title":"Languages and Society I"
    },
    {
      "course_id":"013009",
      "subject":"ENGL",
      "catalog_number":"220B",
      "title":"Languages and Society II"
    },
    {
      "course_id":"013877",
      "subject":"ENGL",
      "catalog_number":"220C",
      "title":"Comparative Literature: Theory and Practice"
    },
    {
      "course_id":"004684",
      "subject":"ENGL",
      "catalog_number":"233C",
      "title":"Survey of Dramatic Literature and Theory 5"
    },
    {
      "course_id":"004685",
      "subject":"ENGL",
      "catalog_number":"233D",
      "title":"Survey of Dramatic Literature and Theory 6"
    },
    {
      "course_id":"010338",
      "subject":"ENGL",
      "catalog_number":"247",
      "title":"American Literature and Popular Culture"
    },
    {
      "course_id":"005120",
      "subject":"ENGL",
      "catalog_number":"251A",
      "title":"Criticism 1"
    },
    {
      "course_id":"005121",
      "subject":"ENGL",
      "catalog_number":"251B",
      "title":"Criticism 2"
    },
    {
      "course_id":"011370",
      "subject":"ENGL",
      "catalog_number":"260",
      "title":"Irish Literature and the \"Troubles\""
    },
    {
      "course_id":"013352",
      "subject":"ENGL",
      "catalog_number":"290",
      "title":"Global Shakespeare"
    },
    {
      "course_id":"005122",
      "subject":"ENGL",
      "catalog_number":"292",
      "title":"Contemporary Issues in Language, Writing, and Rhetoric"
    },
    {
      "course_id":"013353",
      "subject":"ENGL",
      "catalog_number":"293",
      "title":"Introduction to Digital Media Studies"
    },
    {
      "course_id":"011582",
      "subject":"ENGL",
      "catalog_number":"301H",
      "title":"Honours Literary Studies"
    },
    {
      "course_id":"011682",
      "subject":"ENGL",
      "catalog_number":"303",
      "title":"Special Topics in Digital Design"
    },
    {
      "course_id":"013106",
      "subject":"ENGL",
      "catalog_number":"304",
      "title":"Designing with Digital Sound"
    },
    {
      "course_id":"005124",
      "subject":"ENGL",
      "catalog_number":"305A",
      "title":"Old English 1"
    },
    {
      "course_id":"005125",
      "subject":"ENGL",
      "catalog_number":"305B",
      "title":"Old English 2"
    },
    {
      "course_id":"005126",
      "subject":"ENGL",
      "catalog_number":"306A",
      "title":"Introduction to Linguistics"
    },
    {
      "course_id":"005127",
      "subject":"ENGL",
      "catalog_number":"306B",
      "title":"Modern English Grammar"
    },
    {
      "course_id":"005128",
      "subject":"ENGL",
      "catalog_number":"306C",
      "title":"Historical Linguistics"
    },
    {
      "course_id":"005129",
      "subject":"ENGL",
      "catalog_number":"306D",
      "title":"The History of English"
    },
    {
      "course_id":"005131",
      "subject":"ENGL",
      "catalog_number":"306F",
      "title":"Introduction to Semiotics"
    },
    {
      "course_id":"005136",
      "subject":"ENGL",
      "catalog_number":"306G",
      "title":"Approaches to Style"
    },
    {
      "course_id":"005133",
      "subject":"ENGL",
      "catalog_number":"309A",
      "title":"Classical Rhetoric"
    },
    {
      "course_id":"005134",
      "subject":"ENGL",
      "catalog_number":"309B",
      "title":"Medieval to Pre-Modern Rhetoric"
    },
    {
      "course_id":"005135",
      "subject":"ENGL",
      "catalog_number":"309C",
      "title":"Contemporary Rhetoric"
    },
    {
      "course_id":"005137",
      "subject":"ENGL",
      "catalog_number":"309E",
      "title":"Speech Writing"
    },
    {
      "course_id":"011393",
      "subject":"ENGL",
      "catalog_number":"309G",
      "title":"The Discourse of Dissent"
    },
    {
      "course_id":"005139",
      "subject":"ENGL",
      "catalog_number":"310A",
      "title":"Chaucer 1"
    },
    {
      "course_id":"005140",
      "subject":"ENGL",
      "catalog_number":"310B",
      "title":"Chaucer 2"
    },
    {
      "course_id":"005141",
      "subject":"ENGL",
      "catalog_number":"310C",
      "title":"Non-Chaucerian Middle English Literature"
    },
    {
      "course_id":"005145",
      "subject":"ENGL",
      "catalog_number":"313",
      "title":"Early Canadian Literatures"
    },
    {
      "course_id":"005147",
      "subject":"ENGL",
      "catalog_number":"315",
      "title":"Modern Canadian Literature"
    },
    {
      "course_id":"005148",
      "subject":"ENGL",
      "catalog_number":"316",
      "title":"Canadian Drama"
    },
    {
      "course_id":"005150",
      "subject":"ENGL",
      "catalog_number":"318",
      "title":"Contemporary Canadian Literature"
    },
    {
      "course_id":"012358",
      "subject":"ENGL",
      "catalog_number":"319",
      "title":"History and Theory of Media 1"
    },
    {
      "course_id":"011392",
      "subject":"ENGL",
      "catalog_number":"320",
      "title":"History and Theory of Media 2"
    },
    {
      "course_id":"011583",
      "subject":"ENGL",
      "catalog_number":"322",
      "title":"Postcolonial Literature of the Americas"
    },
    {
      "course_id":"012931",
      "subject":"ENGL",
      "catalog_number":"325",
      "title":"Austen"
    },
    {
      "course_id":"005152",
      "subject":"ENGL",
      "catalog_number":"330A",
      "title":"Sixteenth-Century Literature 1"
    },
    {
      "course_id":"005153",
      "subject":"ENGL",
      "catalog_number":"330B",
      "title":"Sixteenth-Century Literature 2"
    },
    {
      "course_id":"005155",
      "subject":"ENGL",
      "catalog_number":"335",
      "title":"Creative Writing 1"
    },
    {
      "course_id":"005156",
      "subject":"ENGL",
      "catalog_number":"336",
      "title":"Creative Writing 2"
    },
    {
      "course_id":"010339",
      "subject":"ENGL",
      "catalog_number":"342",
      "title":"American Literature to 1860"
    },
    {
      "course_id":"005157",
      "subject":"ENGL",
      "catalog_number":"343",
      "title":"American Literature 1860-1910"
    },
    {
      "course_id":"005158",
      "subject":"ENGL",
      "catalog_number":"344",
      "title":"Modern American Literature"
    },
    {
      "course_id":"005159",
      "subject":"ENGL",
      "catalog_number":"345",
      "title":"American Literature in a Global Context"
    },
    {
      "course_id":"010195",
      "subject":"ENGL",
      "catalog_number":"346",
      "title":"American Fiction"
    },
    {
      "course_id":"005162",
      "subject":"ENGL",
      "catalog_number":"347",
      "title":"American Literature Since 1945"
    },
    {
      "course_id":"010196",
      "subject":"ENGL",
      "catalog_number":"348",
      "title":"American Poetry Since 1850"
    },
    {
      "course_id":"005164",
      "subject":"ENGL",
      "catalog_number":"350A",
      "title":"Seventeenth-Century Literature 1"
    },
    {
      "course_id":"005165",
      "subject":"ENGL",
      "catalog_number":"350B",
      "title":"Seventeenth-Century Literature 2"
    },
    {
      "course_id":"004682",
      "subject":"ENGL",
      "catalog_number":"361",
      "title":"English Drama to 1642"
    },
    {
      "course_id":"005166",
      "subject":"ENGL",
      "catalog_number":"362",
      "title":"Shakespeare 1"
    },
    {
      "course_id":"005167",
      "subject":"ENGL",
      "catalog_number":"363",
      "title":"Shakespeare 2"
    },
    {
      "course_id":"010197",
      "subject":"ENGL",
      "catalog_number":"364",
      "title":"Shakespeare in Performance at The Stratford Festival"
    },
    {
      "course_id":"005168",
      "subject":"ENGL",
      "catalog_number":"365",
      "title":"Selected Studies"
    },
    {
      "course_id":"005169",
      "subject":"ENGL",
      "catalog_number":"366",
      "title":"Selected Studies"
    },
    {
      "course_id":"011772",
      "subject":"ENGL",
      "catalog_number":"371",
      "title":"Editing Literary Works"
    },
    {
      "course_id":"005172",
      "subject":"ENGL",
      "catalog_number":"376R",
      "title":"Applied English Grammar 1"
    },
    {
      "course_id":"005173",
      "subject":"ENGL",
      "catalog_number":"377R",
      "title":"Applied English Grammar 2"
    },
    {
      "course_id":"005175",
      "subject":"ENGL",
      "catalog_number":"392A",
      "title":"Information Design"
    },
    {
      "course_id":"005176",
      "subject":"ENGL",
      "catalog_number":"392B",
      "title":"Visual Rhetoric"
    },
    {
      "course_id":"011683",
      "subject":"ENGL",
      "catalog_number":"403",
      "title":"Digital Design Research Project"
    },
    {
      "course_id":"012663",
      "subject":"ENGL",
      "catalog_number":"406",
      "title":"Advanced Rhetorical Study"
    },
    {
      "course_id":"012357",
      "subject":"ENGL",
      "catalog_number":"407",
      "title":"Language and Politics"
    },
    {
      "course_id":"005177",
      "subject":"ENGL",
      "catalog_number":"408A",
      "title":"Writing for the Media"
    },
    {
      "course_id":"005178",
      "subject":"ENGL",
      "catalog_number":"408B",
      "title":"The Discourse of Advertising"
    },
    {
      "course_id":"005179",
      "subject":"ENGL",
      "catalog_number":"408C",
      "title":"The Rhetoric of Digital Design: Theory and Practice"
    },
    {
      "course_id":"011394",
      "subject":"ENGL",
      "catalog_number":"409A",
      "title":"Rhetoric of Argumentation"
    },
    {
      "course_id":"005183",
      "subject":"ENGL",
      "catalog_number":"410A",
      "title":"Restoration Literature"
    },
    {
      "course_id":"005184",
      "subject":"ENGL",
      "catalog_number":"410B",
      "title":"Eighteenth-Century Literature 1"
    },
    {
      "course_id":"012930",
      "subject":"ENGL",
      "catalog_number":"410C",
      "title":"Eighteenth-Century Literature 2"
    },
    {
      "course_id":"010341",
      "subject":"ENGL",
      "catalog_number":"410D",
      "title":"Eighteenth-Century Fiction I"
    },
    {
      "course_id":"014557",
      "subject":"ENGL",
      "catalog_number":"410E",
      "title":"Eighteenth-Century Fiction II"
    },
    {
      "course_id":"014558",
      "subject":"ENGL",
      "catalog_number":"410F",
      "title":"Eighteenth-Century Women Writers"
    },
    {
      "course_id":"005185",
      "subject":"ENGL",
      "catalog_number":"430A",
      "title":"Literature of the Romantic Period 1"
    },
    {
      "course_id":"005186",
      "subject":"ENGL",
      "catalog_number":"430B",
      "title":"Literature of the Romantic Period 2"
    },
    {
      "course_id":"005190",
      "subject":"ENGL",
      "catalog_number":"451A",
      "title":"Literature of the Victorian Age 1"
    },
    {
      "course_id":"005191",
      "subject":"ENGL",
      "catalog_number":"451B",
      "title":"Literature of the Victorian Age 2"
    },
    {
      "course_id":"005192",
      "subject":"ENGL",
      "catalog_number":"460A",
      "title":"Early Literature of the Modernist Period in the United Kingdom and Ireland"
    },
    {
      "course_id":"005193",
      "subject":"ENGL",
      "catalog_number":"460B",
      "title":"Literature of the Modernist Period in the United Kingdom and Ireland"
    },
    {
      "course_id":"009982",
      "subject":"ENGL",
      "catalog_number":"487",
      "title":"Topics in British Literature and Commonwealth Literature Since 1800"
    },
    {
      "course_id":"005194",
      "subject":"ENGL",
      "catalog_number":"460C",
      "title":"Literature of the Postwar Period in the United Kingdom and Ireland"
    },
    {
      "course_id":"014269",
      "subject":"ENGL",
      "catalog_number":"460D",
      "title":"Contemporary Literature of the United Kingdom and Ireland"
    },
    {
      "course_id":"011584",
      "subject":"ENGL",
      "catalog_number":"463",
      "title":"Postcolonial Literatures"
    },
    {
      "course_id":"005195",
      "subject":"ENGL",
      "catalog_number":"470A",
      "title":"Contemporary Critical Theory"
    },
    {
      "course_id":"005196",
      "subject":"ENGL",
      "catalog_number":"470B",
      "title":"History of Literary Criticism"
    },
    {
      "course_id":"005197",
      "subject":"ENGL",
      "catalog_number":"470C",
      "title":"Literary Studies in Electronic Forms"
    },
    {
      "course_id":"011773",
      "subject":"ENGL",
      "catalog_number":"471",
      "title":"Adapting Literary Works"
    },
    {
      "course_id":"009976",
      "subject":"ENGL",
      "catalog_number":"481",
      "title":"Topics in the History and Theory of Language"
    },
    {
      "course_id":"009979",
      "subject":"ENGL",
      "catalog_number":"484",
      "title":"Topics in Literatures Medieval to Romantic"
    },
    {
      "course_id":"014485",
      "subject":"ENGL",
      "catalog_number":"485",
      "title":"Topics in Literatures Romantic to Modern"
    },
    {
      "course_id":"014486",
      "subject":"ENGL",
      "catalog_number":"486",
      "title":"Topics in Literatures Modern to Contemporary"
    },
    {
      "course_id":"014487",
      "subject":"ENGL",
      "catalog_number":"492",
      "title":"Topics in the History and Theory of Rhetoric"
    },
    {
      "course_id":"014488",
      "subject":"ENGL",
      "catalog_number":"493",
      "title":"Topics in Professional Writing and Communication Design"
    },
    {
      "course_id":"014489",
      "subject":"ENGL",
      "catalog_number":"494",
      "title":"Topics in Forms of Media and Critical Analysis"
    },
    {
      "course_id":"005223",
      "subject":"ENGL",
      "catalog_number":"495A",
      "title":"Supervision of Honours Essay"
    },
    {
      "course_id":"005224",
      "subject":"ENGL",
      "catalog_number":"495B",
      "title":"Supervision of Honours Essay"
    },
    {
      "course_id":"001021",
      "subject":"ENGL",
      "catalog_number":"700",
      "title":"Rhetorical Studies"
    },
    {
      "course_id":"010560",
      "subject":"ENGL",
      "catalog_number":"705",
      "title":"Studies in Old and Middle English Literature"
    },
    {
      "course_id":"010561",
      "subject":"ENGL",
      "catalog_number":"710",
      "title":"Studies in Renaissance Drama"
    },
    {
      "course_id":"010562",
      "subject":"ENGL",
      "catalog_number":"715",
      "title":"Studies in Renaissance Prose and Poetry"
    },
    {
      "course_id":"010563",
      "subject":"ENGL",
      "catalog_number":"720",
      "title":"Studies in the Restoration and Eighteenth Century Literature"
    },
    {
      "course_id":"010564",
      "subject":"ENGL",
      "catalog_number":"725",
      "title":"Studies in Romanticism"
    },
    {
      "course_id":"010565",
      "subject":"ENGL",
      "catalog_number":"730",
      "title":"Studies in Victorian Literature"
    },
    {
      "course_id":"010566",
      "subject":"ENGL",
      "catalog_number":"735",
      "title":"Studies in Modern British Literature"
    },
    {
      "course_id":"010567",
      "subject":"ENGL",
      "catalog_number":"750",
      "title":"Studies in Early American Literature"
    },
    {
      "course_id":"010568",
      "subject":"ENGL",
      "catalog_number":"755",
      "title":"Studies in 19th Century American Literature"
    },
    {
      "course_id":"010569",
      "subject":"ENGL",
      "catalog_number":"760",
      "title":"Studies in 20th-Century American Literature"
    },
    {
      "course_id":"010570",
      "subject":"ENGL",
      "catalog_number":"770",
      "title":"Studies in Canadian Literature"
    },
    {
      "course_id":"001208",
      "subject":"ERS",
      "catalog_number":"618",
      "title":"Sustainable Energy Systems"
    },
    {
      "course_id":"010571",
      "subject":"ENGL",
      "catalog_number":"775",
      "title":"Studies in Commonwealth Literature"
    },
    {
      "course_id":"010572",
      "subject":"ENGL",
      "catalog_number":"780",
      "title":"Studies in Genre"
    },
    {
      "course_id":"010573",
      "subject":"ENGL",
      "catalog_number":"785",
      "title":"Studies in Literary Criticism"
    },
    {
      "course_id":"014217",
      "subject":"ENGL",
      "catalog_number":"788",
      "title":"Topics in Rhetorical Theory and Criticism"
    },
    {
      "course_id":"014218",
      "subject":"ENGL",
      "catalog_number":"789",
      "title":"Writing Studies"
    },
    {
      "course_id":"010574",
      "subject":"ENGL",
      "catalog_number":"790",
      "title":"Discourse Analysis"
    },
    {
      "course_id":"010575",
      "subject":"ENGL",
      "catalog_number":"791",
      "title":"Professional Writing"
    },
    {
      "course_id":"010576",
      "subject":"ENGL",
      "catalog_number":"792",
      "title":"Semiotics"
    },
    {
      "course_id":"010577",
      "subject":"ENGL",
      "catalog_number":"793",
      "title":"History of Rhetoric"
    },
    {
      "course_id":"010578",
      "subject":"ENGL",
      "catalog_number":"794",
      "title":"Digital Culture"
    },
    {
      "course_id":"010579",
      "subject":"ENGL",
      "catalog_number":"795",
      "title":"Studies in Selected Topics"
    },
    {
      "course_id":"001206",
      "subject":"ERS",
      "catalog_number":"605",
      "title":"Ecosystem Perspectives and Analysis"
    },
    {
      "course_id":"010429",
      "subject":"ERS",
      "catalog_number":"610",
      "title":"Public Administration of the Environment & Natural Resources"
    },
    {
      "course_id":"009098",
      "subject":"ENGL",
      "catalog_number":"796",
      "title":"Propaganda and Ideology"
    },
    {
      "course_id":"001200",
      "subject":"ENGL",
      "catalog_number":"797",
      "title":"Digital Media and Literature"
    },
    {
      "course_id":"001201",
      "subject":"ENGL",
      "catalog_number":"799",
      "title":"Media Theory and Critique"
    },
    {
      "course_id":"005226",
      "subject":"ENVE",
      "catalog_number":"100",
      "title":"Environmental and Geological Engineering Concepts"
    },
    {
      "course_id":"005230",
      "subject":"ENVE",
      "catalog_number":"127",
      "title":"Statics and Solid Mechanics"
    },
    {
      "course_id":"011496",
      "subject":"ENVE",
      "catalog_number":"153",
      "title":"Earth Engineering"
    },
    {
      "course_id":"005232",
      "subject":"ENVE",
      "catalog_number":"214",
      "title":"Fluid Mechanics and Thermal Sciences"
    },
    {
      "course_id":"005234",
      "subject":"ENVE",
      "catalog_number":"221",
      "title":"Advanced Calculus"
    },
    {
      "course_id":"005236",
      "subject":"ENVE",
      "catalog_number":"223",
      "title":"Differential Equations"
    },
    {
      "course_id":"005237",
      "subject":"ENVE",
      "catalog_number":"224",
      "title":"Probability and Statistics"
    },
    {
      "course_id":"005239",
      "subject":"ENVE",
      "catalog_number":"275",
      "title":"Environmental Chemistry"
    },
    {
      "course_id":"011506",
      "subject":"ENVE",
      "catalog_number":"276",
      "title":"Environmental Biology and Biotechnology"
    },
    {
      "course_id":"005242",
      "subject":"ENVE",
      "catalog_number":"292",
      "title":"Economics for Environmental Engineering"
    },
    {
      "course_id":"009251",
      "subject":"ENVE",
      "catalog_number":"298",
      "title":"Seminar"
    },
    {
      "course_id":"009252",
      "subject":"ENVE",
      "catalog_number":"299",
      "title":"Seminar"
    },
    {
      "course_id":"005240",
      "subject":"ENVE",
      "catalog_number":"320",
      "title":"Environmental Resource Management"
    },
    {
      "course_id":"005241",
      "subject":"ENVE",
      "catalog_number":"321",
      "title":"Advanced Mathematics"
    },
    {
      "course_id":"005244",
      "subject":"ENVE",
      "catalog_number":"330",
      "title":"Lab Analysis and Field Sampling Techniques"
    },
    {
      "course_id":"014965",
      "subject":"ENVE",
      "catalog_number":"335",
      "title":"Decision Making for Environmental Engineers"
    },
    {
      "course_id":"005248",
      "subject":"ENVE",
      "catalog_number":"375",
      "title":"Water Quality Engineering"
    },
    {
      "course_id":"005249",
      "subject":"ENVE",
      "catalog_number":"391",
      "title":"Law and Ethics for Environmental Engineers"
    },
    {
      "course_id":"009253",
      "subject":"ENVE",
      "catalog_number":"398",
      "title":"Seminar"
    },
    {
      "course_id":"009254",
      "subject":"ENVE",
      "catalog_number":"399",
      "title":"Seminar"
    },
    {
      "course_id":"005253",
      "subject":"ENVE",
      "catalog_number":"430",
      "title":"Environmental Engineering Project 1"
    },
    {
      "course_id":"005254",
      "subject":"ENVE",
      "catalog_number":"431",
      "title":"Environmental Engineering Project 2"
    },
    {
      "course_id":"005255",
      "subject":"ENVE",
      "catalog_number":"472",
      "title":"Wastewater Treatment"
    },
    {
      "course_id":"009255",
      "subject":"ENVE",
      "catalog_number":"498",
      "title":"Seminar"
    },
    {
      "course_id":"009256",
      "subject":"ENVE",
      "catalog_number":"499",
      "title":"Seminar"
    },
    {
      "course_id":"005256",
      "subject":"ENVE",
      "catalog_number":"573",
      "title":"Contaminant Transport"
    },
    {
      "course_id":"005257",
      "subject":"ENVE",
      "catalog_number":"577",
      "title":"Engineering for Solid Waste Management"
    },
    {
      "course_id":"014371",
      "subject":"ENVS",
      "catalog_number":"105",
      "title":"Environmental Sustainability and Ethics"
    },
    {
      "course_id":"013019",
      "subject":"ENVS",
      "catalog_number":"131",
      "title":"Communications for Environmental Professions"
    },
    {
      "course_id":"005261",
      "subject":"ENVS",
      "catalog_number":"178",
      "title":"Introduction to Environmental Research Methods"
    },
    {
      "course_id":"005262",
      "subject":"ENVS",
      "catalog_number":"195",
      "title":"Introduction to Environmental Studies"
    },
    {
      "course_id":"005263",
      "subject":"ENVS",
      "catalog_number":"200",
      "title":"Field Ecology"
    },
    {
      "course_id":"005264",
      "subject":"ENVS",
      "catalog_number":"201",
      "title":"Introduction to Canadian Environmental Law"
    },
    {
      "course_id":"005266",
      "subject":"ENVS",
      "catalog_number":"220",
      "title":"Ecological Economics"
    },
    {
      "course_id":"005271",
      "subject":"ENVS",
      "catalog_number":"278",
      "title":"Advanced Environmental Research Methods"
    },
    {
      "course_id":"005274",
      "subject":"ENVS",
      "catalog_number":"334",
      "title":"Introduction to Park Management"
    },
    {
      "course_id":"005290",
      "subject":"ENVS",
      "catalog_number":"395",
      "title":"Study Abroad"
    },
    {
      "course_id":"005294",
      "subject":"ENVS",
      "catalog_number":"401",
      "title":"Aboriginal Law and Natural Resource Development"
    },
    {
      "course_id":"005299",
      "subject":"ENVS",
      "catalog_number":"433",
      "title":"Ecotourism and Park Tourism"
    },
    {
      "course_id":"012661",
      "subject":"ENVS",
      "catalog_number":"444",
      "title":"Ecosystem and Resource Management in Parks\/Natural Areas"
    },
    {
      "course_id":"005302",
      "subject":"ENVS",
      "catalog_number":"469",
      "title":"Landscape Ecology, Restoration and Rehabilitation"
    },
    {
      "course_id":"012288",
      "subject":"ENVS",
      "catalog_number":"474",
      "title":"Special Topics in Environmental Studies"
    },
    {
      "course_id":"005304",
      "subject":"ERS",
      "catalog_number":"110",
      "title":"Environmental Analysis and Solutions I: Foundations"
    },
    {
      "course_id":"005305",
      "subject":"ERS",
      "catalog_number":"111",
      "title":"Environmental Analysis and Solutions II: Experiential Approaches"
    },
    {
      "course_id":"010023",
      "subject":"ERS",
      "catalog_number":"210",
      "title":"Environmental Analysis and Solutions III: Greening Communities"
    },
    {
      "course_id":"013301",
      "subject":"ERS",
      "catalog_number":"211",
      "title":"Environmental Analysis and Solutions IV: Restoration Ecology"
    },
    {
      "course_id":"005311",
      "subject":"ERS",
      "catalog_number":"215",
      "title":"Environmental and Sustainability Assessment I"
    },
    {
      "course_id":"013898",
      "subject":"ERS",
      "catalog_number":"234",
      "title":"Forest Ecosystems"
    },
    {
      "course_id":"005342",
      "subject":"ERS",
      "catalog_number":"253",
      "title":"The Politics of Sustainable Communities"
    },
    {
      "course_id":"013671",
      "subject":"ERS",
      "catalog_number":"265",
      "title":"Water: Environmental History and Change"
    },
    {
      "course_id":"013854",
      "subject":"ERS",
      "catalog_number":"266",
      "title":"Water: Environmental History and Change"
    },
    {
      "course_id":"005312",
      "subject":"ERS",
      "catalog_number":"270",
      "title":"Introduction to Sustainable Agriculture"
    },
    {
      "course_id":"005313",
      "subject":"ERS",
      "catalog_number":"275",
      "title":"Special Readings\/Seminar on Select Topics"
    },
    {
      "course_id":"012892",
      "subject":"ERS",
      "catalog_number":"283",
      "title":"Ontario Natural History: Species and Patterns"
    },
    {
      "course_id":"010224",
      "subject":"ERS",
      "catalog_number":"294",
      "title":"The Sacred Earth: Religion and Ecology"
    },
    {
      "course_id":"005374",
      "subject":"ERS",
      "catalog_number":"310",
      "title":"Environmental Analysis and Solutions V: Environmental Thought"
    },
    {
      "course_id":"005370",
      "subject":"ERS",
      "catalog_number":"311",
      "title":"Environmental Research Project I: Systems Thinking for Interdisciplinary Research"
    },
    {
      "course_id":"005380",
      "subject":"ERS",
      "catalog_number":"409",
      "title":"Activism! Community Action for Environmental and Social Change"
    },
    {
      "course_id":"005339",
      "subject":"ERS",
      "catalog_number":"315",
      "title":"Environmental and Sustainability Assessment II"
    },
    {
      "course_id":"011666",
      "subject":"ERS",
      "catalog_number":"316",
      "title":"Urban Water and Wastewater Systems: Integrated Planning and Management"
    },
    {
      "course_id":"014716",
      "subject":"ERS",
      "catalog_number":"373",
      "title":"Special Topics in Environmental and Resource Studies"
    },
    {
      "course_id":"005332",
      "subject":"ERS",
      "catalog_number":"317",
      "title":"Waste Management"
    },
    {
      "course_id":"005336",
      "subject":"ERS",
      "catalog_number":"330",
      "title":"Environmental Journalism 1"
    },
    {
      "course_id":"014098",
      "subject":"ERS",
      "catalog_number":"340",
      "title":"Ecosystem Assessment"
    },
    {
      "course_id":"014099",
      "subject":"ERS",
      "catalog_number":"341",
      "title":"Professional Conservation and Restoration Practice I"
    },
    {
      "course_id":"005343",
      "subject":"ERS",
      "catalog_number":"360",
      "title":"Nature: Art, Myth and Folklore"
    },
    {
      "course_id":"013672",
      "subject":"ERS",
      "catalog_number":"365",
      "title":"Water Governance"
    },
    {
      "course_id":"005345",
      "subject":"ERS",
      "catalog_number":"370",
      "title":"Corporate Sustainability: Issues and Prospects"
    },
    {
      "course_id":"011117",
      "subject":"ERS",
      "catalog_number":"371",
      "title":"An Ecosystem Approach to Environment and Health"
    },
    {
      "course_id":"011667",
      "subject":"ERS",
      "catalog_number":"372",
      "title":"First Nations and the Environment"
    },
    {
      "course_id":"005346",
      "subject":"ERS",
      "catalog_number":"375",
      "title":"Special Readings\/Seminar on Select Topics"
    },
    {
      "course_id":"005326",
      "subject":"ERS",
      "catalog_number":"382",
      "title":"Ecological Monitoring"
    },
    {
      "course_id":"015023",
      "subject":"ERS",
      "catalog_number":"406",
      "title":"Paths to Sustainability"
    },
    {
      "course_id":"012580",
      "subject":"ERS",
      "catalog_number":"383",
      "title":"Tropical Ecosystems"
    },
    {
      "course_id":"005377",
      "subject":"ERS",
      "catalog_number":"404",
      "title":"Global Environmental Governance"
    },
    {
      "course_id":"005407",
      "subject":"ERS",
      "catalog_number":"410",
      "title":"Environmental Analysis and Solutions VI: Ecosocial Systems"
    },
    {
      "course_id":"005401",
      "subject":"ERS",
      "catalog_number":"411A",
      "title":"Environmental Research Project II"
    },
    {
      "course_id":"005402",
      "subject":"ERS",
      "catalog_number":"411B",
      "title":"Environmental Research Project III"
    },
    {
      "course_id":"005403",
      "subject":"ERS",
      "catalog_number":"412A",
      "title":"Environmental Research Project II"
    },
    {
      "course_id":"005404",
      "subject":"ERS",
      "catalog_number":"412B",
      "title":"Environmental Research Project III"
    },
    {
      "course_id":"013962",
      "subject":"ERS",
      "catalog_number":"413",
      "title":"Senior Honours Research Seminar"
    },
    {
      "course_id":"005386",
      "subject":"ERS",
      "catalog_number":"415",
      "title":"Environmental and Sustainability Assessment III"
    },
    {
      "course_id":"005385",
      "subject":"ERS",
      "catalog_number":"430",
      "title":"Environmental Journalism 2"
    },
    {
      "course_id":"013956",
      "subject":"ERS",
      "catalog_number":"461",
      "title":"Food Systems and Sustainability"
    },
    {
      "course_id":"013955",
      "subject":"ERS",
      "catalog_number":"462",
      "title":"Global Food and Agricultural Politics"
    },
    {
      "course_id":"014369",
      "subject":"ERS",
      "catalog_number":"464",
      "title":"Economics and Sustainability"
    },
    {
      "course_id":"010174",
      "subject":"ERS",
      "catalog_number":"474",
      "title":"Special Topics in Environmental and Resource Studies"
    },
    {
      "course_id":"005388",
      "subject":"ERS",
      "catalog_number":"475",
      "title":"Special Readings\/Seminar on Select Topics"
    },
    {
      "course_id":"012202",
      "subject":"ERS",
      "catalog_number":"476",
      "title":"Environmental Education"
    },
    {
      "course_id":"012719",
      "subject":"ERS",
      "catalog_number":"484",
      "title":"Soil Ecosystem Dynamics"
    },
    {
      "course_id":"001205",
      "subject":"ERS",
      "catalog_number":"604",
      "title":"Advanced Topics in Global Environmental Governance"
    },
    {
      "course_id":"012738",
      "subject":"ERS",
      "catalog_number":"606",
      "title":"Governing Global Food and Agriculture Systems"
    },
    {
      "course_id":"001842",
      "subject":"ERS",
      "catalog_number":"615",
      "title":"Community Economic Development"
    },
    {
      "course_id":"012666",
      "subject":"ERS",
      "catalog_number":"619",
      "title":"Energy Sustainability"
    },
    {
      "course_id":"014119",
      "subject":"ERS",
      "catalog_number":"650",
      "title":"Topics in Governance and Sustainable Communities"
    },
    {
      "course_id":"001210",
      "subject":"ERS",
      "catalog_number":"660",
      "title":"Perspectives in Resource and Environmental Management"
    },
    {
      "course_id":"001213",
      "subject":"ERS",
      "catalog_number":"669",
      "title":"Research and Design Methods"
    },
    {
      "course_id":"011630",
      "subject":"ERS",
      "catalog_number":"670",
      "title":"MES Research Development"
    },
    {
      "course_id":"012340",
      "subject":"ERS",
      "catalog_number":"674",
      "title":"Special Topics in Environment and Resource Studies"
    },
    {
      "course_id":"010430",
      "subject":"ERS",
      "catalog_number":"675",
      "title":"Special Readings and Seminars on Selected Topics in Environment and Resource Studies"
    },
    {
      "course_id":"011631",
      "subject":"ERS",
      "catalog_number":"680",
      "title":"Sustainability Foundations"
    },
    {
      "course_id":"014364",
      "subject":"ERS",
      "catalog_number":"681",
      "title":"Sustainability Applications"
    },
    {
      "course_id":"013380",
      "subject":"ERS",
      "catalog_number":"701",
      "title":"Sustainability in Complex Socio-Ecological Systems"
    },
    {
      "course_id":"013381",
      "subject":"ERS",
      "catalog_number":"702",
      "title":"Critical Analysis and Advance Research in Environmental Studies"
    },
    {
      "course_id":"011984",
      "subject":"ESL",
      "catalog_number":"101R",
      "title":"Oral Communications for Academic Purposes"
    },
    {
      "course_id":"011985",
      "subject":"ESL",
      "catalog_number":"102R",
      "title":"Error Correction in Academic Writing"
    },
    {
      "course_id":"014140",
      "subject":"ESL",
      "catalog_number":"103R",
      "title":"Phonetics for Effective English Pronunciation"
    },
    {
      "course_id":"013932",
      "subject":"ESL",
      "catalog_number":"110R",
      "title":"Canadian Academic Culture"
    },
    {
      "course_id":"005061",
      "subject":"ESL",
      "catalog_number":"129R",
      "title":"Written Academic English"
    },
    {
      "course_id":"012351",
      "subject":"ESL",
      "catalog_number":"601R",
      "title":"Speaking English for Professional Purposes"
    },
    {
      "course_id":"012153",
      "subject":"ESL",
      "catalog_number":"602R",
      "title":"Scholarly Writing in English"
    },
    {
      "course_id":"012222",
      "subject":"ESL",
      "catalog_number":"612R",
      "title":"Professional Writing for Engineers"
    },
    {
      "course_id":"013490",
      "subject":"FINE",
      "catalog_number":"100",
      "title":"Studio Fundamentals"
    },
    {
      "course_id":"013622",
      "subject":"FINE",
      "catalog_number":"101",
      "title":"Art History and Visual Culture"
    },
    {
      "course_id":"013621",
      "subject":"FINE",
      "catalog_number":"102",
      "title":"World Cinema and Visual Culture"
    },
    {
      "course_id":"005422",
      "subject":"FINE",
      "catalog_number":"112",
      "title":"Modern Art, 1874-1945"
    },
    {
      "course_id":"013957",
      "subject":"FINE",
      "catalog_number":"130",
      "title":"Introduction to Digital Imaging"
    },
    {
      "course_id":"011369",
      "subject":"FINE",
      "catalog_number":"150",
      "title":"Appreciation and Expression"
    },
    {
      "course_id":"013491",
      "subject":"FINE",
      "catalog_number":"202",
      "title":"Painting"
    },
    {
      "course_id":"013500",
      "subject":"FINE",
      "catalog_number":"204",
      "title":"Topics in Studio Practice"
    },
    {
      "course_id":"013501",
      "subject":"FINE",
      "catalog_number":"205",
      "title":"Topics in Art History"
    },
    {
      "course_id":"013502",
      "subject":"FINE",
      "catalog_number":"206",
      "title":"Topics in Film Studies"
    },
    {
      "course_id":"012716",
      "subject":"FINE",
      "catalog_number":"209",
      "title":"Modern Art, 1940-1970"
    },
    {
      "course_id":"005425",
      "subject":"FINE",
      "catalog_number":"210",
      "title":"Art, 1780-1875"
    },
    {
      "course_id":"005427",
      "subject":"FINE",
      "catalog_number":"212",
      "title":"Renaissance Art, 1300-1500"
    },
    {
      "course_id":"005429",
      "subject":"FINE",
      "catalog_number":"213",
      "title":"Art of the 16th Century in Europe"
    },
    {
      "course_id":"005430",
      "subject":"FINE",
      "catalog_number":"214",
      "title":"Medieval Art and Architecture"
    },
    {
      "course_id":"005431",
      "subject":"FINE",
      "catalog_number":"215",
      "title":"Art of the 17th Century in Europe"
    },
    {
      "course_id":"005483",
      "subject":"FINE",
      "catalog_number":"216",
      "title":"Topics in First Nations' Visual Culture"
    },
    {
      "course_id":"005435",
      "subject":"FINE",
      "catalog_number":"220",
      "title":"Oil Painting"
    },
    {
      "course_id":"005438",
      "subject":"FINE",
      "catalog_number":"221",
      "title":"Acrylic and Mixed Media"
    },
    {
      "course_id":"005439",
      "subject":"FINE",
      "catalog_number":"222",
      "title":"Principles of Sculpture"
    },
    {
      "course_id":"005440",
      "subject":"FINE",
      "catalog_number":"223",
      "title":"Methods and Materials of Sculpture"
    },
    {
      "course_id":"005441",
      "subject":"FINE",
      "catalog_number":"223A",
      "title":"Clay Studies"
    },
    {
      "course_id":"005442",
      "subject":"FINE",
      "catalog_number":"224",
      "title":"Expressive Drawing"
    },
    {
      "course_id":"005443",
      "subject":"FINE",
      "catalog_number":"225",
      "title":"Observational Drawing"
    },
    {
      "course_id":"005445",
      "subject":"FINE",
      "catalog_number":"226A",
      "title":"Introduction to Printmaking A"
    },
    {
      "course_id":"013492",
      "subject":"FINE",
      "catalog_number":"226",
      "title":"Experimental Drawing"
    },
    {
      "course_id":"005453",
      "subject":"FINE",
      "catalog_number":"227",
      "title":"Photography"
    },
    {
      "course_id":"005452",
      "subject":"FINE",
      "catalog_number":"228",
      "title":"Digital Imaging"
    },
    {
      "course_id":"005456",
      "subject":"FINE",
      "catalog_number":"229",
      "title":"Hybrid Digital Media"
    },
    {
      "course_id":"005445",
      "subject":"FINE",
      "catalog_number":"230",
      "title":"Printmaking"
    },
    {
      "course_id":"013494",
      "subject":"FINE",
      "catalog_number":"231",
      "title":"Mixed Multiples"
    },
    {
      "course_id":"013495",
      "subject":"FINE",
      "catalog_number":"232",
      "title":"Video and Sound"
    },
    {
      "course_id":"005478",
      "subject":"FINE",
      "catalog_number":"241",
      "title":"Survey of Greek Art and Architecture"
    },
    {
      "course_id":"005480",
      "subject":"FINE",
      "catalog_number":"242",
      "title":"Survey of Roman Art and Architecture"
    },
    {
      "course_id":"013496",
      "subject":"FINE",
      "catalog_number":"243",
      "title":"Topics in Fine Arts Experiential Learning"
    },
    {
      "course_id":"014402",
      "subject":"FINE",
      "catalog_number":"244",
      "title":"History of Visual Media to 1910"
    },
    {
      "course_id":"014391",
      "subject":"FINE",
      "catalog_number":"245",
      "title":"History of Film and Visual Media from 1900 to Today"
    },
    {
      "course_id":"005468",
      "subject":"FINE",
      "catalog_number":"252",
      "title":"Religion in Popular Film"
    },
    {
      "course_id":"005469",
      "subject":"FINE",
      "catalog_number":"253",
      "title":"Thematic Approaches to Religion in Film"
    },
    {
      "course_id":"005470",
      "subject":"FINE",
      "catalog_number":"255R",
      "title":"Film as Social Criticism"
    },
    {
      "course_id":"014390",
      "subject":"FINE",
      "catalog_number":"256",
      "title":"Experimental Film"
    },
    {
      "course_id":"014389",
      "subject":"FINE",
      "catalog_number":"257",
      "title":"Video, New Media & the Digital Turn"
    },
    {
      "course_id":"013221",
      "subject":"FINE",
      "catalog_number":"262",
      "title":"Global Queer Cinema"
    },
    {
      "course_id":"014413",
      "subject":"FINE",
      "catalog_number":"271",
      "title":"Ceramics: Studies in Material Practice"
    },
    {
      "course_id":"005441",
      "subject":"FINE",
      "catalog_number":"272",
      "title":"Clay Studies"
    },
    {
      "course_id":"013493",
      "subject":"FINE",
      "catalog_number":"274",
      "title":"Figure and Anatomy"
    },
    {
      "course_id":"005475",
      "subject":"FINE",
      "catalog_number":"281",
      "title":"Art and Gender"
    },
    {
      "course_id":"012079",
      "subject":"FINE",
      "catalog_number":"282",
      "title":"Canadian Art from the 17th Century to 1940"
    },
    {
      "course_id":"012455",
      "subject":"FINE",
      "catalog_number":"293",
      "title":"Fine Arts Abroad"
    },
    {
      "course_id":"011782",
      "subject":"FINE",
      "catalog_number":"294",
      "title":"Fine Arts Abroad"
    },
    {
      "course_id":"013505",
      "subject":"FINE",
      "catalog_number":"300",
      "title":"Studio Practice"
    },
    {
      "course_id":"013506",
      "subject":"FINE",
      "catalog_number":"301",
      "title":"Advanced Studio Practice"
    },
    {
      "course_id":"013507",
      "subject":"FINE",
      "catalog_number":"302",
      "title":"Honours Studio\/Art History Research"
    },
    {
      "course_id":"013508",
      "subject":"FINE",
      "catalog_number":"303",
      "title":"Honours Art History Research"
    },
    {
      "course_id":"013509",
      "subject":"FINE",
      "catalog_number":"304",
      "title":"Topics in Studio Practice"
    },
    {
      "course_id":"013510",
      "subject":"FINE",
      "catalog_number":"305",
      "title":"Topics in Art History"
    },
    {
      "course_id":"013511",
      "subject":"FINE",
      "catalog_number":"306",
      "title":"Topics in Film Studies"
    },
    {
      "course_id":"005485",
      "subject":"FINE",
      "catalog_number":"319",
      "title":"Contemporary Art"
    },
    {
      "course_id":"005499",
      "subject":"FINE",
      "catalog_number":"330",
      "title":"Topics Course in Museums, Galleries, Curatorship"
    },
    {
      "course_id":"005500",
      "subject":"FINE",
      "catalog_number":"331",
      "title":"Art of the 18th Century in Europe"
    },
    {
      "course_id":"005501",
      "subject":"FINE",
      "catalog_number":"332",
      "title":"History of Art Academies"
    },
    {
      "course_id":"010103",
      "subject":"FINE",
      "catalog_number":"333",
      "title":"Costume Design"
    },
    {
      "course_id":"004694",
      "subject":"FINE",
      "catalog_number":"335",
      "title":"Design Theory and Practice"
    },
    {
      "course_id":"012204",
      "subject":"FINE",
      "catalog_number":"337",
      "title":"History of Costume"
    },
    {
      "course_id":"007315",
      "subject":"FINE",
      "catalog_number":"338",
      "title":"Philosophy of Art"
    },
    {
      "course_id":"012914",
      "subject":"FINE",
      "catalog_number":"341",
      "title":"Advanced Studies in Greek Art and Architecture"
    },
    {
      "course_id":"012915",
      "subject":"FINE",
      "catalog_number":"342",
      "title":"Advanced Studies in Roman Art and Architecture"
    },
    {
      "course_id":"013514",
      "subject":"FINE",
      "catalog_number":"343",
      "title":"Topics in Fine Arts Experiential Learning"
    },
    {
      "course_id":"013515",
      "subject":"FINE",
      "catalog_number":"344",
      "title":"Fine Arts Internship"
    },
    {
      "course_id":"005509",
      "subject":"FINE",
      "catalog_number":"351",
      "title":"Central and East European Film"
    },
    {
      "course_id":"011606",
      "subject":"FINE",
      "catalog_number":"359",
      "title":"Topics in German Film"
    },
    {
      "course_id":"005516",
      "subject":"FINE",
      "catalog_number":"360",
      "title":"Film and Television 1"
    },
    {
      "course_id":"005517",
      "subject":"FINE",
      "catalog_number":"361",
      "title":"Film and Television 2"
    },
    {
      "course_id":"013634",
      "subject":"FINE",
      "catalog_number":"362",
      "title":"German Film Classics"
    },
    {
      "course_id":"013635",
      "subject":"FINE",
      "catalog_number":"363",
      "title":"German Filmmakers in Hollywood"
    },
    {
      "course_id":"013636",
      "subject":"FINE",
      "catalog_number":"364",
      "title":"German and Russian Film Pioneers"
    },
    {
      "course_id":"011908",
      "subject":"FINE",
      "catalog_number":"365",
      "title":"Film Noir"
    },
    {
      "course_id":"004687",
      "subject":"FINE",
      "catalog_number":"366",
      "title":"Musical Theatre and Musical Film"
    },
    {
      "course_id":"013625",
      "subject":"FINE",
      "catalog_number":"368",
      "title":"International Comics and Animation Film"
    },
    {
      "course_id":"011401",
      "subject":"FINE",
      "catalog_number":"376",
      "title":"American Film"
    },
    {
      "course_id":"011713",
      "subject":"FINE",
      "catalog_number":"377",
      "title":"The New Hollywood"
    },
    {
      "course_id":"010177",
      "subject":"FINE",
      "catalog_number":"378",
      "title":"Women and Film"
    },
    {
      "course_id":"012456",
      "subject":"FINE",
      "catalog_number":"393",
      "title":"Fine Arts Abroad"
    },
    {
      "course_id":"005521",
      "subject":"FINE",
      "catalog_number":"396",
      "title":"Methods in the History of Art"
    },
    {
      "course_id":"013519",
      "subject":"FINE",
      "catalog_number":"402",
      "title":"Directed Study"
    },
    {
      "course_id":"013520",
      "subject":"FINE",
      "catalog_number":"404",
      "title":"Topics in Studio Practice"
    },
    {
      "course_id":"013521",
      "subject":"FINE",
      "catalog_number":"405",
      "title":"Topics in Art History"
    },
    {
      "course_id":"013618",
      "subject":"FINE",
      "catalog_number":"406",
      "title":"Topics in Film Studies"
    },
    {
      "course_id":"005531",
      "subject":"FINE",
      "catalog_number":"470",
      "title":"Senior Seminar in Film Concepts"
    },
    {
      "course_id":"005532",
      "subject":"FINE",
      "catalog_number":"471",
      "title":"Senior Seminar in Film Concepts 2"
    },
    {
      "course_id":"005533",
      "subject":"FINE",
      "catalog_number":"472",
      "title":"Honours Studio Thesis 1"
    },
    {
      "course_id":"005534",
      "subject":"FINE",
      "catalog_number":"473",
      "title":"Honours Studio Thesis 2"
    },
    {
      "course_id":"005535",
      "subject":"FINE",
      "catalog_number":"474",
      "title":"Honours Studio Practicum 1"
    },
    {
      "course_id":"005536",
      "subject":"FINE",
      "catalog_number":"475",
      "title":"Honours Studio Practicum 2"
    },
    {
      "course_id":"005538",
      "subject":"FINE",
      "catalog_number":"490",
      "title":"Honours Film Studies Thesis 1"
    },
    {
      "course_id":"005540",
      "subject":"FINE",
      "catalog_number":"491",
      "title":"Honours Film Studies Thesis 2"
    },
    {
      "course_id":"005539",
      "subject":"FINE",
      "catalog_number":"492",
      "title":"Senior General Film Studies Project"
    },
    {
      "course_id":"012717",
      "subject":"FINE",
      "catalog_number":"493",
      "title":"Senior General Art History Project"
    },
    {
      "course_id":"012616",
      "subject":"FINE",
      "catalog_number":"496",
      "title":"Honours Art History Thesis 1"
    },
    {
      "course_id":"012614",
      "subject":"FINE",
      "catalog_number":"497",
      "title":"Honours Art History Thesis 2"
    },
    {
      "course_id":"011835",
      "subject":"FINE",
      "catalog_number":"670A",
      "title":"Graduate Studio 1 (Part-Time)"
    },
    {
      "course_id":"011836",
      "subject":"FINE",
      "catalog_number":"670B",
      "title":"Graduate Studio 1 (Part-time)"
    },
    {
      "course_id":"011834",
      "subject":"FINE",
      "catalog_number":"671",
      "title":"Graduate Summer Studies 1 (Part-time)"
    },
    {
      "course_id":"011839",
      "subject":"FINE",
      "catalog_number":"672A",
      "title":"Graduate Studio 2 (Part-Time)"
    },
    {
      "course_id":"011840",
      "subject":"FINE",
      "catalog_number":"672B",
      "title":"Graduate Studio 2 (Part-Time)"
    },
    {
      "course_id":"011837",
      "subject":"FINE",
      "catalog_number":"673",
      "title":"Graduate Summer Studio 2 (Part-Time)"
    },
    {
      "course_id":"011838",
      "subject":"FINE",
      "catalog_number":"674",
      "title":"Graduate Studio 3 (Part-time)"
    },
    {
      "course_id":"001237",
      "subject":"FINE",
      "catalog_number":"680",
      "title":"Issues in Contemporary Art 1"
    },
    {
      "course_id":"001238",
      "subject":"FINE",
      "catalog_number":"681",
      "title":"Issues in Contemporary Art 2"
    },
    {
      "course_id":"001239",
      "subject":"FINE",
      "catalog_number":"682",
      "title":"Graduate Senior Seminar 1"
    },
    {
      "course_id":"001240",
      "subject":"FINE",
      "catalog_number":"683",
      "title":"Graduate Senior Seminar 2"
    },
    {
      "course_id":"001241",
      "subject":"FINE",
      "catalog_number":"690",
      "title":"Graduate Studio 1"
    },
    {
      "course_id":"001242",
      "subject":"FINE",
      "catalog_number":"691",
      "title":"Graduate Studio 2"
    },
    {
      "course_id":"001243",
      "subject":"FINE",
      "catalog_number":"692",
      "title":"Graduate Summer Studio"
    },
    {
      "course_id":"010614",
      "subject":"FINE",
      "catalog_number":"694",
      "title":"Special Topics in Art History and Criticism"
    },
    {
      "course_id":"010615",
      "subject":"FINE",
      "catalog_number":"695",
      "title":"Selected Subjects in Studio Art"
    },
    {
      "course_id":"014526",
      "subject":"FR",
      "catalog_number":"101",
      "title":"Beginner French"
    },
    {
      "course_id":"005547",
      "subject":"FR",
      "catalog_number":"151",
      "title":"Basic French 1"
    },
    {
      "course_id":"005548",
      "subject":"FR",
      "catalog_number":"152",
      "title":"Basic French 2"
    },
    {
      "course_id":"005551",
      "subject":"FR",
      "catalog_number":"192A",
      "title":"French Language 1: Module 1"
    },
    {
      "course_id":"005552",
      "subject":"FR",
      "catalog_number":"192B",
      "title":"French Language 1: Module 2"
    },
    {
      "course_id":"011615",
      "subject":"FR",
      "catalog_number":"197",
      "title":"French Culture & Literature: Origins to 1715"
    },
    {
      "course_id":"005565",
      "subject":"FR",
      "catalog_number":"203",
      "title":"Introduction to Phonetics of French"
    },
    {
      "course_id":"005579",
      "subject":"FR",
      "catalog_number":"250A",
      "title":"Intermediate Spoken French"
    },
    {
      "course_id":"005580",
      "subject":"FR",
      "catalog_number":"251",
      "title":"French Language 2: Module 1"
    },
    {
      "course_id":"005582",
      "subject":"FR",
      "catalog_number":"252",
      "title":"French Language 2: Module 2"
    },
    {
      "course_id":"005586",
      "subject":"FR",
      "catalog_number":"255",
      "title":"Business French I"
    },
    {
      "course_id":"011861",
      "subject":"FR",
      "catalog_number":"263",
      "title":"Major Works 1 - France and la francophonie"
    },
    {
      "course_id":"011860",
      "subject":"FR",
      "catalog_number":"276",
      "title":"Major Works 2 - French Canada"
    },
    {
      "course_id":"005593",
      "subject":"FR",
      "catalog_number":"291",
      "title":"French Civilization 1"
    },
    {
      "course_id":"005594",
      "subject":"FR",
      "catalog_number":"292",
      "title":"French Civilization 2"
    },
    {
      "course_id":"011616",
      "subject":"FR",
      "catalog_number":"297",
      "title":"French Culture & Literature: 1715 to the Present"
    },
    {
      "course_id":"005597",
      "subject":"FR",
      "catalog_number":"300A",
      "title":"Advanced Spoken French"
    },
    {
      "course_id":"005601",
      "subject":"FR",
      "catalog_number":"303",
      "title":"Introduction to Linguistics"
    },
    {
      "course_id":"005605",
      "subject":"FR",
      "catalog_number":"332",
      "title":"17th-Century French Literature"
    },
    {
      "course_id":"005606",
      "subject":"FR",
      "catalog_number":"332A",
      "title":"17th-Century French Literature"
    },
    {
      "course_id":"005607",
      "subject":"FR",
      "catalog_number":"332B",
      "title":"17th-Century French Literature"
    },
    {
      "course_id":"005609",
      "subject":"FR",
      "catalog_number":"343",
      "title":"18th-Century French Literature"
    },
    {
      "course_id":"005610",
      "subject":"FR",
      "catalog_number":"343A",
      "title":"18th-Century French Literature"
    },
    {
      "course_id":"005611",
      "subject":"FR",
      "catalog_number":"343B",
      "title":"18th-Century French Literature"
    },
    {
      "course_id":"005613",
      "subject":"FR",
      "catalog_number":"351",
      "title":"French Language 3"
    },
    {
      "course_id":"012991",
      "subject":"FR",
      "catalog_number":"353",
      "title":"Introduction to Translation"
    },
    {
      "course_id":"005616",
      "subject":"FR",
      "catalog_number":"354",
      "title":"19th-Century French Literature"
    },
    {
      "course_id":"005617",
      "subject":"FR",
      "catalog_number":"354A",
      "title":"19th-Century French Literature"
    },
    {
      "course_id":"005618",
      "subject":"FR",
      "catalog_number":"354B",
      "title":"19th-Century French Literature"
    },
    {
      "course_id":"014222",
      "subject":"FR",
      "catalog_number":"355",
      "title":"Business French II"
    },
    {
      "course_id":"005619",
      "subject":"FR",
      "catalog_number":"363",
      "title":"20th-Century French Literature"
    },
    {
      "course_id":"005620",
      "subject":"FR",
      "catalog_number":"363A",
      "title":"20th-Century French Literature"
    },
    {
      "course_id":"005621",
      "subject":"FR",
      "catalog_number":"363B",
      "title":"20th-Century French Literature"
    },
    {
      "course_id":"013006",
      "subject":"FR",
      "catalog_number":"365",
      "title":"20th-Century French Theatre"
    },
    {
      "course_id":"013107",
      "subject":"FR",
      "catalog_number":"367",
      "title":"21st-Century French Literature"
    },
    {
      "course_id":"012936",
      "subject":"FR",
      "catalog_number":"373",
      "title":"Languages in Contact: The History of French-English Bilingualism"
    },
    {
      "course_id":"005625",
      "subject":"FR",
      "catalog_number":"375",
      "title":"Contemporary French-Canadian Novel"
    },
    {
      "course_id":"014374",
      "subject":"FR",
      "catalog_number":"392A",
      "title":"French Language Practice"
    },
    {
      "course_id":"014375",
      "subject":"FR",
      "catalog_number":"392B",
      "title":"French Language Practice"
    },
    {
      "course_id":"005630",
      "subject":"FR",
      "catalog_number":"393A",
      "title":"French Civilization, 20th-Century French History"
    },
    {
      "course_id":"005631",
      "subject":"FR",
      "catalog_number":"393B",
      "title":"French Civilization, 20th-Century French History"
    },
    {
      "course_id":"005632",
      "subject":"FR",
      "catalog_number":"395A",
      "title":"French Thought"
    },
    {
      "course_id":"005633",
      "subject":"FR",
      "catalog_number":"395B",
      "title":"French Thought"
    },
    {
      "course_id":"005634",
      "subject":"FR",
      "catalog_number":"399A",
      "title":"Independent Cultural Study"
    },
    {
      "course_id":"005635",
      "subject":"FR",
      "catalog_number":"400",
      "title":"Advanced Translation"
    },
    {
      "course_id":"005640",
      "subject":"FR",
      "catalog_number":"403",
      "title":"Topics in Linguistics"
    },
    {
      "course_id":"005641",
      "subject":"FR",
      "catalog_number":"409",
      "title":"Medieval French Language"
    },
    {
      "course_id":"005642",
      "subject":"FR",
      "catalog_number":"410",
      "title":"Medieval French Literature"
    },
    {
      "course_id":"005648",
      "subject":"FR",
      "catalog_number":"424",
      "title":"16th-Century French Literature"
    },
    {
      "course_id":"010202",
      "subject":"FR",
      "catalog_number":"424A",
      "title":"16th-Century French Literature"
    },
    {
      "course_id":"010203",
      "subject":"FR",
      "catalog_number":"424B",
      "title":"16th-Century French Literature"
    },
    {
      "course_id":"005651",
      "subject":"FR",
      "catalog_number":"452",
      "title":"Advanced French Language"
    },
    {
      "course_id":"005652",
      "subject":"FR",
      "catalog_number":"471",
      "title":"French-Canadian Literature"
    },
    {
      "course_id":"005653",
      "subject":"FR",
      "catalog_number":"473",
      "title":"Aspects of French Canada"
    },
    {
      "course_id":"005655",
      "subject":"FR",
      "catalog_number":"482",
      "title":"Study of Individual Authors"
    },
    {
      "course_id":"005656",
      "subject":"FR",
      "catalog_number":"483",
      "title":"Introduction to Literary Theory"
    },
    {
      "course_id":"005657",
      "subject":"FR",
      "catalog_number":"484",
      "title":"Children's Literature in French"
    },
    {
      "course_id":"005658",
      "subject":"FR",
      "catalog_number":"485",
      "title":"French Women Writers"
    },
    {
      "course_id":"011862",
      "subject":"FR",
      "catalog_number":"486",
      "title":"Topics in French Cultural Studies"
    },
    {
      "course_id":"005660",
      "subject":"FR",
      "catalog_number":"487",
      "title":"African and Caribbean French Literature"
    },
    {
      "course_id":"013007",
      "subject":"FR",
      "catalog_number":"488",
      "title":"Francophone Literature and Psychoanalytic Theory"
    },
    {
      "course_id":"005661",
      "subject":"FR",
      "catalog_number":"490",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005662",
      "subject":"FR",
      "catalog_number":"491",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005663",
      "subject":"FR",
      "catalog_number":"492",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005664",
      "subject":"FR",
      "catalog_number":"493",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005665",
      "subject":"FR",
      "catalog_number":"494",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"012848",
      "subject":"FR",
      "catalog_number":"600",
      "title":"Research Methods and Professional Communication in French Studies"
    },
    {
      "course_id":"001253",
      "subject":"FR",
      "catalog_number":"601",
      "title":"Language"
    },
    {
      "course_id":"001254",
      "subject":"FR",
      "catalog_number":"603",
      "title":"Linguistics"
    },
    {
      "course_id":"010492",
      "subject":"FR",
      "catalog_number":"611",
      "title":"Old French Language & Literature"
    },
    {
      "course_id":"010493",
      "subject":"FR",
      "catalog_number":"621",
      "title":"Renaissance Literature"
    },
    {
      "course_id":"010494",
      "subject":"FR",
      "catalog_number":"631",
      "title":"17th-Century Literature"
    },
    {
      "course_id":"001278",
      "subject":"FR",
      "catalog_number":"641",
      "title":"18th-Century Literature"
    },
    {
      "course_id":"010495",
      "subject":"FR",
      "catalog_number":"651",
      "title":"19th-Century Literature"
    },
    {
      "course_id":"010496",
      "subject":"FR",
      "catalog_number":"661",
      "title":"20th-Century Literature"
    },
    {
      "course_id":"001301",
      "subject":"FR",
      "catalog_number":"671",
      "title":"French-Canadian Literature"
    },
    {
      "course_id":"001313",
      "subject":"FR",
      "catalog_number":"681",
      "title":"Critical Methods - Theory of Literature"
    },
    {
      "course_id":"010497",
      "subject":"FR",
      "catalog_number":"685",
      "title":"Studies in Selected Topics"
    },
    {
      "course_id":"001326",
      "subject":"FR",
      "catalog_number":"687",
      "title":"Topics in North African Literature"
    },
    {
      "course_id":"013255",
      "subject":"GBDA",
      "catalog_number":"101",
      "title":"Digital Media Design and Production"
    },
    {
      "course_id":"013256",
      "subject":"GBDA",
      "catalog_number":"102",
      "title":"International Business and Cross-Cultural Management"
    },
    {
      "course_id":"014117",
      "subject":"GBDA",
      "catalog_number":"103",
      "title":"User Experience Design"
    },
    {
      "course_id":"013257",
      "subject":"GBDA",
      "catalog_number":"201",
      "title":"Digital Media Project 1"
    },
    {
      "course_id":"013258",
      "subject":"GBDA",
      "catalog_number":"202",
      "title":"Digital Media Project 2"
    },
    {
      "course_id":"013259",
      "subject":"GBDA",
      "catalog_number":"203",
      "title":"Introduction to Digital Culture"
    },
    {
      "course_id":"013273",
      "subject":"GBDA",
      "catalog_number":"204",
      "title":"Applied Leadership and Management"
    },
    {
      "course_id":"013260",
      "subject":"GBDA",
      "catalog_number":"205",
      "title":"Quantitative Methods"
    },
    {
      "course_id":"005452",
      "subject":"GBDA",
      "catalog_number":"228",
      "title":"Digital Imaging"
    },
    {
      "course_id":"005456",
      "subject":"GBDA",
      "catalog_number":"229",
      "title":"Hybrid Digital Media"
    },
    {
      "course_id":"013261",
      "subject":"GBDA",
      "catalog_number":"301",
      "title":"Global Digital Project 1"
    },
    {
      "course_id":"013262",
      "subject":"GBDA",
      "catalog_number":"302",
      "title":"Global Digital Project 2"
    },
    {
      "course_id":"013263",
      "subject":"GBDA",
      "catalog_number":"303",
      "title":"Innovation, Project and Change Management"
    },
    {
      "course_id":"014240",
      "subject":"GBDA",
      "catalog_number":"304",
      "title":"Marketing in the Digital World"
    },
    {
      "course_id":"013265",
      "subject":"GBDA",
      "catalog_number":"305",
      "title":"Global Development and Business"
    },
    {
      "course_id":"013266",
      "subject":"GBDA",
      "catalog_number":"306",
      "title":"Comparative Ethics in a Globalized World"
    },
    {
      "course_id":"014250",
      "subject":"GBDA",
      "catalog_number":"365",
      "title":"Study Abroad"
    },
    {
      "course_id":"013269",
      "subject":"GBDA",
      "catalog_number":"401",
      "title":"Cross-Cultural Digital Business 1"
    },
    {
      "course_id":"013270",
      "subject":"GBDA",
      "catalog_number":"402",
      "title":"Cross-Cultural Digital Business 2"
    },
    {
      "course_id":"013271",
      "subject":"GBDA",
      "catalog_number":"403",
      "title":"Extended E-portfolio 1"
    },
    {
      "course_id":"013272",
      "subject":"GBDA",
      "catalog_number":"404",
      "title":"Extended E-Portfolio 2"
    },
    {
      "course_id":"014251",
      "subject":"GBDA",
      "catalog_number":"465",
      "title":"Study Abroad"
    },
    {
      "course_id":"010625",
      "subject":"GEMCC",
      "catalog_number":"601",
      "title":"Climate Change: Physical Science Basis"
    },
    {
      "course_id":"009423",
      "subject":"GEMCC",
      "catalog_number":"602",
      "title":"Climate Change Vulnerability and Adaptation"
    },
    {
      "course_id":"014507",
      "subject":"GEMCC",
      "catalog_number":"603",
      "title":"Climate Change Mitigation"
    },
    {
      "course_id":"014506",
      "subject":"GEMCC",
      "catalog_number":"610",
      "title":"Climate Prediction, Modeling and Scenarios"
    },
    {
      "course_id":"014508",
      "subject":"GEMCC",
      "catalog_number":"620",
      "title":"Climate and Society"
    },
    {
      "course_id":"014502",
      "subject":"GEMCC",
      "catalog_number":"621",
      "title":"Advanced Climate Change Adaptation"
    },
    {
      "course_id":"014509",
      "subject":"GEMCC",
      "catalog_number":"622",
      "title":"Climate Change, Natural Hazards and Disaster Risk Reduction"
    },
    {
      "course_id":"014510",
      "subject":"GEMCC",
      "catalog_number":"630",
      "title":"Land Use and the Carbon Cycle"
    },
    {
      "course_id":"014511",
      "subject":"GEMCC",
      "catalog_number":"640",
      "title":"Climate Policy, Law and Institutions"
    },
    {
      "course_id":"014504",
      "subject":"GEMCC",
      "catalog_number":"642",
      "title":"Climate Compatible Development"
    },
    {
      "course_id":"012565",
      "subject":"GENE",
      "catalog_number":"21A",
      "title":"Topics for Technical Courses Taken on Exchange by Architecture Students"
    },
    {
      "course_id":"011799",
      "subject":"GENE",
      "catalog_number":"21C",
      "title":"Topics for Technical Courses Taken on Exchange by Chemical Engineering Students"
    },
    {
      "course_id":"011807",
      "subject":"GENE",
      "catalog_number":"21D",
      "title":"Topics for Technical Courses Taken on Exchange by Systems Design Engineering Students"
    },
    {
      "course_id":"011802",
      "subject":"GENE",
      "catalog_number":"21E",
      "title":"Topics for Technical Courses Taken on Exchange by Electrical Engineering Students"
    },
    {
      "course_id":"011803",
      "subject":"GENE",
      "catalog_number":"21I",
      "title":"Topics for Technical Courses Taken on Exchange by Environmental Engineering Students"
    },
    {
      "course_id":"011800",
      "subject":"GENE",
      "catalog_number":"21K",
      "title":"Topics for Technical Courses Taken on Exchange by Civil Engineering Students"
    },
    {
      "course_id":"011804",
      "subject":"GENE",
      "catalog_number":"21L",
      "title":"Topics for Technical Courses Taken on Exchange by Geological Engineering Students"
    },
    {
      "course_id":"011805",
      "subject":"GENE",
      "catalog_number":"21M",
      "title":"Topics for Technical Courses Taken on Exchange by Mechanical Engineering Students"
    },
    {
      "course_id":"011801",
      "subject":"GENE",
      "catalog_number":"21Q",
      "title":"Topics for Technical Courses Taken on Exchange by Computer Engineering Students"
    },
    {
      "course_id":"011808",
      "subject":"GENE",
      "catalog_number":"21S",
      "title":"Topics for Technical Courses Taken on Exchange by Software Engineering Students"
    },
    {
      "course_id":"011806",
      "subject":"GENE",
      "catalog_number":"21T",
      "title":"Topics for Technical Courses Taken on Exchange by Mechatronics Engineering Students"
    },
    {
      "course_id":"011809",
      "subject":"GENE",
      "catalog_number":"22A",
      "title":"Topics for List A Complementary Studies Courses Taken on Exchange by Engineering Students"
    },
    {
      "course_id":"011810",
      "subject":"GENE",
      "catalog_number":"22B",
      "title":"Topics for List B Complementary Studies Courses Taken on Exchange by Engineering Students"
    },
    {
      "course_id":"011811",
      "subject":"GENE",
      "catalog_number":"22C",
      "title":"Topics for List C Complementary Studies Courses Taken on Exchange by Engineering Students"
    },
    {
      "course_id":"011812",
      "subject":"GENE",
      "catalog_number":"22D",
      "title":"Topics for List D Complementary Studies Courses Taken on Exchange by Engineering Students"
    },
    {
      "course_id":"014367",
      "subject":"GENE",
      "catalog_number":"101",
      "title":"Strategies and Skills for Academic Success"
    },
    {
      "course_id":"009263",
      "subject":"GENE",
      "catalog_number":"119",
      "title":"Problems Seminar"
    },
    {
      "course_id":"005779",
      "subject":"GENE",
      "catalog_number":"121",
      "title":"Digital Computation"
    },
    {
      "course_id":"005780",
      "subject":"GENE",
      "catalog_number":"123",
      "title":"Electrical Engineering"
    },
    {
      "course_id":"005831",
      "subject":"GEOG",
      "catalog_number":"165",
      "title":"Computer Cartography: Principles and Design"
    },
    {
      "course_id":"013772",
      "subject":"GENE",
      "catalog_number":"199",
      "title":"Special Topics in First Year Engineering"
    },
    {
      "course_id":"013773",
      "subject":"GENE",
      "catalog_number":"299",
      "title":"Special Topics in Second Year Engineering"
    },
    {
      "course_id":"005786",
      "subject":"GENE",
      "catalog_number":"301",
      "title":"Special Directed Studies"
    },
    {
      "course_id":"005787",
      "subject":"GENE",
      "catalog_number":"302",
      "title":"Special Directed Studies"
    },
    {
      "course_id":"005788",
      "subject":"GENE",
      "catalog_number":"303",
      "title":"International Studies In Engineering"
    },
    {
      "course_id":"005789",
      "subject":"GENE",
      "catalog_number":"315",
      "title":"Special Directed Non-Technical Studies"
    },
    {
      "course_id":"010162",
      "subject":"GENE",
      "catalog_number":"395",
      "title":"Engineering Study Abroad"
    },
    {
      "course_id":"010163",
      "subject":"GENE",
      "catalog_number":"396",
      "title":"Engineering Study Abroad"
    },
    {
      "course_id":"010022",
      "subject":"GENE",
      "catalog_number":"397",
      "title":"Engineering Study Abroad"
    },
    {
      "course_id":"013774",
      "subject":"GENE",
      "catalog_number":"399",
      "title":"Special Topics in Third Year Engineering"
    },
    {
      "course_id":"005807",
      "subject":"GENE",
      "catalog_number":"401",
      "title":"Special Directed Studies"
    },
    {
      "course_id":"005809",
      "subject":"GENE",
      "catalog_number":"402",
      "title":"Special Directed Studies"
    },
    {
      "course_id":"014282",
      "subject":"GENE",
      "catalog_number":"403",
      "title":"Interdisciplinary Design Project 1"
    },
    {
      "course_id":"014283",
      "subject":"GENE",
      "catalog_number":"404",
      "title":"Interdisciplinary Design Project 2"
    },
    {
      "course_id":"005810",
      "subject":"GENE",
      "catalog_number":"411",
      "title":"Engineering Law and Ethics"
    },
    {
      "course_id":"005811",
      "subject":"GENE",
      "catalog_number":"412",
      "title":"Ethics and The Engineering Profession"
    },
    {
      "course_id":"005812",
      "subject":"GENE",
      "catalog_number":"415",
      "title":"Special Directed Non-Technical Studies"
    },
    {
      "course_id":"013775",
      "subject":"GENE",
      "catalog_number":"499",
      "title":"Special Topics in Fourth Year Engineering"
    },
    {
      "course_id":"005816",
      "subject":"GENE",
      "catalog_number":"501",
      "title":"Directed Studies for Visiting Exchange Students"
    },
    {
      "course_id":"005817",
      "subject":"GENE",
      "catalog_number":"502",
      "title":"Directed Studies for Visiting Exchange Students"
    },
    {
      "course_id":"005818",
      "subject":"GENE",
      "catalog_number":"503",
      "title":"Directed Studies for Visiting Exchange Students"
    },
    {
      "course_id":"011496",
      "subject":"GEOE",
      "catalog_number":"153",
      "title":"Earth Engineering"
    },
    {
      "course_id":"009264",
      "subject":"GEOE",
      "catalog_number":"298",
      "title":"Seminar"
    },
    {
      "course_id":"009265",
      "subject":"GEOE",
      "catalog_number":"299",
      "title":"Seminar"
    },
    {
      "course_id":"009266",
      "subject":"GEOE",
      "catalog_number":"398",
      "title":"Seminar"
    },
    {
      "course_id":"009267",
      "subject":"GEOE",
      "catalog_number":"399",
      "title":"Seminar"
    },
    {
      "course_id":"005820",
      "subject":"GEOE",
      "catalog_number":"400",
      "title":"Geological Engineering Design Project 1"
    },
    {
      "course_id":"005821",
      "subject":"GEOE",
      "catalog_number":"401",
      "title":"Geological Engineering Design Project 2"
    },
    {
      "course_id":"009268",
      "subject":"GEOE",
      "catalog_number":"498",
      "title":"Seminar"
    },
    {
      "course_id":"009269",
      "subject":"GEOE",
      "catalog_number":"499",
      "title":"Seminar"
    },
    {
      "course_id":"011981",
      "subject":"GEOG",
      "catalog_number":"100",
      "title":"On Becoming a Geographer"
    },
    {
      "course_id":"005823",
      "subject":"GEOG",
      "catalog_number":"101",
      "title":"Geography and Human Habitat"
    },
    {
      "course_id":"005824",
      "subject":"GEOG",
      "catalog_number":"102",
      "title":"Geography and Our Planetary Environment"
    },
    {
      "course_id":"014542",
      "subject":"GEOG",
      "catalog_number":"181",
      "title":"Principles of GIScience"
    },
    {
      "course_id":"014543",
      "subject":"GEOG",
      "catalog_number":"187",
      "title":"Problem Solving in Geomatics"
    },
    {
      "course_id":"005834",
      "subject":"GEOG",
      "catalog_number":"201",
      "title":"Fluvial Geomorphology"
    },
    {
      "course_id":"005839",
      "subject":"GEOG",
      "catalog_number":"202",
      "title":"Geography of the Global Economy"
    },
    {
      "course_id":"011140",
      "subject":"GEOG",
      "catalog_number":"203",
      "title":"Environment and Development in a Global Perspective"
    },
    {
      "course_id":"013045",
      "subject":"GEOG",
      "catalog_number":"209",
      "title":"Hydroclimatology"
    },
    {
      "course_id":"005999",
      "subject":"GEOG",
      "catalog_number":"212",
      "title":"Japan and the Pacific Rim"
    },
    {
      "course_id":"012608",
      "subject":"GEOG",
      "catalog_number":"215",
      "title":"China: Diverse and Dynamic"
    },
    {
      "course_id":"005911",
      "subject":"GEOG",
      "catalog_number":"222",
      "title":"Geographical Study of Canada"
    },
    {
      "course_id":"011097",
      "subject":"GEOG",
      "catalog_number":"233",
      "title":"Geography of Tourism"
    },
    {
      "course_id":"005932",
      "subject":"GEOG",
      "catalog_number":"250",
      "title":"Urban and Economic Systems: Inter-City and Global Connections"
    },
    {
      "course_id":"012605",
      "subject":"GEOG",
      "catalog_number":"271",
      "title":"Earth from Space Using Remote Sensing"
    },
    {
      "course_id":"007509",
      "subject":"GEOG",
      "catalog_number":"281",
      "title":"Introduction to Geographic Information Systems (GIS)"
    },
    {
      "course_id":"005982",
      "subject":"GEOG",
      "catalog_number":"293",
      "title":"Professional and Scholarly Practice in Geography"
    },
    {
      "course_id":"012888",
      "subject":"GEOG",
      "catalog_number":"294",
      "title":"Approaches to Research in Physical Geography"
    },
    {
      "course_id":"005895",
      "subject":"GEOG",
      "catalog_number":"300",
      "title":"Geomorphology and the Southern Ontario Environment"
    },
    {
      "course_id":"005898",
      "subject":"GEOG",
      "catalog_number":"303",
      "title":"Physical Hydrology"
    },
    {
      "course_id":"012402",
      "subject":"GEOG",
      "catalog_number":"306",
      "title":"Human Dimensions of Natural Hazards"
    },
    {
      "course_id":"005846",
      "subject":"GEOG",
      "catalog_number":"308",
      "title":"Human Dimensions of Global Climate Change"
    },
    {
      "course_id":"005902",
      "subject":"GEOG",
      "catalog_number":"309",
      "title":"Physical Climatology"
    },
    {
      "course_id":"012606",
      "subject":"GEOG",
      "catalog_number":"310",
      "title":"Geodesy and Surveying"
    },
    {
      "course_id":"013018",
      "subject":"GEOG",
      "catalog_number":"311",
      "title":"Local Development in a Global Context"
    },
    {
      "course_id":"005905",
      "subject":"GEOG",
      "catalog_number":"316",
      "title":"Multivariate Statistics"
    },
    {
      "course_id":"005908",
      "subject":"GEOG",
      "catalog_number":"318",
      "title":"Spatial Analysis"
    },
    {
      "course_id":"005909",
      "subject":"GEOG",
      "catalog_number":"319",
      "title":"Economic Analyses for Regional Planning"
    },
    {
      "course_id":"005912",
      "subject":"GEOG",
      "catalog_number":"323",
      "title":"Perspectives on International Tourism"
    },
    {
      "course_id":"005919",
      "subject":"GEOG",
      "catalog_number":"333",
      "title":"Recreation Geography"
    },
    {
      "course_id":"005924",
      "subject":"GEOG",
      "catalog_number":"340",
      "title":"Settlements of Rural Canada"
    },
    {
      "course_id":"007561",
      "subject":"GEOG",
      "catalog_number":"349",
      "title":"Urban Form and Internal Spatial Structure"
    },
    {
      "course_id":"005934",
      "subject":"GEOG",
      "catalog_number":"351",
      "title":"Geography of Transportation"
    },
    {
      "course_id":"005945",
      "subject":"GEOG",
      "catalog_number":"356",
      "title":"Resources Management"
    },
    {
      "course_id":"007559",
      "subject":"GEOG",
      "catalog_number":"368",
      "title":"Conservation\/Resource Management of the Built Environment"
    },
    {
      "course_id":"012607",
      "subject":"GEOG",
      "catalog_number":"371",
      "title":"Advanced Remote Sensing Techniques"
    },
    {
      "course_id":"006014",
      "subject":"GEOG",
      "catalog_number":"381",
      "title":"Advanced Geographic Information Systems"
    },
    {
      "course_id":"005943",
      "subject":"GEOG",
      "catalog_number":"387",
      "title":"Spatial Databases"
    },
    {
      "course_id":"005978",
      "subject":"GEOG",
      "catalog_number":"391",
      "title":"Field Research"
    },
    {
      "course_id":"012719",
      "subject":"GEOG",
      "catalog_number":"404",
      "title":"Soil Ecosystem Dynamics"
    },
    {
      "course_id":"005992",
      "subject":"GEOG",
      "catalog_number":"405",
      "title":"Wetlands"
    },
    {
      "course_id":"005994",
      "subject":"GEOG",
      "catalog_number":"407",
      "title":"Environmental Hydrology"
    },
    {
      "course_id":"014541",
      "subject":"GEOG",
      "catalog_number":"408",
      "title":"Modeling our Future Climate"
    },
    {
      "course_id":"005996",
      "subject":"GEOG",
      "catalog_number":"409",
      "title":"Energy Balance Climatology"
    },
    {
      "course_id":"014106",
      "subject":"GEOG",
      "catalog_number":"410",
      "title":"Global Navigation Satellite Systems"
    },
    {
      "course_id":"005998",
      "subject":"GEOG",
      "catalog_number":"411",
      "title":"Global and Local Dimensions of Industrial Restructuring"
    },
    {
      "course_id":"014544",
      "subject":"GEOG",
      "catalog_number":"418",
      "title":"The Arctic Climate System"
    },
    {
      "course_id":"014545",
      "subject":"GEOG",
      "catalog_number":"419",
      "title":"The Cryosphere"
    },
    {
      "course_id":"011098",
      "subject":"GEOG",
      "catalog_number":"423",
      "title":"Tourism Lecture Series"
    },
    {
      "course_id":"006007",
      "subject":"GEOG",
      "catalog_number":"426",
      "title":"Geographies of Development"
    },
    {
      "course_id":"006008",
      "subject":"GEOG",
      "catalog_number":"430A",
      "title":"Field Research in Regional Geography"
    },
    {
      "course_id":"006009",
      "subject":"GEOG",
      "catalog_number":"430B",
      "title":"Field Research in Regional Geography"
    },
    {
      "course_id":"006010",
      "subject":"GEOG",
      "catalog_number":"430C",
      "title":"Field Research in Regional Geography"
    },
    {
      "course_id":"006442",
      "subject":"GEOG",
      "catalog_number":"432",
      "title":"Health, Environment, and Planning"
    },
    {
      "course_id":"006011",
      "subject":"GEOG",
      "catalog_number":"450",
      "title":"Changing Form and Structure of Metropolitan Canada"
    },
    {
      "course_id":"010134",
      "subject":"GEOG",
      "catalog_number":"452",
      "title":"Resource Management Project"
    },
    {
      "course_id":"011527",
      "subject":"GEOG",
      "catalog_number":"453",
      "title":"Urban Stormwater Management"
    },
    {
      "course_id":"014546",
      "subject":"GEOG",
      "catalog_number":"454",
      "title":"Retail Landscapes"
    },
    {
      "course_id":"006015",
      "subject":"GEOG",
      "catalog_number":"459",
      "title":"Energy and Sustainability"
    },
    {
      "course_id":"013956",
      "subject":"GEOG",
      "catalog_number":"461",
      "title":"Food Systems and Sustainability"
    },
    {
      "course_id":"013955",
      "subject":"GEOG",
      "catalog_number":"462",
      "title":"Global Food and Agricultural Politics"
    },
    {
      "course_id":"006019",
      "subject":"GEOG",
      "catalog_number":"471",
      "title":"Remote Sensing Project"
    },
    {
      "course_id":"009503",
      "subject":"GEOG",
      "catalog_number":"474",
      "title":"Special Topics in Geography"
    },
    {
      "course_id":"009506",
      "subject":"GEOG",
      "catalog_number":"475",
      "title":"Independent Study of Selected Topics"
    },
    {
      "course_id":"009505",
      "subject":"GEOG",
      "catalog_number":"481",
      "title":"Geographic Information Systems Project"
    },
    {
      "course_id":"014547",
      "subject":"GEOG",
      "catalog_number":"483",
      "title":"Geoweb and Location-Based Services"
    },
    {
      "course_id":"009498",
      "subject":"GEOG",
      "catalog_number":"487",
      "title":"Management Issues in Geographic Information Systems"
    },
    {
      "course_id":"006045",
      "subject":"GEOG",
      "catalog_number":"490A",
      "title":"Honours Thesis Preparation"
    },
    {
      "course_id":"006046",
      "subject":"GEOG",
      "catalog_number":"490B",
      "title":"Honours Thesis Completion"
    },
    {
      "course_id":"001344",
      "subject":"GEOG",
      "catalog_number":"600",
      "title":"Seminar in Spatial Data Handling"
    },
    {
      "course_id":"009416",
      "subject":"GEOG",
      "catalog_number":"601",
      "title":"Environmental Change and Remote"
    },
    {
      "course_id":"001345",
      "subject":"GEOG",
      "catalog_number":"602",
      "title":"Remote Sensing of Cold Regions"
    },
    {
      "course_id":"001346",
      "subject":"GEOG",
      "catalog_number":"603",
      "title":"Remote Sensing and Earth System Science"
    },
    {
      "course_id":"001347",
      "subject":"GEOG",
      "catalog_number":"604",
      "title":"Spatial Statistics"
    },
    {
      "course_id":"011818",
      "subject":"GEOG",
      "catalog_number":"605",
      "title":"Spatial Information Technology, Globalization and International Development"
    },
    {
      "course_id":"001348",
      "subject":"GEOG",
      "catalog_number":"606",
      "title":"Introduction to Geographic Information Systems"
    },
    {
      "course_id":"001349",
      "subject":"GEOG",
      "catalog_number":"607",
      "title":"Applications of Geographic Information Systems"
    },
    {
      "course_id":"012793",
      "subject":"GEOG",
      "catalog_number":"608",
      "title":"Urban Remote Sensing"
    },
    {
      "course_id":"011491",
      "subject":"GEOG",
      "catalog_number":"609",
      "title":"GIS and Spatial Decision Support for Planning  and Resource Management"
    },
    {
      "course_id":"001839",
      "subject":"GEOG",
      "catalog_number":"611",
      "title":"Industrial Location Theory and Concepts"
    },
    {
      "course_id":"001841",
      "subject":"GEOG",
      "catalog_number":"613",
      "title":"Regional Development Principles and Practice"
    },
    {
      "course_id":"001842",
      "subject":"GEOG",
      "catalog_number":"615",
      "title":"Community Economic Development"
    },
    {
      "course_id":"001360",
      "subject":"GEOG",
      "catalog_number":"616",
      "title":"Multivariate Statistics"
    },
    {
      "course_id":"002245",
      "subject":"GEOG",
      "catalog_number":"619",
      "title":"Regional Planning Economic and Investment Analysis"
    },
    {
      "course_id":"001364",
      "subject":"GEOG",
      "catalog_number":"620",
      "title":"Seminar in Human Geography"
    },
    {
      "course_id":"010621",
      "subject":"GEOG",
      "catalog_number":"621",
      "title":"Metropolitan Form and Structure in Canada"
    },
    {
      "course_id":"001368",
      "subject":"GEOG",
      "catalog_number":"624",
      "title":"Human Activity and Travel Behaviour"
    },
    {
      "course_id":"010624",
      "subject":"GEOG",
      "catalog_number":"634",
      "title":"Selected Topics in Regional Studies"
    },
    {
      "course_id":"001369",
      "subject":"GEOG",
      "catalog_number":"625",
      "title":"Qualitative Methods in Geography"
    },
    {
      "course_id":"001374",
      "subject":"GEOG",
      "catalog_number":"635",
      "title":"International Development: Theories and Practice"
    },
    {
      "course_id":"013243",
      "subject":"GEOG",
      "catalog_number":"637",
      "title":"Cultural Geography"
    },
    {
      "course_id":"010724",
      "subject":"GEOG",
      "catalog_number":"638",
      "title":"Sustainable Tourism"
    },
    {
      "course_id":"013394",
      "subject":"GEOG",
      "catalog_number":"639",
      "title":"Food Systems and Sustainability"
    },
    {
      "course_id":"001375",
      "subject":"GEOG",
      "catalog_number":"640",
      "title":"Seminar in Physical Geography"
    },
    {
      "course_id":"010625",
      "subject":"GEOG",
      "catalog_number":"641",
      "title":"Climate Change: Physical Science Basis"
    },
    {
      "course_id":"001397",
      "subject":"GEOG",
      "catalog_number":"668",
      "title":"Environmental Assessment"
    },
    {
      "course_id":"001376",
      "subject":"GEOG",
      "catalog_number":"642",
      "title":"Micrometeorology"
    },
    {
      "course_id":"001377",
      "subject":"GEOG",
      "catalog_number":"643",
      "title":"Dynamic Geomorphology"
    },
    {
      "course_id":"001378",
      "subject":"GEOG",
      "catalog_number":"644",
      "title":"Applied Geomorphology"
    },
    {
      "course_id":"009420",
      "subject":"GEOG",
      "catalog_number":"645",
      "title":"Fluvial & Glaciofluvial Sediment Transport"
    },
    {
      "course_id":"001379",
      "subject":"GEOG",
      "catalog_number":"646",
      "title":"Hydrology"
    },
    {
      "course_id":"001380",
      "subject":"GEOG",
      "catalog_number":"647",
      "title":"Recent Advances in Wetland Studies"
    },
    {
      "course_id":"012794",
      "subject":"GEOG",
      "catalog_number":"648",
      "title":"Paleolimnology"
    },
    {
      "course_id":"012795",
      "subject":"GEOG",
      "catalog_number":"649",
      "title":"Hydrology of Cold Regions"
    },
    {
      "course_id":"013757",
      "subject":"GEOG",
      "catalog_number":"651",
      "title":"Hydroecology for Freshwater Ecosystem Management"
    },
    {
      "course_id":"014506",
      "subject":"GEOG",
      "catalog_number":"652",
      "title":"Climate Prediction, Modeling and Scenarios"
    },
    {
      "course_id":"014510",
      "subject":"GEOG",
      "catalog_number":"653",
      "title":"Land Use and the Carbon Cycle"
    },
    {
      "course_id":"001210",
      "subject":"GEOG",
      "catalog_number":"660",
      "title":"Perspectives in Resource and Environmental Management"
    },
    {
      "course_id":"002264",
      "subject":"GEOG",
      "catalog_number":"661A",
      "title":"Applied Studies in Hydrology and the Environment 1"
    },
    {
      "course_id":"001389",
      "subject":"GEOG",
      "catalog_number":"661B",
      "title":"Applied Studies in Hydrology and the Environment 2"
    },
    {
      "course_id":"001392",
      "subject":"GEOG",
      "catalog_number":"664",
      "title":"Political Ecology: Nature, Society and Sustainability"
    },
    {
      "course_id":"002269",
      "subject":"GEOG",
      "catalog_number":"665",
      "title":"Environmental Planning Theory and Practice"
    },
    {
      "course_id":"002270",
      "subject":"GEOG",
      "catalog_number":"666",
      "title":"Ecosystem Approach to Park Planning"
    },
    {
      "course_id":"012666",
      "subject":"GEOG",
      "catalog_number":"669",
      "title":"Energy Sustainability"
    },
    {
      "course_id":"001400",
      "subject":"GEOG",
      "catalog_number":"671",
      "title":"Contemporary Perspectives on Tourism"
    },
    {
      "course_id":"001401",
      "subject":"GEOG",
      "catalog_number":"672",
      "title":"Human Ecology of Stressed Environments"
    },
    {
      "course_id":"001402",
      "subject":"GEOG",
      "catalog_number":"673",
      "title":"International Perspectives on Resource and Environmental Management"
    },
    {
      "course_id":"014508",
      "subject":"GEOG",
      "catalog_number":"674",
      "title":"Climate and Society"
    },
    {
      "course_id":"001403",
      "subject":"GEOG",
      "catalog_number":"675",
      "title":"Selected Topics in Geography"
    },
    {
      "course_id":"013029",
      "subject":"GRK",
      "catalog_number":"632",
      "title":"Local Cultures in Hellenistic Greek Poetry"
    },
    {
      "course_id":"013051",
      "subject":"GRK",
      "catalog_number":"633",
      "title":"Ancient Religions through Epigraphy"
    },
    {
      "course_id":"013052",
      "subject":"GRK",
      "catalog_number":"651",
      "title":"Senior Greek Composition, Grammar and Reading"
    },
    {
      "course_id":"009423",
      "subject":"GEOG",
      "catalog_number":"676",
      "title":"Climate Change Vulnerability and Adaptation"
    },
    {
      "course_id":"014509",
      "subject":"GEOG",
      "catalog_number":"677",
      "title":"Climate Change, Natural Hazards and Disaster Risk Reduction"
    },
    {
      "course_id":"014511",
      "subject":"GEOG",
      "catalog_number":"678",
      "title":"Climate Policy, Law and Institutions"
    },
    {
      "course_id":"014507",
      "subject":"GEOG",
      "catalog_number":"679",
      "title":"Climate Change Mitigation"
    },
    {
      "course_id":"001843",
      "subject":"GEOG",
      "catalog_number":"685",
      "title":"Theory of Local Economic Development"
    },
    {
      "course_id":"001434",
      "subject":"GEOG",
      "catalog_number":"690",
      "title":"Geographic Thought and Methodology"
    },
    {
      "course_id":"001435",
      "subject":"GEOG",
      "catalog_number":"691",
      "title":"Graduate Student and Faculty Seminar in Geography"
    },
    {
      "course_id":"010626",
      "subject":"GEOG",
      "catalog_number":"692",
      "title":"International Study"
    },
    {
      "course_id":"013628",
      "subject":"GER",
      "catalog_number":"100",
      "title":"Zeitgeist and Popular Culture"
    },
    {
      "course_id":"006056",
      "subject":"GER",
      "catalog_number":"101",
      "title":"Elementary German I"
    },
    {
      "course_id":"006057",
      "subject":"GER",
      "catalog_number":"102",
      "title":"Elementary German II"
    },
    {
      "course_id":"013630",
      "subject":"GER",
      "catalog_number":"180",
      "title":"German and Russian Literary Masterpieces"
    },
    {
      "course_id":"006070",
      "subject":"GER",
      "catalog_number":"201",
      "title":"Intermediate German I"
    },
    {
      "course_id":"006072",
      "subject":"GER",
      "catalog_number":"202",
      "title":"Intermediate German II"
    },
    {
      "course_id":"014285",
      "subject":"GER",
      "catalog_number":"211",
      "title":"Integrative Language Seminar I"
    },
    {
      "course_id":"011595",
      "subject":"GER",
      "catalog_number":"212",
      "title":"Integrative Language Seminar II"
    },
    {
      "course_id":"013653",
      "subject":"GER",
      "catalog_number":"220",
      "title":"Once Upon a Fairy Tale: Fairy Tales, Then and Now"
    },
    {
      "course_id":"011596",
      "subject":"GER",
      "catalog_number":"250",
      "title":"Performance German I"
    },
    {
      "course_id":"013008",
      "subject":"GER",
      "catalog_number":"261",
      "title":"Languages and Society I"
    },
    {
      "course_id":"013009",
      "subject":"GER",
      "catalog_number":"262",
      "title":"Languages and Society II"
    },
    {
      "course_id":"006084",
      "subject":"GER",
      "catalog_number":"271",
      "title":"German Thought and Culture: Objects"
    },
    {
      "course_id":"006085",
      "subject":"GER",
      "catalog_number":"272",
      "title":"German Thought and Culture: People"
    },
    {
      "course_id":"013877",
      "subject":"GER",
      "catalog_number":"280",
      "title":"Comparative Literature: Theory and Practice"
    },
    {
      "course_id":"014480",
      "subject":"GER",
      "catalog_number":"298",
      "title":"Topics in Cultural Studies"
    },
    {
      "course_id":"014481",
      "subject":"GER",
      "catalog_number":"299",
      "title":"German Abroad"
    },
    {
      "course_id":"011597",
      "subject":"GER",
      "catalog_number":"303",
      "title":"German Through Media"
    },
    {
      "course_id":"011598",
      "subject":"GER",
      "catalog_number":"304",
      "title":"Reading and Translating"
    },
    {
      "course_id":"013631",
      "subject":"GER",
      "catalog_number":"307",
      "title":"German for Professional Purposes"
    },
    {
      "course_id":"013632",
      "subject":"GER",
      "catalog_number":"308",
      "title":"German through Comics"
    },
    {
      "course_id":"014286",
      "subject":"GER",
      "catalog_number":"309",
      "title":"The Structure of German"
    },
    {
      "course_id":"011599",
      "subject":"GER",
      "catalog_number":"331",
      "title":"Exploring the German Language"
    },
    {
      "course_id":"013633",
      "subject":"GER",
      "catalog_number":"334",
      "title":"Exploring German Literature"
    },
    {
      "course_id":"011602",
      "subject":"GER",
      "catalog_number":"350",
      "title":"Performance German II"
    },
    {
      "course_id":"006112",
      "subject":"GER",
      "catalog_number":"353",
      "title":"Intermediate Conversation and Composition on Topics in German \"Landeskunde\""
    },
    {
      "course_id":"006113",
      "subject":"GER",
      "catalog_number":"354",
      "title":"Intermediate Conversation and Composition on Topics in German \"Landeskunde\""
    },
    {
      "course_id":"011606",
      "subject":"GER",
      "catalog_number":"359",
      "title":"Topics in German Film"
    },
    {
      "course_id":"013634",
      "subject":"GER",
      "catalog_number":"362",
      "title":"German Film Classics"
    },
    {
      "course_id":"013635",
      "subject":"GER",
      "catalog_number":"363",
      "title":"German Filmmakers in Hollywood"
    },
    {
      "course_id":"013636",
      "subject":"GER",
      "catalog_number":"364",
      "title":"German and Russian Film Pioneers"
    },
    {
      "course_id":"012957",
      "subject":"GER",
      "catalog_number":"383",
      "title":"Culture in the Third Reich: Racism, Resistance, Legacy"
    },
    {
      "course_id":"013650",
      "subject":"GER",
      "catalog_number":"385",
      "title":"Culture Behind the Iron Curtain"
    },
    {
      "course_id":"006125",
      "subject":"GER",
      "catalog_number":"395",
      "title":"Waterloo in Germany Program"
    },
    {
      "course_id":"006128",
      "subject":"GER",
      "catalog_number":"396",
      "title":"Waterloo in Germany Program"
    },
    {
      "course_id":"011867",
      "subject":"GER",
      "catalog_number":"397",
      "title":"Waterloo in Germany Program"
    },
    {
      "course_id":"014483",
      "subject":"GER",
      "catalog_number":"398",
      "title":"Topics in Cultural Studies"
    },
    {
      "course_id":"014484",
      "subject":"GER",
      "catalog_number":"399",
      "title":"German Abroad"
    },
    {
      "course_id":"011197",
      "subject":"GER",
      "catalog_number":"407",
      "title":"Applied Apprenticeship"
    },
    {
      "course_id":"012634",
      "subject":"GER",
      "catalog_number":"420",
      "title":"Topics in Language Pedagogy"
    },
    {
      "course_id":"011604",
      "subject":"GER",
      "catalog_number":"431",
      "title":"Senior Seminar"
    },
    {
      "course_id":"006143",
      "subject":"GER",
      "catalog_number":"490",
      "title":"Senior Honours Project"
    },
    {
      "course_id":"006144",
      "subject":"GER",
      "catalog_number":"495",
      "title":"Reading Course in Approved Topics"
    },
    {
      "course_id":"001448",
      "subject":"GER",
      "catalog_number":"600",
      "title":"Methods of Research"
    },
    {
      "course_id":"011669",
      "subject":"GER",
      "catalog_number":"601",
      "title":"Approaches in Linguistics"
    },
    {
      "course_id":"001449",
      "subject":"GER",
      "catalog_number":"602",
      "title":"Approaches in Literary and Cultural Theory"
    },
    {
      "course_id":"001450",
      "subject":"GER",
      "catalog_number":"603",
      "title":"Approaches in Language Didactics"
    },
    {
      "course_id":"011670",
      "subject":"GER",
      "catalog_number":"604",
      "title":"Approaches in Film and Performance Theory"
    },
    {
      "course_id":"010403",
      "subject":"GER",
      "catalog_number":"610",
      "title":"Topics in German Linguistics"
    },
    {
      "course_id":"001451",
      "subject":"GER",
      "catalog_number":"611",
      "title":"Topics in Second Language Acquisition and Computer Assisted Language Learning"
    },
    {
      "course_id":"010405",
      "subject":"GER",
      "catalog_number":"612",
      "title":"Topics in Sociolinguistics"
    },
    {
      "course_id":"013050",
      "subject":"GRK",
      "catalog_number":"631",
      "title":"Oaths and Curses in Mediterranean Culture"
    },
    {
      "course_id":"010404",
      "subject":"GER",
      "catalog_number":"613",
      "title":"Topics in Discourse Analysis"
    },
    {
      "course_id":"010406",
      "subject":"GER",
      "catalog_number":"614",
      "title":"Topics in Linguistic Theory"
    },
    {
      "course_id":"014084",
      "subject":"GER",
      "catalog_number":"615",
      "title":"Topics in Language Education"
    },
    {
      "course_id":"011671",
      "subject":"GER",
      "catalog_number":"620",
      "title":"Topics in German Literature and Culture"
    },
    {
      "course_id":"001464",
      "subject":"GER",
      "catalog_number":"621",
      "title":"Topics in Comparative Literature and Culture"
    },
    {
      "course_id":"010267",
      "subject":"GER",
      "catalog_number":"622",
      "title":"Topics in Film and Electronic Media"
    },
    {
      "course_id":"001465",
      "subject":"GER",
      "catalog_number":"623",
      "title":"Topics in Literature and Cultural Theory"
    },
    {
      "course_id":"001496",
      "subject":"GER",
      "catalog_number":"695",
      "title":"Reading Courses in Approved Topics"
    },
    {
      "course_id":"001448",
      "subject":"GER",
      "catalog_number":"700",
      "title":"Methods of Research"
    },
    {
      "course_id":"011669",
      "subject":"GER",
      "catalog_number":"701",
      "title":"Approaches in Linguistics"
    },
    {
      "course_id":"001449",
      "subject":"GER",
      "catalog_number":"702",
      "title":"Approaches in Literary and Cultural Theory"
    },
    {
      "course_id":"001450",
      "subject":"GER",
      "catalog_number":"703",
      "title":"Approaches in Language Didactics"
    },
    {
      "course_id":"011670",
      "subject":"GER",
      "catalog_number":"704",
      "title":"Approaches in Film and Performance Theory"
    },
    {
      "course_id":"010403",
      "subject":"GER",
      "catalog_number":"710",
      "title":"Topics in German Linguistics"
    },
    {
      "course_id":"001451",
      "subject":"GER",
      "catalog_number":"711",
      "title":"Topics in Second Language Acquisition and Computer Assisted Language Learning"
    },
    {
      "course_id":"010405",
      "subject":"GER",
      "catalog_number":"712",
      "title":"Topics in Sociolinguistics"
    },
    {
      "course_id":"010404",
      "subject":"GER",
      "catalog_number":"713",
      "title":"Topics in Discourse Analysis"
    },
    {
      "course_id":"010406",
      "subject":"GER",
      "catalog_number":"714",
      "title":"Topics in Linguistic Theory"
    },
    {
      "course_id":"014084",
      "subject":"GER",
      "catalog_number":"715",
      "title":"Topics in Language Education"
    },
    {
      "course_id":"011671",
      "subject":"GER",
      "catalog_number":"720",
      "title":"Topics in German Literature and Culture"
    },
    {
      "course_id":"001464",
      "subject":"GER",
      "catalog_number":"721",
      "title":"Topics in Comparative Literature and Culture"
    },
    {
      "course_id":"010267",
      "subject":"GER",
      "catalog_number":"722",
      "title":"Topics in Film and Electronic Media"
    },
    {
      "course_id":"001465",
      "subject":"GER",
      "catalog_number":"723",
      "title":"Topics in Literature and Cultural Theory"
    },
    {
      "course_id":"013937",
      "subject":"GER",
      "catalog_number":"751",
      "title":"Topics in Linguistic Methodology"
    },
    {
      "course_id":"013938",
      "subject":"GER",
      "catalog_number":"752",
      "title":"Topics in Theories and Models of Applied Linguistics"
    },
    {
      "course_id":"013939",
      "subject":"GER",
      "catalog_number":"753",
      "title":"Topics in Theories and Methods of Cultural and Literary Studies"
    },
    {
      "course_id":"013940",
      "subject":"GER",
      "catalog_number":"754",
      "title":"Topics in Theories and Conceptions of Modernity"
    },
    {
      "course_id":"013941",
      "subject":"GER",
      "catalog_number":"761",
      "title":"Topics in Interaction and Text"
    },
    {
      "course_id":"013942",
      "subject":"GER",
      "catalog_number":"762",
      "title":"Topics in Research Directions in Language Acquisition and Multilinualism"
    },
    {
      "course_id":"014793",
      "subject":"HIST",
      "catalog_number":"203",
      "title":"Methods of Applied History"
    },
    {
      "course_id":"013943",
      "subject":"GER",
      "catalog_number":"763",
      "title":"Topics in Sociology of Language and Cultural Differentiation"
    },
    {
      "course_id":"013944",
      "subject":"GER",
      "catalog_number":"764",
      "title":"Topics in History of Language"
    },
    {
      "course_id":"014792",
      "subject":"HIST",
      "catalog_number":"202",
      "title":"Introduction to Applied History"
    },
    {
      "course_id":"013945",
      "subject":"GER",
      "catalog_number":"765",
      "title":"Topics in German Grammar"
    },
    {
      "course_id":"013946",
      "subject":"GER",
      "catalog_number":"771",
      "title":"Topics in Individual and Society in Historical Transformation"
    },
    {
      "course_id":"014940",
      "subject":"Graduate",
      "catalog_number":"Studie",
      "title":"Research"
    },
    {
      "course_id":"013947",
      "subject":"GER",
      "catalog_number":"772",
      "title":"Topics in Aesthetic Transformations and Theoretical Concepts"
    },
    {
      "course_id":"013948",
      "subject":"GER",
      "catalog_number":"773",
      "title":"Topics in Intercultural Perspectives, Post-colonial Consteallations & Transnational Discourses"
    },
    {
      "course_id":"013949",
      "subject":"GER",
      "catalog_number":"774",
      "title":"Topics in German Literature and Culture Before 1700"
    },
    {
      "course_id":"013949",
      "subject":"GER",
      "catalog_number":"774`",
      "title":"German Literature and Culture Before 1700"
    },
    {
      "course_id":"013950",
      "subject":"GER",
      "catalog_number":"775",
      "title":"Topics in Modern German Literature"
    },
    {
      "course_id":"013951",
      "subject":"GER",
      "catalog_number":"780",
      "title":"Topics in Media Studies"
    },
    {
      "course_id":"014736",
      "subject":"GER",
      "catalog_number":"792",
      "title":"Master's Thesis Colloquium"
    },
    {
      "course_id":"014304",
      "subject":"GER",
      "catalog_number":"791",
      "title":"AcademicWriting"
    },
    {
      "course_id":"006420",
      "subject":"GERON",
      "catalog_number":"201",
      "title":"Aging and Health"
    },
    {
      "course_id":"006426",
      "subject":"GERON",
      "catalog_number":"210",
      "title":"Development, Aging and Health"
    },
    {
      "course_id":"006428",
      "subject":"GERON",
      "catalog_number":"218",
      "title":"Psychology of Death and Dying"
    },
    {
      "course_id":"006429",
      "subject":"GERON",
      "catalog_number":"220",
      "title":"Psychosocial Perspectives on Lifespan Development and Health"
    },
    {
      "course_id":"006430",
      "subject":"GERON",
      "catalog_number":"245",
      "title":"The Canadian Health Care System"
    },
    {
      "course_id":"006156",
      "subject":"GERON",
      "catalog_number":"255",
      "title":"The Biology of Aging"
    },
    {
      "course_id":"006438",
      "subject":"GERON",
      "catalog_number":"352",
      "title":"Sociology of Aging"
    },
    {
      "course_id":"013897",
      "subject":"GERON",
      "catalog_number":"355",
      "title":"Biology of Human Aging"
    },
    {
      "course_id":"006440",
      "subject":"GERON",
      "catalog_number":"400",
      "title":"Multidisciplinary Seminar on Aging"
    },
    {
      "course_id":"006160",
      "subject":"GERON",
      "catalog_number":"401A",
      "title":"Independent Study in Aging"
    },
    {
      "course_id":"006161",
      "subject":"GERON",
      "catalog_number":"401B",
      "title":"Independent Study in Aging"
    },
    {
      "course_id":"013675",
      "subject":"GGOV",
      "catalog_number":"600",
      "title":"Global Governance"
    },
    {
      "course_id":"002468",
      "subject":"GGOV",
      "catalog_number":"610",
      "title":"Governance of Global Economy"
    },
    {
      "course_id":"002466",
      "subject":"GGOV",
      "catalog_number":"611",
      "title":"Emerging Economies in Global Governance"
    },
    {
      "course_id":"002419",
      "subject":"GGOV",
      "catalog_number":"612",
      "title":"Theories of Globalization"
    },
    {
      "course_id":"002454",
      "subject":"GGOV",
      "catalog_number":"613",
      "title":"The Politics of National Innovation Systems"
    },
    {
      "course_id":"013687",
      "subject":"GGOV",
      "catalog_number":"614",
      "title":"Global Business and Development"
    },
    {
      "course_id":"014932",
      "subject":"GGOV",
      "catalog_number":"622",
      "title":"Complexity and Global Governance"
    },
    {
      "course_id":"013688",
      "subject":"GGOV",
      "catalog_number":"615",
      "title":"Global Poverty"
    },
    {
      "course_id":"013692",
      "subject":"GGOV",
      "catalog_number":"618",
      "title":"Special Topics in Global Political Economy"
    },
    {
      "course_id":"013697",
      "subject":"GGOV",
      "catalog_number":"619",
      "title":"Readings in Global Political Economy"
    },
    {
      "course_id":"014061",
      "subject":"GLOBAL",
      "catalog_number":"327W",
      "title":"Tourists, Tourism & the Globe (WLU)"
    },
    {
      "course_id":"001205",
      "subject":"GGOV",
      "catalog_number":"620",
      "title":"Advanced Topics in Global Environmental Governance"
    },
    {
      "course_id":"012738",
      "subject":"GGOV",
      "catalog_number":"621",
      "title":"Governing Global Food and Agriculture Systems"
    },
    {
      "course_id":"013693",
      "subject":"GGOV",
      "catalog_number":"628",
      "title":"Topics in Global Environment"
    },
    {
      "course_id":"013698",
      "subject":"GGOV",
      "catalog_number":"629",
      "title":"Readings in Global Environment"
    },
    {
      "course_id":"002461",
      "subject":"GGOV",
      "catalog_number":"630",
      "title":"Security Ontology-Theory"
    },
    {
      "course_id":"013686",
      "subject":"GGOV",
      "catalog_number":"631",
      "title":"Security Governance: Actors, Institutions, and Issues"
    },
    {
      "course_id":"002444",
      "subject":"GGOV",
      "catalog_number":"632",
      "title":"Post-War Reconstruction and State Building"
    },
    {
      "course_id":"013921",
      "subject":"GGOV",
      "catalog_number":"633",
      "title":"Managing Nuclear Risk"
    },
    {
      "course_id":"014363",
      "subject":"GGOV",
      "catalog_number":"634",
      "title":"Gender and Global Politics"
    },
    {
      "course_id":"013694",
      "subject":"GGOV",
      "catalog_number":"638",
      "title":"Special Topics in Conflict and Security"
    },
    {
      "course_id":"013699",
      "subject":"GGOV",
      "catalog_number":"639",
      "title":"Readings in Conflict and Security"
    },
    {
      "course_id":"002448",
      "subject":"GGOV",
      "catalog_number":"640",
      "title":"Human Rights in the Globalized World"
    },
    {
      "course_id":"013683",
      "subject":"GGOV",
      "catalog_number":"641",
      "title":"International Human Rights"
    },
    {
      "course_id":"012553",
      "subject":"GGOV",
      "catalog_number":"642",
      "title":"Global Social Governance"
    },
    {
      "course_id":"013689",
      "subject":"GGOV",
      "catalog_number":"643",
      "title":"Global Health Governance"
    },
    {
      "course_id":"013695",
      "subject":"GGOV",
      "catalog_number":"648",
      "title":"Special Topics in Global Justice and Human Rights"
    },
    {
      "course_id":"013700",
      "subject":"GGOV",
      "catalog_number":"649",
      "title":"Readings in Global Justice"
    },
    {
      "course_id":"002447",
      "subject":"GGOV",
      "catalog_number":"650",
      "title":"International Organizations and Global Governance"
    },
    {
      "course_id":"013077",
      "subject":"GRK",
      "catalog_number":"621",
      "title":"Greek Epigraphy"
    },
    {
      "course_id":"013684",
      "subject":"GGOV",
      "catalog_number":"651",
      "title":"Unconventional Diplomacy"
    },
    {
      "course_id":"013685",
      "subject":"GGOV",
      "catalog_number":"652",
      "title":"Non-State Actors in Global Governance"
    },
    {
      "course_id":"013922",
      "subject":"GGOV",
      "catalog_number":"653",
      "title":"International Organizations and Public Policy"
    },
    {
      "course_id":"013696",
      "subject":"GGOV",
      "catalog_number":"658",
      "title":"Special Topics in Multilateral Institutions and Diplomacy"
    },
    {
      "course_id":"013701",
      "subject":"GGOV",
      "catalog_number":"659",
      "title":"Readings in Multilateral Institutions and Diplomacy"
    },
    {
      "course_id":"013690",
      "subject":"GGOV",
      "catalog_number":"660",
      "title":"Public International Law"
    },
    {
      "course_id":"013691",
      "subject":"GGOV",
      "catalog_number":"661",
      "title":"International Organizations Law"
    },
    {
      "course_id":"014219",
      "subject":"GGOV",
      "catalog_number":"662",
      "title":"Global Development Governance"
    },
    {
      "course_id":"014301",
      "subject":"GGOV",
      "catalog_number":"663",
      "title":"China and Global Governance"
    },
    {
      "course_id":"014551",
      "subject":"GGOV",
      "catalog_number":"668",
      "title":"Special Topics in Global Social Governance"
    },
    {
      "course_id":"014552",
      "subject":"GGOV",
      "catalog_number":"669",
      "title":"Readings in Global Social Governance"
    },
    {
      "course_id":"013677",
      "subject":"GGOV",
      "catalog_number":"700",
      "title":"Global Governance"
    },
    {
      "course_id":"013678",
      "subject":"GGOV",
      "catalog_number":"701",
      "title":"Research Methods"
    },
    {
      "course_id":"006164",
      "subject":"GRK",
      "catalog_number":"101",
      "title":"Introductory Ancient Greek 1"
    },
    {
      "course_id":"006165",
      "subject":"GRK",
      "catalog_number":"102",
      "title":"Introductory Ancient Greek 2"
    },
    {
      "course_id":"013426",
      "subject":"GRK",
      "catalog_number":"105",
      "title":"Introductory Modern Greek"
    },
    {
      "course_id":"008292",
      "subject":"GRK",
      "catalog_number":"133",
      "title":"New Testament Greek 1"
    },
    {
      "course_id":"008293",
      "subject":"GRK",
      "catalog_number":"134",
      "title":"New Testament Greek 2"
    },
    {
      "course_id":"006166",
      "subject":"GRK",
      "catalog_number":"201",
      "title":"Intermediate Greek"
    },
    {
      "course_id":"006169",
      "subject":"GRK",
      "catalog_number":"202",
      "title":"Selections from Greek Authors"
    },
    {
      "course_id":"008363",
      "subject":"GRK",
      "catalog_number":"233",
      "title":"Intermediate New Testament Greek"
    },
    {
      "course_id":"008364",
      "subject":"GRK",
      "catalog_number":"234",
      "title":"Hellenistic Greek"
    },
    {
      "course_id":"012919",
      "subject":"GRK",
      "catalog_number":"331",
      "title":"Advanced Studies in Greek: Prose"
    },
    {
      "course_id":"012920",
      "subject":"GRK",
      "catalog_number":"332",
      "title":"Advanced Studies in Greek: Poetry"
    },
    {
      "course_id":"013048",
      "subject":"GRK",
      "catalog_number":"341",
      "title":"Advanced Studies in Greek: Selected Topics"
    },
    {
      "course_id":"006175",
      "subject":"GRK",
      "catalog_number":"351",
      "title":"Greek Composition, Grammar and Reading"
    },
    {
      "course_id":"012922",
      "subject":"GRK",
      "catalog_number":"421",
      "title":"Greek Epigraphy"
    },
    {
      "course_id":"012185",
      "subject":"GRK",
      "catalog_number":"451",
      "title":"Senior Greek Composition, Grammar and Reading"
    },
    {
      "course_id":"009960",
      "subject":"GRK",
      "catalog_number":"490",
      "title":"Senior Studies in Greek: Selected Topics"
    },
    {
      "course_id":"009961",
      "subject":"GRK",
      "catalog_number":"491",
      "title":"Senior Studies in Greek: Independent Study"
    },
    {
      "course_id":"014421",
      "subject":"GRK",
      "catalog_number":"600",
      "title":"Topics in Greek Language"
    },
    {
      "course_id":"014422",
      "subject":"GRK",
      "catalog_number":"601",
      "title":"Topics in Greek Language"
    },
    {
      "course_id":"011492",
      "subject":"operative",
      "catalog_number":"Work",
      "title":"Term"
    },
    {
      "course_id":"009116",
      "subject":"GS",
      "catalog_number":"901",
      "title":"Preparing for University Teaching"
    },
    {
      "course_id":"010330",
      "subject":"GS",
      "catalog_number":"902",
      "title":"Preparing for an Academic Career"
    },
    {
      "course_id":"009117",
      "subject":"GS",
      "catalog_number":"903",
      "title":"Teaching Practicum"
    },
    {
      "course_id":"006196",
      "subject":"HIST",
      "catalog_number":"102",
      "title":"War and Society in Europe, 1914-1945"
    },
    {
      "course_id":"006208",
      "subject":"HIST",
      "catalog_number":"103",
      "title":"Canadian History Through Biography"
    },
    {
      "course_id":"006209",
      "subject":"HIST",
      "catalog_number":"104",
      "title":"An Introduction to Western Intellectual History Since the Renaissance"
    },
    {
      "course_id":"012594",
      "subject":"HIST",
      "catalog_number":"105",
      "title":"Rock 'n' Roll and US History"
    },
    {
      "course_id":"006211",
      "subject":"HIST",
      "catalog_number":"106",
      "title":"Canada at War"
    },
    {
      "course_id":"015165",
      "subject":"ENGL",
      "catalog_number":"108P",
      "title":"Popular Potter"
    },
    {
      "course_id":"014151",
      "subject":"HIST",
      "catalog_number":"109",
      "title":"Ten Days That Shook the World"
    },
    {
      "course_id":"010208",
      "subject":"HIST",
      "catalog_number":"110",
      "title":"A History of the Western World I"
    },
    {
      "course_id":"010209",
      "subject":"HIST",
      "catalog_number":"111",
      "title":"A History of the Western World II"
    },
    {
      "course_id":"010343",
      "subject":"HIST",
      "catalog_number":"113",
      "title":"Canadian Business History: Innovators and Entrepreneurs"
    },
    {
      "course_id":"012629",
      "subject":"HIST",
      "catalog_number":"115",
      "title":"Crusading in the Middle Ages"
    },
    {
      "course_id":"011154",
      "subject":"HIST",
      "catalog_number":"120",
      "title":"The United States at War, 1861-1945"
    },
    {
      "course_id":"013716",
      "subject":"HIST",
      "catalog_number":"191",
      "title":"Special Topics in History"
    },
    {
      "course_id":"006220",
      "subject":"HIST",
      "catalog_number":"200",
      "title":"History and Film"
    },
    {
      "course_id":"012751",
      "subject":"HIST",
      "catalog_number":"201",
      "title":"Columbus and After: New Worlds in the Americas"
    },
    {
      "course_id":"006230",
      "subject":"HIST",
      "catalog_number":"205",
      "title":"History of Western Sport"
    },
    {
      "course_id":"012596",
      "subject":"HIST",
      "catalog_number":"206",
      "title":"The Victorian Age"
    },
    {
      "course_id":"006239",
      "subject":"HIST",
      "catalog_number":"209",
      "title":"Smallpox to Medicare: Canadian Medical History"
    },
    {
      "course_id":"006241",
      "subject":"HIST",
      "catalog_number":"210",
      "title":"History of Ancient Law"
    },
    {
      "course_id":"006243",
      "subject":"HIST",
      "catalog_number":"211",
      "title":"British History to 1485"
    },
    {
      "course_id":"006246",
      "subject":"HIST",
      "catalog_number":"213",
      "title":"A History of Popular Culture"
    },
    {
      "course_id":"012407",
      "subject":"HIST",
      "catalog_number":"214",
      "title":"History of Women in the Modern United States"
    },
    {
      "course_id":"006251",
      "subject":"HIST",
      "catalog_number":"215",
      "title":"Canadian Women in Historical Perspective"
    },
    {
      "course_id":"006342",
      "subject":"HIST",
      "catalog_number":"220",
      "title":"The Vietnam War"
    },
    {
      "course_id":"006263",
      "subject":"HIST",
      "catalog_number":"221",
      "title":"Racism and Response in Canadian History"
    },
    {
      "course_id":"006267",
      "subject":"HIST",
      "catalog_number":"223",
      "title":"The Holocaust in History"
    },
    {
      "course_id":"012983",
      "subject":"HIST",
      "catalog_number":"224",
      "title":"Food, Culture, and History"
    },
    {
      "course_id":"013734",
      "subject":"HIST",
      "catalog_number":"225",
      "title":"History of Education in Canada"
    },
    {
      "course_id":"010212",
      "subject":"HIST",
      "catalog_number":"226",
      "title":"Canada in World War II"
    },
    {
      "course_id":"013083",
      "subject":"HIST",
      "catalog_number":"227",
      "title":"The French Revolution and Napoleonic Europe"
    },
    {
      "course_id":"012170",
      "subject":"HIST",
      "catalog_number":"230",
      "title":"Introduction to the Modern Middle East"
    },
    {
      "course_id":"011391",
      "subject":"HIST",
      "catalog_number":"231R",
      "title":"The History of East Asian Communities in Canada"
    },
    {
      "course_id":"011120",
      "subject":"HIST",
      "catalog_number":"232",
      "title":"A History of Peace Movements"
    },
    {
      "course_id":"008323",
      "subject":"HIST",
      "catalog_number":"234",
      "title":"The Catholic Church in Canada"
    },
    {
      "course_id":"008318",
      "subject":"HIST",
      "catalog_number":"235",
      "title":"History of Christianity"
    },
    {
      "course_id":"006194",
      "subject":"HIST",
      "catalog_number":"236",
      "title":"Law and Society in the Middle Ages"
    },
    {
      "course_id":"006279",
      "subject":"HIST",
      "catalog_number":"237",
      "title":"The Ancient Near East and Egypt"
    },
    {
      "course_id":"006281",
      "subject":"HIST",
      "catalog_number":"239",
      "title":"History of Modern China, 1911 to the Present"
    },
    {
      "course_id":"004278",
      "subject":"HIST",
      "catalog_number":"242",
      "title":"Greek History"
    },
    {
      "course_id":"006285",
      "subject":"HIST",
      "catalog_number":"243",
      "title":"European Business History: From Workshop to Factory and Beyond"
    },
    {
      "course_id":"006291",
      "subject":"HIST",
      "catalog_number":"247",
      "title":"Mennonite History: A Survey"
    },
    {
      "course_id":"006298",
      "subject":"HIST",
      "catalog_number":"250",
      "title":"What is History? An Introduction to Historical Thinking"
    },
    {
      "course_id":"004279",
      "subject":"HIST",
      "catalog_number":"252",
      "title":"Roman History"
    },
    {
      "course_id":"006302",
      "subject":"HIST",
      "catalog_number":"253",
      "title":"Canada: Cultures and Conflicts in the Colonial Era"
    },
    {
      "course_id":"006304",
      "subject":"HIST",
      "catalog_number":"254",
      "title":"Canada Since 1867: A New Nation"
    },
    {
      "course_id":"014392",
      "subject":"HIST",
      "catalog_number":"255",
      "title":"History of Childhood and Youth in Canada"
    },
    {
      "course_id":"006309",
      "subject":"HIST",
      "catalog_number":"257",
      "title":"America: From Slavery to Civil War"
    },
    {
      "course_id":"006310",
      "subject":"HIST",
      "catalog_number":"258",
      "title":"The United States: From World Power to the War on Terror"
    },
    {
      "course_id":"006314",
      "subject":"HIST",
      "catalog_number":"260",
      "title":"Europe: 410-1303"
    },
    {
      "course_id":"006316",
      "subject":"HIST",
      "catalog_number":"262",
      "title":"Early Modern Europe 1450-1700"
    },
    {
      "course_id":"006317",
      "subject":"HIST",
      "catalog_number":"263",
      "title":"The Age of Revolution: Europe in the 19th Century"
    },
    {
      "course_id":"006318",
      "subject":"HIST",
      "catalog_number":"264",
      "title":"Western Europe Since 1945"
    },
    {
      "course_id":"011792",
      "subject":"HIST",
      "catalog_number":"265",
      "title":"Eastern Europe Since 1945"
    },
    {
      "course_id":"012316",
      "subject":"HIST",
      "catalog_number":"266",
      "title":"The British Empire 1857-1956"
    },
    {
      "course_id":"012597",
      "subject":"HIST",
      "catalog_number":"268",
      "title":"A Global History of Empires"
    },
    {
      "course_id":"014393",
      "subject":"HIST",
      "catalog_number":"269",
      "title":"Aboriginal History of Canada"
    },
    {
      "course_id":"014394",
      "subject":"HIST",
      "catalog_number":"271",
      "title":"Global Indigenous Issues"
    },
    {
      "course_id":"006219",
      "subject":"HIST",
      "catalog_number":"275",
      "title":"The Modern World in Historical Perspective"
    },
    {
      "course_id":"011574",
      "subject":"HIST",
      "catalog_number":"277",
      "title":"Canadian Legal History"
    },
    {
      "course_id":"012630",
      "subject":"HIST",
      "catalog_number":"278",
      "title":"Red Star vs. Swastika: Russia and WWII"
    },
    {
      "course_id":"013925",
      "subject":"HIST",
      "catalog_number":"282",
      "title":"History of Modern South Asia 1750-2000"
    },
    {
      "course_id":"012065",
      "subject":"HIST",
      "catalog_number":"291",
      "title":"Special Topics in History"
    },
    {
      "course_id":"006327",
      "subject":"HIST",
      "catalog_number":"300",
      "title":"History and the Human Sciences"
    },
    {
      "course_id":"014395",
      "subject":"HIST",
      "catalog_number":"302",
      "title":"Applied History Project"
    },
    {
      "course_id":"014396",
      "subject":"HIST",
      "catalog_number":"303",
      "title":"History Gone Digital: An Introduction to History with the Web"
    },
    {
      "course_id":"008378",
      "subject":"HIST",
      "catalog_number":"304",
      "title":"Heresy and Religious Crises in Late Medieval Europe"
    },
    {
      "course_id":"014469",
      "subject":"HIST",
      "catalog_number":"305",
      "title":"Historical Memory and National Identity"
    },
    {
      "course_id":"011393",
      "subject":"HIST",
      "catalog_number":"309",
      "title":"The Discourse of Dissent"
    },
    {
      "course_id":"006255",
      "subject":"HIST",
      "catalog_number":"310",
      "title":"The American West: Legend and Reality"
    },
    {
      "course_id":"012595",
      "subject":"HIST",
      "catalog_number":"311",
      "title":"International Relations, 1890-1951"
    },
    {
      "course_id":"012364",
      "subject":"HIST",
      "catalog_number":"313",
      "title":"History of the Family in North America"
    },
    {
      "course_id":"012315",
      "subject":"HIST",
      "catalog_number":"314",
      "title":"The American Civil Rights Movement"
    },
    {
      "course_id":"012714",
      "subject":"HIST",
      "catalog_number":"315",
      "title":"U.S. and the World"
    },
    {
      "course_id":"012631",
      "subject":"HIST",
      "catalog_number":"316",
      "title":"The Russian Revolution"
    },
    {
      "course_id":"013234",
      "subject":"HIST",
      "catalog_number":"317",
      "title":"History of Sexuality: The Pre-Modern Period"
    },
    {
      "course_id":"012964",
      "subject":"HIST",
      "catalog_number":"318",
      "title":"History of Sexuality: The Modern Period"
    },
    {
      "course_id":"006346",
      "subject":"HIST",
      "catalog_number":"321",
      "title":"Human Rights in Historical Perspective"
    },
    {
      "course_id":"006352",
      "subject":"HIST",
      "catalog_number":"329",
      "title":"Origins of the Common Law"
    },
    {
      "course_id":"006359",
      "subject":"HIST",
      "catalog_number":"340",
      "title":"A Social History of Europe: 1789-1914"
    },
    {
      "course_id":"006360",
      "subject":"HIST",
      "catalog_number":"341",
      "title":"The Nazi Occupation of Europe"
    },
    {
      "course_id":"014231",
      "subject":"HIST",
      "catalog_number":"347",
      "title":"Witches, Wives, and Whores"
    },
    {
      "course_id":"008377",
      "subject":"HIST",
      "catalog_number":"348",
      "title":"The Radical Reformation"
    },
    {
      "course_id":"006296",
      "subject":"HIST",
      "catalog_number":"350",
      "title":"Canada and the Americas"
    },
    {
      "course_id":"010213",
      "subject":"HIST",
      "catalog_number":"351",
      "title":"Canada: The Immigrant Experience"
    },
    {
      "course_id":"006372",
      "subject":"HIST",
      "catalog_number":"356",
      "title":"Russia: From Tsars to Putin"
    },
    {
      "course_id":"006373",
      "subject":"HIST",
      "catalog_number":"358",
      "title":"Nazi Germany"
    },
    {
      "course_id":"012944",
      "subject":"HIST",
      "catalog_number":"369",
      "title":"The Politics of Decolonization"
    },
    {
      "course_id":"011384",
      "subject":"HIST",
      "catalog_number":"371",
      "title":"Ireland Before the Famine"
    },
    {
      "course_id":"011385",
      "subject":"HIST",
      "catalog_number":"372",
      "title":"Ireland After the Famine"
    },
    {
      "course_id":"006377",
      "subject":"HIST",
      "catalog_number":"374",
      "title":"Canada's Social History"
    },
    {
      "course_id":"006380",
      "subject":"HIST",
      "catalog_number":"379",
      "title":"Reformation History"
    },
    {
      "course_id":"012317",
      "subject":"HIST",
      "catalog_number":"380",
      "title":"History of the Canadian North: From Pre-contact to the Creation of Nunavut"
    },
    {
      "course_id":"006381",
      "subject":"HIST",
      "catalog_number":"385",
      "title":"From Macdonald to Laurier: Canada, 1841-1921"
    },
    {
      "course_id":"006384",
      "subject":"HIST",
      "catalog_number":"388",
      "title":"Modern Canada"
    },
    {
      "course_id":"006385",
      "subject":"HIST",
      "catalog_number":"389",
      "title":"Canada in World Affairs"
    },
    {
      "course_id":"012066",
      "subject":"HIST",
      "catalog_number":"391",
      "title":"Special Topics in History"
    },
    {
      "course_id":"006390",
      "subject":"HIST",
      "catalog_number":"397",
      "title":"Directed Studies in Special Topics"
    },
    {
      "course_id":"006392",
      "subject":"HIST",
      "catalog_number":"398",
      "title":"Directed Studies in Special Topics"
    },
    {
      "course_id":"006394",
      "subject":"HIST",
      "catalog_number":"400A",
      "title":"Early Modern Europe"
    },
    {
      "course_id":"014153",
      "subject":"HIST",
      "catalog_number":"400B",
      "title":"Early Modern Europe"
    },
    {
      "course_id":"006396",
      "subject":"HIST",
      "catalog_number":"401A",
      "title":"European"
    },
    {
      "course_id":"006397",
      "subject":"HIST",
      "catalog_number":"401B",
      "title":"European"
    },
    {
      "course_id":"012632",
      "subject":"HIST",
      "catalog_number":"402A",
      "title":"Medieval Europe"
    },
    {
      "course_id":"012633",
      "subject":"HIST",
      "catalog_number":"402B",
      "title":"Medieval Europe"
    },
    {
      "course_id":"006400",
      "subject":"HIST",
      "catalog_number":"403A",
      "title":"Canadian"
    },
    {
      "course_id":"006401",
      "subject":"HIST",
      "catalog_number":"403B",
      "title":"Canadian"
    },
    {
      "course_id":"006404",
      "subject":"HIST",
      "catalog_number":"407A",
      "title":"Race in Modern History"
    },
    {
      "course_id":"006405",
      "subject":"HIST",
      "catalog_number":"407B",
      "title":"Race in Modern History"
    },
    {
      "course_id":"006406",
      "subject":"HIST",
      "catalog_number":"409A",
      "title":"American"
    },
    {
      "course_id":"006407",
      "subject":"HIST",
      "catalog_number":"409B",
      "title":"American"
    },
    {
      "course_id":"014246",
      "subject":"HIST",
      "catalog_number":"411A",
      "title":"Senior Seminar - International"
    },
    {
      "course_id":"014247",
      "subject":"HIST",
      "catalog_number":"411B",
      "title":"Senior Seminar - International"
    },
    {
      "course_id":"006416",
      "subject":"HIST",
      "catalog_number":"491",
      "title":"Independent Study in Special Subjects"
    },
    {
      "course_id":"001560",
      "subject":"HIST",
      "catalog_number":"601",
      "title":"Canadian History I"
    },
    {
      "course_id":"001559",
      "subject":"HIST",
      "catalog_number":"602",
      "title":"Canadian History II"
    },
    {
      "course_id":"012549",
      "subject":"HIST",
      "catalog_number":"603",
      "title":"Nationalism and Ethnic Policies of Multinational States"
    },
    {
      "course_id":"001561",
      "subject":"HIST",
      "catalog_number":"604",
      "title":"Theory and Practice of Insurgency and Counterinsurgency:  Historical and Contemporary Issues"
    },
    {
      "course_id":"012550",
      "subject":"HIST",
      "catalog_number":"605",
      "title":"Global Governance in Historical Perspective"
    },
    {
      "course_id":"012847",
      "subject":"HIST",
      "catalog_number":"606",
      "title":"International Development in Historical Perspective"
    },
    {
      "course_id":"012970",
      "subject":"HIST",
      "catalog_number":"607",
      "title":"Human Rights in Historical Perspective I"
    },
    {
      "course_id":"012971",
      "subject":"HIST",
      "catalog_number":"608",
      "title":"Human Rights in Historical Perspective II"
    },
    {
      "course_id":"012181",
      "subject":"HIST",
      "catalog_number":"610",
      "title":"War and Society in the Twentieth Century"
    },
    {
      "course_id":"012177",
      "subject":"HIST",
      "catalog_number":"611",
      "title":"War and Society in the Twentieth Century II"
    },
    {
      "course_id":"001568",
      "subject":"HIST",
      "catalog_number":"612",
      "title":"Indigenous Rights and Claims: A Global Perspective"
    },
    {
      "course_id":"013344",
      "subject":"HIST",
      "catalog_number":"614",
      "title":"Space, Identity and Culture: Reading in Canadian Social History"
    },
    {
      "course_id":"001578",
      "subject":"HIST",
      "catalog_number":"620",
      "title":"Early Modern History I"
    },
    {
      "course_id":"001579",
      "subject":"HIST",
      "catalog_number":"621",
      "title":"Early Modern History II"
    },
    {
      "course_id":"013808",
      "subject":"HIST",
      "catalog_number":"622",
      "title":"Microhistory and the Lost Peoples of Europe"
    },
    {
      "course_id":"001582",
      "subject":"HIST",
      "catalog_number":"626",
      "title":"Modern European History I"
    },
    {
      "course_id":"001583",
      "subject":"HIST",
      "catalog_number":"627",
      "title":"Modern European History II"
    },
    {
      "course_id":"001590",
      "subject":"HIST",
      "catalog_number":"632",
      "title":"History of the United States I"
    },
    {
      "course_id":"001591",
      "subject":"HIST",
      "catalog_number":"633",
      "title":"History of the United States II"
    },
    {
      "course_id":"001592",
      "subject":"HIST",
      "catalog_number":"635",
      "title":"Race in Modern History I"
    },
    {
      "course_id":"001593",
      "subject":"HIST",
      "catalog_number":"636",
      "title":"Race in Modern History II"
    },
    {
      "course_id":"001602",
      "subject":"HIST",
      "catalog_number":"651",
      "title":"Historians and Public Policy"
    },
    {
      "course_id":"001604",
      "subject":"HIST",
      "catalog_number":"653",
      "title":"Public History Interpretation"
    },
    {
      "course_id":"001615",
      "subject":"HIST",
      "catalog_number":"691A",
      "title":"Directed Studies"
    },
    {
      "course_id":"001616",
      "subject":"HIST",
      "catalog_number":"691B",
      "title":"Directed Studies"
    },
    {
      "course_id":"001617",
      "subject":"HIST",
      "catalog_number":"691C",
      "title":"Directed Studies"
    },
    {
      "course_id":"009427",
      "subject":"HIST",
      "catalog_number":"701",
      "title":"Major Field Oral Qualifying Examination"
    },
    {
      "course_id":"001627",
      "subject":"HIST",
      "catalog_number":"704",
      "title":"Major Field Written Qualifying Examination"
    },
    {
      "course_id":"001630",
      "subject":"HIST",
      "catalog_number":"705",
      "title":"First Minor Area of Concentration"
    },
    {
      "course_id":"001631",
      "subject":"HIST",
      "catalog_number":"706",
      "title":"Second Minor Area of Concentration"
    },
    {
      "course_id":"009428",
      "subject":"HIST",
      "catalog_number":"710",
      "title":"Canadian History Major Field"
    },
    {
      "course_id":"010523",
      "subject":"HIST",
      "catalog_number":"712",
      "title":"Scottish History Major Field"
    },
    {
      "course_id":"010525",
      "subject":"HIST",
      "catalog_number":"714",
      "title":"Early Modern European History Major Field"
    },
    {
      "course_id":"010526",
      "subject":"HIST",
      "catalog_number":"715",
      "title":"Modern European History Major Field"
    },
    {
      "course_id":"012972",
      "subject":"HIST",
      "catalog_number":"719",
      "title":"War and Society Major Field"
    },
    {
      "course_id":"013809",
      "subject":"HIST",
      "catalog_number":"725",
      "title":"Cold War Era History Major Field"
    },
    {
      "course_id":"013810",
      "subject":"HIST",
      "catalog_number":"726",
      "title":"Medieval History Major Field"
    },
    {
      "course_id":"013811",
      "subject":"HIST",
      "catalog_number":"727",
      "title":"World History Major Field"
    },
    {
      "course_id":"013079",
      "subject":"HIST",
      "catalog_number":"759",
      "title":"War and Society Minor Area Seminar"
    },
    {
      "course_id":"001638",
      "subject":"HIST",
      "catalog_number":"760",
      "title":"Canadian History Minor Area Seminar"
    },
    {
      "course_id":"001639",
      "subject":"HIST",
      "catalog_number":"761",
      "title":"British History Minor Area Seminar"
    },
    {
      "course_id":"010529",
      "subject":"HIST",
      "catalog_number":"762",
      "title":"Scottish History Minor Area Seminar"
    },
    {
      "course_id":"001640",
      "subject":"HIST",
      "catalog_number":"763",
      "title":"Community Studies Minor Area Seminar"
    },
    {
      "course_id":"010530",
      "subject":"HIST",
      "catalog_number":"764",
      "title":"Early Modern European History Minor Area Seminar"
    },
    {
      "course_id":"010531",
      "subject":"HIST",
      "catalog_number":"765",
      "title":"Modern European History Minor Area Seminar"
    },
    {
      "course_id":"001641",
      "subject":"HIST",
      "catalog_number":"766",
      "title":"Gender, Women and Family Minor Area Seminar"
    },
    {
      "course_id":"010532",
      "subject":"HIST",
      "catalog_number":"767",
      "title":"Race, Class, Imperialism and Slavery Minor Area Seminar"
    },
    {
      "course_id":"001642",
      "subject":"HIST",
      "catalog_number":"768",
      "title":"United States Minor Area Seminar"
    },
    {
      "course_id":"010268",
      "subject":"HIST",
      "catalog_number":"769",
      "title":"International  Relations Minor Area Seminar"
    },
    {
      "course_id":"001643",
      "subject":"HIST",
      "catalog_number":"770",
      "title":"Science, Medicine and Technology Minor Area Seminar"
    },
    {
      "course_id":"001644",
      "subject":"HIST",
      "catalog_number":"771",
      "title":"Minor Area of Concentration"
    },
    {
      "course_id":"013812",
      "subject":"HIST",
      "catalog_number":"775",
      "title":"Cold War Era History Minor Area Seminar"
    },
    {
      "course_id":"013813",
      "subject":"HIST",
      "catalog_number":"776",
      "title":"Medieval History Minor Area Seminar"
    },
    {
      "course_id":"013814",
      "subject":"HIST",
      "catalog_number":"777",
      "title":"World History Minor Area Seminar"
    },
    {
      "course_id":"006421",
      "subject":"HLTH",
      "catalog_number":"101",
      "title":"Introduction to Health 1"
    },
    {
      "course_id":"006422",
      "subject":"HLTH",
      "catalog_number":"102",
      "title":"Introduction to Health 2"
    },
    {
      "course_id":"014309",
      "subject":"HLTH",
      "catalog_number":"103",
      "title":"Biological Determinants of Health"
    },
    {
      "course_id":"006420",
      "subject":"HLTH",
      "catalog_number":"201",
      "title":"Aging and Health"
    },
    {
      "course_id":"014310",
      "subject":"HLTH",
      "catalog_number":"202",
      "title":"Introduction to Public and Population Health"
    },
    {
      "course_id":"014311",
      "subject":"HLTH",
      "catalog_number":"203",
      "title":"Systems Thinking for Health"
    },
    {
      "course_id":"006426",
      "subject":"HLTH",
      "catalog_number":"210",
      "title":"Development, Aging and Health"
    },
    {
      "course_id":"006428",
      "subject":"HLTH",
      "catalog_number":"218",
      "title":"Psychology of Death and Dying"
    },
    {
      "course_id":"006429",
      "subject":"HLTH",
      "catalog_number":"220",
      "title":"Psychosocial Perspectives on Lifespan Development and Health"
    },
    {
      "course_id":"006430",
      "subject":"HLTH",
      "catalog_number":"245",
      "title":"The Canadian Health Care System"
    },
    {
      "course_id":"008634",
      "subject":"HLTH",
      "catalog_number":"253",
      "title":"Demographic Change in Canada"
    },
    {
      "course_id":"013200",
      "subject":"HLTH",
      "catalog_number":"260",
      "title":"Social Determinants of Health"
    },
    {
      "course_id":"014313",
      "subject":"HLTH",
      "catalog_number":"302",
      "title":"Cultural and Community Competency"
    },
    {
      "course_id":"014314",
      "subject":"HLTH",
      "catalog_number":"303",
      "title":"Program Planning"
    },
    {
      "course_id":"014315",
      "subject":"HLTH",
      "catalog_number":"305",
      "title":"Community Development, Engagement and Advocacy"
    },
    {
      "course_id":"006426",
      "subject":"HLTH",
      "catalog_number":"310",
      "title":"Development, Aging and Health"
    },
    {
      "course_id":"011462",
      "subject":"HLTH",
      "catalog_number":"330",
      "title":"Health Informatics"
    },
    {
      "course_id":"013201",
      "subject":"HLTH",
      "catalog_number":"333",
      "title":"Experimental Methods and Observational Methods in Epidemiology"
    },
    {
      "course_id":"006431",
      "subject":"HLTH",
      "catalog_number":"340",
      "title":"Environmental Toxicology and Public Health"
    },
    {
      "course_id":"006432",
      "subject":"HLTH",
      "catalog_number":"341",
      "title":"Immunobiology and Public Health"
    },
    {
      "course_id":"013202",
      "subject":"HLTH",
      "catalog_number":"344",
      "title":"Evaluation, Qualitative, and Survey Methods"
    },
    {
      "course_id":"015257",
      "subject":"HLTH",
      "catalog_number":"355",
      "title":"Public Health Nutrition"
    },
    {
      "course_id":"006435",
      "subject":"HLTH",
      "catalog_number":"348",
      "title":"Social Psychology of Health Behaviour"
    },
    {
      "course_id":"006434",
      "subject":"HLTH",
      "catalog_number":"346",
      "title":"Human Nutrition"
    },
    {
      "course_id":"006437",
      "subject":"HLTH",
      "catalog_number":"350",
      "title":"Occupational Health"
    },
    {
      "course_id":"006438",
      "subject":"HLTH",
      "catalog_number":"352",
      "title":"Sociology of Aging"
    },
    {
      "course_id":"013203",
      "subject":"HLTH",
      "catalog_number":"360",
      "title":"Psychological Determinants of Health"
    },
    {
      "course_id":"006440",
      "subject":"HLTH",
      "catalog_number":"400",
      "title":"Multidisciplinary Seminar on Aging"
    },
    {
      "course_id":"006439",
      "subject":"HLTH",
      "catalog_number":"405",
      "title":"International Exchange"
    },
    {
      "course_id":"006441",
      "subject":"HLTH",
      "catalog_number":"407",
      "title":"Coronary Artery Disease - Prevention and Rehabilitation"
    },
    {
      "course_id":"013204",
      "subject":"HLTH",
      "catalog_number":"410",
      "title":"Health Policy"
    },
    {
      "course_id":"006442",
      "subject":"HLTH",
      "catalog_number":"420",
      "title":"Health, Environment, and Planning"
    },
    {
      "course_id":"012212",
      "subject":"HLTH",
      "catalog_number":"421",
      "title":"Nutritional Aspects of Chronic Disease"
    },
    {
      "course_id":"006445",
      "subject":"HLTH",
      "catalog_number":"432A",
      "title":"Honours Thesis (A)"
    },
    {
      "course_id":"006446",
      "subject":"HLTH",
      "catalog_number":"432B",
      "title":"Honours Thesis (B)"
    },
    {
      "course_id":"006447",
      "subject":"HLTH",
      "catalog_number":"433",
      "title":"Advanced Experimental Methods"
    },
    {
      "course_id":"013374",
      "subject":"HLTH",
      "catalog_number":"435",
      "title":"Knowledge Translation and the Application of Health Evidence"
    },
    {
      "course_id":"006448",
      "subject":"HLTH",
      "catalog_number":"442",
      "title":"Epidemiology of Chronic Diseases"
    },
    {
      "course_id":"015260",
      "subject":"HLTH",
      "catalog_number":"443",
      "title":"Epidemiology of Communicable Diseases"
    },
    {
      "course_id":"006433",
      "subject":"HLTH",
      "catalog_number":"444",
      "title":"Program Evaluation"
    },
    {
      "course_id":"006450",
      "subject":"HLTH",
      "catalog_number":"445",
      "title":"Seminar in Health Promotion"
    },
    {
      "course_id":"012775",
      "subject":"HLTH",
      "catalog_number":"448",
      "title":"Advanced Studies in Social Determinants of Health"
    },
    {
      "course_id":"012776",
      "subject":"HLTH",
      "catalog_number":"449",
      "title":"Alcohol and Drug Use and Abuse in Contemporary Society"
    },
    {
      "course_id":"012213",
      "subject":"HLTH",
      "catalog_number":"451",
      "title":"Analysis and Management of Health Information in Aging Populations"
    },
    {
      "course_id":"012210",
      "subject":"HLTH",
      "catalog_number":"452",
      "title":"Decision Making and Decision Support in Health Informatics"
    },
    {
      "course_id":"014378",
      "subject":"HLTH",
      "catalog_number":"458",
      "title":"Social Neuroscience and Health"
    },
    {
      "course_id":"012214",
      "subject":"HLTH",
      "catalog_number":"461",
      "title":"Psychoneuroimmunology"
    },
    {
      "course_id":"010093",
      "subject":"HLTH",
      "catalog_number":"471",
      "title":"Psychopharmacology"
    },
    {
      "course_id":"009508",
      "subject":"HLTH",
      "catalog_number":"472",
      "title":"Independent Study"
    },
    {
      "course_id":"013205",
      "subject":"HLTH",
      "catalog_number":"473",
      "title":"Contemporary Issues in Health"
    },
    {
      "course_id":"006474",
      "subject":"HRM",
      "catalog_number":"200",
      "title":"Basic Human Resources Management"
    },
    {
      "course_id":"011707",
      "subject":"HRM",
      "catalog_number":"301",
      "title":"Strategic Human Resources Management"
    },
    {
      "course_id":"013563",
      "subject":"HRM",
      "catalog_number":"303",
      "title":"Compensation"
    },
    {
      "course_id":"013565",
      "subject":"HRM",
      "catalog_number":"305",
      "title":"Health and Safety"
    },
    {
      "course_id":"013564",
      "subject":"HRM",
      "catalog_number":"307",
      "title":"Labour Relations"
    },
    {
      "course_id":"013566",
      "subject":"HRM",
      "catalog_number":"400",
      "title":"Honours Seminar in Human Resources Management - Special Topics"
    },
    {
      "course_id":"001724",
      "subject":"HSG",
      "catalog_number":"601",
      "title":"Lifespan Approaches to Disease Prevention and Health Promotion"
    },
    {
      "course_id":"010533",
      "subject":"HSG",
      "catalog_number":"603",
      "title":"Health Policy"
    },
    {
      "course_id":"001725",
      "subject":"HSG",
      "catalog_number":"604",
      "title":"Evaluation of Health and Human Service Programs"
    },
    {
      "course_id":"010534",
      "subject":"HSG",
      "catalog_number":"605A",
      "title":"Survey Research Methods"
    },
    {
      "course_id":"001755",
      "subject":"HSG",
      "catalog_number":"605B",
      "title":"Correlation and Regression"
    },
    {
      "course_id":"001756",
      "subject":"HSG",
      "catalog_number":"605C",
      "title":"Logistic Regression and Its Application"
    },
    {
      "course_id":"001757",
      "subject":"HSG",
      "catalog_number":"605D",
      "title":"Analysis of Variance I"
    },
    {
      "course_id":"001758",
      "subject":"HSG",
      "catalog_number":"605E",
      "title":"Analysis of Variance II"
    },
    {
      "course_id":"001754",
      "subject":"HSG",
      "catalog_number":"605F",
      "title":"Introduction to Statistics"
    },
    {
      "course_id":"001730",
      "subject":"HSG",
      "catalog_number":"606",
      "title":"Epidemiological Methods"
    },
    {
      "course_id":"010535",
      "subject":"HSG",
      "catalog_number":"607",
      "title":"Mechanisms of Disease Processes"
    },
    {
      "course_id":"010536",
      "subject":"HSG",
      "catalog_number":"609",
      "title":"Population Intervention Research for Chronic Disease Prevention"
    },
    {
      "course_id":"001731",
      "subject":"HSG",
      "catalog_number":"610",
      "title":"Program Development and Service Delivery for the Elderly"
    },
    {
      "course_id":"013806",
      "subject":"HSG",
      "catalog_number":"611",
      "title":"The Health Care System"
    },
    {
      "course_id":"013604",
      "subject":"HSG",
      "catalog_number":"612",
      "title":"Data Structures and Standards in Health Informatics"
    },
    {
      "course_id":"010537",
      "subject":"HSG",
      "catalog_number":"620",
      "title":"Selected Topics"
    },
    {
      "course_id":"013030",
      "subject":"LAT",
      "catalog_number":"622",
      "title":"Latin Palaeography"
    },
    {
      "course_id":"013031",
      "subject":"LAT",
      "catalog_number":"633",
      "title":"Greek and Roman Identities in the Lyric Poetry of Horace"
    },
    {
      "course_id":"011245",
      "subject":"HSG",
      "catalog_number":"620Q",
      "title":"Health Communications"
    },
    {
      "course_id":"010253",
      "subject":"HSG",
      "catalog_number":"641",
      "title":"Practicum"
    },
    {
      "course_id":"013452",
      "subject":"HSG",
      "catalog_number":"651",
      "title":"Analysis and Management of Health Information in Aging Populations"
    },
    {
      "course_id":"013454",
      "subject":"HSG",
      "catalog_number":"652",
      "title":"Decision Making and Decision Support in Health"
    },
    {
      "course_id":"012851",
      "subject":"HSG",
      "catalog_number":"654",
      "title":"Knowledge Mobilzation to Serve Society"
    },
    {
      "course_id":"012969",
      "subject":"HSG",
      "catalog_number":"655",
      "title":"Building Community-University Research Alliances"
    },
    {
      "course_id":"010230",
      "subject":"HSG",
      "catalog_number":"671",
      "title":"Psychopharmacology"
    },
    {
      "course_id":"012868",
      "subject":"HSG",
      "catalog_number":"672",
      "title":"Epidemiologic Methods in Aging Research"
    },
    {
      "course_id":"002626",
      "subject":"HSG",
      "catalog_number":"677",
      "title":"Fundamentals of Behavioural Neuroscience"
    },
    {
      "course_id":"010539",
      "subject":"HSG",
      "catalog_number":"720",
      "title":"Advanced Topics"
    },
    {
      "course_id":"001801",
      "subject":"KIN",
      "catalog_number":"707",
      "title":"Integrative Physiology in Work"
    },
    {
      "course_id":"013139",
      "subject":"HSG",
      "catalog_number":"730",
      "title":"Fundamentals of Work and Health"
    },
    {
      "course_id":"013140",
      "subject":"HSG",
      "catalog_number":"731",
      "title":"Approaches to Research in Work and Health"
    },
    {
      "course_id":"013141",
      "subject":"HSG",
      "catalog_number":"732A",
      "title":"Work and Health Research Seminar (I)"
    },
    {
      "course_id":"013142",
      "subject":"HSG",
      "catalog_number":"732B",
      "title":"Work and Health Research Seminar (II)"
    },
    {
      "course_id":"001743",
      "subject":"HSG",
      "catalog_number":"741",
      "title":"Advanced Practicum"
    },
    {
      "course_id":"012422",
      "subject":"HSG",
      "catalog_number":"750",
      "title":"Fundamentals of Aging, Health and Well-being"
    },
    {
      "course_id":"012426",
      "subject":"HSG",
      "catalog_number":"751",
      "title":"Aging, Health and Well-being Research Seminar"
    },
    {
      "course_id":"011869",
      "subject":"HUMSC",
      "catalog_number":"101",
      "title":"Great Dialogues: Reflection and Action"
    },
    {
      "course_id":"011870",
      "subject":"HUMSC",
      "catalog_number":"102",
      "title":"Great Dialogues: Politics and Morality"
    },
    {
      "course_id":"012363",
      "subject":"HUMSC",
      "catalog_number":"201",
      "title":"Great Dialogues: Reason and Faith"
    },
    {
      "course_id":"012453",
      "subject":"HUMSC",
      "catalog_number":"301",
      "title":"Great Dialogues: The Sacred and the Profane"
    },
    {
      "course_id":"012454",
      "subject":"HUMSC",
      "catalog_number":"401",
      "title":"Great Dialogues: Athens, Jerusalem, and Technological Society"
    },
    {
      "course_id":"012962",
      "subject":"HUMSC",
      "catalog_number":"490",
      "title":"Great Dialogues: Medical Humanities on Health and Life"
    },
    {
      "course_id":"013449",
      "subject":"INDEV",
      "catalog_number":"10",
      "title":"International Development Seminar"
    },
    {
      "course_id":"012674",
      "subject":"INDEV",
      "catalog_number":"100",
      "title":"Introduction to International Development"
    },
    {
      "course_id":"014370",
      "subject":"INDEV",
      "catalog_number":"101",
      "title":"Issues in International Development"
    },
    {
      "course_id":"012675",
      "subject":"INDEV",
      "catalog_number":"200",
      "title":"The Political Economy of Development"
    },
    {
      "course_id":"012676",
      "subject":"INDEV",
      "catalog_number":"202",
      "title":"Accounting for Development Organizations"
    },
    {
      "course_id":"012677",
      "subject":"INDEV",
      "catalog_number":"212",
      "title":"Problem-solving for Development"
    },
    {
      "course_id":"014686",
      "subject":"INDEV",
      "catalog_number":"404",
      "title":"International Development Theory"
    },
    {
      "course_id":"013191",
      "subject":"INDEV",
      "catalog_number":"275",
      "title":"Special Topics in International Development"
    },
    {
      "course_id":"012678",
      "subject":"INDEV",
      "catalog_number":"300",
      "title":"Culture and Ethics"
    },
    {
      "course_id":"012679",
      "subject":"INDEV",
      "catalog_number":"302",
      "title":"Development Agents"
    },
    {
      "course_id":"013447",
      "subject":"INDEV",
      "catalog_number":"303",
      "title":"Marketing and Communication for Development Agents"
    },
    {
      "course_id":"012680",
      "subject":"INDEV",
      "catalog_number":"304",
      "title":"Language Conversation for Development Field Work"
    },
    {
      "course_id":"012682",
      "subject":"INDEV",
      "catalog_number":"308",
      "title":"Introduction to Social Entrepreneurship"
    },
    {
      "course_id":"013192",
      "subject":"INDEV",
      "catalog_number":"375",
      "title":"Special Topics in International Development"
    },
    {
      "course_id":"013860",
      "subject":"INDEV",
      "catalog_number":"387",
      "title":"Global Cities in Global Development"
    },
    {
      "course_id":"013930",
      "subject":"INDEV",
      "catalog_number":"388",
      "title":"Key Issues in Urban Development"
    },
    {
      "course_id":"012684",
      "subject":"INDEV",
      "catalog_number":"401",
      "title":"International Development Placement 1"
    },
    {
      "course_id":"012685",
      "subject":"INDEV",
      "catalog_number":"402",
      "title":"International Development Placement 2"
    },
    {
      "course_id":"012686",
      "subject":"INDEV",
      "catalog_number":"403",
      "title":"Advanced Marketing and Communication for Development Agents"
    },
    {
      "course_id":"013448",
      "subject":"INDEV",
      "catalog_number":"474",
      "title":"Special Topics in International Development"
    },
    {
      "course_id":"014685",
      "subject":"INDEV",
      "catalog_number":"475",
      "title":"Contemporary Development Issues"
    },
    {
      "course_id":"014308",
      "subject":"INDEV",
      "catalog_number":"601",
      "title":"Foundations of Sustainable Development Practice"
    },
    {
      "course_id":"001374",
      "subject":"INDEV",
      "catalog_number":"602",
      "title":"International Development: Theories and Practice"
    },
    {
      "course_id":"014328",
      "subject":"INDEV",
      "catalog_number":"603",
      "title":"Global Health"
    },
    {
      "course_id":"014121",
      "subject":"INDEV",
      "catalog_number":"604",
      "title":"Sustainable Cities"
    },
    {
      "course_id":"014013",
      "subject":"INDEV",
      "catalog_number":"605",
      "title":"Economics for Sustainable Development"
    },
    {
      "course_id":"012666",
      "subject":"INDEV",
      "catalog_number":"606",
      "title":"Energy Sustainability"
    },
    {
      "course_id":"014014",
      "subject":"INDEV",
      "catalog_number":"607",
      "title":"Methods for Sustainable Development Practice:  A Systems Approach"
    },
    {
      "course_id":"014015",
      "subject":"INDEV",
      "catalog_number":"608",
      "title":"Water and Security"
    },
    {
      "course_id":"014327",
      "subject":"INDEV",
      "catalog_number":"609",
      "title":"Sustainability Concepts, Applications and Key Debates"
    },
    {
      "course_id":"014027",
      "subject":"INDEV",
      "catalog_number":"611",
      "title":"Field Placement"
    },
    {
      "course_id":"014016",
      "subject":"INDEV",
      "catalog_number":"612",
      "title":"Introduction to Water Resources"
    },
    {
      "course_id":"014017",
      "subject":"INDEV",
      "catalog_number":"613",
      "title":"Water, Human Security and Development"
    },
    {
      "course_id":"014018",
      "subject":"INDEV",
      "catalog_number":"614",
      "title":"Integrated Water Resources Management"
    },
    {
      "course_id":"014019",
      "subject":"INDEV",
      "catalog_number":"615",
      "title":"Transboundary Water Governance"
    },
    {
      "course_id":"014020",
      "subject":"INDEV",
      "catalog_number":"616",
      "title":"Urban Food Security"
    },
    {
      "course_id":"012691",
      "subject":"INTEG",
      "catalog_number":"10",
      "title":"Knowledge Integration Seminar"
    },
    {
      "course_id":"012690",
      "subject":"INTEG",
      "catalog_number":"120",
      "title":"Introduction to the Academy: Disciplines and Integrative Practices"
    },
    {
      "course_id":"012692",
      "subject":"INTEG",
      "catalog_number":"121",
      "title":"Introduction to the Academy: Design and Problem-Solving"
    },
    {
      "course_id":"012693",
      "subject":"INTEG",
      "catalog_number":"220",
      "title":"Nature of Scientific Knowledge"
    },
    {
      "course_id":"012694",
      "subject":"INTEG",
      "catalog_number":"221",
      "title":"The Social Nature of Knowledge"
    },
    {
      "course_id":"004929",
      "subject":"INTTS",
      "catalog_number":"301",
      "title":"Institutions of International Trade and Finance"
    },
    {
      "course_id":"012695",
      "subject":"INTEG",
      "catalog_number":"230",
      "title":"The Museum Course: Preparation and Field Trip"
    },
    {
      "course_id":"012696",
      "subject":"INTEG",
      "catalog_number":"231",
      "title":"The Museum Course: Field Trip Project"
    },
    {
      "course_id":"014109",
      "subject":"INTEG",
      "catalog_number":"251",
      "title":"Creative Thinking"
    },
    {
      "course_id":"013043",
      "subject":"INTEG",
      "catalog_number":"275",
      "title":"Special Topics in Knowledge Integration"
    },
    {
      "course_id":"012697",
      "subject":"INTEG",
      "catalog_number":"320",
      "title":"The Museum Course: Research & Design"
    },
    {
      "course_id":"012698",
      "subject":"INTEG",
      "catalog_number":"321",
      "title":"The Museum Course: Practicum and Presentation"
    },
    {
      "course_id":"013044",
      "subject":"INTEG",
      "catalog_number":"375",
      "title":"Special Topics in Knowledge Integration"
    },
    {
      "course_id":"012699",
      "subject":"INTEG",
      "catalog_number":"420",
      "title":"Senior Research Project A"
    },
    {
      "course_id":"012700",
      "subject":"INTEG",
      "catalog_number":"421",
      "title":"Senior Research Project B"
    },
    {
      "course_id":"013714",
      "subject":"INTEG",
      "catalog_number":"475",
      "title":"Special Topics in Knowledge Integration"
    },
    {
      "course_id":"012277",
      "subject":"INTST",
      "catalog_number":"101",
      "title":"Introduction to International Studies"
    },
    {
      "course_id":"006477",
      "subject":"INTTS",
      "catalog_number":"400",
      "title":"International Trade Seminar"
    },
    {
      "course_id":"006479",
      "subject":"IS",
      "catalog_number":"100",
      "title":"Introduction to Research Methods"
    },
    {
      "course_id":"012419",
      "subject":"IS",
      "catalog_number":"101",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"012443",
      "subject":"IS",
      "catalog_number":"102",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011535",
      "subject":"IS",
      "catalog_number":"103",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011536",
      "subject":"IS",
      "catalog_number":"104",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011537",
      "subject":"IS",
      "catalog_number":"105",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011538",
      "subject":"IS",
      "catalog_number":"106",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011539",
      "subject":"IS",
      "catalog_number":"107",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011540",
      "subject":"IS",
      "catalog_number":"108",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"011541",
      "subject":"IS",
      "catalog_number":"109",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"012428",
      "subject":"IS",
      "catalog_number":"110",
      "title":"Introductory Independent Research"
    },
    {
      "course_id":"013211",
      "subject":"IS",
      "catalog_number":"200",
      "title":"Interdisciplinary Research Design for Independent Studies"
    },
    {
      "course_id":"006487",
      "subject":"IS",
      "catalog_number":"201",
      "title":"Independent Research"
    },
    {
      "course_id":"006488",
      "subject":"IS",
      "catalog_number":"202",
      "title":"Independent Research"
    },
    {
      "course_id":"006489",
      "subject":"IS",
      "catalog_number":"203",
      "title":"Independent Research"
    },
    {
      "course_id":"006490",
      "subject":"IS",
      "catalog_number":"204",
      "title":"Independent Research"
    },
    {
      "course_id":"006491",
      "subject":"IS",
      "catalog_number":"205",
      "title":"Independent Research"
    },
    {
      "course_id":"009895",
      "subject":"IS",
      "catalog_number":"206",
      "title":"Independent Research"
    },
    {
      "course_id":"009897",
      "subject":"IS",
      "catalog_number":"207",
      "title":"Independent Research"
    },
    {
      "course_id":"009870",
      "subject":"IS",
      "catalog_number":"208",
      "title":"Independent Research"
    },
    {
      "course_id":"009871",
      "subject":"IS",
      "catalog_number":"209",
      "title":"Independent Research"
    },
    {
      "course_id":"012429",
      "subject":"IS",
      "catalog_number":"210",
      "title":"Independent Research"
    },
    {
      "course_id":"012430",
      "subject":"IS",
      "catalog_number":"211",
      "title":"Independent Research"
    },
    {
      "course_id":"012431",
      "subject":"IS",
      "catalog_number":"212",
      "title":"Independent Research"
    },
    {
      "course_id":"012432",
      "subject":"IS",
      "catalog_number":"220",
      "title":"Thesis Proposal Development"
    },
    {
      "course_id":"012433",
      "subject":"IS",
      "catalog_number":"301",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"012434",
      "subject":"IS",
      "catalog_number":"302",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"011542",
      "subject":"IS",
      "catalog_number":"304",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"011543",
      "subject":"IS",
      "catalog_number":"305",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"011544",
      "subject":"IS",
      "catalog_number":"306",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"011545",
      "subject":"IS",
      "catalog_number":"307",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"011546",
      "subject":"IS",
      "catalog_number":"308",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"011547",
      "subject":"IS",
      "catalog_number":"309",
      "title":"Advanced Independent Research"
    },
    {
      "course_id":"012441",
      "subject":"IS",
      "catalog_number":"310",
      "title":"Thesis Phase I"
    },
    {
      "course_id":"012618",
      "subject":"IS",
      "catalog_number":"311",
      "title":"Part-time Thesis Phase Stage I - Part 1"
    },
    {
      "course_id":"012619",
      "subject":"IS",
      "catalog_number":"312",
      "title":"Part-time Thesis Phase Stage I - Part 2"
    },
    {
      "course_id":"012442",
      "subject":"IS",
      "catalog_number":"320",
      "title":"Thesis Phase II"
    },
    {
      "course_id":"012620",
      "subject":"IS",
      "catalog_number":"321",
      "title":"Part-time Thesis Phase Stage II - Part 1"
    },
    {
      "course_id":"012621",
      "subject":"IS",
      "catalog_number":"322",
      "title":"Part-time Thesis Phase Stage II - Part 2"
    },
    {
      "course_id":"013212",
      "subject":"IS",
      "catalog_number":"330",
      "title":"Honours Thesis Proposal Development"
    },
    {
      "course_id":"013206",
      "subject":"IS",
      "catalog_number":"401",
      "title":"Honours Independent Research"
    },
    {
      "course_id":"013207",
      "subject":"IS",
      "catalog_number":"402",
      "title":"Honours Independent Research"
    },
    {
      "course_id":"013208",
      "subject":"IS",
      "catalog_number":"403",
      "title":"Honours Independent Research"
    },
    {
      "course_id":"013209",
      "subject":"IS",
      "catalog_number":"404",
      "title":"Honours Independent Research"
    },
    {
      "course_id":"013210",
      "subject":"IS",
      "catalog_number":"405",
      "title":"Honours Independent Research"
    },
    {
      "course_id":"013213",
      "subject":"IS",
      "catalog_number":"410",
      "title":"Honours Thesis Phase I"
    },
    {
      "course_id":"013214",
      "subject":"IS",
      "catalog_number":"411",
      "title":"Part-time Honours Thesis Phase Stage I - Part 1"
    },
    {
      "course_id":"013215",
      "subject":"IS",
      "catalog_number":"412",
      "title":"Part-time Honours Thesis Phase Stage I - Part 2"
    },
    {
      "course_id":"013216",
      "subject":"IS",
      "catalog_number":"420",
      "title":"Honours Thesis Phase II"
    },
    {
      "course_id":"013217",
      "subject":"IS",
      "catalog_number":"421",
      "title":"Part-time Honours Thesis Phase Stage II - Part 1"
    },
    {
      "course_id":"013218",
      "subject":"IS",
      "catalog_number":"422",
      "title":"Part-time Honours Thesis Phase Stage II - Part 2"
    },
    {
      "course_id":"006518",
      "subject":"ITAL",
      "catalog_number":"101",
      "title":"Introduction to Italian Language 1"
    },
    {
      "course_id":"006519",
      "subject":"ITAL",
      "catalog_number":"102",
      "title":"Introduction to Italian Language 2"
    },
    {
      "course_id":"013611",
      "subject":"ITAL",
      "catalog_number":"155",
      "title":"Intensive Introductory Italian Language"
    },
    {
      "course_id":"006522",
      "subject":"ITAL",
      "catalog_number":"201",
      "title":"Intermediate Italian 1"
    },
    {
      "course_id":"006523",
      "subject":"ITAL",
      "catalog_number":"202",
      "title":"Intermediate Italian 2"
    },
    {
      "course_id":"006524",
      "subject":"ITAL",
      "catalog_number":"251",
      "title":"Issues in Contemporary Italian Society"
    },
    {
      "course_id":"006525",
      "subject":"ITAL",
      "catalog_number":"255",
      "title":"Italian for Business and Technology"
    },
    {
      "course_id":"006528",
      "subject":"ITAL",
      "catalog_number":"311",
      "title":"Medieval Italian Literature"
    },
    {
      "course_id":"006529",
      "subject":"ITAL",
      "catalog_number":"312",
      "title":"Renaissance Italian Literature"
    },
    {
      "course_id":"013233",
      "subject":"ITAL",
      "catalog_number":"370",
      "title":"Women Writers of the Italian Renaissance"
    },
    {
      "course_id":"006530",
      "subject":"ITAL",
      "catalog_number":"391",
      "title":"The Italian Novel and Cinema"
    },
    {
      "course_id":"006531",
      "subject":"ITAL",
      "catalog_number":"392",
      "title":"Modern Italian Poetry and Theatre"
    },
    {
      "course_id":"012273",
      "subject":"ITAL",
      "catalog_number":"394",
      "title":"Italian Studies in Italy"
    },
    {
      "course_id":"006532",
      "subject":"ITAL",
      "catalog_number":"396",
      "title":"Special Topics\/Directed Readings"
    },
    {
      "course_id":"006533",
      "subject":"ITAL",
      "catalog_number":"397",
      "title":"Special Topics\/Directed Readings"
    },
    {
      "course_id":"012274",
      "subject":"ITALST",
      "catalog_number":"111",
      "title":"Women, Family, Sex and Tradition"
    },
    {
      "course_id":"011970",
      "subject":"ITALST",
      "catalog_number":"260",
      "title":"Great Works in Italian Literature"
    },
    {
      "course_id":"011972",
      "subject":"ITALST",
      "catalog_number":"270",
      "title":"Modern Italy"
    },
    {
      "course_id":"011973",
      "subject":"ITALST",
      "catalog_number":"271",
      "title":"Italian Canadian Experience"
    },
    {
      "course_id":"006526",
      "subject":"ITALST",
      "catalog_number":"291",
      "title":"Italian Culture and Civilization 1"
    },
    {
      "course_id":"006527",
      "subject":"ITALST",
      "catalog_number":"292",
      "title":"Italian Culture and Civilization 2"
    },
    {
      "course_id":"006528",
      "subject":"ITALST",
      "catalog_number":"311",
      "title":"Medieval Italian Literature"
    },
    {
      "course_id":"006529",
      "subject":"ITALST",
      "catalog_number":"312",
      "title":"Renaissance Italian Literature"
    },
    {
      "course_id":"011898",
      "subject":"ITALST",
      "catalog_number":"360",
      "title":"Dante's Divine Comedy"
    },
    {
      "course_id":"013233",
      "subject":"ITALST",
      "catalog_number":"370",
      "title":"Women Writers of the Italian Renaissance"
    },
    {
      "course_id":"006530",
      "subject":"ITALST",
      "catalog_number":"391",
      "title":"The Italian Novel and Cinema"
    },
    {
      "course_id":"006531",
      "subject":"ITALST",
      "catalog_number":"392",
      "title":"Modern Italian Poetry and Theatre"
    },
    {
      "course_id":"012273",
      "subject":"ITALST",
      "catalog_number":"394",
      "title":"Italian Studies in Italy"
    },
    {
      "course_id":"006532",
      "subject":"ITALST",
      "catalog_number":"396",
      "title":"Special Topics\/Directed Readings"
    },
    {
      "course_id":"006533",
      "subject":"ITALST",
      "catalog_number":"397",
      "title":"Special Topics\/Directed Readings"
    },
    {
      "course_id":"006535",
      "subject":"JAPAN",
      "catalog_number":"101R",
      "title":"First-Year Japanese 1"
    },
    {
      "course_id":"006536",
      "subject":"JAPAN",
      "catalog_number":"102R",
      "title":"First-Year Japanese 2"
    },
    {
      "course_id":"006537",
      "subject":"JAPAN",
      "catalog_number":"111R",
      "title":"Japanese for Business 1"
    },
    {
      "course_id":"006538",
      "subject":"JAPAN",
      "catalog_number":"112R",
      "title":"Japanese for Business 2"
    },
    {
      "course_id":"006539",
      "subject":"JAPAN",
      "catalog_number":"201R",
      "title":"Second-Year Japanese 1"
    },
    {
      "course_id":"006540",
      "subject":"JAPAN",
      "catalog_number":"202R",
      "title":"Second-Year Japanese 2"
    },
    {
      "course_id":"014000",
      "subject":"JAPAN",
      "catalog_number":"272R",
      "title":"Japanese Culture and Society"
    },
    {
      "course_id":"006541",
      "subject":"JAPAN",
      "catalog_number":"301R",
      "title":"Third-Year Japanese 1"
    },
    {
      "course_id":"012783",
      "subject":"JAPAN",
      "catalog_number":"302R",
      "title":"Third-Year Japanese 2"
    },
    {
      "course_id":"008290",
      "subject":"JS",
      "catalog_number":"105A",
      "title":"Classical Hebrew 1"
    },
    {
      "course_id":"008291",
      "subject":"JS",
      "catalog_number":"105B",
      "title":"Classical Hebrew 2"
    },
    {
      "course_id":"010108",
      "subject":"JS",
      "catalog_number":"120",
      "title":"Relationships in the Bible (Old Testament)"
    },
    {
      "course_id":"010110",
      "subject":"JS",
      "catalog_number":"125",
      "title":"Great Texts in the Jewish Tradition"
    },
    {
      "course_id":"010109",
      "subject":"JS",
      "catalog_number":"130",
      "title":"Power and Corruption in the Bible (Old Testament)"
    },
    {
      "course_id":"010119",
      "subject":"JS",
      "catalog_number":"150",
      "title":"The Quest for Meaning in Modern Judaism"
    },
    {
      "course_id":"011635",
      "subject":"JS",
      "catalog_number":"203",
      "title":"Jewish Responses to the Holocaust"
    },
    {
      "course_id":"008297",
      "subject":"JS",
      "catalog_number":"205",
      "title":"The Hebrew Prophets"
    },
    {
      "course_id":"010111",
      "subject":"JS",
      "catalog_number":"210",
      "title":"Jewish Philosophy"
    },
    {
      "course_id":"012171",
      "subject":"JS",
      "catalog_number":"211",
      "title":"Kabbalah: Jewish Mysticism"
    },
    {
      "course_id":"014248",
      "subject":"JS",
      "catalog_number":"215",
      "title":"Visions of Israel in Judaism: From Biblical to Modern Times"
    },
    {
      "course_id":"008308",
      "subject":"JS",
      "catalog_number":"217",
      "title":"Judaism"
    },
    {
      "course_id":"011636",
      "subject":"JS",
      "catalog_number":"233",
      "title":"The Holocaust and Film"
    },
    {
      "course_id":"011983",
      "subject":"JS",
      "catalog_number":"250",
      "title":"Special Topics"
    },
    {
      "course_id":"011155",
      "subject":"JS",
      "catalog_number":"301",
      "title":"Canada and the Holocaust"
    },
    {
      "course_id":"008365",
      "subject":"JS",
      "catalog_number":"306A",
      "title":"Intermediate Classical Hebrew"
    },
    {
      "course_id":"008366",
      "subject":"JS",
      "catalog_number":"306B",
      "title":"Ancient Semitic Texts and Inscriptions"
    },
    {
      "course_id":"014249",
      "subject":"JS",
      "catalog_number":"310",
      "title":"Jews in the New World"
    },
    {
      "course_id":"013095",
      "subject":"JS",
      "catalog_number":"313",
      "title":"Moses Maimonides: Life and Thought"
    },
    {
      "course_id":"012959",
      "subject":"JS",
      "catalog_number":"339",
      "title":"The Bible (Old Testament) and Archaeology"
    },
    {
      "course_id":"013232",
      "subject":"JS",
      "catalog_number":"341",
      "title":"Jewish Contributions to Political Thought"
    },
    {
      "course_id":"011187",
      "subject":"JS",
      "catalog_number":"350",
      "title":"Special Topics in Jewish Studies"
    },
    {
      "course_id":"011188",
      "subject":"JS",
      "catalog_number":"450",
      "title":"Special Topics in Jewish Studies"
    },
    {
      "course_id":"009275",
      "subject":"KIN",
      "catalog_number":"1",
      "title":"Discussion of Behavioural Issues"
    },
    {
      "course_id":"006542",
      "subject":"KIN",
      "catalog_number":"10",
      "title":"Ergonomics Option Seminar"
    },
    {
      "course_id":"006543",
      "subject":"KIN",
      "catalog_number":"100",
      "title":"Human Anatomy: Limbs and Trunk"
    },
    {
      "course_id":"006544",
      "subject":"KIN",
      "catalog_number":"100L",
      "title":"Human Anatomy Lab"
    },
    {
      "course_id":"006545",
      "subject":"KIN",
      "catalog_number":"101",
      "title":"Biophysical Evaluation Lab"
    },
    {
      "course_id":"013465",
      "subject":"KIN",
      "catalog_number":"104",
      "title":"Issues and Approaches in Kinesiology"
    },
    {
      "course_id":"006548",
      "subject":"KIN",
      "catalog_number":"105",
      "title":"Cardiovascular and Respiratory Responses to Exercise"
    },
    {
      "course_id":"006550",
      "subject":"KIN",
      "catalog_number":"121",
      "title":"Biomechanics of Human Activity"
    },
    {
      "course_id":"011558",
      "subject":"KIN",
      "catalog_number":"140L",
      "title":"Sport Injury Management Lab"
    },
    {
      "course_id":"015107",
      "subject":"KIN",
      "catalog_number":"204",
      "title":"Movement Assessment and Exercise Prescription"
    },
    {
      "course_id":"006560",
      "subject":"KIN",
      "catalog_number":"155",
      "title":"Introduction to Neuroscience for Kinesiology"
    },
    {
      "course_id":"006553",
      "subject":"KIN",
      "catalog_number":"205",
      "title":"Muscle Physiology in Exercise and Work"
    },
    {
      "course_id":"006426",
      "subject":"KIN",
      "catalog_number":"210",
      "title":"Development, Aging and Health"
    },
    {
      "course_id":"006555",
      "subject":"KIN",
      "catalog_number":"217",
      "title":"Human Biochemistry"
    },
    {
      "course_id":"009502",
      "subject":"KIN",
      "catalog_number":"221",
      "title":"Advanced Biomechanics of Human Movement"
    },
    {
      "course_id":"006556",
      "subject":"KIN",
      "catalog_number":"222",
      "title":"Statistical Techniques Applied to Kinesiology"
    },
    {
      "course_id":"006557",
      "subject":"KIN",
      "catalog_number":"242",
      "title":"Introduction to Movement Disorders"
    },
    {
      "course_id":"006558",
      "subject":"KIN",
      "catalog_number":"250",
      "title":"Sociology of Physical Activity"
    },
    {
      "course_id":"006552",
      "subject":"KIN",
      "catalog_number":"301",
      "title":"Human Anatomy of the Central Nervous System"
    },
    {
      "course_id":"010094",
      "subject":"KIN",
      "catalog_number":"307",
      "title":"Methods in Physiological Research"
    },
    {
      "course_id":"012037",
      "subject":"KIN",
      "catalog_number":"320",
      "title":"Task Analysis"
    },
    {
      "course_id":"006566",
      "subject":"KIN",
      "catalog_number":"330",
      "title":"Research Design"
    },
    {
      "course_id":"006568",
      "subject":"KIN",
      "catalog_number":"340",
      "title":"Musculoskeletal Injuries in Work and Sport"
    },
    {
      "course_id":"006569",
      "subject":"KIN",
      "catalog_number":"341",
      "title":"Selected Topics in Sport and Work Injuries"
    },
    {
      "course_id":"014695",
      "subject":"KIN",
      "catalog_number":"342",
      "title":"Nutrition and Aging"
    },
    {
      "course_id":"014696",
      "subject":"KIN",
      "catalog_number":"343",
      "title":"Micronutrient Metabolism"
    },
    {
      "course_id":"006434",
      "subject":"KIN",
      "catalog_number":"346",
      "title":"Human Nutrition"
    },
    {
      "course_id":"006438",
      "subject":"KIN",
      "catalog_number":"352",
      "title":"Sociology of Aging"
    },
    {
      "course_id":"006574",
      "subject":"KIN",
      "catalog_number":"354",
      "title":"Psychology of Physical Activity"
    },
    {
      "course_id":"006575",
      "subject":"KIN",
      "catalog_number":"356",
      "title":"Information Processing in Human Perceptual Motor Performance"
    },
    {
      "course_id":"006576",
      "subject":"KIN",
      "catalog_number":"357",
      "title":"Motor Learning"
    },
    {
      "course_id":"012118",
      "subject":"KIN",
      "catalog_number":"372",
      "title":"International Exchange"
    },
    {
      "course_id":"009507",
      "subject":"KIN",
      "catalog_number":"391",
      "title":"Research Apprenticeship"
    },
    {
      "course_id":"006578",
      "subject":"KIN",
      "catalog_number":"402",
      "title":"Microgravity, Hypo- and Hyperbaric Physiology"
    },
    {
      "course_id":"011125",
      "subject":"KIN",
      "catalog_number":"403",
      "title":"Occupational and Environmental Physiology"
    },
    {
      "course_id":"012966",
      "subject":"KIN",
      "catalog_number":"404",
      "title":"Physiological Basis of Obesity and Type 2 Diabetes"
    },
    {
      "course_id":"006579",
      "subject":"KIN",
      "catalog_number":"405",
      "title":"Exercise Management"
    },
    {
      "course_id":"012967",
      "subject":"KIN",
      "catalog_number":"406",
      "title":"Physiology of Muscle Aging and Disease"
    },
    {
      "course_id":"006441",
      "subject":"KIN",
      "catalog_number":"407",
      "title":"Coronary Artery Disease - Prevention and Rehabilitation"
    },
    {
      "course_id":"013375",
      "subject":"KIN",
      "catalog_number":"408",
      "title":"Cardiovascular Physiology and Pathophysiology"
    },
    {
      "course_id":"012554",
      "subject":"KIN",
      "catalog_number":"415",
      "title":"Clinical Neurophysiology: Fundamentals for Rehabilitation of Human Movement"
    },
    {
      "course_id":"006581",
      "subject":"KIN",
      "catalog_number":"416",
      "title":"Neuromuscular Integration"
    },
    {
      "course_id":"013376",
      "subject":"KIN",
      "catalog_number":"418",
      "title":"Age-Related Physical and Mental Changes and Effect of Exercise on Improving Health in the Aged"
    },
    {
      "course_id":"006582",
      "subject":"KIN",
      "catalog_number":"420",
      "title":"Occupational Biomechanics"
    },
    {
      "course_id":"006583",
      "subject":"KIN",
      "catalog_number":"422",
      "title":"Human Gait, Posture, and Balance: Pathological and Aging Considerations"
    },
    {
      "course_id":"006584",
      "subject":"KIN",
      "catalog_number":"425",
      "title":"Biomechanical Modelling of Human Movement"
    },
    {
      "course_id":"011844",
      "subject":"KIN",
      "catalog_number":"427",
      "title":"Low Back Disorders"
    },
    {
      "course_id":"012555",
      "subject":"KIN",
      "catalog_number":"428",
      "title":"Upper Extremity Musculoskeletal Disorders: Prevention, Assessment, and Rehabilitation"
    },
    {
      "course_id":"012556",
      "subject":"KIN",
      "catalog_number":"429",
      "title":"Bone and Joint Health"
    },
    {
      "course_id":"006586",
      "subject":"KIN",
      "catalog_number":"431",
      "title":"Research Proposal"
    },
    {
      "course_id":"006601",
      "subject":"KIN",
      "catalog_number":"432",
      "title":"Research Project"
    },
    {
      "course_id":"006616",
      "subject":"KIN",
      "catalog_number":"433",
      "title":"Senior Essay"
    },
    {
      "course_id":"011559",
      "subject":"KIN",
      "catalog_number":"440",
      "title":"Sport Injury Management Seminar"
    },
    {
      "course_id":"012557",
      "subject":"KIN",
      "catalog_number":"446",
      "title":"Physiological and Biochemical Aspects of Nutrition and Health"
    },
    {
      "course_id":"012119",
      "subject":"KIN",
      "catalog_number":"451",
      "title":"Social Aspects of Injury in Work and Sport"
    },
    {
      "course_id":"006631",
      "subject":"KIN",
      "catalog_number":"453",
      "title":"The Psychology of Sport and Physical Activity"
    },
    {
      "course_id":"006632",
      "subject":"KIN",
      "catalog_number":"456",
      "title":"Cognitive Dysfunction and Motor Skill"
    },
    {
      "course_id":"006633",
      "subject":"KIN",
      "catalog_number":"457",
      "title":"Cognitive, Perceptual and Motor Assessment"
    },
    {
      "course_id":"014378",
      "subject":"KIN",
      "catalog_number":"458",
      "title":"Social Neuroscience and Health"
    },
    {
      "course_id":"006634",
      "subject":"KIN",
      "catalog_number":"470",
      "title":"Seminar in Kinesiology"
    },
    {
      "course_id":"006635",
      "subject":"KIN",
      "catalog_number":"470E",
      "title":"Seminar in Integrative Ergonomics"
    },
    {
      "course_id":"012777",
      "subject":"KIN",
      "catalog_number":"471",
      "title":"Contemporary Issues in Kinesiology"
    },
    {
      "course_id":"006640",
      "subject":"KIN",
      "catalog_number":"472",
      "title":"Directed Study in Special Topics"
    },
    {
      "course_id":"006661",
      "subject":"KIN",
      "catalog_number":"491",
      "title":"Clinical Kinesiology -- Sports Injuries Assessment"
    },
    {
      "course_id":"006662",
      "subject":"KIN",
      "catalog_number":"492A",
      "title":"Clinical Kinesiology -- Cardiac Rehabilitation Practicum"
    },
    {
      "course_id":"006663",
      "subject":"KIN",
      "catalog_number":"492B",
      "title":"Clinical Kinesiology -- Cardiac Rehabilitation Practicum"
    },
    {
      "course_id":"006664",
      "subject":"KIN",
      "catalog_number":"493",
      "title":"Clinical Kinesiology: Movement Assessment Practicum"
    },
    {
      "course_id":"006665",
      "subject":"KIN",
      "catalog_number":"494",
      "title":"Integrative Ergonomics Practicum"
    },
    {
      "course_id":"001745",
      "subject":"KIN",
      "catalog_number":"601",
      "title":"Muscle Physiology"
    },
    {
      "course_id":"001746",
      "subject":"KIN",
      "catalog_number":"602",
      "title":"Respiratory and Cardiovascular Physiology"
    },
    {
      "course_id":"013459",
      "subject":"KIN",
      "catalog_number":"606",
      "title":"Molecular Basis of Disease"
    },
    {
      "course_id":"013453",
      "subject":"KIN",
      "catalog_number":"607",
      "title":"Integrative Energy Metabolism in Health and Disease"
    },
    {
      "course_id":"001748",
      "subject":"KIN",
      "catalog_number":"611",
      "title":"Biomechanics of Human Motion"
    },
    {
      "course_id":"001749",
      "subject":"KIN",
      "catalog_number":"612",
      "title":"Instrumentation and Signal Processing in Biophysical Research"
    },
    {
      "course_id":"014288",
      "subject":"KIN",
      "catalog_number":"613",
      "title":"Modern Methods in Biomechanical Modeling, Kinematics, and Kinetics"
    },
    {
      "course_id":"001750",
      "subject":"KIN",
      "catalog_number":"616",
      "title":"Neural Control of Human Movement"
    },
    {
      "course_id":"001751",
      "subject":"KIN",
      "catalog_number":"620",
      "title":"Ergonomic Aspects of Occupational Musculoskeletal Injuries"
    },
    {
      "course_id":"001753",
      "subject":"KIN",
      "catalog_number":"625",
      "title":"The Social Psychology of Sport and Motor Performance"
    },
    {
      "course_id":"001754",
      "subject":"KIN",
      "catalog_number":"631A",
      "title":"Introduction to Statistics"
    },
    {
      "course_id":"001755",
      "subject":"KIN",
      "catalog_number":"631C",
      "title":"Correlation and Regression"
    },
    {
      "course_id":"001756",
      "subject":"KIN",
      "catalog_number":"631D",
      "title":"Logistic Regression and Its Application"
    },
    {
      "course_id":"001757",
      "subject":"KIN",
      "catalog_number":"631E",
      "title":"Analysis of Variance I"
    },
    {
      "course_id":"001758",
      "subject":"KIN",
      "catalog_number":"631F",
      "title":"Analysis of Variance II"
    },
    {
      "course_id":"001759",
      "subject":"KIN",
      "catalog_number":"631G",
      "title":"Biological Deterministic Modelling and Signal Processing"
    },
    {
      "course_id":"013455",
      "subject":"KIN",
      "catalog_number":"646",
      "title":"Physiological and Biochemical Aspects of Nutrition and Health"
    },
    {
      "course_id":"001760",
      "subject":"KIN",
      "catalog_number":"651",
      "title":"Motor Learning"
    },
    {
      "course_id":"001761",
      "subject":"KIN",
      "catalog_number":"652",
      "title":"Movement Control and Learning"
    },
    {
      "course_id":"013457",
      "subject":"KIN",
      "catalog_number":"653",
      "title":"Human Neuroscience Theory"
    },
    {
      "course_id":"013458",
      "subject":"KIN",
      "catalog_number":"654",
      "title":"Instrumentation in Neuroscience Research"
    },
    {
      "course_id":"001762",
      "subject":"KIN",
      "catalog_number":"656",
      "title":"Neurobehavioural Analyses of  Perceptual and Motor Deficits"
    },
    {
      "course_id":"010540",
      "subject":"KIN",
      "catalog_number":"670A",
      "title":"Movement Neuroscience Seminar"
    },
    {
      "course_id":"010541",
      "subject":"KIN",
      "catalog_number":"670B",
      "title":"Behavioual Neuroscience Seminar"
    },
    {
      "course_id":"001763",
      "subject":"KIN",
      "catalog_number":"670C",
      "title":"Seminar 1: Motor Learning"
    },
    {
      "course_id":"001764",
      "subject":"KIN",
      "catalog_number":"670D",
      "title":"Seminar 1: Psychomotor Behavior"
    },
    {
      "course_id":"001765",
      "subject":"KIN",
      "catalog_number":"670E",
      "title":"Seminar 1:  Biomechanics and Ergonomics"
    },
    {
      "course_id":"001766",
      "subject":"KIN",
      "catalog_number":"670F",
      "title":"Seminar 1: Biomechanics and Rehabilitation"
    },
    {
      "course_id":"001767",
      "subject":"KIN",
      "catalog_number":"670H",
      "title":"Physiology and Nutrition Part One"
    },
    {
      "course_id":"001768",
      "subject":"KIN",
      "catalog_number":"670I",
      "title":"Physiology and Nutrition Part Two"
    },
    {
      "course_id":"001769",
      "subject":"KIN",
      "catalog_number":"680",
      "title":"Selected Topics in Physiology and Nutrition"
    },
    {
      "course_id":"009476",
      "subject":"KIN",
      "catalog_number":"682",
      "title":"Selected Topics in Biomechanics"
    },
    {
      "course_id":"001799",
      "subject":"KIN",
      "catalog_number":"700",
      "title":"Muscle Metabolism in Work"
    },
    {
      "course_id":"010542",
      "subject":"KIN",
      "catalog_number":"684",
      "title":"Selected Topics in the Social Science of Sport"
    },
    {
      "course_id":"001790",
      "subject":"KIN",
      "catalog_number":"686",
      "title":"Selected Topics in Neuroscience I"
    },
    {
      "course_id":"002626",
      "subject":"KIN",
      "catalog_number":"687",
      "title":"Fundamentals of Behavioural Neuroscience"
    },
    {
      "course_id":"001800",
      "subject":"KIN",
      "catalog_number":"702",
      "title":"Cardiorespiratory Integration"
    },
    {
      "course_id":"013460",
      "subject":"KIN",
      "catalog_number":"704",
      "title":"Bioactive Lipids"
    },
    {
      "course_id":"001802",
      "subject":"KIN",
      "catalog_number":"713",
      "title":"Modelling of Human Musculoskeletal System during Movement"
    },
    {
      "course_id":"001803",
      "subject":"KIN",
      "catalog_number":"714",
      "title":"Advanced Electromyography"
    },
    {
      "course_id":"001804",
      "subject":"KIN",
      "catalog_number":"715",
      "title":"Assessment of Pathological Movement"
    },
    {
      "course_id":"011876",
      "subject":"KIN",
      "catalog_number":"727",
      "title":"Low Back Disorders: Optimizing Prevention, Rehabilitation and Performance"
    },
    {
      "course_id":"013139",
      "subject":"KIN",
      "catalog_number":"730",
      "title":"Fundamentals of Work and Health"
    },
    {
      "course_id":"013140",
      "subject":"KIN",
      "catalog_number":"731",
      "title":"Approaches to Research in Work and Health"
    },
    {
      "course_id":"013141",
      "subject":"KIN",
      "catalog_number":"732A",
      "title":"Work and Health Research Seminar (I)"
    },
    {
      "course_id":"013142",
      "subject":"KIN",
      "catalog_number":"732B",
      "title":"Work and Health Research Seminar (II)"
    },
    {
      "course_id":"012422",
      "subject":"KIN",
      "catalog_number":"750",
      "title":"Fundamentals of Aging, Health and Well-being"
    },
    {
      "course_id":"012426",
      "subject":"KIN",
      "catalog_number":"751",
      "title":"Aging, Health and Well-being Research Seminar"
    },
    {
      "course_id":"010546",
      "subject":"KIN",
      "catalog_number":"760",
      "title":"Selected Topics Neuroscience II"
    },
    {
      "course_id":"012869",
      "subject":"KIN",
      "catalog_number":"775",
      "title":"Key Issues and Concerns in Kinesiology"
    },
    {
      "course_id":"001820",
      "subject":"KIN",
      "catalog_number":"780",
      "title":"Selected Topics in Physiology and Nutrition"
    },
    {
      "course_id":"009477",
      "subject":"KIN",
      "catalog_number":"782",
      "title":"Selected Topics in Biomechanics"
    },
    {
      "course_id":"013078",
      "subject":"LAT",
      "catalog_number":"621",
      "title":"Latin Epigraphy"
    },
    {
      "course_id":"006666",
      "subject":"KOREA",
      "catalog_number":"101R",
      "title":"First-Year Korean 1"
    },
    {
      "course_id":"006667",
      "subject":"KOREA",
      "catalog_number":"102R",
      "title":"First-Year Korean 2"
    },
    {
      "course_id":"006668",
      "subject":"KOREA",
      "catalog_number":"201R",
      "title":"Second-Year Korean 1"
    },
    {
      "course_id":"009930",
      "subject":"KOREA",
      "catalog_number":"202R",
      "title":"Second-Year Korean 2"
    },
    {
      "course_id":"013998",
      "subject":"KOREA",
      "catalog_number":"272R",
      "title":"Korean Culture and Society"
    },
    {
      "course_id":"006670",
      "subject":"LAT",
      "catalog_number":"101",
      "title":"Introductory Latin 1"
    },
    {
      "course_id":"006671",
      "subject":"LAT",
      "catalog_number":"102",
      "title":"Introductory Latin 2"
    },
    {
      "course_id":"006673",
      "subject":"LAT",
      "catalog_number":"201",
      "title":"Intermediate Latin"
    },
    {
      "course_id":"006674",
      "subject":"LAT",
      "catalog_number":"202",
      "title":"Selections from Latin Authors"
    },
    {
      "course_id":"006674",
      "subject":"LAT",
      "catalog_number":"202W",
      "title":"Selections from Latin Authors"
    },
    {
      "course_id":"012923",
      "subject":"LAT",
      "catalog_number":"331",
      "title":"Advanced Readings in Latin: Prose"
    },
    {
      "course_id":"012924",
      "subject":"LAT",
      "catalog_number":"332",
      "title":"Advanced Readings in Latin: Poetry"
    },
    {
      "course_id":"012925",
      "subject":"LAT",
      "catalog_number":"341",
      "title":"Advanced Studies in Latin: Selected Topics"
    },
    {
      "course_id":"006678",
      "subject":"LAT",
      "catalog_number":"351",
      "title":"Latin Composition, Grammar and Reading"
    },
    {
      "course_id":"006689",
      "subject":"LAT",
      "catalog_number":"381",
      "title":"Medieval Latin"
    },
    {
      "course_id":"006692",
      "subject":"LAT",
      "catalog_number":"421",
      "title":"Latin Epigraphy"
    },
    {
      "course_id":"011788",
      "subject":"LAT",
      "catalog_number":"422",
      "title":"Latin Palaeography"
    },
    {
      "course_id":"012186",
      "subject":"LAT",
      "catalog_number":"451",
      "title":"Senior Latin Composition, Grammar and Reading"
    },
    {
      "course_id":"009936",
      "subject":"LAT",
      "catalog_number":"490",
      "title":"Senior Studies in Latin: Selected Topics"
    },
    {
      "course_id":"009945",
      "subject":"LAT",
      "catalog_number":"491",
      "title":"Senior Studies in Latin: Independent Study"
    },
    {
      "course_id":"014423",
      "subject":"LAT",
      "catalog_number":"600",
      "title":"Topics in Latin Language"
    },
    {
      "course_id":"014422",
      "subject":"LAT",
      "catalog_number":"601",
      "title":"Topics in Greek Language"
    },
    {
      "course_id":"001839",
      "subject":"LED",
      "catalog_number":"611",
      "title":"Industrial Location Theory and Concepts"
    },
    {
      "course_id":"011469",
      "subject":"LED",
      "catalog_number":"612",
      "title":"Land Development Planning"
    },
    {
      "course_id":"001841",
      "subject":"LED",
      "catalog_number":"613",
      "title":"Regional Development Principles and Practice"
    },
    {
      "course_id":"001842",
      "subject":"LED",
      "catalog_number":"615",
      "title":"Community Economic Development"
    },
    {
      "course_id":"002245",
      "subject":"LED",
      "catalog_number":"619",
      "title":"Regional Planning Economic and Investment Analysis"
    },
    {
      "course_id":"012790",
      "subject":"LED",
      "catalog_number":"621",
      "title":"Environment & Business"
    },
    {
      "course_id":"001400",
      "subject":"LED",
      "catalog_number":"671",
      "title":"Contemporary Perspectives on Tourism"
    },
    {
      "course_id":"001843",
      "subject":"LED",
      "catalog_number":"685",
      "title":"Theory of Local Economic Development"
    },
    {
      "course_id":"001844",
      "subject":"LED",
      "catalog_number":"686",
      "title":"Practice of Local Economic Development"
    },
    {
      "course_id":"001845",
      "subject":"LED",
      "catalog_number":"687",
      "title":"Communication, Market Research and Marketing for the Public Sector"
    },
    {
      "course_id":"001846",
      "subject":"LED",
      "catalog_number":"688",
      "title":"Entrepreneurship and Small Business Development"
    },
    {
      "course_id":"011710",
      "subject":"LS",
      "catalog_number":"101",
      "title":"Introduction to Legal Studies"
    },
    {
      "course_id":"011711",
      "subject":"LS",
      "catalog_number":"102",
      "title":"Introduction to Criminal Law"
    },
    {
      "course_id":"012768",
      "subject":"LS",
      "catalog_number":"201",
      "title":"Women and the Law"
    },
    {
      "course_id":"008645",
      "subject":"LS",
      "catalog_number":"280",
      "title":"Social Statistics"
    },
    {
      "course_id":"008661",
      "subject":"LS",
      "catalog_number":"321",
      "title":"Introduction to Research Methods"
    },
    {
      "course_id":"008664",
      "subject":"LS",
      "catalog_number":"322",
      "title":"Field Research Methods"
    },
    {
      "course_id":"011899",
      "subject":"LS",
      "catalog_number":"401",
      "title":"Law, Culture, and Rights"
    },
    {
      "course_id":"011900",
      "subject":"LS",
      "catalog_number":"402",
      "title":"Perspectives on Legal Authority and Subjectivity"
    },
    {
      "course_id":"013627",
      "subject":"LS",
      "catalog_number":"403",
      "title":"Socio-Legal Responses to Crime"
    },
    {
      "course_id":"013626",
      "subject":"LS",
      "catalog_number":"496",
      "title":"Special Topics in Legal Studies"
    },
    {
      "course_id":"012278",
      "subject":"LS",
      "catalog_number":"498",
      "title":"Directed Readings in Legal Studies"
    },
    {
      "course_id":"013755",
      "subject":"MATBUS",
      "catalog_number":"470",
      "title":"Derivatives"
    },
    {
      "course_id":"013865",
      "subject":"MATBUS",
      "catalog_number":"471",
      "title":"Fixed Income Securities"
    },
    {
      "course_id":"013866",
      "subject":"MATBUS",
      "catalog_number":"472",
      "title":"Risk Management"
    },
    {
      "course_id":"010374",
      "subject":"MATH",
      "catalog_number":"51",
      "title":"Pre-University Algebra and Geometry"
    },
    {
      "course_id":"010375",
      "subject":"MATH",
      "catalog_number":"52",
      "title":"Pre-University Calculus"
    },
    {
      "course_id":"010113",
      "subject":"MATH",
      "catalog_number":"97",
      "title":"Study Abroad"
    },
    {
      "course_id":"006847",
      "subject":"MATH",
      "catalog_number":"103",
      "title":"Introductory Algebra for Arts and Social Science"
    },
    {
      "course_id":"006848",
      "subject":"MATH",
      "catalog_number":"104",
      "title":"Introductory Calculus for Arts and Social Science"
    },
    {
      "course_id":"006869",
      "subject":"MATH",
      "catalog_number":"106",
      "title":"Applied Linear Algebra 1"
    },
    {
      "course_id":"006853",
      "subject":"MATH",
      "catalog_number":"109",
      "title":"Mathematics for Accounting"
    },
    {
      "course_id":"011645",
      "subject":"MATH",
      "catalog_number":"114",
      "title":"Linear Algebra for Science"
    },
    {
      "course_id":"006862",
      "subject":"MATH",
      "catalog_number":"115",
      "title":"Linear Algebra for Engineering"
    },
    {
      "course_id":"006865",
      "subject":"MATH",
      "catalog_number":"116",
      "title":"Calculus 1 for Engineering"
    },
    {
      "course_id":"006866",
      "subject":"MATH",
      "catalog_number":"117",
      "title":"Calculus 1 for Engineering"
    },
    {
      "course_id":"006867",
      "subject":"MATH",
      "catalog_number":"118",
      "title":"Calculus 2 for Engineering"
    },
    {
      "course_id":"006868",
      "subject":"MATH",
      "catalog_number":"119",
      "title":"Calculus 2 for Engineering"
    },
    {
      "course_id":"012879",
      "subject":"MATH",
      "catalog_number":"124",
      "title":"Calculus and Vector Algebra for Kinesiology"
    },
    {
      "course_id":"006871",
      "subject":"MATH",
      "catalog_number":"127",
      "title":"Calculus 1 for the Sciences"
    },
    {
      "course_id":"006872",
      "subject":"MATH",
      "catalog_number":"128",
      "title":"Calculus 2 for the Sciences"
    },
    {
      "course_id":"006878",
      "subject":"MATH",
      "catalog_number":"135",
      "title":"Algebra for Honours Mathematics"
    },
    {
      "course_id":"006879",
      "subject":"MATH",
      "catalog_number":"136",
      "title":"Linear Algebra 1 for Honours Mathematics"
    },
    {
      "course_id":"006880",
      "subject":"MATH",
      "catalog_number":"137",
      "title":"Calculus 1 for Honours Mathematics"
    },
    {
      "course_id":"006881",
      "subject":"MATH",
      "catalog_number":"138",
      "title":"Calculus 2 For Honours Mathematics"
    },
    {
      "course_id":"015053",
      "subject":"MATH",
      "catalog_number":"661",
      "title":"Problem Solving and Proof in Geometry"
    },
    {
      "course_id":"006886",
      "subject":"MATH",
      "catalog_number":"145",
      "title":"Algebra (Advanced Level)"
    },
    {
      "course_id":"006887",
      "subject":"MATH",
      "catalog_number":"146",
      "title":"Linear Algebra 1 (Advanced level)"
    },
    {
      "course_id":"006888",
      "subject":"MATH",
      "catalog_number":"147",
      "title":"Calculus 1 (Advanced Level)"
    },
    {
      "course_id":"006889",
      "subject":"MATH",
      "catalog_number":"148",
      "title":"Calculus 2 (Advanced Level)"
    },
    {
      "course_id":"013105",
      "subject":"MATH",
      "catalog_number":"207",
      "title":"Calculus 3 (Non-Specialist Level)"
    },
    {
      "course_id":"006891",
      "subject":"MATH",
      "catalog_number":"211",
      "title":"Advanced Calculus 1 for Electrical and Computer Engineers"
    },
    {
      "course_id":"006892",
      "subject":"MATH",
      "catalog_number":"212",
      "title":"Advanced Calculus 2 for Electrical Engineers"
    },
    {
      "course_id":"011849",
      "subject":"MATH",
      "catalog_number":"213",
      "title":"Advanced Mathematics for Software Engineers"
    },
    {
      "course_id":"013464",
      "subject":"MATH",
      "catalog_number":"215",
      "title":"Linear Algebra for Engineering"
    },
    {
      "course_id":"006897",
      "subject":"MATH",
      "catalog_number":"217",
      "title":"Calculus 3 for Chemical Engineering"
    },
    {
      "course_id":"006898",
      "subject":"MATH",
      "catalog_number":"218",
      "title":"Differential Equations for Engineers"
    },
    {
      "course_id":"006870",
      "subject":"MATH",
      "catalog_number":"225",
      "title":"Applied Linear Algebra 2"
    },
    {
      "course_id":"006907",
      "subject":"MATH",
      "catalog_number":"227",
      "title":"Calculus 3 for Honours Physics"
    },
    {
      "course_id":"006908",
      "subject":"MATH",
      "catalog_number":"228",
      "title":"Differential Equations for Physics and Chemistry"
    },
    {
      "course_id":"013104",
      "subject":"MATH",
      "catalog_number":"229",
      "title":"Introduction to Combinatorics (Non-Specialist Level)"
    },
    {
      "course_id":"006913",
      "subject":"MATH",
      "catalog_number":"235",
      "title":"Linear Algebra 2 for Honours Mathematics"
    },
    {
      "course_id":"006914",
      "subject":"MATH",
      "catalog_number":"237",
      "title":"Calculus 3 for Honours Mathematics"
    },
    {
      "course_id":"006915",
      "subject":"MATH",
      "catalog_number":"239",
      "title":"Introduction to Combinatorics"
    },
    {
      "course_id":"014804",
      "subject":"MATH",
      "catalog_number":"636",
      "title":"Linear Algebra for Teachers"
    },
    {
      "course_id":"006920",
      "subject":"MATH",
      "catalog_number":"245",
      "title":"Linear Algebra 2 (Advanced Level)"
    },
    {
      "course_id":"006921",
      "subject":"MATH",
      "catalog_number":"247",
      "title":"Calculus 3 (Advanced Level)"
    },
    {
      "course_id":"006922",
      "subject":"MATH",
      "catalog_number":"249",
      "title":"Introduction to Combinatorics (Advanced Level)"
    },
    {
      "course_id":"013923",
      "subject":"MATH",
      "catalog_number":"600",
      "title":"Introduction to Mathematical Software for Teachers"
    },
    {
      "course_id":"013831",
      "subject":"MATH",
      "catalog_number":"630",
      "title":"Foundations of Probability"
    },
    {
      "course_id":"014701",
      "subject":"MATH",
      "catalog_number":"631",
      "title":"Statistics for Teachers"
    },
    {
      "course_id":"014212",
      "subject":"MATH",
      "catalog_number":"640",
      "title":"Number Theory for Teachers"
    },
    {
      "course_id":"014340",
      "subject":"MATH",
      "catalog_number":"641",
      "title":"Algorithm Design and Analysis"
    },
    {
      "course_id":"013841",
      "subject":"MATH",
      "catalog_number":"647",
      "title":"Foundations of Calculus I"
    },
    {
      "course_id":"013840",
      "subject":"MATH",
      "catalog_number":"648",
      "title":"Foundations of Calculus II"
    },
    {
      "course_id":"014058",
      "subject":"MATH",
      "catalog_number":"650",
      "title":"Mathematical Modeling with Differential Equations"
    },
    {
      "course_id":"013833",
      "subject":"MATH",
      "catalog_number":"660",
      "title":"Explorations in Geometry"
    },
    {
      "course_id":"014213",
      "subject":"MATH",
      "catalog_number":"674",
      "title":"Special Topics in Mathematical Connections"
    },
    {
      "course_id":"013842",
      "subject":"MATH",
      "catalog_number":"680",
      "title":"History of Mathematics"
    },
    {
      "course_id":"013835",
      "subject":"MATH",
      "catalog_number":"681",
      "title":"Problem Solving and Mathematical Discovery"
    },
    {
      "course_id":"013834",
      "subject":"MATH",
      "catalog_number":"690",
      "title":"Summer Conference for Teachers of Mathematics"
    },
    {
      "course_id":"009357",
      "subject":"MATH",
      "catalog_number":"692",
      "title":"Reading, Writing and Discovering Proofs"
    },
    {
      "course_id":"014236",
      "subject":"MATH",
      "catalog_number":"698",
      "title":"Reading Course in Mathematics for Teachers"
    },
    {
      "course_id":"013832",
      "subject":"MATH",
      "catalog_number":"699",
      "title":"Master of Mathematics for Teachers Capstone"
    },
    {
      "course_id":"014344",
      "subject":"MATH",
      "catalog_number":"700",
      "title":"Math for Teachers - OVGS Transfer Course"
    },
    {
      "course_id":"006703",
      "subject":"ME",
      "catalog_number":"100",
      "title":"Introduction to Mechanical Engineering Practice 1"
    },
    {
      "course_id":"013359",
      "subject":"ME",
      "catalog_number":"100B",
      "title":"Seminar"
    },
    {
      "course_id":"014560",
      "subject":"ME",
      "catalog_number":"101",
      "title":"Introduction to Mechanical Engineering Practice 2"
    },
    {
      "course_id":"006710",
      "subject":"ME",
      "catalog_number":"115",
      "title":"Structure and Properties of Materials"
    },
    {
      "course_id":"009306",
      "subject":"ME",
      "catalog_number":"200A",
      "title":"Seminar"
    },
    {
      "course_id":"009305",
      "subject":"ME",
      "catalog_number":"200B",
      "title":"Seminar"
    },
    {
      "course_id":"006706",
      "subject":"ME",
      "catalog_number":"201",
      "title":"Advanced Calculus"
    },
    {
      "course_id":"006707",
      "subject":"ME",
      "catalog_number":"202",
      "title":"Statistics for Engineers"
    },
    {
      "course_id":"006708",
      "subject":"ME",
      "catalog_number":"203",
      "title":"Ordinary Differential Equations"
    },
    {
      "course_id":"006709",
      "subject":"ME",
      "catalog_number":"212",
      "title":"Dynamics"
    },
    {
      "course_id":"006711",
      "subject":"ME",
      "catalog_number":"219",
      "title":"Mechanics of Deformable Solids 1"
    },
    {
      "course_id":"006712",
      "subject":"ME",
      "catalog_number":"220",
      "title":"Mechanics of Deformable Solids 2"
    },
    {
      "course_id":"006713",
      "subject":"ME",
      "catalog_number":"230",
      "title":"Control of Properties of Materials"
    },
    {
      "course_id":"012406",
      "subject":"ME",
      "catalog_number":"235",
      "title":"Materials Science and Engineering"
    },
    {
      "course_id":"006714",
      "subject":"ME",
      "catalog_number":"250",
      "title":"Thermodynamics 1"
    },
    {
      "course_id":"006715",
      "subject":"ME",
      "catalog_number":"262",
      "title":"Introduction to Microprocessors and Digital Logic"
    },
    {
      "course_id":"006716",
      "subject":"ME",
      "catalog_number":"269",
      "title":"Electromechanical Devices and Power Processing"
    },
    {
      "course_id":"009307",
      "subject":"ME",
      "catalog_number":"300A",
      "title":"Seminar"
    },
    {
      "course_id":"009308",
      "subject":"ME",
      "catalog_number":"300B",
      "title":"Seminar"
    },
    {
      "course_id":"006718",
      "subject":"ME",
      "catalog_number":"303",
      "title":"Advanced Engineering Mathematics"
    },
    {
      "course_id":"006721",
      "subject":"ME",
      "catalog_number":"321",
      "title":"Kinematics and Dynamics of Machines"
    },
    {
      "course_id":"006722",
      "subject":"ME",
      "catalog_number":"322",
      "title":"Mechanical Design 1"
    },
    {
      "course_id":"006724",
      "subject":"ME",
      "catalog_number":"340",
      "title":"Manufacturing Processes"
    },
    {
      "course_id":"006725",
      "subject":"ME",
      "catalog_number":"351",
      "title":"Fluid Mechanics 1"
    },
    {
      "course_id":"006726",
      "subject":"ME",
      "catalog_number":"353",
      "title":"Heat Transfer 1"
    },
    {
      "course_id":"006727",
      "subject":"ME",
      "catalog_number":"354",
      "title":"Thermodynamics 2"
    },
    {
      "course_id":"006728",
      "subject":"ME",
      "catalog_number":"360",
      "title":"Introduction to Control Systems"
    },
    {
      "course_id":"006729",
      "subject":"ME",
      "catalog_number":"362",
      "title":"Fluid Mechanics 2"
    },
    {
      "course_id":"006731",
      "subject":"ME",
      "catalog_number":"380",
      "title":"Mechanical Engineering Design Workshop"
    },
    {
      "course_id":"009310",
      "subject":"ME",
      "catalog_number":"400A",
      "title":"Seminar"
    },
    {
      "course_id":"009311",
      "subject":"ME",
      "catalog_number":"400B",
      "title":"Seminar"
    },
    {
      "course_id":"006732",
      "subject":"ME",
      "catalog_number":"401",
      "title":"Law for the Professional Engineer"
    },
    {
      "course_id":"006734",
      "subject":"ME",
      "catalog_number":"423",
      "title":"Mechanical Design 2"
    },
    {
      "course_id":"006736",
      "subject":"ME",
      "catalog_number":"435",
      "title":"Industrial Metallurgy"
    },
    {
      "course_id":"006755",
      "subject":"ME",
      "catalog_number":"436",
      "title":"Welding and Joining Processes"
    },
    {
      "course_id":"006739",
      "subject":"ME",
      "catalog_number":"452",
      "title":"Energy Transfer in Buildings"
    },
    {
      "course_id":"006740",
      "subject":"ME",
      "catalog_number":"456",
      "title":"Heat Transfer 2"
    },
    {
      "course_id":"006741",
      "subject":"ME",
      "catalog_number":"459",
      "title":"Energy Conversion"
    },
    {
      "course_id":"006745",
      "subject":"ME",
      "catalog_number":"481",
      "title":"Mechanical Engineering Design Project 1"
    },
    {
      "course_id":"006746",
      "subject":"ME",
      "catalog_number":"482",
      "title":"Mechanical Engineering Design Project 2"
    },
    {
      "course_id":"006748",
      "subject":"ME",
      "catalog_number":"524",
      "title":"Advanced Dynamics and Vibrations"
    },
    {
      "course_id":"010165",
      "subject":"ME",
      "catalog_number":"526",
      "title":"Fatigue and Fracture Analysis"
    },
    {
      "course_id":"006751",
      "subject":"ME",
      "catalog_number":"531",
      "title":"Physical Metallurgy Applied to Manufacturing"
    },
    {
      "course_id":"006752",
      "subject":"ME",
      "catalog_number":"533",
      "title":"Non-metallic and Composite Materials"
    },
    {
      "course_id":"006754",
      "subject":"ME",
      "catalog_number":"535",
      "title":"Welding Metallurgy"
    },
    {
      "course_id":"011726",
      "subject":"ME",
      "catalog_number":"538",
      "title":"Welding Design, Fabrication and Quality Control"
    },
    {
      "course_id":"006762",
      "subject":"ME",
      "catalog_number":"547",
      "title":"Robot Manipulators: Kinematics, Dynamics, Control"
    },
    {
      "course_id":"006763",
      "subject":"ME",
      "catalog_number":"548",
      "title":"Numerical Control of Machine Tools 1"
    },
    {
      "course_id":"006764",
      "subject":"ME",
      "catalog_number":"555",
      "title":"Computer-Aided Design"
    },
    {
      "course_id":"006765",
      "subject":"ME",
      "catalog_number":"557",
      "title":"Combustion 1"
    },
    {
      "course_id":"006766",
      "subject":"ME",
      "catalog_number":"559",
      "title":"Finite Element Methods"
    },
    {
      "course_id":"006767",
      "subject":"ME",
      "catalog_number":"561",
      "title":"Fluid Power Control Systems"
    },
    {
      "course_id":"006768",
      "subject":"ME",
      "catalog_number":"563",
      "title":"Turbomachines"
    },
    {
      "course_id":"006770",
      "subject":"ME",
      "catalog_number":"564",
      "title":"Aerodynamics"
    },
    {
      "course_id":"006772",
      "subject":"ME",
      "catalog_number":"566",
      "title":"Computational Fluid Dynamics for Engineering Design"
    },
    {
      "course_id":"012564",
      "subject":"ME",
      "catalog_number":"567",
      "title":"Fire Safety Engineering"
    },
    {
      "course_id":"006775",
      "subject":"ME",
      "catalog_number":"571",
      "title":"Air Pollution"
    },
    {
      "course_id":"006777",
      "subject":"ME",
      "catalog_number":"595",
      "title":"Special Topics in Mechanical Engineering"
    },
    {
      "course_id":"006779",
      "subject":"ME",
      "catalog_number":"596",
      "title":"Special Topics in Mechanical Engineering"
    },
    {
      "course_id":"010183",
      "subject":"ME",
      "catalog_number":"597",
      "title":"Special Topics in Mechanical Engineering"
    },
    {
      "course_id":"006780",
      "subject":"ME",
      "catalog_number":"598",
      "title":"Special Topics in Mechanical Engineering"
    },
    {
      "course_id":"006781",
      "subject":"ME",
      "catalog_number":"599",
      "title":"Special Topics in Mechanical Engineering"
    },
    {
      "course_id":"010310",
      "subject":"ME",
      "catalog_number":"610",
      "title":"Analytical Methods in Vibrations"
    },
    {
      "course_id":"001852",
      "subject":"ME",
      "catalog_number":"620",
      "title":"Mechanics of Continua"
    },
    {
      "course_id":"014596",
      "subject":"ME",
      "catalog_number":"621",
      "title":"Advanced Finite Element Methods"
    },
    {
      "course_id":"011268",
      "subject":"ME",
      "catalog_number":"627",
      "title":"Fatigue Analysis and Design"
    },
    {
      "course_id":"001855",
      "subject":"ME",
      "catalog_number":"628",
      "title":"Fracture Mechanics"
    },
    {
      "course_id":"001858",
      "subject":"ME",
      "catalog_number":"631",
      "title":"Mechanical Metallurgy"
    },
    {
      "course_id":"011466",
      "subject":"ME",
      "catalog_number":"632",
      "title":"Experimental Methods in Materials Engineering"
    },
    {
      "course_id":"001861",
      "subject":"ME",
      "catalog_number":"645",
      "title":"Metallurgy and Plasticity in Metalworking"
    },
    {
      "course_id":"001862",
      "subject":"ME",
      "catalog_number":"648",
      "title":"Surface Modelling in Machining"
    },
    {
      "course_id":"001863",
      "subject":"ME",
      "catalog_number":"649",
      "title":"Control of Machines and Processes"
    },
    {
      "course_id":"001864",
      "subject":"ME",
      "catalog_number":"651",
      "title":"Heat Conduction"
    },
    {
      "course_id":"001865",
      "subject":"ME",
      "catalog_number":"652",
      "title":"Convective Heat Transfer"
    },
    {
      "course_id":"001866",
      "subject":"ME",
      "catalog_number":"653",
      "title":"Radiation Heat Transfer"
    },
    {
      "course_id":"001868",
      "subject":"ME",
      "catalog_number":"662",
      "title":"Advanced Fluid Mechanics"
    },
    {
      "course_id":"010455",
      "subject":"ME",
      "catalog_number":"663",
      "title":"Computational Fluid Dynamics"
    },
    {
      "course_id":"001869",
      "subject":"ME",
      "catalog_number":"664",
      "title":"Turbulent Flow"
    },
    {
      "course_id":"001870",
      "subject":"ME",
      "catalog_number":"670",
      "title":"Atmospheric Dynamics"
    },
    {
      "course_id":"001873",
      "subject":"ME",
      "catalog_number":"705",
      "title":"Special Topics in Tribology"
    },
    {
      "course_id":"001874",
      "subject":"ME",
      "catalog_number":"706",
      "title":"Advanced Tribology"
    },
    {
      "course_id":"010456",
      "subject":"ME",
      "catalog_number":"707",
      "title":"Machinery Noise and Vibration Analysis"
    },
    {
      "course_id":"001875",
      "subject":"ME",
      "catalog_number":"709",
      "title":"Control Engineering and Mechanical Systems"
    },
    {
      "course_id":"001876",
      "subject":"ME",
      "catalog_number":"710",
      "title":"Special Topics in Control Systems"
    },
    {
      "course_id":"001877",
      "subject":"ME",
      "catalog_number":"711",
      "title":"Non-Linear Vibrations"
    },
    {
      "course_id":"012233",
      "subject":"ME",
      "catalog_number":"720",
      "title":"Special Topics in Solid Mechanics"
    },
    {
      "course_id":"001879",
      "subject":"ME",
      "catalog_number":"722",
      "title":"Topics in Pressure Vessel Design"
    },
    {
      "course_id":"001883",
      "subject":"ME",
      "catalog_number":"725",
      "title":"Special Topics in Advanced Stress Analysis"
    },
    {
      "course_id":"010457",
      "subject":"ME",
      "catalog_number":"729",
      "title":"Special Topics in Advanced Machine Design Methods"
    },
    {
      "course_id":"001888",
      "subject":"ME",
      "catalog_number":"731",
      "title":"Corrosion and Oxidation"
    },
    {
      "course_id":"011465",
      "subject":"ME",
      "catalog_number":"732",
      "title":"Thermodynamics and Phase Transformations"
    },
    {
      "course_id":"001889",
      "subject":"ME",
      "catalog_number":"734",
      "title":"Composite Materials"
    },
    {
      "course_id":"001890",
      "subject":"ME",
      "catalog_number":"735",
      "title":"Special Topics - Welding and Joining"
    },
    {
      "course_id":"001891",
      "subject":"ME",
      "catalog_number":"736",
      "title":"Topics in Mechanical Metallurgy"
    },
    {
      "course_id":"001892",
      "subject":"ME",
      "catalog_number":"737",
      "title":"Microstructural Engineering Topics"
    },
    {
      "course_id":"001893",
      "subject":"ME",
      "catalog_number":"738",
      "title":"Special Topics in Materials"
    },
    {
      "course_id":"001894",
      "subject":"ME",
      "catalog_number":"739",
      "title":"Manufacturing Processes Topics"
    },
    {
      "course_id":"010458",
      "subject":"ME",
      "catalog_number":"741",
      "title":"Design of Intelligent Systems: Mechatronics"
    },
    {
      "course_id":"001895",
      "subject":"ME",
      "catalog_number":"742",
      "title":"Modelling and Control of Dynamic Systems"
    },
    {
      "course_id":"001896",
      "subject":"ME",
      "catalog_number":"743",
      "title":"Modal Analysis and Modelling"
    },
    {
      "course_id":"001898",
      "subject":"ME",
      "catalog_number":"745",
      "title":"Quality Assurance and Reliability in Manufacturing"
    },
    {
      "course_id":"001901",
      "subject":"ME",
      "catalog_number":"747",
      "title":"Topics in Manufacturing"
    },
    {
      "course_id":"001902",
      "subject":"ME",
      "catalog_number":"748",
      "title":"Topics in Surface Modelling"
    },
    {
      "course_id":"001903",
      "subject":"ME",
      "catalog_number":"749",
      "title":"Special Topics in Machining"
    },
    {
      "course_id":"010459",
      "subject":"ME",
      "catalog_number":"750",
      "title":"Advanced Engineering Thermodynamics"
    },
    {
      "course_id":"010460",
      "subject":"ME",
      "catalog_number":"751",
      "title":"Fuel Cell Technology"
    },
    {
      "course_id":"001904",
      "subject":"ME",
      "catalog_number":"753",
      "title":"Solar Energy"
    },
    {
      "course_id":"001906",
      "subject":"ME",
      "catalog_number":"755",
      "title":"Advanced Differential Equations and Special Functions"
    },
    {
      "course_id":"009374",
      "subject":"ME",
      "catalog_number":"756",
      "title":"Combustion 2"
    },
    {
      "course_id":"001907",
      "subject":"ME",
      "catalog_number":"758",
      "title":"Thermal Contact Resistance"
    },
    {
      "course_id":"001908",
      "subject":"ME",
      "catalog_number":"759",
      "title":"Advanced Experimental Methods in Thermal and Fluids Engineering"
    },
    {
      "course_id":"001909",
      "subject":"ME",
      "catalog_number":"760",
      "title":"Special Topics in Thermal Engineering: Air Pollution and Greenhouse Gases"
    },
    {
      "course_id":"001910",
      "subject":"ME",
      "catalog_number":"761",
      "title":"Fluid Dynamic Design of Turbomachines"
    },
    {
      "course_id":"001911",
      "subject":"ME",
      "catalog_number":"762",
      "title":"Turbulent Diffusion in the Natural Environment"
    },
    {
      "course_id":"012234",
      "subject":"ME",
      "catalog_number":"765",
      "title":"Special Topics in Fluid Mechanics"
    },
    {
      "course_id":"001912",
      "subject":"ME",
      "catalog_number":"770",
      "title":"Special Topics in Numerical Methods, Fluid Flow and Heat Transfer"
    },
    {
      "course_id":"001915",
      "subject":"ME",
      "catalog_number":"780",
      "title":"Special Topics in Mechatronics"
    },
    {
      "course_id":"011784",
      "subject":"MEDVL",
      "catalog_number":"105",
      "title":"Introduction to Medieval Studies"
    },
    {
      "course_id":"012629",
      "subject":"MEDVL",
      "catalog_number":"115",
      "title":"Crusading in the Middle Ages"
    },
    {
      "course_id":"004280",
      "subject":"MEDVL",
      "catalog_number":"205",
      "title":"Medieval Society"
    },
    {
      "course_id":"006314",
      "subject":"MEDVL",
      "catalog_number":"260",
      "title":"Europe: 410-1303"
    },
    {
      "course_id":"008378",
      "subject":"MEDVL",
      "catalog_number":"304",
      "title":"Heresy and Religious Crises in Late Medieval Europe"
    },
    {
      "course_id":"013979",
      "subject":"MNS",
      "catalog_number":"101",
      "title":"Materials and Nanosciences in the Modern World"
    },
    {
      "course_id":"013980",
      "subject":"MNS",
      "catalog_number":"102",
      "title":"Techniques for Materials and Nanosciences"
    },
    {
      "course_id":"014028",
      "subject":"MNS",
      "catalog_number":"201L",
      "title":"Materials and Nanosciences Laboratory"
    },
    {
      "course_id":"013981",
      "subject":"MNS",
      "catalog_number":"211",
      "title":"Chemistry and the Solid State"
    },
    {
      "course_id":"013984",
      "subject":"MNS",
      "catalog_number":"221",
      "title":"Physics and the Solid State"
    },
    {
      "course_id":"013988",
      "subject":"MNS",
      "catalog_number":"321",
      "title":"Electrical and Optical Properties of Materials"
    },
    {
      "course_id":"014029",
      "subject":"MNS",
      "catalog_number":"322",
      "title":"Polymer Materials"
    },
    {
      "course_id":"013987",
      "subject":"MNS",
      "catalog_number":"331",
      "title":"Biomaterials"
    },
    {
      "course_id":"012366",
      "subject":"MSCI",
      "catalog_number":"100",
      "title":"Management Engineering Concepts"
    },
    {
      "course_id":"013370",
      "subject":"MSCI",
      "catalog_number":"100B",
      "title":"Seminar"
    },
    {
      "course_id":"014426",
      "subject":"MSCI",
      "catalog_number":"121",
      "title":"Introduction to Computer Programming"
    },
    {
      "course_id":"013371",
      "subject":"MSCI",
      "catalog_number":"131",
      "title":"Work Design and Facilities Planning"
    },
    {
      "course_id":"012368",
      "subject":"MSCI",
      "catalog_number":"200A",
      "title":"Seminar"
    },
    {
      "course_id":"012369",
      "subject":"MSCI",
      "catalog_number":"200B",
      "title":"Seminar"
    },
    {
      "course_id":"006818",
      "subject":"MSCI",
      "catalog_number":"211",
      "title":"Organizational Behaviour"
    },
    {
      "course_id":"012370",
      "subject":"MSCI",
      "catalog_number":"240",
      "title":"Algorithms and Data Structures"
    },
    {
      "course_id":"012367",
      "subject":"MSCI",
      "catalog_number":"252",
      "title":"Probability and Statistics for Engineers"
    },
    {
      "course_id":"006820",
      "subject":"MSCI",
      "catalog_number":"261",
      "title":"Engineering Economics: Financial Management for Engineers"
    },
    {
      "course_id":"012371",
      "subject":"MSCI",
      "catalog_number":"262",
      "title":"Managerial and Cost Accounting"
    },
    {
      "course_id":"012372",
      "subject":"MSCI",
      "catalog_number":"263",
      "title":"Managerial Economics"
    },
    {
      "course_id":"012373",
      "subject":"MSCI",
      "catalog_number":"271",
      "title":"Advanced Calculus and Numerical Methods"
    },
    {
      "course_id":"012374",
      "subject":"MSCI",
      "catalog_number":"300A",
      "title":"Seminar"
    },
    {
      "course_id":"012375",
      "subject":"MSCI",
      "catalog_number":"300B",
      "title":"Seminar"
    },
    {
      "course_id":"006821",
      "subject":"MSCI",
      "catalog_number":"311",
      "title":"Organizational Design and Technology"
    },
    {
      "course_id":"006822",
      "subject":"MSCI",
      "catalog_number":"331",
      "title":"Introduction to Optimization"
    },
    {
      "course_id":"012376",
      "subject":"MSCI",
      "catalog_number":"332",
      "title":"Deterministic Optimization Models and Methods"
    },
    {
      "course_id":"012377",
      "subject":"MSCI",
      "catalog_number":"333",
      "title":"Simulation Analysis and Design"
    },
    {
      "course_id":"013762",
      "subject":"MSCI",
      "catalog_number":"334",
      "title":"Operations Planning and Inventory Control"
    },
    {
      "course_id":"012378",
      "subject":"MSCI",
      "catalog_number":"342",
      "title":"Principles of Software Engineering"
    },
    {
      "course_id":"012379",
      "subject":"MSCI",
      "catalog_number":"343",
      "title":"Human-Computer Interaction"
    },
    {
      "course_id":"012380",
      "subject":"MSCI",
      "catalog_number":"346",
      "title":"Database Systems"
    },
    {
      "course_id":"012381",
      "subject":"MSCI",
      "catalog_number":"400A",
      "title":"Seminar"
    },
    {
      "course_id":"012382",
      "subject":"MSCI",
      "catalog_number":"400B",
      "title":"Seminar"
    },
    {
      "course_id":"012383",
      "subject":"MSCI",
      "catalog_number":"401",
      "title":"Management Engineering Design Project 1"
    },
    {
      "course_id":"012384",
      "subject":"MSCI",
      "catalog_number":"402",
      "title":"Management Engineering Design Project 2"
    },
    {
      "course_id":"014556",
      "subject":"MSCI",
      "catalog_number":"411",
      "title":"Leadership and Influence"
    },
    {
      "course_id":"011498",
      "subject":"MSCI",
      "catalog_number":"421",
      "title":"Strategic Management of Technology"
    },
    {
      "course_id":"011499",
      "subject":"MSCI",
      "catalog_number":"422",
      "title":"Economic Impact of Technological Change and Entrepreneurship"
    },
    {
      "course_id":"012385",
      "subject":"MSCI",
      "catalog_number":"423",
      "title":"Managing New Product and Process Innovation"
    },
    {
      "course_id":"006823",
      "subject":"MSCI",
      "catalog_number":"431",
      "title":"Stochastic Models and Methods"
    },
    {
      "course_id":"006824",
      "subject":"MSCI",
      "catalog_number":"432",
      "title":"Production and Service Operations Management"
    },
    {
      "course_id":"012387",
      "subject":"MSCI",
      "catalog_number":"433",
      "title":"Applications of Management Engineering"
    },
    {
      "course_id":"012388",
      "subject":"MSCI",
      "catalog_number":"434",
      "title":"Supply Chain Management"
    },
    {
      "course_id":"012389",
      "subject":"MSCI",
      "catalog_number":"435",
      "title":"Advanced Optimization Techniques"
    },
    {
      "course_id":"012390",
      "subject":"MSCI",
      "catalog_number":"436",
      "title":"Decision Support Systems"
    },
    {
      "course_id":"006826",
      "subject":"MSCI",
      "catalog_number":"442",
      "title":"Impact of Information Systems on Organizations and Society"
    },
    {
      "course_id":"012042",
      "subject":"MSCI",
      "catalog_number":"444",
      "title":"Information Systems Analysis and Design"
    },
    {
      "course_id":"013763",
      "subject":"MSCI",
      "catalog_number":"445",
      "title":"Telecommunication Systems: from protocols to applications"
    },
    {
      "course_id":"012391",
      "subject":"MSCI",
      "catalog_number":"446",
      "title":"Data Warehousing and Mining"
    },
    {
      "course_id":"012392",
      "subject":"MSCI",
      "catalog_number":"453",
      "title":"Business Processes and Information Technology"
    },
    {
      "course_id":"006827",
      "subject":"MSCI",
      "catalog_number":"452",
      "title":"Decision Making Under Uncertainty"
    },
    {
      "course_id":"005813",
      "subject":"MSCI",
      "catalog_number":"454",
      "title":"Technical Entrepreneurship"
    },
    {
      "course_id":"013764",
      "subject":"MSCI",
      "catalog_number":"531",
      "title":"Stochastic Processes and Decision Making"
    },
    {
      "course_id":"013765",
      "subject":"MSCI",
      "catalog_number":"541",
      "title":"Information Retrieval Systems"
    },
    {
      "course_id":"013766",
      "subject":"MSCI",
      "catalog_number":"551",
      "title":"Quality Management and Control"
    },
    {
      "course_id":"013767",
      "subject":"MSCI",
      "catalog_number":"555",
      "title":"Scheduling: Theory and Practice"
    },
    {
      "course_id":"013768",
      "subject":"MSCI",
      "catalog_number":"597",
      "title":"Complementary Studies Topics in Management Sciences"
    },
    {
      "course_id":"013769",
      "subject":"MSCI",
      "catalog_number":"598",
      "title":"Special Topics in Management Engineering"
    },
    {
      "course_id":"013770",
      "subject":"MSCI",
      "catalog_number":"599",
      "title":"Special Topics in Management Engineering Design"
    },
    {
      "course_id":"001925",
      "subject":"MSCI",
      "catalog_number":"601",
      "title":"Research Methods in the Management Sciences"
    },
    {
      "course_id":"001926",
      "subject":"MSCI",
      "catalog_number":"602",
      "title":"Strategic Management of Technological Innovation"
    },
    {
      "course_id":"001927",
      "subject":"MSCI",
      "catalog_number":"603",
      "title":"Principles of Operations Research"
    },
    {
      "course_id":"001929",
      "subject":"MSCI",
      "catalog_number":"605",
      "title":"Organizational Theory & Behaviour"
    },
    {
      "course_id":"011267",
      "subject":"MSCI",
      "catalog_number":"606",
      "title":"Foundations of Senior Management"
    },
    {
      "course_id":"011080",
      "subject":"MSCI",
      "catalog_number":"607",
      "title":"Applied Economics for Management"
    },
    {
      "course_id":"013147",
      "subject":"MSCI",
      "catalog_number":"609",
      "title":"Quantitative Data Analysis for Management Sciences"
    },
    {
      "course_id":"001934",
      "subject":"MSCI",
      "catalog_number":"620",
      "title":"Organizations & Technical Systems"
    },
    {
      "course_id":"001937",
      "subject":"MSCI",
      "catalog_number":"631",
      "title":"Probabilistic  Models in Operations Research"
    },
    {
      "course_id":"001938",
      "subject":"MSCI",
      "catalog_number":"632",
      "title":"Discrete Event Simulation"
    },
    {
      "course_id":"001939",
      "subject":"MSCI",
      "catalog_number":"633",
      "title":"Production and Inventory Management"
    },
    {
      "course_id":"012974",
      "subject":"MSCI",
      "catalog_number":"638",
      "title":"Information Systems Analysis and Design"
    },
    {
      "course_id":"001950",
      "subject":"MSCI",
      "catalog_number":"646",
      "title":"Database Management Systems"
    },
    {
      "course_id":"014234",
      "subject":"MSCI",
      "catalog_number":"651",
      "title":"International Project Management"
    },
    {
      "course_id":"014235",
      "subject":"MSCI",
      "catalog_number":"652",
      "title":"International Business Management"
    },
    {
      "course_id":"010503",
      "subject":"MSCI",
      "catalog_number":"700",
      "title":"Topics in Operations Research and Management"
    },
    {
      "course_id":"001957",
      "subject":"MSCI",
      "catalog_number":"702",
      "title":"Linear Programming and Extensions"
    },
    {
      "course_id":"001958",
      "subject":"MSCI",
      "catalog_number":"703",
      "title":"Applied Optimization"
    },
    {
      "course_id":"001960",
      "subject":"MSCI",
      "catalog_number":"709",
      "title":"Logistics and Supply Chain Management"
    },
    {
      "course_id":"001963",
      "subject":"MSCI",
      "catalog_number":"712",
      "title":"Decision Analysis Under Uncertainty"
    },
    {
      "course_id":"009482",
      "subject":"MSCI",
      "catalog_number":"720",
      "title":"Topics in Information and Information Systems"
    },
    {
      "course_id":"001971",
      "subject":"MSCI",
      "catalog_number":"721",
      "title":"Knowledge Engineering for Management"
    },
    {
      "course_id":"001978",
      "subject":"MSCI",
      "catalog_number":"730",
      "title":"Human Computer Interaction"
    },
    {
      "course_id":"009483",
      "subject":"MSCI",
      "catalog_number":"740",
      "title":"Topics in Management of Technology"
    },
    {
      "course_id":"010308",
      "subject":"MSCI",
      "catalog_number":"765",
      "title":"Statistical Quality Control"
    },
    {
      "course_id":"010512",
      "subject":"MSCI",
      "catalog_number":"767",
      "title":"Management of Quality"
    },
    {
      "course_id":"001986",
      "subject":"MSCI",
      "catalog_number":"741",
      "title":"Economics of Technological Change"
    },
    {
      "course_id":"001991",
      "subject":"MSCI",
      "catalog_number":"750",
      "title":"Topics in Organizational Analysis and Behaviour"
    },
    {
      "course_id":"012975",
      "subject":"MSCI",
      "catalog_number":"751",
      "title":"Knowledge Management"
    },
    {
      "course_id":"001995",
      "subject":"MSCI",
      "catalog_number":"753",
      "title":"Entrepreneurship and Intrapreneurship: Managing New Technology-based Firms"
    },
    {
      "course_id":"001999",
      "subject":"MSCI",
      "catalog_number":"760",
      "title":"Topics in Other Areas of Management Sciences"
    },
    {
      "course_id":"002006",
      "subject":"MSCI",
      "catalog_number":"770",
      "title":"Special Directed Readings"
    },
    {
      "course_id":"011424",
      "subject":"MTE",
      "catalog_number":"100",
      "title":"Mechatronics Engineering"
    },
    {
      "course_id":"011455",
      "subject":"MTE",
      "catalog_number":"100B",
      "title":"Seminar"
    },
    {
      "course_id":"011425",
      "subject":"MTE",
      "catalog_number":"111",
      "title":"Structure and Properties of Materials"
    },
    {
      "course_id":"011426",
      "subject":"MTE",
      "catalog_number":"119",
      "title":"Statics"
    },
    {
      "course_id":"011452",
      "subject":"MTE",
      "catalog_number":"120",
      "title":"Circuits"
    },
    {
      "course_id":"010083",
      "subject":"MTE",
      "catalog_number":"140",
      "title":"Algorithms and Data Structures"
    },
    {
      "course_id":"011456",
      "subject":"MTE",
      "catalog_number":"200A",
      "title":"Seminar"
    },
    {
      "course_id":"011457",
      "subject":"MTE",
      "catalog_number":"200B",
      "title":"Seminar"
    },
    {
      "course_id":"011427",
      "subject":"MTE",
      "catalog_number":"201",
      "title":"Experimental Measurement & Statistical Analysis"
    },
    {
      "course_id":"011421",
      "subject":"MTE",
      "catalog_number":"202",
      "title":"Ordinary Differential Equations"
    },
    {
      "course_id":"011422",
      "subject":"MTE",
      "catalog_number":"203",
      "title":"Advanced Calculus"
    },
    {
      "course_id":"011423",
      "subject":"MTE",
      "catalog_number":"204",
      "title":"Numerical Methods"
    },
    {
      "course_id":"011428",
      "subject":"MTE",
      "catalog_number":"219",
      "title":"Mechanics of Deformable Solids"
    },
    {
      "course_id":"011453",
      "subject":"MTE",
      "catalog_number":"220",
      "title":"Sensors and Instrumentation"
    },
    {
      "course_id":"010084",
      "subject":"MTE",
      "catalog_number":"241",
      "title":"Introduction to Computer Structures & Real-Time Systems"
    },
    {
      "course_id":"013777",
      "subject":"MTE",
      "catalog_number":"262",
      "title":"Introduction to Microprocessors and Digital Logic"
    },
    {
      "course_id":"011458",
      "subject":"MTE",
      "catalog_number":"300A",
      "title":"Seminar"
    },
    {
      "course_id":"011459",
      "subject":"MTE",
      "catalog_number":"300B",
      "title":"Seminar"
    },
    {
      "course_id":"011454",
      "subject":"MTE",
      "catalog_number":"320",
      "title":"Actuators & Power Electronics"
    },
    {
      "course_id":"011429",
      "subject":"MTE",
      "catalog_number":"322",
      "title":"Electromechanical Machine Design"
    },
    {
      "course_id":"011044",
      "subject":"MTE",
      "catalog_number":"325",
      "title":"Microprocessor Systems and Interfacing for Mechatronics Engineering"
    },
    {
      "course_id":"011430",
      "subject":"MTE",
      "catalog_number":"360",
      "title":"Automatic Control Systems"
    },
    {
      "course_id":"013778",
      "subject":"MTE",
      "catalog_number":"380",
      "title":"Mechatronics Engineering Design Workshop"
    },
    {
      "course_id":"011460",
      "subject":"MTE",
      "catalog_number":"400A",
      "title":"Seminar"
    },
    {
      "course_id":"011461",
      "subject":"MTE",
      "catalog_number":"400B",
      "title":"Seminar"
    },
    {
      "course_id":"014026",
      "subject":"MTE",
      "catalog_number":"420",
      "title":"Power Electronics and Motor Drives"
    },
    {
      "course_id":"013905",
      "subject":"MTE",
      "catalog_number":"460",
      "title":"Mechatronic System Integration"
    },
    {
      "course_id":"013779",
      "subject":"MTE",
      "catalog_number":"481",
      "title":"Mechatronics Engineering Design Project"
    },
    {
      "course_id":"013780",
      "subject":"MTE",
      "catalog_number":"482",
      "title":"Mechatronics Engineering Project"
    },
    {
      "course_id":"013776",
      "subject":"MTE",
      "catalog_number":"545",
      "title":"Introduction to MEMS Fabrication"
    },
    {
      "course_id":"012764",
      "subject":"MTHEL",
      "catalog_number":"131",
      "title":"Introduction to Actuarial Practice"
    },
    {
      "course_id":"010168",
      "subject":"MTHEL",
      "catalog_number":"198",
      "title":"Mathematics Elective Topics 1"
    },
    {
      "course_id":"006940",
      "subject":"MTHEL",
      "catalog_number":"206A",
      "title":"Introduction to Mathematics Education"
    },
    {
      "course_id":"010169",
      "subject":"MTHEL",
      "catalog_number":"298",
      "title":"Mathematics Elective Topics 2"
    },
    {
      "course_id":"010170",
      "subject":"MTHEL",
      "catalog_number":"398",
      "title":"Mathematics Elective Topics 3"
    },
    {
      "course_id":"010171",
      "subject":"MTHEL",
      "catalog_number":"498",
      "title":"Mathematics Elective Topics 4"
    },
    {
      "course_id":"006944",
      "subject":"MUSIC",
      "catalog_number":"100",
      "title":"Understanding Music"
    },
    {
      "course_id":"006948",
      "subject":"MUSIC",
      "catalog_number":"111",
      "title":"Fundamentals of Music Theory"
    },
    {
      "course_id":"006951",
      "subject":"MUSIC",
      "catalog_number":"116",
      "title":"Music Ensemble"
    },
    {
      "course_id":"006952",
      "subject":"MUSIC",
      "catalog_number":"117",
      "title":"Music Ensemble"
    },
    {
      "course_id":"006959",
      "subject":"MUSIC",
      "catalog_number":"140",
      "title":"Popular Music and Culture"
    },
    {
      "course_id":"006981",
      "subject":"MUSIC",
      "catalog_number":"216",
      "title":"Music Ensemble"
    },
    {
      "course_id":"006982",
      "subject":"MUSIC",
      "catalog_number":"217",
      "title":"Music Ensemble"
    },
    {
      "course_id":"006986",
      "subject":"MUSIC",
      "catalog_number":"222",
      "title":"Conducting 1"
    },
    {
      "course_id":"006988",
      "subject":"MUSIC",
      "catalog_number":"226",
      "title":"Music Studio"
    },
    {
      "course_id":"006989",
      "subject":"MUSIC",
      "catalog_number":"227",
      "title":"Music Studio"
    },
    {
      "course_id":"006990",
      "subject":"MUSIC",
      "catalog_number":"231",
      "title":"Psychology of Music"
    },
    {
      "course_id":"006991",
      "subject":"MUSIC",
      "catalog_number":"240",
      "title":"Introduction to Jazz"
    },
    {
      "course_id":"006993",
      "subject":"MUSIC",
      "catalog_number":"245",
      "title":"World Music"
    },
    {
      "course_id":"011587",
      "subject":"MUSIC",
      "catalog_number":"246",
      "title":"Soundtracks: Music in Film"
    },
    {
      "course_id":"007001",
      "subject":"MUSIC",
      "catalog_number":"253",
      "title":"Cathedral and Court: Music to 1600"
    },
    {
      "course_id":"007002",
      "subject":"MUSIC",
      "catalog_number":"254",
      "title":"Monteverdi to Mozart: Music from 1600-1800"
    },
    {
      "course_id":"007003",
      "subject":"MUSIC",
      "catalog_number":"255",
      "title":"The Romantic Century: Beethoven and Beyond"
    },
    {
      "course_id":"007004",
      "subject":"MUSIC",
      "catalog_number":"256",
      "title":"Music Since 1900"
    },
    {
      "course_id":"007009",
      "subject":"MUSIC",
      "catalog_number":"260",
      "title":"The Symphony"
    },
    {
      "course_id":"010205",
      "subject":"MUSIC",
      "catalog_number":"261",
      "title":"Opera"
    },
    {
      "course_id":"007018",
      "subject":"MUSIC",
      "catalog_number":"270",
      "title":"Music Theory 1"
    },
    {
      "course_id":"007020",
      "subject":"MUSIC",
      "catalog_number":"271",
      "title":"Music Theory 2"
    },
    {
      "course_id":"007025",
      "subject":"MUSIC",
      "catalog_number":"275",
      "title":"Music and Technology"
    },
    {
      "course_id":"010206",
      "subject":"MUSIC",
      "catalog_number":"290",
      "title":"Special Topics"
    },
    {
      "course_id":"007036",
      "subject":"MUSIC",
      "catalog_number":"316",
      "title":"Music Ensemble"
    },
    {
      "course_id":"007037",
      "subject":"MUSIC",
      "catalog_number":"317",
      "title":"Music Ensemble"
    },
    {
      "course_id":"007038",
      "subject":"MUSIC",
      "catalog_number":"322",
      "title":"Conducting 2"
    },
    {
      "course_id":"007039",
      "subject":"MUSIC",
      "catalog_number":"326",
      "title":"Music Studio"
    },
    {
      "course_id":"007040",
      "subject":"MUSIC",
      "catalog_number":"327",
      "title":"Music Studio"
    },
    {
      "course_id":"007041",
      "subject":"MUSIC",
      "catalog_number":"332",
      "title":"Aesthetics of Music"
    },
    {
      "course_id":"007042",
      "subject":"MUSIC",
      "catalog_number":"334",
      "title":"Women, Music and Gender"
    },
    {
      "course_id":"007045",
      "subject":"MUSIC",
      "catalog_number":"355",
      "title":"Music and Culture Travel Course"
    },
    {
      "course_id":"007049",
      "subject":"MUSIC",
      "catalog_number":"361",
      "title":"Art Song"
    },
    {
      "course_id":"007050",
      "subject":"MUSIC",
      "catalog_number":"362",
      "title":"Piano Literature"
    },
    {
      "course_id":"007051",
      "subject":"MUSIC",
      "catalog_number":"363",
      "title":"Christian Hymnody"
    },
    {
      "course_id":"007052",
      "subject":"MUSIC",
      "catalog_number":"364",
      "title":"Worship and Music"
    },
    {
      "course_id":"007058",
      "subject":"MUSIC",
      "catalog_number":"370",
      "title":"Music Theory 3 (19th-Century)"
    },
    {
      "course_id":"007059",
      "subject":"MUSIC",
      "catalog_number":"371",
      "title":"Theory 4 (20th-Century)"
    },
    {
      "course_id":"007064",
      "subject":"MUSIC",
      "catalog_number":"376",
      "title":"Composition Seminar"
    },
    {
      "course_id":"007066",
      "subject":"MUSIC",
      "catalog_number":"380",
      "title":"Directed Study in Music"
    },
    {
      "course_id":"007069",
      "subject":"MUSIC",
      "catalog_number":"381",
      "title":"Directed Study in Music"
    },
    {
      "course_id":"007072",
      "subject":"MUSIC",
      "catalog_number":"390",
      "title":"Special Topics in Music 1"
    },
    {
      "course_id":"007073",
      "subject":"MUSIC",
      "catalog_number":"391",
      "title":"Special Topics in Music 2"
    },
    {
      "course_id":"007076",
      "subject":"MUSIC",
      "catalog_number":"426",
      "title":"Music Studio"
    },
    {
      "course_id":"007077",
      "subject":"MUSIC",
      "catalog_number":"427",
      "title":"Music Studio"
    },
    {
      "course_id":"013997",
      "subject":"MUSIC",
      "catalog_number":"428",
      "title":"Music Studio"
    },
    {
      "course_id":"012958",
      "subject":"MUSIC",
      "catalog_number":"491",
      "title":"Honours Research Seminar"
    },
    {
      "course_id":"007083",
      "subject":"MUSIC",
      "catalog_number":"492",
      "title":"Senior Honours Thesis"
    },
    {
      "course_id":"013600",
      "subject":"NANO",
      "catalog_number":"701",
      "title":"Fundamentals of Nanotechnology"
    },
    {
      "course_id":"013601",
      "subject":"NANO",
      "catalog_number":"702",
      "title":"Nanotechnology Tools"
    },
    {
      "course_id":"013057",
      "subject":"NES",
      "catalog_number":"611",
      "title":"Ancient Near Eastern Societies"
    },
    {
      "course_id":"003945",
      "subject":"NATST",
      "catalog_number":"370",
      "title":"Issues in Contemporary Native Communities in Canada"
    },
    {
      "course_id":"011923",
      "subject":"NE",
      "catalog_number":"100",
      "title":"Introduction to Nanotechnology Engineering"
    },
    {
      "course_id":"011915",
      "subject":"NE",
      "catalog_number":"101",
      "title":"Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011916",
      "subject":"NE",
      "catalog_number":"102",
      "title":"Introduction to Nanomaterials Health Risk; Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011924",
      "subject":"NE",
      "catalog_number":"112",
      "title":"Linear Algebra for Nanotechnology Engineers"
    },
    {
      "course_id":"011925",
      "subject":"NE",
      "catalog_number":"113",
      "title":"Introduction to Computational Methods"
    },
    {
      "course_id":"011926",
      "subject":"NE",
      "catalog_number":"115",
      "title":"Probability and Statistics"
    },
    {
      "course_id":"011928",
      "subject":"NE",
      "catalog_number":"121",
      "title":"Chemical Principles"
    },
    {
      "course_id":"012237",
      "subject":"NE",
      "catalog_number":"122",
      "title":"Organic Chemistry for Nanotechnology Engineers"
    },
    {
      "course_id":"012238",
      "subject":"NE",
      "catalog_number":"125",
      "title":"Introduction to Materials Science and Engineering"
    },
    {
      "course_id":"011930",
      "subject":"NE",
      "catalog_number":"131",
      "title":"Physics for Nanotechnology Engineering"
    },
    {
      "course_id":"011917",
      "subject":"NE",
      "catalog_number":"201",
      "title":"Nanotoxicology; Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011918",
      "subject":"NE",
      "catalog_number":"202",
      "title":"Nanotechnology Environmental and Occupational Health; Nanotechnology Engineering Practice"
    },
    {
      "course_id":"013158",
      "subject":"NE",
      "catalog_number":"216",
      "title":"Advanced Calculus 1 for Nanotechnology Engineering"
    },
    {
      "course_id":"013160",
      "subject":"NE",
      "catalog_number":"217",
      "title":"Advanced Calculus 2 for Nanotechnology Engineering"
    },
    {
      "course_id":"012582",
      "subject":"NE",
      "catalog_number":"220L",
      "title":"Materials Science and Engineering Laboratory"
    },
    {
      "course_id":"011933",
      "subject":"NE",
      "catalog_number":"224",
      "title":"Biochemistry for Nanotechnology Engineers"
    },
    {
      "course_id":"012239",
      "subject":"NE",
      "catalog_number":"225",
      "title":"Structure and Properties of Nanomaterials"
    },
    {
      "course_id":"011934",
      "subject":"NE",
      "catalog_number":"226",
      "title":"Characterization of Materials"
    },
    {
      "course_id":"014070",
      "subject":"NE",
      "catalog_number":"226L",
      "title":"Laboratory Characterization Methods"
    },
    {
      "course_id":"011935",
      "subject":"NE",
      "catalog_number":"232",
      "title":"Quantum Mechanics"
    },
    {
      "course_id":"011931",
      "subject":"NE",
      "catalog_number":"241",
      "title":"Electromagnetism"
    },
    {
      "course_id":"011937",
      "subject":"NE",
      "catalog_number":"242",
      "title":"Semiconductor Physics and Devices"
    },
    {
      "course_id":"011919",
      "subject":"NE",
      "catalog_number":"301",
      "title":"Environmental Impact, Ecotoxicology, and Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011920",
      "subject":"NE",
      "catalog_number":"302",
      "title":"Nanomaterials Risks\/Benefits and Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011963",
      "subject":"NE",
      "catalog_number":"307",
      "title":"Introduction to Nanosystems Design"
    },
    {
      "course_id":"011938",
      "subject":"NE",
      "catalog_number":"318",
      "title":"Continuum Mechanics for Nanotechnology Engineering"
    },
    {
      "course_id":"012874",
      "subject":"NE",
      "catalog_number":"320L",
      "title":"Characterization of Materials Laboratory"
    },
    {
      "course_id":"013323",
      "subject":"NE",
      "catalog_number":"330L",
      "title":"Macromolecular Science Laboratory"
    },
    {
      "course_id":"011936",
      "subject":"NE",
      "catalog_number":"333",
      "title":"Macromolecular Science 1"
    },
    {
      "course_id":"011939",
      "subject":"NE",
      "catalog_number":"334",
      "title":"Statistical Thermodynamics"
    },
    {
      "course_id":"011940",
      "subject":"NE",
      "catalog_number":"335",
      "title":"Macromolecular Science 2"
    },
    {
      "course_id":"011941",
      "subject":"NE",
      "catalog_number":"336",
      "title":"Micro and Nanosystem Computer-aided Design"
    },
    {
      "course_id":"012875",
      "subject":"NE",
      "catalog_number":"340L",
      "title":"Microfabrication and Thin-film Technology Laboratory"
    },
    {
      "course_id":"011942",
      "subject":"NE",
      "catalog_number":"343",
      "title":"Microfabrication and Thin-film Technology"
    },
    {
      "course_id":"011943",
      "subject":"NE",
      "catalog_number":"344",
      "title":"Electronic Circuits and Integration"
    },
    {
      "course_id":"011945",
      "subject":"NE",
      "catalog_number":"352",
      "title":"Surfaces and Interfaces"
    },
    {
      "course_id":"011946",
      "subject":"NE",
      "catalog_number":"353",
      "title":"Nanoprobing and Lithography"
    },
    {
      "course_id":"011921",
      "subject":"NE",
      "catalog_number":"401",
      "title":"Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011922",
      "subject":"NE",
      "catalog_number":"402",
      "title":"Nanotechnology Engineering Practice"
    },
    {
      "course_id":"011964",
      "subject":"NE",
      "catalog_number":"408",
      "title":"Nanosystems Design Project"
    },
    {
      "course_id":"011965",
      "subject":"NE",
      "catalog_number":"409",
      "title":"Nanosystems Design Project and Symposium"
    },
    {
      "course_id":"011944",
      "subject":"NE",
      "catalog_number":"445",
      "title":"Photonic Materials and Devices"
    },
    {
      "course_id":"012876",
      "subject":"NE",
      "catalog_number":"450L",
      "title":"Nanoprobing and Lithography Laboratory"
    },
    {
      "course_id":"014071",
      "subject":"NE",
      "catalog_number":"451",
      "title":"Simulation Methods in Nanotechnology Engineering"
    },
    {
      "course_id":"014072",
      "subject":"NE",
      "catalog_number":"452",
      "title":"Special Topics in Nanoscale Simulations"
    },
    {
      "course_id":"012877",
      "subject":"NE",
      "catalog_number":"454L",
      "title":"Nanotechnology Engineering Advanced Laboratory 1"
    },
    {
      "course_id":"012878",
      "subject":"NE",
      "catalog_number":"455L",
      "title":"Nanotechnology Engineering Advanced Laboratory 2"
    },
    {
      "course_id":"014947",
      "subject":"OPTOM",
      "catalog_number":"650",
      "title":"Research Methodology for Vision Science"
    },
    {
      "course_id":"014721",
      "subject":"PD",
      "catalog_number":"10",
      "title":"Professional Responsibility in Computing"
    },
    {
      "course_id":"012240",
      "subject":"NE",
      "catalog_number":"459",
      "title":"Nanotechnology Engineering Research Project"
    },
    {
      "course_id":"011947",
      "subject":"NE",
      "catalog_number":"461",
      "title":"Micro and Nanoinstruments"
    },
    {
      "course_id":"012241",
      "subject":"NE",
      "catalog_number":"469",
      "title":"Special Topics in Micro and Nanoinstruments"
    },
    {
      "course_id":"011951",
      "subject":"NE",
      "catalog_number":"471",
      "title":"Physics, Technology, and Applications of Nanoelectronics"
    },
    {
      "course_id":"012242",
      "subject":"NE",
      "catalog_number":"479",
      "title":"Special Topics in Nanoelectronics"
    },
    {
      "course_id":"011955",
      "subject":"NE",
      "catalog_number":"481",
      "title":"Introduction to Nanomedicine and Nanobiotechnology"
    },
    {
      "course_id":"013087",
      "subject":"NES",
      "catalog_number":"625W",
      "title":"Myth and Burial Customs in the Ancient Near East"
    },
    {
      "course_id":"012243",
      "subject":"NE",
      "catalog_number":"489",
      "title":"Special Topics in Nanoscale Biosystems"
    },
    {
      "course_id":"011959",
      "subject":"NE",
      "catalog_number":"491",
      "title":"Nanostructured Materials"
    },
    {
      "course_id":"012244",
      "subject":"NE",
      "catalog_number":"499",
      "title":"Special Topics in Nanostructured Materials"
    },
    {
      "course_id":"007086",
      "subject":"OPTOM",
      "catalog_number":"103",
      "title":"Pathophysiology"
    },
    {
      "course_id":"007087",
      "subject":"OPTOM",
      "catalog_number":"104",
      "title":"Anatomy of the Eye 1"
    },
    {
      "course_id":"007088",
      "subject":"OPTOM",
      "catalog_number":"105",
      "title":"Medical Microbiology"
    },
    {
      "course_id":"007089",
      "subject":"OPTOM",
      "catalog_number":"106",
      "title":"Geometrical, Physical and Visual Optics"
    },
    {
      "course_id":"012881",
      "subject":"OPTOM",
      "catalog_number":"108",
      "title":"Histology of Tissues and Organs"
    },
    {
      "course_id":"007090",
      "subject":"OPTOM",
      "catalog_number":"109",
      "title":"Visual Perception 1: Perception of Light"
    },
    {
      "course_id":"007092",
      "subject":"OPTOM",
      "catalog_number":"114",
      "title":"Anatomy of the Eye 2"
    },
    {
      "course_id":"012882",
      "subject":"OPTOM",
      "catalog_number":"124",
      "title":"Human Gross Anatomy"
    },
    {
      "course_id":"009975",
      "subject":"OPTOM",
      "catalog_number":"126",
      "title":"Fundamentals of Visual Optics"
    },
    {
      "course_id":"012883",
      "subject":"OPTOM",
      "catalog_number":"134",
      "title":"Immunology"
    },
    {
      "course_id":"009988",
      "subject":"OPTOM",
      "catalog_number":"143",
      "title":"Physiology of the Eye"
    },
    {
      "course_id":"009955",
      "subject":"OPTOM",
      "catalog_number":"152",
      "title":"Clinical Techniques 1"
    },
    {
      "course_id":"012247",
      "subject":"OPTOM",
      "catalog_number":"152L",
      "title":"Clinical Techniques 1 Laboratory"
    },
    {
      "course_id":"007093",
      "subject":"OPTOM",
      "catalog_number":"215",
      "title":"Systemic Disease"
    },
    {
      "course_id":"007097",
      "subject":"OPTOM",
      "catalog_number":"216",
      "title":"Ophthalmic Optics 1"
    },
    {
      "course_id":"009957",
      "subject":"OPTOM",
      "catalog_number":"219",
      "title":"Visual Perception 2: Monocular and Binocular Visual Processes"
    },
    {
      "course_id":"009958",
      "subject":"OPTOM",
      "catalog_number":"231",
      "title":"Introductory Clinical Pharmacology"
    },
    {
      "course_id":"009990",
      "subject":"OPTOM",
      "catalog_number":"243",
      "title":"Neurophysiology of Vision"
    },
    {
      "course_id":"009956",
      "subject":"OPTOM",
      "catalog_number":"245",
      "title":"Diseases of the Eye 1"
    },
    {
      "course_id":"012248",
      "subject":"OPTOM",
      "catalog_number":"245L",
      "title":"Diseases of the Eye 1 Laboratory"
    },
    {
      "course_id":"007102",
      "subject":"OPTOM",
      "catalog_number":"246",
      "title":"Ophthalmic Optics 2"
    },
    {
      "course_id":"009991",
      "subject":"OPTOM",
      "catalog_number":"250",
      "title":"Optometric Jurisprudence"
    },
    {
      "course_id":"007104",
      "subject":"OPTOM",
      "catalog_number":"252",
      "title":"Clinical Techniques 2"
    },
    {
      "course_id":"012249",
      "subject":"OPTOM",
      "catalog_number":"252L",
      "title":"Clinical Techniques 2 Laboratory"
    },
    {
      "course_id":"007106",
      "subject":"OPTOM",
      "catalog_number":"255",
      "title":"Diseases of the Eye 2"
    },
    {
      "course_id":"012250",
      "subject":"OPTOM",
      "catalog_number":"255L",
      "title":"Diseases of the Eye 2 Laboratory"
    },
    {
      "course_id":"007107",
      "subject":"OPTOM",
      "catalog_number":"261",
      "title":"Clinical Ocular Pharmacology"
    },
    {
      "course_id":"009993",
      "subject":"OPTOM",
      "catalog_number":"262",
      "title":"Clinical Techniques 3"
    },
    {
      "course_id":"009995",
      "subject":"OPTOM",
      "catalog_number":"270",
      "title":"Public Health Optometry"
    },
    {
      "course_id":"009996",
      "subject":"OPTOM",
      "catalog_number":"272",
      "title":"Strabismus and Aniseikonia"
    },
    {
      "course_id":"009989",
      "subject":"OPTOM",
      "catalog_number":"339",
      "title":"Visual Perception 3:Colour Vision"
    },
    {
      "course_id":"010388",
      "subject":"OPTOM",
      "catalog_number":"342A",
      "title":"Case Analysis and Optometric Therapies 1"
    },
    {
      "course_id":"010389",
      "subject":"OPTOM",
      "catalog_number":"342B",
      "title":"Case Analysis and Optometric Therapies 2"
    },
    {
      "course_id":"007113",
      "subject":"OPTOM",
      "catalog_number":"346",
      "title":"Ophthalmic Optics 3"
    },
    {
      "course_id":"007115",
      "subject":"OPTOM",
      "catalog_number":"347",
      "title":"Contact Lenses 1"
    },
    {
      "course_id":"012251",
      "subject":"OPTOM",
      "catalog_number":"347L",
      "title":"Contact Lenses 1 Laboratory"
    },
    {
      "course_id":"007118",
      "subject":"OPTOM",
      "catalog_number":"348A",
      "title":"Optometry Clinics"
    },
    {
      "course_id":"007119",
      "subject":"OPTOM",
      "catalog_number":"348B",
      "title":"Optometry Clinics"
    },
    {
      "course_id":"009992",
      "subject":"OPTOM",
      "catalog_number":"360",
      "title":"Professional Ethics and Optometric Communication"
    },
    {
      "course_id":"009994",
      "subject":"OPTOM",
      "catalog_number":"365",
      "title":"Ophthalmic Lasers and Refractive Surgery"
    },
    {
      "course_id":"007128",
      "subject":"OPTOM",
      "catalog_number":"367",
      "title":"Contact Lenses 2"
    },
    {
      "course_id":"010390",
      "subject":"OPTOM",
      "catalog_number":"375",
      "title":"Diseases of the Eye 3"
    },
    {
      "course_id":"012252",
      "subject":"OPTOM",
      "catalog_number":"375L",
      "title":"Diseases of the Eye 3 Laboratory"
    },
    {
      "course_id":"010391",
      "subject":"OPTOM",
      "catalog_number":"377",
      "title":"Pediatric Optometry and Learning Disabilities"
    },
    {
      "course_id":"010392",
      "subject":"OPTOM",
      "catalog_number":"380",
      "title":"Practice Management"
    },
    {
      "course_id":"010393",
      "subject":"OPTOM",
      "catalog_number":"385",
      "title":"Clinical Medicine for Optometric Practice"
    },
    {
      "course_id":"010394",
      "subject":"OPTOM",
      "catalog_number":"387",
      "title":"Gerontology and Low Vision"
    },
    {
      "course_id":"007132",
      "subject":"OPTOM",
      "catalog_number":"412",
      "title":"Case Analysis 3"
    },
    {
      "course_id":"007134",
      "subject":"OPTOM",
      "catalog_number":"441",
      "title":"Optometry Research Proposal"
    },
    {
      "course_id":"007140",
      "subject":"OPTOM",
      "catalog_number":"451",
      "title":"Optometry Research Project"
    },
    {
      "course_id":"007137",
      "subject":"OPTOM",
      "catalog_number":"458",
      "title":"Primary Care Externship"
    },
    {
      "course_id":"010025",
      "subject":"OPTOM",
      "catalog_number":"460",
      "title":"Advanced Study Topics"
    },
    {
      "course_id":"007150",
      "subject":"OPTOM",
      "catalog_number":"461S",
      "title":"Optometry Seminar"
    },
    {
      "course_id":"007138",
      "subject":"OPTOM",
      "catalog_number":"468",
      "title":"Ocular Disease and Therapeutics Externship"
    },
    {
      "course_id":"007152",
      "subject":"OPTOM",
      "catalog_number":"477",
      "title":"Clinical Techniques 4"
    },
    {
      "course_id":"007136",
      "subject":"OPTOM",
      "catalog_number":"478",
      "title":"Optometry Clinics"
    },
    {
      "course_id":"011554",
      "subject":"OPTOM",
      "catalog_number":"488",
      "title":"Exit Exam Remediation"
    },
    {
      "course_id":"002032",
      "subject":"OPTOM",
      "catalog_number":"600",
      "title":"Physiology of the Eye"
    },
    {
      "course_id":"002033",
      "subject":"OPTOM",
      "catalog_number":"601",
      "title":"Optical Characteristics of the Eye"
    },
    {
      "course_id":"010513",
      "subject":"OPTOM",
      "catalog_number":"602",
      "title":"Ocular Motility"
    },
    {
      "course_id":"002034",
      "subject":"OPTOM",
      "catalog_number":"603",
      "title":"Accommodation and Convergence"
    },
    {
      "course_id":"002035",
      "subject":"OPTOM",
      "catalog_number":"604",
      "title":"Visual Perception of Space"
    },
    {
      "course_id":"009471",
      "subject":"OPTOM",
      "catalog_number":"605",
      "title":"Psychophysics of Colour Vision"
    },
    {
      "course_id":"002036",
      "subject":"OPTOM",
      "catalog_number":"606",
      "title":"Radiation and the Visual Stimulus"
    },
    {
      "course_id":"002037",
      "subject":"OPTOM",
      "catalog_number":"607",
      "title":"Neurophysiology of Vision"
    },
    {
      "course_id":"002038",
      "subject":"OPTOM",
      "catalog_number":"608",
      "title":"Special Topics in Vision Science"
    },
    {
      "course_id":"014994",
      "subject":"OPTOM",
      "catalog_number":"661",
      "title":"Practical Advancement Data Analysis"
    },
    {
      "course_id":"014989",
      "subject":"OPTOM",
      "catalog_number":"670",
      "title":"Vision Science Part 1"
    },
    {
      "course_id":"014990",
      "subject":"OPTOM",
      "catalog_number":"671",
      "title":"Vision Science Part"
    },
    {
      "course_id":"014991",
      "subject":"OPTOM",
      "catalog_number":"672",
      "title":"Comparative Anatomy & Physiology of the Vertebrate Eye"
    },
    {
      "course_id":"014992",
      "subject":"OPTOM",
      "catalog_number":"680",
      "title":"Visual Development"
    },
    {
      "course_id":"014995",
      "subject":"OPTOM",
      "catalog_number":"681",
      "title":"Ageing and Vision"
    },
    {
      "course_id":"002210",
      "subject":"PHYS",
      "catalog_number":"736",
      "title":"Optical Properties of Semiconductors"
    },
    {
      "course_id":"002064",
      "subject":"OPTOM",
      "catalog_number":"610",
      "title":"The Comparative Anatomy and Physiology of the Vertbrate Eye"
    },
    {
      "course_id":"002065",
      "subject":"OPTOM",
      "catalog_number":"611",
      "title":"Epidemiology of Vision Anomalies"
    },
    {
      "course_id":"002066",
      "subject":"OPTOM",
      "catalog_number":"613",
      "title":"Visual Development"
    },
    {
      "course_id":"002068",
      "subject":"OPTOM",
      "catalog_number":"614A",
      "title":"Clinical OptometryPart 1-MSc"
    },
    {
      "course_id":"002069",
      "subject":"OPTOM",
      "catalog_number":"614B",
      "title":"Clinical Optometry Part 2 - MSc"
    },
    {
      "course_id":"002070",
      "subject":"OPTOM",
      "catalog_number":"615",
      "title":"Visual Psychophysics"
    },
    {
      "course_id":"002071",
      "subject":"OPTOM",
      "catalog_number":"616",
      "title":"Research Methodology for Vision Science"
    },
    {
      "course_id":"011798",
      "subject":"OPTOM",
      "catalog_number":"620",
      "title":"Data Analysis in Vision Science"
    },
    {
      "course_id":"009139",
      "subject":"OPTOM",
      "catalog_number":"624A",
      "title":"Clinical Optometry Part 1 - PhD"
    },
    {
      "course_id":"009140",
      "subject":"OPTOM",
      "catalog_number":"624B",
      "title":"Clinical Optometry Part 2-PhD"
    },
    {
      "course_id":"002072",
      "subject":"OPTOM",
      "catalog_number":"628",
      "title":"Special Topics in Vision Science"
    },
    {
      "course_id":"014948",
      "subject":"OPTOM",
      "catalog_number":"651",
      "title":"Data Analysis in Vision Science"
    },
    {
      "course_id":"014949",
      "subject":"OPTOM",
      "catalog_number":"660",
      "title":"Visual Psychophysics"
    },
    {
      "course_id":"014939",
      "subject":"PHARM",
      "catalog_number":"601",
      "title":"MSc Thesis Proposal"
    },
    {
      "course_id":"009473",
      "subject":"OPTOM",
      "catalog_number":"630",
      "title":"Principles of Clinical Instruction"
    },
    {
      "course_id":"010514",
      "subject":"OPTOM",
      "catalog_number":"631",
      "title":"Graduate Clinic"
    },
    {
      "course_id":"002083",
      "subject":"OPTOM",
      "catalog_number":"690A",
      "title":"Vision Science Part 1"
    },
    {
      "course_id":"002084",
      "subject":"OPTOM",
      "catalog_number":"690B",
      "title":"Vision Science Part II"
    },
    {
      "course_id":"014548",
      "subject":"PACS",
      "catalog_number":"101",
      "title":"Peace is Everybody's Business"
    },
    {
      "course_id":"007191",
      "subject":"PACS",
      "catalog_number":"201",
      "title":"Roots of Conflict, Violence, and Peace"
    },
    {
      "course_id":"007192",
      "subject":"PACS",
      "catalog_number":"202",
      "title":"Conflict Resolution"
    },
    {
      "course_id":"011120",
      "subject":"PACS",
      "catalog_number":"203",
      "title":"A History of Peace Movements"
    },
    {
      "course_id":"010211",
      "subject":"PACS",
      "catalog_number":"301",
      "title":"Special Topics in Peace and Conflict Studies 1"
    },
    {
      "course_id":"007203",
      "subject":"PACS",
      "catalog_number":"302",
      "title":"Special Topics in Peace and Conflict Studies 2"
    },
    {
      "course_id":"007210",
      "subject":"PACS",
      "catalog_number":"311",
      "title":"Doing Development: Issues of Justice and Peace"
    },
    {
      "course_id":"007211",
      "subject":"PACS",
      "catalog_number":"312",
      "title":"Quest for Peace in Literature and Film"
    },
    {
      "course_id":"007212",
      "subject":"PACS",
      "catalog_number":"313",
      "title":"Community Conflict Resolution"
    },
    {
      "course_id":"007213",
      "subject":"PACS",
      "catalog_number":"314",
      "title":"Conflict Resolution in the Schools"
    },
    {
      "course_id":"009925",
      "subject":"PACS",
      "catalog_number":"316",
      "title":"Violence, Non-violence, and War"
    },
    {
      "course_id":"009927",
      "subject":"PACS",
      "catalog_number":"318",
      "title":"Peace-building, Human Rights, and Civil Society"
    },
    {
      "course_id":"008329",
      "subject":"PACS",
      "catalog_number":"320",
      "title":"Christian Approaches to Peacemaking"
    },
    {
      "course_id":"011121",
      "subject":"PACS",
      "catalog_number":"321",
      "title":"Gender in War and Peace"
    },
    {
      "course_id":"007201",
      "subject":"PACS",
      "catalog_number":"323",
      "title":"Negotiation: Theories and Strategies"
    },
    {
      "course_id":"011009",
      "subject":"PACS",
      "catalog_number":"324",
      "title":"Human Rights, Peace, and Business"
    },
    {
      "course_id":"012189",
      "subject":"PACS",
      "catalog_number":"326",
      "title":"Religion and Peace-Building"
    },
    {
      "course_id":"013306",
      "subject":"PACS",
      "catalog_number":"327",
      "title":"Cultural Approaches to Conflict Resolution"
    },
    {
      "course_id":"013486",
      "subject":"PACS",
      "catalog_number":"328",
      "title":"Fair Trade"
    },
    {
      "course_id":"013487",
      "subject":"PACS",
      "catalog_number":"329",
      "title":"Restorative Justice"
    },
    {
      "course_id":"008399",
      "subject":"PACS",
      "catalog_number":"330",
      "title":"War and Peace in Christian Theology"
    },
    {
      "course_id":"014277",
      "subject":"PACS",
      "catalog_number":"331",
      "title":"Trauma, Healing and Conflict Resolution"
    },
    {
      "course_id":"007215",
      "subject":"PACS",
      "catalog_number":"390",
      "title":"Internship"
    },
    {
      "course_id":"013484",
      "subject":"PACS",
      "catalog_number":"391",
      "title":"Conflict Resolution Skills"
    },
    {
      "course_id":"013485",
      "subject":"PACS",
      "catalog_number":"395",
      "title":"Peace and Conflict Studies Travel Course"
    },
    {
      "course_id":"007217",
      "subject":"PACS",
      "catalog_number":"398",
      "title":"Directed Readings in Peace and Conflict Studies"
    },
    {
      "course_id":"007218",
      "subject":"PACS",
      "catalog_number":"399",
      "title":"Directed Readings in Peace and Conflict Studies"
    },
    {
      "course_id":"012182",
      "subject":"PACS",
      "catalog_number":"401",
      "title":"Senior Research Seminar"
    },
    {
      "course_id":"012195",
      "subject":"PACS",
      "catalog_number":"402",
      "title":"Senior Research Seminar"
    },
    {
      "course_id":"014154",
      "subject":"PACS",
      "catalog_number":"601",
      "title":"Systems of Peace, Order, and Good Governance"
    },
    {
      "course_id":"014155",
      "subject":"PACS",
      "catalog_number":"602",
      "title":"The Practice of Peace"
    },
    {
      "course_id":"014156",
      "subject":"PACS",
      "catalog_number":"603",
      "title":"Building Civil Society"
    },
    {
      "course_id":"014157",
      "subject":"PACS",
      "catalog_number":"604",
      "title":"Conflict Analysis"
    },
    {
      "course_id":"014158",
      "subject":"PACS",
      "catalog_number":"605",
      "title":"Conflict Transformation and Peacebuilding"
    },
    {
      "course_id":"014159",
      "subject":"PACS",
      "catalog_number":"610",
      "title":"Contemporary Nonviolent Movements"
    },
    {
      "course_id":"014160",
      "subject":"PACS",
      "catalog_number":"611",
      "title":"Reconciliation"
    },
    {
      "course_id":"014172",
      "subject":"PACS",
      "catalog_number":"612",
      "title":"Culture, Religion, and Peacebuilding"
    },
    {
      "course_id":"014173",
      "subject":"PACS",
      "catalog_number":"620",
      "title":"Special Topics in Peace and Conflict Studies"
    },
    {
      "course_id":"014174",
      "subject":"PACS",
      "catalog_number":"621",
      "title":"Peace Research"
    },
    {
      "course_id":"014175",
      "subject":"PACS",
      "catalog_number":"625",
      "title":"Internship"
    },
    {
      "course_id":"014176",
      "subject":"PACS",
      "catalog_number":"626",
      "title":"Conflict Resolution Skills Training"
    },
    {
      "course_id":"002468",
      "subject":"PACS",
      "catalog_number":"630",
      "title":"Governance of Global Economy"
    },
    {
      "course_id":"002419",
      "subject":"PACS",
      "catalog_number":"631",
      "title":"Theories of Globalization"
    },
    {
      "course_id":"002444",
      "subject":"PACS",
      "catalog_number":"632",
      "title":"Post-War Reconstruction and State Building"
    },
    {
      "course_id":"002448",
      "subject":"PACS",
      "catalog_number":"633",
      "title":"Human Rights in the Globalized World"
    },
    {
      "course_id":"002461",
      "subject":"PACS",
      "catalog_number":"634",
      "title":"Security Ontology-Theory"
    },
    {
      "course_id":"013686",
      "subject":"PACS",
      "catalog_number":"635",
      "title":"Security Governance: Actors, Institutions, and Issues"
    },
    {
      "course_id":"014121",
      "subject":"PACS",
      "catalog_number":"650",
      "title":"Sustainable Cities"
    },
    {
      "course_id":"014013",
      "subject":"PACS",
      "catalog_number":"651",
      "title":"Economics for Sustainable Development"
    },
    {
      "course_id":"014015",
      "subject":"PACS",
      "catalog_number":"652",
      "title":"Water and Security"
    },
    {
      "course_id":"002423",
      "subject":"PACS",
      "catalog_number":"660",
      "title":"Justice and Gender"
    },
    {
      "course_id":"002445",
      "subject":"PACS",
      "catalog_number":"661",
      "title":"Ethnic Conflict and Conflict Resolution I"
    },
    {
      "course_id":"002449",
      "subject":"PACS",
      "catalog_number":"662",
      "title":"Conflict and Conflict Resolution"
    },
    {
      "course_id":"012819",
      "subject":"PACS",
      "catalog_number":"670",
      "title":"War and Peace in Christian Thought"
    },
    {
      "course_id":"012802",
      "subject":"PACS",
      "catalog_number":"671",
      "title":"The Bible and Peace"
    },
    {
      "course_id":"012833",
      "subject":"PACS",
      "catalog_number":"672",
      "title":"Christianity's Encounter with Other Faiths"
    },
    {
      "course_id":"012559",
      "subject":"PD",
      "catalog_number":"1",
      "title":"Co-op Fundamentals"
    },
    {
      "course_id":"012636",
      "subject":"PD",
      "catalog_number":"2",
      "title":"Critical Reflection and Report Writing"
    },
    {
      "course_id":"012637",
      "subject":"PD",
      "catalog_number":"3",
      "title":"Communication"
    },
    {
      "course_id":"012770",
      "subject":"PD",
      "catalog_number":"4",
      "title":"Teamwork"
    },
    {
      "course_id":"012988",
      "subject":"PD",
      "catalog_number":"5",
      "title":"Project Management"
    },
    {
      "course_id":"012989",
      "subject":"PD",
      "catalog_number":"6",
      "title":"Problem Solving"
    },
    {
      "course_id":"012990",
      "subject":"PD",
      "catalog_number":"7",
      "title":"Conflict Resolution"
    },
    {
      "course_id":"014258",
      "subject":"PD",
      "catalog_number":"8",
      "title":"Intercultural Skills"
    },
    {
      "course_id":"014451",
      "subject":"PD",
      "catalog_number":"9",
      "title":"Ethical Decision Making"
    },
    {
      "course_id":"013870",
      "subject":"PD",
      "catalog_number":"20",
      "title":"Engineering Workplace Skills I: Developing Reasoned Conclusions"
    },
    {
      "course_id":"013871",
      "subject":"PD",
      "catalog_number":"21",
      "title":"Engineering Workplace Skills II: Developing Effective Plans"
    },
    {
      "course_id":"014339",
      "subject":"PD",
      "catalog_number":"22",
      "title":"Professionalism and Ethics in Engineering Practice"
    },
    {
      "course_id":"014333",
      "subject":"PDARCH",
      "catalog_number":"1",
      "title":"Portfolio Development"
    },
    {
      "course_id":"014332",
      "subject":"PDARCH",
      "catalog_number":"2",
      "title":"Co-op Fundamentals for Architects"
    },
    {
      "course_id":"012459",
      "subject":"PHARM",
      "catalog_number":"120",
      "title":"Introduction to the Profession of Pharmacy"
    },
    {
      "course_id":"014334",
      "subject":"PDARCH",
      "catalog_number":"3",
      "title":"Electronic Communications and Web Design"
    },
    {
      "course_id":"014335",
      "subject":"PDARCH",
      "catalog_number":"4",
      "title":"Writing, Editing and Research"
    },
    {
      "course_id":"013412",
      "subject":"PDPHRM",
      "catalog_number":"1",
      "title":"Co-op Fundamentals"
    },
    {
      "course_id":"013413",
      "subject":"PDPHRM",
      "catalog_number":"2",
      "title":"Communication for Pharmacy"
    },
    {
      "course_id":"013414",
      "subject":"PDPHRM",
      "catalog_number":"3",
      "title":"Drug Distribution for Pharmacy"
    },
    {
      "course_id":"013415",
      "subject":"PDPHRM",
      "catalog_number":"4",
      "title":"Patient Safety for Pharmacy"
    },
    {
      "course_id":"013416",
      "subject":"PDPHRM",
      "catalog_number":"5",
      "title":"Patient Care for Pharmacy"
    },
    {
      "course_id":"013417",
      "subject":"PDPHRM",
      "catalog_number":"6",
      "title":"Drug Information for Pharmacy"
    },
    {
      "course_id":"013418",
      "subject":"PDPHRM",
      "catalog_number":"7",
      "title":"Interprofessional Relations"
    },
    {
      "course_id":"013419",
      "subject":"PDPHRM",
      "catalog_number":"8",
      "title":"Pharmacy Practice - Management and Leadership"
    },
    {
      "course_id":"013120",
      "subject":"PHARM",
      "catalog_number":"110",
      "title":"Systems Approach to the Study of the Human Body 1"
    },
    {
      "course_id":"013121",
      "subject":"PHARM",
      "catalog_number":"111",
      "title":"Systems Approach to the Study of the Human Body 2"
    },
    {
      "course_id":"012459",
      "subject":"PHARM",
      "catalog_number":"120A",
      "title":"Introduction to the Profession of Pharmacy"
    },
    {
      "course_id":"013128",
      "subject":"PHARM",
      "catalog_number":"120B",
      "title":"Introduction to the Profession of Pharmacy"
    },
    {
      "course_id":"012458",
      "subject":"PHARM",
      "catalog_number":"124",
      "title":"Pharmaceutics 1"
    },
    {
      "course_id":"012460",
      "subject":"PHARM",
      "catalog_number":"125",
      "title":"Pharmaceutics 2"
    },
    {
      "course_id":"013420",
      "subject":"PHARM",
      "catalog_number":"126",
      "title":"Pharmaceutical Calculations"
    },
    {
      "course_id":"012461",
      "subject":"PHARM",
      "catalog_number":"127",
      "title":"Professional Communication Skills in Pharmacy Practice"
    },
    {
      "course_id":"012462",
      "subject":"PHARM",
      "catalog_number":"128",
      "title":"Professional Communication Skills in Pharmacy Practice 2"
    },
    {
      "course_id":"012463",
      "subject":"PHARM",
      "catalog_number":"129",
      "title":"Professional Practice 1"
    },
    {
      "course_id":"012464",
      "subject":"PHARM",
      "catalog_number":"130",
      "title":"Professional Practice 2"
    },
    {
      "course_id":"012483",
      "subject":"PHARM",
      "catalog_number":"151",
      "title":"Foundation and Application of Health Informatics"
    },
    {
      "course_id":"012465",
      "subject":"PHARM",
      "catalog_number":"131",
      "title":"Professional Practice Laboratory 1"
    },
    {
      "course_id":"012467",
      "subject":"PHARM",
      "catalog_number":"141",
      "title":"Introduction to Medicinal Chemistry, Toxicology and Pharmacology"
    },
    {
      "course_id":"012468",
      "subject":"PHARM",
      "catalog_number":"150",
      "title":"Introduction to Applied Pharmaceutical Sciences"
    },
    {
      "course_id":"012470",
      "subject":"PHARM",
      "catalog_number":"220",
      "title":"Integrated Patient Focused Care 1"
    },
    {
      "course_id":"012471",
      "subject":"PHARM",
      "catalog_number":"221",
      "title":"Integrated Patient Focused Care 2"
    },
    {
      "course_id":"013124",
      "subject":"PHARM",
      "catalog_number":"222",
      "title":"Integrated Patient Focused Care 3"
    },
    {
      "course_id":"013125",
      "subject":"PHARM",
      "catalog_number":"223",
      "title":"Integrated Patient Focused Care 4"
    },
    {
      "course_id":"012472",
      "subject":"PHARM",
      "catalog_number":"224",
      "title":"Pharmacokinetic Fundamentals"
    },
    {
      "course_id":"012474",
      "subject":"PHARM",
      "catalog_number":"227",
      "title":"Health Systems in Society"
    },
    {
      "course_id":"012475",
      "subject":"PHARM",
      "catalog_number":"228",
      "title":"Professional Practice 3"
    },
    {
      "course_id":"012476",
      "subject":"PHARM",
      "catalog_number":"229",
      "title":"Professional Practice 4"
    },
    {
      "course_id":"013122",
      "subject":"PHARM",
      "catalog_number":"232",
      "title":"Medical Microbiology"
    },
    {
      "course_id":"013122",
      "subject":"PHARM",
      "catalog_number":"232L",
      "title":"Medical Microbiology Laboratory 1"
    },
    {
      "course_id":"013123",
      "subject":"PHARM",
      "catalog_number":"233L",
      "title":"Medical Microbiology Laboratory 2"
    },
    {
      "course_id":"012492",
      "subject":"PHARM",
      "catalog_number":"237",
      "title":"Applications of Analyses and Devices in Pharmacy and Medicine"
    },
    {
      "course_id":"012482",
      "subject":"PHARM",
      "catalog_number":"252",
      "title":"Institutional Pharmacy Practice"
    },
    {
      "course_id":"014742",
      "subject":"PHARM",
      "catalog_number":"378",
      "title":"Advanced Women's Health Pharmacotherapeutics"
    },
    {
      "course_id":"012483",
      "subject":"PHARM",
      "catalog_number":"262",
      "title":"Foundation and Application of Health Informatics"
    },
    {
      "course_id":"012484",
      "subject":"PHARM",
      "catalog_number":"290",
      "title":"Seminars in Pharmacy 1"
    },
    {
      "course_id":"012486",
      "subject":"PHARM",
      "catalog_number":"320",
      "title":"Integrated Patient Focused Care 5"
    },
    {
      "course_id":"012487",
      "subject":"PHARM",
      "catalog_number":"321",
      "title":"Integrated Patient Focused Care 6"
    },
    {
      "course_id":"012488",
      "subject":"PHARM",
      "catalog_number":"322",
      "title":"Clinical Application of Pharmaceutical Sciences"
    },
    {
      "course_id":"012494",
      "subject":"PHARM",
      "catalog_number":"329",
      "title":"Professional Practice 5"
    },
    {
      "course_id":"012496",
      "subject":"PHARM",
      "catalog_number":"350",
      "title":"Fundamentals of Business Administration and Management"
    },
    {
      "course_id":"012503",
      "subject":"PHARM",
      "catalog_number":"391",
      "title":"Seminars in Pharmacy 2"
    },
    {
      "course_id":"013363",
      "subject":"PHARM",
      "catalog_number":"361",
      "title":"Advanced Compounding"
    },
    {
      "course_id":"013364",
      "subject":"PHARM",
      "catalog_number":"362",
      "title":"Advanced Patient Self Care"
    },
    {
      "course_id":"013365",
      "subject":"PHARM",
      "catalog_number":"363",
      "title":"Global Infectious Disease Management"
    },
    {
      "course_id":"013367",
      "subject":"PHARM",
      "catalog_number":"364",
      "title":"The Pharmacist as Educator"
    },
    {
      "course_id":"013366",
      "subject":"PHARM",
      "catalog_number":"365",
      "title":"Biotech Pharma Business Strategy"
    },
    {
      "course_id":"013791",
      "subject":"PHARM",
      "catalog_number":"366",
      "title":"Concepts in Nutritional Sciences"
    },
    {
      "course_id":"013792",
      "subject":"PHARM",
      "catalog_number":"367",
      "title":"Pediatric Pharmacy"
    },
    {
      "course_id":"013793",
      "subject":"PHARM",
      "catalog_number":"368",
      "title":"Advanced Drug Information & Evidence-Based Medicine"
    },
    {
      "course_id":"013794",
      "subject":"PHARM",
      "catalog_number":"369",
      "title":"Global Medical Aid"
    },
    {
      "course_id":"013795",
      "subject":"PHARM",
      "catalog_number":"370",
      "title":"Personal & New Venture Financial Management"
    },
    {
      "course_id":"013796",
      "subject":"PHARM",
      "catalog_number":"371",
      "title":"Advanced Topics in Health Economics"
    },
    {
      "course_id":"013797",
      "subject":"PHARM",
      "catalog_number":"372",
      "title":"Strategic Global Health & Pharmacy Practice"
    },
    {
      "course_id":"014161",
      "subject":"PHARM",
      "catalog_number":"373",
      "title":"Healthcare Delivery in Rural and Underserved Populations"
    },
    {
      "course_id":"014162",
      "subject":"PHARM",
      "catalog_number":"374",
      "title":"Complementary and Alternate Medicine"
    },
    {
      "course_id":"014163",
      "subject":"PHARM",
      "catalog_number":"375",
      "title":"Substance Abuse & Chemical Dependency"
    },
    {
      "course_id":"014164",
      "subject":"PHARM",
      "catalog_number":"376",
      "title":"Practicing Pharmacy with Diverse Populations"
    },
    {
      "course_id":"014165",
      "subject":"PHARM",
      "catalog_number":"377",
      "title":"Drug-Induced Disease"
    },
    {
      "course_id":"012504",
      "subject":"PHARM",
      "catalog_number":"400",
      "title":"Independent Study 1"
    },
    {
      "course_id":"012505",
      "subject":"PHARM",
      "catalog_number":"401",
      "title":"Independent Study 2"
    },
    {
      "course_id":"012509",
      "subject":"PHARM",
      "catalog_number":"415A",
      "title":"Clinical Rotation: Integrated Care"
    },
    {
      "course_id":"014331",
      "subject":"PHARM",
      "catalog_number":"415B",
      "title":"Clinical Rotation: Integrated Care"
    },
    {
      "course_id":"013126",
      "subject":"PHARM",
      "catalog_number":"420",
      "title":"Integrated Patient Focused Care 7"
    },
    {
      "course_id":"012510",
      "subject":"PHARM",
      "catalog_number":"421",
      "title":"Integrated Patient Focused Care 8"
    },
    {
      "course_id":"013127",
      "subject":"PHARM",
      "catalog_number":"422",
      "title":"Integrated Patient Focused Care 9"
    },
    {
      "course_id":"012493",
      "subject":"PHARM",
      "catalog_number":"428",
      "title":"Professional Practice 4"
    },
    {
      "course_id":"013798",
      "subject":"PHARM",
      "catalog_number":"460",
      "title":"Leadership in Pharmacy"
    },
    {
      "course_id":"013799",
      "subject":"PHARM",
      "catalog_number":"461",
      "title":"Advanced Patient Safety"
    },
    {
      "course_id":"013800",
      "subject":"PHARM",
      "catalog_number":"462",
      "title":"Interprofessional Case Management"
    },
    {
      "course_id":"013801",
      "subject":"PHARM",
      "catalog_number":"464",
      "title":"Advanced Therapeutic Concepts in Oncology"
    },
    {
      "course_id":"013802",
      "subject":"PHARM",
      "catalog_number":"465",
      "title":"Critical Care & Emergency Medicine for Pharmacists"
    },
    {
      "course_id":"013803",
      "subject":"PHARM",
      "catalog_number":"466",
      "title":"Advanced Geriatric Care"
    },
    {
      "course_id":"013804",
      "subject":"PHARM",
      "catalog_number":"467",
      "title":"Management of Oral Anticoagulation Therapy"
    },
    {
      "course_id":"014166",
      "subject":"PHARM",
      "catalog_number":"468",
      "title":"Clinical Neurology in Family Practice"
    },
    {
      "course_id":"014167",
      "subject":"PHARM",
      "catalog_number":"469",
      "title":"Pharmacoepidemiology and Pharmacy Practice"
    },
    {
      "course_id":"014168",
      "subject":"PHARM",
      "catalog_number":"470",
      "title":"Advanced Medical Writing"
    },
    {
      "course_id":"014169",
      "subject":"PHARM",
      "catalog_number":"471",
      "title":"Selected Topics in Medicinal Chemistry"
    },
    {
      "course_id":"014170",
      "subject":"PHARM",
      "catalog_number":"472",
      "title":"Community Practice in a Changing Environment"
    },
    {
      "course_id":"012503",
      "subject":"PHARM",
      "catalog_number":"490",
      "title":"Seminars in Pharmacy 2"
    },
    {
      "course_id":"012522",
      "subject":"PHARM",
      "catalog_number":"491",
      "title":"Seminars in Pharmacy 3"
    },
    {
      "course_id":"014809",
      "subject":"PHARM",
      "catalog_number":"495",
      "title":"Advanced Topics in Patient Focused Care"
    },
    {
      "course_id":"013817",
      "subject":"PHARM",
      "catalog_number":"602",
      "title":"Grant Writing in the Sciences"
    },
    {
      "course_id":"013818",
      "subject":"PHARM",
      "catalog_number":"603",
      "title":"Selected Topics in Medicinal Chemistry"
    },
    {
      "course_id":"013819",
      "subject":"PHARM",
      "catalog_number":"604",
      "title":"Gene Therapy"
    },
    {
      "course_id":"013820",
      "subject":"PHARM",
      "catalog_number":"605",
      "title":"Physical Chemistry and Application of Surfactants"
    },
    {
      "course_id":"013821",
      "subject":"PHARM",
      "catalog_number":"606",
      "title":"Neuroscience in the 21st Century"
    },
    {
      "course_id":"013822",
      "subject":"PHARM",
      "catalog_number":"607",
      "title":"Advanced Pharmaceutical Analysis"
    },
    {
      "course_id":"013919",
      "subject":"PHARM",
      "catalog_number":"608A",
      "title":"Selected Topics in Pharmaceutical Sciences 1"
    },
    {
      "course_id":"014082",
      "subject":"PHARM",
      "catalog_number":"609",
      "title":"Advanced Pharmacokinetics"
    },
    {
      "course_id":"014083",
      "subject":"PHARM",
      "catalog_number":"610",
      "title":"Topics in Drug Development"
    },
    {
      "course_id":"014366",
      "subject":"PHARM",
      "catalog_number":"611",
      "title":"Special Topics in Pharmacy Practice"
    },
    {
      "course_id":"007231",
      "subject":"PHIL",
      "catalog_number":"100J",
      "title":"Introduction to Philosophy"
    },
    {
      "course_id":"007228",
      "subject":"PHIL",
      "catalog_number":"110A",
      "title":"Introduction to Philosophy: Knowledge and Reality"
    },
    {
      "course_id":"010344",
      "subject":"PHIL",
      "catalog_number":"110B",
      "title":"Introduction to Philosophy: Ethics and Values"
    },
    {
      "course_id":"007241",
      "subject":"PHIL",
      "catalog_number":"118J",
      "title":"The Moral Life"
    },
    {
      "course_id":"007242",
      "subject":"PHIL",
      "catalog_number":"120J",
      "title":"Philosophy of Life and Death"
    },
    {
      "course_id":"007246",
      "subject":"PHIL",
      "catalog_number":"145",
      "title":"Critical Thinking"
    },
    {
      "course_id":"007250",
      "subject":"PHIL",
      "catalog_number":"200J",
      "title":"Aristotelian Logic"
    },
    {
      "course_id":"007251",
      "subject":"PHIL",
      "catalog_number":"201",
      "title":"Philosophy of Sex and Love"
    },
    {
      "course_id":"007253",
      "subject":"PHIL",
      "catalog_number":"202",
      "title":"Gender Issues"
    },
    {
      "course_id":"007254",
      "subject":"PHIL",
      "catalog_number":"204J",
      "title":"Philosophy and Culture"
    },
    {
      "course_id":"007259",
      "subject":"PHIL",
      "catalog_number":"208",
      "title":"Philosophy Through Science Fiction"
    },
    {
      "course_id":"007260",
      "subject":"PHIL",
      "catalog_number":"209",
      "title":"Philosophy in Literature"
    },
    {
      "course_id":"007263",
      "subject":"PHIL",
      "catalog_number":"210J",
      "title":"Philosophy of Human Nature"
    },
    {
      "course_id":"007266",
      "subject":"PHIL",
      "catalog_number":"215",
      "title":"Professional and Business Ethics"
    },
    {
      "course_id":"007267",
      "subject":"PHIL",
      "catalog_number":"216",
      "title":"Probability and Decision Making"
    },
    {
      "course_id":"007269",
      "subject":"PHIL",
      "catalog_number":"218J",
      "title":"Ethical Theory"
    },
    {
      "course_id":"007270",
      "subject":"PHIL",
      "catalog_number":"219J",
      "title":"Practical Ethics"
    },
    {
      "course_id":"007271",
      "subject":"PHIL",
      "catalog_number":"220",
      "title":"Moral Issues"
    },
    {
      "course_id":"007272",
      "subject":"PHIL",
      "catalog_number":"221",
      "title":"Ethics"
    },
    {
      "course_id":"007274",
      "subject":"PHIL",
      "catalog_number":"224",
      "title":"Environmental Ethics"
    },
    {
      "course_id":"007275",
      "subject":"PHIL",
      "catalog_number":"226",
      "title":"Biomedical Ethics"
    },
    {
      "course_id":"012678",
      "subject":"PHIL",
      "catalog_number":"227",
      "title":"Culture and Ethics"
    },
    {
      "course_id":"007277",
      "subject":"PHIL",
      "catalog_number":"230J",
      "title":"God and Philosophy"
    },
    {
      "course_id":"007281",
      "subject":"PHIL",
      "catalog_number":"237",
      "title":"Introduction to the Philosophy of Religion"
    },
    {
      "course_id":"007285",
      "subject":"PHIL",
      "catalog_number":"240",
      "title":"Introduction to Formal Logic"
    },
    {
      "course_id":"013567",
      "subject":"PHIL",
      "catalog_number":"245",
      "title":"Critical Thinking About Science"
    },
    {
      "course_id":"007248",
      "subject":"PHIL",
      "catalog_number":"250A",
      "title":"Great Works: Ancient and Medieval"
    },
    {
      "course_id":"007249",
      "subject":"PHIL",
      "catalog_number":"250B",
      "title":"Great Works: Modern"
    },
    {
      "course_id":"007292",
      "subject":"PHIL",
      "catalog_number":"255",
      "title":"Philosophy of Mind"
    },
    {
      "course_id":"007293",
      "subject":"PHIL",
      "catalog_number":"256",
      "title":"Introduction to Cognitive Science"
    },
    {
      "course_id":"008523",
      "subject":"PHIL",
      "catalog_number":"258",
      "title":"Introduction to the Philosophy of Science"
    },
    {
      "course_id":"011904",
      "subject":"PHIL",
      "catalog_number":"259",
      "title":"Philosophy of Technology"
    },
    {
      "course_id":"007297",
      "subject":"PHIL",
      "catalog_number":"265",
      "title":"The Existentialist Experience"
    },
    {
      "course_id":"013568",
      "subject":"PHIL",
      "catalog_number":"271",
      "title":"Special Topics"
    },
    {
      "course_id":"007256",
      "subject":"PHIL",
      "catalog_number":"305J",
      "title":"Philosophy of Nature"
    },
    {
      "course_id":"007257",
      "subject":"PHIL",
      "catalog_number":"306J",
      "title":"Philosophy of Science"
    },
    {
      "course_id":"007305",
      "subject":"PHIL",
      "catalog_number":"311",
      "title":"Philosophy of Education"
    },
    {
      "course_id":"005811",
      "subject":"PHIL",
      "catalog_number":"315",
      "title":"Ethics and The Engineering Profession"
    },
    {
      "course_id":"007308",
      "subject":"PHIL",
      "catalog_number":"318J",
      "title":"Philosophy and the Family"
    },
    {
      "course_id":"007309",
      "subject":"PHIL",
      "catalog_number":"319J",
      "title":"Bioethics"
    },
    {
      "course_id":"010346",
      "subject":"PHIL",
      "catalog_number":"324",
      "title":"Social and Political Philosophy"
    },
    {
      "course_id":"007311",
      "subject":"PHIL",
      "catalog_number":"327",
      "title":"Philosophy of Law"
    },
    {
      "course_id":"011185",
      "subject":"PHIL",
      "catalog_number":"328",
      "title":"Human Rights"
    },
    {
      "course_id":"009925",
      "subject":"PHIL",
      "catalog_number":"329",
      "title":"Violence, Non-violence, and War"
    },
    {
      "course_id":"007315",
      "subject":"PHIL",
      "catalog_number":"331",
      "title":"Philosophy of Art"
    },
    {
      "course_id":"009525",
      "subject":"PHIL",
      "catalog_number":"341",
      "title":"Intermediate Classical Logic"
    },
    {
      "course_id":"009526",
      "subject":"PHIL",
      "catalog_number":"342",
      "title":"Non-Standard Logics"
    },
    {
      "course_id":"007317",
      "subject":"PHIL",
      "catalog_number":"350",
      "title":"Theories of Knowledge"
    },
    {
      "course_id":"007322",
      "subject":"PHIL",
      "catalog_number":"362",
      "title":"Philosophy of the Social Sciences"
    },
    {
      "course_id":"009527",
      "subject":"PHIL",
      "catalog_number":"355",
      "title":"Theories of Reality"
    },
    {
      "course_id":"007320",
      "subject":"PHIL",
      "catalog_number":"359",
      "title":"Philosophy of Mathematics"
    },
    {
      "course_id":"009528",
      "subject":"PHIL",
      "catalog_number":"363",
      "title":"Philosophy of Language"
    },
    {
      "course_id":"013569",
      "subject":"PHIL",
      "catalog_number":"371",
      "title":"Special Topics"
    },
    {
      "course_id":"007323",
      "subject":"PHIL",
      "catalog_number":"378",
      "title":"American Philosophy"
    },
    {
      "course_id":"007324",
      "subject":"PHIL",
      "catalog_number":"380",
      "title":"History of Ancient Philosophy"
    },
    {
      "course_id":"007325",
      "subject":"PHIL",
      "catalog_number":"381",
      "title":"History of Ancient Philosophy 2"
    },
    {
      "course_id":"007326",
      "subject":"PHIL",
      "catalog_number":"382",
      "title":"Medieval Philosophy"
    },
    {
      "course_id":"007327",
      "subject":"PHIL",
      "catalog_number":"383",
      "title":"Medieval Philosophy 2"
    },
    {
      "course_id":"007328",
      "subject":"PHIL",
      "catalog_number":"384",
      "title":"History of Modern Philosophy"
    },
    {
      "course_id":"007329",
      "subject":"PHIL",
      "catalog_number":"385",
      "title":"History of Modern Philosophy 2"
    },
    {
      "course_id":"007330",
      "subject":"PHIL",
      "catalog_number":"386",
      "title":"19th-Century Philosophy"
    },
    {
      "course_id":"007335",
      "subject":"PHIL",
      "catalog_number":"402",
      "title":"Studies in Feminist Philosophy\/Philosophy of Sex"
    },
    {
      "course_id":"011189",
      "subject":"PHIL",
      "catalog_number":"403",
      "title":"Studies in Ancient Philosophy"
    },
    {
      "course_id":"011190",
      "subject":"PHIL",
      "catalog_number":"404",
      "title":"Studies in Medieval Philosophy"
    },
    {
      "course_id":"011191",
      "subject":"PHIL",
      "catalog_number":"405",
      "title":"Studies in Modern Philosophy"
    },
    {
      "course_id":"011193",
      "subject":"PHIL",
      "catalog_number":"407",
      "title":"Studies in 19th Century Philosophy"
    },
    {
      "course_id":"011194",
      "subject":"PHIL",
      "catalog_number":"408",
      "title":"Early 20th Century Philosophy"
    },
    {
      "course_id":"013574",
      "subject":"PHIL",
      "catalog_number":"416",
      "title":"Studies in Probability and Decision Theory"
    },
    {
      "course_id":"007336",
      "subject":"PHIL",
      "catalog_number":"418J",
      "title":"Ethics and Society"
    },
    {
      "course_id":"007337",
      "subject":"PHIL",
      "catalog_number":"420",
      "title":"Studies in Ethics"
    },
    {
      "course_id":"007339",
      "subject":"PHIL",
      "catalog_number":"422",
      "title":"Studies in Political Philosophy"
    },
    {
      "course_id":"007345",
      "subject":"PHIL",
      "catalog_number":"441",
      "title":"Studies in Logic"
    },
    {
      "course_id":"012715",
      "subject":"PHIL",
      "catalog_number":"447",
      "title":"Seminar in Cognitive Science"
    },
    {
      "course_id":"007348",
      "subject":"PHIL",
      "catalog_number":"450J",
      "title":"Being and Existence"
    },
    {
      "course_id":"007349",
      "subject":"PHIL",
      "catalog_number":"451J",
      "title":"Thomas Aquinas"
    },
    {
      "course_id":"013582",
      "subject":"PHIL",
      "catalog_number":"452",
      "title":"Studies in Epistemology"
    },
    {
      "course_id":"007350",
      "subject":"PHIL",
      "catalog_number":"455",
      "title":"Studies in Metaphysics"
    },
    {
      "course_id":"013576",
      "subject":"PHIL",
      "catalog_number":"458",
      "title":"Studies in the Philosophy of Science"
    },
    {
      "course_id":"013577",
      "subject":"PHIL",
      "catalog_number":"459",
      "title":"Studies in the Philosophy of Physics"
    },
    {
      "course_id":"013578",
      "subject":"PHIL",
      "catalog_number":"463",
      "title":"Studies in the Philosophy of Language"
    },
    {
      "course_id":"007355",
      "subject":"PHIL",
      "catalog_number":"471",
      "title":"Special Topics"
    },
    {
      "course_id":"007356",
      "subject":"PHIL",
      "catalog_number":"472",
      "title":"Special Topics"
    },
    {
      "course_id":"007365",
      "subject":"PHIL",
      "catalog_number":"481",
      "title":"Special Topics"
    },
    {
      "course_id":"007366",
      "subject":"PHIL",
      "catalog_number":"482",
      "title":"Special Topics"
    },
    {
      "course_id":"010026",
      "subject":"PHIL",
      "catalog_number":"498",
      "title":"Directed Reading in Special Areas"
    },
    {
      "course_id":"010431",
      "subject":"PHIL",
      "catalog_number":"670",
      "title":"Fall Term Reading Course"
    },
    {
      "course_id":"010432",
      "subject":"PHIL",
      "catalog_number":"671",
      "title":"Winter Term Reading course"
    },
    {
      "course_id":"010433",
      "subject":"PHIL",
      "catalog_number":"672",
      "title":"Spring Term Reading Course"
    },
    {
      "course_id":"010434",
      "subject":"PHIL",
      "catalog_number":"673",
      "title":"Graduate Courses"
    },
    {
      "course_id":"002209",
      "subject":"PHYS",
      "catalog_number":"735",
      "title":"Photoconductivity and Luminescence"
    },
    {
      "course_id":"011841",
      "subject":"PHIL",
      "catalog_number":"674",
      "title":"Graduate Courses"
    },
    {
      "course_id":"011842",
      "subject":"PHIL",
      "catalog_number":"680A",
      "title":"Departmental Graduate Seminar"
    },
    {
      "course_id":"011843",
      "subject":"PHIL",
      "catalog_number":"680B",
      "title":"Departmental Graduate Seminar"
    },
    {
      "course_id":"013641",
      "subject":"PHYS",
      "catalog_number":"191",
      "title":"Electricity and Magnetism"
    },
    {
      "course_id":"010435",
      "subject":"PHIL",
      "catalog_number":"696",
      "title":"Directed Research for MA Candidates"
    },
    {
      "course_id":"010436",
      "subject":"PHIL",
      "catalog_number":"698",
      "title":"Research Area Tutorials for PhD"
    },
    {
      "course_id":"012523",
      "subject":"PHS",
      "catalog_number":"601",
      "title":"Foundations of Public Health"
    },
    {
      "course_id":"012524",
      "subject":"PHS",
      "catalog_number":"602",
      "title":"Capstone Integrative Seminar for Public Health"
    },
    {
      "course_id":"012525",
      "subject":"PHS",
      "catalog_number":"603",
      "title":"Health Policy in Public Health"
    },
    {
      "course_id":"012526",
      "subject":"PHS",
      "catalog_number":"604",
      "title":"Public Health and the Environment"
    },
    {
      "course_id":"012527",
      "subject":"PHS",
      "catalog_number":"605",
      "title":"Quantitative Methods and Analysis"
    },
    {
      "course_id":"012528",
      "subject":"PHS",
      "catalog_number":"606",
      "title":"Principles of Epidemiology for Public Health"
    },
    {
      "course_id":"012529",
      "subject":"PHS",
      "catalog_number":"607",
      "title":"Social, Cultural and Behavioural Aspects of Public Health I"
    },
    {
      "course_id":"012530",
      "subject":"PHS",
      "catalog_number":"608",
      "title":"Health and Risk Communication in Public Health"
    },
    {
      "course_id":"012531",
      "subject":"PHS",
      "catalog_number":"609",
      "title":"Management and Administration of Public Health Services"
    },
    {
      "course_id":"013806",
      "subject":"PHS",
      "catalog_number":"611",
      "title":"The Health Care System"
    },
    {
      "course_id":"013604",
      "subject":"PHS",
      "catalog_number":"612",
      "title":"Data Structures and Standards in Health Informatics"
    },
    {
      "course_id":"014291",
      "subject":"PHS",
      "catalog_number":"613",
      "title":"Information Technology for the Health Professional"
    },
    {
      "course_id":"012532",
      "subject":"PHS",
      "catalog_number":"614",
      "title":"Foundations of Program Evaluation"
    },
    {
      "course_id":"014292",
      "subject":"PHS",
      "catalog_number":"615",
      "title":"Requirements Specification and Analysys in Health Systems"
    },
    {
      "course_id":"014293",
      "subject":"PHS",
      "catalog_number":"616",
      "title":"Decision Making and Systems Thinking in Health Informatics"
    },
    {
      "course_id":"012533",
      "subject":"PHS",
      "catalog_number":"617",
      "title":"Population Intervention for Disease Prevention and Health Promotion"
    },
    {
      "course_id":"012534",
      "subject":"PHS",
      "catalog_number":"623",
      "title":"Risk and Exposure Assessment in Public Health"
    },
    {
      "course_id":"012535",
      "subject":"PHS",
      "catalog_number":"624",
      "title":"Environmental Toxicology in Public Health"
    },
    {
      "course_id":"012536",
      "subject":"PHS",
      "catalog_number":"631",
      "title":"Public Health Surveillance"
    },
    {
      "course_id":"012537",
      "subject":"PHS",
      "catalog_number":"632",
      "title":"Health Economics and Public Health"
    },
    {
      "course_id":"012538",
      "subject":"PHS",
      "catalog_number":"633",
      "title":"Water Quality and Public Health"
    },
    {
      "course_id":"012539",
      "subject":"PHS",
      "catalog_number":"634",
      "title":"Environmental Epidemiology for Public Health"
    },
    {
      "course_id":"012540",
      "subject":"PHS",
      "catalog_number":"635",
      "title":"Public Health, Environment and Planning"
    },
    {
      "course_id":"012541",
      "subject":"PHS",
      "catalog_number":"636",
      "title":"Applied Epidemiology: Advanced Concepts and Applications for Public Health"
    },
    {
      "course_id":"012542",
      "subject":"PHS",
      "catalog_number":"637",
      "title":"Public Health Informatics"
    },
    {
      "course_id":"012543",
      "subject":"PHS",
      "catalog_number":"638",
      "title":"Selected Topics in Public Health"
    },
    {
      "course_id":"012544",
      "subject":"PHS",
      "catalog_number":"641",
      "title":"Professional Experience Practicum"
    },
    {
      "course_id":"002201",
      "subject":"PHYS",
      "catalog_number":"711",
      "title":"Scattering Theory"
    },
    {
      "course_id":"013386",
      "subject":"PHS",
      "catalog_number":"661",
      "title":"Geographic Information  Systems and Public Health"
    },
    {
      "course_id":"013387",
      "subject":"PHS",
      "catalog_number":"662",
      "title":"Global Health"
    },
    {
      "course_id":"013388",
      "subject":"PHS",
      "catalog_number":"663",
      "title":"Human Development  and Health"
    },
    {
      "course_id":"010216",
      "subject":"PHYS",
      "catalog_number":"1",
      "title":"Pre-University Physics"
    },
    {
      "course_id":"009328",
      "subject":"PHYS",
      "catalog_number":"10",
      "title":"Physics Seminar"
    },
    {
      "course_id":"007388",
      "subject":"PHYS",
      "catalog_number":"111",
      "title":"Physics 1"
    },
    {
      "course_id":"007389",
      "subject":"PHYS",
      "catalog_number":"111L",
      "title":"Physics 1 Laboratory"
    },
    {
      "course_id":"007390",
      "subject":"PHYS",
      "catalog_number":"112",
      "title":"Physics 2"
    },
    {
      "course_id":"007391",
      "subject":"PHYS",
      "catalog_number":"112L",
      "title":"Physics 2 Laboratory"
    },
    {
      "course_id":"007392",
      "subject":"PHYS",
      "catalog_number":"115",
      "title":"Mechanics"
    },
    {
      "course_id":"007393",
      "subject":"PHYS",
      "catalog_number":"121",
      "title":"Mechanics"
    },
    {
      "course_id":"007394",
      "subject":"PHYS",
      "catalog_number":"121L",
      "title":"Mechanics Laboratory"
    },
    {
      "course_id":"013651",
      "subject":"PHYS",
      "catalog_number":"122",
      "title":"Waves, Electricity and Magnetism"
    },
    {
      "course_id":"011212",
      "subject":"PHYS",
      "catalog_number":"139",
      "title":"Scientific Computer Programming"
    },
    {
      "course_id":"007396",
      "subject":"PHYS",
      "catalog_number":"122L",
      "title":"Waves, Electricity and Magnetism Laboratory"
    },
    {
      "course_id":"013640",
      "subject":"PHYS",
      "catalog_number":"124",
      "title":"Modern Physics"
    },
    {
      "course_id":"007398",
      "subject":"PHYS",
      "catalog_number":"125",
      "title":"Physics for Engineers"
    },
    {
      "course_id":"010359",
      "subject":"PHYS",
      "catalog_number":"131L",
      "title":"Mechanics Laboratory"
    },
    {
      "course_id":"010360",
      "subject":"PHYS",
      "catalog_number":"132L",
      "title":"Waves, Electricity, Magnetism and Measurement Laboratory"
    },
    {
      "course_id":"013959",
      "subject":"PHYS",
      "catalog_number":"175",
      "title":"Introduction to the Universe"
    },
    {
      "course_id":"013960",
      "subject":"PHYS",
      "catalog_number":"175L",
      "title":"Introduction to the Universe Laboratory"
    },
    {
      "course_id":"007399",
      "subject":"PHYS",
      "catalog_number":"222",
      "title":"Electricity and Magnetism 1"
    },
    {
      "course_id":"007401",
      "subject":"PHYS",
      "catalog_number":"223",
      "title":"Electricity and Magnetism 2"
    },
    {
      "course_id":"013965",
      "subject":"PHYS",
      "catalog_number":"224",
      "title":"Electricity and Magnetism for Life and Medical Physics"
    },
    {
      "course_id":"013966",
      "subject":"PHYS",
      "catalog_number":"224L",
      "title":"Electricity and Magnetism Laboratory"
    },
    {
      "course_id":"013968",
      "subject":"PHYS",
      "catalog_number":"225",
      "title":"Modeling Life Physics"
    },
    {
      "course_id":"007405",
      "subject":"PHYS",
      "catalog_number":"226",
      "title":"Geometrical Optics"
    },
    {
      "course_id":"010361",
      "subject":"PHYS",
      "catalog_number":"232L",
      "title":"Measurement Laboratory"
    },
    {
      "course_id":"013969",
      "subject":"PHYS",
      "catalog_number":"233",
      "title":"Introduction to Quantum Mechanics"
    },
    {
      "course_id":"007407",
      "subject":"PHYS",
      "catalog_number":"234",
      "title":"Quantum Physics 1"
    },
    {
      "course_id":"013642",
      "subject":"PHYS",
      "catalog_number":"236",
      "title":"Computational Physics 1"
    },
    {
      "course_id":"007408",
      "subject":"PHYS",
      "catalog_number":"239",
      "title":"Computational Physics 2"
    },
    {
      "course_id":"007417",
      "subject":"PHYS",
      "catalog_number":"241",
      "title":"Electricity and Magnetism"
    },
    {
      "course_id":"013643",
      "subject":"PHYS",
      "catalog_number":"242",
      "title":"Electricity and Magnetism 1"
    },
    {
      "course_id":"007418",
      "subject":"PHYS",
      "catalog_number":"242L",
      "title":"Electricity and Magnetism Laboratory"
    },
    {
      "course_id":"007411",
      "subject":"PHYS",
      "catalog_number":"246",
      "title":"Physical Optics"
    },
    {
      "course_id":"007422",
      "subject":"PHYS",
      "catalog_number":"256",
      "title":"Geometrical and Physical Optics"
    },
    {
      "course_id":"007423",
      "subject":"PHYS",
      "catalog_number":"256L",
      "title":"Optics Laboratory"
    },
    {
      "course_id":"013118",
      "subject":"PHYS",
      "catalog_number":"260L",
      "title":"Intermediate Physics Laboratory"
    },
    {
      "course_id":"003320",
      "subject":"PHYS",
      "catalog_number":"263",
      "title":"Classical Mechanics and Special Relativity"
    },
    {
      "course_id":"013961",
      "subject":"PHYS",
      "catalog_number":"270",
      "title":"Astronomical Observations, Instrumentation and Data Analysis"
    },
    {
      "course_id":"013963",
      "subject":"PHYS",
      "catalog_number":"270L",
      "title":"Astronomical Observations, Instrumentation and Data Analysis Laboratory"
    },
    {
      "course_id":"007428",
      "subject":"PHYS",
      "catalog_number":"275",
      "title":"Planets"
    },
    {
      "course_id":"012773",
      "subject":"PHYS",
      "catalog_number":"280",
      "title":"Introduction to Biophysics"
    },
    {
      "course_id":"007434",
      "subject":"PHYS",
      "catalog_number":"334",
      "title":"Quantum Physics 2"
    },
    {
      "course_id":"012032",
      "subject":"PHYS",
      "catalog_number":"335",
      "title":"Condensed Matter Physics"
    },
    {
      "course_id":"007435",
      "subject":"PHYS",
      "catalog_number":"339",
      "title":"Scientific Computation 2"
    },
    {
      "course_id":"013644",
      "subject":"PHYS",
      "catalog_number":"342",
      "title":"Electricity and Magnetism 2"
    },
    {
      "course_id":"007444",
      "subject":"PHYS",
      "catalog_number":"358",
      "title":"Thermal Physics"
    },
    {
      "course_id":"007445",
      "subject":"PHYS",
      "catalog_number":"359",
      "title":"Statistical Mechanics"
    },
    {
      "course_id":"007446",
      "subject":"PHYS",
      "catalog_number":"360A",
      "title":"Modern Physics Laboratory 1"
    },
    {
      "course_id":"007447",
      "subject":"PHYS",
      "catalog_number":"360B",
      "title":"Modern Physics Laboratory 2"
    },
    {
      "course_id":"007449",
      "subject":"PHYS",
      "catalog_number":"363",
      "title":"Intermediate Classical Mechanics"
    },
    {
      "course_id":"007450",
      "subject":"PHYS",
      "catalog_number":"364",
      "title":"Mathematical Physics 1"
    },
    {
      "course_id":"007451",
      "subject":"PHYS",
      "catalog_number":"365",
      "title":"Mathematical Physics 2"
    },
    {
      "course_id":"007459",
      "subject":"PHYS",
      "catalog_number":"381",
      "title":"Cellular Biophysics"
    },
    {
      "course_id":"013978",
      "subject":"PHYS",
      "catalog_number":"370L",
      "title":"Astronomy Laboratory 1"
    },
    {
      "course_id":"007457",
      "subject":"PHYS",
      "catalog_number":"375",
      "title":"Stars"
    },
    {
      "course_id":"007458",
      "subject":"PHYS",
      "catalog_number":"380",
      "title":"Molecular and Cellular Biophysics"
    },
    {
      "course_id":"013970",
      "subject":"PHYS",
      "catalog_number":"383",
      "title":"Medical Physics"
    },
    {
      "course_id":"007438",
      "subject":"PHYS",
      "catalog_number":"391",
      "title":"Electronics"
    },
    {
      "course_id":"007439",
      "subject":"PHYS",
      "catalog_number":"391L",
      "title":"Electronics Laboratory"
    },
    {
      "course_id":"007440",
      "subject":"PHYS",
      "catalog_number":"392",
      "title":"Scientific Measurement and Control"
    },
    {
      "course_id":"007441",
      "subject":"PHYS",
      "catalog_number":"392L",
      "title":"Scientific Measurement and Control Laboratory"
    },
    {
      "course_id":"013645",
      "subject":"PHYS",
      "catalog_number":"393",
      "title":"Physical Optics"
    },
    {
      "course_id":"013646",
      "subject":"PHYS",
      "catalog_number":"394",
      "title":"Light-Matter Interactions"
    },
    {
      "course_id":"013659",
      "subject":"PHYS",
      "catalog_number":"395",
      "title":"Biophysics of Therapeutic Methods"
    },
    {
      "course_id":"011381",
      "subject":"PHYS",
      "catalog_number":"396",
      "title":"Biophysics of Imaging"
    },
    {
      "course_id":"007463",
      "subject":"PHYS",
      "catalog_number":"434",
      "title":"Quantum Physics 3"
    },
    {
      "course_id":"007464",
      "subject":"PHYS",
      "catalog_number":"435",
      "title":"Current Topics in Condensed Matter Physics"
    },
    {
      "course_id":"007465",
      "subject":"PHYS",
      "catalog_number":"437A",
      "title":"Research Project"
    },
    {
      "course_id":"007467",
      "subject":"PHYS",
      "catalog_number":"441A",
      "title":"Electromagnetic Theory"
    },
    {
      "course_id":"007466",
      "subject":"PHYS",
      "catalog_number":"437B",
      "title":"Research Project (continued)"
    },
    {
      "course_id":"013647",
      "subject":"PHYS",
      "catalog_number":"442",
      "title":"Electricity and Magnetism 3"
    },
    {
      "course_id":"007470",
      "subject":"PHYS",
      "catalog_number":"444",
      "title":"Introduction to Particle Physics"
    },
    {
      "course_id":"003369",
      "subject":"PHYS",
      "catalog_number":"454",
      "title":"Quantum Theory 2"
    },
    {
      "course_id":"010364",
      "subject":"PHYS",
      "catalog_number":"460A",
      "title":"Advanced Laboratory 1"
    },
    {
      "course_id":"010365",
      "subject":"PHYS",
      "catalog_number":"460B",
      "title":"Advanced Laboratory 2"
    },
    {
      "course_id":"013648",
      "subject":"PHYS",
      "catalog_number":"461",
      "title":"Nanophysics"
    },
    {
      "course_id":"011497",
      "subject":"PHYS",
      "catalog_number":"467",
      "title":"Introduction to Quantum Information Processing"
    },
    {
      "course_id":"013649",
      "subject":"PHYS",
      "catalog_number":"468",
      "title":"Introduction to the Implementation of Quantum Information Processing"
    },
    {
      "course_id":"007479",
      "subject":"PHYS",
      "catalog_number":"475",
      "title":"Cosmology"
    },
    {
      "course_id":"007485",
      "subject":"PHYS",
      "catalog_number":"480",
      "title":"Radiation Biophysics"
    },
    {
      "course_id":"003371",
      "subject":"PHYS",
      "catalog_number":"476",
      "title":"Introduction to General Relativity"
    },
    {
      "course_id":"010227",
      "subject":"PHYS",
      "catalog_number":"490",
      "title":"Special topics in Physics"
    },
    {
      "course_id":"013275",
      "subject":"PHYS",
      "catalog_number":"601",
      "title":"Perimeter Scholars International Quantum Field Theory 1"
    },
    {
      "course_id":"013276",
      "subject":"PHYS",
      "catalog_number":"602",
      "title":"Perimeter Scholars International Statistical Physics"
    },
    {
      "course_id":"013277",
      "subject":"PHYS",
      "catalog_number":"603",
      "title":"Perimeter Scholars International Quantum Field Theory 2"
    },
    {
      "course_id":"013278",
      "subject":"PHYS",
      "catalog_number":"604",
      "title":"Perimeter Scholars International Relativity"
    },
    {
      "course_id":"013279",
      "subject":"PHYS",
      "catalog_number":"605",
      "title":"Perimeter Scholars International Quantum Theory"
    },
    {
      "course_id":"013280",
      "subject":"PHYS",
      "catalog_number":"606",
      "title":"Perimeter Scholars International Information and Data Analysis"
    },
    {
      "course_id":"013281",
      "subject":"PHYS",
      "catalog_number":"607",
      "title":"Perimeter Scholars International Dynamical Systems"
    },
    {
      "course_id":"013282",
      "subject":"PHYS",
      "catalog_number":"608",
      "title":"Perimeter Scholars International Computation"
    },
    {
      "course_id":"013916",
      "subject":"PHYS",
      "catalog_number":"609",
      "title":"Perimeter Scholars International Conformal Field Theory"
    },
    {
      "course_id":"013917",
      "subject":"PHYS",
      "catalog_number":"610",
      "title":"Perimeter Scholars International Mathematics Physics"
    },
    {
      "course_id":"014237",
      "subject":"PHYS",
      "catalog_number":"611",
      "title":"PSI Condensed Matter Physics"
    },
    {
      "course_id":"013283",
      "subject":"PHYS",
      "catalog_number":"621",
      "title":"Perimeter Scholars International Cosmology"
    },
    {
      "course_id":"013284",
      "subject":"PHYS",
      "catalog_number":"622",
      "title":"Perimeter Scholars International Standard Model"
    },
    {
      "course_id":"013285",
      "subject":"PHYS",
      "catalog_number":"623",
      "title":"Perimeter Scholars International String Theory"
    },
    {
      "course_id":"013286",
      "subject":"PHYS",
      "catalog_number":"624",
      "title":"Perimeter Scholars International Mathematical Physics Topics"
    },
    {
      "course_id":"013918",
      "subject":"PHYS",
      "catalog_number":"625",
      "title":"Perimeter Scholars International Supersymmetry"
    },
    {
      "course_id":"013287",
      "subject":"PHYS",
      "catalog_number":"635",
      "title":"Perimeter Scholars International Quantum Information Review"
    },
    {
      "course_id":"013288",
      "subject":"PHYS",
      "catalog_number":"636",
      "title":"Perimeter Scholars International Gravitational Physics Review"
    },
    {
      "course_id":"013289",
      "subject":"PHYS",
      "catalog_number":"637",
      "title":"Perimeter Scholars International Condensed Matter Theory"
    },
    {
      "course_id":"013290",
      "subject":"PHYS",
      "catalog_number":"638",
      "title":"Perimeter Scholars International Quantum Gravity"
    },
    {
      "course_id":"013291",
      "subject":"PHYS",
      "catalog_number":"639",
      "title":"Perimeter Scholars International Foundations of Quantum Theory"
    },
    {
      "course_id":"013292",
      "subject":"PHYS",
      "catalog_number":"641",
      "title":"Perimeter Scholars International Explorations in Quantum Information"
    },
    {
      "course_id":"013293",
      "subject":"PHYS",
      "catalog_number":"642",
      "title":"Perimeter Scholars International Explorations in Numerical Gravitational Physics"
    },
    {
      "course_id":"013294",
      "subject":"PHYS",
      "catalog_number":"643",
      "title":"Perimeter Scholars International Explorations in Condensed Matter Theory"
    },
    {
      "course_id":"013295",
      "subject":"PHYS",
      "catalog_number":"644",
      "title":"Perimeter Scholars International Explorations in Quantum Gravity"
    },
    {
      "course_id":"013296",
      "subject":"PHYS",
      "catalog_number":"645",
      "title":"Perimeter Scholars International Explorations in Foundations of Quantum Theory"
    },
    {
      "course_id":"013297",
      "subject":"PHYS",
      "catalog_number":"646",
      "title":"Perimeter Scholars International Explorations in Particle Physics"
    },
    {
      "course_id":"013298",
      "subject":"PHYS",
      "catalog_number":"647",
      "title":"Perimeter Scholars International Explorations in String Theory"
    },
    {
      "course_id":"013299",
      "subject":"PHYS",
      "catalog_number":"648",
      "title":"Perimeter Scholars International Explorations in Complex Systems"
    },
    {
      "course_id":"013300",
      "subject":"PHYS",
      "catalog_number":"649",
      "title":"Perimeter Scholars International Explorations in Cosmology"
    },
    {
      "course_id":"002192",
      "subject":"PHYS",
      "catalog_number":"701",
      "title":"Quantum Mechanics 1"
    },
    {
      "course_id":"002193",
      "subject":"PHYS",
      "catalog_number":"702",
      "title":"Quantum Mechanics 2"
    },
    {
      "course_id":"000135",
      "subject":"PHYS",
      "catalog_number":"703",
      "title":"Introduction to Quantum Field Theory"
    },
    {
      "course_id":"002195",
      "subject":"PHYS",
      "catalog_number":"704",
      "title":"Statistical Physics 1"
    },
    {
      "course_id":"002196",
      "subject":"PHYS",
      "catalog_number":"705",
      "title":"Statistical Physics 2"
    },
    {
      "course_id":"002197",
      "subject":"PHYS",
      "catalog_number":"706",
      "title":"Electromagnetic Theory"
    },
    {
      "course_id":"002198",
      "subject":"PHYS",
      "catalog_number":"708",
      "title":"Applications of Group Theory"
    },
    {
      "course_id":"002199",
      "subject":"PHYS",
      "catalog_number":"709",
      "title":"Green's Function Method"
    },
    {
      "course_id":"002200",
      "subject":"PHYS",
      "catalog_number":"710",
      "title":"Atomic Physics"
    },
    {
      "course_id":"002202",
      "subject":"PHYS",
      "catalog_number":"712",
      "title":"Special Topics in Theoretical Physics"
    },
    {
      "course_id":"002203",
      "subject":"PHYS",
      "catalog_number":"713",
      "title":"Molecular Physics"
    },
    {
      "course_id":"013590",
      "subject":"PHYS",
      "catalog_number":"714",
      "title":"Nonlinear Optics"
    },
    {
      "course_id":"009358",
      "subject":"PHYS",
      "catalog_number":"715",
      "title":"Nuclear Physics"
    },
    {
      "course_id":"013591",
      "subject":"PHYS",
      "catalog_number":"716",
      "title":"Special Topics in Subatomic and Nuclear Physcis"
    },
    {
      "course_id":"002204",
      "subject":"PHYS",
      "catalog_number":"717",
      "title":"Intermediate and High Energy Physics"
    },
    {
      "course_id":"013592",
      "subject":"PHYS",
      "catalog_number":"718",
      "title":"Special Topics in Subatomic and Nuclear Physics"
    },
    {
      "course_id":"013597",
      "subject":"PHYS",
      "catalog_number":"730",
      "title":"Liquid State Physics"
    },
    {
      "course_id":"002206",
      "subject":"PHYS",
      "catalog_number":"731",
      "title":"Solid State Physics 1"
    },
    {
      "course_id":"002207",
      "subject":"PHYS",
      "catalog_number":"732",
      "title":"Solid State Physics 2"
    },
    {
      "course_id":"002208",
      "subject":"PHYS",
      "catalog_number":"733",
      "title":"Special Topics in Theoretical Condensed Matter Physics"
    },
    {
      "course_id":"013599",
      "subject":"PHYS",
      "catalog_number":"737",
      "title":"Special Topics in Surface Physics"
    },
    {
      "course_id":"013598",
      "subject":"PHYS",
      "catalog_number":"738",
      "title":"Special Topics in Condensed Matter and Materials Physics"
    },
    {
      "course_id":"002215",
      "subject":"PHYS",
      "catalog_number":"745",
      "title":"Special Topics in Experimental Physics"
    },
    {
      "course_id":"002217",
      "subject":"PHYS",
      "catalog_number":"748",
      "title":"Microprocessors in the Physics Laboratory"
    },
    {
      "course_id":"011592",
      "subject":"PHYS",
      "catalog_number":"747",
      "title":"Optical Electronics"
    },
    {
      "course_id":"002218",
      "subject":"PHYS",
      "catalog_number":"749",
      "title":"Special Topics in Experimental Physics"
    },
    {
      "course_id":"002219",
      "subject":"PHYS",
      "catalog_number":"751",
      "title":"Cellular Biophysics"
    },
    {
      "course_id":"002220",
      "subject":"PHYS",
      "catalog_number":"752",
      "title":"Molecular Biophysics"
    },
    {
      "course_id":"002222",
      "subject":"PHYS",
      "catalog_number":"754",
      "title":"Special Topics in Biophysics"
    },
    {
      "course_id":"002224",
      "subject":"PHYS",
      "catalog_number":"757",
      "title":"Special Topics in Biophysics"
    },
    {
      "course_id":"011589",
      "subject":"PHYS",
      "catalog_number":"767",
      "title":"Quantum Information Processing"
    },
    {
      "course_id":"013593",
      "subject":"PHYS",
      "catalog_number":"768",
      "title":"Special Topics in Quantum Information Processing"
    },
    {
      "course_id":"013594",
      "subject":"PHYS",
      "catalog_number":"769",
      "title":"Special Topics in quantum Information Processing"
    },
    {
      "course_id":"002227",
      "subject":"PHYS",
      "catalog_number":"771",
      "title":"Special Lecture and Reading Course"
    },
    {
      "course_id":"010489",
      "subject":"PHYS",
      "catalog_number":"772",
      "title":"Selected Seminar & Module Course"
    },
    {
      "course_id":"002228",
      "subject":"PHYS",
      "catalog_number":"773",
      "title":"Special Topics in Physics"
    },
    {
      "course_id":"010490",
      "subject":"PHYS",
      "catalog_number":"775",
      "title":"Inter-Institution Exchange"
    },
    {
      "course_id":"013588",
      "subject":"PHYS",
      "catalog_number":"776",
      "title":"Special Topics in Physics"
    },
    {
      "course_id":"013589",
      "subject":"PHYS",
      "catalog_number":"777",
      "title":"Special Topics in Physics"
    },
    {
      "course_id":"002229",
      "subject":"PHYS",
      "catalog_number":"780",
      "title":"Galactic Structure"
    },
    {
      "course_id":"002230",
      "subject":"PHYS",
      "catalog_number":"781",
      "title":"Fundamentals of Astrophysics"
    },
    {
      "course_id":"010439",
      "subject":"PHYS",
      "catalog_number":"784",
      "title":"Advanced techniques in General Relativity and Applications to Black Holes"
    },
    {
      "course_id":"012151",
      "subject":"PHYS",
      "catalog_number":"785",
      "title":"Introduction to Quantum Field Theory for Cosmology"
    },
    {
      "course_id":"011282",
      "subject":"PHYS",
      "catalog_number":"786",
      "title":"Introduction to General Relativity with Applications to Cosmology"
    },
    {
      "course_id":"002232",
      "subject":"PHYS",
      "catalog_number":"787",
      "title":"Cosmology"
    },
    {
      "course_id":"002233",
      "subject":"PHYS",
      "catalog_number":"788",
      "title":"Special Topics in Astrophysics"
    },
    {
      "course_id":"002234",
      "subject":"PHYS",
      "catalog_number":"789",
      "title":"Special Topics in Astrophysics"
    },
    {
      "course_id":"013595",
      "subject":"PHYS",
      "catalog_number":"790",
      "title":"Special Topics in Gravitation and Cosmology"
    },
    {
      "course_id":"010491",
      "subject":"PHYS",
      "catalog_number":"890",
      "title":"Inter-university Graduate Course in Biophysics"
    },
    {
      "course_id":"013596",
      "subject":"PHYS",
      "catalog_number":"791",
      "title":"Special Topics in Gravitation and Cosmology"
    },
    {
      "course_id":"007489",
      "subject":"PLAN",
      "catalog_number":"100",
      "title":"The Evolution of Planning"
    },
    {
      "course_id":"011119",
      "subject":"PLAN",
      "catalog_number":"102",
      "title":"Professional Communication"
    },
    {
      "course_id":"007531",
      "subject":"PLAN",
      "catalog_number":"103",
      "title":"Planning, Administration, and Finance"
    },
    {
      "course_id":"013247",
      "subject":"PLAN",
      "catalog_number":"104",
      "title":"Perspectives on Planning"
    },
    {
      "course_id":"013248",
      "subject":"PLAN",
      "catalog_number":"105",
      "title":"Introduction to Planning Analysis"
    },
    {
      "course_id":"007493",
      "subject":"PLAN",
      "catalog_number":"110",
      "title":"Visual Approaches to Design and Communication"
    },
    {
      "course_id":"013249",
      "subject":"PLAN",
      "catalog_number":"203",
      "title":"Transportation Planning and Analysis"
    },
    {
      "course_id":"007500",
      "subject":"PLAN",
      "catalog_number":"210",
      "title":"Urban Planning Design and the Environment"
    },
    {
      "course_id":"011520",
      "subject":"PLAN",
      "catalog_number":"233",
      "title":"People and Plans"
    },
    {
      "course_id":"011521",
      "subject":"PLAN",
      "catalog_number":"261",
      "title":"Urban and Metropolitan Planning and Development"
    },
    {
      "course_id":"007509",
      "subject":"PLAN",
      "catalog_number":"281",
      "title":"Introduction to Geographic Information Systems (GIS)"
    },
    {
      "course_id":"007539",
      "subject":"PLAN",
      "catalog_number":"300",
      "title":"Planning Theory"
    },
    {
      "course_id":"011522",
      "subject":"PLAN",
      "catalog_number":"309",
      "title":"Site Planning and Design Studio"
    },
    {
      "course_id":"011523",
      "subject":"PLAN",
      "catalog_number":"313",
      "title":"Community Design Studio"
    },
    {
      "course_id":"005909",
      "subject":"PLAN",
      "catalog_number":"320",
      "title":"Economic Analyses for Regional Planning"
    },
    {
      "course_id":"007557",
      "subject":"PLAN",
      "catalog_number":"333",
      "title":"Neighbourhood and Community Planning"
    },
    {
      "course_id":"007558",
      "subject":"PLAN",
      "catalog_number":"340",
      "title":"Ecology-Based Policy-Making"
    },
    {
      "course_id":"007559",
      "subject":"PLAN",
      "catalog_number":"341",
      "title":"Conservation\/Resource Management of the Built Environment"
    },
    {
      "course_id":"013246",
      "subject":"PLAN",
      "catalog_number":"346",
      "title":"Advanced Tools for Planning: Public Participation and Mediation"
    },
    {
      "course_id":"007561",
      "subject":"PLAN",
      "catalog_number":"349",
      "title":"Urban Form and Internal Spatial Structure"
    },
    {
      "course_id":"007562",
      "subject":"PLAN",
      "catalog_number":"350",
      "title":"Research Methods for Planners"
    },
    {
      "course_id":"005905",
      "subject":"PLAN",
      "catalog_number":"351",
      "title":"Multivariate Statistics"
    },
    {
      "course_id":"005908",
      "subject":"PLAN",
      "catalog_number":"353",
      "title":"Spatial Analysis"
    },
    {
      "course_id":"007502",
      "subject":"PLAN",
      "catalog_number":"362",
      "title":"Regional Planning and Economic Development"
    },
    {
      "course_id":"006014",
      "subject":"PLAN",
      "catalog_number":"381",
      "title":"Advanced Geographic Information Systems"
    },
    {
      "course_id":"005943",
      "subject":"PLAN",
      "catalog_number":"387",
      "title":"Spatial Databases"
    },
    {
      "course_id":"007577",
      "subject":"PLAN",
      "catalog_number":"401",
      "title":"Planners and Planning Tribunals"
    },
    {
      "course_id":"007579",
      "subject":"PLAN",
      "catalog_number":"403",
      "title":"Professional Practice, Public and Private Administration"
    },
    {
      "course_id":"013250",
      "subject":"PLAN",
      "catalog_number":"405",
      "title":"Integrated Planning Project"
    },
    {
      "course_id":"011525",
      "subject":"PLAN",
      "catalog_number":"408",
      "title":"Urban Design Seminar"
    },
    {
      "course_id":"011524",
      "subject":"PLAN",
      "catalog_number":"409",
      "title":"Urban Design Studio"
    },
    {
      "course_id":"008208",
      "subject":"PLAN",
      "catalog_number":"414",
      "title":"Heritage Planning Workshop"
    },
    {
      "course_id":"013996",
      "subject":"PLAN",
      "catalog_number":"416",
      "title":"Modelling the City"
    },
    {
      "course_id":"014145",
      "subject":"PLAN",
      "catalog_number":"418",
      "title":"Spatial Demography"
    },
    {
      "course_id":"007588",
      "subject":"PLAN",
      "catalog_number":"431",
      "title":"Issues in Housing"
    },
    {
      "course_id":"006442",
      "subject":"PLAN",
      "catalog_number":"432",
      "title":"Health, Environment, and Planning"
    },
    {
      "course_id":"011765",
      "subject":"PLAN",
      "catalog_number":"433",
      "title":"Social Concepts in Planning"
    },
    {
      "course_id":"007592",
      "subject":"PLAN",
      "catalog_number":"440",
      "title":"Urban Services Planning"
    },
    {
      "course_id":"006011",
      "subject":"PLAN",
      "catalog_number":"450",
      "title":"Changing Form and Structure of Metropolitan Canada"
    },
    {
      "course_id":"014146",
      "subject":"PLAN",
      "catalog_number":"451",
      "title":"Tools for Sustainable Communities"
    },
    {
      "course_id":"011526",
      "subject":"PLAN",
      "catalog_number":"452",
      "title":"Policy Analysis and Program Evaluation for Planners"
    },
    {
      "course_id":"011527",
      "subject":"PLAN",
      "catalog_number":"453",
      "title":"Urban Stormwater Management"
    },
    {
      "course_id":"007599",
      "subject":"PLAN",
      "catalog_number":"471",
      "title":"Planning Law"
    },
    {
      "course_id":"010228",
      "subject":"PLAN",
      "catalog_number":"474",
      "title":"Special Topics in Planning"
    },
    {
      "course_id":"012197",
      "subject":"PLAN",
      "catalog_number":"477",
      "title":"Freight Planning and Policy"
    },
    {
      "course_id":"004249",
      "subject":"PLAN",
      "catalog_number":"478",
      "title":"Transit Planning and Operations"
    },
    {
      "course_id":"009499",
      "subject":"PLAN",
      "catalog_number":"480",
      "title":"Theory and Practice of Planning in the U.K."
    },
    {
      "course_id":"009505",
      "subject":"PLAN",
      "catalog_number":"481",
      "title":"Geographic Information Systems Project"
    },
    {
      "course_id":"007667",
      "subject":"PMATH",
      "catalog_number":"345",
      "title":"Polynomials, Rings and Finite Fields"
    },
    {
      "course_id":"007636",
      "subject":"PLAN",
      "catalog_number":"483",
      "title":"Land Development Planning"
    },
    {
      "course_id":"007637",
      "subject":"PLAN",
      "catalog_number":"484",
      "title":"Physical Infrastructure Planning"
    },
    {
      "course_id":"007638",
      "subject":"PLAN",
      "catalog_number":"485",
      "title":"Projects, Problems, and Readings in Planning"
    },
    {
      "course_id":"009498",
      "subject":"PLAN",
      "catalog_number":"487",
      "title":"Management Issues in Geographic Information Systems"
    },
    {
      "course_id":"007655",
      "subject":"PLAN",
      "catalog_number":"490",
      "title":"Senior Honours Essay"
    },
    {
      "course_id":"002238",
      "subject":"PLAN",
      "catalog_number":"601",
      "title":"Planning Tribunals"
    },
    {
      "course_id":"011470",
      "subject":"PLAN",
      "catalog_number":"603",
      "title":"Real Estate Finance and Investment"
    },
    {
      "course_id":"011469",
      "subject":"PLAN",
      "catalog_number":"602",
      "title":"Land Development Planning"
    },
    {
      "course_id":"001839",
      "subject":"PLAN",
      "catalog_number":"611",
      "title":"Industrial Location Theory and Concepts"
    },
    {
      "course_id":"001841",
      "subject":"PLAN",
      "catalog_number":"613",
      "title":"Regional Development Principles and Practice"
    },
    {
      "course_id":"002242",
      "subject":"PLAN",
      "catalog_number":"614",
      "title":"Issues in Housing"
    },
    {
      "course_id":"011489",
      "subject":"PLAN",
      "catalog_number":"649",
      "title":"Graduate Urban Design Planning Studio"
    },
    {
      "course_id":"001842",
      "subject":"PLAN",
      "catalog_number":"615",
      "title":"Community Economic Development"
    },
    {
      "course_id":"001360",
      "subject":"PLAN",
      "catalog_number":"616",
      "title":"Multivariate Statistics"
    },
    {
      "course_id":"002245",
      "subject":"PLAN",
      "catalog_number":"619",
      "title":"Regional Planning Economic and Investment Analysis"
    },
    {
      "course_id":"010621",
      "subject":"PLAN",
      "catalog_number":"621",
      "title":"Metropolitan Form and Structure in Canada"
    },
    {
      "course_id":"011472",
      "subject":"PLAN",
      "catalog_number":"622",
      "title":"Contemporary Urban Planning and Governance"
    },
    {
      "course_id":"002247",
      "subject":"PLAN",
      "catalog_number":"623",
      "title":"Social Concepts in Planning"
    },
    {
      "course_id":"002249",
      "subject":"PLAN",
      "catalog_number":"625",
      "title":"Methods of Social Investigation for Planners"
    },
    {
      "course_id":"002251",
      "subject":"PLAN",
      "catalog_number":"630",
      "title":"Planning Law"
    },
    {
      "course_id":"011476",
      "subject":"PLAN",
      "catalog_number":"639",
      "title":"Health, Environment and Planning"
    },
    {
      "course_id":"011485",
      "subject":"PLAN",
      "catalog_number":"641",
      "title":"Heritage Planning Workshop"
    },
    {
      "course_id":"011486",
      "subject":"PLAN",
      "catalog_number":"646",
      "title":"Site Planning and Design Studio"
    },
    {
      "course_id":"011487",
      "subject":"PLAN",
      "catalog_number":"647",
      "title":"Community Design Studio"
    },
    {
      "course_id":"011488",
      "subject":"PLAN",
      "catalog_number":"648",
      "title":"Urban Design Philosophy and Methodology"
    },
    {
      "course_id":"012036",
      "subject":"PLAN",
      "catalog_number":"652",
      "title":"Environmental Policy Analysis"
    },
    {
      "course_id":"011818",
      "subject":"PLAN",
      "catalog_number":"654",
      "title":"Spatial Information Technology, Globalization and International Development"
    },
    {
      "course_id":"011491",
      "subject":"PLAN",
      "catalog_number":"657",
      "title":"GIS and Spatial Decision Support for Planning  and Resource Management"
    },
    {
      "course_id":"001210",
      "subject":"PLAN",
      "catalog_number":"660",
      "title":"Perspectives in Resource and Environmental Management"
    },
    {
      "course_id":"002264",
      "subject":"PLAN",
      "catalog_number":"661A",
      "title":"Applied Studies in Hydrology and the Environment 1"
    },
    {
      "course_id":"001389",
      "subject":"PLAN",
      "catalog_number":"661B",
      "title":"Applied Studies in Hydrology and the Environment 2"
    },
    {
      "course_id":"002269",
      "subject":"PLAN",
      "catalog_number":"665",
      "title":"Environmental Planning Theory and Practice"
    },
    {
      "course_id":"002270",
      "subject":"PLAN",
      "catalog_number":"666",
      "title":"Ecosystem Approach to Park Planning"
    },
    {
      "course_id":"011474",
      "subject":"PLAN",
      "catalog_number":"669",
      "title":"Landscape Restoration"
    },
    {
      "course_id":"010620",
      "subject":"PLAN",
      "catalog_number":"674",
      "title":"Special Topics in Planning"
    },
    {
      "course_id":"009445",
      "subject":"PLAN",
      "catalog_number":"675",
      "title":"Special Readings on Selected Planning Topics"
    },
    {
      "course_id":"012168",
      "subject":"PLAN",
      "catalog_number":"677",
      "title":"Freight Planning and Policy"
    },
    {
      "course_id":"012341",
      "subject":"PLAN",
      "catalog_number":"678",
      "title":"Advances in Public Transportation Planning, Operations & Control"
    },
    {
      "course_id":"012546",
      "subject":"PLAN",
      "catalog_number":"684",
      "title":"Physical Infrastructure and Planning"
    },
    {
      "course_id":"002307",
      "subject":"PLAN",
      "catalog_number":"700",
      "title":"Planning Paradigms and Theory"
    },
    {
      "course_id":"012547",
      "subject":"PLAN",
      "catalog_number":"701",
      "title":"Land Use Planning Fundamentals"
    },
    {
      "course_id":"012762",
      "subject":"PLAN",
      "catalog_number":"702",
      "title":"Critical Assessment of Theories, Methods and Practices of Planning"
    },
    {
      "course_id":"011475",
      "subject":"PLAN",
      "catalog_number":"703",
      "title":"Planning Professional Practice"
    },
    {
      "course_id":"014405",
      "subject":"PLAN",
      "catalog_number":"704",
      "title":"Methods of Planning Analysis"
    },
    {
      "course_id":"002308",
      "subject":"PLAN",
      "catalog_number":"710",
      "title":"Research Design"
    },
    {
      "course_id":"014406",
      "subject":"PLAN",
      "catalog_number":"720",
      "title":"Introductory Planning Project Studio"
    },
    {
      "course_id":"014408",
      "subject":"PLAN",
      "catalog_number":"721",
      "title":"Advanced Planning Project Studio"
    },
    {
      "course_id":"002317",
      "subject":"PLAN",
      "catalog_number":"801",
      "title":"PhD Research Forum 1"
    },
    {
      "course_id":"002320",
      "subject":"PLAN",
      "catalog_number":"802",
      "title":"PhD Research Forum 2"
    },
    {
      "course_id":"007659",
      "subject":"PMATH",
      "catalog_number":"330",
      "title":"Introduction to Mathematical Logic"
    },
    {
      "course_id":"003323",
      "subject":"PMATH",
      "catalog_number":"331",
      "title":"Applied Real Analysis"
    },
    {
      "course_id":"003324",
      "subject":"PMATH",
      "catalog_number":"332",
      "title":"Applied Complex Analysis"
    },
    {
      "course_id":"007662",
      "subject":"PMATH",
      "catalog_number":"334",
      "title":"Introduction to Rings and Fields with Applications"
    },
    {
      "course_id":"007663",
      "subject":"PMATH",
      "catalog_number":"336",
      "title":"Introduction to Group Theory with Applications"
    },
    {
      "course_id":"007664",
      "subject":"PMATH",
      "catalog_number":"340",
      "title":"Elementary Number Theory"
    },
    {
      "course_id":"014182",
      "subject":"PMATH",
      "catalog_number":"347",
      "title":"Groups and Rings"
    },
    {
      "course_id":"014183",
      "subject":"PMATH",
      "catalog_number":"348",
      "title":"Fields and Galois Theory"
    },
    {
      "course_id":"007669",
      "subject":"PMATH",
      "catalog_number":"351",
      "title":"Real Analysis"
    },
    {
      "course_id":"007672",
      "subject":"PMATH",
      "catalog_number":"352",
      "title":"Complex Analysis"
    },
    {
      "course_id":"007675",
      "subject":"PMATH",
      "catalog_number":"360",
      "title":"Geometry"
    },
    {
      "course_id":"003325",
      "subject":"PMATH",
      "catalog_number":"365",
      "title":"Elementary Differential Geometry"
    },
    {
      "course_id":"007677",
      "subject":"PMATH",
      "catalog_number":"367",
      "title":"Set Theory & General Topology"
    },
    {
      "course_id":"009496",
      "subject":"PMATH",
      "catalog_number":"370",
      "title":"Chaos and Fractals"
    },
    {
      "course_id":"007680",
      "subject":"PMATH",
      "catalog_number":"399",
      "title":"Readings in Pure Mathematics"
    },
    {
      "course_id":"007687",
      "subject":"PMATH",
      "catalog_number":"432",
      "title":"First Order Logic and Computability"
    },
    {
      "course_id":"012623",
      "subject":"PMATH",
      "catalog_number":"433",
      "title":"Model Theory and Set Theory"
    },
    {
      "course_id":"007690",
      "subject":"PMATH",
      "catalog_number":"440",
      "title":"Analytic Number Theory"
    },
    {
      "course_id":"007691",
      "subject":"PMATH",
      "catalog_number":"441",
      "title":"Algebraic Number Theory"
    },
    {
      "course_id":"014184",
      "subject":"PMATH",
      "catalog_number":"445",
      "title":"Representations of Finite Groups"
    },
    {
      "course_id":"014185",
      "subject":"PMATH",
      "catalog_number":"446",
      "title":"Introduction to Commutative Algebra"
    },
    {
      "course_id":"007674",
      "subject":"PMATH",
      "catalog_number":"450",
      "title":"Lebesgue Integration and Fourier Analysis"
    },
    {
      "course_id":"003348",
      "subject":"PMATH",
      "catalog_number":"451",
      "title":"Measure and Integration"
    },
    {
      "course_id":"003349",
      "subject":"PMATH",
      "catalog_number":"453",
      "title":"Functional Analysis"
    },
    {
      "course_id":"010733",
      "subject":"PMATH",
      "catalog_number":"464",
      "title":"Introduction to Algebraic Geometry"
    },
    {
      "course_id":"007733",
      "subject":"PSCI",
      "catalog_number":"214",
      "title":"Quantitative Analysis"
    },
    {
      "course_id":"003350",
      "subject":"PMATH",
      "catalog_number":"465",
      "title":"Differential Geometry"
    },
    {
      "course_id":"007704",
      "subject":"PMATH",
      "catalog_number":"467",
      "title":"Topology"
    },
    {
      "course_id":"007706",
      "subject":"PMATH",
      "catalog_number":"499",
      "title":"Readings in Pure Mathematics"
    },
    {
      "course_id":"002339",
      "subject":"PMATH",
      "catalog_number":"632",
      "title":"First Order Logic and Computability"
    },
    {
      "course_id":"002341",
      "subject":"PMATH",
      "catalog_number":"641",
      "title":"Algebraic Number Theory"
    },
    {
      "course_id":"002342",
      "subject":"PMATH",
      "catalog_number":"642",
      "title":"Fields and Galois Theory"
    },
    {
      "course_id":"002343",
      "subject":"PMATH",
      "catalog_number":"644",
      "title":"Rings, Modules and Representations"
    },
    {
      "course_id":"014670",
      "subject":"PMATH",
      "catalog_number":"646",
      "title":"Introduction to Commutative Algebra"
    },
    {
      "course_id":"013667",
      "subject":"PMATH",
      "catalog_number":"650",
      "title":"Lebesgue Integration and Fourier Analysis"
    },
    {
      "course_id":"002346",
      "subject":"PMATH",
      "catalog_number":"651",
      "title":"Measure and Integration"
    },
    {
      "course_id":"002347",
      "subject":"PMATH",
      "catalog_number":"652",
      "title":"Topics in Complex Analysis"
    },
    {
      "course_id":"002349",
      "subject":"PMATH",
      "catalog_number":"665",
      "title":"Differential Geometry"
    },
    {
      "course_id":"002350",
      "subject":"PMATH",
      "catalog_number":"667",
      "title":"Algebraic Topology"
    },
    {
      "course_id":"002351",
      "subject":"PMATH",
      "catalog_number":"690",
      "title":"Literature and Research Studies"
    },
    {
      "course_id":"011873",
      "subject":"PMATH",
      "catalog_number":"701",
      "title":"Graduate Algebra"
    },
    {
      "course_id":"011874",
      "subject":"PMATH",
      "catalog_number":"702",
      "title":"Graduate Analysis"
    },
    {
      "course_id":"013668",
      "subject":"PMATH",
      "catalog_number":"733",
      "title":"Model Theory and Set Theory"
    },
    {
      "course_id":"013669",
      "subject":"PMATH",
      "catalog_number":"740",
      "title":"Analytic Number Theory"
    },
    {
      "course_id":"014343",
      "subject":"PMATH",
      "catalog_number":"745",
      "title":"Representations of Finite Groups"
    },
    {
      "course_id":"013670",
      "subject":"PMATH",
      "catalog_number":"753",
      "title":"Functional Analysis"
    },
    {
      "course_id":"002391",
      "subject":"PMATH",
      "catalog_number":"763",
      "title":"Introduction to Lie Groups and Lie Algebras"
    },
    {
      "course_id":"002392",
      "subject":"PMATH",
      "catalog_number":"764",
      "title":"Introduction to Algebraic Geometry"
    },
    {
      "course_id":"010486",
      "subject":"PMATH",
      "catalog_number":"800",
      "title":"Topics in Real and Complex Analysis"
    },
    {
      "course_id":"011875",
      "subject":"PMATH",
      "catalog_number":"810",
      "title":"Banach Algebras and Operator Theory"
    },
    {
      "course_id":"010487",
      "subject":"PMATH",
      "catalog_number":"811",
      "title":"Topics in Functional Analysis"
    },
    {
      "course_id":"002408",
      "subject":"PMATH",
      "catalog_number":"822",
      "title":"Topics in Operator Theory"
    },
    {
      "course_id":"002412",
      "subject":"PMATH",
      "catalog_number":"833",
      "title":"Topics in Harmonic Analysis"
    },
    {
      "course_id":"002414",
      "subject":"PMATH",
      "catalog_number":"844",
      "title":"Topics in Functional Equations"
    },
    {
      "course_id":"010483",
      "subject":"PMATH",
      "catalog_number":"900",
      "title":"Topics in Algebra"
    },
    {
      "course_id":"011832",
      "subject":"PSYCH",
      "catalog_number":"608A",
      "title":"Child Psychopathology & Psychotherapy"
    },
    {
      "course_id":"010484",
      "subject":"PMATH",
      "catalog_number":"911",
      "title":"Topics in Mathematical Logic"
    },
    {
      "course_id":"002366",
      "subject":"PMATH",
      "catalog_number":"922",
      "title":"Topics in Universal Algebra"
    },
    {
      "course_id":"002377",
      "subject":"PMATH",
      "catalog_number":"933",
      "title":"Topics in Group Theory"
    },
    {
      "course_id":"002383",
      "subject":"PMATH",
      "catalog_number":"944",
      "title":"Topics in Number Theory"
    },
    {
      "course_id":"002388",
      "subject":"PMATH",
      "catalog_number":"955",
      "title":"Topics in Geometry"
    },
    {
      "course_id":"010485",
      "subject":"PMATH",
      "catalog_number":"966",
      "title":"Topics in Topology"
    },
    {
      "course_id":"007712",
      "subject":"POLSH",
      "catalog_number":"101",
      "title":"Elementary Polish I"
    },
    {
      "course_id":"007713",
      "subject":"POLSH",
      "catalog_number":"102",
      "title":"Elementary Polish II"
    },
    {
      "course_id":"007714",
      "subject":"POLSH",
      "catalog_number":"201",
      "title":"Intermediate Polish I"
    },
    {
      "course_id":"007715",
      "subject":"POLSH",
      "catalog_number":"202",
      "title":"Intermediate Polish II"
    },
    {
      "course_id":"010099",
      "subject":"PORT",
      "catalog_number":"101",
      "title":"Introduction to Portuguese 1"
    },
    {
      "course_id":"010097",
      "subject":"PORT",
      "catalog_number":"102",
      "title":"Introduction to Portuguese 2"
    },
    {
      "course_id":"013702",
      "subject":"PS",
      "catalog_number":"611",
      "title":"Government, Politics and the Public Service"
    },
    {
      "course_id":"013703",
      "subject":"PS",
      "catalog_number":"612",
      "title":"Government Finance I:  Accounting and Accountability"
    },
    {
      "course_id":"013704",
      "subject":"PS",
      "catalog_number":"613",
      "title":"The Politics of Difference in Canada:  Challenges and Policy Responses"
    },
    {
      "course_id":"013705",
      "subject":"PS",
      "catalog_number":"614",
      "title":"Communicating with Diverse Audiences"
    },
    {
      "course_id":"002502",
      "subject":"PSYCH",
      "catalog_number":"607S",
      "title":"Efficacy and Program Evaluation"
    },
    {
      "course_id":"013706",
      "subject":"PS",
      "catalog_number":"615",
      "title":"Effective Problem-Solving and Decision-Making"
    },
    {
      "course_id":"013707",
      "subject":"PS",
      "catalog_number":"616",
      "title":"Spoken French in Context"
    },
    {
      "course_id":"013708",
      "subject":"PS",
      "catalog_number":"617",
      "title":"Values and Ethics in Government"
    },
    {
      "course_id":"013709",
      "subject":"PS",
      "catalog_number":"618",
      "title":"Public Policy Development"
    },
    {
      "course_id":"013710",
      "subject":"PS",
      "catalog_number":"619",
      "title":"Government Finance II: Practices and Procedures"
    },
    {
      "course_id":"013711",
      "subject":"PS",
      "catalog_number":"620",
      "title":"Effective Leadership and Management"
    },
    {
      "course_id":"013712",
      "subject":"PS",
      "catalog_number":"621",
      "title":"Project Management in Government"
    },
    {
      "course_id":"012551",
      "subject":"PSCI",
      "catalog_number":"601",
      "title":"Research Applications in Political Science"
    },
    {
      "course_id":"013713",
      "subject":"PS",
      "catalog_number":"622",
      "title":"Major Team Project"
    },
    {
      "course_id":"014427",
      "subject":"PS",
      "catalog_number":"623",
      "title":"Government, Business and Civil Society"
    },
    {
      "course_id":"014428",
      "subject":"PS",
      "catalog_number":"624",
      "title":"Research Methods and Data Analysis"
    },
    {
      "course_id":"014189",
      "subject":"PS",
      "catalog_number":"699",
      "title":"Special Topics"
    },
    {
      "course_id":"014381",
      "subject":"PSCI",
      "catalog_number":"100",
      "title":"Introduction to Government"
    },
    {
      "course_id":"007719",
      "subject":"PSCI",
      "catalog_number":"101",
      "title":"Introduction to Political Ideas"
    },
    {
      "course_id":"011331",
      "subject":"PSCI",
      "catalog_number":"110",
      "title":"Introduction to Politics in the Contemporary World"
    },
    {
      "course_id":"014382",
      "subject":"PSCI",
      "catalog_number":"150",
      "title":"Introduction to Global Politics"
    },
    {
      "course_id":"014383",
      "subject":"PSCI",
      "catalog_number":"190",
      "title":"Special Studies"
    },
    {
      "course_id":"013717",
      "subject":"PSCI",
      "catalog_number":"200",
      "title":"Political Science Nuts and Bolts"
    },
    {
      "course_id":"007738",
      "subject":"PSCI",
      "catalog_number":"225",
      "title":"Classics in Political Thought"
    },
    {
      "course_id":"007740",
      "subject":"PSCI",
      "catalog_number":"226",
      "title":"Modern Political Thought"
    },
    {
      "course_id":"007744",
      "subject":"PSCI",
      "catalog_number":"231",
      "title":"Government and Business"
    },
    {
      "course_id":"014267",
      "subject":"PSCI",
      "catalog_number":"244",
      "title":"Irrational and Rational Choices in Politics"
    },
    {
      "course_id":"011344",
      "subject":"PSCI",
      "catalog_number":"250",
      "title":"The Comparative Politics of State and Nation"
    },
    {
      "course_id":"007724",
      "subject":"PSCI",
      "catalog_number":"252",
      "title":"Global South"
    },
    {
      "course_id":"014797",
      "subject":"PSCI",
      "catalog_number":"299",
      "title":"Political Science Beyond the Classroom"
    },
    {
      "course_id":"014384",
      "subject":"PSCI",
      "catalog_number":"254",
      "title":"The Political Documentary"
    },
    {
      "course_id":"007747",
      "subject":"PSCI",
      "catalog_number":"255",
      "title":"Comparative Political Economy of Advanced Industrial Democracies"
    },
    {
      "course_id":"007759",
      "subject":"PSCI",
      "catalog_number":"291",
      "title":"The Canadian Legal Process"
    },
    {
      "course_id":"012170",
      "subject":"PSCI",
      "catalog_number":"257",
      "title":"Introduction to the Modern Middle East"
    },
    {
      "course_id":"012187",
      "subject":"PSCI",
      "catalog_number":"259",
      "title":"Government and Politics of Asia"
    },
    {
      "course_id":"007749",
      "subject":"PSCI",
      "catalog_number":"260",
      "title":"Canadian Government & Politics"
    },
    {
      "course_id":"007752",
      "subject":"PSCI",
      "catalog_number":"264",
      "title":"American Government and Politics"
    },
    {
      "course_id":"007756",
      "subject":"PSCI",
      "catalog_number":"281",
      "title":"World Politics"
    },
    {
      "course_id":"007757",
      "subject":"PSCI",
      "catalog_number":"282",
      "title":"Foreign Policy"
    },
    {
      "course_id":"012302",
      "subject":"PSCI",
      "catalog_number":"283",
      "title":"International Political Economy"
    },
    {
      "course_id":"014224",
      "subject":"PSCI",
      "catalog_number":"300",
      "title":"Foundations of Political Economy"
    },
    {
      "course_id":"007733",
      "subject":"PSCI",
      "catalog_number":"314",
      "title":"Quantitative Analysis"
    },
    {
      "course_id":"007764",
      "subject":"PSCI",
      "catalog_number":"315",
      "title":"Research Design in Political Science"
    },
    {
      "course_id":"007768",
      "subject":"PSCI",
      "catalog_number":"321",
      "title":"Marxist Theory"
    },
    {
      "course_id":"007771",
      "subject":"PSCI",
      "catalog_number":"324",
      "title":"Issues in Contemporary Political Theory"
    },
    {
      "course_id":"007774",
      "subject":"PSCI",
      "catalog_number":"331",
      "title":"Public Administration"
    },
    {
      "course_id":"011638",
      "subject":"PSCI",
      "catalog_number":"334",
      "title":"Public Policy"
    },
    {
      "course_id":"007789",
      "subject":"PSCI",
      "catalog_number":"350",
      "title":"Political Economy of Development"
    },
    {
      "course_id":"007791",
      "subject":"PSCI",
      "catalog_number":"351",
      "title":"Power Sharing in Divided Societies"
    },
    {
      "course_id":"014386",
      "subject":"PSCI",
      "catalog_number":"352",
      "title":"Culture and Political Violence"
    },
    {
      "course_id":"011637",
      "subject":"PSCI",
      "catalog_number":"353",
      "title":"Politics in Russia"
    },
    {
      "course_id":"009514",
      "subject":"PSCI",
      "catalog_number":"355",
      "title":"Russia and its Neighbours"
    },
    {
      "course_id":"013474",
      "subject":"PSCI",
      "catalog_number":"356",
      "title":"Business and Politics of Japan"
    },
    {
      "course_id":"012183",
      "subject":"PSCI",
      "catalog_number":"358",
      "title":"Political Change in Greater China"
    },
    {
      "course_id":"011768",
      "subject":"PSCI",
      "catalog_number":"360",
      "title":"Topics in Canadian Government and Politics"
    },
    {
      "course_id":"014387",
      "subject":"PSCI",
      "catalog_number":"362",
      "title":"Cultural Politics and Indigenous Practices"
    },
    {
      "course_id":"007797",
      "subject":"PSCI",
      "catalog_number":"363",
      "title":"Canadian Constitutional Law"
    },
    {
      "course_id":"012063",
      "subject":"PSCI",
      "catalog_number":"367",
      "title":"Topics in American Government and Politics"
    },
    {
      "course_id":"012449",
      "subject":"PSCI",
      "catalog_number":"368",
      "title":"Russian Politics through Literature"
    },
    {
      "course_id":"012944",
      "subject":"PSCI",
      "catalog_number":"369",
      "title":"The Politics of Decolonization"
    },
    {
      "course_id":"011639",
      "subject":"PSCI",
      "catalog_number":"370",
      "title":"Women and Politics"
    },
    {
      "course_id":"011118",
      "subject":"PSCI",
      "catalog_number":"373",
      "title":"Political Parties, Elections, and Political Marketing"
    },
    {
      "course_id":"007804",
      "subject":"PSCI",
      "catalog_number":"381",
      "title":"Foreign Policies of South Asian States"
    },
    {
      "course_id":"014268",
      "subject":"PSCI",
      "catalog_number":"375",
      "title":"Transnational Migration"
    },
    {
      "course_id":"007805",
      "subject":"PSCI",
      "catalog_number":"382",
      "title":"Politics of Canadian Foreign Policy"
    },
    {
      "course_id":"012945",
      "subject":"PSCI",
      "catalog_number":"383",
      "title":"Transatlantic Relations"
    },
    {
      "course_id":"010348",
      "subject":"PSCI",
      "catalog_number":"387",
      "title":"Globalization"
    },
    {
      "course_id":"012593",
      "subject":"PSCI",
      "catalog_number":"389",
      "title":"Global Governance"
    },
    {
      "course_id":"007806",
      "subject":"PSCI",
      "catalog_number":"390",
      "title":"Special Studies"
    },
    {
      "course_id":"007807",
      "subject":"PSCI",
      "catalog_number":"391",
      "title":"Special Studies"
    },
    {
      "course_id":"013475",
      "subject":"PSCI",
      "catalog_number":"401",
      "title":"Projects in Political Science"
    },
    {
      "course_id":"014225",
      "subject":"PSCI",
      "catalog_number":"402",
      "title":"Politics of International Trade"
    },
    {
      "course_id":"014226",
      "subject":"PSCI",
      "catalog_number":"403",
      "title":"Topics in Politics and Business"
    },
    {
      "course_id":"014527",
      "subject":"PSCI",
      "catalog_number":"404",
      "title":"Globalization, International Business, and Development"
    },
    {
      "course_id":"014528",
      "subject":"PSCI",
      "catalog_number":"405",
      "title":"Chinese Political Economy"
    },
    {
      "course_id":"007813",
      "subject":"PSCI",
      "catalog_number":"421",
      "title":"Justice and Gender"
    },
    {
      "course_id":"007815",
      "subject":"PSCI",
      "catalog_number":"423",
      "title":"Democratic Theory and Practice"
    },
    {
      "course_id":"007816",
      "subject":"PSCI",
      "catalog_number":"426",
      "title":"Selected Subjects in Political Philosophy"
    },
    {
      "course_id":"007818",
      "subject":"PSCI",
      "catalog_number":"428",
      "title":"The State and Economic Life"
    },
    {
      "course_id":"011709",
      "subject":"PSCI",
      "catalog_number":"429",
      "title":"Genetics and Justice"
    },
    {
      "course_id":"007819",
      "subject":"PSCI",
      "catalog_number":"431",
      "title":"Canadian Public Policy"
    },
    {
      "course_id":"005377",
      "subject":"PSCI",
      "catalog_number":"432",
      "title":"Global Environmental Governance"
    },
    {
      "course_id":"007776",
      "subject":"PSCI",
      "catalog_number":"433",
      "title":"Topics in Canadian Public Administration"
    },
    {
      "course_id":"007822",
      "subject":"PSCI",
      "catalog_number":"434",
      "title":"Comparative Public Administration"
    },
    {
      "course_id":"014529",
      "subject":"PSCI",
      "catalog_number":"435",
      "title":"Comparative Public Policy"
    },
    {
      "course_id":"012359",
      "subject":"PSCI",
      "catalog_number":"439",
      "title":"Global Social Policy"
    },
    {
      "course_id":"007827",
      "subject":"PSCI",
      "catalog_number":"451",
      "title":"Comparative Political Systems: Eastern Europe"
    },
    {
      "course_id":"012947",
      "subject":"PSCI",
      "catalog_number":"452",
      "title":"Comparative Political Parties"
    },
    {
      "course_id":"007830",
      "subject":"PSCI",
      "catalog_number":"454",
      "title":"Topics in Politics in the Global South"
    },
    {
      "course_id":"012949",
      "subject":"PSCI",
      "catalog_number":"455",
      "title":"Comparative Political Economy"
    },
    {
      "course_id":"007831",
      "subject":"PSCI",
      "catalog_number":"456",
      "title":"Ethnic Conflict and Conflict Resolution"
    },
    {
      "course_id":"007832",
      "subject":"PSCI",
      "catalog_number":"458",
      "title":"Cultural Explanations of Politics"
    },
    {
      "course_id":"014388",
      "subject":"PSCI",
      "catalog_number":"460",
      "title":"The Cultural Politics of Israel\/Palestine"
    },
    {
      "course_id":"007834",
      "subject":"PSCI",
      "catalog_number":"461",
      "title":"Canadian National Politics"
    },
    {
      "course_id":"013476",
      "subject":"PSCI",
      "catalog_number":"462",
      "title":"Government and Politics of Indigenous Peoples"
    },
    {
      "course_id":"014530",
      "subject":"PSCI",
      "catalog_number":"463",
      "title":"Rights and Public Policy"
    },
    {
      "course_id":"007837",
      "subject":"PSCI",
      "catalog_number":"472",
      "title":"Women and Public Policy"
    },
    {
      "course_id":"014531",
      "subject":"PSCI",
      "catalog_number":"479",
      "title":"International Political Economy of Asia"
    },
    {
      "course_id":"014227",
      "subject":"PSCI",
      "catalog_number":"480",
      "title":"China and Global Governance"
    },
    {
      "course_id":"007841",
      "subject":"PSCI",
      "catalog_number":"481",
      "title":"Interstate War"
    },
    {
      "course_id":"012950",
      "subject":"PSCI",
      "catalog_number":"482",
      "title":"Critical Security Studies"
    },
    {
      "course_id":"007844",
      "subject":"PSCI",
      "catalog_number":"485",
      "title":"Selected Topics in International Political Economy"
    },
    {
      "course_id":"010240",
      "subject":"PSCI",
      "catalog_number":"486",
      "title":"Special Topics in International Diplomacy"
    },
    {
      "course_id":"012951",
      "subject":"PSCI",
      "catalog_number":"487",
      "title":"International Relations Theory"
    },
    {
      "course_id":"013955",
      "subject":"PSCI",
      "catalog_number":"488",
      "title":"Global Food and Agricultural Politics"
    },
    {
      "course_id":"007847",
      "subject":"PSCI",
      "catalog_number":"490",
      "title":"Special Subjects"
    },
    {
      "course_id":"007848",
      "subject":"PSCI",
      "catalog_number":"491",
      "title":"Special Subjects"
    },
    {
      "course_id":"007849",
      "subject":"PSCI",
      "catalog_number":"492",
      "title":"Special Subjects"
    },
    {
      "course_id":"007859",
      "subject":"PSCI",
      "catalog_number":"499A",
      "title":"Special Honours Essay"
    },
    {
      "course_id":"007860",
      "subject":"PSCI",
      "catalog_number":"499B",
      "title":"Special Honours Essay"
    },
    {
      "course_id":"011481",
      "subject":"PSCI",
      "catalog_number":"600",
      "title":"Theories and Methods of Political Analysis"
    },
    {
      "course_id":"001205",
      "subject":"PSCI",
      "catalog_number":"604",
      "title":"Advanced Topics in Global Environmental Governance"
    },
    {
      "course_id":"012738",
      "subject":"PSCI",
      "catalog_number":"606",
      "title":"Governing Global Food and Agriculture Systems"
    },
    {
      "course_id":"002419",
      "subject":"PSCI",
      "catalog_number":"612",
      "title":"Theories of Globalization"
    },
    {
      "course_id":"010616",
      "subject":"PSCI",
      "catalog_number":"613",
      "title":"Directed Readings in Political Methodology"
    },
    {
      "course_id":"013687",
      "subject":"PSCI",
      "catalog_number":"614",
      "title":"Global Business and Development"
    },
    {
      "course_id":"014925",
      "subject":"PSCI",
      "catalog_number":"666",
      "title":"Rights and Public Policy"
    },
    {
      "course_id":"013688",
      "subject":"PSCI",
      "catalog_number":"615",
      "title":"Global Poverty"
    },
    {
      "course_id":"013689",
      "subject":"PSCI",
      "catalog_number":"616",
      "title":"Global Health Governance"
    },
    {
      "course_id":"013684",
      "subject":"PSCI",
      "catalog_number":"617",
      "title":"Unconventional Diplomacy"
    },
    {
      "course_id":"013685",
      "subject":"PSCI",
      "catalog_number":"618",
      "title":"Non-State Actors in Global Governance"
    },
    {
      "course_id":"014301",
      "subject":"PSCI",
      "catalog_number":"619",
      "title":"China and Global Governance"
    },
    {
      "course_id":"014363",
      "subject":"PSCI",
      "catalog_number":"620",
      "title":"Gender and Global Politics"
    },
    {
      "course_id":"002420",
      "subject":"PSCI",
      "catalog_number":"621",
      "title":"Political Theory 1"
    },
    {
      "course_id":"002421",
      "subject":"PSCI",
      "catalog_number":"622",
      "title":"Political Theory 2"
    },
    {
      "course_id":"002422",
      "subject":"PSCI",
      "catalog_number":"623",
      "title":"Democratic Theory and Practice"
    },
    {
      "course_id":"002423",
      "subject":"PSCI",
      "catalog_number":"624",
      "title":"Justice and Gender"
    },
    {
      "course_id":"002424",
      "subject":"PSCI",
      "catalog_number":"625",
      "title":"Directed Readings in Political Theory"
    },
    {
      "course_id":"002501",
      "subject":"PSYCH",
      "catalog_number":"607R",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"002425",
      "subject":"PSCI",
      "catalog_number":"626",
      "title":"Normative Political Theory"
    },
    {
      "course_id":"012973",
      "subject":"PSCI",
      "catalog_number":"629",
      "title":"Genetics and Justice"
    },
    {
      "course_id":"002428",
      "subject":"PSCI",
      "catalog_number":"630A",
      "title":"Public Administration and Policy 1"
    },
    {
      "course_id":"002429",
      "subject":"PSCI",
      "catalog_number":"630B",
      "title":"Public Administration and Policy 2"
    },
    {
      "course_id":"002430",
      "subject":"PSCI",
      "catalog_number":"631",
      "title":"The State and Economic Life"
    },
    {
      "course_id":"002431",
      "subject":"PSCI",
      "catalog_number":"632",
      "title":"The Politics of Canadian Resource Development"
    },
    {
      "course_id":"002432",
      "subject":"PSCI",
      "catalog_number":"633",
      "title":"Canadian Public Policy"
    },
    {
      "course_id":"002433",
      "subject":"PSCI",
      "catalog_number":"634",
      "title":"Comparative Public Administration"
    },
    {
      "course_id":"002434",
      "subject":"PSCI",
      "catalog_number":"635",
      "title":"Directed Readings in Public Policy and Administration"
    },
    {
      "course_id":"002435",
      "subject":"PSCI",
      "catalog_number":"636",
      "title":"Crime and Politics"
    },
    {
      "course_id":"012553",
      "subject":"PSCI",
      "catalog_number":"639",
      "title":"Global Social Governance"
    },
    {
      "course_id":"002437",
      "subject":"PSCI",
      "catalog_number":"642",
      "title":"Politics in Ontario"
    },
    {
      "course_id":"010617",
      "subject":"PSCI",
      "catalog_number":"643",
      "title":"Directed Readings in Provincial and Local Politics"
    },
    {
      "course_id":"002440",
      "subject":"PSCI",
      "catalog_number":"650",
      "title":"Approaches to the Study of Comparative Politics"
    },
    {
      "course_id":"002441",
      "subject":"PSCI",
      "catalog_number":"651",
      "title":"Democracy and Development"
    },
    {
      "course_id":"002442",
      "subject":"PSCI",
      "catalog_number":"652",
      "title":"Advanced Topics in Third World Politics and Development II"
    },
    {
      "course_id":"002443",
      "subject":"PSCI",
      "catalog_number":"653",
      "title":"Comparative Political Systems: Eastern Europe"
    },
    {
      "course_id":"002444",
      "subject":"PSCI",
      "catalog_number":"654",
      "title":"Post-War Reconstruction and State Building"
    },
    {
      "course_id":"002445",
      "subject":"PSCI",
      "catalog_number":"655",
      "title":"Ethnic Conflict and Conflict Resolution I"
    },
    {
      "course_id":"002446",
      "subject":"PSCI",
      "catalog_number":"656",
      "title":"Ethnic Conflict and  Conflict Resolution II"
    },
    {
      "course_id":"002447",
      "subject":"PSCI",
      "catalog_number":"657",
      "title":"International Organizations and Global Governance"
    },
    {
      "course_id":"002448",
      "subject":"PSCI",
      "catalog_number":"658",
      "title":"Human Rights in the Globalized World"
    },
    {
      "course_id":"002449",
      "subject":"PSCI",
      "catalog_number":"659",
      "title":"Conflict and Conflict Resolution"
    },
    {
      "course_id":"002450",
      "subject":"PSCI",
      "catalog_number":"661",
      "title":"Canadian Politics 1"
    },
    {
      "course_id":"002451",
      "subject":"PSCI",
      "catalog_number":"662",
      "title":"Canadian Politics 2"
    },
    {
      "course_id":"010618",
      "subject":"PSCI",
      "catalog_number":"663",
      "title":"Directed Readings in Canadian Politics"
    },
    {
      "course_id":"002452",
      "subject":"PSCI",
      "catalog_number":"664",
      "title":"Canada in the World: Foreign Policy"
    },
    {
      "course_id":"002454",
      "subject":"PSCI",
      "catalog_number":"668",
      "title":"The Politics of National Innovation Systems"
    },
    {
      "course_id":"002455",
      "subject":"PSCI",
      "catalog_number":"671",
      "title":"Women and Public Policy"
    },
    {
      "course_id":"002456",
      "subject":"PSCI",
      "catalog_number":"673",
      "title":"Directed Readings in Political Behaviour"
    },
    {
      "course_id":"002461",
      "subject":"PSCI",
      "catalog_number":"678",
      "title":"Security Ontology-Theory"
    },
    {
      "course_id":"013686",
      "subject":"PSCI",
      "catalog_number":"679",
      "title":"Security Governance: Actors, Institutions, and Issues"
    },
    {
      "course_id":"013377",
      "subject":"PSCI",
      "catalog_number":"680",
      "title":"Critical Security Studies"
    },
    {
      "course_id":"002462",
      "subject":"PSCI",
      "catalog_number":"681",
      "title":"Power Politics and World Order Studies"
    },
    {
      "course_id":"002463",
      "subject":"PSCI",
      "catalog_number":"682",
      "title":"Contemporary Strategy: Theories and Policies"
    },
    {
      "course_id":"002464",
      "subject":"PSCI",
      "catalog_number":"683",
      "title":"Topics in International Political Economy"
    },
    {
      "course_id":"009393",
      "subject":"PSCI",
      "catalog_number":"684",
      "title":"Special Topics in International Diplomacy"
    },
    {
      "course_id":"002465",
      "subject":"PSCI",
      "catalog_number":"685",
      "title":"Directed Readings in International Politics"
    },
    {
      "course_id":"002500",
      "subject":"PSYCH",
      "catalog_number":"607P",
      "title":"Cognitive Behaviour Therapy"
    },
    {
      "course_id":"002466",
      "subject":"PSCI",
      "catalog_number":"686",
      "title":"Emerging Economies in Global Governance"
    },
    {
      "course_id":"002467",
      "subject":"PSCI",
      "catalog_number":"687",
      "title":"Explaining Interstate War"
    },
    {
      "course_id":"002468",
      "subject":"PSCI",
      "catalog_number":"688",
      "title":"Governance of Global Economy"
    },
    {
      "course_id":"011482",
      "subject":"PSCI",
      "catalog_number":"689",
      "title":"International Political Economy"
    },
    {
      "course_id":"002471",
      "subject":"PSCI",
      "catalog_number":"692",
      "title":"Graduate Research Seminars"
    },
    {
      "course_id":"007865",
      "subject":"PSYCH",
      "catalog_number":"101",
      "title":"Introductory Psychology"
    },
    {
      "course_id":"007865",
      "subject":"PSYCH",
      "catalog_number":"101R",
      "title":"Introductory Psychology"
    },
    {
      "course_id":"007889",
      "subject":"PSYCH",
      "catalog_number":"207",
      "title":"Cognitive Processes"
    },
    {
      "course_id":"007894",
      "subject":"PSYCH",
      "catalog_number":"211",
      "title":"Developmental Psychology"
    },
    {
      "course_id":"007895",
      "subject":"PSYCH",
      "catalog_number":"212",
      "title":"Educational Psychology"
    },
    {
      "course_id":"007895",
      "subject":"PSYCH",
      "catalog_number":"212R",
      "title":"Educational Psychology"
    },
    {
      "course_id":"007896",
      "subject":"PSYCH",
      "catalog_number":"213R",
      "title":"Exceptional Children"
    },
    {
      "course_id":"006428",
      "subject":"PSYCH",
      "catalog_number":"218",
      "title":"Psychology of Death and Dying"
    },
    {
      "course_id":"013890",
      "subject":"PSYCH",
      "catalog_number":"226R",
      "title":"Positive Psychology"
    },
    {
      "course_id":"010100",
      "subject":"PSYCH",
      "catalog_number":"230",
      "title":"Psychology and Law"
    },
    {
      "course_id":"007913",
      "subject":"PSYCH",
      "catalog_number":"231",
      "title":"The Psychology of Religious Experience"
    },
    {
      "course_id":"007915",
      "subject":"PSYCH",
      "catalog_number":"232",
      "title":"Psychology of Evil"
    },
    {
      "course_id":"007917",
      "subject":"PSYCH",
      "catalog_number":"235",
      "title":"Psychological Perspectives on Gender and Sex"
    },
    {
      "course_id":"007918",
      "subject":"PSYCH",
      "catalog_number":"236",
      "title":"A Psychological Analysis of Human Sexuality"
    },
    {
      "course_id":"007904",
      "subject":"PSYCH",
      "catalog_number":"253",
      "title":"Social Psychology"
    },
    {
      "course_id":"007904",
      "subject":"PSYCH",
      "catalog_number":"253R",
      "title":"Social Psychology"
    },
    {
      "course_id":"007293",
      "subject":"PSYCH",
      "catalog_number":"256",
      "title":"Introduction to Cognitive Science"
    },
    {
      "course_id":"007928",
      "subject":"PSYCH",
      "catalog_number":"257",
      "title":"Psychopathology"
    },
    {
      "course_id":"007928",
      "subject":"PSYCH",
      "catalog_number":"257R",
      "title":"Psychopathology"
    },
    {
      "course_id":"007931",
      "subject":"PSYCH",
      "catalog_number":"261",
      "title":"Physiological Psychology"
    },
    {
      "course_id":"011664",
      "subject":"PSYCH",
      "catalog_number":"264",
      "title":"Research Apprenticeship"
    },
    {
      "course_id":"007934",
      "subject":"PSYCH",
      "catalog_number":"291",
      "title":"Basic Research Methods"
    },
    {
      "course_id":"007935",
      "subject":"PSYCH",
      "catalog_number":"292",
      "title":"Basic Data Analysis"
    },
    {
      "course_id":"007936",
      "subject":"PSYCH",
      "catalog_number":"304",
      "title":"Thinking and Deciding"
    },
    {
      "course_id":"007938",
      "subject":"PSYCH",
      "catalog_number":"306",
      "title":"Perception"
    },
    {
      "course_id":"007939",
      "subject":"PSYCH",
      "catalog_number":"307",
      "title":"Human Neuropsychology"
    },
    {
      "course_id":"007940",
      "subject":"PSYCH",
      "catalog_number":"308",
      "title":"Psychology of Reading"
    },
    {
      "course_id":"007943",
      "subject":"PSYCH",
      "catalog_number":"312",
      "title":"Learning Disabilities"
    },
    {
      "course_id":"007943",
      "subject":"PSYCH",
      "catalog_number":"312R",
      "title":"Learning Disabilities"
    },
    {
      "course_id":"007944",
      "subject":"PSYCH",
      "catalog_number":"314",
      "title":"Cognitive Development"
    },
    {
      "course_id":"007945",
      "subject":"PSYCH",
      "catalog_number":"315",
      "title":"Psychology of Adolescence"
    },
    {
      "course_id":"007947",
      "subject":"PSYCH",
      "catalog_number":"317",
      "title":"Child Psychopathology"
    },
    {
      "course_id":"007948",
      "subject":"PSYCH",
      "catalog_number":"318",
      "title":"Psychosexual Organization"
    },
    {
      "course_id":"011396",
      "subject":"PSYCH",
      "catalog_number":"319",
      "title":"Problem Behaviour in the Classroom"
    },
    {
      "course_id":"011305",
      "subject":"PSYCH",
      "catalog_number":"320",
      "title":"Language Development"
    },
    {
      "course_id":"013343",
      "subject":"PSYCH",
      "catalog_number":"321",
      "title":"Conceptual Development"
    },
    {
      "course_id":"007952",
      "subject":"PSYCH",
      "catalog_number":"322R",
      "title":"Personality Theory"
    },
    {
      "course_id":"010042",
      "subject":"PSYCH",
      "catalog_number":"330",
      "title":"Criminal Profiling"
    },
    {
      "course_id":"012325",
      "subject":"PSYCH",
      "catalog_number":"332",
      "title":"Human Motivation and Emotion"
    },
    {
      "course_id":"007962",
      "subject":"PSYCH",
      "catalog_number":"334R",
      "title":"Theories of Individual Counselling Psychology"
    },
    {
      "course_id":"014223",
      "subject":"PSYCH",
      "catalog_number":"335",
      "title":"Developmental Neuropsychology"
    },
    {
      "course_id":"007965",
      "subject":"PSYCH",
      "catalog_number":"336",
      "title":"Introduction to Clinical Psychology"
    },
    {
      "course_id":"007967",
      "subject":"PSYCH",
      "catalog_number":"338",
      "title":"Organizational Psychology"
    },
    {
      "course_id":"007968",
      "subject":"PSYCH",
      "catalog_number":"339",
      "title":"Personnel Psychology"
    },
    {
      "course_id":"011708",
      "subject":"PSYCH",
      "catalog_number":"340",
      "title":"Training and Development"
    },
    {
      "course_id":"014501",
      "subject":"PSYCH",
      "catalog_number":"342",
      "title":"The Psychology of Groups and Teams"
    },
    {
      "course_id":"011388",
      "subject":"PSYCH",
      "catalog_number":"349R",
      "title":"Cross-Cultural Psychology"
    },
    {
      "course_id":"013526",
      "subject":"PSYCH",
      "catalog_number":"350",
      "title":"Political Psychology"
    },
    {
      "course_id":"010124",
      "subject":"PSYCH",
      "catalog_number":"352",
      "title":"Culture and Psychology"
    },
    {
      "course_id":"007972",
      "subject":"PSYCH",
      "catalog_number":"353",
      "title":"Social Cognition"
    },
    {
      "course_id":"007906",
      "subject":"PSYCH",
      "catalog_number":"354",
      "title":"Interpersonal Relations"
    },
    {
      "course_id":"007906",
      "subject":"PSYCH",
      "catalog_number":"354R",
      "title":"Interpersonal Relations"
    },
    {
      "course_id":"014503",
      "subject":"PSYCH",
      "catalog_number":"355",
      "title":"Intergroup Relations"
    },
    {
      "course_id":"011585",
      "subject":"PSYCH",
      "catalog_number":"356",
      "title":"Personality"
    },
    {
      "course_id":"011585",
      "subject":"PSYCH",
      "catalog_number":"356R",
      "title":"Personality"
    },
    {
      "course_id":"007977",
      "subject":"PSYCH",
      "catalog_number":"361",
      "title":"Evolutionary and Comparative Psychology"
    },
    {
      "course_id":"010159",
      "subject":"PSYCH",
      "catalog_number":"363",
      "title":"Special Subjects"
    },
    {
      "course_id":"014512",
      "subject":"PSYCH",
      "catalog_number":"372",
      "title":"Environmental Psychology"
    },
    {
      "course_id":"012190",
      "subject":"PSYCH",
      "catalog_number":"375R",
      "title":"Studies in Psychology"
    },
    {
      "course_id":"012961",
      "subject":"PSYCH",
      "catalog_number":"380",
      "title":"History of Psychology"
    },
    {
      "course_id":"007998",
      "subject":"PSYCH",
      "catalog_number":"391",
      "title":"Advanced Data Analysis"
    },
    {
      "course_id":"013001",
      "subject":"PSYCH",
      "catalog_number":"392",
      "title":"Research in Human Cognitive Neuroscience"
    },
    {
      "course_id":"008000",
      "subject":"PSYCH",
      "catalog_number":"393",
      "title":"Research in Developmental Psychology"
    },
    {
      "course_id":"008001",
      "subject":"PSYCH",
      "catalog_number":"394",
      "title":"Research in Cognition and Perception"
    },
    {
      "course_id":"008002",
      "subject":"PSYCH",
      "catalog_number":"395",
      "title":"Research in Social Psychology"
    },
    {
      "course_id":"008003",
      "subject":"PSYCH",
      "catalog_number":"396",
      "title":"Research in Behavioural Neuroscience"
    },
    {
      "course_id":"008004",
      "subject":"PSYCH",
      "catalog_number":"397",
      "title":"Research in Personality and Clinical Psychology"
    },
    {
      "course_id":"008005",
      "subject":"PSYCH",
      "catalog_number":"398",
      "title":"Research in Memory"
    },
    {
      "course_id":"008006",
      "subject":"PSYCH",
      "catalog_number":"398R",
      "title":"Independent Study"
    },
    {
      "course_id":"011678",
      "subject":"PSYCH",
      "catalog_number":"399",
      "title":"Research in Industrial\/Organizational Psychology"
    },
    {
      "course_id":"008007",
      "subject":"PSYCH",
      "catalog_number":"399R",
      "title":"Independent Study"
    },
    {
      "course_id":"013342",
      "subject":"PSYCH",
      "catalog_number":"420",
      "title":"An Introduction to Computational Neuroscience Methods"
    },
    {
      "course_id":"012754",
      "subject":"PSYCH",
      "catalog_number":"439",
      "title":"Negotiation in the Workplace: Theory and Practice"
    },
    {
      "course_id":"012715",
      "subject":"PSYCH",
      "catalog_number":"447",
      "title":"Seminar in Cognitive Science"
    },
    {
      "course_id":"014379",
      "subject":"PSYCH",
      "catalog_number":"448R",
      "title":"Close Relationships"
    },
    {
      "course_id":"014380",
      "subject":"PSYCH",
      "catalog_number":"449R",
      "title":"Race and Gender Equality"
    },
    {
      "course_id":"013096",
      "subject":"PSYCH",
      "catalog_number":"450R",
      "title":"Honours Seminar in Special Topics"
    },
    {
      "course_id":"008019",
      "subject":"PSYCH",
      "catalog_number":"453",
      "title":"Honours Seminar in Developmental Psychology"
    },
    {
      "course_id":"008027",
      "subject":"PSYCH",
      "catalog_number":"454",
      "title":"Honours Seminar in Educational Psychology"
    },
    {
      "course_id":"008035",
      "subject":"PSYCH",
      "catalog_number":"455",
      "title":"Honours Seminar in Social Psychology"
    },
    {
      "course_id":"008049",
      "subject":"PSYCH",
      "catalog_number":"457",
      "title":"Honours Seminar in Personality and Clinical Psychology"
    },
    {
      "course_id":"008060",
      "subject":"PSYCH",
      "catalog_number":"458",
      "title":"Honours Seminar in Cognition"
    },
    {
      "course_id":"008065",
      "subject":"PSYCH",
      "catalog_number":"461",
      "title":"Honours Seminar in Cognitive Neuroscience"
    },
    {
      "course_id":"008073",
      "subject":"PSYCH",
      "catalog_number":"462",
      "title":"Honours Seminar in Industrial\/Organizational Psychology"
    },
    {
      "course_id":"010160",
      "subject":"PSYCH",
      "catalog_number":"463",
      "title":"Honours Seminar in Special Topics"
    },
    {
      "course_id":"008094",
      "subject":"PSYCH",
      "catalog_number":"464",
      "title":"Advanced Research Apprenticeship"
    },
    {
      "course_id":"008096",
      "subject":"PSYCH",
      "catalog_number":"465",
      "title":"Applied Apprenticeship"
    },
    {
      "course_id":"012756",
      "subject":"PSYCH",
      "catalog_number":"467",
      "title":"Human Resources Apprenticeship"
    },
    {
      "course_id":"008098",
      "subject":"PSYCH",
      "catalog_number":"480",
      "title":"Directed Studies - Elective"
    },
    {
      "course_id":"011169",
      "subject":"PSYCH",
      "catalog_number":"481",
      "title":"Directed Studies - Natural Science Advanced Psych"
    },
    {
      "course_id":"011170",
      "subject":"PSYCH",
      "catalog_number":"482",
      "title":"Directed Studies - Social Science Advanced Psych"
    },
    {
      "course_id":"011171",
      "subject":"PSYCH",
      "catalog_number":"483",
      "title":"Directed Studies - Natural Science Research"
    },
    {
      "course_id":"011172",
      "subject":"PSYCH",
      "catalog_number":"484",
      "title":"Directed Studies - Social Science Research"
    },
    {
      "course_id":"011173",
      "subject":"PSYCH",
      "catalog_number":"485",
      "title":"Directed Studies - Seminar"
    },
    {
      "course_id":"012281",
      "subject":"PSYCH",
      "catalog_number":"486",
      "title":"Directed Studies - Advanced Statistics"
    },
    {
      "course_id":"013100",
      "subject":"PSYCH",
      "catalog_number":"490R",
      "title":"Special Studies"
    },
    {
      "course_id":"010123",
      "subject":"PSYCH",
      "catalog_number":"492",
      "title":"Psychological Measurement: Foundations of Research and Practice"
    },
    {
      "course_id":"008105",
      "subject":"PSYCH",
      "catalog_number":"499A",
      "title":"Honours Thesis - Part 1"
    },
    {
      "course_id":"008106",
      "subject":"PSYCH",
      "catalog_number":"499B",
      "title":"Honours Thesis - Part 2"
    },
    {
      "course_id":"008107",
      "subject":"PSYCH",
      "catalog_number":"499C",
      "title":"Honours Thesis - Part 3"
    },
    {
      "course_id":"010580",
      "subject":"PSYCH",
      "catalog_number":"605",
      "title":"Special Topics in Clinical Psychology"
    },
    {
      "course_id":"002517",
      "subject":"PSYCH",
      "catalog_number":"621",
      "title":"Advanced Clinical Research"
    },
    {
      "course_id":"011138",
      "subject":"PSYCH",
      "catalog_number":"630",
      "title":"Advanced Analysis of Variance"
    },
    {
      "course_id":"002539",
      "subject":"PSYCH",
      "catalog_number":"632",
      "title":"Multiple Regression"
    },
    {
      "course_id":"010589",
      "subject":"PSYCH",
      "catalog_number":"640",
      "title":"Special Topics in Psychology"
    },
    {
      "course_id":"002572",
      "subject":"PSYCH",
      "catalog_number":"650",
      "title":"Special Topics in Cognition and Perception"
    },
    {
      "course_id":"010590",
      "subject":"PSYCH",
      "catalog_number":"670",
      "title":"Special Topics in Behavioural Neuroscience"
    },
    {
      "course_id":"002626",
      "subject":"PSYCH",
      "catalog_number":"677A",
      "title":"Fundamentals of Behavioural Neuroscience"
    },
    {
      "course_id":"010591",
      "subject":"PSYCH",
      "catalog_number":"680",
      "title":"Special Topics in Child Behaviour and Development"
    },
    {
      "course_id":"010592",
      "subject":"PSYCH",
      "catalog_number":"690",
      "title":"Special Topics in Social and Personality"
    },
    {
      "course_id":"002722",
      "subject":"PSYCH",
      "catalog_number":"707A",
      "title":"Behavioural Neuroscience Seminar I"
    },
    {
      "course_id":"014865",
      "subject":"PSYCH",
      "catalog_number":"701",
      "title":"Foundations in Cognitive\/Social Development: Basic"
    },
    {
      "course_id":"014866",
      "subject":"PSYCH",
      "catalog_number":"702",
      "title":"Foundations in Cognitive\/Social Development: Social Cognitive Development"
    },
    {
      "course_id":"002717",
      "subject":"PSYCH",
      "catalog_number":"703",
      "title":"Language Development"
    },
    {
      "course_id":"002719",
      "subject":"PSYCH",
      "catalog_number":"704A",
      "title":"Social Psychology"
    },
    {
      "course_id":"002720",
      "subject":"PSYCH",
      "catalog_number":"704B",
      "title":"Social Psychology"
    },
    {
      "course_id":"014867",
      "subject":"PSYCH",
      "catalog_number":"705",
      "title":"Foundations in Language Development: Basic Language Development"
    },
    {
      "course_id":"014868",
      "subject":"PSYCH",
      "catalog_number":"706",
      "title":"Foundations in Language Development: Pragmatics of Language"
    },
    {
      "course_id":"014726",
      "subject":"PSYCH",
      "catalog_number":"877",
      "title":"Work Motivation"
    },
    {
      "course_id":"010594",
      "subject":"PSYCH",
      "catalog_number":"707",
      "title":"Cognitive Neuroscience Seminar"
    },
    {
      "course_id":"002724",
      "subject":"PSYCH",
      "catalog_number":"708",
      "title":"Reasoning about Ownership of Property"
    },
    {
      "course_id":"012223",
      "subject":"PSYCH",
      "catalog_number":"709",
      "title":"Reasoning about Beliefs and Desires"
    },
    {
      "course_id":"010595",
      "subject":"PSYCH",
      "catalog_number":"710",
      "title":"Current Issues in Developmental Psych Seminar"
    },
    {
      "course_id":"002742",
      "subject":"PSYCH",
      "catalog_number":"714A",
      "title":"Behavioural Neuroscience Seminar II"
    },
    {
      "course_id":"010596",
      "subject":"PSYCH",
      "catalog_number":"711",
      "title":"Seminar In Personality"
    },
    {
      "course_id":"002741",
      "subject":"PSYCH",
      "catalog_number":"712",
      "title":"Social Development"
    },
    {
      "course_id":"010597",
      "subject":"PSYCH",
      "catalog_number":"713",
      "title":"Theories of Pretence"
    },
    {
      "course_id":"010279",
      "subject":"PSYCH",
      "catalog_number":"714",
      "title":"Current Topics in Social Psych Seminar"
    },
    {
      "course_id":"014570",
      "subject":"PSYCH",
      "catalog_number":"716",
      "title":"Adult Psychopathology"
    },
    {
      "course_id":"014571",
      "subject":"PSYCH",
      "catalog_number":"717",
      "title":"Psychological Assessment I"
    },
    {
      "course_id":"014573",
      "subject":"PSYCH",
      "catalog_number":"718",
      "title":"Psychological Assessment II"
    },
    {
      "course_id":"014572",
      "subject":"PSYCH",
      "catalog_number":"719",
      "title":"Ethics, Diversity, and Professional Issues in Clinical Psychology"
    },
    {
      "course_id":"014574",
      "subject":"PSYCH",
      "catalog_number":"720A",
      "title":"Practicum in Interviewing & Cognitive Assessment I"
    },
    {
      "course_id":"014575",
      "subject":"PSYCH",
      "catalog_number":"720B",
      "title":"Practicum in Interviewing & Cognitive Assessment II"
    },
    {
      "course_id":"014576",
      "subject":"PSYCH",
      "catalog_number":"721A",
      "title":"Diagnostic Assessment Practicum I"
    },
    {
      "course_id":"014577",
      "subject":"PSYCH",
      "catalog_number":"721B",
      "title":"Diagnostic Assessment Practicum II"
    },
    {
      "course_id":"014578",
      "subject":"PSYCH",
      "catalog_number":"722C",
      "title":"Clinical Fieldwork Placement I"
    },
    {
      "course_id":"014579",
      "subject":"PSYCH",
      "catalog_number":"723",
      "title":"Child Psychopathology and Psychotherapy"
    },
    {
      "course_id":"014580",
      "subject":"PSYCH",
      "catalog_number":"724",
      "title":"Personality & Measurement Theory"
    },
    {
      "course_id":"014581",
      "subject":"PSYCH",
      "catalog_number":"725",
      "title":"Cognitive Behaviour Therapy"
    },
    {
      "course_id":"014582",
      "subject":"PSYCH",
      "catalog_number":"726A",
      "title":"Practicum in Integrated Assessment I"
    },
    {
      "course_id":"014583",
      "subject":"PSYCH",
      "catalog_number":"726B",
      "title":"Practicum in Integrated Assessment II"
    },
    {
      "course_id":"014584",
      "subject":"PSYCH",
      "catalog_number":"727",
      "title":"Efficacy & Program Evaluation"
    },
    {
      "course_id":"014585",
      "subject":"PSYCH",
      "catalog_number":"728",
      "title":"Psychotherapy:  Classical Roots & Contemporary Developments"
    },
    {
      "course_id":"014586",
      "subject":"PSYCH",
      "catalog_number":"729A",
      "title":"Child and Adolescent Psychotherapy Practicum I"
    },
    {
      "course_id":"014587",
      "subject":"PSYCH",
      "catalog_number":"729B",
      "title":"Child and Adolescent Psychotherapy Practicum II"
    },
    {
      "course_id":"014588",
      "subject":"PSYCH",
      "catalog_number":"729C",
      "title":"Child and Adolescent Psychotherapy Practicum III"
    },
    {
      "course_id":"014589",
      "subject":"PSYCH",
      "catalog_number":"730A",
      "title":"Adult Psychotherapy Practicum I"
    },
    {
      "course_id":"014590",
      "subject":"PSYCH",
      "catalog_number":"730B",
      "title":"Adult Psychotherapy Practicum II"
    },
    {
      "course_id":"014604",
      "subject":"PSYCH",
      "catalog_number":"730C",
      "title":"Adult Psychotherapy Practicum III"
    },
    {
      "course_id":"002749",
      "subject":"PSYCH",
      "catalog_number":"731",
      "title":"Emotion-Focused Therapy"
    },
    {
      "course_id":"002754",
      "subject":"PSYCH",
      "catalog_number":"747A",
      "title":"Behavioural Neuroscience Seminar IV"
    },
    {
      "course_id":"002755",
      "subject":"PSYCH",
      "catalog_number":"747B",
      "title":"Behavioural Neuroscience Seminar IV"
    },
    {
      "course_id":"014605",
      "subject":"PSYCH",
      "catalog_number":"732A",
      "title":"Child and Adolescent Psychotherapy Practicum I"
    },
    {
      "course_id":"014606",
      "subject":"PSYCH",
      "catalog_number":"732B",
      "title":"Child and Adolescent Psychotherapy Practicum II"
    },
    {
      "course_id":"014607",
      "subject":"PSYCH",
      "catalog_number":"732C",
      "title":"Child and Adolescent Psychotherapy Practicum III"
    },
    {
      "course_id":"014608",
      "subject":"PSYCH",
      "catalog_number":"733A",
      "title":"Adult Psychotherapy Practicum I"
    },
    {
      "course_id":"014609",
      "subject":"PSYCH",
      "catalog_number":"733B",
      "title":"Adult Psychotherapy Practicum II"
    },
    {
      "course_id":"014610",
      "subject":"PSYCH",
      "catalog_number":"733C",
      "title":"Adult Psychotherapy Practicum III"
    },
    {
      "course_id":"014611",
      "subject":"PSYCH",
      "catalog_number":"734A",
      "title":"Practicum in Supervision I"
    },
    {
      "course_id":"014612",
      "subject":"PSYCH",
      "catalog_number":"734B",
      "title":"Practicum in Supervision II"
    },
    {
      "course_id":"014613",
      "subject":"PSYCH",
      "catalog_number":"734C",
      "title":"Practicum in Supervision III"
    },
    {
      "course_id":"014614",
      "subject":"PSYCH",
      "catalog_number":"735A",
      "title":"Child and Adolescent Psychotherapy Practicum I"
    },
    {
      "course_id":"014615",
      "subject":"PSYCH",
      "catalog_number":"735B",
      "title":"Child and Adolescent Psychotherapy Practicum II"
    },
    {
      "course_id":"014616",
      "subject":"PSYCH",
      "catalog_number":"735C",
      "title":"Child and Adolescent Psychotherapy Practicum III"
    },
    {
      "course_id":"014617",
      "subject":"PSYCH",
      "catalog_number":"736A",
      "title":"Adult Psychotherapy Practicum I"
    },
    {
      "course_id":"014618",
      "subject":"PSYCH",
      "catalog_number":"736B",
      "title":"Adult Psychotherapy Practicum II"
    },
    {
      "course_id":"014619",
      "subject":"PSYCH",
      "catalog_number":"736C",
      "title":"Adult Psychotherapy Practicum III"
    },
    {
      "course_id":"014620",
      "subject":"PSYCH",
      "catalog_number":"737A",
      "title":"Emotion-Focused Therapy Practicum"
    },
    {
      "course_id":"014621",
      "subject":"PSYCH",
      "catalog_number":"737B",
      "title":"Emotion-Focused Therapy Practicum"
    },
    {
      "course_id":"014622",
      "subject":"PSYCH",
      "catalog_number":"737C",
      "title":"Couples' Therapy Practicum"
    },
    {
      "course_id":"014623",
      "subject":"PSYCH",
      "catalog_number":"738A",
      "title":"Clinical Fieldwork Placement II"
    },
    {
      "course_id":"014624",
      "subject":"PSYCH",
      "catalog_number":"738B",
      "title":"Clinical Fieldwork Placement II"
    },
    {
      "course_id":"014625",
      "subject":"PSYCH",
      "catalog_number":"738C",
      "title":"Clinical Fieldwork Placement II"
    },
    {
      "course_id":"014626",
      "subject":"PSYCH",
      "catalog_number":"739A",
      "title":"Clinical Fieldwork Placement III"
    },
    {
      "course_id":"014627",
      "subject":"PSYCH",
      "catalog_number":"739B",
      "title":"Clinical Fieldwork Placement III"
    },
    {
      "course_id":"014628",
      "subject":"PSYCH",
      "catalog_number":"739C",
      "title":"Clinical Fieldwork Placement III"
    },
    {
      "course_id":"014629",
      "subject":"PSYCH",
      "catalog_number":"740A",
      "title":"Senior Practicum I"
    },
    {
      "course_id":"014630",
      "subject":"PSYCH",
      "catalog_number":"740B",
      "title":"Senior Practicum I"
    },
    {
      "course_id":"014631",
      "subject":"PSYCH",
      "catalog_number":"740C",
      "title":"Senior Practicum I"
    },
    {
      "course_id":"014632",
      "subject":"PSYCH",
      "catalog_number":"741A",
      "title":"Senior Practicum II"
    },
    {
      "course_id":"014592",
      "subject":"PSYCH",
      "catalog_number":"741B",
      "title":"Senior Practicum II"
    },
    {
      "course_id":"014591",
      "subject":"PSYCH",
      "catalog_number":"741C",
      "title":"Senior Practicum II"
    },
    {
      "course_id":"014593",
      "subject":"PSYCH",
      "catalog_number":"742A",
      "title":"Senior Practicum III"
    },
    {
      "course_id":"014594",
      "subject":"PSYCH",
      "catalog_number":"742B",
      "title":"Senior Practicum III"
    },
    {
      "course_id":"014595",
      "subject":"PSYCH",
      "catalog_number":"742C",
      "title":"Senior Practicum III"
    },
    {
      "course_id":"002754",
      "subject":"PSYCH",
      "catalog_number":"747",
      "title":"C\/P Research Seminar"
    },
    {
      "course_id":"012224",
      "subject":"PSYCH",
      "catalog_number":"769",
      "title":"Causal Reasoning"
    },
    {
      "course_id":"002758",
      "subject":"PSYCH",
      "catalog_number":"770",
      "title":"Basic Issues in Cognition"
    },
    {
      "course_id":"002759",
      "subject":"PSYCH",
      "catalog_number":"771",
      "title":"Basic Visual Processes"
    },
    {
      "course_id":"002760",
      "subject":"PSYCH",
      "catalog_number":"772",
      "title":"Auditory Processes and Speech Perception"
    },
    {
      "course_id":"002761",
      "subject":"PSYCH",
      "catalog_number":"773",
      "title":"Psychophysics and Measurement"
    },
    {
      "course_id":"002762",
      "subject":"PSYCH",
      "catalog_number":"774",
      "title":"Visual Cognition"
    },
    {
      "course_id":"002763",
      "subject":"PSYCH",
      "catalog_number":"775",
      "title":"Consciousness and Cognition"
    },
    {
      "course_id":"002764",
      "subject":"PSYCH",
      "catalog_number":"776",
      "title":"Problem Solving, Judgment and  Decision-Making"
    },
    {
      "course_id":"002765",
      "subject":"PSYCH",
      "catalog_number":"777",
      "title":"Human Memory"
    },
    {
      "course_id":"002766",
      "subject":"PSYCH",
      "catalog_number":"778",
      "title":"Attention"
    },
    {
      "course_id":"002767",
      "subject":"PSYCH",
      "catalog_number":"779",
      "title":"Language and Reading"
    },
    {
      "course_id":"002768",
      "subject":"PSYCH",
      "catalog_number":"779A",
      "title":"Cognitive Neuropsychology I"
    },
    {
      "course_id":"010601",
      "subject":"PSYCH",
      "catalog_number":"779B",
      "title":"Cognitive Neuropsychology II"
    },
    {
      "course_id":"002770",
      "subject":"PSYCH",
      "catalog_number":"781",
      "title":"Cognitive Neuroscience of Memory"
    },
    {
      "course_id":"010602",
      "subject":"PSYCH",
      "catalog_number":"782",
      "title":"Visual Neuroscience"
    },
    {
      "course_id":"002772",
      "subject":"PSYCH",
      "catalog_number":"783",
      "title":"Neuroimaging of Cognition"
    },
    {
      "course_id":"010603",
      "subject":"PSYCH",
      "catalog_number":"784",
      "title":"Human Neuroanatomy and Neuropathology"
    },
    {
      "course_id":"010604",
      "subject":"PSYCH",
      "catalog_number":"785",
      "title":"Clinical Neuropsychology"
    },
    {
      "course_id":"010605",
      "subject":"PSYCH",
      "catalog_number":"786",
      "title":"Neuropsychological Assessment Practicum"
    },
    {
      "course_id":"010606",
      "subject":"PSYCH",
      "catalog_number":"787",
      "title":"Visual Perception"
    },
    {
      "course_id":"012868",
      "subject":"PSYCH",
      "catalog_number":"788",
      "title":"Epidemiologic Methods in Aging Research"
    },
    {
      "course_id":"013251",
      "subject":"PSYCH",
      "catalog_number":"789",
      "title":"Mind-wandering and Inattention"
    },
    {
      "course_id":"013252",
      "subject":"PSYCH",
      "catalog_number":"790",
      "title":"Case Studies in Neuropsychology"
    },
    {
      "course_id":"013253",
      "subject":"PSYCH",
      "catalog_number":"791",
      "title":"Real and Virtual Spaces"
    },
    {
      "course_id":"013254",
      "subject":"PSYCH",
      "catalog_number":"792",
      "title":"An Introduction to Methods in Computational Neuroscience"
    },
    {
      "course_id":"013378",
      "subject":"PSYCH",
      "catalog_number":"793",
      "title":"Electrophysiology Methodologies in Brain Research: from Basic Concepts to Lab Practice"
    },
    {
      "course_id":"014425",
      "subject":"PSYCH",
      "catalog_number":"794",
      "title":"Cognitive Neuroscience of Face Perception"
    },
    {
      "course_id":"014307",
      "subject":"PSYCH",
      "catalog_number":"795",
      "title":"Structure and Function in the Developing Brain"
    },
    {
      "course_id":"002774",
      "subject":"PSYCH",
      "catalog_number":"800",
      "title":"Psychometric Theory & Structural Equation Modeling"
    },
    {
      "course_id":"002775",
      "subject":"PSYCH",
      "catalog_number":"801",
      "title":"Advanced Structural Equation Modeling"
    },
    {
      "course_id":"010607",
      "subject":"PSYCH",
      "catalog_number":"803",
      "title":"Statistical Reasoning & Advanced Experimental Analysis"
    },
    {
      "course_id":"012329",
      "subject":"PSYCH",
      "catalog_number":"804",
      "title":"Multi-Level Modeling Applications in Psychology"
    },
    {
      "course_id":"010608",
      "subject":"PSYCH",
      "catalog_number":"810",
      "title":"Directed Studies"
    },
    {
      "course_id":"012229",
      "subject":"PSYCH",
      "catalog_number":"820",
      "title":"Community Practicum I"
    },
    {
      "course_id":"012230",
      "subject":"PSYCH",
      "catalog_number":"821",
      "title":"Community Practicum II"
    },
    {
      "course_id":"012231",
      "subject":"PSYCH",
      "catalog_number":"822",
      "title":"Community Practicum III"
    },
    {
      "course_id":"002790",
      "subject":"PSYCH",
      "catalog_number":"836A",
      "title":"Advanced Practicum in Applied Psychology"
    },
    {
      "course_id":"010609",
      "subject":"PSYCH",
      "catalog_number":"844",
      "title":"Special Topics in Educational Psychology"
    },
    {
      "course_id":"010610",
      "subject":"PSYCH",
      "catalog_number":"846",
      "title":"Special Topics in Applied Psychology"
    },
    {
      "course_id":"013065",
      "subject":"RUSS",
      "catalog_number":"614",
      "title":"Topics in Linguistic Theory"
    },
    {
      "course_id":"012232",
      "subject":"PSYCH",
      "catalog_number":"851",
      "title":"Research Lab Internship I"
    },
    {
      "course_id":"009412",
      "subject":"PSYCH",
      "catalog_number":"852",
      "title":"Research Lab Internship II"
    },
    {
      "course_id":"002862",
      "subject":"PSYCH",
      "catalog_number":"853",
      "title":"Research Lab Internship III"
    },
    {
      "course_id":"012339",
      "subject":"PSYCH",
      "catalog_number":"870",
      "title":"Research Design & Methods"
    },
    {
      "course_id":"002867",
      "subject":"PSYCH",
      "catalog_number":"880",
      "title":"Industrial and Organizational Psychology"
    },
    {
      "course_id":"002869",
      "subject":"PSYCH",
      "catalog_number":"881A",
      "title":"Personnel Psychology"
    },
    {
      "course_id":"002872",
      "subject":"PSYCH",
      "catalog_number":"883",
      "title":"Organizational Development"
    },
    {
      "course_id":"010612",
      "subject":"PSYCH",
      "catalog_number":"884",
      "title":"Special Topics in Industrial & Organizational Psychology"
    },
    {
      "course_id":"010613",
      "subject":"PSYCH",
      "catalog_number":"885",
      "title":"Industrial & Organizational Psychology Research Seminar"
    },
    {
      "course_id":"002890",
      "subject":"PSYCH",
      "catalog_number":"886",
      "title":"Psychology of Training"
    },
    {
      "course_id":"011831",
      "subject":"PSYCH",
      "catalog_number":"887",
      "title":"Research Methods in Industrial\/Organizational"
    },
    {
      "course_id":"012845",
      "subject":"PSYCH",
      "catalog_number":"888",
      "title":"Negotiation: Theory and Practice"
    },
    {
      "course_id":"011589",
      "subject":"QIC",
      "catalog_number":"710",
      "title":"Quantum Information Processing"
    },
    {
      "course_id":"013787",
      "subject":"QIC",
      "catalog_number":"750",
      "title":"Implementation of Quantum Information Processing"
    },
    {
      "course_id":"000711",
      "subject":"QIC",
      "catalog_number":"820",
      "title":"Theory of Quantum Information"
    },
    {
      "course_id":"013823",
      "subject":"QIC",
      "catalog_number":"823",
      "title":"Quantum Algorithms"
    },
    {
      "course_id":"012567",
      "subject":"QIC",
      "catalog_number":"845",
      "title":"Open Quantum Systems"
    },
    {
      "course_id":"013788",
      "subject":"QIC",
      "catalog_number":"880",
      "title":"Nanoelectronics for Quantum Information Processing"
    },
    {
      "course_id":"013824",
      "subject":"QIC",
      "catalog_number":"885",
      "title":"Quantum Electronics and Photonics"
    },
    {
      "course_id":"013789",
      "subject":"QIC",
      "catalog_number":"890",
      "title":"Topics in Quantum Information"
    },
    {
      "course_id":"013063",
      "subject":"RUSS",
      "catalog_number":"612",
      "title":"Topics in Sociolinguistics"
    },
    {
      "course_id":"013064",
      "subject":"RUSS",
      "catalog_number":"613",
      "title":"Topics in Discourse Analysis"
    },
    {
      "course_id":"013920",
      "subject":"QIC",
      "catalog_number":"891",
      "title":"Topics in Quantum Information"
    },
    {
      "course_id":"013790",
      "subject":"QIC",
      "catalog_number":"895",
      "title":"Topics in Quantum Information"
    },
    {
      "course_id":"008108",
      "subject":"REC",
      "catalog_number":"100",
      "title":"Introduction to the Study of Recreation and Leisure"
    },
    {
      "course_id":"008109",
      "subject":"REC",
      "catalog_number":"101",
      "title":"Introduction to Recreation and Leisure Services"
    },
    {
      "course_id":"014320",
      "subject":"REC",
      "catalog_number":"151",
      "title":"Foundations of Therapeutic Recreation Practice"
    },
    {
      "course_id":"008110",
      "subject":"REC",
      "catalog_number":"200",
      "title":"Play, Creativity and Child Development"
    },
    {
      "course_id":"006230",
      "subject":"REC",
      "catalog_number":"202",
      "title":"History of Western Sport"
    },
    {
      "course_id":"008112",
      "subject":"REC",
      "catalog_number":"203",
      "title":"Sociology of Sport"
    },
    {
      "course_id":"008114",
      "subject":"REC",
      "catalog_number":"205",
      "title":"Social Psychology of Leisure"
    },
    {
      "course_id":"008117",
      "subject":"REC",
      "catalog_number":"215",
      "title":"Marketing Recreation and Sport Services"
    },
    {
      "course_id":"008118",
      "subject":"REC",
      "catalog_number":"220",
      "title":"Program Management"
    },
    {
      "course_id":"008119",
      "subject":"REC",
      "catalog_number":"230",
      "title":"Outdoor Recreation Resources Management"
    },
    {
      "course_id":"008122",
      "subject":"REC",
      "catalog_number":"251",
      "title":"Therapeutic Recreation: Developmental and Emotional Disabilities"
    },
    {
      "course_id":"008123",
      "subject":"REC",
      "catalog_number":"252",
      "title":"Therapeutic Recreation: Physical Disabilities"
    },
    {
      "course_id":"012743",
      "subject":"REC",
      "catalog_number":"253",
      "title":"Practicum in Therapeutic Recreation"
    },
    {
      "course_id":"008125",
      "subject":"REC",
      "catalog_number":"270",
      "title":"Research Design Applicable to Leisure Studies"
    },
    {
      "course_id":"008128",
      "subject":"REC",
      "catalog_number":"280",
      "title":"Introduction to Tourism"
    },
    {
      "course_id":"008130",
      "subject":"REC",
      "catalog_number":"301",
      "title":"Sociology of Leisure"
    },
    {
      "course_id":"008133",
      "subject":"REC",
      "catalog_number":"304",
      "title":"Culture and Recreation"
    },
    {
      "course_id":"012750",
      "subject":"REC",
      "catalog_number":"306",
      "title":"Contemporary Health Issues for Women"
    },
    {
      "course_id":"008136",
      "subject":"REC",
      "catalog_number":"309",
      "title":"History and Philosophy of Leisure"
    },
    {
      "course_id":"013882",
      "subject":"REC",
      "catalog_number":"311",
      "title":"Event Management"
    },
    {
      "course_id":"013954",
      "subject":"REC",
      "catalog_number":"312",
      "title":"Practicum in Recreation, Sport, and Tourism"
    },
    {
      "course_id":"015115",
      "subject":"REC",
      "catalog_number":"372",
      "title":"Special Topics in Leisure Studies 3"
    },
    {
      "course_id":"009928",
      "subject":"REC",
      "catalog_number":"314",
      "title":"Quality Assurance in Recreation and Sport Services"
    },
    {
      "course_id":"010161",
      "subject":"REC",
      "catalog_number":"316",
      "title":"Financing Recreation and Sport Services"
    },
    {
      "course_id":"005919",
      "subject":"REC",
      "catalog_number":"333",
      "title":"Recreation Geography"
    },
    {
      "course_id":"005274",
      "subject":"REC",
      "catalog_number":"334",
      "title":"Introduction to Park Management"
    },
    {
      "course_id":"013581",
      "subject":"REC",
      "catalog_number":"351",
      "title":"Therapeutic Recreation Facilitation Techniques"
    },
    {
      "course_id":"008170",
      "subject":"REC",
      "catalog_number":"354",
      "title":"Leisure Education - Concepts and Practices"
    },
    {
      "course_id":"008172",
      "subject":"REC",
      "catalog_number":"356",
      "title":"Recreation and Community Development"
    },
    {
      "course_id":"014697",
      "subject":"REC",
      "catalog_number":"357",
      "title":"Theories and Evidence for Therapeutic Recreation Practice"
    },
    {
      "course_id":"008173",
      "subject":"REC",
      "catalog_number":"361",
      "title":"Aging and Leisure"
    },
    {
      "course_id":"006438",
      "subject":"REC",
      "catalog_number":"362",
      "title":"Sociology of Aging"
    },
    {
      "course_id":"008188",
      "subject":"REC",
      "catalog_number":"371",
      "title":"Statistical Techniques Applied to Leisure Studies"
    },
    {
      "course_id":"010028",
      "subject":"REC",
      "catalog_number":"375",
      "title":"International Exchange"
    },
    {
      "course_id":"008194",
      "subject":"REC",
      "catalog_number":"380",
      "title":"Tourism Analysis"
    },
    {
      "course_id":"005912",
      "subject":"REC",
      "catalog_number":"383",
      "title":"Perspectives on International Tourism"
    },
    {
      "course_id":"012215",
      "subject":"REC",
      "catalog_number":"401",
      "title":"Advanced Seminar on the Socio-Cultural and Behavioral Dimensions of Leisure"
    },
    {
      "course_id":"011560",
      "subject":"REC",
      "catalog_number":"405",
      "title":"Leisure and Well-Being"
    },
    {
      "course_id":"008200",
      "subject":"REC",
      "catalog_number":"408",
      "title":"Gender and Leisure"
    },
    {
      "course_id":"008203",
      "subject":"REC",
      "catalog_number":"413",
      "title":"Advanced Seminar in Recreation and Sport Business"
    },
    {
      "course_id":"008205",
      "subject":"REC",
      "catalog_number":"415",
      "title":"Consumer Research in Recreation and Sport Services"
    },
    {
      "course_id":"008206",
      "subject":"REC",
      "catalog_number":"416",
      "title":"Principles of Recreation Planning"
    },
    {
      "course_id":"008207",
      "subject":"REC",
      "catalog_number":"420",
      "title":"Program Evaluation in Leisure Services"
    },
    {
      "course_id":"012120",
      "subject":"REC",
      "catalog_number":"422",
      "title":"Urban Recreation"
    },
    {
      "course_id":"008208",
      "subject":"REC",
      "catalog_number":"425",
      "title":"Heritage Planning Workshop"
    },
    {
      "course_id":"005299",
      "subject":"REC",
      "catalog_number":"433",
      "title":"Ecotourism and Park Tourism"
    },
    {
      "course_id":"012661",
      "subject":"REC",
      "catalog_number":"437",
      "title":"Ecosystem and Resource Management in Parks\/Natural Areas"
    },
    {
      "course_id":"008216",
      "subject":"REC",
      "catalog_number":"450A",
      "title":"Internship for Therapeutic Recreation"
    },
    {
      "course_id":"013883",
      "subject":"REC",
      "catalog_number":"450B",
      "title":"Internship for Therapeutic Recreation"
    },
    {
      "course_id":"008217",
      "subject":"REC",
      "catalog_number":"455",
      "title":"Advanced Seminar in Therapeutic Recreation"
    },
    {
      "course_id":"008220",
      "subject":"REC",
      "catalog_number":"471A",
      "title":"Honours Thesis"
    },
    {
      "course_id":"008221",
      "subject":"REC",
      "catalog_number":"471B",
      "title":"Honours Thesis"
    },
    {
      "course_id":"011561",
      "subject":"REC",
      "catalog_number":"472",
      "title":"Special Topics in Recreation and Leisure Studies 4"
    },
    {
      "course_id":"009509",
      "subject":"REC",
      "catalog_number":"475",
      "title":"Directed Study in Special Topics"
    },
    {
      "course_id":"008235",
      "subject":"REC",
      "catalog_number":"480",
      "title":"Advanced Seminar in Tourism Development"
    },
    {
      "course_id":"002892",
      "subject":"REC",
      "catalog_number":"600",
      "title":"Integrative Seminar in Recreation and Leisure Studies"
    },
    {
      "course_id":"002893",
      "subject":"REC",
      "catalog_number":"601",
      "title":"Epistemological and Methodological Issues in Leisure Research"
    },
    {
      "course_id":"002895",
      "subject":"REC",
      "catalog_number":"603",
      "title":"Leisure and Social Policy"
    },
    {
      "course_id":"011668",
      "subject":"REC",
      "catalog_number":"605",
      "title":"Social and Psychological Analysis of Leisure"
    },
    {
      "course_id":"002897",
      "subject":"REC",
      "catalog_number":"608",
      "title":"Seminar in Gender and Leisure"
    },
    {
      "course_id":"002898",
      "subject":"REC",
      "catalog_number":"609",
      "title":"Internship in Recreation Service"
    },
    {
      "course_id":"002899",
      "subject":"REC",
      "catalog_number":"610",
      "title":"Administrative Practice in Recreational Service"
    },
    {
      "course_id":"002900",
      "subject":"REC",
      "catalog_number":"615",
      "title":"Consumer Research and Marketing Leisure Services"
    },
    {
      "course_id":"002901",
      "subject":"REC",
      "catalog_number":"630",
      "title":"Policy and Planning of Nature-based Recreation and Tourism"
    },
    {
      "course_id":"002902",
      "subject":"REC",
      "catalog_number":"640",
      "title":"Community Development, Capacity Building and Leisure"
    },
    {
      "course_id":"002903",
      "subject":"REC",
      "catalog_number":"650",
      "title":"Critical Reflections on Disability, Illness and Leisure"
    },
    {
      "course_id":"014354",
      "subject":"REC",
      "catalog_number":"651",
      "title":"Philosophical Foundations of Therapeutic Recreation"
    },
    {
      "course_id":"014355",
      "subject":"REC",
      "catalog_number":"652",
      "title":"Knowledge-Based Practice in Therapeutic Recreation"
    },
    {
      "course_id":"002904",
      "subject":"REC",
      "catalog_number":"672",
      "title":"Quantitative Research Data Analysis and Interpretation"
    },
    {
      "course_id":"002905",
      "subject":"REC",
      "catalog_number":"673",
      "title":"Qualitative Research Data Analysis and Interpretation"
    },
    {
      "course_id":"002906",
      "subject":"REC",
      "catalog_number":"680",
      "title":"The Dynamics of Tourism"
    },
    {
      "course_id":"011082",
      "subject":"REC",
      "catalog_number":"685",
      "title":"The Structure of Tourism"
    },
    {
      "course_id":"013062",
      "subject":"RUSS",
      "catalog_number":"611",
      "title":"Topics in Second Language Acquisition and Computer-Assisted Language Learning"
    },
    {
      "course_id":"002908",
      "subject":"REC",
      "catalog_number":"695",
      "title":"Selected Topics in Leisure Behaviour and Cultural Studies"
    },
    {
      "course_id":"013072",
      "subject":"RUSS",
      "catalog_number":"604",
      "title":"Approaches to Film and Performance Theory"
    },
    {
      "course_id":"009478",
      "subject":"REC",
      "catalog_number":"696",
      "title":"Topics in Administration and Management for Services"
    },
    {
      "course_id":"002952",
      "subject":"REC",
      "catalog_number":"697",
      "title":"Selected Topics in Recreation and Leisure Resources"
    },
    {
      "course_id":"002969",
      "subject":"REC",
      "catalog_number":"700",
      "title":"Foundations of Knowledge in Leisure Studies"
    },
    {
      "course_id":"013139",
      "subject":"REC",
      "catalog_number":"730",
      "title":"Fundamentals of Work and Health"
    },
    {
      "course_id":"013140",
      "subject":"REC",
      "catalog_number":"731",
      "title":"Approaches to Research in Work and Health"
    },
    {
      "course_id":"013141",
      "subject":"REC",
      "catalog_number":"732A",
      "title":"Work and Health Research Seminar (I)"
    },
    {
      "course_id":"013142",
      "subject":"REC",
      "catalog_number":"732B",
      "title":"Work and Health Research Seminar (II)"
    },
    {
      "course_id":"012422",
      "subject":"REC",
      "catalog_number":"750",
      "title":"Fundamentals of Aging, Health and Well-being"
    },
    {
      "course_id":"012426",
      "subject":"REC",
      "catalog_number":"751",
      "title":"Aging, Health and Well-being Research Seminar"
    },
    {
      "course_id":"002970",
      "subject":"REC",
      "catalog_number":"792",
      "title":"Advanced Research Methods"
    },
    {
      "course_id":"002997",
      "subject":"RUSS",
      "catalog_number":"601",
      "title":"Approaches to Linguistics"
    },
    {
      "course_id":"010424",
      "subject":"RUSS",
      "catalog_number":"602",
      "title":"Approaches to Literary and Cultural Theory"
    },
    {
      "course_id":"009479",
      "subject":"REC",
      "catalog_number":"798",
      "title":"Advanced Topics in Leisure Studies"
    },
    {
      "course_id":"013878",
      "subject":"REES",
      "catalog_number":"100",
      "title":"Legendary Past: Russian Myths and Heroes"
    },
    {
      "course_id":"013630",
      "subject":"REES",
      "catalog_number":"180",
      "title":"German and Russian Literary Masterpieces"
    },
    {
      "course_id":"013653",
      "subject":"REES",
      "catalog_number":"220",
      "title":"Once Upon a Fairy Tale: Fairy Tales, Then and Now"
    },
    {
      "course_id":"012445",
      "subject":"REES",
      "catalog_number":"230",
      "title":"The Devil"
    },
    {
      "course_id":"012446",
      "subject":"REES",
      "catalog_number":"260",
      "title":"Special Topics"
    },
    {
      "course_id":"013008",
      "subject":"REES",
      "catalog_number":"261",
      "title":"Languages and Society I"
    },
    {
      "course_id":"013009",
      "subject":"REES",
      "catalog_number":"262",
      "title":"Languages and Society II"
    },
    {
      "course_id":"008446",
      "subject":"REES",
      "catalog_number":"271",
      "title":"Russian Thought and Culture"
    },
    {
      "course_id":"008447",
      "subject":"REES",
      "catalog_number":"272",
      "title":"Russian Thought and Culture"
    },
    {
      "course_id":"004353",
      "subject":"REES",
      "catalog_number":"273",
      "title":"Croatian Culture and Literature"
    },
    {
      "course_id":"004355",
      "subject":"REES",
      "catalog_number":"274",
      "title":"Croatian Culture and Literature"
    },
    {
      "course_id":"013877",
      "subject":"REES",
      "catalog_number":"280",
      "title":"Comparative Literature: Theory and Practice"
    },
    {
      "course_id":"011198",
      "subject":"REES",
      "catalog_number":"281",
      "title":"Women in Russia: The Conscience of a Nation"
    },
    {
      "course_id":"012444",
      "subject":"REES",
      "catalog_number":"310",
      "title":"Russian Folklore"
    },
    {
      "course_id":"012457",
      "subject":"REES",
      "catalog_number":"320",
      "title":"The Slavic Short Story"
    },
    {
      "course_id":"012449",
      "subject":"REES",
      "catalog_number":"330",
      "title":"Russian Politics through Literature"
    },
    {
      "course_id":"008456",
      "subject":"REES",
      "catalog_number":"341",
      "title":"Russian Drama before 1905"
    },
    {
      "course_id":"008457",
      "subject":"REES",
      "catalog_number":"342",
      "title":"Russian Drama after 1905"
    },
    {
      "course_id":"012448",
      "subject":"REES",
      "catalog_number":"360",
      "title":"Special Topics"
    },
    {
      "course_id":"013636",
      "subject":"REES",
      "catalog_number":"364",
      "title":"German and Russian Film Pioneers"
    },
    {
      "course_id":"013650",
      "subject":"REES",
      "catalog_number":"385",
      "title":"Culture Behind the Iron Curtain"
    },
    {
      "course_id":"012634",
      "subject":"REES",
      "catalog_number":"420",
      "title":"Topics in Language Pedagogy"
    },
    {
      "course_id":"012451",
      "subject":"REES",
      "catalog_number":"460",
      "title":"Special Topics"
    },
    {
      "course_id":"012447",
      "subject":"REES",
      "catalog_number":"490",
      "title":"Senior Honours Project"
    },
    {
      "course_id":"008480",
      "subject":"REES",
      "catalog_number":"495",
      "title":"Reading Course in Approved Topics"
    },
    {
      "course_id":"008479",
      "subject":"REES",
      "catalog_number":"496",
      "title":"Study Abroad"
    },
    {
      "course_id":"008280",
      "subject":"RS",
      "catalog_number":"100",
      "title":"Religions of the East"
    },
    {
      "course_id":"008281",
      "subject":"RS",
      "catalog_number":"110",
      "title":"Religions of the West"
    },
    {
      "course_id":"010108",
      "subject":"RS",
      "catalog_number":"111",
      "title":"Relationships in the Bible (Old Testament)"
    },
    {
      "course_id":"010109",
      "subject":"RS",
      "catalog_number":"112",
      "title":"Power and Corruption in the Bible (Old Testament)"
    },
    {
      "course_id":"010119",
      "subject":"RS",
      "catalog_number":"113",
      "title":"The Quest for Meaning in Modern Judaism"
    },
    {
      "course_id":"010215",
      "subject":"RS",
      "catalog_number":"121",
      "title":"Evil"
    },
    {
      "course_id":"009532",
      "subject":"RS",
      "catalog_number":"122",
      "title":"Sacred Beauty: Religion and the Arts"
    },
    {
      "course_id":"013308",
      "subject":"RS",
      "catalog_number":"125",
      "title":"What is Religion?"
    },
    {
      "course_id":"012721",
      "subject":"RS",
      "catalog_number":"130",
      "title":"Big Ideas of the Bible"
    },
    {
      "course_id":"008290",
      "subject":"RS",
      "catalog_number":"131",
      "title":"Classical Hebrew 1"
    },
    {
      "course_id":"008291",
      "subject":"RS",
      "catalog_number":"132",
      "title":"Classical Hebrew 2"
    },
    {
      "course_id":"008292",
      "subject":"RS",
      "catalog_number":"133",
      "title":"New Testament Greek 1"
    },
    {
      "course_id":"008293",
      "subject":"RS",
      "catalog_number":"134",
      "title":"New Testament Greek 2"
    },
    {
      "course_id":"008283",
      "subject":"RS",
      "catalog_number":"150",
      "title":"Christian Ethics"
    },
    {
      "course_id":"008286",
      "subject":"RS",
      "catalog_number":"151",
      "title":"Roman Catholicism"
    },
    {
      "course_id":"008287",
      "subject":"RS",
      "catalog_number":"152",
      "title":"Introduction to Christian Theology"
    },
    {
      "course_id":"011863",
      "subject":"RS",
      "catalog_number":"170",
      "title":"Religion and Popular Culture"
    },
    {
      "course_id":"008288",
      "subject":"RS",
      "catalog_number":"180",
      "title":"Love and Friendship"
    },
    {
      "course_id":"004872",
      "subject":"RS",
      "catalog_number":"201",
      "title":"Religion in East Asia"
    },
    {
      "course_id":"010217",
      "subject":"RS",
      "catalog_number":"202",
      "title":"Sikhism"
    },
    {
      "course_id":"008304",
      "subject":"RS",
      "catalog_number":"203",
      "title":"Hinduism"
    },
    {
      "course_id":"008305",
      "subject":"RS",
      "catalog_number":"204",
      "title":"Buddhism"
    },
    {
      "course_id":"008306",
      "subject":"RS",
      "catalog_number":"205",
      "title":"Buddhism in Tibet"
    },
    {
      "course_id":"012997",
      "subject":"RS",
      "catalog_number":"206",
      "title":"Japanese Religions"
    },
    {
      "course_id":"012998",
      "subject":"RS",
      "catalog_number":"207",
      "title":"Chinese Religions"
    },
    {
      "course_id":"008308",
      "subject":"RS",
      "catalog_number":"210",
      "title":"Judaism"
    },
    {
      "course_id":"011635",
      "subject":"RS",
      "catalog_number":"211",
      "title":"Jewish Responses to the Holocaust"
    },
    {
      "course_id":"010110",
      "subject":"RS",
      "catalog_number":"212",
      "title":"Great Texts in the Jewish Tradition"
    },
    {
      "course_id":"012171",
      "subject":"RS",
      "catalog_number":"213",
      "title":"Kabbalah: Jewish Mysticism"
    },
    {
      "course_id":"010111",
      "subject":"RS",
      "catalog_number":"214",
      "title":"Jewish Philosophy"
    },
    {
      "course_id":"011983",
      "subject":"RS",
      "catalog_number":"215",
      "title":"Special Topics"
    },
    {
      "course_id":"008307",
      "subject":"RS",
      "catalog_number":"216",
      "title":"Islam"
    },
    {
      "course_id":"013902",
      "subject":"RS",
      "catalog_number":"217",
      "title":"Islam in North America"
    },
    {
      "course_id":"008310",
      "subject":"RS",
      "catalog_number":"219",
      "title":"Religion in America"
    },
    {
      "course_id":"011866",
      "subject":"RS",
      "catalog_number":"220",
      "title":"World Religions and Politics"
    },
    {
      "course_id":"012722",
      "subject":"RS",
      "catalog_number":"221",
      "title":"Global Religious Fundamentalism"
    },
    {
      "course_id":"008340",
      "subject":"RS",
      "catalog_number":"222",
      "title":"Sacred Places"
    },
    {
      "course_id":"012723",
      "subject":"RS",
      "catalog_number":"223",
      "title":"Sacred Words and Sacred Texts"
    },
    {
      "course_id":"014248",
      "subject":"RS",
      "catalog_number":"230",
      "title":"Visions of Israel in Judaism: From Biblical to Modern Times"
    },
    {
      "course_id":"008297",
      "subject":"RS",
      "catalog_number":"232",
      "title":"The Hebrew Prophets"
    },
    {
      "course_id":"008363",
      "subject":"RS",
      "catalog_number":"233",
      "title":"Intermediate New Testament Greek"
    },
    {
      "course_id":"008364",
      "subject":"RS",
      "catalog_number":"234",
      "title":"Hellenistic Greek"
    },
    {
      "course_id":"008298",
      "subject":"RS",
      "catalog_number":"235",
      "title":"Jesus: Life and Legacy"
    },
    {
      "course_id":"008301",
      "subject":"RS",
      "catalog_number":"236",
      "title":"Paul: Life and Letters"
    },
    {
      "course_id":"012724",
      "subject":"RS",
      "catalog_number":"237",
      "title":"Insiders and Outsiders in the Bible"
    },
    {
      "course_id":"008318",
      "subject":"RS",
      "catalog_number":"240",
      "title":"History of Christianity"
    },
    {
      "course_id":"008323",
      "subject":"RS",
      "catalog_number":"245",
      "title":"The Catholic Church in Canada"
    },
    {
      "course_id":"010112",
      "subject":"RS",
      "catalog_number":"248",
      "title":"The Anglican Tradition"
    },
    {
      "course_id":"008319",
      "subject":"RS",
      "catalog_number":"250",
      "title":"History of Christian Thought"
    },
    {
      "course_id":"008315",
      "subject":"RS",
      "catalog_number":"251",
      "title":"Catholic Social Thought"
    },
    {
      "course_id":"010218",
      "subject":"RS",
      "catalog_number":"252",
      "title":"Religious Responses to Political Oppression"
    },
    {
      "course_id":"008348",
      "subject":"RS",
      "catalog_number":"253",
      "title":"Women and the Church"
    },
    {
      "course_id":"008324",
      "subject":"RS",
      "catalog_number":"254",
      "title":"Christian Sexual Ethics"
    },
    {
      "course_id":"008343",
      "subject":"RS",
      "catalog_number":"255",
      "title":"Gospel and Liberation"
    },
    {
      "course_id":"008329",
      "subject":"RS",
      "catalog_number":"256",
      "title":"Christian Approaches to Peacemaking"
    },
    {
      "course_id":"012201",
      "subject":"RS",
      "catalog_number":"257",
      "title":"Eastern Christianity: Being God and Human"
    },
    {
      "course_id":"008296",
      "subject":"RS",
      "catalog_number":"258",
      "title":"God"
    },
    {
      "course_id":"008295",
      "subject":"RS",
      "catalog_number":"260",
      "title":"How to Study Religion"
    },
    {
      "course_id":"007281",
      "subject":"RS",
      "catalog_number":"261",
      "title":"Introduction to the Philosophy of Religion"
    },
    {
      "course_id":"008309",
      "subject":"RS",
      "catalog_number":"262",
      "title":"Religion in Sociological Perspective"
    },
    {
      "course_id":"005468",
      "subject":"RS",
      "catalog_number":"270R",
      "title":"Religion in Popular Film"
    },
    {
      "course_id":"005469",
      "subject":"RS",
      "catalog_number":"271R",
      "title":"Thematic Approaches to Religion in Film"
    },
    {
      "course_id":"011636",
      "subject":"RS",
      "catalog_number":"272",
      "title":"The Holocaust and Film"
    },
    {
      "course_id":"010219",
      "subject":"RS",
      "catalog_number":"273",
      "title":"Religion and the Media"
    },
    {
      "course_id":"014245",
      "subject":"RS",
      "catalog_number":"275",
      "title":"Religion and Japanese Film"
    },
    {
      "course_id":"008312",
      "subject":"RS",
      "catalog_number":"280",
      "title":"Cults and New Religious Movements"
    },
    {
      "course_id":"008311",
      "subject":"RS",
      "catalog_number":"281",
      "title":"Millennialism & Violence"
    },
    {
      "course_id":"008313",
      "subject":"RS",
      "catalog_number":"282",
      "title":"Christian Fundamentalism"
    },
    {
      "course_id":"008328",
      "subject":"RS",
      "catalog_number":"283",
      "title":"Current Ethical Issues"
    },
    {
      "course_id":"008331",
      "subject":"RS",
      "catalog_number":"284",
      "title":"Women and the Great Religions"
    },
    {
      "course_id":"010224",
      "subject":"RS",
      "catalog_number":"285",
      "title":"The Sacred Earth: Religion and Ecology"
    },
    {
      "course_id":"008357",
      "subject":"RS",
      "catalog_number":"286",
      "title":"Spirit in Motion: Secular and Religious Spiritualities Today"
    },
    {
      "course_id":"010239",
      "subject":"RS",
      "catalog_number":"291",
      "title":"Special Topics"
    },
    {
      "course_id":"012999",
      "subject":"RS",
      "catalog_number":"301",
      "title":"Pure Land Buddhism"
    },
    {
      "course_id":"012265",
      "subject":"RS",
      "catalog_number":"302",
      "title":"Images of the Feminine: India"
    },
    {
      "course_id":"012268",
      "subject":"RS",
      "catalog_number":"303",
      "title":"Gender and Asian Religions"
    },
    {
      "course_id":"012263",
      "subject":"RS",
      "catalog_number":"304",
      "title":"Zen and Now: History and Influence of Zen"
    },
    {
      "course_id":"014249",
      "subject":"RS",
      "catalog_number":"310",
      "title":"Jews in the New World"
    },
    {
      "course_id":"013095",
      "subject":"RS",
      "catalog_number":"313",
      "title":"Moses Maimonides: Life and Thought"
    },
    {
      "course_id":"009533",
      "subject":"RS",
      "catalog_number":"314",
      "title":"Islam and Christianity"
    },
    {
      "course_id":"004290",
      "subject":"RS",
      "catalog_number":"315",
      "title":"Greek and Roman Religion"
    },
    {
      "course_id":"010156",
      "subject":"RS",
      "catalog_number":"318",
      "title":"Canadian Native Religious Traditions"
    },
    {
      "course_id":"011607",
      "subject":"RS",
      "catalog_number":"319",
      "title":"Religion in Canada"
    },
    {
      "course_id":"011659",
      "subject":"RS",
      "catalog_number":"320",
      "title":"East Comes West, West Turns East"
    },
    {
      "course_id":"012264",
      "subject":"RS",
      "catalog_number":"321",
      "title":"Women in Buddhism: A Global Perspective"
    },
    {
      "course_id":"008400",
      "subject":"RS",
      "catalog_number":"322",
      "title":"Interreligious Encounter and Dialogue"
    },
    {
      "course_id":"011868",
      "subject":"RS",
      "catalog_number":"323",
      "title":"Religious Ethics and Global Politics"
    },
    {
      "course_id":"008411",
      "subject":"RS",
      "catalog_number":"324",
      "title":"Religious Perspectives on Marriage and Family"
    },
    {
      "course_id":"012739",
      "subject":"RS",
      "catalog_number":"325",
      "title":"Sex and the World Religions"
    },
    {
      "course_id":"012725",
      "subject":"RS",
      "catalog_number":"326",
      "title":"Global Christianity"
    },
    {
      "course_id":"013000",
      "subject":"RS",
      "catalog_number":"327",
      "title":"Buddhism in North America"
    },
    {
      "course_id":"010223",
      "subject":"RS",
      "catalog_number":"330",
      "title":"Selected Topics in Biblical Studies"
    },
    {
      "course_id":"008365",
      "subject":"RS",
      "catalog_number":"331",
      "title":"Intermediate Classical Hebrew"
    },
    {
      "course_id":"008366",
      "subject":"RS",
      "catalog_number":"332",
      "title":"Ancient Semitic Texts and Inscriptions"
    },
    {
      "course_id":"008398",
      "subject":"RS",
      "catalog_number":"337",
      "title":"The Bible and Peace"
    },
    {
      "course_id":"012720",
      "subject":"RS",
      "catalog_number":"338",
      "title":"Seeking Wisdom in the Bible"
    },
    {
      "course_id":"012959",
      "subject":"RS",
      "catalog_number":"339",
      "title":"The Bible (Old Testament) and Archaeology"
    },
    {
      "course_id":"013232",
      "subject":"RS",
      "catalog_number":"341",
      "title":"Jewish Contributions to Political Thought"
    },
    {
      "course_id":"008378",
      "subject":"RS",
      "catalog_number":"342",
      "title":"Heresy and Religious Crises in Late Medieval Europe"
    },
    {
      "course_id":"006380",
      "subject":"RS",
      "catalog_number":"343",
      "title":"Reformation History"
    },
    {
      "course_id":"008377",
      "subject":"RS",
      "catalog_number":"344",
      "title":"The Radical Reformation"
    },
    {
      "course_id":"008384",
      "subject":"RS",
      "catalog_number":"348",
      "title":"Vatican II"
    },
    {
      "course_id":"008390",
      "subject":"RS",
      "catalog_number":"350",
      "title":"Modern Christian Thought"
    },
    {
      "course_id":"008391",
      "subject":"RS",
      "catalog_number":"351",
      "title":"Contemporary Christian Thought"
    },
    {
      "course_id":"008399",
      "subject":"RS",
      "catalog_number":"353",
      "title":"War and Peace in Christian Theology"
    },
    {
      "course_id":"008412",
      "subject":"RS",
      "catalog_number":"354",
      "title":"Shapers of the Roman Catholic Tradition"
    },
    {
      "course_id":"008381",
      "subject":"RS",
      "catalog_number":"355",
      "title":"Christian Feminist Thought"
    },
    {
      "course_id":"007051",
      "subject":"RS",
      "catalog_number":"357",
      "title":"Christian Hymnody"
    },
    {
      "course_id":"007052",
      "subject":"RS",
      "catalog_number":"358",
      "title":"Worship and Music"
    },
    {
      "course_id":"014005",
      "subject":"RS",
      "catalog_number":"370",
      "title":"Atheism, Skepticism, and Free Thought"
    },
    {
      "course_id":"013334",
      "subject":"RS",
      "catalog_number":"374",
      "title":"Religious Quests"
    },
    {
      "course_id":"012205",
      "subject":"RS",
      "catalog_number":"375",
      "title":"Icons in Eastern Christianity: Windows to Heaven"
    },
    {
      "course_id":"012189",
      "subject":"RS",
      "catalog_number":"380",
      "title":"Religion and Peace-Building"
    },
    {
      "course_id":"008397",
      "subject":"RS",
      "catalog_number":"381",
      "title":"Religious Perspectives on the Environmental Crisis"
    },
    {
      "course_id":"010222",
      "subject":"RS",
      "catalog_number":"382",
      "title":"Bioethics and Religious Values"
    },
    {
      "course_id":"008332",
      "subject":"RS",
      "catalog_number":"383",
      "title":"Justice, Peace, and Development"
    },
    {
      "course_id":"010229",
      "subject":"RS",
      "catalog_number":"391",
      "title":"Special Topics"
    },
    {
      "course_id":"010226",
      "subject":"RS",
      "catalog_number":"395",
      "title":"Study-Travel Seminar in Religion"
    },
    {
      "course_id":"008417",
      "subject":"RS",
      "catalog_number":"398",
      "title":"Directed Readings in Special Subjects"
    },
    {
      "course_id":"010232",
      "subject":"RS",
      "catalog_number":"462",
      "title":"Sociology of Religion"
    },
    {
      "course_id":"012734",
      "subject":"RS",
      "catalog_number":"482",
      "title":"Religion, Science, and Technology"
    },
    {
      "course_id":"010231",
      "subject":"RS",
      "catalog_number":"491",
      "title":"Special Topics"
    },
    {
      "course_id":"010729",
      "subject":"RS",
      "catalog_number":"495",
      "title":"Study Term Abroad"
    },
    {
      "course_id":"012735",
      "subject":"RS",
      "catalog_number":"498",
      "title":"Directed Readings in Special Subjects"
    },
    {
      "course_id":"012736",
      "subject":"RS",
      "catalog_number":"499",
      "title":"Senior Seminar"
    },
    {
      "course_id":"012010",
      "subject":"RS",
      "catalog_number":"700",
      "title":"Religious Diversity in North America"
    },
    {
      "course_id":"012011",
      "subject":"RS",
      "catalog_number":"701",
      "title":"Case Studies in Religion"
    },
    {
      "course_id":"012012",
      "subject":"RS",
      "catalog_number":"703",
      "title":"Directed Study"
    },
    {
      "course_id":"002996",
      "subject":"RUSS",
      "catalog_number":"600",
      "title":"Methods of Research"
    },
    {
      "course_id":"012013",
      "subject":"RS",
      "catalog_number":"704",
      "title":"Special Topics"
    },
    {
      "course_id":"014221",
      "subject":"RS",
      "catalog_number":"705",
      "title":"History of Religion in North America"
    },
    {
      "course_id":"014303",
      "subject":"RS",
      "catalog_number":"710",
      "title":"Approaches to the Study of Religion in North America"
    },
    {
      "course_id":"003051",
      "subject":"RS",
      "catalog_number":"730",
      "title":"Sociology of Religion"
    },
    {
      "course_id":"008434",
      "subject":"RUSS",
      "catalog_number":"101",
      "title":"Elementary Russian I"
    },
    {
      "course_id":"008436",
      "subject":"RUSS",
      "catalog_number":"102",
      "title":"Elementary Russian II"
    },
    {
      "course_id":"008442",
      "subject":"RUSS",
      "catalog_number":"201",
      "title":"Intermediate Russian I"
    },
    {
      "course_id":"008521",
      "subject":"SCI",
      "catalog_number":"263",
      "title":"Science and Society"
    },
    {
      "course_id":"008443",
      "subject":"RUSS",
      "catalog_number":"202",
      "title":"Intermediate Russian II"
    },
    {
      "course_id":"013880",
      "subject":"RUSS",
      "catalog_number":"203",
      "title":"Integrative Language Studies I"
    },
    {
      "course_id":"013879",
      "subject":"RUSS",
      "catalog_number":"204",
      "title":"Russian for Heritage Speakers"
    },
    {
      "course_id":"008458",
      "subject":"RUSS",
      "catalog_number":"301",
      "title":"Advanced Russian I"
    },
    {
      "course_id":"008459",
      "subject":"RUSS",
      "catalog_number":"302",
      "title":"Advanced Russian II"
    },
    {
      "course_id":"013881",
      "subject":"RUSS",
      "catalog_number":"303",
      "title":"Integrative Language Studies II"
    },
    {
      "course_id":"002998",
      "subject":"RUSS",
      "catalog_number":"603",
      "title":"Approaches to Language Didactics"
    },
    {
      "course_id":"013068",
      "subject":"RUSS",
      "catalog_number":"622",
      "title":"Topics in Soviet and Post-Soviet Literature"
    },
    {
      "course_id":"012255",
      "subject":"SCBUS",
      "catalog_number":"122",
      "title":"Management of Business Organizations"
    },
    {
      "course_id":"008507",
      "subject":"SCBUS",
      "catalog_number":"123",
      "title":"Science & Business Workshop 1"
    },
    {
      "course_id":"008512",
      "subject":"SCBUS",
      "catalog_number":"223",
      "title":"Science and Business Workshop 2"
    },
    {
      "course_id":"012665",
      "subject":"SCBUS",
      "catalog_number":"225",
      "title":"Organizational Behaviour and Human Decision Processes Workshop"
    },
    {
      "course_id":"008526",
      "subject":"SCBUS",
      "catalog_number":"323",
      "title":"Technology Development Workshop 3"
    },
    {
      "course_id":"010041",
      "subject":"SCBUS",
      "catalog_number":"423",
      "title":"Senior Honours Science and Business Workshop 4"
    },
    {
      "course_id":"012256",
      "subject":"SCBUS",
      "catalog_number":"424",
      "title":"Science & Business Workshop 5"
    },
    {
      "course_id":"012257",
      "subject":"SCBUS",
      "catalog_number":"425",
      "title":"Science & Business Workshop 6"
    },
    {
      "course_id":"013620",
      "subject":"SCI",
      "catalog_number":"200",
      "title":"Energy - Its Development, Use and Issues"
    },
    {
      "course_id":"014123",
      "subject":"SCI",
      "catalog_number":"201",
      "title":"Global Warming and Climate Change"
    },
    {
      "course_id":"008508",
      "subject":"SCI",
      "catalog_number":"205",
      "title":"Physics of High Fidelity Sound Reproduction"
    },
    {
      "course_id":"010135",
      "subject":"SCI",
      "catalog_number":"206",
      "title":"The Physics of How Things Work"
    },
    {
      "course_id":"013362",
      "subject":"SCI",
      "catalog_number":"227",
      "title":"Chemistry in Society: Yesterday, Today and Tomorrow"
    },
    {
      "course_id":"008513",
      "subject":"SCI",
      "catalog_number":"237",
      "title":"Exploring the Universe"
    },
    {
      "course_id":"008514",
      "subject":"SCI",
      "catalog_number":"238",
      "title":"Introductory Astronomy"
    },
    {
      "course_id":"008515",
      "subject":"SCI",
      "catalog_number":"250",
      "title":"Environmental Geology"
    },
    {
      "course_id":"006156",
      "subject":"SCI",
      "catalog_number":"255",
      "title":"The Biology of Aging"
    },
    {
      "course_id":"008523",
      "subject":"SCI",
      "catalog_number":"267",
      "title":"Introduction to the Philosophy of Science"
    },
    {
      "course_id":"010366",
      "subject":"SCI",
      "catalog_number":"395",
      "title":"Science Study Abroad Program"
    },
    {
      "course_id":"010367",
      "subject":"SCI",
      "catalog_number":"396",
      "title":"Science Study Abroad Program"
    },
    {
      "course_id":"010368",
      "subject":"SCI",
      "catalog_number":"397",
      "title":"Science Study Abroad Program"
    },
    {
      "course_id":"011759",
      "subject":"SCI",
      "catalog_number":"455",
      "title":"Human Impact on Aquatic Systems"
    },
    {
      "course_id":"008536",
      "subject":"SCI",
      "catalog_number":"462",
      "title":"Biology of Food Production"
    },
    {
      "course_id":"006501",
      "subject":"SDS",
      "catalog_number":"131R",
      "title":"Social Ideas, Social Policy and Political Practice"
    },
    {
      "course_id":"006502",
      "subject":"SDS",
      "catalog_number":"150R",
      "title":"Lifespan Processes: The Normal Events"
    },
    {
      "course_id":"013734",
      "subject":"SDS",
      "catalog_number":"205R",
      "title":"History of Education in Canada"
    },
    {
      "course_id":"014137",
      "subject":"SDS",
      "catalog_number":"210R",
      "title":"Children's Rights in Canada"
    },
    {
      "course_id":"013735",
      "subject":"SDS",
      "catalog_number":"215R",
      "title":"Education and Social Development from a Global Perspective"
    },
    {
      "course_id":"006503",
      "subject":"SDS",
      "catalog_number":"220R",
      "title":"Changing Concepts of Childhood"
    },
    {
      "course_id":"013893",
      "subject":"SDS",
      "catalog_number":"231R",
      "title":"Introduction to Social Policy Processes"
    },
    {
      "course_id":"006504",
      "subject":"SDS",
      "catalog_number":"240R",
      "title":"Art and Society"
    },
    {
      "course_id":"006507",
      "subject":"SDS",
      "catalog_number":"250R",
      "title":"Social Statistics"
    },
    {
      "course_id":"006508",
      "subject":"SDS",
      "catalog_number":"251R",
      "title":"Social Research"
    },
    {
      "course_id":"011378",
      "subject":"SDS",
      "catalog_number":"311R",
      "title":"Public Policy and Native Peoples in Canada"
    },
    {
      "course_id":"011979",
      "subject":"SDS",
      "catalog_number":"312R",
      "title":"Homelessness & Public Policy"
    },
    {
      "course_id":"013894",
      "subject":"SDS",
      "catalog_number":"331R",
      "title":"Social Inequality, Social Justice, and Public Policy"
    },
    {
      "course_id":"006510",
      "subject":"SDS",
      "catalog_number":"350R",
      "title":"Adult Life Crises and Events"
    },
    {
      "course_id":"013736",
      "subject":"SDS",
      "catalog_number":"351R",
      "title":"Qualitative Research in Social Development Studies"
    },
    {
      "course_id":"011390",
      "subject":"SDS",
      "catalog_number":"353R",
      "title":"The Evolution of Family Law in Canadian Society"
    },
    {
      "course_id":"006513",
      "subject":"SDS",
      "catalog_number":"354R",
      "title":"Values and the Contemporary Family"
    },
    {
      "course_id":"013891",
      "subject":"SDS",
      "catalog_number":"355R",
      "title":"Resilience and Social Support"
    },
    {
      "course_id":"012746",
      "subject":"SDS",
      "catalog_number":"370R",
      "title":"International Learning Experience"
    },
    {
      "course_id":"012191",
      "subject":"SDS",
      "catalog_number":"375R",
      "title":"Studies in Interdisciplinary Social Science"
    },
    {
      "course_id":"014138",
      "subject":"SDS",
      "catalog_number":"388R",
      "title":"Globalization and Social Development"
    },
    {
      "course_id":"006514",
      "subject":"SDS",
      "catalog_number":"398R",
      "title":"Independent Study"
    },
    {
      "course_id":"006515",
      "subject":"SDS",
      "catalog_number":"399R",
      "title":"Independent Study"
    },
    {
      "course_id":"013331",
      "subject":"SDS",
      "catalog_number":"400R",
      "title":"Comparative Social Policy"
    },
    {
      "course_id":"014385",
      "subject":"SDS",
      "catalog_number":"405R",
      "title":"Cosmopolitanism and Social Development"
    },
    {
      "course_id":"013737",
      "subject":"SDS",
      "catalog_number":"415R",
      "title":"Gender Relations within Educational Institutions"
    },
    {
      "course_id":"006509",
      "subject":"SDS",
      "catalog_number":"420R",
      "title":"Critical Encounter with Human Nature"
    },
    {
      "course_id":"013738",
      "subject":"SDS",
      "catalog_number":"425R",
      "title":"Educational Equity in Canada"
    },
    {
      "course_id":"014244",
      "subject":"SDS",
      "catalog_number":"431R",
      "title":"Radical Ideology and Social Policy"
    },
    {
      "course_id":"013892",
      "subject":"SDS",
      "catalog_number":"440R",
      "title":"Optimal Living"
    },
    {
      "course_id":"013099",
      "subject":"SDS",
      "catalog_number":"450R",
      "title":"Honours Seminar in Special Topics"
    },
    {
      "course_id":"013103",
      "subject":"SDS",
      "catalog_number":"490R",
      "title":"Special Studies"
    },
    {
      "course_id":"011389",
      "subject":"SDS",
      "catalog_number":"495R",
      "title":"Research Apprenticeship"
    },
    {
      "course_id":"013220",
      "subject":"SDS",
      "catalog_number":"496R",
      "title":"Applied Apprenticeship in Social Development Studies"
    },
    {
      "course_id":"006516",
      "subject":"SDS",
      "catalog_number":"499A",
      "title":"Senior Honours Essay\/Thesis"
    },
    {
      "course_id":"006517",
      "subject":"SDS",
      "catalog_number":"499B",
      "title":"Senior Honours Essay\/Thesis"
    },
    {
      "course_id":"010030",
      "subject":"SE",
      "catalog_number":"101",
      "title":"Introduction to Methods of Software Engineering"
    },
    {
      "course_id":"011339",
      "subject":"SE",
      "catalog_number":"102",
      "title":"Seminar"
    },
    {
      "course_id":"011341",
      "subject":"SE",
      "catalog_number":"201",
      "title":"Seminar"
    },
    {
      "course_id":"011330",
      "subject":"SE",
      "catalog_number":"202",
      "title":"Seminar"
    },
    {
      "course_id":"010031",
      "subject":"SE",
      "catalog_number":"212",
      "title":"Logic and Computation"
    },
    {
      "course_id":"011335",
      "subject":"SE",
      "catalog_number":"301",
      "title":"Seminar"
    },
    {
      "course_id":"011336",
      "subject":"SE",
      "catalog_number":"302",
      "title":"Seminar"
    },
    {
      "course_id":"013372",
      "subject":"SE",
      "catalog_number":"350",
      "title":"Operating Systems"
    },
    {
      "course_id":"013373",
      "subject":"SE",
      "catalog_number":"380",
      "title":"Introduction to Feedback Control"
    },
    {
      "course_id":"010131",
      "subject":"SE",
      "catalog_number":"382",
      "title":"Human-computer Interaction"
    },
    {
      "course_id":"012940",
      "subject":"SE",
      "catalog_number":"390",
      "title":"Design Project Planning"
    },
    {
      "course_id":"011337",
      "subject":"SE",
      "catalog_number":"401",
      "title":"Seminar"
    },
    {
      "course_id":"011338",
      "subject":"SE",
      "catalog_number":"402",
      "title":"Seminar"
    },
    {
      "course_id":"010034",
      "subject":"SE",
      "catalog_number":"463",
      "title":"Software Requirements Specification and Analysis"
    },
    {
      "course_id":"010035",
      "subject":"SE",
      "catalog_number":"464",
      "title":"Software Design and Architectures"
    },
    {
      "course_id":"010036",
      "subject":"SE",
      "catalog_number":"465",
      "title":"Software Testing and Quality Assurance"
    },
    {
      "course_id":"012941",
      "subject":"SE",
      "catalog_number":"490",
      "title":"Design Project 1"
    },
    {
      "course_id":"012942",
      "subject":"SE",
      "catalog_number":"491",
      "title":"Design Project 2"
    },
    {
      "course_id":"012292",
      "subject":"SE",
      "catalog_number":"498",
      "title":"Advanced Topics in Software Engineering"
    },
    {
      "course_id":"012293",
      "subject":"SE",
      "catalog_number":"499",
      "title":"Project"
    },
    {
      "course_id":"013338",
      "subject":"SI",
      "catalog_number":"101R",
      "title":"Introduction to Arabic 1"
    },
    {
      "course_id":"013339",
      "subject":"SI",
      "catalog_number":"102R",
      "title":"Introduction to Arabic 2"
    },
    {
      "course_id":"013340",
      "subject":"SI",
      "catalog_number":"121R",
      "title":"Islam in the World"
    },
    {
      "course_id":"014001",
      "subject":"SI",
      "catalog_number":"201R",
      "title":"Intermediate Arabic 1"
    },
    {
      "course_id":"014002",
      "subject":"SI",
      "catalog_number":"202R",
      "title":"Intermediate Arabic 2"
    },
    {
      "course_id":"014398",
      "subject":"SI",
      "catalog_number":"221R",
      "title":"Islam, the West, and the Modern World"
    },
    {
      "course_id":"014003",
      "subject":"SI",
      "catalog_number":"301R",
      "title":"Advanced Arabic 1"
    },
    {
      "course_id":"014004",
      "subject":"SI",
      "catalog_number":"302R",
      "title":"Advanced Arabic 2"
    },
    {
      "course_id":"014399",
      "subject":"SI",
      "catalog_number":"315R",
      "title":"Islam, Women, and the Modern World"
    },
    {
      "course_id":"014139",
      "subject":"SI",
      "catalog_number":"375R",
      "title":"Special Topics in Islam"
    },
    {
      "course_id":"013354",
      "subject":"SI",
      "catalog_number":"390R",
      "title":"Understanding Islam"
    },
    {
      "course_id":"008554",
      "subject":"SMF",
      "catalog_number":"204",
      "title":"Introduction to Human Sexuality"
    },
    {
      "course_id":"008555",
      "subject":"SMF",
      "catalog_number":"205",
      "title":"The Dark Side of Sexuality"
    },
    {
      "course_id":"008556",
      "subject":"SMF",
      "catalog_number":"206",
      "title":"Couples, Marriages, and Families"
    },
    {
      "course_id":"008557",
      "subject":"SMF",
      "catalog_number":"207",
      "title":"Parents, Children, and Family Relations"
    },
    {
      "course_id":"012038",
      "subject":"SMF",
      "catalog_number":"208",
      "title":"Introduction to Couple, Family, and Sex Therapy"
    },
    {
      "course_id":"012963",
      "subject":"SMF",
      "catalog_number":"220",
      "title":"Research Methods"
    },
    {
      "course_id":"013010",
      "subject":"SMF",
      "catalog_number":"230",
      "title":"Introduction to Statistics in Sexuality, Marriage, and Family Studies"
    },
    {
      "course_id":"013613",
      "subject":"SMF",
      "catalog_number":"301",
      "title":"Communication and Counselling Skills"
    },
    {
      "course_id":"008566",
      "subject":"SMF",
      "catalog_number":"304",
      "title":"Human Sexuality in Relationships"
    },
    {
      "course_id":"008567",
      "subject":"SMF",
      "catalog_number":"305",
      "title":"Social Issues and Controversies in Human Sexuality"
    },
    {
      "course_id":"008568",
      "subject":"SMF",
      "catalog_number":"306",
      "title":"The Formation and Maintenance of Close Relationships"
    },
    {
      "course_id":"008569",
      "subject":"SMF",
      "catalog_number":"307",
      "title":"Conflict, Crisis, and Dissolution in Close Relationships"
    },
    {
      "course_id":"008570",
      "subject":"SMF",
      "catalog_number":"308",
      "title":"Couple and Family Therapy"
    },
    {
      "course_id":"008571",
      "subject":"SMF",
      "catalog_number":"309",
      "title":"Sex Therapy"
    },
    {
      "course_id":"011878",
      "subject":"SMF",
      "catalog_number":"310",
      "title":"Sexual Ethics"
    },
    {
      "course_id":"013234",
      "subject":"SMF",
      "catalog_number":"317",
      "title":"History of Sexuality: The Pre-Modern Period"
    },
    {
      "course_id":"012964",
      "subject":"SMF",
      "catalog_number":"318",
      "title":"History of Sexuality: The Modern Period"
    },
    {
      "course_id":"013011",
      "subject":"SMF",
      "catalog_number":"319",
      "title":"History of Sexuality: Special Topics"
    },
    {
      "course_id":"010353",
      "subject":"SMF",
      "catalog_number":"365",
      "title":"Special Topics in Human Sexuality"
    },
    {
      "course_id":"011879",
      "subject":"SMF",
      "catalog_number":"366",
      "title":"Special Topics in Couples, Marriage, and Family Studies"
    },
    {
      "course_id":"011880",
      "subject":"SMF",
      "catalog_number":"367",
      "title":"Special Topics in Sexuality, Marriage, and Family Studies"
    },
    {
      "course_id":"008574",
      "subject":"SMF",
      "catalog_number":"404",
      "title":"Independent Study: Special Topics in Sexuality"
    },
    {
      "course_id":"008575",
      "subject":"SMF",
      "catalog_number":"406",
      "title":"Independent Study: Special Topics in Marriage and Family Studies"
    },
    {
      "course_id":"008576",
      "subject":"SMF",
      "catalog_number":"408",
      "title":"Independent Study: Special Topics in Couple and Family Therapy"
    },
    {
      "course_id":"012117",
      "subject":"SMF",
      "catalog_number":"460",
      "title":"Practicum and Professional Ethics"
    },
    {
      "course_id":"013012",
      "subject":"SMF",
      "catalog_number":"461",
      "title":"Practicum and Applied Theory"
    },
    {
      "course_id":"013013",
      "subject":"SMF",
      "catalog_number":"462",
      "title":"Research Thesis and Applied Theory"
    },
    {
      "course_id":"013014",
      "subject":"SMF",
      "catalog_number":"490",
      "title":"Seminar in Sexuality, Marriage, and Family Ethics"
    },
    {
      "course_id":"013015",
      "subject":"SMF",
      "catalog_number":"494",
      "title":"Seminar in Sexuality"
    },
    {
      "course_id":"013016",
      "subject":"SMF",
      "catalog_number":"496",
      "title":"Seminar in Family Studies"
    },
    {
      "course_id":"013017",
      "subject":"SMF",
      "catalog_number":"498",
      "title":"Seminar in Therapy: Couple, Family, and Sex Therapy"
    },
    {
      "course_id":"008580",
      "subject":"SOC",
      "catalog_number":"101",
      "title":"Introduction to Sociology"
    },
    {
      "course_id":"008580",
      "subject":"SOC",
      "catalog_number":"101R",
      "title":"Introduction to Sociology"
    },
    {
      "course_id":"008581",
      "subject":"SOC",
      "catalog_number":"102",
      "title":"Social Problems"
    },
    {
      "course_id":"008583",
      "subject":"SOC",
      "catalog_number":"200",
      "title":"Sociology of Marriage and Family"
    },
    {
      "course_id":"008584",
      "subject":"SOC",
      "catalog_number":"201",
      "title":"Victims and Society"
    },
    {
      "course_id":"009512",
      "subject":"SOC",
      "catalog_number":"202",
      "title":"Classical Sociological Theory"
    },
    {
      "course_id":"008587",
      "subject":"SOC",
      "catalog_number":"204",
      "title":"Sociology of Adolescence"
    },
    {
      "course_id":"008587",
      "subject":"SOC",
      "catalog_number":"204R",
      "title":"Sociology of Adolescence"
    },
    {
      "course_id":"008588",
      "subject":"SOC",
      "catalog_number":"206",
      "title":"Gender Relations"
    },
    {
      "course_id":"008590",
      "subject":"SOC",
      "catalog_number":"207",
      "title":"Sociology of Education"
    },
    {
      "course_id":"008590",
      "subject":"SOC",
      "catalog_number":"207R",
      "title":"Sociology of Education"
    },
    {
      "course_id":"008593",
      "subject":"SOC",
      "catalog_number":"209",
      "title":"Ancestry, History and Personal Identity"
    },
    {
      "course_id":"008112",
      "subject":"SOC",
      "catalog_number":"210",
      "title":"Sociology of Sport"
    },
    {
      "course_id":"008602",
      "subject":"SOC",
      "catalog_number":"222",
      "title":"Juvenile Delinquency"
    },
    {
      "course_id":"008603",
      "subject":"SOC",
      "catalog_number":"223",
      "title":"Deviance: Perspectives and Processes"
    },
    {
      "course_id":"008603",
      "subject":"SOC",
      "catalog_number":"223R",
      "title":"Deviance: Perspectives and Processes"
    },
    {
      "course_id":"008605",
      "subject":"SOC",
      "catalog_number":"224R",
      "title":"Poverty in Canada and its Social Consequences"
    },
    {
      "course_id":"008608",
      "subject":"SOC",
      "catalog_number":"226",
      "title":"Juvenile Justice"
    },
    {
      "course_id":"008609",
      "subject":"SOC",
      "catalog_number":"227",
      "title":"Criminology"
    },
    {
      "course_id":"008610",
      "subject":"SOC",
      "catalog_number":"228",
      "title":"Sociology of Criminal Justice"
    },
    {
      "course_id":"010101",
      "subject":"SOC",
      "catalog_number":"229",
      "title":"Selected Topics in Criminology"
    },
    {
      "course_id":"008612",
      "subject":"SOC",
      "catalog_number":"232",
      "title":"Technology and Social Change"
    },
    {
      "course_id":"008616",
      "subject":"SOC",
      "catalog_number":"234",
      "title":"Social Psychology and Everyday Life"
    },
    {
      "course_id":"008621",
      "subject":"SOC",
      "catalog_number":"237",
      "title":"Collective Behaviour"
    },
    {
      "course_id":"008623",
      "subject":"SOC",
      "catalog_number":"241",
      "title":"Sociology of Work and Occupations"
    },
    {
      "course_id":"015069",
      "subject":"SOC",
      "catalog_number":"263",
      "title":"Organized Crime"
    },
    {
      "course_id":"008625",
      "subject":"SOC",
      "catalog_number":"243",
      "title":"Occupational Sociology"
    },
    {
      "course_id":"008628",
      "subject":"SOC",
      "catalog_number":"246",
      "title":"Mass Communication"
    },
    {
      "course_id":"008630",
      "subject":"SOC",
      "catalog_number":"248",
      "title":"Health, Illness and Society"
    },
    {
      "course_id":"008631",
      "subject":"SOC",
      "catalog_number":"249",
      "title":"Sociology of Mental Disorder"
    },
    {
      "course_id":"008632",
      "subject":"SOC",
      "catalog_number":"250",
      "title":"Contemporary Japanese Society"
    },
    {
      "course_id":"008634",
      "subject":"SOC",
      "catalog_number":"253",
      "title":"Demographic Change in Canada"
    },
    {
      "course_id":"008636",
      "subject":"SOC",
      "catalog_number":"256",
      "title":"Ethnic and Racial Relations"
    },
    {
      "course_id":"008311",
      "subject":"SOC",
      "catalog_number":"258",
      "title":"Millennialism & Violence"
    },
    {
      "course_id":"008309",
      "subject":"SOC",
      "catalog_number":"260",
      "title":"Religion in Sociological Perspective"
    },
    {
      "course_id":"008310",
      "subject":"SOC",
      "catalog_number":"261",
      "title":"Religion in America"
    },
    {
      "course_id":"008312",
      "subject":"SOC",
      "catalog_number":"262",
      "title":"Cults and New Religious Movements"
    },
    {
      "course_id":"008644",
      "subject":"SOC",
      "catalog_number":"275",
      "title":"Mennonites as a Sociological Community"
    },
    {
      "course_id":"008645",
      "subject":"SOC",
      "catalog_number":"280",
      "title":"Social Statistics"
    },
    {
      "course_id":"008649",
      "subject":"SOC",
      "catalog_number":"286",
      "title":"Environment and Behaviour"
    },
    {
      "course_id":"009513",
      "subject":"SOC",
      "catalog_number":"302",
      "title":"Contemporary Sociological Theory"
    },
    {
      "course_id":"008653",
      "subject":"SOC",
      "catalog_number":"307",
      "title":"Problems in Contemporary Education"
    },
    {
      "course_id":"008658",
      "subject":"SOC",
      "catalog_number":"312",
      "title":"Sociology of Science"
    },
    {
      "course_id":"008659",
      "subject":"SOC",
      "catalog_number":"315",
      "title":"Class, Status and Power"
    },
    {
      "course_id":"008661",
      "subject":"SOC",
      "catalog_number":"321",
      "title":"Introduction to Research Methods"
    },
    {
      "course_id":"008664",
      "subject":"SOC",
      "catalog_number":"322",
      "title":"Field Research Methods"
    },
    {
      "course_id":"008667",
      "subject":"SOC",
      "catalog_number":"325",
      "title":"Sexuality and the Law"
    },
    {
      "course_id":"014130",
      "subject":"SOC",
      "catalog_number":"326",
      "title":"Punishment and Society"
    },
    {
      "course_id":"009873",
      "subject":"SOC",
      "catalog_number":"327",
      "title":"Policing in a Democratic Society"
    },
    {
      "course_id":"008676",
      "subject":"SOC",
      "catalog_number":"336",
      "title":"Sociology of Professions"
    },
    {
      "course_id":"012613",
      "subject":"SOC",
      "catalog_number":"339",
      "title":"The Knowledge Society and Waterloo Region"
    },
    {
      "course_id":"008679",
      "subject":"SOC",
      "catalog_number":"340",
      "title":"Sociology of Organizations"
    },
    {
      "course_id":"014132",
      "subject":"SOC",
      "catalog_number":"342",
      "title":"Mobility and Regulation"
    },
    {
      "course_id":"011157",
      "subject":"SOC",
      "catalog_number":"345",
      "title":"Cyberspace and Social Life"
    },
    {
      "course_id":"010098",
      "subject":"SOC",
      "catalog_number":"346",
      "title":"Social Movements"
    },
    {
      "course_id":"008130",
      "subject":"SOC",
      "catalog_number":"347",
      "title":"Sociology of Leisure"
    },
    {
      "course_id":"014133",
      "subject":"SOC",
      "catalog_number":"349",
      "title":"Migration and Development"
    },
    {
      "course_id":"006438",
      "subject":"SOC",
      "catalog_number":"352",
      "title":"Sociology of Aging"
    },
    {
      "course_id":"011845",
      "subject":"SOC",
      "catalog_number":"354",
      "title":"Comparative Health Care Systems"
    },
    {
      "course_id":"009517",
      "subject":"SOC",
      "catalog_number":"355J",
      "title":"Power and Parenting"
    },
    {
      "course_id":"010096",
      "subject":"SOC",
      "catalog_number":"362",
      "title":"Canadian Society: Special Topics"
    },
    {
      "course_id":"008689",
      "subject":"SOC",
      "catalog_number":"365",
      "title":"Urban Life and Culture"
    },
    {
      "course_id":"011186",
      "subject":"SOC",
      "catalog_number":"366",
      "title":"Entertainment Motifs: An Interactionist Analysis"
    },
    {
      "course_id":"008693",
      "subject":"SOC",
      "catalog_number":"368",
      "title":"Custodial and Rehabilitative Institutions"
    },
    {
      "course_id":"009876",
      "subject":"SOC",
      "catalog_number":"369J",
      "title":"The Sociology of Community"
    },
    {
      "course_id":"008694",
      "subject":"SOC",
      "catalog_number":"370",
      "title":"Sociology of Law"
    },
    {
      "course_id":"009874",
      "subject":"SOC",
      "catalog_number":"372",
      "title":"Good and Evil in Social Relations"
    },
    {
      "course_id":"012193",
      "subject":"SOC",
      "catalog_number":"375R",
      "title":"Studies in Sociology"
    },
    {
      "course_id":"008696",
      "subject":"SOC",
      "catalog_number":"378",
      "title":"Sociology of Women"
    },
    {
      "course_id":"008699",
      "subject":"SOC",
      "catalog_number":"382",
      "title":"Survey Methodology"
    },
    {
      "course_id":"008701",
      "subject":"SOC",
      "catalog_number":"398R",
      "title":"Independent Study"
    },
    {
      "course_id":"009900",
      "subject":"SOC",
      "catalog_number":"399R",
      "title":"Independent Study"
    },
    {
      "course_id":"008702",
      "subject":"SOC",
      "catalog_number":"401",
      "title":"Theoretical Perspectives on Gender"
    },
    {
      "course_id":"010232",
      "subject":"SOC",
      "catalog_number":"402",
      "title":"Sociology of Religion"
    },
    {
      "course_id":"008703",
      "subject":"SOC",
      "catalog_number":"404",
      "title":"Sociology of Knowledge"
    },
    {
      "course_id":"008704",
      "subject":"SOC",
      "catalog_number":"405",
      "title":"Seminar in Classical Sociological Theory"
    },
    {
      "course_id":"008705",
      "subject":"SOC",
      "catalog_number":"406",
      "title":"Seminar in Contemporary Sociological Theory"
    },
    {
      "course_id":"008706",
      "subject":"SOC",
      "catalog_number":"407",
      "title":"Canadian Social Thought"
    },
    {
      "course_id":"008707",
      "subject":"SOC",
      "catalog_number":"408",
      "title":"Contemporary Debates in Sociological Theory"
    },
    {
      "course_id":"009878",
      "subject":"SOC",
      "catalog_number":"409",
      "title":"Knowing and Acting: Social Theory from the Early Greeks to the Present"
    },
    {
      "course_id":"008708",
      "subject":"SOC",
      "catalog_number":"410",
      "title":"Symbolic Interaction and Ethnographic Research"
    },
    {
      "course_id":"011614",
      "subject":"SOC",
      "catalog_number":"414",
      "title":"Power, Persuasion, and Management"
    },
    {
      "course_id":"008710",
      "subject":"SOC",
      "catalog_number":"415",
      "title":"Social Networks"
    },
    {
      "course_id":"012405",
      "subject":"SOC",
      "catalog_number":"416",
      "title":"Educational Theory and Practice"
    },
    {
      "course_id":"012617",
      "subject":"SOC",
      "catalog_number":"417",
      "title":"Sociology of Higher Education"
    },
    {
      "course_id":"014842",
      "subject":"SOC",
      "catalog_number":"434",
      "title":"Sociology of At-Risk Youth"
    },
    {
      "course_id":"014135",
      "subject":"SOC",
      "catalog_number":"418",
      "title":"Social Theory and Popular Culture"
    },
    {
      "course_id":"009879",
      "subject":"SOC",
      "catalog_number":"420",
      "title":"Seminar in Social Inequality"
    },
    {
      "course_id":"008711",
      "subject":"SOC",
      "catalog_number":"421",
      "title":"Quantitative Methods"
    },
    {
      "course_id":"011846",
      "subject":"SOC",
      "catalog_number":"424",
      "title":"Seminar in Sociology of Health"
    },
    {
      "course_id":"010152",
      "subject":"SOC",
      "catalog_number":"428",
      "title":"Sentencing as a Social Process"
    },
    {
      "course_id":"008713",
      "subject":"SOC",
      "catalog_number":"435",
      "title":"Environmental Sociology"
    },
    {
      "course_id":"013097",
      "subject":"SOC",
      "catalog_number":"450R",
      "title":"Honours Seminar in Special Topics"
    },
    {
      "course_id":"014134",
      "subject":"SOC",
      "catalog_number":"451",
      "title":"Global Development"
    },
    {
      "course_id":"014136",
      "subject":"SOC",
      "catalog_number":"452",
      "title":"Humanitarianism"
    },
    {
      "course_id":"008731",
      "subject":"SOC",
      "catalog_number":"459",
      "title":"Sociology of Work and Occupations"
    },
    {
      "course_id":"013101",
      "subject":"SOC",
      "catalog_number":"490R",
      "title":"Special Studies"
    },
    {
      "course_id":"011348",
      "subject":"SOC",
      "catalog_number":"497",
      "title":"Honours Research Practicum"
    },
    {
      "course_id":"010021",
      "subject":"SOC",
      "catalog_number":"498",
      "title":"Directed Studies"
    },
    {
      "course_id":"008744",
      "subject":"SOC",
      "catalog_number":"499A",
      "title":"Senior Honours Essay"
    },
    {
      "course_id":"008745",
      "subject":"SOC",
      "catalog_number":"499B",
      "title":"Senior Honours Essay"
    },
    {
      "course_id":"014549",
      "subject":"SOC",
      "catalog_number":"696",
      "title":"Sociology of the Life Course"
    },
    {
      "course_id":"010287",
      "subject":"SOC",
      "catalog_number":"697",
      "title":"Practicum in Survey Administration"
    },
    {
      "course_id":"003036",
      "subject":"SOC",
      "catalog_number":"700",
      "title":"Sociological Theory"
    },
    {
      "course_id":"010515",
      "subject":"SOC",
      "catalog_number":"703",
      "title":"Social Theory and Enacted Realities: From the Early Greeks to the Present Time"
    },
    {
      "course_id":"003038",
      "subject":"SOC",
      "catalog_number":"704",
      "title":"Key Theoretical Debates"
    },
    {
      "course_id":"003039",
      "subject":"SOC",
      "catalog_number":"705",
      "title":"Theory and Research in Social Organization"
    },
    {
      "course_id":"003040",
      "subject":"SOC",
      "catalog_number":"706",
      "title":"Theory and Research in Social Psychology"
    },
    {
      "course_id":"003041",
      "subject":"SOC",
      "catalog_number":"707",
      "title":"Canadian Sociological Thought"
    },
    {
      "course_id":"003042",
      "subject":"SOC",
      "catalog_number":"708",
      "title":"Contemporary Debates in Sociological Theory"
    },
    {
      "course_id":"003043",
      "subject":"SOC",
      "catalog_number":"709",
      "title":"Selected Problems in Sociological Theory"
    },
    {
      "course_id":"003044",
      "subject":"SOC",
      "catalog_number":"710",
      "title":"Intermediate Social Statistics"
    },
    {
      "course_id":"013074",
      "subject":"SOC",
      "catalog_number":"711",
      "title":"Techniques in Longitudinal Analysis"
    },
    {
      "course_id":"003045",
      "subject":"SOC",
      "catalog_number":"712",
      "title":"Elements of Social Research"
    },
    {
      "course_id":"003046",
      "subject":"SOC",
      "catalog_number":"713",
      "title":"Design and Data Analysis in Quantitative Research"
    },
    {
      "course_id":"003047",
      "subject":"SOC",
      "catalog_number":"714",
      "title":"Ethnographic Research in the Social Sciences"
    },
    {
      "course_id":"003048",
      "subject":"SOC",
      "catalog_number":"715",
      "title":"Research Design"
    },
    {
      "course_id":"013075",
      "subject":"SOC",
      "catalog_number":"716",
      "title":"Qualitative Methods"
    },
    {
      "course_id":"012778",
      "subject":"SOC",
      "catalog_number":"717",
      "title":"Reflexive Research Methodologies: Contemporary Interpretive Traditions"
    },
    {
      "course_id":"003049",
      "subject":"SOC",
      "catalog_number":"719",
      "title":"Selected Problems in Sociological Research"
    },
    {
      "course_id":"003050",
      "subject":"SOC",
      "catalog_number":"720",
      "title":"Social Inequality"
    },
    {
      "course_id":"012018",
      "subject":"SOC",
      "catalog_number":"725",
      "title":"Sociology of Health"
    },
    {
      "course_id":"003051",
      "subject":"SOC",
      "catalog_number":"730",
      "title":"Sociology of Religion"
    },
    {
      "course_id":"003052",
      "subject":"SOC",
      "catalog_number":"735",
      "title":"Environmental Sociology"
    },
    {
      "course_id":"003053",
      "subject":"SOC",
      "catalog_number":"740",
      "title":"Sociology of Deviance"
    },
    {
      "course_id":"013073",
      "subject":"SOC",
      "catalog_number":"744",
      "title":"Sociology of Crime and Justice"
    },
    {
      "course_id":"009415",
      "subject":"SOC",
      "catalog_number":"745",
      "title":"Deviance: An Interactionist Perspective"
    },
    {
      "course_id":"003055",
      "subject":"SOC",
      "catalog_number":"750",
      "title":"Sociology of Gender Roles"
    },
    {
      "course_id":"003056",
      "subject":"SOC",
      "catalog_number":"751",
      "title":"Theories of Gender Relations"
    },
    {
      "course_id":"003057",
      "subject":"SOC",
      "catalog_number":"759",
      "title":"Sociology of Work and Occupations"
    },
    {
      "course_id":"003058",
      "subject":"SOC",
      "catalog_number":"760",
      "title":"Social Networks"
    },
    {
      "course_id":"003059",
      "subject":"SOC",
      "catalog_number":"765",
      "title":"Political Sociology"
    },
    {
      "course_id":"013329",
      "subject":"SOC",
      "catalog_number":"766",
      "title":"Participatory Action Research"
    },
    {
      "course_id":"013330",
      "subject":"SOC",
      "catalog_number":"768",
      "title":"Community Engagement and Social Development"
    },
    {
      "course_id":"010516",
      "subject":"SOC",
      "catalog_number":"770",
      "title":"Comparative Social Structure"
    },
    {
      "course_id":"003060",
      "subject":"SOC",
      "catalog_number":"774",
      "title":"Family and Kinship"
    },
    {
      "course_id":"003061",
      "subject":"SOC",
      "catalog_number":"776",
      "title":"Sociology of Knowledge"
    },
    {
      "course_id":"013379",
      "subject":"SOC",
      "catalog_number":"778",
      "title":"Theorizing Discourses of Health, Illness and Disease in Everyday Life"
    },
    {
      "course_id":"003062",
      "subject":"SOC",
      "catalog_number":"780",
      "title":"Theories of Social Change"
    },
    {
      "course_id":"014219",
      "subject":"SOC",
      "catalog_number":"781",
      "title":"Global Development Governance"
    },
    {
      "course_id":"014550",
      "subject":"SOC",
      "catalog_number":"782",
      "title":"Law, Globalization and Women's Empowerment"
    },
    {
      "course_id":"014220",
      "subject":"SOC",
      "catalog_number":"783",
      "title":"Security and Regulation"
    },
    {
      "course_id":"003066",
      "subject":"SOC",
      "catalog_number":"786",
      "title":"Interdisciplinary Seminar in Aging"
    },
    {
      "course_id":"003068",
      "subject":"SOC",
      "catalog_number":"789",
      "title":"Graduate Readings in Sociology"
    },
    {
      "course_id":"011270",
      "subject":"STAT",
      "catalog_number":"846",
      "title":"Mathematical Models in Finance"
    },
    {
      "course_id":"014007",
      "subject":"SOCIN",
      "catalog_number":"601",
      "title":"Social Innovations in Complex Systems"
    },
    {
      "course_id":"014008",
      "subject":"SOCIN",
      "catalog_number":"602",
      "title":"Design Thinking for System Change"
    },
    {
      "course_id":"014075",
      "subject":"SOCIN",
      "catalog_number":"603",
      "title":"Team Process and Research Skills:  Communication, Facilitation, Collaboration, Problem Solving"
    },
    {
      "course_id":"014010",
      "subject":"SOCIN",
      "catalog_number":"604",
      "title":"Scaling Innovation for Greater Impact: social finance, social marketing, public policy development"
    },
    {
      "course_id":"014011",
      "subject":"SOCIN",
      "catalog_number":"605",
      "title":"Social Innovation Project"
    },
    {
      "course_id":"008748",
      "subject":"SOCWK",
      "catalog_number":"120R",
      "title":"Introduction to Social Work"
    },
    {
      "course_id":"008749",
      "subject":"SOCWK",
      "catalog_number":"220R",
      "title":"Social Work with Individuals - Theory and Practice 1"
    },
    {
      "course_id":"008750",
      "subject":"SOCWK",
      "catalog_number":"221R",
      "title":"Social Group Work"
    },
    {
      "course_id":"008751",
      "subject":"SOCWK",
      "catalog_number":"222R",
      "title":"Community Organization 1"
    },
    {
      "course_id":"008753",
      "subject":"SOCWK",
      "catalog_number":"240R",
      "title":"Palliative Care"
    },
    {
      "course_id":"008755",
      "subject":"SOCWK",
      "catalog_number":"300R",
      "title":"Canadian Social Welfare Policy"
    },
    {
      "course_id":"011116",
      "subject":"SOCWK",
      "catalog_number":"301R",
      "title":"Understanding Diversity in Canada"
    },
    {
      "course_id":"008757",
      "subject":"SOCWK",
      "catalog_number":"320R",
      "title":"Social Work with Individuals - Theory and Practice 2"
    },
    {
      "course_id":"008758",
      "subject":"SOCWK",
      "catalog_number":"321R",
      "title":"Social Work with Families"
    },
    {
      "course_id":"008759",
      "subject":"SOCWK",
      "catalog_number":"322R",
      "title":"International Perspectives in Community Organization"
    },
    {
      "course_id":"008760",
      "subject":"SOCWK",
      "catalog_number":"326R",
      "title":"Philosophy and History of Social Welfare"
    },
    {
      "course_id":"008767",
      "subject":"SOCWK",
      "catalog_number":"355R",
      "title":"Child Maltreatment: Identification and Prevention"
    },
    {
      "course_id":"008768",
      "subject":"SOCWK",
      "catalog_number":"356R",
      "title":"Developmental Disabilities and the Family"
    },
    {
      "course_id":"008769",
      "subject":"SOCWK",
      "catalog_number":"357R",
      "title":"Family Violence"
    },
    {
      "course_id":"008770",
      "subject":"SOCWK",
      "catalog_number":"365R",
      "title":"Social Work in Health Care"
    },
    {
      "course_id":"008771",
      "subject":"SOCWK",
      "catalog_number":"367R",
      "title":"Social Work with the Elderly"
    },
    {
      "course_id":"012192",
      "subject":"SOCWK",
      "catalog_number":"375R",
      "title":"Studies in Social Work"
    },
    {
      "course_id":"008772",
      "subject":"SOCWK",
      "catalog_number":"390A",
      "title":"Family Violence: An Advanced Seminar"
    },
    {
      "course_id":"008773",
      "subject":"SOCWK",
      "catalog_number":"390B",
      "title":"Family Violence: An Advanced Seminar"
    },
    {
      "course_id":"008774",
      "subject":"SOCWK",
      "catalog_number":"398R",
      "title":"Independent Study"
    },
    {
      "course_id":"008775",
      "subject":"SOCWK",
      "catalog_number":"399R",
      "title":"Independent Study"
    },
    {
      "course_id":"013335",
      "subject":"SOCWK",
      "catalog_number":"421R",
      "title":"Advanced Family Practices"
    },
    {
      "course_id":"013098",
      "subject":"SOCWK",
      "catalog_number":"450R",
      "title":"Honours Seminar in Special Topics"
    },
    {
      "course_id":"013102",
      "subject":"SOCWK",
      "catalog_number":"490R",
      "title":"Special Studies"
    },
    {
      "course_id":"008783",
      "subject":"SPAN",
      "catalog_number":"101",
      "title":"Introduction to Spanish 1"
    },
    {
      "course_id":"008786",
      "subject":"SPAN",
      "catalog_number":"102",
      "title":"Introduction to Spanish 2"
    },
    {
      "course_id":"008809",
      "subject":"SPAN",
      "catalog_number":"223W",
      "title":"Early Spanish Literature (WLU)"
    },
    {
      "course_id":"014279",
      "subject":"SPAN",
      "catalog_number":"150",
      "title":"The Hispanic World Through Literature and the Arts"
    },
    {
      "course_id":"008791",
      "subject":"SPAN",
      "catalog_number":"201A",
      "title":"Intermediate Spanish 1"
    },
    {
      "course_id":"008792",
      "subject":"SPAN",
      "catalog_number":"201B",
      "title":"Intermediate Spanish 2"
    },
    {
      "course_id":"012753",
      "subject":"SPAN",
      "catalog_number":"210",
      "title":"Intermediate Spanish for Native Speakers"
    },
    {
      "course_id":"008804",
      "subject":"SPAN",
      "catalog_number":"217",
      "title":"Latin American Civilization 1"
    },
    {
      "course_id":"008808",
      "subject":"SPAN",
      "catalog_number":"222W",
      "title":"Modern Spanish Literature (WLU)"
    },
    {
      "course_id":"008805",
      "subject":"SPAN",
      "catalog_number":"218",
      "title":"Latin American Civilization 2"
    },
    {
      "course_id":"012172",
      "subject":"SPAN",
      "catalog_number":"220W",
      "title":"Topics in Spanish Culture(WLU)"
    },
    {
      "course_id":"008810",
      "subject":"SPAN",
      "catalog_number":"227",
      "title":"Introduction to Latin American Poetry and Drama"
    },
    {
      "course_id":"008811",
      "subject":"SPAN",
      "catalog_number":"228",
      "title":"Introduction to Latin American Literature"
    },
    {
      "course_id":"008812",
      "subject":"SPAN",
      "catalog_number":"301A",
      "title":"Spanish in Context 1"
    },
    {
      "course_id":"008813",
      "subject":"SPAN",
      "catalog_number":"301B",
      "title":"Spanish in Context 2"
    },
    {
      "course_id":"008822",
      "subject":"SPAN",
      "catalog_number":"305W",
      "title":"The Hispanic Realist Novel (WLU)"
    },
    {
      "course_id":"008833",
      "subject":"SPAN",
      "catalog_number":"326",
      "title":"Theatre of the Spanish Golden Age: Texts and Cultural Contexts"
    },
    {
      "course_id":"008835",
      "subject":"SPAN",
      "catalog_number":"327W",
      "title":"Cervantes & His Time (WLU)"
    },
    {
      "course_id":"008838",
      "subject":"SPAN",
      "catalog_number":"334",
      "title":"Narrating Place and Ethnicity in Nineteenth Century Latin America"
    },
    {
      "course_id":"011661",
      "subject":"SPAN",
      "catalog_number":"335W",
      "title":"Aesthetic Practices of Spanish and Latin American Filmmakers(WLU)"
    },
    {
      "course_id":"008839",
      "subject":"SPAN",
      "catalog_number":"344",
      "title":"Special Topics in Hispanic Studies"
    },
    {
      "course_id":"013958",
      "subject":"SPAN",
      "catalog_number":"345",
      "title":"Directed Studies"
    },
    {
      "course_id":"014415",
      "subject":"SPAN",
      "catalog_number":"350",
      "title":"Poetry of the Tango"
    },
    {
      "course_id":"009915",
      "subject":"SPAN",
      "catalog_number":"366",
      "title":"Aesthetics of Rupture: Latin American Avant-garde Movements"
    },
    {
      "course_id":"014280",
      "subject":"SPAN",
      "catalog_number":"386",
      "title":"Memory and Performance in Latin American Literature"
    },
    {
      "course_id":"008848",
      "subject":"SPAN",
      "catalog_number":"387",
      "title":"Gender, Power, and Representations in Latin America"
    },
    {
      "course_id":"009916",
      "subject":"SPAN",
      "catalog_number":"390",
      "title":"Introduction to Spanish Business Translation"
    },
    {
      "course_id":"011349",
      "subject":"SPAN",
      "catalog_number":"400",
      "title":"Memories and Representations: Constructive Truths and Competing Realities"
    },
    {
      "course_id":"008842",
      "subject":"SPAN",
      "catalog_number":"401A",
      "title":"Advanced Composition and Conversation 1"
    },
    {
      "course_id":"008843",
      "subject":"SPAN",
      "catalog_number":"401B",
      "title":"Advanced Composition and Conversation 2"
    },
    {
      "course_id":"013341",
      "subject":"SPAN",
      "catalog_number":"410",
      "title":"Visual Culture in the Contemporary Hispanic World"
    },
    {
      "course_id":"014414",
      "subject":"SPAN",
      "catalog_number":"415",
      "title":"The Hispanic Transatlantic"
    },
    {
      "course_id":"013889",
      "subject":"SPAN",
      "catalog_number":"418",
      "title":"Modernity and the Colonial Encounter in Latin America"
    },
    {
      "course_id":"010352",
      "subject":"SPAN",
      "catalog_number":"430",
      "title":"Literary Women in Early Modern Hispanic Culture"
    },
    {
      "course_id":"008850",
      "subject":"SPAN",
      "catalog_number":"445",
      "title":"History of the Spanish Language"
    },
    {
      "course_id":"011660",
      "subject":"SPAN",
      "catalog_number":"450",
      "title":"Theory and Practice of Translation"
    },
    {
      "course_id":"008856",
      "subject":"SPAN",
      "catalog_number":"490",
      "title":"Advanced Translation"
    },
    {
      "course_id":"008858",
      "subject":"SPAN",
      "catalog_number":"497",
      "title":"The Novel in Latin America"
    },
    {
      "course_id":"004666",
      "subject":"SPCOM",
      "catalog_number":"100",
      "title":"Interpersonal Communication"
    },
    {
      "course_id":"014532",
      "subject":"SPCOM",
      "catalog_number":"101",
      "title":"Theories of Communication"
    },
    {
      "course_id":"004662",
      "subject":"SPCOM",
      "catalog_number":"102",
      "title":"Introduction to Performance"
    },
    {
      "course_id":"013718",
      "subject":"SPCOM",
      "catalog_number":"111",
      "title":"Leadership, Communication, and Collaboration"
    },
    {
      "course_id":"013723",
      "subject":"SPCOM",
      "catalog_number":"204",
      "title":"Leadership, Teams, and Communication"
    },
    {
      "course_id":"012417",
      "subject":"SPCOM",
      "catalog_number":"220",
      "title":"Performance Studies"
    },
    {
      "course_id":"004665",
      "subject":"SPCOM",
      "catalog_number":"223",
      "title":"Public Speaking"
    },
    {
      "course_id":"004667",
      "subject":"SPCOM",
      "catalog_number":"225",
      "title":"Interviewing"
    },
    {
      "course_id":"012411",
      "subject":"SPCOM",
      "catalog_number":"226",
      "title":"Introduction to Intercultural Communication"
    },
    {
      "course_id":"010342",
      "subject":"SPCOM",
      "catalog_number":"227",
      "title":"Leadership"
    },
    {
      "course_id":"012410",
      "subject":"SPCOM",
      "catalog_number":"228",
      "title":"Public Communication"
    },
    {
      "course_id":"011682",
      "subject":"SPCOM",
      "catalog_number":"300",
      "title":"Special Topics in Digital Design"
    },
    {
      "course_id":"005137",
      "subject":"SPCOM",
      "catalog_number":"323",
      "title":"Speech Writing"
    },
    {
      "course_id":"004691",
      "subject":"SPCOM",
      "catalog_number":"324",
      "title":"Small Group Communication"
    },
    {
      "course_id":"004739",
      "subject":"SPCOM",
      "catalog_number":"325",
      "title":"Organizational Communication"
    },
    {
      "course_id":"004692",
      "subject":"SPCOM",
      "catalog_number":"326",
      "title":"Performing the Voice"
    },
    {
      "course_id":"012415",
      "subject":"SPCOM",
      "catalog_number":"329",
      "title":"Digital Presentations"
    },
    {
      "course_id":"014533",
      "subject":"SPCOM",
      "catalog_number":"399",
      "title":"Communication Inquiry"
    },
    {
      "course_id":"012412",
      "subject":"SPCOM",
      "catalog_number":"401",
      "title":"Gender, Communication and Culture"
    },
    {
      "course_id":"012413",
      "subject":"SPCOM",
      "catalog_number":"402",
      "title":"Advanced Intercultural Communication"
    },
    {
      "course_id":"012414",
      "subject":"SPCOM",
      "catalog_number":"404",
      "title":"Communicating Across Differences: Spiritual Development in a Diverse World"
    },
    {
      "course_id":"013571",
      "subject":"SPCOM",
      "catalog_number":"420",
      "title":"Persuasion"
    },
    {
      "course_id":"013570",
      "subject":"SPCOM",
      "catalog_number":"430",
      "title":"Communication and Social Justice"
    },
    {
      "course_id":"010340",
      "subject":"SPCOM",
      "catalog_number":"431",
      "title":"Crisis Communication"
    },
    {
      "course_id":"010350",
      "subject":"SPCOM",
      "catalog_number":"432",
      "title":"Conflict Management"
    },
    {
      "course_id":"010345",
      "subject":"SPCOM",
      "catalog_number":"433",
      "title":"The Organizational Consultant"
    },
    {
      "course_id":"011393",
      "subject":"SPCOM",
      "catalog_number":"434",
      "title":"The Discourse of Dissent"
    },
    {
      "course_id":"011906",
      "subject":"SPCOM",
      "catalog_number":"440",
      "title":"Performative Inquiry and Practice"
    },
    {
      "course_id":"013573",
      "subject":"SPCOM",
      "catalog_number":"475",
      "title":"Communication Ethics"
    },
    {
      "course_id":"011402",
      "subject":"SPCOM",
      "catalog_number":"490",
      "title":"Selected Seminars in Speech Communication"
    },
    {
      "course_id":"011403",
      "subject":"SPCOM",
      "catalog_number":"491",
      "title":"Selected Seminars in Speech Communication"
    },
    {
      "course_id":"004740",
      "subject":"SPCOM",
      "catalog_number":"499A",
      "title":"Senior Seminar"
    },
    {
      "course_id":"004741",
      "subject":"SPCOM",
      "catalog_number":"499B",
      "title":"Senior Seminar"
    },
    {
      "course_id":"008859",
      "subject":"STAT",
      "catalog_number":"202",
      "title":"Introductory Statistics for Scientists"
    },
    {
      "course_id":"010128",
      "subject":"STAT",
      "catalog_number":"206",
      "title":"Statistics for Software Engineering"
    },
    {
      "course_id":"008861",
      "subject":"STAT",
      "catalog_number":"211",
      "title":"Introductory Statistics and Sampling for Accounting"
    },
    {
      "course_id":"008862",
      "subject":"STAT",
      "catalog_number":"220",
      "title":"Probability (Non-Specialist Level)"
    },
    {
      "course_id":"008863",
      "subject":"STAT",
      "catalog_number":"221",
      "title":"Statistics (Non-Specialist Level)"
    },
    {
      "course_id":"008864",
      "subject":"STAT",
      "catalog_number":"230",
      "title":"Probability"
    },
    {
      "course_id":"008865",
      "subject":"STAT",
      "catalog_number":"231",
      "title":"Statistics"
    },
    {
      "course_id":"008866",
      "subject":"STAT",
      "catalog_number":"240",
      "title":"Probability (Advanced Level)"
    },
    {
      "course_id":"008867",
      "subject":"STAT",
      "catalog_number":"241",
      "title":"Statistics (Advanced Level)"
    },
    {
      "course_id":"004384",
      "subject":"STAT",
      "catalog_number":"316",
      "title":"Introduction to Statistical Problem Solving by Computer"
    },
    {
      "course_id":"008870",
      "subject":"STAT",
      "catalog_number":"321",
      "title":"Regression and Forecasting (Non-Specialist Level)"
    },
    {
      "course_id":"008871",
      "subject":"STAT",
      "catalog_number":"322",
      "title":"Sampling and Experimental Design (Non-Specialist Level)"
    },
    {
      "course_id":"008872",
      "subject":"STAT",
      "catalog_number":"330",
      "title":"Mathematical Statistics"
    },
    {
      "course_id":"003305",
      "subject":"STAT",
      "catalog_number":"446",
      "title":"Mathematical Models in Finance"
    },
    {
      "course_id":"008873",
      "subject":"STAT",
      "catalog_number":"331",
      "title":"Applied Linear Models"
    },
    {
      "course_id":"008874",
      "subject":"STAT",
      "catalog_number":"332",
      "title":"Sampling and Experimental Design"
    },
    {
      "course_id":"008875",
      "subject":"STAT",
      "catalog_number":"333",
      "title":"Applied Probability"
    },
    {
      "course_id":"012662",
      "subject":"STAT",
      "catalog_number":"334",
      "title":"Probability Models for Business and Accounting"
    },
    {
      "course_id":"013320",
      "subject":"STAT",
      "catalog_number":"337",
      "title":"Introduction to Medical Statistics"
    },
    {
      "course_id":"004408",
      "subject":"STAT",
      "catalog_number":"340",
      "title":"Computer Simulation of Complex Systems"
    },
    {
      "course_id":"011431",
      "subject":"STAT",
      "catalog_number":"341",
      "title":"Computational Statistics and Data Analysis"
    },
    {
      "course_id":"011723",
      "subject":"STAT",
      "catalog_number":"371",
      "title":"Applied Linear Models and Process Improvement for Business"
    },
    {
      "course_id":"011724",
      "subject":"STAT",
      "catalog_number":"372",
      "title":"Survey Sampling and Experimental Design Techniques for Business"
    },
    {
      "course_id":"012225",
      "subject":"STAT",
      "catalog_number":"373",
      "title":"Regression and Forecasting Methods in Finance"
    },
    {
      "course_id":"008880",
      "subject":"STAT",
      "catalog_number":"430",
      "title":"Experimental Design"
    },
    {
      "course_id":"008881",
      "subject":"STAT",
      "catalog_number":"431",
      "title":"Generalized Linear Models and their Applications"
    },
    {
      "course_id":"008882",
      "subject":"STAT",
      "catalog_number":"433",
      "title":"Stochastic Processes"
    },
    {
      "course_id":"011042",
      "subject":"STAT",
      "catalog_number":"435",
      "title":"Statistical Methods for Process Improvements"
    },
    {
      "course_id":"013322",
      "subject":"STAT",
      "catalog_number":"436",
      "title":"Introduction to the Analysis of Spatial Data in Health Research"
    },
    {
      "course_id":"013321",
      "subject":"STAT",
      "catalog_number":"437",
      "title":"Analysis of Longitudinal Data in Health Research"
    },
    {
      "course_id":"008883",
      "subject":"STAT",
      "catalog_number":"440",
      "title":"Computational Inference"
    },
    {
      "course_id":"008884",
      "subject":"STAT",
      "catalog_number":"441",
      "title":"Statistical Learning - Classification"
    },
    {
      "course_id":"011434",
      "subject":"STAT",
      "catalog_number":"442",
      "title":"Data Visualization"
    },
    {
      "course_id":"008885",
      "subject":"STAT",
      "catalog_number":"443",
      "title":"Forecasting"
    },
    {
      "course_id":"011436",
      "subject":"STAT",
      "catalog_number":"444",
      "title":"Statistical Learning - Function Estimation"
    },
    {
      "course_id":"008888",
      "subject":"STAT",
      "catalog_number":"450",
      "title":"Estimation and Hypothesis Testing"
    },
    {
      "course_id":"008890",
      "subject":"STAT",
      "catalog_number":"454",
      "title":"Sampling Theory and Practice"
    },
    {
      "course_id":"008891",
      "subject":"STAT",
      "catalog_number":"464",
      "title":"Topics in Probability Theory"
    },
    {
      "course_id":"008892",
      "subject":"STAT",
      "catalog_number":"466",
      "title":"Topics in Statistics 1"
    },
    {
      "course_id":"008893",
      "subject":"STAT",
      "catalog_number":"467",
      "title":"Topics in Statistics 2"
    },
    {
      "course_id":"008894",
      "subject":"STAT",
      "catalog_number":"468",
      "title":"Readings in Statistics 1"
    },
    {
      "course_id":"010728",
      "subject":"STAT",
      "catalog_number":"469",
      "title":"Readings in Statistics 2"
    },
    {
      "course_id":"013825",
      "subject":"STAT",
      "catalog_number":"631",
      "title":"Introduction to Statistical Methods in Health Informatics"
    },
    {
      "course_id":"010554",
      "subject":"STAT",
      "catalog_number":"690",
      "title":"Literature and Research Studies"
    },
    {
      "course_id":"010065",
      "subject":"STAT",
      "catalog_number":"830",
      "title":"Experimental Design"
    },
    {
      "course_id":"003087",
      "subject":"STAT",
      "catalog_number":"831",
      "title":"Generalized  Linear Models and Applications"
    },
    {
      "course_id":"003088",
      "subject":"STAT",
      "catalog_number":"833",
      "title":"Stochastic Processes"
    },
    {
      "course_id":"003089",
      "subject":"STAT",
      "catalog_number":"835",
      "title":"Statistical Methods for Process Improvement"
    },
    {
      "course_id":"014078",
      "subject":"STAT",
      "catalog_number":"836",
      "title":"Introduction to the Analysis of Spatial Data in Health Research"
    },
    {
      "course_id":"014081",
      "subject":"STAT",
      "catalog_number":"837",
      "title":"Analysis of Longitudinal Data in Health Research"
    },
    {
      "course_id":"003090",
      "subject":"STAT",
      "catalog_number":"840",
      "title":"Computational Inference"
    },
    {
      "course_id":"003091",
      "subject":"STAT",
      "catalog_number":"841",
      "title":"Statistical Learning - Classification"
    },
    {
      "course_id":"012612",
      "subject":"STAT",
      "catalog_number":"842",
      "title":"Data Visualization"
    },
    {
      "course_id":"003092",
      "subject":"STAT",
      "catalog_number":"844",
      "title":"Statistical Learning - Function Estimation"
    },
    {
      "course_id":"003094",
      "subject":"STAT",
      "catalog_number":"850",
      "title":"Estimation and Hypothesis Testing"
    },
    {
      "course_id":"003097",
      "subject":"STAT",
      "catalog_number":"854",
      "title":"Sampling Theory and Practice"
    },
    {
      "course_id":"010555",
      "subject":"STAT",
      "catalog_number":"890",
      "title":"Topics in Statistics"
    },
    {
      "course_id":"003121",
      "subject":"STAT",
      "catalog_number":"937",
      "title":"Introduction  to Biostatistics and Epidemiology"
    },
    {
      "course_id":"010556",
      "subject":"STAT",
      "catalog_number":"891",
      "title":"Topics in Probability"
    },
    {
      "course_id":"003101",
      "subject":"STAT",
      "catalog_number":"901",
      "title":"Theory of Probability 1"
    },
    {
      "course_id":"003102",
      "subject":"STAT",
      "catalog_number":"902",
      "title":"Theory of Probability 2"
    },
    {
      "course_id":"003104",
      "subject":"STAT",
      "catalog_number":"906",
      "title":"Computer Intensive Methods for Stochastic Models in Finance"
    },
    {
      "course_id":"003105",
      "subject":"STAT",
      "catalog_number":"908",
      "title":"Statistical Inference"
    },
    {
      "course_id":"003113",
      "subject":"STAT",
      "catalog_number":"923",
      "title":"Multivariate Analysis"
    },
    {
      "course_id":"003116",
      "subject":"STAT",
      "catalog_number":"929",
      "title":"Time Series 1"
    },
    {
      "course_id":"003117",
      "subject":"STAT",
      "catalog_number":"930",
      "title":"Time Series 2"
    },
    {
      "course_id":"014341",
      "subject":"STAT",
      "catalog_number":"931",
      "title":"Statistical Methods for the Design and Analysis of Epidemiological Studies"
    },
    {
      "course_id":"014342",
      "subject":"STAT",
      "catalog_number":"932",
      "title":"Statistical Methods for the Design and Analysis of Randomized Intervention Trials"
    },
    {
      "course_id":"003120",
      "subject":"STAT",
      "catalog_number":"935",
      "title":"Analysis of Survival Data"
    },
    {
      "course_id":"013084",
      "subject":"STAT",
      "catalog_number":"936",
      "title":"Longitudinal Data Analysis"
    },
    {
      "course_id":"003122",
      "subject":"STAT",
      "catalog_number":"938",
      "title":"Statistical Consulting"
    },
    {
      "course_id":"010557",
      "subject":"STAT",
      "catalog_number":"946",
      "title":"Topics in Probability and Statistics"
    },
    {
      "course_id":"003144",
      "subject":"SYDE",
      "catalog_number":"622",
      "title":"Machine Intelligence"
    },
    {
      "course_id":"010558",
      "subject":"STAT",
      "catalog_number":"947",
      "title":"Topics in Biostatistics"
    },
    {
      "course_id":"014063",
      "subject":"STAT",
      "catalog_number":"974",
      "title":"Financial Econometrics"
    },
    {
      "course_id":"008896",
      "subject":"STV",
      "catalog_number":"100",
      "title":"Society, Technology and Values: Introduction"
    },
    {
      "course_id":"010150",
      "subject":"STV",
      "catalog_number":"201",
      "title":"Society, Technology and Values: Special Topics"
    },
    {
      "course_id":"008905",
      "subject":"STV",
      "catalog_number":"202",
      "title":"Design and Society"
    },
    {
      "course_id":"008906",
      "subject":"STV",
      "catalog_number":"203",
      "title":"Biotechnology and Society"
    },
    {
      "course_id":"011619",
      "subject":"STV",
      "catalog_number":"205",
      "title":"Cybernetics and Society"
    },
    {
      "course_id":"008908",
      "subject":"STV",
      "catalog_number":"302",
      "title":"Information Technology and Society"
    },
    {
      "course_id":"008909",
      "subject":"STV",
      "catalog_number":"303",
      "title":"Cross-Cultural Change, Technology and Society"
    },
    {
      "course_id":"008910",
      "subject":"STV",
      "catalog_number":"400",
      "title":"Society, Technology and Values: Senior Project"
    },
    {
      "course_id":"010151",
      "subject":"STV",
      "catalog_number":"401",
      "title":"Society, Technology & Values: Advanced Topics"
    },
    {
      "course_id":"011199",
      "subject":"STV",
      "catalog_number":"404",
      "title":"Technology in Canadian Society"
    },
    {
      "course_id":"014470",
      "subject":"SUSM",
      "catalog_number":"601",
      "title":"Foundations for Sustainability Management"
    },
    {
      "course_id":"014471",
      "subject":"SUSM",
      "catalog_number":"602",
      "title":"Theories and Concepts of Sustainability Management"
    },
    {
      "course_id":"014472",
      "subject":"SUSM",
      "catalog_number":"603",
      "title":"Research Methods for Sustainable Management"
    },
    {
      "course_id":"014362",
      "subject":"SUSM",
      "catalog_number":"605",
      "title":"Thesis Development"
    },
    {
      "course_id":"014569",
      "subject":"SUSM",
      "catalog_number":"620",
      "title":"Sustainable Operations"
    },
    {
      "course_id":"014568",
      "subject":"SUSM",
      "catalog_number":"630",
      "title":"Marketing for Sustainability"
    },
    {
      "course_id":"014601",
      "subject":"SUSM",
      "catalog_number":"640",
      "title":"Strategy for Sustainable Enterprises"
    },
    {
      "course_id":"014602",
      "subject":"SUSM",
      "catalog_number":"650",
      "title":"Sustainable Finance"
    },
    {
      "course_id":"014603",
      "subject":"SUSM",
      "catalog_number":"675",
      "title":"Reading Course"
    },
    {
      "course_id":"014192",
      "subject":"SWK",
      "catalog_number":"600R",
      "title":"Diversity and Health"
    },
    {
      "course_id":"014191",
      "subject":"SWK",
      "catalog_number":"601R",
      "title":"Health Policy"
    },
    {
      "course_id":"014193",
      "subject":"SWK",
      "catalog_number":"602R",
      "title":"Social Work Practice in Health"
    },
    {
      "course_id":"014194",
      "subject":"SWK",
      "catalog_number":"603R",
      "title":"Critical Exploration of Supervision and Leadership Roles for Social Worker"
    },
    {
      "course_id":"014195",
      "subject":"SWK",
      "catalog_number":"604R",
      "title":"Evaluation of Health and Human Service Programs"
    },
    {
      "course_id":"014196",
      "subject":"SWK",
      "catalog_number":"605R",
      "title":"Knowledge Mobilization and Evidence-Based Practice"
    },
    {
      "course_id":"014210",
      "subject":"SWK",
      "catalog_number":"608R",
      "title":"Health Issues and Ethics"
    },
    {
      "course_id":"014190",
      "subject":"SWK",
      "catalog_number":"609R",
      "title":"Social Work Practice in Mental Health"
    },
    {
      "course_id":"014653",
      "subject":"SWK",
      "catalog_number":"650R",
      "title":"Interprofessional Pscyhosocail Oncology: Introduction to Theory and Practice"
    },
    {
      "course_id":"014654",
      "subject":"SWK",
      "catalog_number":"651R",
      "title":"Relational Practice with Families"
    },
    {
      "course_id":"014655",
      "subject":"SWK",
      "catalog_number":"652R",
      "title":"Sexual Health & Counseling in Cancer"
    },
    {
      "course_id":"008748",
      "subject":"SWREN",
      "catalog_number":"120R",
      "title":"Introduction to Social Work"
    },
    {
      "course_id":"008749",
      "subject":"SWREN",
      "catalog_number":"220R",
      "title":"Social Work with Individuals - Theory and Practice 1"
    },
    {
      "course_id":"008750",
      "subject":"SWREN",
      "catalog_number":"221R",
      "title":"Social Group Work"
    },
    {
      "course_id":"008751",
      "subject":"SWREN",
      "catalog_number":"222R",
      "title":"Community Organization 1"
    },
    {
      "course_id":"008605",
      "subject":"SWREN",
      "catalog_number":"224R",
      "title":"Poverty in Canada and its Social Consequences"
    },
    {
      "course_id":"006507",
      "subject":"SWREN",
      "catalog_number":"250R",
      "title":"Social Statistics"
    },
    {
      "course_id":"006508",
      "subject":"SWREN",
      "catalog_number":"251R",
      "title":"Social Research"
    },
    {
      "course_id":"008755",
      "subject":"SWREN",
      "catalog_number":"300R",
      "title":"Canadian Social Welfare Policy"
    },
    {
      "course_id":"011116",
      "subject":"SWREN",
      "catalog_number":"301R",
      "title":"Understanding Diversity in Canada"
    },
    {
      "course_id":"011378",
      "subject":"SWREN",
      "catalog_number":"311R",
      "title":"Public Policy and Native Peoples in Canada"
    },
    {
      "course_id":"011979",
      "subject":"SWREN",
      "catalog_number":"312R",
      "title":"Homelessness & Public Policy"
    },
    {
      "course_id":"008758",
      "subject":"SWREN",
      "catalog_number":"321R",
      "title":"Social Work with Families"
    },
    {
      "course_id":"011388",
      "subject":"SWREN",
      "catalog_number":"349R",
      "title":"Cross-Cultural Psychology"
    },
    {
      "course_id":"008915",
      "subject":"SWREN",
      "catalog_number":"411R",
      "title":"Integrative Practice: Aboriginal Perspectives and Social Work"
    },
    {
      "course_id":"008916",
      "subject":"SWREN",
      "catalog_number":"414R",
      "title":"Interviewing and Assessment in Social Work Practice"
    },
    {
      "course_id":"008918",
      "subject":"SWREN",
      "catalog_number":"422R",
      "title":"Advanced Macro Practice"
    },
    {
      "course_id":"012135",
      "subject":"SWREN",
      "catalog_number":"423R",
      "title":"Advanced Social Group Work Practice"
    },
    {
      "course_id":"008919",
      "subject":"SWREN",
      "catalog_number":"424R",
      "title":"Diversity and Empowerment"
    },
    {
      "course_id":"008920",
      "subject":"SWREN",
      "catalog_number":"431R",
      "title":"Fields of Practice"
    },
    {
      "course_id":"008921",
      "subject":"SWREN",
      "catalog_number":"434R",
      "title":"Selected Theories for Social Work Practice: Analysis and Application"
    },
    {
      "course_id":"012395",
      "subject":"SWREN",
      "catalog_number":"441A",
      "title":"Practicum 1A"
    },
    {
      "course_id":"012396",
      "subject":"SWREN",
      "catalog_number":"441B",
      "title":"Practicum 1B"
    },
    {
      "course_id":"008922",
      "subject":"SWREN",
      "catalog_number":"441R",
      "title":"Practicum 1"
    },
    {
      "course_id":"012397",
      "subject":"SWREN",
      "catalog_number":"442A",
      "title":"Practicum 2A"
    },
    {
      "course_id":"012398",
      "subject":"SWREN",
      "catalog_number":"442B",
      "title":"Practicum 2B"
    },
    {
      "course_id":"008923",
      "subject":"SWREN",
      "catalog_number":"442R",
      "title":"Practicum 2"
    },
    {
      "course_id":"012399",
      "subject":"SWREN",
      "catalog_number":"443A",
      "title":"Practicum 3A"
    },
    {
      "course_id":"012400",
      "subject":"SWREN",
      "catalog_number":"443B",
      "title":"Practicum 3B"
    },
    {
      "course_id":"008924",
      "subject":"SWREN",
      "catalog_number":"443R",
      "title":"Practicum 3"
    },
    {
      "course_id":"012671",
      "subject":"SWREN",
      "catalog_number":"470R",
      "title":"Mental Health and Addiction Issues: Social Work Responses"
    },
    {
      "course_id":"012672",
      "subject":"SWREN",
      "catalog_number":"471R",
      "title":"Social Work with Older Adults: Critical Issues and Future Trends"
    },
    {
      "course_id":"012673",
      "subject":"SWREN",
      "catalog_number":"472R",
      "title":"International Context of Practice: An Experiential Learning Opportunity"
    },
    {
      "course_id":"009341",
      "subject":"SYDE",
      "catalog_number":"101",
      "title":"Introduction to Systems Design Engineering"
    },
    {
      "course_id":"012857",
      "subject":"SYDE",
      "catalog_number":"101L",
      "title":"Graphics Laboratory"
    },
    {
      "course_id":"009342",
      "subject":"SYDE",
      "catalog_number":"102",
      "title":"Seminar"
    },
    {
      "course_id":"008925",
      "subject":"SYDE",
      "catalog_number":"111",
      "title":"Fundamental Engineering Math 1"
    },
    {
      "course_id":"008926",
      "subject":"SYDE",
      "catalog_number":"112",
      "title":"Fundamental Engineering Math 2"
    },
    {
      "course_id":"013144",
      "subject":"SYDE",
      "catalog_number":"113",
      "title":"Matrices and Linear Systems"
    },
    {
      "course_id":"008948",
      "subject":"SYDE",
      "catalog_number":"281",
      "title":"Mechanics of Deformable Solids"
    },
    {
      "course_id":"008928",
      "subject":"SYDE",
      "catalog_number":"114",
      "title":"Numerical and Applied Calculus"
    },
    {
      "course_id":"008929",
      "subject":"SYDE",
      "catalog_number":"121",
      "title":"Digital Computation"
    },
    {
      "course_id":"008933",
      "subject":"SYDE",
      "catalog_number":"161",
      "title":"Introduction to Design"
    },
    {
      "course_id":"008932",
      "subject":"SYDE",
      "catalog_number":"162",
      "title":"Human Factors in Design"
    },
    {
      "course_id":"008934",
      "subject":"SYDE",
      "catalog_number":"181",
      "title":"Physics 1 (Statics)"
    },
    {
      "course_id":"008935",
      "subject":"SYDE",
      "catalog_number":"182",
      "title":"Physics 2 (Dynamics)"
    },
    {
      "course_id":"008938",
      "subject":"SYDE",
      "catalog_number":"192",
      "title":"Digital Systems"
    },
    {
      "course_id":"012858",
      "subject":"SYDE",
      "catalog_number":"192L",
      "title":"Digital Systems Laboratory"
    },
    {
      "course_id":"009343",
      "subject":"SYDE",
      "catalog_number":"201",
      "title":"Seminar"
    },
    {
      "course_id":"009344",
      "subject":"SYDE",
      "catalog_number":"202",
      "title":"Seminar"
    },
    {
      "course_id":"008939",
      "subject":"SYDE",
      "catalog_number":"211",
      "title":"Advanced Engineering Math 1"
    },
    {
      "course_id":"013145",
      "subject":"SYDE",
      "catalog_number":"212",
      "title":"Probability and Statistics"
    },
    {
      "course_id":"008957",
      "subject":"SYDE",
      "catalog_number":"223",
      "title":"Data Structures and Algorithms"
    },
    {
      "course_id":"008945",
      "subject":"SYDE",
      "catalog_number":"252",
      "title":"Linear Systems and Signals"
    },
    {
      "course_id":"012861",
      "subject":"SYDE",
      "catalog_number":"261",
      "title":"Design, Systems, and Society"
    },
    {
      "course_id":"008958",
      "subject":"SYDE",
      "catalog_number":"262",
      "title":"Engineering Economics of Design"
    },
    {
      "course_id":"008950",
      "subject":"SYDE",
      "catalog_number":"283",
      "title":"Physics 3 (Electricity, Magnetism and Optics)"
    },
    {
      "course_id":"008936",
      "subject":"SYDE",
      "catalog_number":"285",
      "title":"Materials Chemistry"
    },
    {
      "course_id":"008948",
      "subject":"SYDE",
      "catalog_number":"286",
      "title":"Mechanics of Deformable Solids"
    },
    {
      "course_id":"008952",
      "subject":"SYDE",
      "catalog_number":"292",
      "title":"Circuits, Instrumentation, and Measurements"
    },
    {
      "course_id":"012859",
      "subject":"SYDE",
      "catalog_number":"292L",
      "title":"Circuits, Instrumentation, and Measurements Laboratory"
    },
    {
      "course_id":"009345",
      "subject":"SYDE",
      "catalog_number":"301",
      "title":"Seminar"
    },
    {
      "course_id":"009346",
      "subject":"SYDE",
      "catalog_number":"302",
      "title":"Seminar"
    },
    {
      "course_id":"008953",
      "subject":"SYDE",
      "catalog_number":"311",
      "title":"Advanced Engineering Math 2"
    },
    {
      "course_id":"008954",
      "subject":"SYDE",
      "catalog_number":"312",
      "title":"Applied Linear Algebra"
    },
    {
      "course_id":"008943",
      "subject":"SYDE",
      "catalog_number":"322",
      "title":"Software Design"
    },
    {
      "course_id":"013382",
      "subject":"SYDE",
      "catalog_number":"332",
      "title":"Societal and Environmental Systems"
    },
    {
      "course_id":"008961",
      "subject":"SYDE",
      "catalog_number":"334",
      "title":"Applied Statistics"
    },
    {
      "course_id":"010066",
      "subject":"SYDE",
      "catalog_number":"348",
      "title":"User Centred Design Methods"
    },
    {
      "course_id":"008981",
      "subject":"SYDE",
      "catalog_number":"422",
      "title":"Machine Intelligence"
    },
    {
      "course_id":"008964",
      "subject":"SYDE",
      "catalog_number":"351",
      "title":"Systems Models 1"
    },
    {
      "course_id":"008965",
      "subject":"SYDE",
      "catalog_number":"352",
      "title":"Introduction to Control Systems"
    },
    {
      "course_id":"012860",
      "subject":"SYDE",
      "catalog_number":"352L",
      "title":"Control Systems Laboratory"
    },
    {
      "course_id":"008968",
      "subject":"SYDE",
      "catalog_number":"361",
      "title":"Engineering Design"
    },
    {
      "course_id":"008969",
      "subject":"SYDE",
      "catalog_number":"362",
      "title":"Systems Design Workshop 1"
    },
    {
      "course_id":"008972",
      "subject":"SYDE",
      "catalog_number":"372",
      "title":"Introduction to Pattern Recognition"
    },
    {
      "course_id":"008973",
      "subject":"SYDE",
      "catalog_number":"381",
      "title":"Thermodynamics"
    },
    {
      "course_id":"008949",
      "subject":"SYDE",
      "catalog_number":"383",
      "title":"Fluid Mechanics"
    },
    {
      "course_id":"013384",
      "subject":"SYDE",
      "catalog_number":"384",
      "title":"Biological and Human Systems"
    },
    {
      "course_id":"009347",
      "subject":"SYDE",
      "catalog_number":"401",
      "title":"Seminar"
    },
    {
      "course_id":"009348",
      "subject":"SYDE",
      "catalog_number":"402",
      "title":"Seminar"
    },
    {
      "course_id":"013146",
      "subject":"SYDE",
      "catalog_number":"411",
      "title":"Optimization and Numerical Methods"
    },
    {
      "course_id":"008993",
      "subject":"SYDE",
      "catalog_number":"461",
      "title":"Systems Design Workshop 2"
    },
    {
      "course_id":"008994",
      "subject":"SYDE",
      "catalog_number":"462",
      "title":"Systems Design Workshop 3"
    },
    {
      "course_id":"008981",
      "subject":"SYDE",
      "catalog_number":"522",
      "title":"Machine Intelligence"
    },
    {
      "course_id":"013383",
      "subject":"SYDE",
      "catalog_number":"531",
      "title":"Design Optimization Under Probabilistic Uncertainty"
    },
    {
      "course_id":"009003",
      "subject":"SYDE",
      "catalog_number":"533",
      "title":"Conflict Resolution"
    },
    {
      "course_id":"010067",
      "subject":"SYDE",
      "catalog_number":"542",
      "title":"Interface Design"
    },
    {
      "course_id":"009006",
      "subject":"SYDE",
      "catalog_number":"543",
      "title":"Cognitive Ergonomics"
    },
    {
      "course_id":"008988",
      "subject":"SYDE",
      "catalog_number":"544",
      "title":"Biomedical Measurement and Signal Processing"
    },
    {
      "course_id":"014290",
      "subject":"SYDE",
      "catalog_number":"552",
      "title":"Computational Neuroscience"
    },
    {
      "course_id":"009010",
      "subject":"SYDE",
      "catalog_number":"553",
      "title":"Advanced Dynamics"
    },
    {
      "course_id":"012084",
      "subject":"SYDE",
      "catalog_number":"556",
      "title":"Simulating Neurobiological Systems"
    },
    {
      "course_id":"009016",
      "subject":"SYDE",
      "catalog_number":"575",
      "title":"Image Processing"
    },
    {
      "course_id":"003143",
      "subject":"SYDE",
      "catalog_number":"621",
      "title":"Mathematics of Computation"
    },
    {
      "course_id":"003146",
      "subject":"SYDE",
      "catalog_number":"625",
      "title":"Tools of Intelligent Systems Design"
    },
    {
      "course_id":"003147",
      "subject":"SYDE",
      "catalog_number":"631",
      "title":"Time Series Modelling"
    },
    {
      "course_id":"003148",
      "subject":"SYDE",
      "catalog_number":"632",
      "title":"Optimization Methods"
    },
    {
      "course_id":"014482",
      "subject":"SYDE",
      "catalog_number":"633",
      "title":"Remote Sensing Systems"
    },
    {
      "course_id":"003149",
      "subject":"SYDE",
      "catalog_number":"642",
      "title":"Cognitive Engineering Methods"
    },
    {
      "course_id":"003155",
      "subject":"SYDE",
      "catalog_number":"676",
      "title":"Information Theory in Pattern Synthesis and Analysis"
    },
    {
      "course_id":"014495",
      "subject":"SYDE",
      "catalog_number":"643",
      "title":"Collaborative Systems Design"
    },
    {
      "course_id":"014497",
      "subject":"SYDE",
      "catalog_number":"644",
      "title":"Human Factors Testing"
    },
    {
      "course_id":"003151",
      "subject":"SYDE",
      "catalog_number":"652",
      "title":"Dynamics of Multibody  Systems"
    },
    {
      "course_id":"003153",
      "subject":"SYDE",
      "catalog_number":"654",
      "title":"Graphic Theoretic Models for Complex Systems"
    },
    {
      "course_id":"014498",
      "subject":"SYDE",
      "catalog_number":"655",
      "title":"Optimal Control"
    },
    {
      "course_id":"014490",
      "subject":"SYDE",
      "catalog_number":"661",
      "title":"Model-Based Robust Design"
    },
    {
      "course_id":"014499",
      "subject":"SYDE",
      "catalog_number":"671",
      "title":"Advanced Image Processing"
    },
    {
      "course_id":"014491",
      "subject":"SYDE",
      "catalog_number":"672",
      "title":"Statistical Image Processing"
    },
    {
      "course_id":"014492",
      "subject":"SYDE",
      "catalog_number":"673",
      "title":"Video Processing and Analysis"
    },
    {
      "course_id":"014493",
      "subject":"SYDE",
      "catalog_number":"674",
      "title":"3D Computer Vision"
    },
    {
      "course_id":"003154",
      "subject":"SYDE",
      "catalog_number":"675",
      "title":"Pattern Recognition"
    },
    {
      "course_id":"003156",
      "subject":"SYDE",
      "catalog_number":"677",
      "title":"Medical Imaging"
    },
    {
      "course_id":"012235",
      "subject":"SYDE",
      "catalog_number":"682",
      "title":"Advanced MicroElectroMechanical Systems:  Principles, Design & Fabrication"
    },
    {
      "course_id":"014494",
      "subject":"SYDE",
      "catalog_number":"683",
      "title":"Modeling, Simulation and Design of MEMS and NEMS"
    },
    {
      "course_id":"014500",
      "subject":"SYDE",
      "catalog_number":"684",
      "title":"Materials Biocompatibility"
    },
    {
      "course_id":"003163",
      "subject":"SYDE",
      "catalog_number":"710",
      "title":"Topics in Mathematics"
    },
    {
      "course_id":"003173",
      "subject":"SYDE",
      "catalog_number":"720",
      "title":"Selected Topics in Computation"
    },
    {
      "course_id":"003183",
      "subject":"SYDE",
      "catalog_number":"730",
      "title":"Selected Topics in Societal-Environmental Systems"
    },
    {
      "course_id":"010502",
      "subject":"SYDE",
      "catalog_number":"740",
      "title":"Selected Topics in Human Systems"
    },
    {
      "course_id":"003199",
      "subject":"SYDE",
      "catalog_number":"750",
      "title":"Topics in Systems Modelling"
    },
    {
      "course_id":"003209",
      "subject":"SYDE",
      "catalog_number":"760",
      "title":"Topics in Engineering Design"
    },
    {
      "course_id":"003214",
      "subject":"SYDE",
      "catalog_number":"770",
      "title":"Selected Topics in Communication and Information Systems"
    },
    {
      "course_id":"003224",
      "subject":"SYDE",
      "catalog_number":"780",
      "title":"Selected Topics in Engineering Sciences"
    },
    {
      "course_id":"010293",
      "subject":"TAX",
      "catalog_number":"600",
      "title":"Introductory Tax and Accounting for MTax Students"
    },
    {
      "course_id":"010289",
      "subject":"TAX",
      "catalog_number":"615",
      "title":"Taxation and Finance"
    },
    {
      "course_id":"010294",
      "subject":"TAX",
      "catalog_number":"616",
      "title":"Tax Research and Statutory Interpretation"
    },
    {
      "course_id":"010290",
      "subject":"TAX",
      "catalog_number":"617",
      "title":"Integration of Tax\/Audit\/Accounting"
    },
    {
      "course_id":"012178",
      "subject":"TAX",
      "catalog_number":"619",
      "title":"Taxation of Corporations"
    },
    {
      "course_id":"012179",
      "subject":"TAX",
      "catalog_number":"620",
      "title":"Introduction to Business Structuring"
    },
    {
      "course_id":"010292",
      "subject":"TAX",
      "catalog_number":"625",
      "title":"Tax Policy"
    },
    {
      "course_id":"010465",
      "subject":"TAX",
      "catalog_number":"626",
      "title":"Business Structuring"
    },
    {
      "course_id":"010295",
      "subject":"TAX",
      "catalog_number":"627",
      "title":"International Tax I"
    },
    {
      "course_id":"010296",
      "subject":"TAX",
      "catalog_number":"628",
      "title":"Tax Planning for the Owner-Manager and Executive"
    },
    {
      "course_id":"012180",
      "subject":"TAX",
      "catalog_number":"629",
      "title":"Tax Risk Management"
    },
    {
      "course_id":"010297",
      "subject":"TAX",
      "catalog_number":"635",
      "title":"The Microeconomic Approach to Tax Planning"
    },
    {
      "course_id":"010466",
      "subject":"TAX",
      "catalog_number":"636",
      "title":"Estate & Retirement Planning"
    },
    {
      "course_id":"010467",
      "subject":"TAX",
      "catalog_number":"637",
      "title":"International Tax II"
    },
    {
      "course_id":"010468",
      "subject":"TAX",
      "catalog_number":"638",
      "title":"Research Paper"
    },
    {
      "course_id":"010469",
      "subject":"TAX",
      "catalog_number":"690",
      "title":"Topics in Taxation"
    },
    {
      "course_id":"013355",
      "subject":"TN",
      "catalog_number":"700",
      "title":"Theoretical Neuroscience Research Seminar"
    },
    {
      "course_id":"001400",
      "subject":"TOUR",
      "catalog_number":"601",
      "title":"Contemporary Perspectives on Tourism"
    },
    {
      "course_id":"010723",
      "subject":"TOUR",
      "catalog_number":"602",
      "title":"Seminar on Tourism Research"
    },
    {
      "course_id":"010724",
      "subject":"TOUR",
      "catalog_number":"603",
      "title":"Sustainable Tourism"
    },
    {
      "course_id":"010725",
      "subject":"TOUR",
      "catalog_number":"604",
      "title":"Social Planning for Tourism"
    },
    {
      "course_id":"010726",
      "subject":"TOUR",
      "catalog_number":"609",
      "title":"Practicum in Tourism"
    },
    {
      "course_id":"010727",
      "subject":"TOUR",
      "catalog_number":"675",
      "title":"Selected Topics in Tourism"
    },
    {
      "course_id":"012796",
      "subject":"TS",
      "catalog_number":"600",
      "title":"Thinking Theologically"
    },
    {
      "course_id":"012797",
      "subject":"TS",
      "catalog_number":"601",
      "title":"Special Topics in Theological Studies"
    },
    {
      "course_id":"012798",
      "subject":"TS",
      "catalog_number":"603",
      "title":"Intermediate Biblical Hebrew"
    },
    {
      "course_id":"012799",
      "subject":"TS",
      "catalog_number":"607",
      "title":"Intermediate Biblical Greek"
    },
    {
      "course_id":"012842",
      "subject":"TS",
      "catalog_number":"610",
      "title":"Reading and Teaching the Old Testament"
    },
    {
      "course_id":"012843",
      "subject":"TS",
      "catalog_number":"611",
      "title":"Reading and Teaching the New Testament"
    },
    {
      "course_id":"012800",
      "subject":"TS",
      "catalog_number":"613",
      "title":"Special Topics in Old Testament Themes"
    },
    {
      "course_id":"012801",
      "subject":"TS",
      "catalog_number":"617",
      "title":"Unity and Diversity in the New Testament"
    },
    {
      "course_id":"012802",
      "subject":"TS",
      "catalog_number":"619",
      "title":"The Bible and Peace"
    },
    {
      "course_id":"012803",
      "subject":"TS",
      "catalog_number":"621",
      "title":"Special Topics: Pastor's Theology Seminar"
    },
    {
      "course_id":"012804",
      "subject":"TS",
      "catalog_number":"631",
      "title":"Contemporary Christian Theology"
    },
    {
      "course_id":"012805",
      "subject":"TS",
      "catalog_number":"632",
      "title":"Modern Christian Thought"
    },
    {
      "course_id":"012806",
      "subject":"TS",
      "catalog_number":"633",
      "title":"Comtemporary Mennonite Theology"
    },
    {
      "course_id":"012807",
      "subject":"TS",
      "catalog_number":"635",
      "title":"Christian Ethics"
    },
    {
      "course_id":"012808",
      "subject":"TS",
      "catalog_number":"636",
      "title":"Christian Approaches to Peacemaking"
    },
    {
      "course_id":"012809",
      "subject":"TS",
      "catalog_number":"637",
      "title":"War and Peace in Christian Theology"
    },
    {
      "course_id":"012810",
      "subject":"TS",
      "catalog_number":"638",
      "title":"Doing Development: Issues of Justice and Peace"
    },
    {
      "course_id":"012811",
      "subject":"TS",
      "catalog_number":"640",
      "title":"The Mennonite Tradition in Historical Context"
    },
    {
      "course_id":"012812",
      "subject":"TS",
      "catalog_number":"642",
      "title":"The Radical Reformation"
    },
    {
      "course_id":"012813",
      "subject":"TS",
      "catalog_number":"645",
      "title":"Reformation History"
    },
    {
      "course_id":"012814",
      "subject":"TS",
      "catalog_number":"647",
      "title":"Global Christianity"
    },
    {
      "course_id":"012815",
      "subject":"TS",
      "catalog_number":"651",
      "title":"Christian Worship"
    },
    {
      "course_id":"012816",
      "subject":"TS",
      "catalog_number":"652",
      "title":"Christian Hymnody"
    },
    {
      "course_id":"012817",
      "subject":"TS",
      "catalog_number":"653",
      "title":"Worship and Music"
    },
    {
      "course_id":"012818",
      "subject":"TS",
      "catalog_number":"662",
      "title":"Dietrich Bonhoeffer: Life and Thought"
    },
    {
      "course_id":"012819",
      "subject":"TS",
      "catalog_number":"670",
      "title":"War and Peace in Christian Thought"
    },
    {
      "course_id":"012820",
      "subject":"TS",
      "catalog_number":"674",
      "title":"Church Mission"
    },
    {
      "course_id":"012821",
      "subject":"TS",
      "catalog_number":"677",
      "title":"Church and Ministry"
    },
    {
      "course_id":"012822",
      "subject":"TS",
      "catalog_number":"678",
      "title":"The Minister in the Church: Supervised Experience in Ministry I"
    },
    {
      "course_id":"012823",
      "subject":"TS",
      "catalog_number":"679",
      "title":"The Minister in the Church: Supervised Experience in Ministry II"
    },
    {
      "course_id":"012824",
      "subject":"TS",
      "catalog_number":"681",
      "title":"Personal Spirituality: Practices for Daily Living"
    },
    {
      "course_id":"012825",
      "subject":"TS",
      "catalog_number":"684",
      "title":"Pastoral Care"
    },
    {
      "course_id":"012826",
      "subject":"TS",
      "catalog_number":"689",
      "title":"Aging and the Spiritual Life"
    },
    {
      "course_id":"012827",
      "subject":"TS",
      "catalog_number":"690",
      "title":"Seminars in Theological Studies"
    },
    {
      "course_id":"012788",
      "subject":"TS",
      "catalog_number":"691",
      "title":"Selected Special Topics in Theological Studies"
    },
    {
      "course_id":"009496",
      "subject":"CM",
      "catalog_number":"370",
      "title":"Chaos and Fractals"
    },
    {
      "course_id":"012828",
      "subject":"TS",
      "catalog_number":"692",
      "title":"Workshops in Theological Studies"
    },
    {
      "course_id":"012829",
      "subject":"TS",
      "catalog_number":"699",
      "title":"Historical\/Cultural Travel Courses"
    },
    {
      "course_id":"012771",
      "subject":"TS",
      "catalog_number":"715",
      "title":"Special Topics in Old Testament Exegesis"
    },
    {
      "course_id":"012831",
      "subject":"TS",
      "catalog_number":"718",
      "title":"Special Topics in New Testament Exegesis"
    },
    {
      "course_id":"012832",
      "subject":"TS",
      "catalog_number":"724",
      "title":"Biblical Foundations of Peace"
    },
    {
      "course_id":"012833",
      "subject":"TS",
      "catalog_number":"731",
      "title":"Christianity's Encounter with Other Faiths"
    },
    {
      "course_id":"012834",
      "subject":"TS",
      "catalog_number":"735",
      "title":"Theological Perspectives on Peace Issues"
    },
    {
      "course_id":"012835",
      "subject":"TS",
      "catalog_number":"738",
      "title":"Systematic Theology"
    },
    {
      "course_id":"012836",
      "subject":"TS",
      "catalog_number":"746",
      "title":"Anabaptist Spirituality in Historical Context"
    },
    {
      "course_id":"012837",
      "subject":"TS",
      "catalog_number":"751",
      "title":"Worship Ritual and Ministry"
    },
    {
      "course_id":"012838",
      "subject":"TS",
      "catalog_number":"779",
      "title":"Specialized Supervised Experience."
    },
    {
      "course_id":"012839",
      "subject":"TS",
      "catalog_number":"783",
      "title":"Integration Seminar"
    },
    {
      "course_id":"012840",
      "subject":"TS",
      "catalog_number":"787",
      "title":"Spiritual Guidance Seminar"
    },
    {
      "course_id":"012841",
      "subject":"TS",
      "catalog_number":"792",
      "title":"Special Topics Seminars"
    },
    {
      "course_id":"012937",
      "subject":"TS",
      "catalog_number":"796",
      "title":"Thesis Preparation"
    },
    {
      "course_id":"012938",
      "subject":"TS",
      "catalog_number":"798",
      "title":"Thesis Preparation"
    },
    {
      "course_id":"012162",
      "subject":"UN",
      "catalog_number":"700",
      "title":"Industrial Research Project in Nuclear Engineering"
    },
    {
      "course_id":"012163",
      "subject":"UN",
      "catalog_number":"701",
      "title":"Engineering Risk and Reliability Analysis"
    },
    {
      "course_id":"012253",
      "subject":"UN",
      "catalog_number":"702",
      "title":"Power Plant Thermodynamics"
    },
    {
      "course_id":"012254",
      "subject":"UN",
      "catalog_number":"799",
      "title":"Special Topics in Nuclear Engineering"
    },
    {
      "course_id":"012296",
      "subject":"UN",
      "catalog_number":"801",
      "title":"Nuclear Plant Systems and Operations Test"
    },
    {
      "course_id":"012297",
      "subject":"UN",
      "catalog_number":"802",
      "title":"Reactor Physics"
    },
    {
      "course_id":"014171",
      "subject":"UNIV",
      "catalog_number":"101",
      "title":"Strategies and Skills for Academic Success"
    },
    {
      "course_id":"013621",
      "subject":"VCULT",
      "catalog_number":"100",
      "title":"World Cinema and Visual Culture"
    },
    {
      "course_id":"013622",
      "subject":"VCULT",
      "catalog_number":"101",
      "title":"Art History and Visual Culture"
    },
    {
      "course_id":"013623",
      "subject":"VCULT",
      "catalog_number":"200",
      "title":"Visual Studies Across the Discipline"
    },
    {
      "course_id":"013624",
      "subject":"VCULT",
      "catalog_number":"300",
      "title":"Visual Culture in Theory"
    },
    {
      "course_id":"014565",
      "subject":"WATER",
      "catalog_number":"601",
      "title":"Integrated Water Management"
    },
    {
      "course_id":"014566",
      "subject":"WATER",
      "catalog_number":"602",
      "title":"Integrated Water Management Project"
    },
    {
      "course_id":"014567",
      "subject":"WATER",
      "catalog_number":"620",
      "title":"Sustainable Operations"
    },
    {
      "course_id":"014272",
      "subject":"WKRPT",
      "catalog_number":"1",
      "title":"Work-term Report"
    },
    {
      "course_id":"014273",
      "subject":"WKRPT",
      "catalog_number":"2",
      "title":"Work-term Report"
    },
    {
      "course_id":"014274",
      "subject":"WKRPT",
      "catalog_number":"3",
      "title":"Work-term Report"
    },
    {
      "course_id":"014275",
      "subject":"WKRPT",
      "catalog_number":"4",
      "title":"Work-term Report"
    },
    {
      "course_id":"009046",
      "subject":"WKRPT",
      "catalog_number":"100",
      "title":"Work-term Report"
    },
    {
      "course_id":"013195",
      "subject":"WKRPT",
      "catalog_number":"101",
      "title":"Work-term Report"
    },
    {
      "course_id":"014336",
      "subject":"WKRPT",
      "catalog_number":"103",
      "title":"Work-term Report"
    },
    {
      "course_id":"009047",
      "subject":"WKRPT",
      "catalog_number":"200",
      "title":"Work-term Report"
    },
    {
      "course_id":"013196",
      "subject":"WKRPT",
      "catalog_number":"201",
      "title":"Work-term Report"
    },
    {
      "course_id":"014337",
      "subject":"WKRPT",
      "catalog_number":"203",
      "title":"Work-term Report"
    },
    {
      "course_id":"009048",
      "subject":"WKRPT",
      "catalog_number":"300",
      "title":"Work-term Report"
    },
    {
      "course_id":"013197",
      "subject":"WKRPT",
      "catalog_number":"301",
      "title":"Work-term Report"
    },
    {
      "course_id":"014338",
      "subject":"WKRPT",
      "catalog_number":"303",
      "title":"Work-term Report"
    },
    {
      "course_id":"009049",
      "subject":"WKRPT",
      "catalog_number":"400",
      "title":"Work-term Report"
    },
    {
      "course_id":"013198",
      "subject":"WKRPT",
      "catalog_number":"401",
      "title":"Work-term Report"
    },
    {
      "course_id":"009029",
      "subject":"WS",
      "catalog_number":"101",
      "title":"An Introduction to Women's Studies"
    },
    {
      "course_id":"012196",
      "subject":"WS",
      "catalog_number":"102",
      "title":"Contemporary Women's Issues in Canada"
    },
    {
      "course_id":"005049",
      "subject":"WS",
      "catalog_number":"108E",
      "title":"Women in Literature"
    },
    {
      "course_id":"009032",
      "subject":"WS",
      "catalog_number":"201",
      "title":"Images of Women in Popular Culture"
    },
    {
      "course_id":"012301",
      "subject":"WS",
      "catalog_number":"202",
      "title":"Women Across Cultures: Canadian and Global Perspectives"
    },
    {
      "course_id":"011699",
      "subject":"WS",
      "catalog_number":"205",
      "title":"Gender, Culture and Technology"
    },
    {
      "course_id":"012768",
      "subject":"WS",
      "catalog_number":"206",
      "title":"Women and the Law"
    },
    {
      "course_id":"011705",
      "subject":"WS",
      "catalog_number":"207",
      "title":"Women and Entrepreneurship"
    },
    {
      "course_id":"005084",
      "subject":"WS",
      "catalog_number":"208E",
      "title":"Women Writing since 1900"
    },
    {
      "course_id":"008588",
      "subject":"WS",
      "catalog_number":"209",
      "title":"Gender Relations"
    },
    {
      "course_id":"007253",
      "subject":"WS",
      "catalog_number":"222",
      "title":"Gender Issues"
    },
    {
      "course_id":"008331",
      "subject":"WS",
      "catalog_number":"261",
      "title":"Women and the Great Religions"
    },
    {
      "course_id":"013221",
      "subject":"WS",
      "catalog_number":"262",
      "title":"Global Queer Cinema"
    },
    {
      "course_id":"011198",
      "subject":"WS",
      "catalog_number":"281",
      "title":"Women in Russia: The Conscience of a Nation"
    },
    {
      "course_id":"012319",
      "subject":"WS",
      "catalog_number":"302",
      "title":"Thinking Through Gender: Feminist Perspectives"
    },
    {
      "course_id":"012750",
      "subject":"WS",
      "catalog_number":"306",
      "title":"Contemporary Health Issues for Women"
    },
    {
      "course_id":"008200",
      "subject":"WS",
      "catalog_number":"308",
      "title":"Gender and Leisure"
    },
    {
      "course_id":"012739",
      "subject":"WS",
      "catalog_number":"320",
      "title":"Sex and the World Religions"
    },
    {
      "course_id":"012264",
      "subject":"WS",
      "catalog_number":"321",
      "title":"Women in Buddhism: A Global Perspective"
    },
    {
      "course_id":"012265",
      "subject":"WS",
      "catalog_number":"322",
      "title":"Images of the Feminine: India"
    },
    {
      "course_id":"012268",
      "subject":"WS",
      "catalog_number":"323",
      "title":"Gender and Asian Religions"
    },
    {
      "course_id":"012931",
      "subject":"WS",
      "catalog_number":"325",
      "title":"Austen"
    },
    {
      "course_id":"011121",
      "subject":"WS",
      "catalog_number":"331",
      "title":"Gender in War and Peace"
    },
    {
      "course_id":"007042",
      "subject":"WS",
      "catalog_number":"334",
      "title":"Women, Music and Gender"
    },
    {
      "course_id":"014231",
      "subject":"WS",
      "catalog_number":"347",
      "title":"Witches, Wives, and Whores"
    },
    {
      "course_id":"009036",
      "subject":"WS",
      "catalog_number":"365",
      "title":"Special Topics in Women's Studies"
    },
    {
      "course_id":"013233",
      "subject":"WS",
      "catalog_number":"370",
      "title":"Women Writers of the Italian Renaissance"
    },
    {
      "course_id":"008702",
      "subject":"WS",
      "catalog_number":"409",
      "title":"Theoretical Perspectives on Gender"
    },
    {
      "course_id":"014558",
      "subject":"WS",
      "catalog_number":"410F",
      "title":"Eighteenth-Century Women Writers"
    },
    {
      "course_id":"007335",
      "subject":"WS",
      "catalog_number":"422",
      "title":"Studies in Feminist Philosophy\/Philosophy of Sex"
    },
    {
      "course_id":"010352",
      "subject":"WS",
      "catalog_number":"430",
      "title":"Literary Women in Early Modern Hispanic Culture"
    },
    {
      "course_id":"009041",
      "subject":"WS",
      "catalog_number":"475",
      "title":"Advanced Research Project in Women's Studies"
    },
    {
      "course_id":"013230",
      "subject":"WS",
      "catalog_number":"499A",
      "title":"Senior Honours Thesis"
    },
    {
      "course_id":"013231",
      "subject":"WS",
      "catalog_number":"499B",
      "title":"Senior Honours Thesis"
    },
    {
      "course_id":"010452",
      "subject":"WS",
      "catalog_number":"601",
      "title":"Advanced Feminist Theory: Special Topics in Women's Issues"
    },
    {
      "course_id":"003056",
      "subject":"WS",
      "catalog_number":"602",
      "title":"Theories of Gender Relations"
    },
    {
      "course_id":"010454",
      "subject":"WS",
      "catalog_number":"680",
      "title":"Directed Readings in Selected Topics"
    },
    {
      "course_id":"010014",
      "subject":"AFM",
      "catalog_number":"480",
      "title":"Selected Problems and Cases in Managerial Accounting"
    },
    {
      "course_id":"003325",
      "subject":"AMATH",
      "catalog_number":"333",
      "title":"Elementary Differential Geometry"
    },
    {
      "course_id":"003348",
      "subject":"AMATH",
      "catalog_number":"431",
      "title":"Measure and Integration"
    },
    {
      "course_id":"003349",
      "subject":"AMATH",
      "catalog_number":"432",
      "title":"Functional Analysis"
    },
    {
      "course_id":"003350",
      "subject":"AMATH",
      "catalog_number":"433",
      "title":"Differential Geometry"
    },
    {
      "course_id":"004436",
      "subject":"AMATH",
      "catalog_number":"447",
      "title":"Introduction to Symbolic Computation"
    },
    {
      "course_id":"003373",
      "subject":"AMATH",
      "catalog_number":"477",
      "title":"Statistical Mechanics"
    },
    {
      "course_id":"003395",
      "subject":"ANTH",
      "catalog_number":"103",
      "title":"The Nature of Language"
    },
    {
      "course_id":"003401",
      "subject":"ANTH",
      "catalog_number":"203",
      "title":"The Archaeology of North America"
    },
    {
      "course_id":"003406",
      "subject":"ANTH",
      "catalog_number":"210",
      "title":"Anthropology Through Science Fiction"
    },
    {
      "course_id":"003420",
      "subject":"ANTH",
      "catalog_number":"229",
      "title":"Peoples of Africa"
    },
    {
      "course_id":"003421",
      "subject":"ANTH",
      "catalog_number":"230",
      "title":"Native Peoples of Canada"
    },
    {
      "course_id":"003440",
      "subject":"ANTH",
      "catalog_number":"311",
      "title":"Anthropology of Religion"
    },
    {
      "course_id":"009883",
      "subject":"ANTH",
      "catalog_number":"335",
      "title":"Arctic Archaeology"
    },
    {
      "course_id":"003461",
      "subject":"ANTH",
      "catalog_number":"350",
      "title":"Anthropology of Gender"
    },
    {
      "course_id":"010107",
      "subject":"ANTH",
      "catalog_number":"380",
      "title":"Matrilineal Societies in Aboriginal North America"
    },
    {
      "course_id":"003476",
      "subject":"ANTH",
      "catalog_number":"404",
      "title":"Human Development in a Cross-Cultural Perspective"
    },
    {
      "course_id":"009884",
      "subject":"ANTH",
      "catalog_number":"411",
      "title":"Symbolic Anthropology"
    },
    {
      "course_id":"003478",
      "subject":"ANTH",
      "catalog_number":"420",
      "title":"Social and Cultural Change"
    },
    {
      "course_id":"013723",
      "subject":"ARBUS",
      "catalog_number":"204",
      "title":"Leadership, Teams, and Communication"
    },
    {
      "course_id":"003483",
      "subject":"ANTH",
      "catalog_number":"461",
      "title":"Selected Topics in Primate Behaviour"
    },
    {
      "course_id":"004894",
      "subject":"ARBUS",
      "catalog_number":"201",
      "title":"The Principles of Entrepreneurship"
    },
    {
      "course_id":"012946",
      "subject":"ARCH",
      "catalog_number":"114",
      "title":"Visual Communication 3"
    },
    {
      "course_id":"013915",
      "subject":"ARCHL",
      "catalog_number":"347W",
      "title":"Archaeology of Syria and Jordan"
    },
    {
      "course_id":"009898",
      "subject":"ARTS",
      "catalog_number":"303",
      "title":"Designing Learning Activities with Interactive Multimedia"
    },
    {
      "course_id":"012452",
      "subject":"ARTS",
      "catalog_number":"304",
      "title":"Designing Computer Simulations and Games for Learning"
    },
    {
      "course_id":"003665",
      "subject":"BIOL",
      "catalog_number":"139",
      "title":"Genetics"
    },
    {
      "course_id":"011618",
      "subject":"BIOL",
      "catalog_number":"140",
      "title":"Fundamentals of Microbiology"
    },
    {
      "course_id":"011568",
      "subject":"BIOL",
      "catalog_number":"140L",
      "title":"Microbiology Laboratory"
    },
    {
      "course_id":"012245",
      "subject":"BIOL",
      "catalog_number":"208",
      "title":"Analytical Methods in Molecular Biology"
    },
    {
      "course_id":"003668",
      "subject":"BIOL",
      "catalog_number":"250",
      "title":"Organismal and Evolutionary Ecology"
    },
    {
      "course_id":"009491",
      "subject":"BIOL",
      "catalog_number":"265",
      "title":"Diversity of Life"
    },
    {
      "course_id":"013953",
      "subject":"BIOL",
      "catalog_number":"358",
      "title":"Quantitative Ecology"
    },
    {
      "course_id":"003698",
      "subject":"BIOL",
      "catalog_number":"374L",
      "title":"Techniques in Animal Physiology"
    },
    {
      "course_id":"003766",
      "subject":"BIOL",
      "catalog_number":"491B",
      "title":"Field Course in Terrestrial and Aquatic Biology"
    },
    {
      "course_id":"004077",
      "subject":"CHEM",
      "catalog_number":"305",
      "title":"Atmospheric Chemistry and Physics"
    },
    {
      "course_id":"010355",
      "subject":"CHEM",
      "catalog_number":"305L",
      "title":"Atmospheric Modelling Laboratory"
    },
    {
      "course_id":"012563",
      "subject":"CHEM",
      "catalog_number":"340L",
      "title":"Introductory Computational Chemistry Laboratory"
    },
    {
      "course_id":"004120",
      "subject":"CHEM",
      "catalog_number":"406",
      "title":"Environmental Organic Chemistry"
    },
    {
      "course_id":"011363",
      "subject":"CM",
      "catalog_number":"271",
      "title":"Introduction to Computational Mathematics"
    },
    {
      "course_id":"004392",
      "subject":"CM",
      "catalog_number":"339",
      "title":"Algorithms"
    },
    {
      "course_id":"003895",
      "subject":"CM",
      "catalog_number":"340",
      "title":"Introduction to Optimization"
    },
    {
      "course_id":"011451",
      "subject":"CM",
      "catalog_number":"352",
      "title":"Computational Methods for Differential Equations"
    },
    {
      "course_id":"011910",
      "subject":"CM",
      "catalog_number":"353",
      "title":"Computational Modeling of Cellular Systems"
    },
    {
      "course_id":"010136",
      "subject":"CM",
      "catalog_number":"432",
      "title":"Applied Cryptography"
    },
    {
      "course_id":"004436",
      "subject":"CM",
      "catalog_number":"433",
      "title":"Introduction to Symbolic Computation"
    },
    {
      "course_id":"012236",
      "subject":"CM",
      "catalog_number":"434",
      "title":"Techniques in Computational Number Theory"
    },
    {
      "course_id":"011442",
      "subject":"CM",
      "catalog_number":"441",
      "title":"Computational Discrete Optimization"
    },
    {
      "course_id":"003898",
      "subject":"CM",
      "catalog_number":"442",
      "title":"Nonlinear Optimization"
    },
    {
      "course_id":"003899",
      "subject":"CM",
      "catalog_number":"443",
      "title":"Deterministic OR Models"
    },
    {
      "course_id":"011448",
      "subject":"CM",
      "catalog_number":"452",
      "title":"Computational Methods for Partial Differential Equations"
    },
    {
      "course_id":"011443",
      "subject":"CM",
      "catalog_number":"454",
      "title":"Applications of Computational Differential Equations"
    },
    {
      "course_id":"008883",
      "subject":"CM",
      "catalog_number":"461",
      "title":"Computational Inference"
    },
    {
      "course_id":"011434",
      "subject":"CM",
      "catalog_number":"462",
      "title":"Data Visualization"
    },
    {
      "course_id":"008884",
      "subject":"CM",
      "catalog_number":"463",
      "title":"Statistical Learning - Classification"
    },
    {
      "course_id":"011436",
      "subject":"CM",
      "catalog_number":"464",
      "title":"Statistical Learning - Function Estimation"
    },
    {
      "course_id":"011446",
      "subject":"CM",
      "catalog_number":"473",
      "title":"Medical Image Processing"
    },
    {
      "course_id":"003352",
      "subject":"CM",
      "catalog_number":"476",
      "title":"Numeric Computation for Financial Modeling"
    },
    {
      "course_id":"012761",
      "subject":"CM",
      "catalog_number":"498",
      "title":"Advanced Topics in Computational Mathematics"
    },
    {
      "course_id":"011440",
      "subject":"CO",
      "catalog_number":"352",
      "title":"Computational Optimization"
    },
    {
      "course_id":"003897",
      "subject":"CO",
      "catalog_number":"355",
      "title":"Mathematical Optimization"
    },
    {
      "course_id":"009898",
      "subject":"DAC",
      "catalog_number":"303",
      "title":"Designing Learning Activities with Interactive Multimedia"
    },
    {
      "course_id":"012452",
      "subject":"DAC",
      "catalog_number":"304",
      "title":"Designing Computer Simulations and Games for Learning"
    },
    {
      "course_id":"011683",
      "subject":"DAC",
      "catalog_number":"400",
      "title":"Digital Design Research Project"
    },
    {
      "course_id":"011596",
      "subject":"DRAMA",
      "catalog_number":"250",
      "title":"Performance German I"
    },
    {
      "course_id":"010188",
      "subject":"DRAMA",
      "catalog_number":"312",
      "title":"Survey of Dramatic Literature and Theory 3"
    },
    {
      "course_id":"004683",
      "subject":"DRAMA",
      "catalog_number":"313",
      "title":"Survey of Dramatic Literature and Theory 4"
    },
    {
      "course_id":"014889",
      "subject":"DRAMA",
      "catalog_number":"317",
      "title":"Production Participation 6"
    },
    {
      "course_id":"010189",
      "subject":"DRAMA",
      "catalog_number":"319A",
      "title":"William Shakespeare in Performance"
    },
    {
      "course_id":"010191",
      "subject":"DRAMA",
      "catalog_number":"319C",
      "title":"Anton Chekhov in Performance"
    },
    {
      "course_id":"010732",
      "subject":"DRAMA",
      "catalog_number":"319D",
      "title":"Stephen Sondheim in Performance"
    },
    {
      "course_id":"004695",
      "subject":"DRAMA",
      "catalog_number":"332",
      "title":"Design for the Theatre 2"
    },
    {
      "course_id":"010104",
      "subject":"DRAMA",
      "catalog_number":"334",
      "title":"Scenic Painting"
    },
    {
      "course_id":"004700",
      "subject":"DRAMA",
      "catalog_number":"348",
      "title":"Cultural Management 1"
    },
    {
      "course_id":"004701",
      "subject":"DRAMA",
      "catalog_number":"349",
      "title":"Cultural Management 2"
    },
    {
      "course_id":"004702",
      "subject":"DRAMA",
      "catalog_number":"350",
      "title":"Cultural Management 3"
    },
    {
      "course_id":"005510",
      "subject":"DRAMA",
      "catalog_number":"352",
      "title":"The Cinema of Science Fiction"
    },
    {
      "course_id":"005511",
      "subject":"DRAMA",
      "catalog_number":"353",
      "title":"Contemporary Italian Film"
    },
    {
      "course_id":"012326",
      "subject":"DRAMA",
      "catalog_number":"354",
      "title":"New Cinemas of East Asia (from 1985)"
    },
    {
      "course_id":"010011",
      "subject":"DRAMA",
      "catalog_number":"355",
      "title":"History of Animated Film"
    },
    {
      "course_id":"005466",
      "subject":"DRAMA",
      "catalog_number":"356",
      "title":"History of Film 1 (1895-1940)"
    },
    {
      "course_id":"005467",
      "subject":"DRAMA",
      "catalog_number":"357",
      "title":"History of Film 2 (after 1941)"
    },
    {
      "course_id":"005508",
      "subject":"DRAMA",
      "catalog_number":"358",
      "title":"French Film After 1945"
    },
    {
      "course_id":"004714",
      "subject":"DRAMA",
      "catalog_number":"390",
      "title":"Theatre for Young Audiences"
    },
    {
      "course_id":"011180",
      "subject":"DRAMA",
      "catalog_number":"391",
      "title":"Women in the Theatre"
    },
    {
      "course_id":"011712",
      "subject":"DRAMA",
      "catalog_number":"393",
      "title":"Plays on Film"
    },
    {
      "course_id":"011714",
      "subject":"DRAMA",
      "catalog_number":"395",
      "title":"Modern British Film"
    },
    {
      "course_id":"012365",
      "subject":"EARTH",
      "catalog_number":"205",
      "title":"Introduction to Atmospheric Science"
    },
    {
      "course_id":"004077",
      "subject":"EARTH",
      "catalog_number":"305",
      "title":"Atmospheric Chemistry and Physics"
    },
    {
      "course_id":"010355",
      "subject":"EARTH",
      "catalog_number":"305L",
      "title":"Atmospheric Modelling Laboratory"
    },
    {
      "course_id":"012418",
      "subject":"EARTH",
      "catalog_number":"361",
      "title":"Atmospheric Motions and Physics"
    },
    {
      "course_id":"009235",
      "subject":"ECE",
      "catalog_number":"202",
      "title":"Class Professor Seminar"
    },
    {
      "course_id":"004752",
      "subject":"ECE",
      "catalog_number":"204",
      "title":"Numerical Methods"
    },
    {
      "course_id":"004758",
      "subject":"ECE",
      "catalog_number":"241",
      "title":"Circuit Analysis and Design"
    },
    {
      "course_id":"004760",
      "subject":"ECE",
      "catalog_number":"251",
      "title":"Programming Languages and Translators"
    },
    {
      "course_id":"004763",
      "subject":"ECE",
      "catalog_number":"261",
      "title":"Energy Systems"
    },
    {
      "course_id":"009236",
      "subject":"ECE",
      "catalog_number":"301",
      "title":"Class Professor Seminar"
    },
    {
      "course_id":"009237",
      "subject":"ECE",
      "catalog_number":"302",
      "title":"Class Professor Seminar"
    },
    {
      "course_id":"004770",
      "subject":"ECE",
      "catalog_number":"324",
      "title":"Microprocessor Systems and Interfacing"
    },
    {
      "course_id":"004771",
      "subject":"ECE",
      "catalog_number":"332",
      "title":"Electronic Circuits"
    },
    {
      "course_id":"004773",
      "subject":"ECE",
      "catalog_number":"342",
      "title":"Signals and Systems"
    },
    {
      "course_id":"004775",
      "subject":"ECE",
      "catalog_number":"355",
      "title":"Software Engineering"
    },
    {
      "course_id":"004777",
      "subject":"ECE",
      "catalog_number":"370",
      "title":"Electromagnetic Fields"
    },
    {
      "course_id":"004780",
      "subject":"ECE",
      "catalog_number":"391",
      "title":"Engineering Design Concepts"
    },
    {
      "course_id":"009238",
      "subject":"ECE",
      "catalog_number":"401",
      "title":"Class Professor Seminar"
    },
    {
      "course_id":"009239",
      "subject":"ECE",
      "catalog_number":"402",
      "title":"Class Professor Seminar"
    },
    {
      "course_id":"004783",
      "subject":"ECE",
      "catalog_number":"412",
      "title":"Coded Digital Communications"
    },
    {
      "course_id":"004787",
      "subject":"ECE",
      "catalog_number":"428",
      "title":"Computer Networks and Security"
    },
    {
      "course_id":"010385",
      "subject":"ECE",
      "catalog_number":"431",
      "title":"Radio Frequency Microelectronics"
    },
    {
      "course_id":"004789",
      "subject":"ECE",
      "catalog_number":"434",
      "title":"Microsystems Technology"
    },
    {
      "course_id":"004792",
      "subject":"ECE",
      "catalog_number":"437",
      "title":"Integrated VLSI Systems"
    },
    {
      "course_id":"004793",
      "subject":"ECE",
      "catalog_number":"438",
      "title":"Digital Integrated Circuits"
    },
    {
      "course_id":"004794",
      "subject":"ECE",
      "catalog_number":"439",
      "title":"Analog Integrated Circuits"
    },
    {
      "course_id":"004795",
      "subject":"ECE",
      "catalog_number":"443",
      "title":"Circuit Analysis and Filter Design"
    },
    {
      "course_id":"004797",
      "subject":"ECE",
      "catalog_number":"450",
      "title":"Software Systems"
    },
    {
      "course_id":"004804",
      "subject":"ECE",
      "catalog_number":"457",
      "title":"Applied Artificial Intelligence"
    },
    {
      "course_id":"004809",
      "subject":"ECE",
      "catalog_number":"471",
      "title":"Electromagnetic Waves"
    },
    {
      "course_id":"010386",
      "subject":"ECE",
      "catalog_number":"476",
      "title":"Antennas and Wireless Systems"
    },
    {
      "course_id":"010039",
      "subject":"ECE",
      "catalog_number":"492B",
      "title":"Engineering Design Symposium"
    },
    {
      "course_id":"004907",
      "subject":"ECON",
      "catalog_number":"265",
      "title":"Economic Development of Early Modern Europe, 1492-1780"
    },
    {
      "course_id":"004920",
      "subject":"ECON",
      "catalog_number":"310",
      "title":"History of Canadian Economic Development"
    },
    {
      "course_id":"004928",
      "subject":"ECON",
      "catalog_number":"333",
      "title":"Urban and Regional Economics"
    },
    {
      "course_id":"004929",
      "subject":"ECON",
      "catalog_number":"334",
      "title":"Institutions of International Trade and Finance"
    },
    {
      "course_id":"004930",
      "subject":"ECON",
      "catalog_number":"335",
      "title":"Economic Development"
    },
    {
      "course_id":"009939",
      "subject":"ECON",
      "catalog_number":"384",
      "title":"Special Topics"
    },
    {
      "course_id":"009940",
      "subject":"ECON",
      "catalog_number":"385",
      "title":"Special Topics"
    },
    {
      "course_id":"009941",
      "subject":"ECON",
      "catalog_number":"386",
      "title":"Special Topics"
    },
    {
      "course_id":"009942",
      "subject":"ECON",
      "catalog_number":"387",
      "title":"Special Topics"
    },
    {
      "course_id":"009943",
      "subject":"ECON",
      "catalog_number":"388",
      "title":"Special Topics"
    },
    {
      "course_id":"009944",
      "subject":"ECON",
      "catalog_number":"389",
      "title":"Special Topics"
    },
    {
      "course_id":"004965",
      "subject":"ECON",
      "catalog_number":"461",
      "title":"Comparative Economic Systems"
    },
    {
      "course_id":"004973",
      "subject":"ECON",
      "catalog_number":"485",
      "title":"Special Studies"
    },
    {
      "course_id":"009952",
      "subject":"ECON",
      "catalog_number":"486",
      "title":"Special Studies"
    },
    {
      "course_id":"005038",
      "subject":"ENGL",
      "catalog_number":"102A",
      "title":"The Major Forms of Literature: Short Stories and Drama"
    },
    {
      "course_id":"005039",
      "subject":"ENGL",
      "catalog_number":"102B",
      "title":"The Major Forms of Literature: Novels and Poetry"
    },
    {
      "course_id":"005041",
      "subject":"ENGL",
      "catalog_number":"103A",
      "title":"The Nature and Structure of the English Language"
    },
    {
      "course_id":"005044",
      "subject":"ENGL",
      "catalog_number":"105A",
      "title":"Literature in English, 1900 -1960"
    },
    {
      "course_id":"005045",
      "subject":"ENGL",
      "catalog_number":"105B",
      "title":"Literature in English, 1960 to the present"
    },
    {
      "course_id":"005047",
      "subject":"ENGL",
      "catalog_number":"107",
      "title":"Issues in Canadian Literature"
    },
    {
      "course_id":"015063",
      "subject":"ENGL",
      "catalog_number":"209",
      "title":"Advanced Academic Writing"
    },
    {
      "course_id":"005107",
      "subject":"ENGL",
      "catalog_number":"219",
      "title":"Contemporary Usage"
    },
    {
      "course_id":"010188",
      "subject":"ENGL",
      "catalog_number":"233A",
      "title":"Survey of Dramatic Literature and Theory 3"
    },
    {
      "course_id":"004683",
      "subject":"ENGL",
      "catalog_number":"233B",
      "title":"Survey of Dramatic Literature and Theory 4"
    },
    {
      "course_id":"004686",
      "subject":"ENGL",
      "catalog_number":"235",
      "title":"Survey of Dramatic Literature and Theory 8"
    },
    {
      "course_id":"009922",
      "subject":"ENGL",
      "catalog_number":"240R",
      "title":"Form and Function 1"
    },
    {
      "course_id":"009923",
      "subject":"ENGL",
      "catalog_number":"241R",
      "title":"Form and Function 2"
    },
    {
      "course_id":"005130",
      "subject":"ENGL",
      "catalog_number":"306E",
      "title":"Linguistics and Literature"
    },
    {
      "course_id":"009985",
      "subject":"ENGL",
      "catalog_number":"490",
      "title":"Topics in North American Literature"
    },
    {
      "course_id":"011140",
      "subject":"ERS",
      "catalog_number":"203",
      "title":"Environment and Development in a Global Perspective"
    },
    {
      "course_id":"005325",
      "subject":"ERS",
      "catalog_number":"280",
      "title":"Applied Field Studies"
    },
    {
      "course_id":"005405",
      "subject":"ERS",
      "catalog_number":"413A",
      "title":"Environmental Research Project II"
    },
    {
      "course_id":"005406",
      "subject":"ERS",
      "catalog_number":"413B",
      "title":"Environmental Research Project III"
    },
    {
      "course_id":"012635",
      "subject":"ERS",
      "catalog_number":"489",
      "title":"Global Food Systems"
    },
    {
      "course_id":"013004",
      "subject":"ESL",
      "catalog_number":"100R",
      "title":"English Language in Canadian Contexts"
    },
    {
      "course_id":"005420",
      "subject":"FINE",
      "catalog_number":"110",
      "title":"Introduction to Art History"
    },
    {
      "course_id":"005423",
      "subject":"FINE",
      "catalog_number":"120",
      "title":"Fundamentals of Visual Art 1"
    },
    {
      "course_id":"005424",
      "subject":"FINE",
      "catalog_number":"121",
      "title":"Fundamentals of Visual Art 2"
    },
    {
      "course_id":"011369",
      "subject":"FINE",
      "catalog_number":"200",
      "title":"Appreciation and Expression"
    },
    {
      "course_id":"005446",
      "subject":"FINE",
      "catalog_number":"226B",
      "title":"Intermediate Printmaking B"
    },
    {
      "course_id":"010009",
      "subject":"FINE",
      "catalog_number":"226D",
      "title":"Special Topics in Printmaking"
    },
    {
      "course_id":"005453",
      "subject":"FINE",
      "catalog_number":"228E",
      "title":"Photography for Artists"
    },
    {
      "course_id":"005462",
      "subject":"FINE",
      "catalog_number":"248A",
      "title":"Art in Context"
    },
    {
      "course_id":"005463",
      "subject":"FINE",
      "catalog_number":"248B",
      "title":"Art in Context"
    },
    {
      "course_id":"005464",
      "subject":"FINE",
      "catalog_number":"249A",
      "title":"Art in Context"
    },
    {
      "course_id":"005465",
      "subject":"FINE",
      "catalog_number":"249B",
      "title":"Art in Context"
    },
    {
      "course_id":"005466",
      "subject":"FINE",
      "catalog_number":"250",
      "title":"History of Film 1 (1895-1940)"
    },
    {
      "course_id":"005467",
      "subject":"FINE",
      "catalog_number":"251",
      "title":"History of Film 2 (after 1941)"
    },
    {
      "course_id":"011783",
      "subject":"FINE",
      "catalog_number":"290",
      "title":"Selected Subjects in Fine Arts"
    },
    {
      "course_id":"005482",
      "subject":"FINE",
      "catalog_number":"313",
      "title":"Special Topics in 18th- and 19th-Century Art"
    },
    {
      "course_id":"005483",
      "subject":"FINE",
      "catalog_number":"316",
      "title":"First Nations' Art in Canada"
    },
    {
      "course_id":"005486",
      "subject":"FINE",
      "catalog_number":"319A",
      "title":"Special Topics in 20th-Century Art"
    },
    {
      "course_id":"005488",
      "subject":"FINE",
      "catalog_number":"320",
      "title":"Advanced Painting"
    },
    {
      "course_id":"005489",
      "subject":"FINE",
      "catalog_number":"321",
      "title":"Advanced Painting Studio"
    },
    {
      "course_id":"005490",
      "subject":"FINE",
      "catalog_number":"322",
      "title":"Advanced Sculpture"
    },
    {
      "course_id":"005491",
      "subject":"FINE",
      "catalog_number":"323",
      "title":"Advanced Sculpture Studio"
    },
    {
      "course_id":"005493",
      "subject":"FINE",
      "catalog_number":"324",
      "title":"Advanced Drawing"
    },
    {
      "course_id":"005494",
      "subject":"FINE",
      "catalog_number":"325",
      "title":"Advanced Drawing Studio"
    },
    {
      "course_id":"005495",
      "subject":"FINE",
      "catalog_number":"326A",
      "title":"Advanced Image-Making Through Printmaking Processes"
    },
    {
      "course_id":"010004",
      "subject":"FINE",
      "catalog_number":"326B",
      "title":"Advanced Printmaking Studio"
    },
    {
      "course_id":"005496",
      "subject":"FINE",
      "catalog_number":"328",
      "title":"Advanced Electronic Imaging"
    },
    {
      "course_id":"005497",
      "subject":"FINE",
      "catalog_number":"329",
      "title":"Electronic Imaging Studio"
    },
    {
      "course_id":"010104",
      "subject":"FINE",
      "catalog_number":"334",
      "title":"Scenic Painting"
    },
    {
      "course_id":"004695",
      "subject":"FINE",
      "catalog_number":"336",
      "title":"Design for the Theatre 2"
    },
    {
      "course_id":"005504",
      "subject":"FINE",
      "catalog_number":"348A",
      "title":"Art in Context"
    },
    {
      "course_id":"005505",
      "subject":"FINE",
      "catalog_number":"348B",
      "title":"Art in Context"
    },
    {
      "course_id":"005506",
      "subject":"FINE",
      "catalog_number":"349A",
      "title":"Art in Context"
    },
    {
      "course_id":"005507",
      "subject":"FINE",
      "catalog_number":"349B",
      "title":"Art in Context"
    },
    {
      "course_id":"005508",
      "subject":"FINE",
      "catalog_number":"350",
      "title":"French Film After 1945"
    },
    {
      "course_id":"005510",
      "subject":"FINE",
      "catalog_number":"352",
      "title":"The Cinema of Science Fiction"
    },
    {
      "course_id":"005511",
      "subject":"FINE",
      "catalog_number":"353",
      "title":"Contemporary Italian Film"
    },
    {
      "course_id":"012326",
      "subject":"FINE",
      "catalog_number":"354",
      "title":"New Cinemas of East Asia (from 1985)"
    },
    {
      "course_id":"010011",
      "subject":"FINE",
      "catalog_number":"355",
      "title":"History of Animated Film"
    },
    {
      "course_id":"010199",
      "subject":"FINE",
      "catalog_number":"356R",
      "title":"Special Topics in Film"
    },
    {
      "course_id":"010200",
      "subject":"FINE",
      "catalog_number":"357R",
      "title":"Special Topics in Film"
    },
    {
      "course_id":"011712",
      "subject":"FINE",
      "catalog_number":"367",
      "title":"Plays on Film"
    },
    {
      "course_id":"012169",
      "subject":"FINE",
      "catalog_number":"371",
      "title":"Advanced Ceramic Studio"
    },
    {
      "course_id":"011714",
      "subject":"FINE",
      "catalog_number":"375",
      "title":"Modern British Film"
    },
    {
      "course_id":"005518",
      "subject":"FINE",
      "catalog_number":"380",
      "title":"Film Studies Seminar"
    },
    {
      "course_id":"005519",
      "subject":"FINE",
      "catalog_number":"381",
      "title":"Film Studies Seminar"
    },
    {
      "course_id":"005520",
      "subject":"FINE",
      "catalog_number":"390",
      "title":"Selected Subjects in Fine Arts"
    },
    {
      "course_id":"005522",
      "subject":"FINE",
      "catalog_number":"391",
      "title":"Selected Subjects in Fine Arts"
    },
    {
      "course_id":"005523",
      "subject":"FINE",
      "catalog_number":"392",
      "title":"Selected Subjects in Fine Arts"
    },
    {
      "course_id":"010005",
      "subject":"FINE",
      "catalog_number":"394",
      "title":"Fine Arts Abroad"
    },
    {
      "course_id":"010006",
      "subject":"FINE",
      "catalog_number":"460A",
      "title":"Senior Honours Seminar"
    },
    {
      "course_id":"010007",
      "subject":"FINE",
      "catalog_number":"460B",
      "title":"Senior Honours Seminar"
    },
    {
      "course_id":"010008",
      "subject":"FINE",
      "catalog_number":"461",
      "title":"Senior Honours Seminar - Joint Honours and Arts and Business"
    },
    {
      "course_id":"012615",
      "subject":"FINE",
      "catalog_number":"499",
      "title":"Senior Studies in Art History"
    },
    {
      "course_id":"005615",
      "subject":"FR",
      "catalog_number":"352",
      "title":"French Language 3: Module 2"
    },
    {
      "course_id":"005643",
      "subject":"FR",
      "catalog_number":"410A",
      "title":"Medieval French Literature"
    },
    {
      "course_id":"005644",
      "subject":"FR",
      "catalog_number":"410B",
      "title":"Medieval French Literature"
    },
    {
      "course_id":"010204",
      "subject":"FR",
      "catalog_number":"471A",
      "title":"French-Canadian Literature"
    },
    {
      "course_id":"010207",
      "subject":"FR",
      "catalog_number":"471B",
      "title":"French-Canadian Literature"
    },
    {
      "course_id":"005666",
      "subject":"FR",
      "catalog_number":"495",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005667",
      "subject":"FR",
      "catalog_number":"496",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005668",
      "subject":"FR",
      "catalog_number":"497",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"005669",
      "subject":"FR",
      "catalog_number":"498",
      "title":"Senior Tutorials"
    },
    {
      "course_id":"012402",
      "subject":"GEOG",
      "catalog_number":"206",
      "title":"Human Dimensions of Natural Hazards"
    },
    {
      "course_id":"005846",
      "subject":"GEOG",
      "catalog_number":"208",
      "title":"Human Dimensions of Global Climate Change"
    },
    {
      "course_id":"010133",
      "subject":"GEOG",
      "catalog_number":"210",
      "title":"Image Interpretation and Photogrammetry"
    },
    {
      "course_id":"005853",
      "subject":"GEOG",
      "catalog_number":"221",
      "title":"The United States"
    },
    {
      "course_id":"005939",
      "subject":"GEOG",
      "catalog_number":"353",
      "title":"Retail Location"
    },
    {
      "course_id":"013046",
      "subject":"GEOG",
      "catalog_number":"360",
      "title":"Environment and Behaviour"
    },
    {
      "course_id":"005275",
      "subject":"GEOG",
      "catalog_number":"365",
      "title":"Study Abroad"
    },
    {
      "course_id":"005277",
      "subject":"GEOG",
      "catalog_number":"366",
      "title":"Study Abroad"
    },
    {
      "course_id":"005963",
      "subject":"GEOG",
      "catalog_number":"372",
      "title":"Waterloo in Switzerland -- Lausanne"
    },
    {
      "course_id":"005964",
      "subject":"GEOG",
      "catalog_number":"373",
      "title":"Waterloo in Switzerland -- Lausanne"
    },
    {
      "course_id":"005982",
      "subject":"GEOG",
      "catalog_number":"393",
      "title":"Approaches to Research in Human Geography"
    },
    {
      "course_id":"012888",
      "subject":"GEOG",
      "catalog_number":"394",
      "title":"Approaches to Research in Physical Geography"
    },
    {
      "course_id":"012635",
      "subject":"GEOG",
      "catalog_number":"429",
      "title":"Global Food Systems"
    },
    {
      "course_id":"011594",
      "subject":"GER",
      "catalog_number":"203",
      "title":"Written Communication"
    },
    {
      "course_id":"011595",
      "subject":"GER",
      "catalog_number":"204",
      "title":"Integrative Language Seminar"
    },
    {
      "course_id":"006089",
      "subject":"GER",
      "catalog_number":"291",
      "title":"Survey of German Literature and Culture"
    },
    {
      "course_id":"006090",
      "subject":"GER",
      "catalog_number":"292",
      "title":"Survey of German Literature and Culture"
    },
    {
      "course_id":"006099",
      "subject":"GER",
      "catalog_number":"305",
      "title":"German for Professional Purposes I"
    },
    {
      "course_id":"006100",
      "subject":"GER",
      "catalog_number":"306",
      "title":"German for Professional Purposes II"
    },
    {
      "course_id":"011600",
      "subject":"GER",
      "catalog_number":"332",
      "title":"Studies in Genre (Prose and Poetry)"
    },
    {
      "course_id":"011601",
      "subject":"GER",
      "catalog_number":"333",
      "title":"Studies in Genre (Theatre and Film)"
    },
    {
      "course_id":"006214",
      "subject":"HIST",
      "catalog_number":"108",
      "title":"Family Ties in History"
    },
    {
      "course_id":"012597",
      "subject":"HIST",
      "catalog_number":"114",
      "title":"A Comparative History of Empires"
    },
    {
      "course_id":"006219",
      "subject":"HIST",
      "catalog_number":"130",
      "title":"The Modern World in Historical Perspective"
    },
    {
      "course_id":"006235",
      "subject":"HIST",
      "catalog_number":"207",
      "title":"Canadian Labour History"
    },
    {
      "course_id":"012714",
      "subject":"HIST",
      "catalog_number":"208",
      "title":"Foreign Relations of the United States since 1900"
    },
    {
      "course_id":"006287",
      "subject":"HIST",
      "catalog_number":"244",
      "title":"The Medium and the Message: Canadian Media, a History"
    },
    {
      "course_id":"006288",
      "subject":"HIST",
      "catalog_number":"245",
      "title":"War, Ethnicity and Religion in East Central Europe, 1453-1739"
    },
    {
      "course_id":"006296",
      "subject":"HIST",
      "catalog_number":"249",
      "title":"The American Impact on Canada"
    },
    {
      "course_id":"015064",
      "subject":"HIST",
      "catalog_number":"312",
      "title":"The First World War"
    },
    {
      "course_id":"006356",
      "subject":"HIST",
      "catalog_number":"339",
      "title":"The History of France in the 19th Century"
    },
    {
      "course_id":"013901",
      "subject":"HIST",
      "catalog_number":"363W",
      "title":"Jews in Modern Europe 1750-1938 (WLU)"
    },
    {
      "course_id":"006383",
      "subject":"HIST",
      "catalog_number":"387",
      "title":"Ontario History since Confederation"
    },
    {
      "course_id":"006386",
      "subject":"HIST",
      "catalog_number":"390",
      "title":"The Canadian City Since 1880"
    },
    {
      "course_id":"006436",
      "subject":"HLTH",
      "catalog_number":"349",
      "title":"Health Behaviour Change"
    },
    {
      "course_id":"013734",
      "subject":"ISS",
      "catalog_number":"205R",
      "title":"History of Education in Canada"
    },
    {
      "course_id":"006501",
      "subject":"ISS",
      "catalog_number":"131R",
      "title":"Social Ideas, Social Policy and Political Practice"
    },
    {
      "course_id":"006502",
      "subject":"ISS",
      "catalog_number":"150R",
      "title":"Lifespan Processes: The Normal Events"
    },
    {
      "course_id":"006503",
      "subject":"ISS",
      "catalog_number":"220R",
      "title":"Changing Concepts of Childhood"
    },
    {
      "course_id":"006504",
      "subject":"ISS",
      "catalog_number":"240R",
      "title":"Art and Society"
    },
    {
      "course_id":"006505",
      "subject":"ISS",
      "catalog_number":"250A",
      "title":"Social Statistics"
    },
    {
      "course_id":"006506",
      "subject":"ISS",
      "catalog_number":"250B",
      "title":"Social Statistics"
    },
    {
      "course_id":"006507",
      "subject":"ISS",
      "catalog_number":"250R",
      "title":"Social Statistics"
    },
    {
      "course_id":"006508",
      "subject":"ISS",
      "catalog_number":"251R",
      "title":"Social Research"
    },
    {
      "course_id":"011378",
      "subject":"ISS",
      "catalog_number":"311R",
      "title":"Public Policy and Native Peoples in Canada"
    },
    {
      "course_id":"011979",
      "subject":"ISS",
      "catalog_number":"312R",
      "title":"Homelessness & Public Policy"
    },
    {
      "course_id":"006510",
      "subject":"ISS",
      "catalog_number":"350D",
      "title":"Adult Life Crises and Events"
    },
    {
      "course_id":"006511",
      "subject":"ISS",
      "catalog_number":"350E",
      "title":"Family Law and Public Policy"
    },
    {
      "course_id":"011390",
      "subject":"ISS",
      "catalog_number":"350G",
      "title":"The Evolution of Family Law in Canadian Society"
    },
    {
      "course_id":"006513",
      "subject":"ISS",
      "catalog_number":"350H",
      "title":"Values and the Contemporary Family"
    },
    {
      "course_id":"012746",
      "subject":"ISS",
      "catalog_number":"370R",
      "title":"International Learning Experience"
    },
    {
      "course_id":"012191",
      "subject":"ISS",
      "catalog_number":"375R",
      "title":"Studies in Interdisciplinary Social Science"
    },
    {
      "course_id":"006514",
      "subject":"ISS",
      "catalog_number":"398R",
      "title":"Independent Study"
    },
    {
      "course_id":"006515",
      "subject":"ISS",
      "catalog_number":"399R",
      "title":"Independent Study"
    },
    {
      "course_id":"013331",
      "subject":"ISS",
      "catalog_number":"400R",
      "title":"Comparative Social Policy"
    },
    {
      "course_id":"006509",
      "subject":"ISS",
      "catalog_number":"420R",
      "title":"Critical Encounter with Human Nature"
    },
    {
      "course_id":"013099",
      "subject":"ISS",
      "catalog_number":"450R",
      "title":"Honours Seminar in Special Topics"
    },
    {
      "course_id":"013103",
      "subject":"ISS",
      "catalog_number":"490R",
      "title":"Special Studies"
    },
    {
      "course_id":"011389",
      "subject":"ISS",
      "catalog_number":"495R",
      "title":"Research Apprenticeship"
    },
    {
      "course_id":"013220",
      "subject":"ISS",
      "catalog_number":"496R",
      "title":"Applied Apprenticeship in Social Development Studies"
    },
    {
      "course_id":"006516",
      "subject":"ISS",
      "catalog_number":"499A",
      "title":"Senior Honours Essay"
    },
    {
      "course_id":"006517",
      "subject":"ISS",
      "catalog_number":"499B",
      "title":"Senior Honours Essay"
    },
    {
      "course_id":"006560",
      "subject":"KIN",
      "catalog_number":"255",
      "title":"Introduction to Psychomotor Behaviour"
    },
    {
      "course_id":"006435",
      "subject":"KIN",
      "catalog_number":"348",
      "title":"Social Psychology of Health Behaviour"
    },
    {
      "course_id":"006436",
      "subject":"KIN",
      "catalog_number":"349",
      "title":"Health Behaviour Change"
    },
    {
      "course_id":"013094",
      "subject":"LS",
      "catalog_number":"250",
      "title":"Introduction to Research Methods"
    },
    {
      "course_id":"013158",
      "subject":"MATH",
      "catalog_number":"211N",
      "title":"Advanced Calculus 1 for Nanotechnology Engineering"
    },
    {
      "course_id":"013160",
      "subject":"MATH",
      "catalog_number":"212N",
      "title":"Advanced Calculus 2 for Nanotechnology Engineering"
    },
    {
      "course_id":"006704",
      "subject":"ME",
      "catalog_number":"123",
      "title":"Electrical Engineering for Mechanical Engineers"
    },
    {
      "course_id":"012406",
      "subject":"ME",
      "catalog_number":"135",
      "title":"Materials Science and Engineering"
    },
    {
      "course_id":"006710",
      "subject":"ME",
      "catalog_number":"215",
      "title":"Structure and Properties of Materials"
    },
    {
      "course_id":"013903",
      "subject":"MI",
      "catalog_number":"202W",
      "title":"Mediterranean Culture and Civilization II (WLU)"
    },
    {
      "course_id":"012386",
      "subject":"MSCI",
      "catalog_number":"424",
      "title":"Organizational Knowledge, Cognition and Communication"
    },
    {
      "course_id":"011500",
      "subject":"MSCI",
      "catalog_number":"443",
      "title":"Telecommunication Management"
    },
    {
      "course_id":"006938",
      "subject":"MTHEL",
      "catalog_number":"100",
      "title":"Commercial and Business Law for Mathematics Students"
    },
    {
      "course_id":"006943",
      "subject":"MTHEL",
      "catalog_number":"400",
      "title":"Entrepreneurship, Technology and the Emerging Information Economy"
    },
    {
      "course_id":"011721",
      "subject":"PACS",
      "catalog_number":"325",
      "title":"Conflict Management for Technical Professions"
    },
    {
      "course_id":"011813",
      "subject":"PDENG",
      "catalog_number":"15",
      "title":"Professional Development - Overview"
    },
    {
      "course_id":"011814",
      "subject":"PDENG",
      "catalog_number":"25",
      "title":"Professional Development - Critical Analysis"
    },
    {
      "course_id":"011815",
      "subject":"PDENG",
      "catalog_number":"35",
      "title":"Professional Development - Responsibility"
    },
    {
      "course_id":"011816",
      "subject":"PDENG",
      "catalog_number":"45",
      "title":"Professional Development - Leadership"
    },
    {
      "course_id":"011817",
      "subject":"PDENG",
      "catalog_number":"55",
      "title":"Professional Development - Integration"
    },
    {
      "course_id":"013005",
      "subject":"PDENG",
      "catalog_number":"57",
      "title":"Integrating Professional Skills for a Global Workplace"
    },
    {
      "course_id":"012466",
      "subject":"PHARM",
      "catalog_number":"140",
      "title":"Computing for Pharmacists - Fundamental Concepts"
    },
    {
      "course_id":"012485",
      "subject":"PHARM",
      "catalog_number":"291",
      "title":"Seminars in Pharmacy 2"
    },
    {
      "course_id":"012502",
      "subject":"PHARM",
      "catalog_number":"390",
      "title":"Seminars in Pharmacy 3"
    },
    {
      "course_id":"012509",
      "subject":"PHARM",
      "catalog_number":"415",
      "title":"Clinical Rotation: Integrated Care"
    },
    {
      "course_id":"007228",
      "subject":"PHIL",
      "catalog_number":"100",
      "title":"Introduction to Philosophy"
    },
    {
      "course_id":"010344",
      "subject":"PHIL",
      "catalog_number":"105",
      "title":"Introduction to Ethics and Values"
    },
    {
      "course_id":"007248",
      "subject":"PHIL",
      "catalog_number":"200A",
      "title":"Great Works of Western Philosophy: Part 1"
    },
    {
      "course_id":"007249",
      "subject":"PHIL",
      "catalog_number":"200B",
      "title":"Great Works of Western Philosophy: Part 2"
    },
    {
      "course_id":"007280",
      "subject":"PHIL",
      "catalog_number":"236",
      "title":"Religious and Paranormal Experience"
    },
    {
      "course_id":"007283",
      "subject":"PHIL",
      "catalog_number":"238",
      "title":"Modern Philosophical Challenges to Religious Belief"
    },
    {
      "course_id":"007288",
      "subject":"PHIL",
      "catalog_number":"243",
      "title":"Creative Thinking, Problem Solving and Decision Making"
    },
    {
      "course_id":"007306",
      "subject":"PHIL",
      "catalog_number":"312",
      "title":"Philosophy of Education 2"
    },
    {
      "course_id":"007310",
      "subject":"PHIL",
      "catalog_number":"322",
      "title":"Contemporary Ethical Theory"
    },
    {
      "course_id":"007331",
      "subject":"PHIL",
      "catalog_number":"387",
      "title":"20th-Century Philosophy"
    },
    {
      "course_id":"011192",
      "subject":"PHIL",
      "catalog_number":"406",
      "title":"Studies in Kant"
    },
    {
      "course_id":"007338",
      "subject":"PHIL",
      "catalog_number":"421",
      "title":"Studies in Ethics"
    },
    {
      "course_id":"007340",
      "subject":"PHIL",
      "catalog_number":"423",
      "title":"Political Philosophy 2"
    },
    {
      "course_id":"007342",
      "subject":"PHIL",
      "catalog_number":"435",
      "title":"Studies in Philosophy of Religion"
    },
    {
      "course_id":"007343",
      "subject":"PHIL",
      "catalog_number":"436",
      "title":"Studies in Philosophy of Religion"
    },
    {
      "course_id":"007344",
      "subject":"PHIL",
      "catalog_number":"440A",
      "title":"Logical Theory"
    },
    {
      "course_id":"009529",
      "subject":"PHIL",
      "catalog_number":"440B",
      "title":"Logical Theory"
    },
    {
      "course_id":"007346",
      "subject":"PHIL",
      "catalog_number":"442",
      "title":"Studies in Logic"
    },
    {
      "course_id":"007351",
      "subject":"PHIL",
      "catalog_number":"456",
      "title":"Problems in Metaphysics"
    },
    {
      "course_id":"007353",
      "subject":"PHIL",
      "catalog_number":"465",
      "title":"Existential Philosophy"
    },
    {
      "course_id":"009531",
      "subject":"PHIL",
      "catalog_number":"470",
      "title":"Phenomenology"
    },
    {
      "course_id":"007357",
      "subject":"PHIL",
      "catalog_number":"473",
      "title":"Special Subjects"
    },
    {
      "course_id":"007358",
      "subject":"PHIL",
      "catalog_number":"474",
      "title":"Special Subjects"
    },
    {
      "course_id":"007359",
      "subject":"PHIL",
      "catalog_number":"475",
      "title":"Special Subjects"
    },
    {
      "course_id":"007360",
      "subject":"PHIL",
      "catalog_number":"476",
      "title":"Special Subjects"
    },
    {
      "course_id":"007361",
      "subject":"PHIL",
      "catalog_number":"477",
      "title":"Special Subjects"
    },
    {
      "course_id":"007362",
      "subject":"PHIL",
      "catalog_number":"478",
      "title":"Special Subjects"
    },
    {
      "course_id":"007363",
      "subject":"PHIL",
      "catalog_number":"479",
      "title":"Special Subjects"
    },
    {
      "course_id":"007364",
      "subject":"PHIL",
      "catalog_number":"480",
      "title":"Special Subjects"
    },
    {
      "course_id":"007367",
      "subject":"PHIL",
      "catalog_number":"483",
      "title":"Special Subjects"
    },
    {
      "course_id":"007368",
      "subject":"PHIL",
      "catalog_number":"484",
      "title":"Special Subjects"
    },
    {
      "course_id":"007444",
      "subject":"PHYS",
      "catalog_number":"258",
      "title":"Thermal Physics"
    },
    {
      "course_id":"007418",
      "subject":"PHYS",
      "catalog_number":"260A",
      "title":"Intermediate Physics Laboratory 1"
    },
    {
      "course_id":"007423",
      "subject":"PHYS",
      "catalog_number":"260B",
      "title":"Intermediate Physics Laboratory 2"
    },
    {
      "course_id":"013118",
      "subject":"PHYS",
      "catalog_number":"260C",
      "title":"Intermediate Physics Laboratory 3"
    },
    {
      "course_id":"013148",
      "subject":"PHYS",
      "catalog_number":"276",
      "title":"Introduction to Gravitational Physics"
    },
    {
      "course_id":"007438",
      "subject":"PHYS",
      "catalog_number":"352",
      "title":"Analogue Electronics"
    },
    {
      "course_id":"007439",
      "subject":"PHYS",
      "catalog_number":"352L",
      "title":"Analogue Electronics Laboratory"
    },
    {
      "course_id":"007440",
      "subject":"PHYS",
      "catalog_number":"353",
      "title":"Digital Electronics"
    },
    {
      "course_id":"007441",
      "subject":"PHYS",
      "catalog_number":"353L",
      "title":"Digital Electronics Laboratory"
    },
    {
      "course_id":"010362",
      "subject":"PHYS",
      "catalog_number":"356",
      "title":"Introduction to Communication and Optical Communication Physics"
    },
    {
      "course_id":"010363",
      "subject":"PHYS",
      "catalog_number":"356L",
      "title":"Introduction to Communication and Optical communication Physics Laboratory"
    },
    {
      "course_id":"007460",
      "subject":"PHYS",
      "catalog_number":"432",
      "title":"Physics of Solid State Devices"
    },
    {
      "course_id":"007468",
      "subject":"PHYS",
      "catalog_number":"441B",
      "title":"Electromagnetic Theory"
    },
    {
      "course_id":"007471",
      "subject":"PHYS",
      "catalog_number":"445",
      "title":"Modern Optics"
    },
    {
      "course_id":"011381",
      "subject":"PHYS",
      "catalog_number":"482",
      "title":"Physics of Medical Imaging"
    },
    {
      "course_id":"007668",
      "subject":"PMATH",
      "catalog_number":"346",
      "title":"Group Theory"
    },
    {
      "course_id":"007674",
      "subject":"PMATH",
      "catalog_number":"354",
      "title":"Measure Theory and Fourier Analysis"
    },
    {
      "course_id":"012236",
      "subject":"PMATH",
      "catalog_number":"434",
      "title":"Techniques in Computational Number Theory"
    },
    {
      "course_id":"007692",
      "subject":"PMATH",
      "catalog_number":"442",
      "title":"Fields and Galois Theory"
    },
    {
      "course_id":"007694",
      "subject":"PMATH",
      "catalog_number":"444",
      "title":"Rings, Modules, and Representations"
    },
    {
      "course_id":"011637",
      "subject":"PSCI",
      "catalog_number":"253",
      "title":"Politics in Russia"
    },
    {
      "course_id":"007760",
      "subject":"PSCI",
      "catalog_number":"292",
      "title":"Issues in Canadian Criminal Law"
    },
    {
      "course_id":"007770",
      "subject":"PSCI",
      "catalog_number":"323",
      "title":"Issues and Concepts in Contemporary Political Philosophy"
    },
    {
      "course_id":"011977",
      "subject":"PSCI",
      "catalog_number":"357",
      "title":"International Organizations"
    },
    {
      "course_id":"010122",
      "subject":"PSCI",
      "catalog_number":"364",
      "title":"The Politics of Ethnicity in Canada"
    },
    {
      "course_id":"007817",
      "subject":"PSCI",
      "catalog_number":"427",
      "title":"Special Topics in Political Philosophy"
    },
    {
      "course_id":"012064",
      "subject":"PSCI",
      "catalog_number":"438",
      "title":"Comparative Public Policy"
    },
    {
      "course_id":"007829",
      "subject":"PSCI",
      "catalog_number":"453",
      "title":"Democracy and Development"
    },
    {
      "course_id":"009535",
      "subject":"PSCI",
      "catalog_number":"457",
      "title":"Ethnic Conflict and Conflict Resolution II"
    },
    {
      "course_id":"012188",
      "subject":"PSCI",
      "catalog_number":"459",
      "title":"Organized Crime and Politics"
    },
    {
      "course_id":"007842",
      "subject":"PSCI",
      "catalog_number":"483",
      "title":"Power Politics and World Order Studies"
    },
    {
      "course_id":"007843",
      "subject":"PSCI",
      "catalog_number":"484",
      "title":"Contemporary Strategies: Theories and Policies"
    },
    {
      "course_id":"012635",
      "subject":"PSCI",
      "catalog_number":"489",
      "title":"Global Food Systems"
    },
    {
      "course_id":"007865",
      "subject":"PSYCH",
      "catalog_number":"121R",
      "title":"Introductory Psychology"
    },
    {
      "course_id":"007904",
      "subject":"PSYCH",
      "catalog_number":"220R",
      "title":"Social Psychology"
    },
    {
      "course_id":"007906",
      "subject":"PSYCH",
      "catalog_number":"221R",
      "title":"Interpersonal Relations"
    },
    {
      "course_id":"011388",
      "subject":"PSYCH",
      "catalog_number":"222R",
      "title":"Cross-Cultural Psychology"
    },
    {
      "course_id":"007928",
      "subject":"PSYCH",
      "catalog_number":"323R",
      "title":"Psychopathology"
    },
    {
      "course_id":"007962",
      "subject":"PSYCH",
      "catalog_number":"334",
      "title":"Theories of Individual Counselling Psychology"
    },
    {
      "course_id":"004700",
      "subject":"REC",
      "catalog_number":"348",
      "title":"Cultural Management 1"
    },
    {
      "course_id":"008167",
      "subject":"REC",
      "catalog_number":"350",
      "title":"Therapeutic Recreation Process and Program Management"
    },
    {
      "course_id":"008216",
      "subject":"REC",
      "catalog_number":"450",
      "title":"Internship for Therapeutic Recreation"
    },
    {
      "course_id":"008284",
      "subject":"RS",
      "catalog_number":"100E",
      "title":"Biblical Studies 1"
    },
    {
      "course_id":"008285",
      "subject":"RS",
      "catalog_number":"100F",
      "title":"Biblical Studies 2"
    },
    {
      "course_id":"010220",
      "subject":"RS",
      "catalog_number":"224",
      "title":"Death and Dying"
    },
    {
      "course_id":"008542",
      "subject":"RS",
      "catalog_number":"263",
      "title":"Psychology of Religion and Spirituality"
    },
    {
      "course_id":"008543",
      "subject":"RS",
      "catalog_number":"264",
      "title":"Personality and Religion"
    },
    {
      "course_id":"010349",
      "subject":"RS",
      "catalog_number":"274",
      "title":"Joan of Arc: Witch, Mystic, Martyr or Saint?"
    },
    {
      "course_id":"008371",
      "subject":"RS",
      "catalog_number":"335",
      "title":"Unity and Diversity in the New Testament"
    },
    {
      "course_id":"008360",
      "subject":"RS",
      "catalog_number":"336",
      "title":"Feminist Approaches to the Bible"
    },
    {
      "course_id":"008392",
      "subject":"RS",
      "catalog_number":"352",
      "title":"Contemporary Mennonite Thought"
    },
    {
      "course_id":"003440",
      "subject":"RS",
      "catalog_number":"361",
      "title":"Anthropology of Religion"
    },
    {
      "course_id":"008547",
      "subject":"RS",
      "catalog_number":"363",
      "title":"Carl Jung's Theory of Religion"
    },
    {
      "course_id":"008405",
      "subject":"RS",
      "catalog_number":"384",
      "title":"Dreams in Religious Experience"
    },
    {
      "course_id":"010102",
      "subject":"RS",
      "catalog_number":"385",
      "title":"Aging as a Spiritual Journey"
    },
    {
      "course_id":"011307",
      "subject":"RS",
      "catalog_number":"386",
      "title":"Spirituality and Psychotherapy"
    },
    {
      "course_id":"010033",
      "subject":"SE",
      "catalog_number":"240",
      "title":"Algorithms and Data Structures"
    },
    {
      "course_id":"013613",
      "subject":"SMF",
      "catalog_number":"311",
      "title":"Communication and Counselling Skills"
    },
    {
      "course_id":"008582",
      "subject":"SOC",
      "catalog_number":"120R",
      "title":"Fundamentals of Sociology"
    },
    {
      "course_id":"008618",
      "subject":"SOC",
      "catalog_number":"235",
      "title":"Individual and Society"
    },
    {
      "course_id":"008629",
      "subject":"SOC",
      "catalog_number":"247",
      "title":"Death and Society"
    },
    {
      "course_id":"008642",
      "subject":"SOC",
      "catalog_number":"265",
      "title":"Political Sociology"
    },
    {
      "course_id":"007322",
      "subject":"SOC",
      "catalog_number":"371",
      "title":"Philosophy of the Social Sciences"
    },
    {
      "course_id":"009877",
      "subject":"SOC",
      "catalog_number":"377",
      "title":"Studies in the Sociology of the Mennonites"
    },
    {
      "course_id":"008709",
      "subject":"SOC",
      "catalog_number":"411",
      "title":"Sociology of the Body"
    },
    {
      "course_id":"010351",
      "subject":"SOC",
      "catalog_number":"412",
      "title":"Social Identities in Canadian Society"
    },
    {
      "course_id":"008815",
      "subject":"SPAN",
      "catalog_number":"261W",
      "title":"Spanish for Communication & Business 1 (WLU)"
    },
    {
      "course_id":"008816",
      "subject":"SPAN",
      "catalog_number":"262W",
      "title":"Spanish for Communication and Business 2 (WLU)"
    },
    {
      "course_id":"008828",
      "subject":"SPAN",
      "catalog_number":"322",
      "title":"The Generation of '98: Fiction"
    },
    {
      "course_id":"008830",
      "subject":"SPAN",
      "catalog_number":"324W",
      "title":"A Journey Through Multicultural Spain (WLU)"
    },
    {
      "course_id":"008832",
      "subject":"SPAN",
      "catalog_number":"325W",
      "title":"Contemporary Spanish Literature and Culture (WLU)"
    },
    {
      "course_id":"011226",
      "subject":"SPAN",
      "catalog_number":"328W",
      "title":"Contemporary Hispanic Theatre (WLU)"
    },
    {
      "course_id":"008837",
      "subject":"SPAN",
      "catalog_number":"333",
      "title":"Modern Latin American Poetry"
    },
    {
      "course_id":"008847",
      "subject":"SPAN",
      "catalog_number":"365W",
      "title":"Spanish Identity Through Literature (WLU)"
    },
    {
      "course_id":"008849",
      "subject":"SPAN",
      "catalog_number":"388",
      "title":"Contemporary Latin American Theatre"
    },
    {
      "course_id":"011386",
      "subject":"SPAN",
      "catalog_number":"438W",
      "title":"Special Topics (WLU)"
    },
    {
      "course_id":"008852",
      "subject":"SPAN",
      "catalog_number":"446W",
      "title":"Love in Medieval Spanish Literature (WLU)"
    },
    {
      "course_id":"008853",
      "subject":"SPAN",
      "catalog_number":"451W",
      "title":"Stylistics and Professional Writing(WLU)"
    },
    {
      "course_id":"013310",
      "subject":"SPAN",
      "catalog_number":"461W",
      "title":"Hispanic Linguistics"
    },
    {
      "course_id":"012362",
      "subject":"SPAN",
      "catalog_number":"465W",
      "title":"Literature and Journalism in the Hispanic World"
    },
    {
      "course_id":"008854",
      "subject":"SPAN",
      "catalog_number":"466W",
      "title":"Subversive Narratives in the Hispanic World (WLU)"
    },
    {
      "course_id":"008855",
      "subject":"SPAN",
      "catalog_number":"467W",
      "title":"Directed Studies (WLU)"
    },
    {
      "course_id":"013311",
      "subject":"SPAN",
      "catalog_number":"498W",
      "title":"Literary Adaptation in Hispanic Cinema"
    },
    {
      "course_id":"011683",
      "subject":"SPCOM",
      "catalog_number":"400",
      "title":"Digital Design Research Project"
    },
    {
      "course_id":"012584",
      "subject":"SPCOM",
      "catalog_number":"403",
      "title":"Special Topics in Speech Communication and Technology"
    },
    {
      "course_id":"012960",
      "subject":"SPCOM",
      "catalog_number":"426",
      "title":"Advanced Voice Technique"
    },
    {
      "course_id":"008542",
      "subject":"SPD",
      "catalog_number":"270",
      "title":"Psychology of Religion and Spirituality"
    },
    {
      "course_id":"008543",
      "subject":"SPD",
      "catalog_number":"271",
      "title":"Personality and Religion"
    },
    {
      "course_id":"008544",
      "subject":"SPD",
      "catalog_number":"302",
      "title":"Selected Topics in Psychology and Religion"
    },
    {
      "course_id":"010102",
      "subject":"SPD",
      "catalog_number":"378",
      "title":"Aging as a Spiritual Journey"
    },
    {
      "course_id":"011307",
      "subject":"SPD",
      "catalog_number":"379",
      "title":"Spirituality and Psychotherapy"
    },
    {
      "course_id":"008547",
      "subject":"SPD",
      "catalog_number":"380",
      "title":"Carl Jung's Theory of Religion"
    },
    {
      "course_id":"013320",
      "subject":"STAT",
      "catalog_number":"232",
      "title":"Introduction to Medical Statistics"
    },
    {
      "course_id":"011388",
      "subject":"SWREN",
      "catalog_number":"223R",
      "title":"Cross-Cultural Psychology"
    },
    {
      "course_id":"006505",
      "subject":"SWREN",
      "catalog_number":"250A",
      "title":"Social Statistics"
    },
    {
      "course_id":"006506",
      "subject":"SWREN",
      "catalog_number":"250B",
      "title":"Social Statistics"
    },
    {
      "course_id":"008949",
      "subject":"SYDE",
      "catalog_number":"282",
      "title":"Fluid Mechanics"
    },
    {
      "course_id":"008936",
      "subject":"SYDE",
      "catalog_number":"284",
      "title":"Materials Chemistry"
    },
    {
      "course_id":"013383",
      "subject":"SYDE",
      "catalog_number":"431",
      "title":"Design Optimization Under Probabilistic Uncertainty"
    },
    {
      "course_id":"009003",
      "subject":"SYDE",
      "catalog_number":"433",
      "title":"Conflict Resolution"
    },
    {
      "course_id":"008988",
      "subject":"SYDE",
      "catalog_number":"444",
      "title":"Biomedical Measurement and Signal Processing"
    },
    {
      "course_id":"009016",
      "subject":"SYDE",
      "catalog_number":"475",
      "title":"Image Processing"
    },
    {
      "course_id":"013385",
      "subject":"SYDE",
      "catalog_number":"482",
      "title":"Dynamic Modelling of Biomechanical Systems"
    },
    {
      "course_id":"009013",
      "subject":"SYDE",
      "catalog_number":"558",
      "title":"Fuzzy Logic and Neural Networks"
    },
    {
      "course_id":"003461",
      "subject":"WS",
      "catalog_number":"350",
      "title":"Culture and Sexuality"
    },
    {
      "course_id":"011676",
      "subject":"ACC",
      "catalog_number":"608",
      "title":"US GAAP"
    },
    {
      "course_id":"011477",
      "subject":"ACC",
      "catalog_number":"620",
      "title":"Enterprise IT Architecture and Configuration Management"
    },
    {
      "course_id":"011480",
      "subject":"ACC",
      "catalog_number":"624",
      "title":"IT Security"
    },
    {
      "course_id":"000011",
      "subject":"ACC",
      "catalog_number":"625",
      "title":"IT Strategic Planning"
    },
    {
      "course_id":"011083",
      "subject":"ACC",
      "catalog_number":"644",
      "title":"E-Business: Enterprise Systems"
    },
    {
      "course_id":"011127",
      "subject":"ACC",
      "catalog_number":"646",
      "title":"E-Business: Introduction  to Electronic Commerce"
    },
    {
      "course_id":"000048",
      "subject":"ACC",
      "catalog_number":"782",
      "title":"Introduction to Research 2"
    },
    {
      "course_id":"013226",
      "subject":"ADMGT",
      "catalog_number":"602",
      "title":"Data Analysis and Management"
    },
    {
      "course_id":"013225",
      "subject":"ADMGT",
      "catalog_number":"603",
      "title":"Operations and Supply Chain Management"
    },
    {
      "course_id":"013224",
      "subject":"ADMGT",
      "catalog_number":"604",
      "title":"Marketing Management"
    },
    {
      "course_id":"013223",
      "subject":"ADMGT",
      "catalog_number":"605",
      "title":"Project Management"
    },
    {
      "course_id":"013222",
      "subject":"ADMGT",
      "catalog_number":"606",
      "title":"Entrepreneurship and Innovation"
    },
    {
      "course_id":"000106",
      "subject":"AMATH",
      "catalog_number":"690",
      "title":"Literature & Research Studies"
    },
    {
      "course_id":"000507",
      "subject":"CIVE",
      "catalog_number":"651",
      "title":"Soil Engineering"
    },
    {
      "course_id":"000508",
      "subject":"CIVE",
      "catalog_number":"652",
      "title":"Experimental Study of Geomaterials"
    },
    {
      "course_id":"000533",
      "subject":"CIVE",
      "catalog_number":"706",
      "title":"Rehabilitation of Structural Concrete"
    },
    {
      "course_id":"000562",
      "subject":"CIVE",
      "catalog_number":"754",
      "title":"Wave Material Interaction and Applications"
    },
    {
      "course_id":"000563",
      "subject":"CIVE",
      "catalog_number":"755",
      "title":"Micromechanics of Soils"
    },
    {
      "course_id":"000571",
      "subject":"CIVE",
      "catalog_number":"773",
      "title":"Microbial Ecology of Aquatic and Engineered Systems"
    },
    {
      "course_id":"000573",
      "subject":"CIVE",
      "catalog_number":"775",
      "title":"Principles of Ecological Engineering"
    },
    {
      "course_id":"000576",
      "subject":"CIVE",
      "catalog_number":"778",
      "title":"Physical Hydrology"
    },
    {
      "course_id":"013034",
      "subject":"CLAS",
      "catalog_number":"635",
      "title":"Dining in the Greek and Roman World"
    },
    {
      "course_id":"013759",
      "subject":"CLAS",
      "catalog_number":"636",
      "title":"Judaeo-Christian Literature and the Classical Past"
    },
    {
      "course_id":"013035",
      "subject":"CLAS",
      "catalog_number":"637",
      "title":"The Underworld and Afterlife in Ancient Mediterranean Literature"
    },
    {
      "course_id":"013036",
      "subject":"CLAS",
      "catalog_number":"640",
      "title":"Eastern Mediterranean Trade and Cultural Exchange"
    },
    {
      "course_id":"013023",
      "subject":"CLAS",
      "catalog_number":"644",
      "title":"The Sacred Island of Delos: Cultural Crossroads"
    },
    {
      "course_id":"013026",
      "subject":"CLAS",
      "catalog_number":"654",
      "title":"Greeks and Egyptians in  Ptolemaic Egypt"
    },
    {
      "course_id":"013027",
      "subject":"CLAS",
      "catalog_number":"655",
      "title":"Roman Frontiers and Provinces"
    },
    {
      "course_id":"013038",
      "subject":"CLAS",
      "catalog_number":"656",
      "title":"Topics in the Principate of Augustus"
    },
    {
      "course_id":"013039",
      "subject":"CLAS",
      "catalog_number":"657",
      "title":"Roman Trade, Travel and Communication"
    },
    {
      "course_id":"013028",
      "subject":"CLAS",
      "catalog_number":"659",
      "title":"The Decline of the Roman Empire and its Conseqences for the Mediterranean"
    },
    {
      "course_id":"013041",
      "subject":"CLAS",
      "catalog_number":"690",
      "title":"Directed Studies"
    },
    {
      "course_id":"013042",
      "subject":"CLAS",
      "catalog_number":"691",
      "title":"Special Topics"
    },
    {
      "course_id":"012670",
      "subject":"CM",
      "catalog_number":"770",
      "title":"Numerical Analysis"
    },
    {
      "course_id":"013603",
      "subject":"CS",
      "catalog_number":"655",
      "title":"System and Network Architectures and Implementation"
    },
    {
      "course_id":"011589",
      "subject":"CS",
      "catalog_number":"667",
      "title":"Quantum Information Processing"
    },
    {
      "course_id":"012670",
      "subject":"CS",
      "catalog_number":"670",
      "title":"Numerical Analysis"
    },
    {
      "course_id":"000617",
      "subject":"CS",
      "catalog_number":"672",
      "title":"Numerical Solution of Large Sparse Systems of Equations"
    },
    {
      "course_id":"000785",
      "subject":"ECE",
      "catalog_number":"633",
      "title":"Bipolar Devices"
    },
    {
      "course_id":"000786",
      "subject":"ECE",
      "catalog_number":"634",
      "title":"Field Effect Devices"
    },
    {
      "course_id":"000787",
      "subject":"ECE",
      "catalog_number":"635",
      "title":"VLSI Systems Design"
    },
    {
      "course_id":"000791",
      "subject":"ECE",
      "catalog_number":"645",
      "title":"Analog Filter Design"
    },
    {
      "course_id":"000830",
      "subject":"ECE",
      "catalog_number":"733",
      "title":"Advanced Bipolar Devices"
    },
    {
      "course_id":"000852",
      "subject":"ECE",
      "catalog_number":"762",
      "title":"Optimization Techniques in Power Systems"
    },
    {
      "course_id":"010658",
      "subject":"ECE",
      "catalog_number":"765",
      "title":"Distribution Systems Engineering"
    },
    {
      "course_id":"013665",
      "subject":"ECON",
      "catalog_number":"622B",
      "title":"Applied Macroeconometrics"
    },
    {
      "course_id":"001209",
      "subject":"ERS",
      "catalog_number":"630",
      "title":"Waste Management"
    },
    {
      "course_id":"013076",
      "subject":"GRK",
      "catalog_number":"673",
      "title":"Greek Comedy"
    },
    {
      "course_id":"013053",
      "subject":"GRK",
      "catalog_number":"691",
      "title":"Special Topics"
    },
    {
      "course_id":"013054",
      "subject":"LAT",
      "catalog_number":"635",
      "title":"Studies in Tacitus Annals I-VI"
    },
    {
      "course_id":"013055",
      "subject":"LAT",
      "catalog_number":"651",
      "title":"Senior Latin Composition, Grammar and Reading"
    },
    {
      "course_id":"013056",
      "subject":"LAT",
      "catalog_number":"691",
      "title":"Special Topics"
    },
    {
      "course_id":"013839",
      "subject":"MATH",
      "catalog_number":"670",
      "title":"Mathematical Connections:  Real World Problems in Mathematics I"
    },
    {
      "course_id":"013838",
      "subject":"MATH",
      "catalog_number":"671",
      "title":"Mathematical Connections: Real World Problems in Mathematics II"
    },
    {
      "course_id":"013837",
      "subject":"MATH",
      "catalog_number":"672",
      "title":"Mathematical Connections:  Real World Problems in Mathematics III"
    },
    {
      "course_id":"013836",
      "subject":"MATH",
      "catalog_number":"673",
      "title":"Mathematical Connections:  Real World Problems in Mathematics IV"
    },
    {
      "course_id":"001924",
      "subject":"MSCI",
      "catalog_number":"600",
      "title":"Modeling in the Management Sciences"
    },
    {
      "course_id":"011081",
      "subject":"MSCI",
      "catalog_number":"726",
      "title":"Telecommunications Management"
    },
    {
      "course_id":"001980",
      "subject":"MSCI",
      "catalog_number":"732",
      "title":"Mathematical Programming Models: Design and Implementation"
    },
    {
      "course_id":"013058",
      "subject":"NES",
      "catalog_number":"615",
      "title":"Ancient Near Eastern Philosophy and Spirituality"
    },
    {
      "course_id":"013086",
      "subject":"NES",
      "catalog_number":"621",
      "title":"Temples and Sanctuaries in the Eastern Mediterranean World"
    },
    {
      "course_id":"013087",
      "subject":"NES",
      "catalog_number":"625",
      "title":"Myth and Burial Customs in the Ancient Near East"
    },
    {
      "course_id":"013088",
      "subject":"NES",
      "catalog_number":"631",
      "title":"Old Babylonian Royal Inscriptions"
    },
    {
      "course_id":"013091",
      "subject":"NES",
      "catalog_number":"632",
      "title":"Old Babylonian Administrative Documents and Literature"
    },
    {
      "course_id":"013089",
      "subject":"NES",
      "catalog_number":"690",
      "title":"Directed Studies"
    },
    {
      "course_id":"013090",
      "subject":"NES",
      "catalog_number":"691",
      "title":"Special Topics"
    },
    {
      "course_id":"002211",
      "subject":"PHYS",
      "catalog_number":"741",
      "title":"Electron Microscopy and Electron Diffraction"
    },
    {
      "course_id":"002212",
      "subject":"PHYS",
      "catalog_number":"742",
      "title":"Basic Theory of Nuclear Magnetic Resonance"
    },
    {
      "course_id":"002221",
      "subject":"PHYS",
      "catalog_number":"753",
      "title":"Radiation Biophysics"
    },
    {
      "course_id":"002223",
      "subject":"PHYS",
      "catalog_number":"755",
      "title":"Biophysics of Organ Systems"
    },
    {
      "course_id":"010429",
      "subject":"PLAN",
      "catalog_number":"610",
      "title":"Public Administration of the Environment & Natural Resources"
    },
    {
      "course_id":"001397",
      "subject":"PLAN",
      "catalog_number":"668",
      "title":"Environmental Assessment"
    },
    {
      "course_id":"002505",
      "subject":"PSYCH",
      "catalog_number":"608C",
      "title":"Child Psychopathology and Psychotherapy Practicum"
    },
    {
      "course_id":"002504",
      "subject":"PSYCH",
      "catalog_number":"608B",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"011259",
      "subject":"PSYCH",
      "catalog_number":"609",
      "title":"Practicum in Supervision"
    },
    {
      "course_id":"002512",
      "subject":"PSYCH",
      "catalog_number":"610A",
      "title":"Practicum in Integrated Assessment 1"
    },
    {
      "course_id":"002513",
      "subject":"PSYCH",
      "catalog_number":"610B",
      "title":"Practicum in Integrated Assessment 2"
    },
    {
      "course_id":"002514",
      "subject":"PSYCH",
      "catalog_number":"611",
      "title":"Ethics Diversity, & Professional Issues in Clinical Psychology"
    },
    {
      "course_id":"014305",
      "subject":"PSYCH",
      "catalog_number":"614C",
      "title":"Practicum in Couples' Therapy"
    },
    {
      "course_id":"013032",
      "subject":"PSYCH",
      "catalog_number":"614A",
      "title":"Theory and Application in Couples'  Therapy"
    },
    {
      "course_id":"013760",
      "subject":"PSYCH",
      "catalog_number":"614B",
      "title":"Practicum in Couples' Therapy"
    },
    {
      "course_id":"002516",
      "subject":"PSYCH",
      "catalog_number":"616",
      "title":"Clinical Research Forum"
    },
    {
      "course_id":"011732",
      "subject":"PSYCH",
      "catalog_number":"617",
      "title":"Cross-Cultural Issues in Clinical Psychology"
    },
    {
      "course_id":"012338",
      "subject":"PSYCH",
      "catalog_number":"618",
      "title":"Practicum in Interviewing & Cognitive Assessment I"
    },
    {
      "course_id":"012328",
      "subject":"PSYCH",
      "catalog_number":"619",
      "title":"Practicum in Interviewing & Cognitive Assessment II"
    },
    {
      "course_id":"013761",
      "subject":"PSYCH",
      "catalog_number":"620",
      "title":"Diagnostic Assessment Practicum"
    },
    {
      "course_id":"002517",
      "subject":"PSYCH",
      "catalog_number":"621A",
      "title":"Advanced Clinical Research Forum I"
    },
    {
      "course_id":"002518",
      "subject":"PSYCH",
      "catalog_number":"621B",
      "title":"Advanced Clinical Research Forum I"
    },
    {
      "course_id":"002520",
      "subject":"PSYCH",
      "catalog_number":"622A",
      "title":"Advanced Clnical Research Forum II"
    },
    {
      "course_id":"002521",
      "subject":"PSYCH",
      "catalog_number":"622B",
      "title":"Advanced Clinical Research Forum II"
    },
    {
      "course_id":"002523",
      "subject":"PSYCH",
      "catalog_number":"623A",
      "title":"Advanced Clinical Research Forum III"
    },
    {
      "course_id":"002524",
      "subject":"PSYCH",
      "catalog_number":"623B",
      "title":"Advanced Clinical Research Forum III"
    },
    {
      "course_id":"002525",
      "subject":"PSYCH",
      "catalog_number":"624A",
      "title":"Advanced Clinical Research Forum IV"
    },
    {
      "course_id":"002526",
      "subject":"PSYCH",
      "catalog_number":"624B",
      "title":"Advanced Clinical Research Forum IV"
    },
    {
      "course_id":"002528",
      "subject":"PSYCH",
      "catalog_number":"625B",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"002529",
      "subject":"PSYCH",
      "catalog_number":"626A",
      "title":"Psychotherapy Practicum I"
    },
    {
      "course_id":"002530",
      "subject":"PSYCH",
      "catalog_number":"626B",
      "title":"Psychotherapy Practicum I"
    },
    {
      "course_id":"002531",
      "subject":"PSYCH",
      "catalog_number":"626C",
      "title":"Psychotherapy Practicum I"
    },
    {
      "course_id":"002532",
      "subject":"PSYCH",
      "catalog_number":"627A",
      "title":"Psychotheraphy Practicum II"
    },
    {
      "course_id":"002533",
      "subject":"PSYCH",
      "catalog_number":"627B",
      "title":"Psychotheraphy Practicum II"
    },
    {
      "course_id":"002534",
      "subject":"PSYCH",
      "catalog_number":"627C",
      "title":"Psychotherapy Practicum II"
    },
    {
      "course_id":"002535",
      "subject":"PSYCH",
      "catalog_number":"628A",
      "title":"Psychotherapy Practicum III"
    },
    {
      "course_id":"002536",
      "subject":"PSYCH",
      "catalog_number":"628B",
      "title":"Psychotherapy Practicum III"
    },
    {
      "course_id":"002537",
      "subject":"PSYCH",
      "catalog_number":"628C",
      "title":"Psychotherapy Practicum III"
    },
    {
      "course_id":"012017",
      "subject":"PSYCH",
      "catalog_number":"629",
      "title":"Psychopathology across the Lifespan"
    },
    {
      "course_id":"010587",
      "subject":"PSYCH",
      "catalog_number":"633",
      "title":"Observation, Interviewing and Cognitive Assessment"
    },
    {
      "course_id":"002540",
      "subject":"PSYCH",
      "catalog_number":"633A",
      "title":"Observation, Interviewing and Cognitive Assessment"
    },
    {
      "course_id":"002541",
      "subject":"PSYCH",
      "catalog_number":"633B",
      "title":"Observation, Interviewing and Cognitive Assessment"
    },
    {
      "course_id":"002542",
      "subject":"PSYCH",
      "catalog_number":"634",
      "title":"Laboratory Research in Clinical Psychology"
    },
    {
      "course_id":"002543",
      "subject":"PSYCH",
      "catalog_number":"635",
      "title":"Clinical Fieldwork Placement I"
    },
    {
      "course_id":"002544",
      "subject":"PSYCH",
      "catalog_number":"636",
      "title":"Clinical Fieldwork Placement II"
    },
    {
      "course_id":"010588",
      "subject":"PSYCH",
      "catalog_number":"637",
      "title":"SCID-I Administration"
    },
    {
      "course_id":"002545",
      "subject":"PSYCH",
      "catalog_number":"638",
      "title":"Personality"
    },
    {
      "course_id":"002548",
      "subject":"PSYCH",
      "catalog_number":"639",
      "title":"Psychopathology in Childhood and Adolescence"
    },
    {
      "course_id":"002723",
      "subject":"PSYCH",
      "catalog_number":"707B",
      "title":"Behavioural Neuroscience Seminar I"
    },
    {
      "course_id":"002743",
      "subject":"PSYCH",
      "catalog_number":"714B",
      "title":"Behavioural Neuroscience Seminar II"
    },
    {
      "course_id":"002747",
      "subject":"PSYCH",
      "catalog_number":"727A",
      "title":"Behavioural Neuroscience Seminar III"
    },
    {
      "course_id":"002748",
      "subject":"PSYCH",
      "catalog_number":"727B",
      "title":"Behavioural Neuroscience Seminar III"
    },
    {
      "course_id":"013066",
      "subject":"RUSS",
      "catalog_number":"620",
      "title":"Topics in Folklore, Early, and Petrine Literature"
    },
    {
      "course_id":"013067",
      "subject":"RUSS",
      "catalog_number":"621",
      "title":"Topics in the Literature of the Golden Age, Realism, and Modernism"
    },
    {
      "course_id":"013069",
      "subject":"RUSS",
      "catalog_number":"623",
      "title":"Themes in Russian Literature"
    },
    {
      "course_id":"013070",
      "subject":"RUSS",
      "catalog_number":"670",
      "title":"Topics in Russian Linguistics"
    },
    {
      "course_id":"013071",
      "subject":"RUSS",
      "catalog_number":"671",
      "title":"Topics in Slavic Linguistics"
    },
    {
      "course_id":"003019",
      "subject":"RUSS",
      "catalog_number":"695",
      "title":"Reading Courses in Approved Topics"
    },
    {
      "course_id":"003145",
      "subject":"SYDE",
      "catalog_number":"624",
      "title":"System Simulation: Advanced Topics"
    },
    {
      "course_id":"013975",
      "subject":"COMST",
      "catalog_number":"202W",
      "title":"Nonverbal Communication (WLU)"
    },
    {
      "course_id":"013973",
      "subject":"ENVS",
      "catalog_number":"295W",
      "title":"Ecotourism and the Environment (WLU)`"
    },
    {
      "course_id":"013274",
      "subject":"GBDA",
      "catalog_number":"206",
      "title":"Issues in Contemporary Global Ethics"
    },
    {
      "course_id":"013267",
      "subject":"GBDA",
      "catalog_number":"307",
      "title":"Workshop in Digital Media, Marketing and Management 1"
    },
    {
      "course_id":"013268",
      "subject":"GBDA",
      "catalog_number":"308",
      "title":"Workshop in Digital Media, Marketing and Management 2"
    },
    {
      "course_id":"013735",
      "subject":"ISS",
      "catalog_number":"215R",
      "title":"Education and Social Development from a Global Perspective"
    },
    {
      "course_id":"013893",
      "subject":"ISS",
      "catalog_number":"231R",
      "title":"Introduction to Social Policy Processes"
    },
    {
      "course_id":"013894",
      "subject":"ISS",
      "catalog_number":"331R",
      "title":"Social Inequality, Social Justice, and Public Policy"
    },
    {
      "course_id":"013736",
      "subject":"ISS",
      "catalog_number":"351R",
      "title":"Qualitative Research in Social Development Studies"
    },
    {
      "course_id":"013891",
      "subject":"ISS",
      "catalog_number":"355R",
      "title":"Resilience and Social Support"
    },
    {
      "course_id":"013737",
      "subject":"ISS",
      "catalog_number":"415R",
      "title":"Gender Relations within Educational Institutions"
    },
    {
      "course_id":"013738",
      "subject":"ISS",
      "catalog_number":"425R",
      "title":"Educational Equity in Canada"
    },
    {
      "course_id":"013892",
      "subject":"ISS",
      "catalog_number":"440R",
      "title":"Optimal Living"
    },
    {
      "course_id":"014101",
      "subject":"PSCI",
      "catalog_number":"350W",
      "title":"Theories of Justice (WLU)"
    },
    {
      "course_id":"011259",
      "subject":"PSYCH",
      "catalog_number":"609A",
      "title":"Practicum in Supervision"
    },
    {
      "course_id":"014066",
      "subject":"PSYCH",
      "catalog_number":"609B",
      "title":"Practicum in Supervision"
    },
    {
      "course_id":"014044",
      "subject":"PSYCH",
      "catalog_number":"609C",
      "title":"Practicum in Supervision"
    },
    {
      "course_id":"010582",
      "subject":"PSYCH",
      "catalog_number":"612A",
      "title":"Private Practice Placement"
    },
    {
      "course_id":"010583",
      "subject":"PSYCH",
      "catalog_number":"612B",
      "title":"Private Practice Placement"
    },
    {
      "course_id":"014025",
      "subject":"PSYCH",
      "catalog_number":"612C",
      "title":"Private Practice Placement"
    },
    {
      "course_id":"010584",
      "subject":"PSYCH",
      "catalog_number":"613A",
      "title":"Senior Practicum"
    },
    {
      "course_id":"010585",
      "subject":"PSYCH",
      "catalog_number":"613B",
      "title":"Senior Practicum"
    },
    {
      "course_id":"010586",
      "subject":"PSYCH",
      "catalog_number":"613C",
      "title":"Senior Practicum"
    },
    {
      "course_id":"013761",
      "subject":"PSYCH",
      "catalog_number":"620A",
      "title":"Diagnostic Assessment Practicum"
    },
    {
      "course_id":"014046",
      "subject":"PSYCH",
      "catalog_number":"620B",
      "title":"Diagnostic Assessment Practicum"
    },
    {
      "course_id":"002527",
      "subject":"PSYCH",
      "catalog_number":"625A",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014047",
      "subject":"PSYCH",
      "catalog_number":"625C",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"002543",
      "subject":"PSYCH",
      "catalog_number":"635A",
      "title":"Clinical Fieldwork Placement I"
    },
    {
      "course_id":"014048",
      "subject":"PSYCH",
      "catalog_number":"635B",
      "title":"Clinical Fieldwork Placement I"
    },
    {
      "course_id":"014049",
      "subject":"PSYCH",
      "catalog_number":"635C",
      "title":"Clinical Fieldwork Placement I"
    },
    {
      "course_id":"002544",
      "subject":"PSYCH",
      "catalog_number":"636A",
      "title":"Clinical Fieldwork Placement II"
    },
    {
      "course_id":"014050",
      "subject":"PSYCH",
      "catalog_number":"636B",
      "title":"Clin Fieldwork Placement II"
    },
    {
      "course_id":"014051",
      "subject":"PSYCH",
      "catalog_number":"636C",
      "title":"Clinical Fieldwork Placement II"
    },
    {
      "course_id":"010588",
      "subject":"PSYCH",
      "catalog_number":"637A",
      "title":"Clinical Fieldwork Placement III"
    },
    {
      "course_id":"014052",
      "subject":"PSYCH",
      "catalog_number":"637B",
      "title":"Clinical Fieldwork Placement III"
    },
    {
      "course_id":"014053",
      "subject":"PSYCH",
      "catalog_number":"637C",
      "title":"Clinical Fieldwork Placement III"
    },
    {
      "course_id":"013974",
      "subject":"RELC",
      "catalog_number":"265W",
      "title":"Cults, Sects and New Religious Movements (WLU)"
    },
    {
      "course_id":"014075",
      "subject":"SOCIN",
      "catalog_number":"63",
      "title":"Team Process and Research Skills: Communication, Facilitation, Collaboration, Problem Solving"
    },
    {
      "course_id":"014317",
      "subject":"HLTH",
      "catalog_number":"402",
      "title":"Advanced Health Promotion"
    },
    {
      "course_id":"002506",
      "subject":"PSYCH",
      "catalog_number":"608D",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"014197",
      "subject":"PSYCH",
      "catalog_number":"608E",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"002507",
      "subject":"PSYCH",
      "catalog_number":"608F",
      "title":"Child Psychopathology & PsychotherapyPracticum"
    },
    {
      "course_id":"014198",
      "subject":"PSYCH",
      "catalog_number":"608G",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"014199",
      "subject":"PSYCH",
      "catalog_number":"608H",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"014200",
      "subject":"PSYCH",
      "catalog_number":"608I",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"014201",
      "subject":"PSYCH",
      "catalog_number":"608J",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"014202",
      "subject":"PSYCH",
      "catalog_number":"608K",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"014203",
      "subject":"PSYCH",
      "catalog_number":"608L",
      "title":"Child Psychopathology & Psychotherapy Practicum"
    },
    {
      "course_id":"002500",
      "subject":"PSYCH",
      "catalog_number":"615A",
      "title":"Cognitive Behaviour Therapy"
    },
    {
      "course_id":"002501",
      "subject":"PSYCH",
      "catalog_number":"615B",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014177",
      "subject":"PSYCH",
      "catalog_number":"615C",
      "title":"Cognitivie Behaviour Theraphy Practicum"
    },
    {
      "course_id":"014178",
      "subject":"PSYCH",
      "catalog_number":"615D",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014179",
      "subject":"PSYCH",
      "catalog_number":"615E",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014180",
      "subject":"PSYCH",
      "catalog_number":"615F",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014181",
      "subject":"PSYCH",
      "catalog_number":"615G",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014186",
      "subject":"PSYCH",
      "catalog_number":"615H",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014187",
      "subject":"PSYCH",
      "catalog_number":"615I",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014188",
      "subject":"PSYCH",
      "catalog_number":"615J",
      "title":"Cognitive Behaviour Therapy Practicum"
    },
    {
      "course_id":"014204",
      "subject":"PSYCH",
      "catalog_number":"625D",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014205",
      "subject":"PSYCH",
      "catalog_number":"625E",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014206",
      "subject":"PSYCH",
      "catalog_number":"625F",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014207",
      "subject":"PSYCH",
      "catalog_number":"625G",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014208",
      "subject":"PSYCH",
      "catalog_number":"625H",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014209",
      "subject":"PSYCH",
      "catalog_number":"625I",
      "title":"Traditional and Contemporary Psychotherapies"
    },
    {
      "course_id":"014306",
      "subject":"PSYCH",
      "catalog_number":"638B",
      "title":"Measurement and Test Theory"
    },
    {
      "course_id":"014307",
      "subject":"PSYCH",
      "catalog_number":"645",
      "title":"Structure and Function in the Developing Brain"
    },
    {
      "course_id":"014238",
      "subject":"SWK",
      "catalog_number":"606R",
      "title":"Practicum 1"
    },
    {
      "course_id":"014239",
      "subject":"SWK",
      "catalog_number":"607R",
      "title":"Practicum 2"
    },
    {
      "course_id":"014656",
      "subject":"ACINTY",
      "catalog_number":"600",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014657",
      "subject":"ACINTY",
      "catalog_number":"610",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014658",
      "subject":"ACINTY",
      "catalog_number":"620",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014659",
      "subject":"ACINTY",
      "catalog_number":"630",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014660",
      "subject":"ACINTY",
      "catalog_number":"640",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014661",
      "subject":"ACINTY",
      "catalog_number":"650",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014662",
      "subject":"ACINTY",
      "catalog_number":"660",
      "title":"Academic Integrity Module"
    },
    {
      "course_id":"014853",
      "subject":"AFM",
      "catalog_number":"479",
      "title":"Cases and Applications in Finance II"
    },
    {
      "course_id":"014564",
      "subject":"AMATH",
      "catalog_number":"390",
      "title":"Mathematics and Music"
    },
    {
      "course_id":"014704",
      "subject":"ANTH",
      "catalog_number":"100",
      "title":"Introduction to Anthropology"
    },
    {
      "course_id":"014705",
      "subject":"ANTH",
      "catalog_number":"204",
      "title":"Biological Anthropology"
    },
    {
      "course_id":"014707",
      "subject":"ANTH",
      "catalog_number":"372",
      "title":"Archaeological Field School"
    },
    {
      "course_id":"014706",
      "subject":"ANTH",
      "catalog_number":"381",
      "title":"Anthropology of South Asia"
    },
    {
      "course_id":"014709",
      "subject":"ANTH",
      "catalog_number":"382",
      "title":"Anthropology of Contemporary China"
    },
    {
      "course_id":"014710",
      "subject":"ANTH",
      "catalog_number":"430",
      "title":"Anthropology of Science"
    },
    {
      "course_id":"014711",
      "subject":"ANTH",
      "catalog_number":"447",
      "title":"Seminar in Medical Anthropology"
    },
    {
      "course_id":"014712",
      "subject":"ANTH",
      "catalog_number":"498",
      "title":"Anthropology Capstone"
    },
    {
      "course_id":"014762",
      "subject":"BASE",
      "catalog_number":"32",
      "title":"Academic Skills"
    },
    {
      "course_id":"014763",
      "subject":"BASE",
      "catalog_number":"34",
      "title":"Writing Skills"
    },
    {
      "course_id":"014764",
      "subject":"BASE",
      "catalog_number":"36",
      "title":"Oral Skills"
    },
    {
      "course_id":"014765",
      "subject":"BASE",
      "catalog_number":"42",
      "title":"Academic Skills"
    },
    {
      "course_id":"014766",
      "subject":"BASE",
      "catalog_number":"44",
      "title":"Writing Skills"
    },
    {
      "course_id":"014767",
      "subject":"BASE",
      "catalog_number":"46",
      "title":"Oral Skills"
    },
    {
      "course_id":"014844",
      "subject":"BET",
      "catalog_number":"100",
      "title":"Essentials of Entrepreneurial Behaviour"
    },
    {
      "course_id":"014679",
      "subject":"BET",
      "catalog_number":"310",
      "title":"Enterprise Co-op Entrepreneurship Planning and Execution"
    },
    {
      "course_id":"014678",
      "subject":"BET",
      "catalog_number":"320",
      "title":"Introduction to Commercialization Management"
    },
    {
      "course_id":"014680",
      "subject":"BET",
      "catalog_number":"410A",
      "title":"Capstone Entrepreneurship Planning and Execution Part 1"
    },
    {
      "course_id":"014681",
      "subject":"BET",
      "catalog_number":"410B",
      "title":"Capstone Entrepreneurship Planning and Execution Part 2"
    },
    {
      "course_id":"014690",
      "subject":"BIOL",
      "catalog_number":"101",
      "title":"Biology in the Modern World"
    },
    {
      "course_id":"014689",
      "subject":"BIOL",
      "catalog_number":"414",
      "title":"Parasitology"
    },
    {
      "course_id":"014858",
      "subject":"BME",
      "catalog_number":"102",
      "title":"Seminar"
    },
    {
      "course_id":"014433",
      "subject":"BME",
      "catalog_number":"184",
      "title":"Engineering Biology"
    },
    {
      "course_id":"014434",
      "subject":"BME",
      "catalog_number":"184L",
      "title":"Engineering Biology Laboratory"
    },
    {
      "course_id":"014859",
      "subject":"BME",
      "catalog_number":"201",
      "title":"Seminar"
    },
    {
      "course_id":"014860",
      "subject":"BME",
      "catalog_number":"202",
      "title":"Seminar"
    },
    {
      "course_id":"014454",
      "subject":"BME",
      "catalog_number":"213",
      "title":"Statistics and Experimental Design"
    },
    {
      "course_id":"014441",
      "subject":"BME",
      "catalog_number":"261",
      "title":"Prototyping, Simulation and Design"
    },
    {
      "course_id":"014455",
      "subject":"BME",
      "catalog_number":"281",
      "title":"Mechanics of Deformable Solids"
    },
    {
      "course_id":"014456",
      "subject":"BME",
      "catalog_number":"281L",
      "title":"Mechanics of Deformable Solids Laboratory"
    },
    {
      "course_id":"014457",
      "subject":"BME",
      "catalog_number":"282",
      "title":"Materials Science for Biomedical Engineers"
    },
    {
      "course_id":"014432",
      "subject":"BME",
      "catalog_number":"283",
      "title":"Chemistry Principles"
    },
    {
      "course_id":"014435",
      "subject":"BME",
      "catalog_number":"284",
      "title":"Physiological and Biological Systems"
    },
    {
      "course_id":"014436",
      "subject":"BME",
      "catalog_number":"284L",
      "title":"Physiology and Anatomy Laboratory"
    },
    {
      "course_id":"014433",
      "subject":"BME",
      "catalog_number":"285",
      "title":"Engineering Biology"
    },
    {
      "course_id":"014459",
      "subject":"BME",
      "catalog_number":"286",
      "title":"The Physics of Medical Imaging"
    },
    {
      "course_id":"014460",
      "subject":"BME",
      "catalog_number":"292",
      "title":"Digital Systems"
    },
    {
      "course_id":"014461",
      "subject":"BME",
      "catalog_number":"292L",
      "title":"Digital Systems Laboratory"
    },
    {
      "course_id":"014861",
      "subject":"BME",
      "catalog_number":"301",
      "title":"Seminar"
    },
    {
      "course_id":"014862",
      "subject":"BME",
      "catalog_number":"302",
      "title":"Seminar"
    },
    {
      "course_id":"014462",
      "subject":"BME",
      "catalog_number":"351",
      "title":"Linear Signals and Systems"
    },
    {
      "course_id":"014463",
      "subject":"BME",
      "catalog_number":"352",
      "title":"Control Systems"
    },
    {
      "course_id":"014464",
      "subject":"BME",
      "catalog_number":"352L",
      "title":"Control Systems Laboratory"
    },
    {
      "course_id":"014437",
      "subject":"BME",
      "catalog_number":"354",
      "title":"Anatomical Systems Modeling"
    },
    {
      "course_id":"014442",
      "subject":"BME",
      "catalog_number":"361",
      "title":"Biomedical Engineering Design"
    },
    {
      "course_id":"014443",
      "subject":"BME",
      "catalog_number":"362",
      "title":"Biomedical Engineering Design Workshop 1"
    },
    {
      "course_id":"014465",
      "subject":"BME",
      "catalog_number":"364",
      "title":"Engineering Healthcare Economics"
    },
    {
      "course_id":"014444",
      "subject":"BME",
      "catalog_number":"381",
      "title":"Biomedical Ethics and Engineering Design"
    },
    {
      "course_id":"014438",
      "subject":"BME",
      "catalog_number":"384",
      "title":"Biomedical Transport: Biofluids and Mass Transfer"
    },
    {
      "course_id":"014466",
      "subject":"BME",
      "catalog_number":"391",
      "title":"Circuits, Instrumentation, and Measurements"
    },
    {
      "course_id":"014467",
      "subject":"BME",
      "catalog_number":"391L",
      "title":"Circuits, Instrumentation, and Measurements Laboratory"
    },
    {
      "course_id":"014863",
      "subject":"BME",
      "catalog_number":"401",
      "title":"Seminar"
    },
    {
      "course_id":"014864",
      "subject":"BME",
      "catalog_number":"402",
      "title":"Seminar"
    },
    {
      "course_id":"014468",
      "subject":"BME",
      "catalog_number":"411",
      "title":"Optimization and Numerical Methods"
    },
    {
      "course_id":"014445",
      "subject":"BME",
      "catalog_number":"461",
      "title":"Biomedical Engineering Design Workshop 2"
    },
    {
      "course_id":"014446",
      "subject":"BME",
      "catalog_number":"462",
      "title":"Biomedical Engineering Design Workshop 3"
    },
    {
      "course_id":"004859",
      "subject":"EARTH",
      "catalog_number":"439",
      "title":"Flow and Transport Through Fractured Rocks"
    },
    {
      "course_id":"014777",
      "subject":"EARTH",
      "catalog_number":"695",
      "title":"Earth MSc Seminar Proposal"
    },
    {
      "course_id":"014876",
      "subject":"EASIA",
      "catalog_number":"231R",
      "title":"Calligraphy to Conceptual Art: Text as an Image in Islamic and East Asian Visual Arts"
    },
    {
      "course_id":"014789",
      "subject":"EASIA",
      "catalog_number":"260R",
      "title":"Modern Chinese Literature (1917 - present day)"
    },
    {
      "course_id":"014875",
      "subject":"EASIA",
      "catalog_number":"377R",
      "title":"Cold War in East Asia"
    },
    {
      "course_id":"014715",
      "subject":"ECE",
      "catalog_number":"650",
      "title":"Methods and Tools for Software Engineering"
    },
    {
      "course_id":"014723",
      "subject":"ECON",
      "catalog_number":"412",
      "title":"Game Theory"
    },
    {
      "course_id":"014730",
      "subject":"ECON",
      "catalog_number":"741",
      "title":"Advanced Public Economics Expenditure"
    },
    {
      "course_id":"014731",
      "subject":"ECON",
      "catalog_number":"742",
      "title":"Advanced Public Economics: Taxation"
    },
    {
      "course_id":"014732",
      "subject":"ECON",
      "catalog_number":"751",
      "title":"Advanced Labour Economics"
    },
    {
      "course_id":"014733",
      "subject":"ECON",
      "catalog_number":"757",
      "title":"Advanced Environmental Economics"
    },
    {
      "course_id":"011984",
      "subject":"EMLS",
      "catalog_number":"101R",
      "title":"Oral Communications for Academic Purposes"
    },
    {
      "course_id":"011985",
      "subject":"EMLS",
      "catalog_number":"102R",
      "title":"Error Correction in Academic Writing"
    },
    {
      "course_id":"014140",
      "subject":"EMLS",
      "catalog_number":"103R",
      "title":"Phonetics for Effective English Pronunciation"
    },
    {
      "course_id":"014967",
      "subject":"EMLS",
      "catalog_number":"104R",
      "title":"Reading and Listening for Academic Purposes"
    },
    {
      "course_id":"013932",
      "subject":"EMLS",
      "catalog_number":"110R",
      "title":"Critical Expression in Canadian Academic Contexts"
    },
    {
      "course_id":"005061",
      "subject":"EMLS",
      "catalog_number":"129R",
      "title":"Written Academic English"
    },
    {
      "course_id":"014790",
      "subject":"ENGL",
      "catalog_number":"294",
      "title":"Game Studies"
    },
    {
      "course_id":"014791",
      "subject":"ENGL",
      "catalog_number":"295",
      "title":"Social Media"
    },
    {
      "course_id":"014717",
      "subject":"ERS",
      "catalog_number":"374",
      "title":"Special Topics in Environmental and Resource Studies"
    },
    {
      "course_id":"014683",
      "subject":"ERS",
      "catalog_number":"422",
      "title":"Biosphere Reserves as Social-Ecological Systems"
    },
    {
      "course_id":"014682",
      "subject":"ERS",
      "catalog_number":"454",
      "title":"Parks and Protected Areas: Issues and Trends"
    },
    {
      "course_id":"014718",
      "subject":"ERS",
      "catalog_number":"473",
      "title":"Special Topics in Environmental and Resource Studies"
    },
    {
      "course_id":"014738",
      "subject":"ERS",
      "catalog_number":"622",
      "title":"Biosphere Reserves as Social-Ecological Systems"
    },
    {
      "course_id":"014739",
      "subject":"ERS",
      "catalog_number":"654",
      "title":"Parks and Protected Areas"
    },
    {
      "course_id":"014740",
      "subject":"ERS",
      "catalog_number":"684",
      "title":"Soil in the Enviornment"
    },
    {
      "course_id":"014691",
      "subject":"EVSY",
      "catalog_number":"302W",
      "title":"Climate Chnge and Soc (WLU)"
    },
    {
      "course_id":"015175",
      "subject":"FINE",
      "catalog_number":"258",
      "title":"Aspects of the Cinemas of the Americas"
    },
    {
      "course_id":"014876",
      "subject":"FINE",
      "catalog_number":"275",
      "title":"Calligraphy to Conceptual Art: Text as an Image in Islamic and East Asian Visual Arts"
    },
    {
      "course_id":"015143",
      "subject":"FINE",
      "catalog_number":"383",
      "title":"Computational Digital Art Studio"
    },
    {
      "course_id":"014649",
      "subject":"GENE",
      "catalog_number":"21N",
      "title":"Topics for Technical Courses Taken on Exchange by Nanotechnology Engineering Students"
    },
    {
      "course_id":"014648",
      "subject":"GENE",
      "catalog_number":"21U",
      "title":"Topics for Technical Courses Taken on Exchange by Management Engineering Students"
    },
    {
      "course_id":"014735",
      "subject":"GEOG",
      "catalog_number":"654",
      "title":"Applied Biogeochemistry"
    },
    {
      "course_id":"014875",
      "subject":"HIST",
      "catalog_number":"377R",
      "title":"Cold War in East Asia"
    },
    {
      "course_id":"014737",
      "subject":"HIST",
      "catalog_number":"660",
      "title":"Transnational and Global History: Old Problems and New Directions"
    },
    {
      "course_id":"014684",
      "subject":"INDEV",
      "catalog_number":"476",
      "title":"Contemporary Issues in Development Practice"
    },
    {
      "course_id":"014687",
      "subject":"INDEV",
      "catalog_number":"490A",
      "title":"Honours Thesis: Project Preparation"
    },
    {
      "course_id":"014688",
      "subject":"INDEV",
      "catalog_number":"490B",
      "title":"Honours Thesis: Project Completion"
    },
    {
      "course_id":"014693",
      "subject":"INTEG",
      "catalog_number":"452A",
      "title":"Real World Problem Solving A"
    },
    {
      "course_id":"014694",
      "subject":"INTEG",
      "catalog_number":"452B",
      "title":"Real world Problem Solving B"
    },
    {
      "course_id":"014871",
      "subject":"JS",
      "catalog_number":"114",
      "title":"Jews and Jewishness"
    },
    {
      "course_id":"012721",
      "subject":"JS",
      "catalog_number":"131",
      "title":"Big Ideas of the Bible"
    },
    {
      "course_id":"012724",
      "subject":"JS",
      "catalog_number":"237",
      "title":"Insiders and Outsiders in the Bible"
    },
    {
      "course_id":"012720",
      "subject":"JS",
      "catalog_number":"338",
      "title":"Seeking Wisdom in the Bible"
    },
    {
      "course_id":"014846",
      "subject":"LS",
      "catalog_number":"240",
      "title":"Terrorism"
    },
    {
      "course_id":"014849",
      "subject":"LS",
      "catalog_number":"425",
      "title":"Crossing Borders: Law & Global Deviance"
    },
    {
      "course_id":"014805",
      "subject":"MATH",
      "catalog_number":"642",
      "title":"Introduction to Computer Science: A Mathematical Perspective"
    },
    {
      "course_id":"014806",
      "subject":"MATH",
      "catalog_number":"643",
      "title":"Theory of Computation"
    },
    {
      "course_id":"014926",
      "subject":"MSCI",
      "catalog_number":"723",
      "title":"Big Data Analytics"
    },
    {
      "course_id":"014928",
      "subject":"MSCI",
      "catalog_number":"724",
      "title":"Design and Analysis of Information Procurement Mechanisms"
    },
    {
      "course_id":"014929",
      "subject":"MSCI",
      "catalog_number":"731",
      "title":"Matrix-Analytic Methods in Stochastic Models"
    },
    {
      "course_id":"014930",
      "subject":"MSCI",
      "catalog_number":"734",
      "title":"Network Models and Applications"
    },
    {
      "course_id":"014931",
      "subject":"MSCI",
      "catalog_number":"744",
      "title":"Science and Technology Policy"
    },
    {
      "course_id":"014677",
      "subject":"NE",
      "catalog_number":"111",
      "title":"Introduction to Engineering Computing"
    },
    {
      "course_id":"014639",
      "subject":"PHARM",
      "catalog_number":"155",
      "title":"Introduction to Drug Information Fundamentals"
    },
    {
      "course_id":"014745",
      "subject":"PHARM",
      "catalog_number":"379",
      "title":"Ethical Decision-Making in Pharmacy Practice"
    },
    {
      "course_id":"014640",
      "subject":"PHARM",
      "catalog_number":"425",
      "title":"Symposium"
    },
    {
      "course_id":"014641",
      "subject":"PHARM",
      "catalog_number":"430",
      "title":"Clinical Rotation 1: Primary Care"
    },
    {
      "course_id":"014642",
      "subject":"PHARM",
      "catalog_number":"440",
      "title":"Clinical Rotation 2: Institutional"
    },
    {
      "course_id":"014643",
      "subject":"PHARM",
      "catalog_number":"450",
      "title":"Clinical Rotation 3: Elective"
    },
    {
      "course_id":"014647",
      "subject":"PHARM",
      "catalog_number":"473",
      "title":"Advanced Infectious Disease"
    },
    {
      "course_id":"014743",
      "subject":"PHARM",
      "catalog_number":"474",
      "title":"Advanced Pharmacotherapeutics in the Hospital Setting"
    },
    {
      "course_id":"014744",
      "subject":"PHARM",
      "catalog_number":"475",
      "title":"Advanced Pharmacotherapeutics in the Ambulatory Care Setting"
    },
    {
      "course_id":"014747",
      "subject":"PHARM",
      "catalog_number":"476",
      "title":"Advanced Skills in Patient Engagement"
    },
    {
      "course_id":"014810",
      "subject":"PHARM",
      "catalog_number":"496",
      "title":"Advanced Professional Practice"
    },
    {
      "course_id":"014811",
      "subject":"PHARM",
      "catalog_number":"497",
      "title":"Clinical Rotation 1: Direct Patient Care Fundamentals"
    },
    {
      "course_id":"014812",
      "subject":"PHARM",
      "catalog_number":"498",
      "title":"Clinical Rotation 2: Direct Patient Care"
    },
    {
      "course_id":"014813",
      "subject":"PHARM",
      "catalog_number":"499",
      "title":"Clinical Rotation 3: Elective"
    },
    {
      "course_id":"014775",
      "subject":"PHARM",
      "catalog_number":"612",
      "title":"Principles and Practices in Systemic Treatments for Cancer"
    },
    {
      "course_id":"014780",
      "subject":"PHARM",
      "catalog_number":"613",
      "title":"Principles and Practices in Systemic Treatments for Cancer"
    },
    {
      "course_id":"015121",
      "subject":"PHIL",
      "catalog_number":"600",
      "title":"Seminar in Cognitive Science"
    },
    {
      "course_id":"014776",
      "subject":"PHYS",
      "catalog_number":"650",
      "title":"Perimeter Scholars International Explorations in Quantum Gravity"
    },
    {
      "course_id":"014734",
      "subject":"PS",
      "catalog_number":"625",
      "title":"Economics and Public Policy I"
    },
    {
      "course_id":"014741",
      "subject":"PS",
      "catalog_number":"626",
      "title":"Economics and Public Policy II"
    },
    {
      "course_id":"014872",
      "subject":"PSCI",
      "catalog_number":"497A",
      "title":"Study Abroad Experience"
    },
    {
      "course_id":"014873",
      "subject":"PSCI",
      "catalog_number":"497B",
      "title":"Study Abroad Experience"
    },
    {
      "course_id":"014794",
      "subject":"PSCI",
      "catalog_number":"498A",
      "title":"Current Issues in Political Science"
    },
    {
      "course_id":"014795",
      "subject":"PSCI",
      "catalog_number":"498B",
      "title":"Research Apprenticeship Experience"
    },
    {
      "course_id":"014808",
      "subject":"PSCI",
      "catalog_number":"498C",
      "title":"Civic Engagement Experience"
    },
    {
      "course_id":"014878",
      "subject":"PSYCH",
      "catalog_number":"316",
      "title":"Pragmatic Language Development"
    },
    {
      "course_id":"014727",
      "subject":"PSYCH",
      "catalog_number":"878",
      "title":"Job Performance"
    },
    {
      "course_id":"014728",
      "subject":"PSYCH",
      "catalog_number":"879",
      "title":"Personnel Selection"
    },
    {
      "course_id":"014871",
      "subject":"RS",
      "catalog_number":"114",
      "title":"Jews and Jewishness"
    },
    {
      "course_id":"014874",
      "subject":"SI",
      "catalog_number":"230R",
      "title":"Islamic Visual Culture: Art, Architecture, and Aesthetics"
    },
    {
      "course_id":"014876",
      "subject":"SI",
      "catalog_number":"231R",
      "title":"Calligraphy to Conceptual Art: Text as an Image in Islamic and East Asian Visual Arts"
    },
    {
      "course_id":"014846",
      "subject":"SOC",
      "catalog_number":"240",
      "title":"Terrorism"
    },
    {
      "course_id":"014847",
      "subject":"SOC",
      "catalog_number":"270",
      "title":"International Migration"
    },
    {
      "course_id":"008710",
      "subject":"SOC",
      "catalog_number":"310",
      "title":"Social Networks"
    },
    {
      "course_id":"014849",
      "subject":"SOC",
      "catalog_number":"425",
      "title":"Crossing Borders: Law & Global Deviance"
    },
    {
      "course_id":"014803",
      "subject":"SOC",
      "catalog_number":"784",
      "title":"International Migration:  Practice, Theory & Regulation"
    },
    {
      "course_id":"015010",
      "subject":"SPAN",
      "catalog_number":"401",
      "title":"Spanish in Motion"
    },
    {
      "course_id":"014725",
      "subject":"SWK",
      "catalog_number":"672R",
      "title":"International Context of Practice (Mexico); Experimental Learning"
    },
    {
      "course_id":"014724",
      "subject":"SWK",
      "catalog_number":"690R",
      "title":"Special Topics in Social Work"
    },
    {
      "course_id":"015124",
      "subject":"ENGL",
      "catalog_number":"208G",
      "title":"Gothic Monsters"
    },
    {
      "course_id":"013998",
      "subject":"EASIA",
      "catalog_number":"204R",
      "title":"Korean Culture and Society"
    },
    {
      "course_id":"015106",
      "subject":"AHS",
      "catalog_number":"100",
      "title":"Foundations of a Healthy Lifestyle"
    },
    {
      "course_id":"015041",
      "subject":"AHS",
      "catalog_number":"600",
      "title":"Foundations of Qualitative Research Methodologies"
    },
    {
      "course_id":"014749",
      "subject":"AMATH",
      "catalog_number":"383",
      "title":"Introduction to Mathematical Biology"
    },
    {
      "course_id":"000136",
      "subject":"AMATH",
      "catalog_number":"877",
      "title":"Foundations of Quantum Theory"
    },
    {
      "course_id":"003945",
      "subject":"ANTH",
      "catalog_number":"272",
      "title":"Issues in Contemporary Native Communities in Canada"
    },
    {
      "course_id":"015125",
      "subject":"EASIA",
      "catalog_number":"291R",
      "title":"Special Topics in East Asian Studies"
    },
    {
      "course_id":"003541",
      "subject":"ARCH",
      "catalog_number":"126",
      "title":"Environmental Building Design"
    },
    {
      "course_id":"009510",
      "subject":"ARCH",
      "catalog_number":"225",
      "title":"Theory and Design of the Contemporary Landscape"
    },
    {
      "course_id":"003536",
      "subject":"ARCH",
      "catalog_number":"248",
      "title":"Enlightenment, Romanticism and the 19th Century"
    },
    {
      "course_id":"010396",
      "subject":"ARCH",
      "catalog_number":"263",
      "title":"Integrated Environmental Systems"
    },
    {
      "course_id":"011141",
      "subject":"ARCH",
      "catalog_number":"264",
      "title":"Building Science"
    },
    {
      "course_id":"013999",
      "subject":"EASIA",
      "catalog_number":"202R",
      "title":"Chinese Culture and Society"
    },
    {
      "course_id":"003561",
      "subject":"ARCH",
      "catalog_number":"428",
      "title":"Rome and the Campagna (Rome)"
    },
    {
      "course_id":"015005",
      "subject":"ARCH",
      "catalog_number":"429",
      "title":"Global Cities"
    },
    {
      "course_id":"014999",
      "subject":"ARCH",
      "catalog_number":"465",
      "title":"Advanced Structures: Design and Analysis"
    },
    {
      "course_id":"015001",
      "subject":"ARCH",
      "catalog_number":"510",
      "title":"Visual and Digital Media Courses"
    },
    {
      "course_id":"015003",
      "subject":"ARCH",
      "catalog_number":"520",
      "title":"Urbanism and Landscape Courses"
    },
    {
      "course_id":"015004",
      "subject":"ARCH",
      "catalog_number":"540",
      "title":"Architectural History and Theory Courses"
    },
    {
      "course_id":"015002",
      "subject":"ARCH",
      "catalog_number":"570",
      "title":"Building Technology and Environmental Courses"
    },
    {
      "course_id":"014933",
      "subject":"ARCH",
      "catalog_number":"610",
      "title":"Architectural Research and Analysis"
    },
    {
      "course_id":"015047",
      "subject":"ARCH",
      "catalog_number":"629",
      "title":"Global Cities"
    },
    {
      "course_id":"014938",
      "subject":"ARCH",
      "catalog_number":"640",
      "title":"Contemporary Theory, Culture and Criticism"
    },
    {
      "course_id":"015045",
      "subject":"ARCH",
      "catalog_number":"662",
      "title":"Steel & Concrete: Design, Structure and Construction"
    },
    {
      "course_id":"015048",
      "subject":"ARCH",
      "catalog_number":"690",
      "title":"Design Studio"
    },
    {
      "course_id":"015044",
      "subject":"ARCH",
      "catalog_number":"691",
      "title":"Design Studio - Comprehensive Building Design"
    },
    {
      "course_id":"015046",
      "subject":"ARCH",
      "catalog_number":"693",
      "title":"Thesis Research & Design Studio II"
    },
    {
      "course_id":"014904",
      "subject":"AVIA",
      "catalog_number":"374",
      "title":"Special Topics in Aviation"
    },
    {
      "course_id":"015007",
      "subject":"BET",
      "catalog_number":"411",
      "title":"Capstone Entrepreneurship Planning and Execution"
    },
    {
      "course_id":"015008",
      "subject":"BET",
      "catalog_number":"412",
      "title":"Advanced Topics in Entrepreneurship"
    },
    {
      "course_id":"015009",
      "subject":"BET",
      "catalog_number":"420",
      "title":"Social Entrepreneurship and Corporate Social Responsibility"
    },
    {
      "course_id":"011508",
      "subject":"BIOL",
      "catalog_number":"266",
      "title":"Introduction to Computational Biology"
    },
    {
      "course_id":"015026",
      "subject":"BIOL",
      "catalog_number":"341",
      "title":"Fundamentals of Immunology"
    },
    {
      "course_id":"010193",
      "subject":"EASIA",
      "catalog_number":"360R",
      "title":"Premodern Chinese Literature"
    },
    {
      "course_id":"014880",
      "subject":"BIOL",
      "catalog_number":"469",
      "title":"Genomics"
    },
    {
      "course_id":"014462",
      "subject":"BME",
      "catalog_number":"252",
      "title":"Linear Signals and Systems"
    },
    {
      "course_id":"014463",
      "subject":"BME",
      "catalog_number":"353",
      "title":"Control Systems"
    },
    {
      "course_id":"014464",
      "subject":"BME",
      "catalog_number":"353L",
      "title":"Control Systems Laboratory"
    },
    {
      "course_id":"014437",
      "subject":"BME",
      "catalog_number":"355",
      "title":"Anatomical Systems Modelling"
    },
    {
      "course_id":"014459",
      "subject":"BME",
      "catalog_number":"386",
      "title":"The Physics of Medical Imaging"
    },
    {
      "course_id":"014466",
      "subject":"BME",
      "catalog_number":"392",
      "title":"Circuits, Instrumentation, and Measurements"
    },
    {
      "course_id":"014467",
      "subject":"BME",
      "catalog_number":"392L",
      "title":"Circuits, Instrumentation, and Measurements Laboratory"
    },
    {
      "course_id":"003960",
      "subject":"CHE",
      "catalog_number":"314",
      "title":"Chemical Reaction Engineering"
    },
    {
      "course_id":"003956",
      "subject":"CHE",
      "catalog_number":"361",
      "title":"Bioprocess Engineering"
    },
    {
      "course_id":"011994",
      "subject":"CHE",
      "catalog_number":"425",
      "title":"Strategies for Process Improvement and Product Development"
    },
    {
      "course_id":"015134",
      "subject":"PD",
      "catalog_number":"12",
      "title":"Reflection and Learning in the Workplace"
    },
    {
      "course_id":"014924",
      "subject":"CHEM",
      "catalog_number":"101",
      "title":"Introduction to Biochemical Sciences"
    },
    {
      "course_id":"014751",
      "subject":"CHEM",
      "catalog_number":"201",
      "title":"Environmental Impact and Management of Resources 1"
    },
    {
      "course_id":"014752",
      "subject":"CHEM",
      "catalog_number":"239",
      "title":"Introduction to Biological Systems"
    },
    {
      "course_id":"014753",
      "subject":"CHEM",
      "catalog_number":"301",
      "title":"Environmental Impact and Management of Resources 2"
    },
    {
      "course_id":"014754",
      "subject":"CHEM",
      "catalog_number":"302",
      "title":"Innovation and Project Management"
    },
    {
      "course_id":"014755",
      "subject":"CHEM",
      "catalog_number":"339",
      "title":"Methods and Tools for Biosyntheses"
    },
    {
      "course_id":"004110",
      "subject":"CHEM",
      "catalog_number":"363",
      "title":"Industrial Organic Chemistry"
    },
    {
      "course_id":"015140",
      "subject":"PACS",
      "catalog_number":"335",
      "title":"Perspectives in Music and Peace"
    },
    {
      "course_id":"014756",
      "subject":"CHEM",
      "catalog_number":"479",
      "title":"Preparation of Biobased Compounds and Materials"
    },
    {
      "course_id":"014758",
      "subject":"CHEM",
      "catalog_number":"491B",
      "title":"Biobased Chemistry Research Project 2"
    },
    {
      "course_id":"014943",
      "subject":"CIVE",
      "catalog_number":"100",
      "title":"Civil Engineering Concepts"
    },
    {
      "course_id":"014944",
      "subject":"CIVE",
      "catalog_number":"104",
      "title":"Mechanics 1"
    },
    {
      "course_id":"014945",
      "subject":"CIVE",
      "catalog_number":"105",
      "title":"Mechanics 2"
    },
    {
      "course_id":"014946",
      "subject":"CIVE",
      "catalog_number":"115",
      "title":"Linear Algebra"
    },
    {
      "course_id":"014954",
      "subject":"CIVE",
      "catalog_number":"241",
      "title":"Transport Principles and Applications"
    },
    {
      "course_id":"014960",
      "subject":"CIVE",
      "catalog_number":"310",
      "title":"Introduction to Structural Design"
    },
    {
      "course_id":"014955",
      "subject":"CIVE",
      "catalog_number":"341",
      "title":"Transportation Engineering Applications"
    },
    {
      "course_id":"014961",
      "subject":"CIVE",
      "catalog_number":"382",
      "title":"Hydrology and Open Channel Flow"
    },
    {
      "course_id":"014962",
      "subject":"CIVE",
      "catalog_number":"392",
      "title":"Economics and Life Cycle Analysis"
    },
    {
      "course_id":"007637",
      "subject":"CIVE",
      "catalog_number":"484",
      "title":"Physical Infrastructure Planning"
    },
    {
      "course_id":"004242",
      "subject":"CIVE",
      "catalog_number":"505",
      "title":"Structural Dynamics"
    },
    {
      "course_id":"011493",
      "subject":"CIVE",
      "catalog_number":"230",
      "title":"Engineering and Sustainable Development"
    },
    {
      "course_id":"014934",
      "subject":"CS",
      "catalog_number":"634",
      "title":"Security and Privacy in Health Systems"
    },
    {
      "course_id":"014935",
      "subject":"CS",
      "catalog_number":"636",
      "title":"Introduction to Computer Networks and Distributed Computer Systems"
    },
    {
      "course_id":"014936",
      "subject":"CS",
      "catalog_number":"638",
      "title":"Principles of Data Management and Use"
    },
    {
      "course_id":"013106",
      "subject":"DAC",
      "catalog_number":"203",
      "title":"Designing with Digital Sound"
    },
    {
      "course_id":"004661",
      "subject":"DRAMA",
      "catalog_number":"100",
      "title":"Introduction to Theatre"
    },
    {
      "course_id":"014896",
      "subject":"DRAMA",
      "catalog_number":"206",
      "title":"Production Participation 1"
    },
    {
      "course_id":"014918",
      "subject":"DRAMA",
      "catalog_number":"207",
      "title":"Production Participation 2"
    },
    {
      "course_id":"015145",
      "subject":"SI",
      "catalog_number":"240R",
      "title":"Migration, Diaspora, and Exile: Muslim Narratives"
    },
    {
      "course_id":"014897",
      "subject":"DRAMA",
      "catalog_number":"246",
      "title":"Design for Performance"
    },
    {
      "course_id":"014914",
      "subject":"DRAMA",
      "catalog_number":"248",
      "title":"Management for the Arts"
    },
    {
      "course_id":"011907",
      "subject":"DRAMA",
      "catalog_number":"278",
      "title":"Theatre and Technology"
    },
    {
      "course_id":"014906",
      "subject":"DRAMA",
      "catalog_number":"280",
      "title":"Theatre and Performance in Canada"
    },
    {
      "course_id":"014884",
      "subject":"DRAMA",
      "catalog_number":"282",
      "title":"Gender and Performance"
    },
    {
      "course_id":"014885",
      "subject":"DRAMA",
      "catalog_number":"284",
      "title":"Site-Specific Performance"
    },
    {
      "course_id":"014907",
      "subject":"DRAMA",
      "catalog_number":"286",
      "title":"Early English Theatre"
    },
    {
      "course_id":"014886",
      "subject":"DRAMA",
      "catalog_number":"288",
      "title":"Language, Theatre, and Performance"
    },
    {
      "course_id":"014887",
      "subject":"DRAMA",
      "catalog_number":"300",
      "title":"Theories of Theatre and Performance"
    },
    {
      "course_id":"014888",
      "subject":"DRAMA",
      "catalog_number":"316",
      "title":"Production Participation 5"
    },
    {
      "course_id":"014902",
      "subject":"DRAMA",
      "catalog_number":"368",
      "title":"Collaborative Creation"
    },
    {
      "course_id":"014890",
      "subject":"DRAMA",
      "catalog_number":"374",
      "title":"Sustainability in Performance"
    },
    {
      "course_id":"011182",
      "subject":"DRAMA",
      "catalog_number":"376",
      "title":"Political Theatre and Performance"
    },
    {
      "course_id":"014891",
      "subject":"DRAMA",
      "catalog_number":"378",
      "title":"Black Theatre and Performance"
    },
    {
      "course_id":"014892",
      "subject":"DRAMA",
      "catalog_number":"379",
      "title":"Virtual Theatre and Performance"
    },
    {
      "course_id":"014893",
      "subject":"DRAMA",
      "catalog_number":"400",
      "title":"Collaborative Performance Project"
    },
    {
      "course_id":"015161",
      "subject":"SMF",
      "catalog_number":"400",
      "title":"Capstone Seminar"
    },
    {
      "course_id":"014898",
      "subject":"DRAMA",
      "catalog_number":"410",
      "title":"Collaborative Performance Project"
    },
    {
      "course_id":"014894",
      "subject":"DRAMA",
      "catalog_number":"416",
      "title":"Production Participation 9"
    },
    {
      "course_id":"014895",
      "subject":"DRAMA",
      "catalog_number":"417",
      "title":"Production Participation 10"
    },
    {
      "course_id":"014937",
      "subject":"EARTH",
      "catalog_number":"321",
      "title":"Introduction to Geomicrobiology"
    },
    {
      "course_id":"014883",
      "subject":"EASIA",
      "catalog_number":"302R",
      "title":"Chinese Foreign Policy since 1949"
    },
    {
      "course_id":"015056",
      "subject":"EASIA",
      "catalog_number":"304R",
      "title":"Korean Law and Society"
    },
    {
      "course_id":"015057",
      "subject":"EASIA",
      "catalog_number":"362R",
      "title":"Introduction to Pre-Modern Japanese Literature"
    },
    {
      "course_id":"015058",
      "subject":"EASIA",
      "catalog_number":"363R",
      "title":"Introduction to Early Modern Japanese Literature"
    },
    {
      "course_id":"014941",
      "subject":"ECE",
      "catalog_number":"204A",
      "title":"Numerical Methods 1"
    },
    {
      "course_id":"014942",
      "subject":"ECE",
      "catalog_number":"204B",
      "title":"Numerical Methods 2"
    },
    {
      "course_id":"007967",
      "subject":"PSYCH",
      "catalog_number":"238",
      "title":"Organizational Psychology"
    },
    {
      "course_id":"014062",
      "subject":"ECON",
      "catalog_number":"100",
      "title":"Principles of Economics"
    },
    {
      "course_id":"015055",
      "subject":"CS",
      "catalog_number":"106",
      "title":"Introduction to Computer Programming 2"
    },
    {
      "course_id":"012351",
      "subject":"EMLS",
      "catalog_number":"601R",
      "title":"Speaking English for Professional Purposes"
    },
    {
      "course_id":"012153",
      "subject":"EMLS",
      "catalog_number":"602R",
      "title":"Scholarly Writing in English"
    },
    {
      "course_id":"012222",
      "subject":"EMLS",
      "catalog_number":"612R",
      "title":"Professional Writing for Engineers"
    },
    {
      "course_id":"012902",
      "subject":"ENBUS",
      "catalog_number":"112",
      "title":"Operationalizing Sustainable Development within Business"
    },
    {
      "course_id":"012901",
      "subject":"ENBUS",
      "catalog_number":"211",
      "title":"Principles of Marketing for Sustainability Professionals"
    },
    {
      "course_id":"014977",
      "subject":"ENBUS",
      "catalog_number":"406",
      "title":"Industrial Ecology: Sustainable Materials"
    },
    {
      "course_id":"014000",
      "subject":"EASIA",
      "catalog_number":"203R",
      "title":"Japanese Culture and Society"
    },
    {
      "course_id":"012900",
      "subject":"ENBUS",
      "catalog_number":"412",
      "title":"Advanced Strategic Management for Sustainable Business"
    },
    {
      "course_id":"014978",
      "subject":"ENBUS",
      "catalog_number":"414",
      "title":"Sustainability for Small and Medium Enterprises"
    },
    {
      "course_id":"015086",
      "subject":"ENGL",
      "catalog_number":"210C",
      "title":"Genres of Creative Writing"
    },
    {
      "course_id":"014911",
      "subject":"ENGL",
      "catalog_number":"210G",
      "title":"Grant Writing"
    },
    {
      "course_id":"014912",
      "subject":"ENGL",
      "catalog_number":"210J",
      "title":"Technical Editing"
    },
    {
      "course_id":"014998",
      "subject":"ENGL",
      "catalog_number":"211",
      "title":"First Nations, Metis, and Inuit Literatures"
    },
    {
      "course_id":"014997",
      "subject":"ENGL",
      "catalog_number":"275",
      "title":"Fiction and Film"
    },
    {
      "course_id":"014901",
      "subject":"ENGL",
      "catalog_number":"280",
      "title":"Literatures of Migration"
    },
    {
      "course_id":"014899",
      "subject":"ENGL",
      "catalog_number":"291",
      "title":"Global Literatures"
    },
    {
      "course_id":"014913",
      "subject":"ENGL",
      "catalog_number":"472",
      "title":"Research Methods in Technical Communication"
    },
    {
      "course_id":"014963",
      "subject":"ENVE",
      "catalog_number":"225",
      "title":"Environmental Modelling"
    },
    {
      "course_id":"014956",
      "subject":"ENVE",
      "catalog_number":"277",
      "title":"Air Quality Engineering"
    },
    {
      "course_id":"014957",
      "subject":"ENVE",
      "catalog_number":"279",
      "title":"Energy and the Environment"
    },
    {
      "course_id":"014964",
      "subject":"ENVE",
      "catalog_number":"280",
      "title":"Fluid Mechanics"
    },
    {
      "course_id":"014966",
      "subject":"ENVE",
      "catalog_number":"376",
      "title":"Biological Processes"
    },
    {
      "course_id":"014958",
      "subject":"ENVE",
      "catalog_number":"383",
      "title":"Advanced Hydrology and Hydraulics"
    },
    {
      "course_id":"015164",
      "subject":"ENGL",
      "catalog_number":"108T",
      "title":"Tolkien: From Book to Film"
    },
    {
      "course_id":"005253",
      "subject":"ENVE",
      "catalog_number":"400",
      "title":"Environmental Engineering Project 1"
    },
    {
      "course_id":"005254",
      "subject":"ENVE",
      "catalog_number":"401",
      "title":"Environmental Engineering Project 2"
    },
    {
      "course_id":"015035",
      "subject":"ENVS",
      "catalog_number":"274",
      "title":"Special Topics in Environment"
    },
    {
      "course_id":"015034",
      "subject":"ENVS",
      "catalog_number":"374",
      "title":"Special Topics in Environment"
    },
    {
      "course_id":"014975",
      "subject":"ENVS",
      "catalog_number":"400",
      "title":"First Peoples and Business Development"
    },
    {
      "course_id":"003401",
      "subject":"ANTH",
      "catalog_number":"309",
      "title":"The Archaeology of North America"
    },
    {
      "course_id":"015018",
      "subject":"ERS",
      "catalog_number":"342",
      "title":"Professional Conservation and Restoration Practice II"
    },
    {
      "course_id":"015020",
      "subject":"ERS",
      "catalog_number":"346",
      "title":"Wildlife Ecology"
    },
    {
      "course_id":"015025",
      "subject":"ERS",
      "catalog_number":"443",
      "title":"Ecosystem Field Research"
    },
    {
      "course_id":"015021",
      "subject":"ERS",
      "catalog_number":"446",
      "title":"Wildlife Management"
    },
    {
      "course_id":"015000",
      "subject":"ARCH",
      "catalog_number":"313",
      "title":"Advanced Visualization and Analysis"
    },
    {
      "course_id":"012718",
      "subject":"GER",
      "catalog_number":"301",
      "title":"Language, Culture, and Identity"
    },
    {
      "course_id":"015050",
      "subject":"GER",
      "catalog_number":"790",
      "title":"Topics in Intercultural Perspectives"
    },
    {
      "course_id":"014803",
      "subject":"GGOV",
      "catalog_number":"644",
      "title":"International Migration:  Practice, Theory & Regulation"
    },
    {
      "course_id":"014922",
      "subject":"HIST",
      "catalog_number":"212",
      "title":"The Computing Society"
    },
    {
      "course_id":"015085",
      "subject":"HIST",
      "catalog_number":"289",
      "title":"JFK: The Decision-Maker Behind the Myth"
    },
    {
      "course_id":"015098",
      "subject":"PSCI",
      "catalog_number":"420",
      "title":"Gender and Global Politics"
    },
    {
      "course_id":"015105",
      "subject":"HLTH",
      "catalog_number":"107",
      "title":"Sociology of Activity, Health, and Well-being"
    },
    {
      "course_id":"015093",
      "subject":"HLTH",
      "catalog_number":"173",
      "title":"Contemporary Issues in Health 1"
    },
    {
      "course_id":"015118",
      "subject":"HLTH",
      "catalog_number":"273",
      "title":"Contemporary Issues in Health 2"
    },
    {
      "course_id":"014312",
      "subject":"HLTH",
      "catalog_number":"301",
      "title":"Introduction to Health Promotion Techniques"
    },
    {
      "course_id":"015119",
      "subject":"HLTH",
      "catalog_number":"373",
      "title":"Contemporary Issues in Health 3"
    },
    {
      "course_id":"014673",
      "subject":"HLTH",
      "catalog_number":"401",
      "title":"Global Health"
    },
    {
      "course_id":"014318",
      "subject":"HLTH",
      "catalog_number":"441",
      "title":"Advanced Qualitative Methods"
    },
    {
      "course_id":"014319",
      "subject":"HLTH",
      "catalog_number":"481",
      "title":"Community Learning Project"
    },
    {
      "course_id":"015114",
      "subject":"REC",
      "catalog_number":"313",
      "title":"Mobilizing Resources for Recreation and Sport Delivery"
    },
    {
      "course_id":"015105",
      "subject":"KIN",
      "catalog_number":"107",
      "title":"Sociology of Activity, Health, and Well-being"
    },
    {
      "course_id":"015123",
      "subject":"RS",
      "catalog_number":"312",
      "title":"Muslim Lives and Practices Worldwide"
    },
    {
      "course_id":"011711",
      "subject":"LS",
      "catalog_number":"202",
      "title":"Criminal Law"
    },
    {
      "course_id":"007749",
      "subject":"LS",
      "catalog_number":"206",
      "title":"Canadian Government & Politics"
    },
    {
      "course_id":"008661",
      "subject":"LS",
      "catalog_number":"221",
      "title":"Research Methods"
    },
    {
      "course_id":"008602",
      "subject":"LS",
      "catalog_number":"222",
      "title":"Juvenile Delinquency"
    },
    {
      "course_id":"008603",
      "subject":"LS",
      "catalog_number":"223",
      "title":"Deviance: Perspectives and Processes"
    },
    {
      "course_id":"008584",
      "subject":"LS",
      "catalog_number":"224",
      "title":"Victims and Society"
    },
    {
      "course_id":"008631",
      "subject":"LS",
      "catalog_number":"226",
      "title":"Sociology of Mental Disorder"
    },
    {
      "course_id":"008609",
      "subject":"LS",
      "catalog_number":"227",
      "title":"Criminology"
    },
    {
      "course_id":"008610",
      "subject":"LS",
      "catalog_number":"228",
      "title":"Sociology of Criminal Justice"
    },
    {
      "course_id":"010101",
      "subject":"LS",
      "catalog_number":"229",
      "title":"Selected Topics in Criminology"
    },
    {
      "course_id":"006241",
      "subject":"LS",
      "catalog_number":"235",
      "title":"History of Ancient Law"
    },
    {
      "course_id":"006194",
      "subject":"LS",
      "catalog_number":"236",
      "title":"Law and Society in the Middle Ages"
    },
    {
      "course_id":"011574",
      "subject":"LS",
      "catalog_number":"237",
      "title":"Canadian Legal History"
    },
    {
      "course_id":"015068",
      "subject":"LS",
      "catalog_number":"249",
      "title":"Mental Disorder and the Law"
    },
    {
      "course_id":"015069",
      "subject":"LS",
      "catalog_number":"263",
      "title":"Organized Crime"
    },
    {
      "course_id":"007192",
      "subject":"LS",
      "catalog_number":"271",
      "title":"Conflict Resolution"
    },
    {
      "course_id":"010100",
      "subject":"LS",
      "catalog_number":"272",
      "title":"Psychology and Law"
    },
    {
      "course_id":"014137",
      "subject":"LS",
      "catalog_number":"273",
      "title":"Children's Rights in Canada"
    },
    {
      "course_id":"003247",
      "subject":"LS",
      "catalog_number":"283",
      "title":"Business Law"
    },
    {
      "course_id":"015067",
      "subject":"LS",
      "catalog_number":"286",
      "title":"Law in Popular Culture"
    },
    {
      "course_id":"010336",
      "subject":"LS",
      "catalog_number":"291",
      "title":"Legal Writing"
    },
    {
      "course_id":"011771",
      "subject":"LS",
      "catalog_number":"292",
      "title":"Literature and the Law"
    },
    {
      "course_id":"008694",
      "subject":"LS",
      "catalog_number":"300",
      "title":"Sociology of Law"
    },
    {
      "course_id":"008608",
      "subject":"LS",
      "catalog_number":"306",
      "title":"Juvenile Justice"
    },
    {
      "course_id":"007201",
      "subject":"LS",
      "catalog_number":"319",
      "title":"Negotiation: Theories and Strategies"
    },
    {
      "course_id":"008667",
      "subject":"LS",
      "catalog_number":"325",
      "title":"Sexuality and the Law"
    },
    {
      "course_id":"014130",
      "subject":"LS",
      "catalog_number":"326",
      "title":"Punishment and Society"
    },
    {
      "course_id":"009873",
      "subject":"LS",
      "catalog_number":"327",
      "title":"Policing in a Democratic Society"
    },
    {
      "course_id":"006346",
      "subject":"LS",
      "catalog_number":"331",
      "title":"Human Rights in Historical Perspective"
    },
    {
      "course_id":"013487",
      "subject":"LS",
      "catalog_number":"344",
      "title":"Restorative Justice"
    },
    {
      "course_id":"007311",
      "subject":"LS",
      "catalog_number":"351",
      "title":"Philosophy of Law"
    },
    {
      "course_id":"011185",
      "subject":"LS",
      "catalog_number":"352",
      "title":"Human Rights"
    },
    {
      "course_id":"007797",
      "subject":"LS",
      "catalog_number":"363",
      "title":"Canadian Constitutional Law"
    },
    {
      "course_id":"014268",
      "subject":"LS",
      "catalog_number":"365",
      "title":"Transnational Migration"
    },
    {
      "course_id":"012593",
      "subject":"LS",
      "catalog_number":"366",
      "title":"Global Governance"
    },
    {
      "course_id":"010042",
      "subject":"LS",
      "catalog_number":"372",
      "title":"Criminal Profiling"
    },
    {
      "course_id":"011378",
      "subject":"LS",
      "catalog_number":"373",
      "title":"Public Policy and Native Peoples in Canada"
    },
    {
      "course_id":"011390",
      "subject":"LS",
      "catalog_number":"374",
      "title":"The Evolution of Family Law in Canadian Society"
    },
    {
      "course_id":"015066",
      "subject":"LS",
      "catalog_number":"386",
      "title":"Law and Violence"
    },
    {
      "course_id":"015148",
      "subject":"MEDVL",
      "catalog_number":"251R",
      "title":"The History of Islamic Civilization from 1300-1800: The Islamic Gunpowder Empires"
    },
    {
      "course_id":"015013",
      "subject":"LS",
      "catalog_number":"413",
      "title":"Surveillance and Society"
    },
    {
      "course_id":"010152",
      "subject":"LS",
      "catalog_number":"428",
      "title":"Sentencing as a Social Process"
    },
    {
      "course_id":"014842",
      "subject":"LS",
      "catalog_number":"434",
      "title":"Sociology of At-Risk Youth"
    },
    {
      "course_id":"015070",
      "subject":"LS",
      "catalog_number":"461",
      "title":"Transnational Organized Crime"
    },
    {
      "course_id":"013476",
      "subject":"LS",
      "catalog_number":"462",
      "title":"Government and Politics of Indigenous Peoples"
    },
    {
      "course_id":"014530",
      "subject":"LS",
      "catalog_number":"463",
      "title":"Rights and Public Policy"
    },
    {
      "course_id":"007813",
      "subject":"LS",
      "catalog_number":"464",
      "title":"Justice and Gender"
    },
    {
      "course_id":"013570",
      "subject":"LS",
      "catalog_number":"492",
      "title":"Communication and Social Justice"
    },
    {
      "course_id":"013990",
      "subject":"MNS",
      "catalog_number":"410",
      "title":"Special Topics in Solid-State Materials"
    },
    {
      "course_id":"013989",
      "subject":"MNS",
      "catalog_number":"431",
      "title":"Special Topics in Nano-Biomaterials"
    },
    {
      "course_id":"014969",
      "subject":"MTHEL",
      "catalog_number":"300",
      "title":"Professional Communications in Statistics and Actuarial Science"
    },
    {
      "course_id":"003945",
      "subject":"NATST",
      "catalog_number":"272",
      "title":"Issues in Contemporary Native Communities in Canada"
    },
    {
      "course_id":"014982",
      "subject":"NE",
      "catalog_number":"109",
      "title":"Societal and Environmental Impacts of Nanotechnology"
    },
    {
      "course_id":"011926",
      "subject":"NE",
      "catalog_number":"215",
      "title":"Probability and Statistics"
    },
    {
      "course_id":"014993",
      "subject":"OPTOM",
      "catalog_number":"682",
      "title":"Visual Motor Neuroscience"
    },
    {
      "course_id":"014996",
      "subject":"OPTOM",
      "catalog_number":"683",
      "title":"Visual Sensory Neuroscience"
    },
    {
      "course_id":"014869",
      "subject":"PACS",
      "catalog_number":"332",
      "title":"Ethics of Peacebuilding"
    },
    {
      "course_id":"014870",
      "subject":"PACS",
      "catalog_number":"333",
      "title":"Advanced Mediation Practice"
    },
    {
      "course_id":"014953",
      "subject":"PHARM",
      "catalog_number":"614",
      "title":"Systematic Review and Meta-Analysis"
    },
    {
      "course_id":"014959",
      "subject":"PHARM",
      "catalog_number":"615",
      "title":"Strategic Management of Biopharmaceutical Technology"
    },
    {
      "course_id":"015241",
      "subject":"PHARM",
      "catalog_number":"616",
      "title":"PhD Thesis Proposal"
    },
    {
      "course_id":"015054",
      "subject":"CS",
      "catalog_number":"105",
      "title":"Introduction to Computer Programming 1"
    },
    {
      "course_id":"015072",
      "subject":"PHS",
      "catalog_number":"651",
      "title":"Theory and Applications in Program Evaluation"
    },
    {
      "course_id":"015073",
      "subject":"PHS",
      "catalog_number":"652",
      "title":"Qualitative and Mixed Methods and Analysis"
    },
    {
      "course_id":"015074",
      "subject":"PHS",
      "catalog_number":"653",
      "title":"Evaluation Practice and Management"
    },
    {
      "course_id":"015075",
      "subject":"PHS",
      "catalog_number":"654",
      "title":"Systems Thinking and Analysis"
    },
    {
      "course_id":"015076",
      "subject":"PHS",
      "catalog_number":"655",
      "title":"Survey Methods"
    },
    {
      "course_id":"013964",
      "subject":"PHYS",
      "catalog_number":"474",
      "title":"Galaxies"
    },
    {
      "course_id":"013971",
      "subject":"PHYS",
      "catalog_number":"483",
      "title":"Advanced Therapeutic Concepts in Oncology and Medical Physics"
    },
    {
      "course_id":"013972",
      "subject":"PHYS",
      "catalog_number":"491",
      "title":"Special Topics in Life, Medical and Biophysics"
    },
    {
      "course_id":"015036",
      "subject":"PLAN",
      "catalog_number":"705",
      "title":"Design in Planning"
    },
    {
      "course_id":"014769",
      "subject":"PMATH",
      "catalog_number":"930",
      "title":"Topics in Logic"
    },
    {
      "course_id":"014770",
      "subject":"PMATH",
      "catalog_number":"940",
      "title":"Topics in Number Theory"
    },
    {
      "course_id":"014771",
      "subject":"PMATH",
      "catalog_number":"945",
      "title":"Topics in Algebra"
    },
    {
      "course_id":"014772",
      "subject":"PMATH",
      "catalog_number":"950",
      "title":"Topics in Analysis"
    },
    {
      "course_id":"014773",
      "subject":"PMATH",
      "catalog_number":"965",
      "title":"Topics in Gemetry and Topology"
    },
    {
      "course_id":"014774",
      "subject":"PMATH",
      "catalog_number":"990",
      "title":"Topics in Pure Mathematics"
    },
    {
      "course_id":"015027",
      "subject":"PSCI",
      "catalog_number":"359",
      "title":"Politics of South Asia"
    },
    {
      "course_id":"015231",
      "subject":"PSCI",
      "catalog_number":"370W",
      "title":"The Political Economy of Eastern Asia (WLU)"
    },
    {
      "course_id":"012154",
      "subject":"EASIA",
      "catalog_number":"391R",
      "title":"Special Topics"
    },
    {
      "course_id":"015028",
      "subject":"PSCI",
      "catalog_number":"450",
      "title":"Politics of Authoritarianism"
    },
    {
      "course_id":"015059",
      "subject":"PSYCH",
      "catalog_number":"444R",
      "title":"Psychological Interventions"
    },
    {
      "course_id":"015015",
      "subject":"PSYCH",
      "catalog_number":"451",
      "title":"Honours Seminar - Child and Adolescent Psychopathology"
    },
    {
      "course_id":"015062",
      "subject":"PSYCH",
      "catalog_number":"459",
      "title":"Honours Seminar - Close Relationships"
    },
    {
      "course_id":"015051",
      "subject":"PSYCH",
      "catalog_number":"823",
      "title":"Research Apprenticeship I"
    },
    {
      "course_id":"015052",
      "subject":"PSYCH",
      "catalog_number":"824",
      "title":"Research Apprenticeship II"
    },
    {
      "course_id":"015060",
      "subject":"PSYCH",
      "catalog_number":"875",
      "title":"Organizational Psychology"
    },
    {
      "course_id":"015061",
      "subject":"PSYCH",
      "catalog_number":"876",
      "title":"The Psychology of Justice in the Workplace"
    },
    {
      "course_id":"015105",
      "subject":"REC",
      "catalog_number":"107",
      "title":"Sociology of Activity, Health, and Well-being"
    },
    {
      "course_id":"015109",
      "subject":"REC",
      "catalog_number":"172",
      "title":"Special Topics in Leisure Studies 1"
    },
    {
      "course_id":"015113",
      "subject":"REC",
      "catalog_number":"272",
      "title":"Special Topics in Leisure Studies 2"
    },
    {
      "course_id":"015116",
      "subject":"REC",
      "catalog_number":"373",
      "title":"Qualitative Approaches to Leisure Research"
    },
    {
      "course_id":"015100",
      "subject":"SPCOM",
      "catalog_number":"335",
      "title":"Power, Agency, Community"
    },
    {
      "course_id":"015016",
      "subject":"RS",
      "catalog_number":"115R",
      "title":"Sex, Politics, and Religion in the U.S. and Canada"
    },
    {
      "course_id":"015077",
      "subject":"SPAN",
      "catalog_number":"395",
      "title":"Cultural Dimensions in English\/Spanish Literary Translation"
    },
    {
      "course_id":"013000",
      "subject":"RS",
      "catalog_number":"227",
      "title":"Buddhism in North America"
    },
    {
      "course_id":"014923",
      "subject":"SCI",
      "catalog_number":"207",
      "title":"Physics, the Universe, and Everything"
    },
    {
      "course_id":"015014",
      "subject":"SI",
      "catalog_number":"320R",
      "title":"Introduction to Modern Arab and Muslim Drama"
    },
    {
      "course_id":"008581",
      "subject":"SOC",
      "catalog_number":"205",
      "title":"Social Problems"
    },
    {
      "course_id":"008661",
      "subject":"SOC",
      "catalog_number":"221",
      "title":"Research Methods"
    },
    {
      "course_id":"015011",
      "subject":"SOC",
      "catalog_number":"225",
      "title":"Games and Gamers"
    },
    {
      "course_id":"008608",
      "subject":"SOC",
      "catalog_number":"306",
      "title":"Juvenile Justice"
    },
    {
      "course_id":"014851",
      "subject":"SOC",
      "catalog_number":"320",
      "title":"Social Problems in a Global Context"
    },
    {
      "course_id":"015012",
      "subject":"SOC",
      "catalog_number":"324",
      "title":"Digital Cultures"
    },
    {
      "course_id":"015013",
      "subject":"SOC",
      "catalog_number":"413",
      "title":"Surveillance and Society"
    },
    {
      "course_id":"015070",
      "subject":"SOC",
      "catalog_number":"461",
      "title":"Transnational Organized Crime"
    },
    {
      "course_id":"014953",
      "subject":"STAT",
      "catalog_number":"814",
      "title":"Systematic Review and Meta-Analysis"
    },
    {
      "course_id":"014922",
      "subject":"STV",
      "catalog_number":"210",
      "title":"The Computing Society"
    },
    {
      "course_id":"015102",
      "subject":"WKRPT",
      "catalog_number":"200M",
      "title":"Work-term Report"
    },
    {
      "course_id":"015103",
      "subject":"WKRPT",
      "catalog_number":"300M",
      "title":"Work-term Report"
    },
    {
      "course_id":"015104",
      "subject":"WKRPT",
      "catalog_number":"400M",
      "title":"Work-term Report"
    },
    {
      "course_id":"014644",
      "subject":"PHARM",
      "catalog_number":"351",
      "title":"Management Issues in Community Pharmacy Practice"
    },
    {
      "course_id":"014434",
      "subject":"BME",
      "catalog_number":"285L",
      "title":"Engineering Biology Laboratory"
    },
    {
      "course_id":"015147",
      "subject":"MEDVL",
      "catalog_number":"250R",
      "title":"The History of Islamic Civilization from Late Antiquity to 1300"
    },
    {
      "course_id":"015146",
      "subject":"SI",
      "catalog_number":"241R",
      "title":"Sacred Spaces and Human Geographies: Literary Expressions"
    },
    {
      "course_id":"015097",
      "subject":"ANTH",
      "catalog_number":"415",
      "title":"Archaeologies of Landscape"
    },
    {
      "course_id":"015143",
      "subject":"CS",
      "catalog_number":"383",
      "title":"Computational Digital Art Studio"
    },
    {
      "course_id":"015127",
      "subject":"JAPAN",
      "catalog_number":"391R",
      "title":"Special Topics"
    },
    {
      "course_id":"015128",
      "subject":"KOREA",
      "catalog_number":"391R",
      "title":"Special Topics"
    },
    {
      "course_id":"015204",
      "subject":"MNS",
      "catalog_number":"10",
      "title":"Materials and Nanosciences Seminar"
    },
    {
      "course_id":"012510",
      "subject":"PHARM",
      "catalog_number":"324",
      "title":"Integrated Patient Focused Care 8"
    },
    {
      "course_id":"015133",
      "subject":"PD",
      "catalog_number":"11",
      "title":"Processes for Technical Report Writing"
    },
    {
      "course_id":"012493",
      "subject":"PHARM",
      "catalog_number":"330",
      "title":"Professional Practice 6"
    },
    {
      "course_id":"014432",
      "subject":"BME",
      "catalog_number":"186",
      "title":"Chemistry Principles"
    },
    {
      "course_id":"013126",
      "subject":"PHARM",
      "catalog_number":"323",
      "title":"Integrated Patient Focused Care 7"
    },
    {
      "course_id":"015147",
      "subject":"SI",
      "catalog_number":"250R",
      "title":"The History of Islamic Civilization from Late Antiquity to 1300"
    },
    {
      "course_id":"015148",
      "subject":"SI",
      "catalog_number":"251R",
      "title":"The History of Islamic Civilization from 1300-1800: The Islamic Gunpowder Empires"
    },
    {
      "course_id":"015209",
      "subject":"NE",
      "catalog_number":"250",
      "title":"Work-term Report 1"
    },
    {
      "course_id":"014645",
      "subject":"PHARM",
      "catalog_number":"352",
      "title":"Management Issues in Pharmacy Practice in Organizations"
    },
    {
      "course_id":"014646",
      "subject":"PHARM",
      "catalog_number":"353",
      "title":"Entrepreneurship in Pharmacy"
    },
    {
      "course_id":"014789",
      "subject":"EASIA",
      "catalog_number":"361R",
      "title":"Modern Chinese Literature (1917 - present day)"
    },
    {
      "course_id":"015179",
      "subject":"ECON",
      "catalog_number":"206",
      "title":"Money and Banking 1"
    },
    {
      "course_id":"015180",
      "subject":"ECON",
      "catalog_number":"207",
      "title":"Economic Growth and Development 1"
    },
    {
      "course_id":"015181",
      "subject":"ECON",
      "catalog_number":"212",
      "title":"Introduction to Game Theory"
    },
    {
      "course_id":"015182",
      "subject":"ECON",
      "catalog_number":"255",
      "title":"Introduction to the Economics of Natural Resources"
    },
    {
      "course_id":"015183",
      "subject":"ECON",
      "catalog_number":"256",
      "title":"Introduction to Health Economics"
    },
    {
      "course_id":"015088",
      "subject":"ECON",
      "catalog_number":"261",
      "title":"Philosophy of Economics"
    },
    {
      "course_id":"015186",
      "subject":"ECON",
      "catalog_number":"262",
      "title":"History of Economic Thought"
    },
    {
      "course_id":"015187",
      "subject":"ECON",
      "catalog_number":"290",
      "title":"Models of Choice in Competitive Markets"
    },
    {
      "course_id":"015188",
      "subject":"ECON",
      "catalog_number":"306",
      "title":"Macroeconomics"
    },
    {
      "course_id":"015189",
      "subject":"ECON",
      "catalog_number":"322",
      "title":"Econometric Analysis 1"
    },
    {
      "course_id":"015190",
      "subject":"ECON",
      "catalog_number":"323",
      "title":"Econometric Analysis 2"
    },
    {
      "course_id":"015192",
      "subject":"ECON",
      "catalog_number":"366",
      "title":"Gender and Economics"
    },
    {
      "course_id":"015193",
      "subject":"ECON",
      "catalog_number":"391",
      "title":"Equilibrium in Market Economies"
    },
    {
      "course_id":"015194",
      "subject":"ECON",
      "catalog_number":"392",
      "title":"Strategic Situations and Welfare Economics"
    },
    {
      "course_id":"015195",
      "subject":"ECON",
      "catalog_number":"393",
      "title":"Market Failures"
    },
    {
      "course_id":"015196",
      "subject":"ECON",
      "catalog_number":"406",
      "title":"Money and Banking 2"
    },
    {
      "course_id":"015197",
      "subject":"ECON",
      "catalog_number":"407",
      "title":"Economic Growth and Development 2"
    },
    {
      "course_id":"015198",
      "subject":"ECON",
      "catalog_number":"408",
      "title":"Business Cycles"
    },
    {
      "course_id":"015199",
      "subject":"ECON",
      "catalog_number":"409",
      "title":"Workers, Jobs, and Wages"
    },
    {
      "course_id":"015200",
      "subject":"ECON",
      "catalog_number":"423",
      "title":"Time Series Econometrics"
    },
    {
      "course_id":"015201",
      "subject":"ECON",
      "catalog_number":"474",
      "title":"Numerical Methods for Economists"
    },
    {
      "course_id":"015202",
      "subject":"ECON",
      "catalog_number":"491",
      "title":"Advanced Microeconomics"
    },
    {
      "course_id":"015203",
      "subject":"ECON",
      "catalog_number":"496",
      "title":"Advanced Macroeconomics"
    },
    {
      "course_id":"005500",
      "subject":"FINE",
      "catalog_number":"217",
      "title":"Art of the 18th Century in Europe"
    },
    {
      "course_id":"015176",
      "subject":"FINE",
      "catalog_number":"259",
      "title":"Aspects of European Cinema"
    },
    {
      "course_id":"015151",
      "subject":"FINE",
      "catalog_number":"307",
      "title":"Advanced Topics in Studio"
    },
    {
      "course_id":"015152",
      "subject":"FINE",
      "catalog_number":"308",
      "title":"Honours Studio\/Seminar"
    },
    {
      "course_id":"015153",
      "subject":"FINE",
      "catalog_number":"403",
      "title":"Honours Concept and Research"
    },
    {
      "course_id":"005579",
      "subject":"FR",
      "catalog_number":"250",
      "title":"Intermediate Spoken French"
    },
    {
      "course_id":"011615",
      "subject":"FR",
      "catalog_number":"296",
      "title":"French Culture & Literature: Origins to 1715"
    },
    {
      "course_id":"015172",
      "subject":"GENE",
      "catalog_number":"23E",
      "title":"Topics for Natural Science Elective Courses Taken on Exchange by Electrical Engineering Students"
    },
    {
      "course_id":"015171",
      "subject":"GENE",
      "catalog_number":"23K",
      "title":"Topics for Natural Science Elective Courses Taken on Exchange by Civil Engineering Students"
    },
    {
      "course_id":"015173",
      "subject":"GENE",
      "catalog_number":"23Q",
      "title":"Topics for Natural Science Elective Courses Taken on Exchange by Computer Engineering Students"
    },
    {
      "course_id":"015174",
      "subject":"GENE",
      "catalog_number":"23S",
      "title":"Topics for Natural Science Elective Courses Taken on Exchange by Software Engineering Students"
    },
    {
      "course_id":"015033",
      "subject":"GEOG",
      "catalog_number":"325",
      "title":"Geographies of Health"
    },
    {
      "course_id":"015149",
      "subject":"GER",
      "catalog_number":"200",
      "title":"Transcultural Studies"
    },
    {
      "course_id":"006426",
      "subject":"GERON",
      "catalog_number":"310",
      "title":"Development, Aging and Health"
    },
    {
      "course_id":"006429",
      "subject":"GERON",
      "catalog_number":"320",
      "title":"Psychosocial Perspectives on Lifespan Development and Health"
    },
    {
      "course_id":"015130",
      "subject":"HIST",
      "catalog_number":"421",
      "title":"Special Topics in History"
    },
    {
      "course_id":"015131",
      "subject":"HIST",
      "catalog_number":"422",
      "title":"Special Topics in History"
    },
    {
      "course_id":"015132",
      "subject":"HIST",
      "catalog_number":"450",
      "title":"The History Capstone"
    },
    {
      "course_id":"015117",
      "subject":"HLTH",
      "catalog_number":"204",
      "title":"Quantitative Approaches to Health Science"
    },
    {
      "course_id":"011462",
      "subject":"HLTH",
      "catalog_number":"230",
      "title":"Introduction to Health Informatics"
    },
    {
      "course_id":"015255",
      "subject":"HLTH",
      "catalog_number":"280",
      "title":"Applied Public Health Ethics"
    },
    {
      "course_id":"015256",
      "subject":"HLTH",
      "catalog_number":"304",
      "title":"Health Communication"
    },
    {
      "course_id":"006429",
      "subject":"HLTH",
      "catalog_number":"320",
      "title":"Psychosocial Perspectives on Lifespan Development and Health"
    },
    {
      "course_id":"015258",
      "subject":"HLTH",
      "catalog_number":"370",
      "title":"Ecological Determinants of Health"
    },
    {
      "course_id":"015259",
      "subject":"HLTH",
      "catalog_number":"412",
      "title":"Comparative Health Systems"
    },
    {
      "course_id":"012699",
      "subject":"INTEG",
      "catalog_number":"420A",
      "title":"Senior Research Project A"
    },
    {
      "course_id":"012700",
      "subject":"INTEG",
      "catalog_number":"420B",
      "title":"Senior Research Project B"
    },
    {
      "course_id":"006426",
      "subject":"KIN",
      "catalog_number":"310",
      "title":"Development, Aging and Health"
    },
    {
      "course_id":"015108",
      "subject":"KIN",
      "catalog_number":"332",
      "title":"Research Design and Statistics in Kinesiology"
    },
    {
      "course_id":"015094",
      "subject":"MSCI",
      "catalog_number":"391",
      "title":"Work-term Report"
    },
    {
      "course_id":"015095",
      "subject":"MSCI",
      "catalog_number":"392",
      "title":"Work-term Report"
    },
    {
      "course_id":"015096",
      "subject":"MSCI",
      "catalog_number":"491",
      "title":"Work-term Report"
    },
    {
      "course_id":"004767",
      "subject":"MTE",
      "catalog_number":"309",
      "title":"Introduction to Thermodynamics and Heat Transfer"
    },
    {
      "course_id":"015135",
      "subject":"MUSIC",
      "catalog_number":"110",
      "title":"Music in Cultural Contexts"
    },
    {
      "course_id":"015136",
      "subject":"MUSIC",
      "catalog_number":"232",
      "title":"Music as a Global Phenomenon"
    },
    {
      "course_id":"015137",
      "subject":"MUSIC",
      "catalog_number":"233",
      "title":"Musical Rhythm in Global Perspective"
    },
    {
      "course_id":"015138",
      "subject":"MUSIC",
      "catalog_number":"262",
      "title":"Music for Vocal Ensemble"
    },
    {
      "course_id":"015139",
      "subject":"MUSIC",
      "catalog_number":"333",
      "title":"Music and Landscape"
    },
    {
      "course_id":"015140",
      "subject":"MUSIC",
      "catalog_number":"335",
      "title":"Perspectives in Music and Peace"
    },
    {
      "course_id":"015141",
      "subject":"MUSIC",
      "catalog_number":"392",
      "title":"Special Topics in Global Music"
    },
    {
      "course_id":"011944",
      "subject":"NE",
      "catalog_number":"345",
      "title":"Photonic Materials and Devices"
    },
    {
      "course_id":"015210",
      "subject":"NE",
      "catalog_number":"350",
      "title":"Work-term Report 2"
    },
    {
      "course_id":"015220",
      "subject":"NE",
      "catalog_number":"381",
      "title":"Introduction to Nanoscale Biosystems"
    },
    {
      "course_id":"015211",
      "subject":"NE",
      "catalog_number":"450",
      "title":"Work-term Report 3"
    },
    {
      "course_id":"015212",
      "subject":"NE",
      "catalog_number":"454A",
      "title":"Nano-instrumentation Laboratory 1"
    },
    {
      "course_id":"015213",
      "subject":"NE",
      "catalog_number":"454B",
      "title":"Nano-electronics Laboratory 1"
    },
    {
      "course_id":"015214",
      "subject":"NE",
      "catalog_number":"454C",
      "title":"Nanobiosystems Laboratory 1"
    },
    {
      "course_id":"015215",
      "subject":"NE",
      "catalog_number":"454D",
      "title":"Nanostructured Materials Laboratory 1"
    },
    {
      "course_id":"015216",
      "subject":"NE",
      "catalog_number":"455A",
      "title":"Nano-instrumentation Laboratory 2"
    },
    {
      "course_id":"015217",
      "subject":"NE",
      "catalog_number":"455B",
      "title":"Nano-electronics Laboratory 2"
    },
    {
      "course_id":"015218",
      "subject":"NE",
      "catalog_number":"455C",
      "title":"Nanobiosystems Laboratory 2"
    },
    {
      "course_id":"015219",
      "subject":"NE",
      "catalog_number":"455D",
      "title":"Nanostructured Materials Laboratory 2"
    },
    {
      "course_id":"015088",
      "subject":"PHIL",
      "catalog_number":"205",
      "title":"Philosophy of Economics"
    },
    {
      "course_id":"015089",
      "subject":"PHIL",
      "catalog_number":"206",
      "title":"Philosophy of Sport"
    },
    {
      "course_id":"015087",
      "subject":"PHIL",
      "catalog_number":"251",
      "title":"Metaphysics and Epistemology"
    },
    {
      "course_id":"007248",
      "subject":"PHIL",
      "catalog_number":"283",
      "title":"Great Works: Ancient and Medieval"
    },
    {
      "course_id":"007249",
      "subject":"PHIL",
      "catalog_number":"284",
      "title":"Great Works: Modern"
    },
    {
      "course_id":"014722",
      "subject":"PHIL",
      "catalog_number":"356",
      "title":"Intelligence in Machines, Humans, and Other Animals"
    },
    {
      "course_id":"015092",
      "subject":"PMATH",
      "catalog_number":"333",
      "title":"Introduction to Real Analysis"
    },
    {
      "course_id":"015166",
      "subject":"PSYCH",
      "catalog_number":"389",
      "title":"Social Science Advanced Research Methods Topics"
    },
    {
      "course_id":"015167",
      "subject":"PSYCH",
      "catalog_number":"390",
      "title":"Natural Science Advanced Research Methods Topics"
    },
    {
      "course_id":"008097",
      "subject":"PSYCH",
      "catalog_number":"466",
      "title":"Emergent Literacy"
    },
    {
      "course_id":"015168",
      "subject":"PSYCH",
      "catalog_number":"470",
      "title":"Special Topics in Applied Psychology"
    },
    {
      "course_id":"015254",
      "subject":"REC",
      "catalog_number":"105",
      "title":"Interdisciplinary Approaches to Leisure"
    },
    {
      "course_id":"008118",
      "subject":"REC",
      "catalog_number":"120",
      "title":"Program Management and Evaluation"
    },
    {
      "course_id":"015110",
      "subject":"REC",
      "catalog_number":"201",
      "title":"Diversity and Leisure"
    },
    {
      "course_id":"015111",
      "subject":"REC",
      "catalog_number":"213",
      "title":"Principles of High Performance Organizations in Recreation and Sport"
    },
    {
      "course_id":"015112",
      "subject":"REC",
      "catalog_number":"218",
      "title":"Social Entrepreneurship for Change"
    },
    {
      "course_id":"014380",
      "subject":"SDS",
      "catalog_number":"449R",
      "title":"Race and Gender Equality"
    },
    {
      "course_id":"008556",
      "subject":"SMF",
      "catalog_number":"101",
      "title":"Introduction to Relationships and Families"
    },
    {
      "course_id":"015154",
      "subject":"SMF",
      "catalog_number":"200",
      "title":"Special Topics in Sexualities, Relationships, or Families"
    },
    {
      "course_id":"015155",
      "subject":"SMF",
      "catalog_number":"211",
      "title":"Dynamics of Dating"
    },
    {
      "course_id":"015156",
      "subject":"SMF",
      "catalog_number":"212",
      "title":"Navigating Sexuality and Relationships in Mid\/Later Life"
    },
    {
      "course_id":"015157",
      "subject":"SMF",
      "catalog_number":"213",
      "title":"Sexual Health and Well-Being"
    },
    {
      "course_id":"015158",
      "subject":"SMF",
      "catalog_number":"214",
      "title":"Constructing Erotics"
    },
    {
      "course_id":"015159",
      "subject":"SMF",
      "catalog_number":"215",
      "title":"Sexuality and Popular Culture"
    },
    {
      "course_id":"015160",
      "subject":"SMF",
      "catalog_number":"216",
      "title":"Sexual Pleasure"
    },
    {
      "course_id":"015208",
      "subject":"SMF",
      "catalog_number":"491",
      "title":"Practicum and Applied Theory"
    },
    {
      "course_id":"015162",
      "subject":"SMF",
      "catalog_number":"499A",
      "title":"Thesis - Part 1"
    },
    {
      "course_id":"015163",
      "subject":"SMF",
      "catalog_number":"499B",
      "title":"Thesis - Part 2"
    },
    {
      "course_id":"015099",
      "subject":"SPCOM",
      "catalog_number":"339",
      "title":"Media, Images, and Communication"
    },
    {
      "course_id":"015177",
      "subject":"VCULT",
      "catalog_number":"400",
      "title":"Visual Culture Seminar"
    },
    {
      "course_id":"015178",
      "subject":"VCULT",
      "catalog_number":"401",
      "title":"Advanced Visual Culture Seminar"
    }
  ]
}
```

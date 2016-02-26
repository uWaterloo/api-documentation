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
```
...
```json
  ]
}
```

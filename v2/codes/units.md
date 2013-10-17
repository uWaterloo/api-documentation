# Code Lookups for Organizational Units

```
GET /codes/units.{format}
```

## Description

> This method returns a list of all code lookups and their respective descriptions for organizations.

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
    <td>1231</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>codes</td>
    <td><b>Service ID</b></td>
    <td>263</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Institution of Analysis & Planning (IAP)</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by steward/via pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- This data is community curated on github
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/Quest/AcademicOrganizations.csv


## Parameters

```
GET /codes/units.{format}
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
GET /codes/units.{format}
```

- **https://api.uwaterloo.ca/v2/codes/units.json**
- **https://api.uwaterloo.ca/v2/codes/units.xml**
- **https://api.uwaterloo.ca/v2/codes/units.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>unit_code</b></td>
    <td>string</td>
    <td>Organizational Unit code</td>
  </tr>
  <tr>
    <td><b>group_code</b></td>
    <td>string</td>
    <td>Unit's parent group</td>
  </tr>
  <tr>
    <td><b>unit_short_name</b></td>
    <td>string</td>
    <td>Organizational Units short name</td>
  </tr>
  <tr>
    <td><b>unit_full_name</b></td>
    <td>string</td>
    <td>Units full name</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":146,
    "timestamp":1382023839,
    "status":200,
    "message":"Request successful",
    "method_id":1231,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "unit_code":"ACC",
      "group_code":"ART",
      "unit_short_name":"Accounting&Finance - School of",
      "unit_full_name":"Accounting & Finance - School of"
    },
    {
      "unit_code":"AHS",
      "group_code":"AHS",
      "unit_short_name":"Applied Health Sciences",
      "unit_full_name":"Applied Health Sciences"
    },
    {
      "unit_code":"AHSDEAN",
      "group_code":"AHS",
      "unit_short_name":"Dean of Applied Hlth Sciences",
      "unit_full_name":"Dean of Applied Health Sciences"
    },
    {
      "unit_code":"AMATH",
      "group_code":"MAT",
      "unit_short_name":"Applied Mathematics",
      "unit_full_name":"Applied Mathematics"
    },
    {
      "unit_code":"ANTH",
      "group_code":"ART",
      "unit_short_name":"Anthropology",
      "unit_full_name":"Anthropology"
    },
    {
      "unit_code":"ARCH",
      "group_code":"ENG",
      "unit_short_name":"Architecture - School of",
      "unit_full_name":"Architecture - School of"
    },
    {
      "unit_code":"ART",
      "group_code":"ART",
      "unit_short_name":"Arts",
      "unit_full_name":"Arts"
    },
    {
      "unit_code":"ARTSDEAN",
      "group_code":"ART",
      "unit_short_name":"Dean of Arts",
      "unit_full_name":"Dean of Arts"
    },
    {
      "unit_code":"BIOL",
      "group_code":"SCI",
      "unit_short_name":"Biology",
      "unit_full_name":"Biology"
    },
    {
      "unit_code":"CBET",
      "group_code":"ENG",
      "unit_short_name":"Conrad Bus, Entrepren & Tech",
      "unit_full_name":"Conrad Business, Entrepreneurship & Technology Ctr"
    },
    {
      "unit_code":"CECS",
      "group_code":"NULL",
      "unit_short_name":"Coop Educn & Career Action",
      "unit_full_name":"Co-operative Education & Career Action"
    },
    {
      "unit_code":"CGC",
      "group_code":"CGC",
      "unit_short_name":"Conrad Grebel College",
      "unit_full_name":"Conrad Grebel College"
    },
    {
      "unit_code":"CHE",
      "group_code":"ENG",
      "unit_short_name":"Chemical Engineering",
      "unit_full_name":"Chemical Engineering"
    },
    {
      "unit_code":"CHEM",
      "group_code":"SCI",
      "unit_short_name":"Chemistry",
      "unit_full_name":"Chemistry"
    },
    {
      "unit_code":"CIVE",
      "group_code":"ENG",
      "unit_short_name":"Civil & Environmental Engg",
      "unit_full_name":"Civil and Environmental Engineering"
    },
    {
      "unit_code":"CLASSICS",
      "group_code":"ART",
      "unit_short_name":"Classical Studies",
      "unit_full_name":"Classical Studies"
    },
    {
      "unit_code":"CO",
      "group_code":"MAT",
      "unit_short_name":"Combinatorics & Optimization",
      "unit_full_name":"Combinatorics & Optimization"
    },
    {
      "unit_code":"CS",
      "group_code":"MAT",
      "unit_short_name":"Computer Sci - Cheriton School",
      "unit_full_name":"Computer Science - David R. Cheriton School of"
    },
    {
      "unit_code":"DANCE",
      "group_code":"ART",
      "unit_short_name":"Dance",
      "unit_full_name":"Dance"
    },
    {
      "unit_code":"DRAMA",
      "group_code":"ART",
      "unit_short_name":"Drama & Speech Communication",
      "unit_full_name":"Drama & Speech Communication"
    },
    {
      "unit_code":"EARTH",
      "group_code":"SCI",
      "unit_short_name":"Earth & Environmental Sciences",
      "unit_full_name":"Earth and Environmental Sciences"
    },
    {
      "unit_code":"ECE",
      "group_code":"ENG",
      "unit_short_name":"Electrical & Computer Engg",
      "unit_full_name":"Electrical & Computer Engineering"
    },
    {
      "unit_code":"ECON",
      "group_code":"ART",
      "unit_short_name":"Economics",
      "unit_full_name":"Economics"
    },
    {
      "unit_code":"ENG",
      "group_code":"ENG",
      "unit_short_name":"Engineering",
      "unit_full_name":"Engineering"
    },
    {
      "unit_code":"ENGDEAN",
      "group_code":"ENG",
      "unit_short_name":"Dean of Engineering",
      "unit_full_name":"Dean of Engineering"
    },
    {
      "unit_code":"ENGL",
      "group_code":"ART",
      "unit_short_name":"English Language & Literature",
      "unit_full_name":"English Language & Literature"
    },
    {
      "unit_code":"ENV",
      "group_code":"ENV",
      "unit_short_name":"Environment",
      "unit_full_name":"Environment"
    },
    {
      "unit_code":"ENVDEAN",
      "group_code":"ENV",
      "unit_short_name":"Dean of Environment",
      "unit_full_name":"Dean of Environment"
    },
    {
      "unit_code":"ERS",
      "group_code":"ENV",
      "unit_short_name":"Environment & Resource Studies",
      "unit_full_name":"Environment & Resource Studies"
    },
    {
      "unit_code":"FINE",
      "group_code":"ART",
      "unit_short_name":"Fine Arts",
      "unit_full_name":"Fine Arts"
    },
    {
      "unit_code":"FR",
      "group_code":"ART",
      "unit_short_name":"French Studies",
      "unit_full_name":"French Studies"
    },
    {
      "unit_code":"GEOE",
      "group_code":"ENG",
      "unit_short_name":"Geological Engineering",
      "unit_full_name":"Geological Engineering"
    },
    {
      "unit_code":"GEOG",
      "group_code":"ENV",
      "unit_short_name":"Geography & Environmental Mgmt",
      "unit_full_name":"Geography & Environmental Management"
    },
    {
      "unit_code":"GERSLAV",
      "group_code":"ART",
      "unit_short_name":"Germanic & Slavic Studies",
      "unit_full_name":"Germanic & Slavic Studies"
    },
    {
      "unit_code":"GRAD",
      "group_code":"GRAD",
      "unit_short_name":"Graduate Studies",
      "unit_full_name":"Graduate Studies"
    },
    {
      "unit_code":"GRADDEAN",
      "group_code":"GRAD",
      "unit_short_name":"Graduate Dean",
      "unit_full_name":"Graduate Dean"
    },
    {
      "unit_code":"HIST",
      "group_code":"ART",
      "unit_short_name":"History",
      "unit_full_name":"History"
    },
    {
      "unit_code":"HLTHGERON",
      "group_code":"AHS",
      "unit_short_name":"Public Hlth&Hlth Sys-School of",
      "unit_full_name":"Public Health and Health Systems - School of"
    },
    {
      "unit_code":"ICR",
      "group_code":"MAT",
      "unit_short_name":"Inst for Computer Research",
      "unit_full_name":"Institute for Computer Research"
    },
    {
      "unit_code":"IS",
      "group_code":"IS",
      "unit_short_name":"Independent Studies",
      "unit_full_name":"Independent Studies"
    },
    {
      "unit_code":"KIN",
      "group_code":"AHS",
      "unit_short_name":"Kinesiology",
      "unit_full_name":"Kinesiology"
    },
    {
      "unit_code":"MAT",
      "group_code":"MAT",
      "unit_short_name":"Math",
      "unit_full_name":"Math"
    },
    {
      "unit_code":"MATHDEAN",
      "group_code":"MAT",
      "unit_short_name":"Dean of Mathematics",
      "unit_full_name":"Dean of Mathematics"
    },
    {
      "unit_code":"ME",
      "group_code":"ENG",
      "unit_short_name":"Mechanical & Mechatronics Engg",
      "unit_full_name":"Mechanical and Mechatronics Engineering"
    },
    {
      "unit_code":"MSCI",
      "group_code":"ENG",
      "unit_short_name":"Management Sciences",
      "unit_full_name":"Management Sciences"
    },
    {
      "unit_code":"OPTOM",
      "group_code":"SCI",
      "unit_short_name":"Optometry & Vision Sci-Sch of",
      "unit_full_name":"Optometry & Vision Science - School of"
    },
    {
      "unit_code":"PHARM",
      "group_code":"SCI",
      "unit_short_name":"Pharmacy - School of",
      "unit_full_name":"Pharmacy - School of"
    },
    {
      "unit_code":"PHIL",
      "group_code":"ART",
      "unit_short_name":"Philosophy",
      "unit_full_name":"Philosophy"
    },
    {
      "unit_code":"PHYS",
      "group_code":"SCI",
      "unit_short_name":"Physics & Astronomy",
      "unit_full_name":"Physics & Astronomy"
    },
    {
      "unit_code":"PLAN",
      "group_code":"ENV",
      "unit_short_name":"Planning - School of",
      "unit_full_name":"Planning - School of"
    },
    {
      "unit_code":"PMATH",
      "group_code":"MAT",
      "unit_short_name":"Pure Mathematics",
      "unit_full_name":"Pure Mathematics"
    },
    {
      "unit_code":"PSCI",
      "group_code":"ART",
      "unit_short_name":"Political Science",
      "unit_full_name":"Political Science"
    },
    {
      "unit_code":"PSYCH",
      "group_code":"ART",
      "unit_short_name":"Psychology",
      "unit_full_name":"Psychology"
    },
    {
      "unit_code":"REC",
      "group_code":"AHS",
      "unit_short_name":"Recreation & Leisure Studies",
      "unit_full_name":"Recreation & Leisure Studies"
    },
    {
      "unit_code":"REN",
      "group_code":"REN",
      "unit_short_name":"Renison University College",
      "unit_full_name":"Renison University College"
    },
    {
      "unit_code":"RS",
      "group_code":"ART",
      "unit_short_name":"Religious Studies",
      "unit_full_name":"Religious Studies"
    },
    {
      "unit_code":"SCI",
      "group_code":"SCI",
      "unit_short_name":"Science",
      "unit_full_name":"Science"
    },
    {
      "unit_code":"SCIDEAN",
      "group_code":"SCI",
      "unit_short_name":"Dean of Science Office",
      "unit_full_name":"Dean of Science Office"
    },
    {
      "unit_code":"SEED",
      "group_code":"ENV",
      "unit_short_name":"Env, Entr & Dev - School of",
      "unit_full_name":"Environment, Enterprise & Development - School of"
    },
    {
      "unit_code":"SOC",
      "group_code":"ART",
      "unit_short_name":"Sociology & Legal Studies",
      "unit_full_name":"Sociology and Legal Studies"
    },
    {
      "unit_code":"SPAN",
      "group_code":"ART",
      "unit_short_name":"Spanish & Latin American Stud.",
      "unit_full_name":"Spanish & Latin American Studies"
    },
    {
      "unit_code":"STATACTSC",
      "group_code":"MAT",
      "unit_short_name":"Statistics & Actuarial Science",
      "unit_full_name":"Statistics & Actuarial Science"
    },
    {
      "unit_code":"STJ",
      "group_code":"STJ",
      "unit_short_name":"St Jerome's University",
      "unit_full_name":"St Jerome's University"
    },
    {
      "unit_code":"STP",
      "group_code":"STP",
      "unit_short_name":"St Paul's University College",
      "unit_full_name":"St Paul's University College"
    },
    {
      "unit_code":"STV",
      "group_code":"ENG",
      "unit_short_name":"Society, Technology&Values Ctr",
      "unit_full_name":"Society, Technology & Values Centre"
    },
    {
      "unit_code":"SYDE",
      "group_code":"ENG",
      "unit_short_name":"Systems Design Engineering",
      "unit_full_name":"Systems Design Engineering"
    },
    {
      "unit_code":"THC",
      "group_code":"NULL",
      "unit_short_name":"Theatre Centre",
      "unit_full_name":"Theatre Centre"
    },
    {
      "unit_code":"UW",
      "group_code":"NULL",
      "unit_short_name":"University of Waterloo",
      "unit_full_name":"University of Waterloo"
    },
    {
      "unit_code":"VPA",
      "group_code":"VPA",
      "unit_short_name":"Interdisciplinary Studies",
      "unit_full_name":"Interdisciplinary Studies"
    },
    {
      "unit_code":"WS",
      "group_code":"ART",
      "unit_short_name":"Women's Studies",
      "unit_full_name":"Women's Studies"
    }
  ]
}
```


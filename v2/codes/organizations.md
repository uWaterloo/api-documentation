# Code Lookups for Organizations

```
GET /codes/organizations.{format}
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
GET /codes/organizations.{format}
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
GET /codes/organizations.{format}
```

- **https://api.uwaterloo.ca/v2/codes/organizations.json**
- **https://api.uwaterloo.ca/v2/codes/organizations.xml**
- **https://api.uwaterloo.ca/v2/codes/organizations.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>organization</b></td>
    <td>string</td>
    <td>Organization</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Description of group</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":126,
    "timestamp":1381958128,
    "status":200,
    "message":"Request successful",
    "method_id":1231,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "organization":"ACC",
      "description":"School of Accounting & Finance"
    },
    {
      "organization":"AHS",
      "description":"Applied Health Sciences"
    },
    {
      "organization":"AHSDEAN",
      "description":"Dean of Applied Health Sciences"
    },
    {
      "organization":"AMATH",
      "description":"Applied Mathematics"
    },
    {
      "organization":"ANTH",
      "description":"Anthropology"
    },
    {
      "organization":"ARCH",
      "description":"School of Architecture"
    },
    {
      "organization":"ART",
      "description":"Arts"
    },
    {
      "organization":"ARTSDEAN",
      "description":"Dean of Arts"
    },
    {
      "organization":"BIOL",
      "description":"Biology"
    },
    {
      "organization":"CBET",
      "description":"Conrad Business, Entrepreneurship & Technology"
    },
    {
      "organization":"CECS",
      "description":"Coop Education & Career Action"
    },
    {
      "organization":"CGC",
      "description":"Conrad Grebel College"
    },
    {
      "organization":"CHE",
      "description":"Chemical Engineering"
    },
    {
      "organization":"CHEM",
      "description":"Chemistry"
    },
    {
      "organization":"CIVE",
      "description":"Civil & Environmental Engineering"
    },
    {
      "organization":"CLASSICS",
      "description":"Classical Studies"
    },
    {
      "organization":"CO",
      "description":"Combinatorics & Optimization"
    },
    {
      "organization":"CS",
      "description":"Computer Science - Cheriton School"
    },
    {
      "organization":"DANCE",
      "description":"Dance"
    },
    {
      "organization":"DRAMA",
      "description":"Drama & Speech Communication"
    },
    {
      "organization":"EARTH",
      "description":"Earth & Environmental Sciences"
    },
    {
      "organization":"ECE",
      "description":"Electrical & Computer Engineering"
    },
    {
      "organization":"ECON",
      "description":"Economics"
    },
    {
      "organization":"ENG",
      "description":"Engineering"
    },
    {
      "organization":"ENGDEAN",
      "description":"Dean of Engineering"
    },
    {
      "organization":"ENGL",
      "description":"English Language & Literature"
    },
    {
      "organization":"ENV",
      "description":"Environment"
    },
    {
      "organization":"ENVDEAN",
      "description":"Dean of Environment"
    },
    {
      "organization":"ERS",
      "description":"Environment & Resource Studies"
    },
    {
      "organization":"FINE",
      "description":"Fine Arts"
    },
    {
      "organization":"FR",
      "description":"French Studies"
    },
    {
      "organization":"GEOE",
      "description":"Geological Engineering"
    },
    {
      "organization":"GEOG",
      "description":"Geography & Environmental Management"
    },
    {
      "organization":"GERSLAV",
      "description":"Germanic & Slavic Studies"
    },
    {
      "organization":"GRAD",
      "description":"Graduate Studies"
    },
    {
      "organization":"GRADDEAN",
      "description":"Graduate Dean"
    },
    {
      "organization":"HIST",
      "description":"History"
    },
    {
      "organization":"HLTHGERON",
      "description":"School of Public Health Science"
    },
    {
      "organization":"ICR",
      "description":"Institute for Computer Research"
    },
    {
      "organization":"IS",
      "description":"Independent Studies"
    },
    {
      "organization":"KIN",
      "description":"Kinesiology"
    },
    {
      "organization":"MAT",
      "description":"Math"
    },
    {
      "organization":"MATHDEAN",
      "description":"Dean of Mathematics"
    },
    {
      "organization":"ME",
      "description":"Mechanical & Mechatronics Engineering"
    },
    {
      "organization":"MSCI",
      "description":"Management Sciences"
    },
    {
      "organization":"OPTOM",
      "description":"School of Optometry & Vision Science"
    },
    {
      "organization":"PHARM",
      "description":"School of Pharmacy"
    },
    {
      "organization":"PHIL",
      "description":"Philosophy"
    },
    {
      "organization":"PHYS",
      "description":"Physics & Astronomy"
    },
    {
      "organization":"PLAN",
      "description":"School of Planning"
    },
    {
      "organization":"PMATH",
      "description":"Pure Mathematics"
    },
    {
      "organization":"PSCI",
      "description":"Political Science"
    },
    {
      "organization":"PSYCH",
      "description":"Psychology"
    },
    {
      "organization":"REC",
      "description":"Recreation & Leisure Studies"
    },
    {
      "organization":"REN",
      "description":"Renison University College"
    },
    {
      "organization":"RS",
      "description":"Religious Studies"
    },
    {
      "organization":"SCI",
      "description":"Science"
    },
    {
      "organization":"SCIDEAN",
      "description":"Dean of Science Office"
    },
    {
      "organization":"SEED",
      "description":"School of Environment, Enterprise & Development"
    },
    {
      "organization":"SOC",
      "description":"Sociology & Legal Studies"
    },
    {
      "organization":"SPAN",
      "description":"Spanish & Latin American Studies"
    },
    {
      "organization":"STATACTSC",
      "description":"Statistics & Actuarial Science"
    },
    {
      "organization":"STJ",
      "description":"St Jerome's University"
    },
    {
      "organization":"STP",
      "description":"St Paul's University College"
    },
    {
      "organization":"STV",
      "description":"Society, Technology & Values"
    },
    {
      "organization":"SYDE",
      "description":"Systems Design Engineering"
    },
    {
      "organization":"THC",
      "description":"Theatre Centre"
    },
    {
      "organization":"UW",
      "description":"University of Waterloo"
    },
    {
      "organization":"VPA",
      "description":"Interdisciplinary Studies"
    },
    {
      "organization":"WS",
      "description":"Women's Studies"
    }
  ]
}
```


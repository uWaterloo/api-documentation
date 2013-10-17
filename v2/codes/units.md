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
    <td><b>unit</b></td>
    <td>string</td>
    <td>Organizational Unit</td>
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
    "requests":144,
    "timestamp":1382021198,
    "status":200,
    "message":"Request successful",
    "method_id":1231,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "unit":"ACC",
      "description":"School of Accounting & Finance"
    },
    {
      "unit":"AHS",
      "description":"Applied Health Sciences"
    },
    {
      "unit":"AHSDEAN",
      "description":"Dean of Applied Health Sciences"
    },
    {
      "unit":"AMATH",
      "description":"Applied Mathematics"
    },
    {
      "unit":"ANTH",
      "description":"Anthropology"
    },
    {
      "unit":"ARCH",
      "description":"School of Architecture"
    },
    {
      "unit":"ART",
      "description":"Arts"
    },
    {
      "unit":"ARTSDEAN",
      "description":"Dean of Arts"
    },
    {
      "unit":"BIOL",
      "description":"Biology"
    },
    {
      "unit":"CBET",
      "description":"Conrad Business, Entrepreneurship & Technology"
    },
    {
      "unit":"CECS",
      "description":"Coop Education & Career Action"
    },
    {
      "unit":"CGC",
      "description":"Conrad Grebel College"
    },
    {
      "unit":"CHE",
      "description":"Chemical Engineering"
    },
    {
      "unit":"CHEM",
      "description":"Chemistry"
    },
    {
      "unit":"CIVE",
      "description":"Civil & Environmental Engineering"
    },
    {
      "unit":"CLASSICS",
      "description":"Classical Studies"
    },
    {
      "unit":"CO",
      "description":"Combinatorics & Optimization"
    },
    {
      "unit":"CS",
      "description":"Computer Science - Cheriton School"
    },
    {
      "unit":"DANCE",
      "description":"Dance"
    },
    {
      "unit":"DRAMA",
      "description":"Drama & Speech Communication"
    },
    {
      "unit":"EARTH",
      "description":"Earth & Environmental Sciences"
    },
    {
      "unit":"ECE",
      "description":"Electrical & Computer Engineering"
    },
    {
      "unit":"ECON",
      "description":"Economics"
    },
    {
      "unit":"ENG",
      "description":"Engineering"
    },
    {
      "unit":"ENGDEAN",
      "description":"Dean of Engineering"
    },
    {
      "unit":"ENGL",
      "description":"English Language & Literature"
    },
    {
      "unit":"ENV",
      "description":"Environment"
    },
    {
      "unit":"ENVDEAN",
      "description":"Dean of Environment"
    },
    {
      "unit":"ERS",
      "description":"Environment & Resource Studies"
    },
    {
      "unit":"FINE",
      "description":"Fine Arts"
    },
    {
      "unit":"FR",
      "description":"French Studies"
    },
    {
      "unit":"GEOE",
      "description":"Geological Engineering"
    },
    {
      "unit":"GEOG",
      "description":"Geography & Environmental Management"
    },
    {
      "unit":"GERSLAV",
      "description":"Germanic & Slavic Studies"
    },
    {
      "unit":"GRAD",
      "description":"Graduate Studies"
    },
    {
      "unit":"GRADDEAN",
      "description":"Graduate Dean"
    },
    {
      "unit":"HIST",
      "description":"History"
    },
    {
      "unit":"HLTHGERON",
      "description":"School of Public Health Science"
    },
    {
      "unit":"ICR",
      "description":"Institute for Computer Research"
    },
    {
      "unit":"IS",
      "description":"Independent Studies"
    },
    {
      "unit":"KIN",
      "description":"Kinesiology"
    },
    {
      "unit":"MAT",
      "description":"Math"
    },
    {
      "unit":"MATHDEAN",
      "description":"Dean of Mathematics"
    },
    {
      "unit":"ME",
      "description":"Mechanical & Mechatronics Engineering"
    },
    {
      "unit":"MSCI",
      "description":"Management Sciences"
    },
    {
      "unit":"OPTOM",
      "description":"School of Optometry & Vision Science"
    },
    {
      "unit":"PHARM",
      "description":"School of Pharmacy"
    },
    {
      "unit":"PHIL",
      "description":"Philosophy"
    },
    {
      "unit":"PHYS",
      "description":"Physics & Astronomy"
    },
    {
      "unit":"PLAN",
      "description":"School of Planning"
    },
    {
      "unit":"PMATH",
      "description":"Pure Mathematics"
    },
    {
      "unit":"PSCI",
      "description":"Political Science"
    },
    {
      "unit":"PSYCH",
      "description":"Psychology"
    },
    {
      "unit":"REC",
      "description":"Recreation & Leisure Studies"
    },
    {
      "unit":"REN",
      "description":"Renison University College"
    },
    {
      "unit":"RS",
      "description":"Religious Studies"
    },
    {
      "unit":"SCI",
      "description":"Science"
    },
    {
      "unit":"SCIDEAN",
      "description":"Dean of Science Office"
    },
    {
      "unit":"SEED",
      "description":"School of Environment, Enterprise & Development"
    },
    {
      "unit":"SOC",
      "description":"Sociology & Legal Studies"
    },
    {
      "unit":"SPAN",
      "description":"Spanish & Latin American Studies"
    },
    {
      "unit":"STATACTSC",
      "description":"Statistics & Actuarial Science"
    },
    {
      "unit":"STJ",
      "description":"St Jerome's University"
    },
    {
      "unit":"STP",
      "description":"St Paul's University College"
    },
    {
      "unit":"STV",
      "description":"Society, Technology & Values"
    },
    {
      "unit":"SYDE",
      "description":"Systems Design Engineering"
    },
    {
      "unit":"THC",
      "description":"Theatre Centre"
    },
    {
      "unit":"UW",
      "description":"University of Waterloo"
    },
    {
      "unit":"VPA",
      "description":"Interdisciplinary Studies"
    },
    {
      "unit":"WS",
      "description":"Women's Studies"
    }
  ]
}
```


# Code Lookups for subjects

```
GET /codes/subjects.{format}
```

## Description

> This method returns a list of all code lookups for subjects.

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
    <td>1237</td>
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

- https://github.com/uWaterloo/Datasets/blob/master/Quest/Subjects.csv


## Parameters

```
GET /codes/subjects.{format}
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
GET /codes/subjects.{format}
```

- **https://api.uwaterloo.ca/v2/codes/subjects.json**
- **https://api.uwaterloo.ca/v2/codes/subjects.xml**
- **https://api.uwaterloo.ca/v2/codes/subjects.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>subject</b></td>
    <td>string</td>
    <td>Subject</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Description of subject</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":127,
    "timestamp":1381958168,
    "status":200,
    "message":"Request successful",
    "method_id":1237,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "subject":"AADMS",
      "description":"Arts Administration Specification Seminar"
    },
    {
      "subject":"AB",
      "description":"Arabic (WLU)"
    },
    {
      "subject":"ACC",
      "description":"Accounting"
    },
    {
      "subject":"ACTSC",
      "description":"Actuarial Science"
    },
    {
      "subject":"ADMGT",
      "description":"Advanced Management"
    },
    {
      "subject":"AES",
      "description":"Applied Environmental Studies"
    },
    {
      "subject":"AFM",
      "description":"Accounting & Financial Management"
    },
    {
      "subject":"AHS",
      "description":"Applied Health Sciences"
    },
    {
      "subject":"AMATH",
      "description":"Applied Mathematics"
    },
    {
      "subject":"ANTH",
      "description":"Anthropology"
    },
    {
      "subject":"APHYS",
      "description":"Applied Physics"
    },
    {
      "subject":"APPLS",
      "description":"Applied Language Studies"
    },
    {
      "subject":"ARBUS",
      "description":"Arts and Business"
    },
    {
      "subject":"ARCH",
      "description":"Architecture"
    },
    {
      "subject":"ARCHL",
      "description":"Archeology (WLU)"
    },
    {
      "subject":"ART",
      "description":"Art"
    },
    {
      "subject":"ARTS",
      "description":"Arts"
    },
    {
      "subject":"ASIAN",
      "description":"Asian Studies"
    },
    {
      "subject":"ASTRN",
      "description":"Astronomy (WLU)"
    },
    {
      "subject":"AVIA",
      "description":"Aviation"
    },
    {
      "subject":"BE",
      "description":"Business Entrepreneurship"
    },
    {
      "subject":"BET",
      "description":"Business, Entrepreneurship & Technology"
    },
    {
      "subject":"BIOL",
      "description":"Biology"
    },
    {
      "subject":"BME",
      "description":"Biomedical Engineering"
    },
    {
      "subject":"BOT",
      "description":"Botany"
    },
    {
      "subject":"BUS",
      "description":"Business"
    },
    {
      "subject":"CCIV",
      "description":"Classical Civilization"
    },
    {
      "subject":"CDNST",
      "description":"Canadian Studies"
    },
    {
      "subject":"CEDEV",
      "description":"Children's Education & Development"
    },
    {
      "subject":"CHE",
      "description":"Chemical Engineering"
    },
    {
      "subject":"CHEM",
      "description":"Chemistry"
    },
    {
      "subject":"CHINA",
      "description":"Chinese"
    },
    {
      "subject":"CIVE",
      "description":"Civil Engineering"
    },
    {
      "subject":"CLAS",
      "description":"Classical Studies"
    },
    {
      "subject":"CM",
      "description":"Computational Mathematics"
    },
    {
      "subject":"CMW",
      "description":"Church Music and Worship"
    },
    {
      "subject":"CO",
      "description":"Combinatorics & Optimization"
    },
    {
      "subject":"COGSCI",
      "description":"Cognitive Science"
    },
    {
      "subject":"COMM",
      "description":"Commerce"
    },
    {
      "subject":"COMPT",
      "description":"Computing (WLU)"
    },
    {
      "subject":"COMST",
      "description":"Communication Studies (WLU)"
    },
    {
      "subject":"CONST",
      "description":"Contemporary Studies (WLU)"
    },
    {
      "subject":"COOP",
      "description":"Co-op"
    },
    {
      "subject":"CROAT",
      "description":"Croatian"
    },
    {
      "subject":"CS",
      "description":"Computer Science"
    },
    {
      "subject":"CT",
      "description":"Catholic Thought"
    },
    {
      "subject":"CULMG",
      "description":"Cultural Management"
    },
    {
      "subject":"CULT",
      "description":"Cultural Studies"
    },
    {
      "subject":"DAC",
      "description":"Digital Arts Communication"
    },
    {
      "subject":"DANCE",
      "description":"Dance"
    },
    {
      "subject":"DEI",
      "description":"Digital Experience Innovation"
    },
    {
      "subject":"DES",
      "description":"Design"
    },
    {
      "subject":"DEVIS",
      "description":"Development & International Studies (WLU)"
    },
    {
      "subject":"DM",
      "description":"Design and Manufacturing"
    },
    {
      "subject":"DRAMA",
      "description":"Drama"
    },
    {
      "subject":"DUTCH",
      "description":"Dutch"
    },
    {
      "subject":"EARTH",
      "description":"Earth Science"
    },
    {
      "subject":"EASIA",
      "description":"East Asian Studies"
    },
    {
      "subject":"ECE",
      "description":"Electrical & Computer Engineering"
    },
    {
      "subject":"ECON",
      "description":"Economics"
    },
    {
      "subject":"EFAS",
      "description":"English for Academic Success"
    },
    {
      "subject":"ELE",
      "description":"Electrical Engineering"
    },
    {
      "subject":"ELPE",
      "description":"English Language Prof Exam"
    },
    {
      "subject":"ENBUS",
      "description":"Environment and Business"
    },
    {
      "subject":"ENGL",
      "description":"English"
    },
    {
      "subject":"ENVE",
      "description":"Environmental Engineering"
    },
    {
      "subject":"ENVS",
      "description":"Environmental Studies"
    },
    {
      "subject":"ERS",
      "description":"Environment & Resource Studies"
    },
    {
      "subject":"ESL",
      "description":"English as a Second Language"
    },
    {
      "subject":"FILM",
      "description":"Film (WLU)"
    },
    {
      "subject":"FINAN",
      "description":"Finance"
    },
    {
      "subject":"FINE",
      "description":"Fine Arts"
    },
    {
      "subject":"FR",
      "description":"French Studies"
    },
    {
      "subject":"FRCS",
      "description":"French Cultural Studies"
    },
    {
      "subject":"GBDA",
      "description":"Global Business & Digital Arts"
    },
    {
      "subject":"GEMCC",
      "description":"Geography & Environment. Management, Climate Change"
    },
    {
      "subject":"GENE",
      "description":"General Engineering"
    },
    {
      "subject":"GEOE",
      "description":"Geological Engineering"
    },
    {
      "subject":"GEOG",
      "description":"Geography"
    },
    {
      "subject":"GEOL",
      "description":"Geology (WLU)"
    },
    {
      "subject":"GER",
      "description":"German"
    },
    {
      "subject":"GERON",
      "description":"Gerontology"
    },
    {
      "subject":"GGOV",
      "description":"Global Governance"
    },
    {
      "subject":"GLOBAL",
      "description":"Global Studies (WLU)"
    },
    {
      "subject":"GRAD",
      "description":"Continuing Graduate Studies"
    },
    {
      "subject":"GRK",
      "description":"Greek"
    },
    {
      "subject":"GS",
      "description":"Graduate Studies"
    },
    {
      "subject":"HEBRW",
      "description":"Hebrew (WLU)"
    },
    {
      "subject":"HIST",
      "description":"History"
    },
    {
      "subject":"HLTH",
      "description":"Health Studies"
    },
    {
      "subject":"HRCS",
      "description":"Human Relations & Counselling Studies"
    },
    {
      "subject":"HRM",
      "description":"Human Resources Management"
    },
    {
      "subject":"HS",
      "description":"High School"
    },
    {
      "subject":"HSG",
      "description":"Health Studies and Gerontology"
    },
    {
      "subject":"HUMSC",
      "description":"Human Sciences"
    },
    {
      "subject":"HUNGN",
      "description":"Hungarian"
    },
    {
      "subject":"IFS",
      "description":"Inter-Faculty Studies"
    },
    {
      "subject":"INDEV",
      "description":"International Development"
    },
    {
      "subject":"INTEG",
      "description":"Integrated Studies"
    },
    {
      "subject":"INTERN",
      "description":"Internship"
    },
    {
      "subject":"INTST",
      "description":"International Studies"
    },
    {
      "subject":"INTTS",
      "description":"International Trade Seminars"
    },
    {
      "subject":"IS",
      "description":"Independent Studies"
    },
    {
      "subject":"ISS",
      "description":"Interdisciplinary Social Sciences"
    },
    {
      "subject":"ITAL",
      "description":"Italian"
    },
    {
      "subject":"ITALST",
      "description":"Italian Studies"
    },
    {
      "subject":"JAPAN",
      "description":"Japanese"
    },
    {
      "subject":"JS",
      "description":"Jewish Studies"
    },
    {
      "subject":"KIN",
      "description":"Kinesiology"
    },
    {
      "subject":"KOREA",
      "description":"Korean"
    },
    {
      "subject":"KPE",
      "description":"Kinesiology & Physical Education (WLU)"
    },
    {
      "subject":"LANG",
      "description":"Language (WLU)"
    },
    {
      "subject":"LAT",
      "description":"Latin"
    },
    {
      "subject":"LATAM",
      "description":"Latin American Studies"
    },
    {
      "subject":"LED",
      "description":"Local Economic Development"
    },
    {
      "subject":"LS",
      "description":"Legal Studies"
    },
    {
      "subject":"LSC",
      "description":"Legal Studies and Criminology"
    },
    {
      "subject":"MATBUS",
      "description":"Mathematical Business"
    },
    {
      "subject":"MATH",
      "description":"Mathematics"
    },
    {
      "subject":"ME",
      "description":"Mechanical Engineering"
    },
    {
      "subject":"MEDST",
      "description":"Media Studies (WLU)"
    },
    {
      "subject":"MEDVL",
      "description":"Medieval Studies"
    },
    {
      "subject":"MENV",
      "description":"Man Environment"
    },
    {
      "subject":"MES",
      "description":"Middle Eastern Studies"
    },
    {
      "subject":"MI",
      "description":"Mediterranean Studies (WLU)"
    },
    {
      "subject":"MISC",
      "description":"Miscellaneous"
    },
    {
      "subject":"MNS",
      "description":"Materials and Nano-Sciences"
    },
    {
      "subject":"MSCI",
      "description":"Management Sciences"
    },
    {
      "subject":"MSE",
      "description":"Management & Systems Engineering"
    },
    {
      "subject":"MTE",
      "description":"Mechatronics Engineering"
    },
    {
      "subject":"MTHEL",
      "description":"Mathematics Elective"
    },
    {
      "subject":"MUSIC",
      "description":"Music"
    },
    {
      "subject":"NANO",
      "description":"Nanotechnology"
    },
    {
      "subject":"NATST",
      "description":"Native Studies"
    },
    {
      "subject":"NE",
      "description":"Nanotechnology Engineering"
    },
    {
      "subject":"NES",
      "description":"Near Eastern Studies (WLU)"
    },
    {
      "subject":"OPTOM",
      "description":"Optometry"
    },
    {
      "subject":"PACS",
      "description":"Peace & Conflict Studies"
    },
    {
      "subject":"PAS",
      "description":"Personnel & Admininstration Studies"
    },
    {
      "subject":"PD",
      "description":"Professional Development"
    },
    {
      "subject":"PDARCH",
      "description":"Professional Development for Architect"
    },
    {
      "subject":"PDENG",
      "description":"Professional Development for Engineers"
    },
    {
      "subject":"PDPHRM",
      "description":"Professional Development for Pharmacy"
    },
    {
      "subject":"PED",
      "description":"Physical Education (WLU)"
    },
    {
      "subject":"PERST",
      "description":"Personnel Studies"
    },
    {
      "subject":"PHARM",
      "description":"Pharmacy"
    },
    {
      "subject":"PHIL",
      "description":"Philosophy"
    },
    {
      "subject":"PHS",
      "description":"Public Health Sciences"
    },
    {
      "subject":"PHYS",
      "description":"Physics"
    },
    {
      "subject":"PLAN",
      "description":"Planning"
    },
    {
      "subject":"PMATH",
      "description":"Pure Mathematics"
    },
    {
      "subject":"POLSH",
      "description":"Polish"
    },
    {
      "subject":"PORT",
      "description":"Portuguese"
    },
    {
      "subject":"PS",
      "description":"Public Service"
    },
    {
      "subject":"PSCI",
      "description":"Political Science"
    },
    {
      "subject":"PSYCH",
      "description":"Psychology"
    },
    {
      "subject":"QIC",
      "description":"Quantum Info & Computation"
    },
    {
      "subject":"REC",
      "description":"Recreation & Leisure Studies"
    },
    {
      "subject":"REES",
      "description":"Russian & Eastern European Studies"
    },
    {
      "subject":"RELC",
      "description":"Religion & Culture (WLU)"
    },
    {
      "subject":"RS",
      "description":"Religious Studies"
    },
    {
      "subject":"RUSS",
      "description":"Russian"
    },
    {
      "subject":"SCBUS",
      "description":"Science and Business"
    },
    {
      "subject":"SCI",
      "description":"Science"
    },
    {
      "subject":"SDS",
      "description":"Social Development Studies"
    },
    {
      "subject":"SE",
      "description":"Software Engineering"
    },
    {
      "subject":"SEQ",
      "description":"Co-op Sequence"
    },
    {
      "subject":"SI",
      "description":"Studies in Islam"
    },
    {
      "subject":"SIPAR",
      "description":"Studies in Personality & Religion"
    },
    {
      "subject":"SMF",
      "description":"Sexuality, Marriage & Family"
    },
    {
      "subject":"SOC",
      "description":"Sociology"
    },
    {
      "subject":"SOCIN",
      "description":"Social Innovation"
    },
    {
      "subject":"SOCWK",
      "description":"Social Work"
    },
    {
      "subject":"SOCWL",
      "description":"Social Welfare (WLU)"
    },
    {
      "subject":"SPAN",
      "description":"Spanish"
    },
    {
      "subject":"SPCOM",
      "description":"Speech Communication"
    },
    {
      "subject":"SPD",
      "description":"Spirituality & Personal Development"
    },
    {
      "subject":"STAT",
      "description":"Statistics"
    },
    {
      "subject":"STV",
      "description":"Society, Technology & Values"
    },
    {
      "subject":"SUSM",
      "description":"Sustainability Management"
    },
    {
      "subject":"SWK",
      "description":"Social Work"
    },
    {
      "subject":"SWREN",
      "description":"Social Work (BSW)"
    },
    {
      "subject":"SYDE",
      "description":"Systems Design Engineering"
    },
    {
      "subject":"TAX",
      "description":"Taxation"
    },
    {
      "subject":"THTRE",
      "description":"Theatre (WLU)"
    },
    {
      "subject":"TN",
      "description":"Theoretical Neuroscience"
    },
    {
      "subject":"TOUR",
      "description":"Tourism"
    },
    {
      "subject":"TPM",
      "description":"Technical Presentation Milestone"
    },
    {
      "subject":"TPPE",
      "description":"Tech Presentation Proficiency Examination"
    },
    {
      "subject":"TS",
      "description":"Theological Studies"
    },
    {
      "subject":"UKRAN",
      "description":"Ukrainian"
    },
    {
      "subject":"UN",
      "description":"Nuclear Engineering"
    },
    {
      "subject":"UNIV",
      "description":"University"
    },
    {
      "subject":"URBAN",
      "description":"Urban Studies (WLU)"
    },
    {
      "subject":"UU",
      "description":"Interdisciplinary Studies (WLU)"
    },
    {
      "subject":"VCULT",
      "description":"Visual Culture"
    },
    {
      "subject":"WATER",
      "description":"WATER"
    },
    {
      "subject":"WHMIS",
      "description":"Workplace Hazardous Materials Information System"
    },
    {
      "subject":"WKRPT",
      "description":"Work Report"
    },
    {
      "subject":"WS",
      "description":"Women's Studies"
    },
    {
      "subject":"ZOOL",
      "description":"Zoology"
    }
  ]
}
```


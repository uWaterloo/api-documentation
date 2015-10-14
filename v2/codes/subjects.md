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
  <tr>
    <td><b>unit</b></td>
    <td>string</td>
    <td>Subjects parent unit</td>
  </tr>
  <tr>
    <td><b>group</b></td>
    <td>string</td>
    <td>Subjects parent group</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":104,
    "timestamp":1444838214,
    "status":200,
    "message":"Request successful",
    "method_id":1237,
    "method":{

    }
  },
  "data":[
    {
      "subject":"AADMS",
      "description":"Arts Administration Specialization Seminar",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"AB",
      "description":"Arabic (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"ACC",
      "description":"Accounting",
      "unit":"ACC",
      "group":"ART"
    },
    {
      "subject":"ACINTY",
      "description":"Academic Integrity",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"ACTSC",
      "description":"Actuarial Science",
      "unit":"STATACTSC",
      "group":"MAT"
    },
    {
      "subject":"ADMGT",
      "description":"Advanced Management",
      "unit":"CBET",
      "group":"ENG"
    },
    {
      "subject":"AES",
      "description":"Applied Environmental Studies",
      "unit":"ENVDEAN",
      "group":"ENV"
    },
    {
      "subject":"AFM",
      "description":"Accounting and Financial Managment",
      "unit":"ACC",
      "group":"ART"
    },
    {
      "subject":"AHS",
      "description":"Applied Health Sciences",
      "unit":"AHSDEAN",
      "group":"AHS"
    },
    {
      "subject":"AMATH",
      "description":"Applied Mathematics",
      "unit":"AMATH",
      "group":"MAT"
    },
    {
      "subject":"ANTH",
      "description":"Anthropology",
      "unit":"ANTH",
      "group":"ART"
    },
    {
      "subject":"APHYS",
      "description":"Applied Physics",
      "unit":"ENGDEAN",
      "group":"ENG"
    },
    {
      "subject":"APPLS",
      "description":"Applied Language Studies",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"ARBUS",
      "description":"Arts and Business",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"ARCH",
      "description":"Architecture",
      "unit":"ARCH",
      "group":"ENG"
    },
    {
      "subject":"ARCHL",
      "description":"Archeology (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"ART",
      "description":"Art",
      "unit":"FINE",
      "group":"ART"
    },
    {
      "subject":"ARTS",
      "description":"Arts",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"ASIAN",
      "description":"Asian Studies",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"ASTRN",
      "description":"Astronomy (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"AVIA",
      "description":"Aviation",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"BASE",
      "description":"Bridge to Academic Success in English",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"BE",
      "description":"Business Entrepreneurship",
      "unit":"CBET",
      "group":"ENG"
    },
    {
      "subject":"BET",
      "description":"Business, Entrepreneurship and Technology",
      "unit":"CBET",
      "group":"ENG"
    },
    {
      "subject":"BIOL",
      "description":"Biology",
      "unit":"BIOL",
      "group":"SCI"
    },
    {
      "subject":"BME",
      "description":"Biomedical Engineering",
      "unit":"ENGDEAN",
      "group":"ENG"
    },
    {
      "subject":"BOT",
      "description":"Botany (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"BUS",
      "description":"Business",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"CCIV",
      "description":"Classical Civilization",
      "unit":"CLASSICS",
      "group":"ART"
    },
    {
      "subject":"CDNST",
      "description":"Canadian Studies",
      "unit":"STP",
      "group":"STP"
    },
    {
      "subject":"CEDEV",
      "description":"Children's Education & Development (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"CHE",
      "description":"Chemical Engineering",
      "unit":"CHE",
      "group":"ENG"
    },
    {
      "subject":"CHEM",
      "description":"Chemistry",
      "unit":"CHEM",
      "group":"SCI"
    },
    {
      "subject":"CHINA",
      "description":"Chinese",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"CIVE",
      "description":"Civil Engineering",
      "unit":"CIVE",
      "group":"ENG"
    },
    {
      "subject":"CLAS",
      "description":"Classical Studies",
      "unit":"CLASSICS",
      "group":"ART"
    },
    {
      "subject":"CM",
      "description":"Computational Mathematics",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"CMW",
      "description":"Church Music and Worship",
      "unit":"CGC",
      "group":"CGC"
    },
    {
      "subject":"CO",
      "description":"Combinatorics and Optimization",
      "unit":"CO",
      "group":"MAT"
    },
    {
      "subject":"COGSCI",
      "description":"Cognitive Science",
      "unit":"PHIL",
      "group":"ART"
    },
    {
      "subject":"COMM",
      "description":"Commerce",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"COMPT",
      "description":"Computing (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"COMST",
      "description":"Communication Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"CONST",
      "description":"Contemporary Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"COOP",
      "description":"Co-op",
      "unit":"CECS",
      "group":"VPA"
    },
    {
      "subject":"CROAT",
      "description":"Croatian",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"CS",
      "description":"Computer Science",
      "unit":"CS",
      "group":"MAT"
    },
    {
      "subject":"CT",
      "description":"Catholic Thought",
      "unit":"STJ",
      "group":"STJ"
    },
    {
      "subject":"CULMG",
      "description":"Cultural Management",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"CULT",
      "description":"Cultural Studies",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"DAC",
      "description":"Digital Arts Communication",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"DANCE",
      "description":"Dance",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"DEI",
      "description":"Digital Experience Innovation",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"DES",
      "description":"Design",
      "unit":"SYDE",
      "group":"ENG"
    },
    {
      "subject":"DEVIS",
      "description":"Development & International Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"DM",
      "description":"Design and Manufacturing",
      "unit":"ME",
      "group":"ENG"
    },
    {
      "subject":"DRAMA",
      "description":"Drama",
      "unit":"DRAMA",
      "group":"ART"
    },
    {
      "subject":"DUTCH",
      "description":"Dutch",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"EARTH",
      "description":"Earth Science",
      "unit":"EARTH",
      "group":"SCI"
    },
    {
      "subject":"EASIA",
      "description":"East Asian Studies",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"EBUS",
      "description":"Environment and Business",
      "unit":"ENVDEAN",
      "group":"ENV"
    },
    {
      "subject":"ECE",
      "description":"Electrical and Computer Engineering",
      "unit":"ECE",
      "group":"ENG"
    },
    {
      "subject":"ECON",
      "description":"Economics",
      "unit":"ECON",
      "group":"ART"
    },
    {
      "subject":"EFAS",
      "description":"English for Academic Success",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"ELE",
      "description":"Electrical Engineering",
      "unit":"ECE",
      "group":"ENG"
    },
    {
      "subject":"ELPE",
      "description":"English Language Proficiency Examination",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"EMLS",
      "description":"English for Multilingual Speakers",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"ENBUS",
      "description":"Environment and Business",
      "unit":"SEED",
      "group":"ENV"
    },
    {
      "subject":"ENGL",
      "description":"English",
      "unit":"ENGL",
      "group":"ART"
    },
    {
      "subject":"ENVE",
      "description":"Environmental Engineering",
      "unit":"ENGDEAN",
      "group":"ENG"
    },
    {
      "subject":"ENVS",
      "description":"Environmental Studies",
      "unit":"ENVDEAN",
      "group":"ENV"
    },
    {
      "subject":"ERS",
      "description":"Environment and Resource Studies",
      "unit":"ERS",
      "group":"ENV"
    },
    {
      "subject":"ESL",
      "description":"English as a Second Language",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"EVSY",
      "description":"Environment and Society",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"FILM",
      "description":"Film (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"FINAN",
      "description":"Finance",
      "unit":"ACC",
      "group":"ART"
    },
    {
      "subject":"FINE",
      "description":"Fine Arts",
      "unit":"FINE",
      "group":"ART"
    },
    {
      "subject":"FR",
      "description":"French Studies",
      "unit":"FR",
      "group":"ART"
    },
    {
      "subject":"FRCS",
      "description":"French Cultural Studies",
      "unit":"FR",
      "group":"ART"
    },
    {
      "subject":"GBDA",
      "description":"Global Business and Digital Arts",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"GEMCC",
      "description":"Geography and Environmental Mgmt, Climate Change",
      "unit":"GEOG",
      "group":"ENV"
    },
    {
      "subject":"GENE",
      "description":"General Engineering",
      "unit":"ENGDEAN",
      "group":"ENG"
    },
    {
      "subject":"GEOE",
      "description":"Geological Engineering",
      "unit":"CIVE",
      "group":"ENG"
    },
    {
      "subject":"GEOG",
      "description":"Geography",
      "unit":"GEOG",
      "group":"ENV"
    },
    {
      "subject":"GEOL",
      "description":"Geology (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"GER",
      "description":"German",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"GERON",
      "description":"Gerontology",
      "unit":"HLTHGERON",
      "group":"AHS"
    },
    {
      "subject":"GGOV",
      "description":"Global Governance",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"GLOBAL",
      "description":"Global Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"GRAD",
      "description":"Continuing Graduate Studies",
      "unit":"GRADDEAN",
      "group":"GRAD"
    },
    {
      "subject":"GRK",
      "description":"Greek",
      "unit":"CLASSICS",
      "group":"ART"
    },
    {
      "subject":"GS",
      "description":"Graduate Studies",
      "unit":"GRADDEAN",
      "group":"GRAD"
    },
    {
      "subject":"HEBRW",
      "description":"Hebrew (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"HIST",
      "description":"History",
      "unit":"HIST",
      "group":"ART"
    },
    {
      "subject":"HLTH",
      "description":"Health Studies",
      "unit":"HLTHGERON",
      "group":"AHS"
    },
    {
      "subject":"HRCS",
      "description":"Human Relations & Counselling Studies",
      "unit":"PSYCH",
      "group":"ART"
    },
    {
      "subject":"HRM",
      "description":"Human Resources Management",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"HS",
      "description":"High School",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"HSG",
      "description":"Health Studies and Gerontology",
      "unit":"HLTHGERON",
      "group":"AHS"
    },
    {
      "subject":"HUMSC",
      "description":"Human Sciences",
      "unit":"STJ",
      "group":"STJ"
    },
    {
      "subject":"HUNGN",
      "description":"Hungarian",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"IFS",
      "description":"Inter-Faculty Studies",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"INDEV",
      "description":"International Development",
      "unit":"SEED",
      "group":"ENV"
    },
    {
      "subject":"INTEG",
      "description":"Integrated Studies",
      "unit":"ENVDEAN",
      "group":"ENV"
    },
    {
      "subject":"INTERN",
      "description":"Internship",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"INTST",
      "description":"International Studies",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"INTTS",
      "description":"International Trade Seminars",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"IS",
      "description":"Independent Studies",
      "unit":"IS",
      "group":"IS"
    },
    {
      "subject":"ISS",
      "description":"Interdisciplinary Social Sciences",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"ITAL",
      "description":"Italian",
      "unit":"STJ",
      "group":"STJ"
    },
    {
      "subject":"ITALST",
      "description":"Italian Studies",
      "unit":"STJ",
      "group":"STJ"
    },
    {
      "subject":"JAPAN",
      "description":"Japanese",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"JS",
      "description":"Jewish Studies",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"KIN",
      "description":"Kinesiology",
      "unit":"KIN",
      "group":"AHS"
    },
    {
      "subject":"KOREA",
      "description":"Korean",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"KPE",
      "description":"Kinesiology and Physical Education (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"LANG",
      "description":"Language (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"LAT",
      "description":"Latin",
      "unit":"CLASSICS",
      "group":"ART"
    },
    {
      "subject":"LATAM",
      "description":"Latin American Studies",
      "unit":"SPAN",
      "group":"ART"
    },
    {
      "subject":"LED",
      "description":"Local Economic Development",
      "unit":"ENVDEAN",
      "group":"ENV"
    },
    {
      "subject":"LS",
      "description":"Legal Studies",
      "unit":"SOC",
      "group":"ART"
    },
    {
      "subject":"LSC",
      "description":"Legal Studies and Criminology",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"MATBUS",
      "description":"Mathematical Business",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"MATH",
      "description":"Mathematics",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"ME",
      "description":"Mechanical Engineering",
      "unit":"ME",
      "group":"ENG"
    },
    {
      "subject":"MEDST",
      "description":"Media Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"MEDVL",
      "description":"Medieval Studies",
      "unit":"CLASSICS",
      "group":"ART"
    },
    {
      "subject":"MENV",
      "description":"Man Environment",
      "unit":"ERS",
      "group":"ENV"
    },
    {
      "subject":"MES",
      "description":"Middle Eastern Studies",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"MI",
      "description":"Mediterranean Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"MISC",
      "description":"Miscellaneous",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"MNS",
      "description":"Materials and Nano-Sciences",
      "unit":"CHEM",
      "group":"SCI"
    },
    {
      "subject":"MSCI",
      "description":"Management Sciences",
      "unit":"MSCI",
      "group":"ENG"
    },
    {
      "subject":"MSE",
      "description":"Management & Systems",
      "unit":"SYDE",
      "group":"ENG"
    },
    {
      "subject":"MTE",
      "description":"Mechatronics Engineering",
      "unit":"ME",
      "group":"ENG"
    },
    {
      "subject":"MTHEL",
      "description":"Mathematics Elective",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"MUSIC",
      "description":"Music",
      "unit":"CGC",
      "group":"CGC"
    },
    {
      "subject":"NANO",
      "description":"Nanotechnology",
      "unit":"GRAD",
      "group":"GRAD"
    },
    {
      "subject":"NATST",
      "description":"Native Studies",
      "unit":"STP",
      "group":"STP"
    },
    {
      "subject":"NE",
      "description":"Nanotechnology Engineering",
      "unit":"ENGDEAN",
      "group":"ENG"
    },
    {
      "subject":"NES",
      "description":"Near Eastern Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"OPTOM",
      "description":"Optometry",
      "unit":"OPTOM",
      "group":"SCI"
    },
    {
      "subject":"PACS",
      "description":"Peace and Conflict Studies",
      "unit":"CGC",
      "group":"CGC"
    },
    {
      "subject":"PAS",
      "description":"Personnel & Administration Studies",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"PD",
      "description":"Professional Development",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"PDARCH",
      "description":"Professional Development for Architecture Students",
      "unit":"ARCH",
      "group":"ENG"
    },
    {
      "subject":"PDENG",
      "description":"Professional Development for Engineering Students",
      "unit":"ENGDEAN",
      "group":"ENG"
    },
    {
      "subject":"PDPHRM",
      "description":"Professional Development for Pharmacy Students",
      "unit":"PHARM",
      "group":"SCI"
    },
    {
      "subject":"PED",
      "description":"Physical Education (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"PERST",
      "description":"Personnel Studies",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"PHARM",
      "description":"Pharmacy",
      "unit":"PHARM",
      "group":"SCI"
    },
    {
      "subject":"PHIL",
      "description":"Philosophy",
      "unit":"PHIL",
      "group":"ART"
    },
    {
      "subject":"PHS",
      "description":"Public Health Sciences",
      "unit":"HLTHGERON",
      "group":"AHS"
    },
    {
      "subject":"PHYS",
      "description":"Physics",
      "unit":"PHYS",
      "group":"SCI"
    },
    {
      "subject":"PLAN",
      "description":"Planning",
      "unit":"PLAN",
      "group":"ENV"
    },
    {
      "subject":"PMATH",
      "description":"Pure Mathematics",
      "unit":"PMATH",
      "group":"MAT"
    },
    {
      "subject":"POLSH",
      "description":"Polish",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"PORT",
      "description":"Portuguese",
      "unit":"SPAN",
      "group":"ART"
    },
    {
      "subject":"PS",
      "description":"Public Serivce",
      "unit":"ARTSDEAN",
      "group":"ART"
    },
    {
      "subject":"PSCI",
      "description":"Political Science",
      "unit":"PSCI",
      "group":"ART"
    },
    {
      "subject":"PSYCH",
      "description":"Psychology",
      "unit":"PSYCH",
      "group":"ART"
    },
    {
      "subject":"QIC",
      "description":"Quantum Information and Computation",
      "unit":"GRAD",
      "group":"GRAD"
    },
    {
      "subject":"REC",
      "description":"Recreation and Leisure Studies",
      "unit":"REC",
      "group":"AHS"
    },
    {
      "subject":"REES",
      "description":"Russian and Eastern European Studies",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"RELC",
      "description":"Religion & Culture (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"RS",
      "description":"Religious Studies",
      "unit":"RS",
      "group":"ART"
    },
    {
      "subject":"RSCH",
      "description":"Research",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"RUSS",
      "description":"Russian",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"SCBUS",
      "description":"Science and Business",
      "unit":"SCIDEAN",
      "group":"SCI"
    },
    {
      "subject":"SCI",
      "description":"Science",
      "unit":"SCIDEAN",
      "group":"SCI"
    },
    {
      "subject":"SDS",
      "description":"Social Development Studies",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"SE",
      "description":"Software Engineering",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"SEQ",
      "description":"Co-op Sequence",
      "unit":"MATHDEAN",
      "group":"MAT"
    },
    {
      "subject":"SI",
      "description":"Studies in Islam",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"SIPAR",
      "description":"Studies in Personality & Religion",
      "unit":"STP",
      "group":"STP"
    },
    {
      "subject":"SMF",
      "description":"Sexuality, Marriage and the Family",
      "unit":"STJ",
      "group":"STJ"
    },
    {
      "subject":"SOC",
      "description":"Sociology",
      "unit":"SOC",
      "group":"ART"
    },
    {
      "subject":"SOCIN",
      "description":"Social Innovation",
      "unit":"SEED",
      "group":"ENV"
    },
    {
      "subject":"SOCWK",
      "description":"Social Work (Social Development Studies)",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"SOCWL",
      "description":"Social Welfare (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"SPAN",
      "description":"Spanish",
      "unit":"SPAN",
      "group":"ART"
    },
    {
      "subject":"SPCOM",
      "description":"Speech Communication",
      "unit":"DRAMA",
      "group":"ART"
    },
    {
      "subject":"SPD",
      "description":"Spirituality and Personal Development",
      "unit":"STP",
      "group":"STP"
    },
    {
      "subject":"STAT",
      "description":"Statistics",
      "unit":"STATACTSC",
      "group":"MAT"
    },
    {
      "subject":"STV",
      "description":"Society, Technology and Values",
      "unit":"STV",
      "group":"ENG"
    },
    {
      "subject":"SUSM",
      "description":"Sustainability Management",
      "unit":"SEED",
      "group":"ENV"
    },
    {
      "subject":"SWK",
      "description":"Social Work",
      "unit":"AHSDEAN",
      "group":"AHS"
    },
    {
      "subject":"SWREN",
      "description":"Social Work (Bachelor of Social Work)",
      "unit":"REN",
      "group":"REN"
    },
    {
      "subject":"SYDE",
      "description":"Systems Design Engineering",
      "unit":"SYDE",
      "group":"ENG"
    },
    {
      "subject":"TAX",
      "description":"Taxation",
      "unit":"ACC",
      "group":"ART"
    },
    {
      "subject":"THTRE",
      "description":"Theatre (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"TN",
      "description":"Theoretical Neuroscience",
      "unit":"GRAD",
      "group":"GRAD"
    },
    {
      "subject":"TOUR",
      "description":"Tourism",
      "unit":"ENVDEAN",
      "group":"ENV"
    },
    {
      "subject":"TPM",
      "description":"Technical Presentation Milestone",
      "unit":"ECE",
      "group":"ENG"
    },
    {
      "subject":"TPPE",
      "description":"Technical Presentation Proficiency Requirement",
      "unit":"ECE",
      "group":"ENG"
    },
    {
      "subject":"TS",
      "description":"Theological Studies",
      "unit":"CGC",
      "group":"CGC"
    },
    {
      "subject":"UKRAN",
      "description":"Ukrainian",
      "unit":"GERSLAV",
      "group":"ART"
    },
    {
      "subject":"UN",
      "description":"Nuclear Engineering",
      "unit":"CIVE",
      "group":"ENG"
    },
    {
      "subject":"UNIV",
      "description":"University",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"URBAN",
      "description":"Urban Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"UU",
      "description":"University Interdisciplinary Studies (WLU)",
      "unit":"VPA",
      "group":"VPA"
    },
    {
      "subject":"VCULT",
      "description":"Visual Culture",
      "unit":"FINE",
      "group":"ART"
    },
    {
      "subject":"WATER",
      "description":"Water",
      "unit":"GRAD",
      "group":"GRAD"
    },
    {
      "subject":"WHMIS",
      "description":"Workplace Hazardous Materials Information Systems",
      "unit":"SCIDEAN",
      "group":"SCI"
    },
    {
      "subject":"WKRPT",
      "description":"Work-term Report",
      "unit":"CECS",
      "group":"VPA"
    },
    {
      "subject":"WS",
      "description":"Women's Studies",
      "unit":"WS",
      "group":"ART"
    },
    {
      "subject":"ZOOL",
      "description":"Zoology (WLU)",
      "unit":"VPA",
      "group":"VPA"
    }
  ]
}
```

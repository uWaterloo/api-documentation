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
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":474,
    "timestamp":1384886344,
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
      "description":"Arts Administration Specialization Seminar",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"AB",
      "description":"Arabic (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"ACC",
      "description":"Accounting",
      "unit":"ACC"
    },
    {
      "subject":"ACINTY",
      "description":"Academic Integrity",
      "unit":"VPA"
    },
    {
      "subject":"ACTSC",
      "description":"Actuarial Science",
      "unit":"STATACTSC"
    },
    {
      "subject":"ADMGT",
      "description":"Advanced Management",
      "unit":"CBET"
    },
    {
      "subject":"AES",
      "description":"Applied Environmental Studies",
      "unit":"ENVDEAN"
    },
    {
      "subject":"AFM",
      "description":"Accounting and Financial Managment",
      "unit":"ACC"
    },
    {
      "subject":"AHS",
      "description":"Applied Health Sciences",
      "unit":"AHSDEAN"
    },
    {
      "subject":"AMATH",
      "description":"Applied Mathematics",
      "unit":"AMATH"
    },
    {
      "subject":"ANTH",
      "description":"Anthropology",
      "unit":"ANTH"
    },
    {
      "subject":"APHYS",
      "description":"Applied Physics",
      "unit":"ENGDEAN"
    },
    {
      "subject":"APPLS",
      "description":"Applied Language Studies",
      "unit":"REN"
    },
    {
      "subject":"ARBUS",
      "description":"Arts and Business",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"ARCH",
      "description":"Architecture",
      "unit":"ARCH"
    },
    {
      "subject":"ARCHL",
      "description":"Archeology (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"ART",
      "description":"Art",
      "unit":"FINE"
    },
    {
      "subject":"ARTS",
      "description":"Arts",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"ASIAN",
      "description":"Asian Studies",
      "unit":"REN"
    },
    {
      "subject":"ASTRN",
      "description":"Astronomy (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"AVIA",
      "description":"Aviation",
      "unit":"VPA"
    },
    {
      "subject":"BE",
      "description":"Business Entrepreneurship",
      "unit":"CBET"
    },
    {
      "subject":"BET",
      "description":"Business, Entrepreneurship and Technology",
      "unit":"CBET"
    },
    {
      "subject":"BIOL",
      "description":"Biology",
      "unit":"BIOL"
    },
    {
      "subject":"BME",
      "description":"Biomedical Engineering",
      "unit":"ENGDEAN"
    },
    {
      "subject":"BOT",
      "description":"Botany (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"BUS",
      "description":"Business",
      "unit":"MATHDEAN"
    },
    {
      "subject":"CCIV",
      "description":"Classical Civilization",
      "unit":"CLASSICS"
    },
    {
      "subject":"CDNST",
      "description":"Canadian Studies",
      "unit":"STP"
    },
    {
      "subject":"CEDEV",
      "description":"Children's Education & Development (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"CHE",
      "description":"Chemical Engineering",
      "unit":"CHE"
    },
    {
      "subject":"CHEM",
      "description":"Chemistry",
      "unit":"CHEM"
    },
    {
      "subject":"CHINA",
      "description":"Chinese",
      "unit":"REN"
    },
    {
      "subject":"CIVE",
      "description":"Civil Engineering",
      "unit":"CIVE"
    },
    {
      "subject":"CLAS",
      "description":"Classical Studies",
      "unit":"CLASSICS"
    },
    {
      "subject":"CM",
      "description":"Computational Mathematics",
      "unit":"MATHDEAN"
    },
    {
      "subject":"CMW",
      "description":"Church Music and Worship",
      "unit":"CGC"
    },
    {
      "subject":"CO",
      "description":"Combinatorics and Optimization",
      "unit":"CO"
    },
    {
      "subject":"COGSCI",
      "description":"Cognitive Science",
      "unit":"GRAD"
    },
    {
      "subject":"COMM",
      "description":"Commerce",
      "unit":"MATHDEAN"
    },
    {
      "subject":"COMPT",
      "description":"Computing (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"COMST",
      "description":"Communication Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"CONST",
      "description":"Contemporary Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"COOP",
      "description":"Co-op",
      "unit":"CECS"
    },
    {
      "subject":"CROAT",
      "description":"Croatian",
      "unit":"GERSLAV"
    },
    {
      "subject":"CS",
      "description":"Computer Science",
      "unit":"CS"
    },
    {
      "subject":"CT",
      "description":"Catholic Thought",
      "unit":"STJ"
    },
    {
      "subject":"CULMG",
      "description":"Cultural Management",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"CULT",
      "description":"Cultural Studies",
      "unit":"VPA"
    },
    {
      "subject":"DAC",
      "description":"Digital Arts Communication",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"DANCE",
      "description":"Dance",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"DEI",
      "description":"Digital Experience Innovation",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"DES",
      "description":"Design",
      "unit":"SYDE"
    },
    {
      "subject":"DEVIS",
      "description":"Development & International Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"DM",
      "description":"Design and Manufacturing",
      "unit":"ME"
    },
    {
      "subject":"DRAMA",
      "description":"Drama",
      "unit":"DRAMA"
    },
    {
      "subject":"DUTCH",
      "description":"Dutch",
      "unit":"GERSLAV"
    },
    {
      "subject":"EARTH",
      "description":"Earth Science",
      "unit":"EARTH"
    },
    {
      "subject":"EASIA",
      "description":"East Asian Studies",
      "unit":"REN"
    },
    {
      "subject":"EBUS",
      "description":"Environment and Business",
      "unit":"ENVDEAN"
    },
    {
      "subject":"ECE",
      "description":"Electrical and Computer Engineering",
      "unit":"ECE"
    },
    {
      "subject":"ECON",
      "description":"Economics",
      "unit":"ECON"
    },
    {
      "subject":"EFAS",
      "description":"English for Academic Success",
      "unit":"REN"
    },
    {
      "subject":"ELE",
      "description":"Electrical Engineering",
      "unit":"ECE"
    },
    {
      "subject":"ELPE",
      "description":"English Language Proficiency Examination",
      "unit":"VPA"
    },
    {
      "subject":"ENBUS",
      "description":"Environment and Business",
      "unit":"SEED"
    },
    {
      "subject":"ENGL",
      "description":"English",
      "unit":"ENGL"
    },
    {
      "subject":"ENVE",
      "description":"Environmental Engineering",
      "unit":"ENGDEAN"
    },
    {
      "subject":"ENVS",
      "description":"Environmental Studies",
      "unit":"ENVDEAN"
    },
    {
      "subject":"ERS",
      "description":"Environment and Resource Studies",
      "unit":"ERS"
    },
    {
      "subject":"ESL",
      "description":"English as a Second Language",
      "unit":"REN"
    },
    {
      "subject":"EVSY",
      "description":"Environment and Society",
      "unit":"VPA"
    },
    {
      "subject":"FILM",
      "description":"Film (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"FINAN",
      "description":"Finance",
      "unit":"ACC"
    },
    {
      "subject":"FINE",
      "description":"Fine Arts",
      "unit":"FINE"
    },
    {
      "subject":"FR",
      "description":"French Studies",
      "unit":"FR"
    },
    {
      "subject":"FRCS",
      "description":"French Cultural Studies",
      "unit":"FR"
    },
    {
      "subject":"GBDA",
      "description":"Global Business and Digital Arts",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"GEMCC",
      "description":"Geography and Environmental Mgmt, Climate Change",
      "unit":"GEOG"
    },
    {
      "subject":"GENE",
      "description":"General Engineering",
      "unit":"ENGDEAN"
    },
    {
      "subject":"GEOE",
      "description":"Geological Engineering",
      "unit":"CIVE"
    },
    {
      "subject":"GEOG",
      "description":"Geography",
      "unit":"GEOG"
    },
    {
      "subject":"GEOL",
      "description":"Geology (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"GER",
      "description":"German",
      "unit":"GERSLAV"
    },
    {
      "subject":"GERON",
      "description":"Gerontology",
      "unit":"HLTHGERON"
    },
    {
      "subject":"GGOV",
      "description":"Global Governance",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"GLOBAL",
      "description":"Global Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"GRAD",
      "description":"Continuing Graduate Studies",
      "unit":"GRADDEAN"
    },
    {
      "subject":"GRK",
      "description":"Greek",
      "unit":"CLASSICS"
    },
    {
      "subject":"GS",
      "description":"Graduate Studies",
      "unit":"GRADDEAN"
    },
    {
      "subject":"HEBRW",
      "description":"Hebrew (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"HIST",
      "description":"History",
      "unit":"HIST"
    },
    {
      "subject":"HLTH",
      "description":"Health Studies",
      "unit":"HLTHGERON"
    },
    {
      "subject":"HRCS",
      "description":"Human Relations & Counselling Studies",
      "unit":"PSYCH"
    },
    {
      "subject":"HRM",
      "description":"Human Resources Management",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"HS",
      "description":"High School",
      "unit":"VPA"
    },
    {
      "subject":"HSG",
      "description":"Health Studies and Gerontology",
      "unit":"HLTHGERON"
    },
    {
      "subject":"HUMSC",
      "description":"Human Sciences",
      "unit":"STJ"
    },
    {
      "subject":"HUNGN",
      "description":"Hungarian",
      "unit":"GERSLAV"
    },
    {
      "subject":"IFS",
      "description":"Inter-Faculty Studies",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"INDEV",
      "description":"International Development",
      "unit":"SEED"
    },
    {
      "subject":"INTEG",
      "description":"Integrated Studies",
      "unit":"ENVDEAN"
    },
    {
      "subject":"INTERN",
      "description":"Internship",
      "unit":"VPA"
    },
    {
      "subject":"INTST",
      "description":"International Studies",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"INTTS",
      "description":"International Trade Seminars",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"IS",
      "description":"Independent Studies",
      "unit":"IS"
    },
    {
      "subject":"ISS",
      "description":"Interdisciplinary Social Sciences",
      "unit":"REN"
    },
    {
      "subject":"ITAL",
      "description":"Italian",
      "unit":"STJ"
    },
    {
      "subject":"ITALST",
      "description":"Italian Studies",
      "unit":"STJ"
    },
    {
      "subject":"JAPAN",
      "description":"Japanese",
      "unit":"REN"
    },
    {
      "subject":"JS",
      "description":"Jewish Studies",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"KIN",
      "description":"Kinesiology",
      "unit":"KIN"
    },
    {
      "subject":"KOREA",
      "description":"Korean",
      "unit":"REN"
    },
    {
      "subject":"KPE",
      "description":"Kinesiology and Physical Education (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"LANG",
      "description":"Language (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"LAT",
      "description":"Latin",
      "unit":"CLASSICS"
    },
    {
      "subject":"LATAM",
      "description":"Latin American Studies",
      "unit":"SPAN"
    },
    {
      "subject":"LED",
      "description":"Local Economic Development",
      "unit":"ENVDEAN"
    },
    {
      "subject":"LS",
      "description":"Legal Studies",
      "unit":"SOC"
    },
    {
      "subject":"LSC",
      "description":"Legal Studies and Criminology",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"MATBUS",
      "description":"Mathematical Business",
      "unit":"MATHDEAN"
    },
    {
      "subject":"MATH",
      "description":"Mathematics",
      "unit":"MATHDEAN"
    },
    {
      "subject":"ME",
      "description":"Mechanical Engineering",
      "unit":"ME"
    },
    {
      "subject":"MEDST",
      "description":"Media Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"MEDVL",
      "description":"Medieval Studies",
      "unit":"CLASSICS"
    },
    {
      "subject":"MENV",
      "description":"Man Environment",
      "unit":"ERS"
    },
    {
      "subject":"MES",
      "description":"Middle Eastern Studies",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"MI",
      "description":"Mediterranean Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"MISC",
      "description":"Miscellaneous",
      "unit":"VPA"
    },
    {
      "subject":"MNS",
      "description":"Materials and Nano-Sciences",
      "unit":"CHEM"
    },
    {
      "subject":"MSCI",
      "description":"Management Sciences",
      "unit":"MSCI"
    },
    {
      "subject":"MSE",
      "description":"Management & Systems",
      "unit":"SYDE"
    },
    {
      "subject":"MTE",
      "description":"Mechatronics Engineering",
      "unit":"ME"
    },
    {
      "subject":"MTHEL",
      "description":"Mathematics Elective",
      "unit":"MATHDEAN"
    },
    {
      "subject":"MUSIC",
      "description":"Music",
      "unit":"CGC"
    },
    {
      "subject":"NANO",
      "description":"Nanotechnology",
      "unit":"GRAD"
    },
    {
      "subject":"NATST",
      "description":"Native Studies",
      "unit":"STP"
    },
    {
      "subject":"NE",
      "description":"Nanotechnology Engineering",
      "unit":"ENGDEAN"
    },
    {
      "subject":"NES",
      "description":"Near Eastern Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"OPTOM",
      "description":"Optometry",
      "unit":"OPTOM"
    },
    {
      "subject":"PACS",
      "description":"Peace and Conflict Studies",
      "unit":"CGC"
    },
    {
      "subject":"PAS",
      "description":"Personnel & Administration Studies",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"PD",
      "description":"Professional Development",
      "unit":"VPA"
    },
    {
      "subject":"PDARCH",
      "description":"Professional Development for Architecture Students",
      "unit":"ARCH"
    },
    {
      "subject":"PDENG",
      "description":"Professional Development for Engineering Students",
      "unit":"ENGDEAN"
    },
    {
      "subject":"PDPHRM",
      "description":"Professional Development for Pharmacy Students",
      "unit":"PHARM"
    },
    {
      "subject":"PED",
      "description":"Physical Education (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"PERST",
      "description":"Personnel Studies",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"PHARM",
      "description":"Pharmacy",
      "unit":"PHARM"
    },
    {
      "subject":"PHIL",
      "description":"Philosophy",
      "unit":"PHIL"
    },
    {
      "subject":"PHS",
      "description":"Public Health Sciences",
      "unit":"HLTHGERON"
    },
    {
      "subject":"PHYS",
      "description":"Physics",
      "unit":"PHYS"
    },
    {
      "subject":"PLAN",
      "description":"Planning",
      "unit":"PLAN"
    },
    {
      "subject":"PMATH",
      "description":"Pure Mathematics",
      "unit":"PMATH"
    },
    {
      "subject":"POLSH",
      "description":"Polish",
      "unit":"GERSLAV"
    },
    {
      "subject":"PORT",
      "description":"Portuguese",
      "unit":"SPAN"
    },
    {
      "subject":"PS",
      "description":"Public Serivce",
      "unit":"ARTSDEAN"
    },
    {
      "subject":"PSCI",
      "description":"Political Science",
      "unit":"PSCI"
    },
    {
      "subject":"PSYCH",
      "description":"Psychology",
      "unit":"PSYCH"
    },
    {
      "subject":"QIC",
      "description":"Quantum Information and Computation",
      "unit":"GRAD"
    },
    {
      "subject":"REC",
      "description":"Recreation and Leisure Studies",
      "unit":"REC"
    },
    {
      "subject":"REES",
      "description":"Russian and Eastern European Studies",
      "unit":"GERSLAV"
    },
    {
      "subject":"RELC",
      "description":"Religion & Culture (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"RS",
      "description":"Religious Studies",
      "unit":"RS"
    },
    {
      "subject":"RUSS",
      "description":"Russian",
      "unit":"GERSLAV"
    },
    {
      "subject":"SCBUS",
      "description":"Science and Business",
      "unit":"SCIDEAN"
    },
    {
      "subject":"SCI",
      "description":"Science",
      "unit":"SCIDEAN"
    },
    {
      "subject":"SDS",
      "description":"Social Development Studies",
      "unit":"REN"
    },
    {
      "subject":"SE",
      "description":"Software Engineering",
      "unit":"VPA"
    },
    {
      "subject":"SEQ",
      "description":"Co-op Sequence",
      "unit":"MATHDEAN"
    },
    {
      "subject":"SI",
      "description":"Studies in Islam",
      "unit":"REN"
    },
    {
      "subject":"SIPAR",
      "description":"Studies in Personality & Religion",
      "unit":"STP"
    },
    {
      "subject":"SMF",
      "description":"Sexuality, Marriage and the Family",
      "unit":"STJ"
    },
    {
      "subject":"SOC",
      "description":"Sociology",
      "unit":"SOC"
    },
    {
      "subject":"SOCIN",
      "description":"Social Innovation",
      "unit":"SEED"
    },
    {
      "subject":"SOCWK",
      "description":"Social Work (Social Development Studies)",
      "unit":"REN"
    },
    {
      "subject":"SOCWL",
      "description":"Social Welfare (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"SPAN",
      "description":"Spanish",
      "unit":"SPAN"
    },
    {
      "subject":"SPCOM",
      "description":"Speech Communication",
      "unit":"DRAMA"
    },
    {
      "subject":"SPD",
      "description":"Spirituality and Personal Development",
      "unit":"STP"
    },
    {
      "subject":"STAT",
      "description":"Statistics",
      "unit":"STATACTSC"
    },
    {
      "subject":"STV",
      "description":"Society, Technology and Values",
      "unit":"STV"
    },
    {
      "subject":"SUSM",
      "description":"Sustainability Management",
      "unit":"SEED"
    },
    {
      "subject":"SWK",
      "description":"Social Work",
      "unit":"AHSDEAN"
    },
    {
      "subject":"SWREN",
      "description":"Social Work (Bachelor of Social Work)",
      "unit":"REN"
    },
    {
      "subject":"SYDE",
      "description":"Systems Design Engineering",
      "unit":"SYDE"
    },
    {
      "subject":"TAX",
      "description":"Taxation",
      "unit":"ACC"
    },
    {
      "subject":"THTRE",
      "description":"Theatre (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"TN",
      "description":"Theoretical Neuroscience",
      "unit":"GRAD"
    },
    {
      "subject":"TOUR",
      "description":"Tourism",
      "unit":"ENVDEAN"
    },
    {
      "subject":"TPM",
      "description":"Technical Presentation Milestone",
      "unit":"ECE"
    },
    {
      "subject":"TPPE",
      "description":"Technical Presentation Proficiency Requirement",
      "unit":"ECE"
    },
    {
      "subject":"TS",
      "description":"Theological Studies",
      "unit":"CGC"
    },
    {
      "subject":"UKRAN",
      "description":"Ukrainian",
      "unit":"GERSLAV"
    },
    {
      "subject":"UN",
      "description":"Nuclear Engineering",
      "unit":"CIVE"
    },
    {
      "subject":"UNIV",
      "description":"University",
      "unit":"VPA"
    },
    {
      "subject":"URBAN",
      "description":"Urban Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"UU",
      "description":"University Interdisciplinary Studies (WLU)",
      "unit":"VPA"
    },
    {
      "subject":"VCULT",
      "description":"Visual Culture",
      "unit":"FINE"
    },
    {
      "subject":"WATER",
      "description":"Water",
      "unit":"GRAD"
    },
    {
      "subject":"WHMIS",
      "description":"Workplace Hazardous Materials Information Systems",
      "unit":"SCIDEAN"
    },
    {
      "subject":"WKRPT",
      "description":"Work-term Report",
      "unit":"CECS"
    },
    {
      "subject":"WS",
      "description":"Women's Studies",
      "unit":"WS"
    },
    {
      "subject":"ZOOL",
      "description":"Zoology (WLU)",
      "unit":"VPA"
    }
  ]
}
```


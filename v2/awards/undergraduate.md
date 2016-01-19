# Get all undergraduate awards and scholarships

```
GET /awards/undergraduate.{format}
```

## Description

> This method returns a a list of all undergraduate awards, bursaries and scholarships available to students

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
    <td>1759</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>awards</td>
    <td><b>Service ID</b></td>
    <td>317</td>
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

- Any value can be `null`


### Sources



## Parameters

```
GET /awards/undergraduate.{format}
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
GET /awards/undergraduate.{format}
```

- **https://api.uwaterloo.ca/v2/awards/undergraduate.json**
- **https://api.uwaterloo.ca/v2/awards/undergraduate.xml**
- **https://api.uwaterloo.ca/v2/awards/undergraduate.json?callback=myResponse**


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
    <td>Unique award id</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Award name</td>
  </tr>
  <tr>
    <td><b>status</b></td>
    <td>string</td>
    <td>Award status</td>
  </tr>
  <tr>
    <td><b>value</b></td>
    <td>string</td>
    <td>Award's monetary value</td>
  </tr>
  <tr>
    <td><b>type</b></td>
    <td>list</td>
    <td>Type of award (scholarship, bursary, etc)</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Award description and criteria</td>
  </tr>
  <tr>
    <td><b>citizenship</b></td>
    <td>list</td>
    <td>Citizenship requirements and eligibility for the award</td>
  </tr>
  <tr>
    <td><b>program</b></td>
    <td>list</td>
    <td>List of academic programs eligible for the award</td>
  </tr>
  <tr>
    <td><b>application</b></td>
    <td>object</td>
    <td>Application requirement object<br><table>
  <tr>
    <td><b>type</b></td>
    <td>list</td>
    <td>Clarification on how to apply (eg: automatically considered or application required)</td>
  </tr>
  <tr>
    <td><b>enrollment_year</b></td>
    <td>list</td>
    <td>Student's enrollment eligibility criteria</td>
  </tr>
  <tr>
    <td><b>eligibility</b></td>
    <td>list</td>
    <td>Award eligibility details</td>
  </tr>
  <tr>
    <td><b>instructions</b></td>
    <td>list</td>
    <td>Instructions on applying for the award</td>
  </tr>
  <tr>
    <td><b>additional</b></td>
    <td>list</td>
    <td>Additional information on the application process</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>deadlines</b></td>
    <td>object</td>
    <td>Award deadlines<br><table>
  <tr>
    <td><b>term</b></td>
    <td>list</td>
    <td>List of terms that the award is offered</td>
  </tr>
  <tr>
    <td><b>application</b></td>
    <td>list</td>
    <td>Application deadline for the given term</td>
  </tr>
  <tr>
    <td><b>extended</b></td>
    <td>date</td>
    <td>Any additional extended deadline (if applicable)</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>links</b></td>
    <td>list</td>
    <td>Additional links for more information</td>
  </tr>
  <tr>
    <td><b>contact</b></td>
    <td>string</td>
    <td>Contact information regarding the award and application</td>
  </tr>
  <tr>
    <td><b>vid</b></td>
    <td>integer</td>
    <td>Award description revision id</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>URL to the award page</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811387,
    "timestamp":1453150849,
    "status":200,
    "message":"Request successful",
    "method_id":1759,
    "method":{
      
    }
  },
  "data":[
    {
      "id":477,
      "title":"Drs. Wensveen and Smith Award in Binocular Vision and Perception",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $1,000, is presented annually to a full-time undergraduate student entering Year Three in the School of Optometry &amp; Vision Science in the Faculty of Science who has demonstrated a particular interest and aptitude in the area of binocular vision and perception. Candidates must have demonstrated academic achievement in related courses (minimum 70%).\u00a0 Interested students should apply by submitting a one-page essay at the completion of Year Two by June 15 of each year. This fund is made possible by a donation from Dr. Janice Wensveen (OD \u201983, University of Waterloo) and Dr. Earl L. Smith, III (OD \u201972, University of Houston). They are both professors from the University of Houston School of Optometry who are grateful for the careers that they have as a result of their optometry education and want to help support the next generation of optometrists.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Optometry",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Two"
        ],
        "eligibility":[
          "Minimum 70% average in related courses:"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form."
        ],
        "additional":[
          "Please attach a one-page essay describing your eligibility for this award. Applications are to be submitted at the completion of Year Two by June 15 to Barb Robinson, OPT 331."
        ]
      },
      "deadlines":{
        "term":[
          "June 15"
        ],
        "application":[
          "June 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact Barb Robinson if you have questions about this award.",
      "vid":3429,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/drs-wensveen-and-smith-award-binocular-vision-and-perception"
    },
    {
      "id":476,
      "title":"Ali Arts Entrepreneurship Award",
      "status":"Active",
      "value":"$2500",
      "type":[
        "Entrepreneurial awards",
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $2,500, is provided annually to a full-time undergraduate student enrolled in Year Two, Three, or Four in the Faculty of Arts. Selection will be made on the basis of academic achievement (minimum 75%) and demonstrated involvement in developing an entrepreneurial idea. Interested students should submit an application by October 1 and provide a minimum 250-word essay on the scope of the entrepreneurial activity and how the award will help in furthering the implementation of the business concept. This fund is made possible by a donation from alumnus Mr. Tanveer Ali, (BA, \u201909) who experienced firsthand how an Arts education can provide a solid foundation for success in the business world.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting and Financial Mgmt",
        "Anthropology",
        "Classical Studies",
        "Drama and Speech Communication",
        "Economics",
        "English Language and Literature",
        "Fine Arts",
        "French Studies",
        "Germanic and Slavic Studies",
        "Global Business and Digital Arts",
        "History",
        "Independent Studies",
        "International Trade Specialization",
        "Medieval Studies",
        "Music",
        "Peace and Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Religious Studies",
        "Russian and European Studies",
        "Sexuality",
        "Marriage and Family Studies",
        "Social Development Studies",
        "Sociology and Legal Studies",
        "Spanish and Latin American Studies",
        "Women&#039;s Studies",
        "Arts"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Year Two, Three, or Four in the Faculty of Arts",
          "Minimum 75% cumulative average",
          "Demonstrated involvement in developing an entrepreneurial idea"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria."
        ],
        "additional":[
          "Applicants must provide a minimum 250-word essay on the scope of the entrepreneurial activity and how the award will help in furthering the implementation of the business idea."
        ]
      },
      "deadlines":{
        "term":[
          "October 1"
        ],
        "application":[
          "October 1"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":null,
      "vid":3413,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/ali-arts-entrepreneurship-award"
    },
    {
      "id":474,
      "title":"WCGS International Opportunities Travel Grants (funded by the Fred and Ruth Stork Awards program)",
      "status":"Active",
      "value":"From $500 up to $1,500 each",
      "type":[
        "International experience awards"
      ],
      "description":"Several grants, valued from $500 to $1,500 each, are provided annually to full-time undergraduate or graduate students enrolled within the first four years of their program and registered in at least one Germanic and Slavic Studies course at the University of Waterloo. Selection will be based on participation in a recognized institutional Canadian-organized German language or cultural studies program abroad. Further information regarding the application process can be found at the Waterloo Centre for German Studies (WCGS) website. Applications are due February 1.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year One",
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Registered in at least one Germanic and Slavic course",
          "Selection is based on participation in a recognized institutional Canadian-organized German language or cultural studies program abroad"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "The application and further details can be found on the WCGS website."
        ]
      },
      "deadlines":{
        "term":[
          "February 1"
        ],
        "application":[
          "February 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/centre-for-german-studies\/scholarships\/fred-ruth-stork-awards-german-studies"
      ],
      "contact":"Please contact the Waterloo Centre for German Studies  for more information.",
      "vid":3441,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/wcgs-international-opportunities-travel-grants-funded-fred"
    },
    {
      "id":472,
      "title":"Drysdale International Experience Award",
      "status":"Active",
      "value":"Up to $2,500",
      "type":[
        "International experience awards"
      ],
      "description":"An award, valued up to $2,500, is available annually to a full-time undergraduate student enrolled in Year Two, Three, or Four in any Faculty, who is embarking on an international work, volunteer, or study experience related to academic requirements. Selection is on the basis of academic achievement (minimum 75%), and the location, duration, and type of international experience. Preference will be given to students with financial need who will be travelling to an unfamiliar country where they will experience a different culture in a new learning environment. Interested students should submit an application by November 15. This award is made possible by a generous donation from the Drysdale Family in recognition of their commitment to ongoing experiential education, international learning opportunities, and active global citizenship.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Full-time undergraduate student enrolled in Year Two, Three, or Four of any program\/Faculty",
          "Embarking on an international work, volunteer, or study experience related to academic requirements",
          "Selection based on academic achievement (minimum 75%), and the location, duration, and type of international experience",
          "Preference will be given to students with financial need who will be travelling to an unfamiliar country where they will experience a different culture in a new learning environment"
        ],
        "instructions":[
          "Complete the general International Experience Award Application form."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "November 15"
        ],
        "application":[
          "November 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3371,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/drysdale-international-experience-award"
    },
    {
      "id":470,
      "title":"McLenaghan International Study Abroad Award",
      "status":"Active",
      "value":"$1200",
      "type":[
        "International experience awards"
      ],
      "description":"An award, valued at up to $1,200, will be provided annually to a full-time undergraduate student who participates in an approved academic exchange or study-abroad term. Eligible candidates include: third-year students enrolled in a French Studies program travelling to France to study at the University of Nantes or other approved school; or third- and fourth-year students enrolled in a program in the Faculty of Mathematics, with preference to students in Applied Mathematics, studying at an approved school in the United Kingdom, Europe or the United States. Selection will be based on academic achievement (minimum 75% overall average) and a personal letter describing planned learning outcomes. Financial need may also be considered. Preference will be given to students who will be travelling to an unfamiliar country where they will experience a different culture in a new learning environment. Interested students should submit an application by July 15. This award is made possible by a donation from Dr. Helene McLenaghan (Language Instructor, French Studies) and Dr. Ray McLenaghan (Professor Emeritus, Applied Math), to encourage students to enhance their Waterloo studies with an international study experience.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident"
      ],
      "programs":[
        "Applied Mathematics",
        "French Studies",
        "Arts",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Full-time undergraduate student who participates in an approved academic exchange or study-abroad term",
          "Third-year students enrolled in a French Studies program travelling to France to study at the University of Nantes or other approved school or",
          "Third- and fourth-year students enrolled in a program in the Faculty of Mathematics, with preference to students in Applied Mathematics, studying at an approved school in the United Kingdom, Europe or the United States",
          "Based on academic achievement (minimum 75% overall average)",
          "Personal letter describing planned learning outcomes",
          "Financial need may also be considered\u00a0",
          "Preference given to students travelling to an unfamiliar country where they will experience a different culture in a new learning environment"
        ],
        "instructions":[
          "Complete the general International Experience Award Application form."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "July 15"
        ],
        "application":[
          "July 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3340,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/mclenaghan-international-study-abroad-award"
    },
    {
      "id":469,
      "title":"Cadesky Tax Award",
      "status":"Active",
      "value":"$2500",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $2,500, is provided annually to a full-time undergraduate student enrolled in Year Four in any program in the School of Accounting and Finance. Selection will be made on the basis of academic excellence in AFM 362 and 363 (tax courses) and extracurricular involvement including sports and\/or volunteer activities. Interested students should submit an application by October 1. This fund is made possible by a donation from Cadesky and Associates LLP \u2018Cadesky Tax.\u2019",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting and Financial Mgmt",
        "Biotechnology\/CPA",
        "Computing and Financial Mgmt",
        "Mathematics\/CPA",
        "Arts",
        "Mathematics",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Four"
        ],
        "eligibility":[
          "Enrolled in Year Four in any program in School of Accounting and Finance",
          "Minimum 80% average in AFM 362 and AFM 363",
          "Involvement in extracurricular activities"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "October 1"
        ],
        "application":[
          "October 1"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"",
      "vid":3327,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/cadesky-tax-award"
    },
    {
      "id":468,
      "title":"Dematic Scholarship for Excellence in Supply Chain Optimization",
      "status":"Active",
      "value":"$2500: \n\t\n\t\ttwo awards, valued at $2,500 each",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"Two scholarships valued at $2,500 each are provided annually to full-time undergraduate students enrolled in Year Three or Four of Management Sciences Engineering in the Faculty of Engineering on the basis of academic achievement (minimum 80% cumulative average) and demonstrated interest in the area of supply chain management or related optimization technologies. Preference will be given to students who can describe how they would use optimization and analytical tools and concepts to design solutions for global supply chain management. Interested students should submit an application by February 1. This fund is made possible by a donation from Dematic Corporation.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Management Sciences",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Minimum 80% overall average",
          "Demonstrated interest in the area of supply chain management or related optimization technologies",
          "Preference to students who can describe how they would use optimization and analytical tools and concepts to design solutions for global supply chain management"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria.",
          "A resume is also required."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 1"
        ],
        "application":[
          "February 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3317,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/dematic-scholarship-excellence-supply-chain-optimization"
    },
    {
      "id":467,
      "title":"Anish Chopra Excellence in Finance Scholarship",
      "status":"Active",
      "value":"$2500",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"One scholarship, valued at $2,500, will be presented annually to a full-time undergraduate student entering Year Four in any program in the School of Accounting and Finance. The successful candidate will have demonstrated academic excellence (cumulative average of 80% or greater) and show an interest in finance through work experience and\/or related activities, such as finance competitions or the SAF Student-run Investment Fund. This fund is made possible by a donation from Anish Chopra, MAcc \u201994.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting and Financial Mgmt",
        "Biotechnology\/CPA",
        "Computing and Financial Mgmt",
        "Mathematics\/CPA",
        "Arts",
        "Mathematics",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Four"
        ],
        "eligibility":[
          "Entering Year Four in any program in the SAF",
          "80% cumulative average or greater",
          "Must show an interest in Finance through work experience and\/or related activities"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria.",
          "A resume is also required."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "October 1"
        ],
        "application":[
          "October 1"
        ],
        "extended":"2015-10-26"
      },
      "links":[
        
      ],
      "contact":null,
      "vid":3323,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/anish-chopra-excellence-finance-scholarship"
    },
    {
      "id":465,
      "title":"M\u00e9tis Nation of Ontario Bursary",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Aboriginal student awards",
        "Financial need awards\/bursaries"
      ],
      "description":"Bursaries, valued at $1,000 or more, are awarded annually to full- or part-time undergraduate M\u00e9tis students from Ontario enrolled in any program of any year at the University of Waterloo who are in good academic standing and who have demonstrated financial need. Interested students must complete the Full-time Bursary\/Award Application or the Part-time Undergraduate Bursary Application by November 1. As well, candidates must self-identify as M\u00e9tis by completing a declaration form. This fund is made possible by a donation from the M\u00e9tis Nation of Ontario.",
      "citizenship":[
        "Canadian citizen"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year One",
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Full- or part-time undergraduate M\u00e9tis students from Ontario",
          "Enrolled in any program of any year at the University of Waterloo",
          "Must be in good academic standing",
          "Must have demonstrated financial need",
          "Candidates must self-identify as M\u00e9tis by completing a declaration form (see below)"
        ],
        "instructions":[
          "Complete a Bursary\/Award Application form."
        ],
        "additional":[
          "Eligible students must complete the M\u00e9tis Nation of Ontario Bursary Declaration Form, which can be found on our Forms Page under Specific Award Application Forms:"
        ]
      },
      "deadlines":{
        "term":[
          "November 1"
        ],
        "application":[
          "November 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3244,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/metis-nation-ontario-bursary"
    },
    {
      "id":463,
      "title":"Dan and Anik Colquhoun Award",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $2,000, is awarded annually to a full-time undergraduate student enrolled in Year Two or above in Computer Engineering\u00a0on the basis of a demonstrated personal or medical challenge that has been overcome and a significant grade increase between any two consecutive terms after 2B. Eligible students should submit an application by November 1. This fund is made possible by a donation from Daniel and Anik Colquhoun.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computer Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Demonstrate a personal or medical challenge that has been overcome",
          "Achieve a significant grade increase between any two consecutive terms after 2B"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "November 1"
        ],
        "application":[
          "November 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3202,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/dan-and-anik-colquhoun-award"
    },
    {
      "id":462,
      "title":"Grand House Award",
      "status":"Active",
      "value":"$3000",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $3,000, is provided annually to a full-time undergraduate student enrolled in any year at the School of Architecture in the Faculty of Engineering on the basis of interest and desire to live in a unique student residence. The Grand House is the only student residence in Cambridge that was designed and built by students for students. It presents a great opportunity for all students to interact with each other, learn more from each other, put their ideas to use, and build enthusiasm for architecture.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year One",
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Awarded on the basis of interest and desire to live in a unique student residence"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "June 15"
        ],
        "application":[
          "June 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/architecture\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Student Services Coordinator at the School of Architecture for information about the application process for this award.",
      "vid":3203,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/grand-house-award"
    },
    {
      "id":461,
      "title":"Rick Haldenby Rome Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "International experience awards"
      ],
      "description":"An award, valued at approximately $1,000 is awarded annually to a full-time undergraduate student in the School of Architecture in the Faculty of Engineering who is participating in the Rome program in their 4A fall term. Candidates must be in good academic standing and have a demonstrated financial need as determined by UW. To be considered, students must complete the general UW International Experience Award application.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Four"
        ],
        "eligibility":[
          "Participating in the Rome program in 4A (fall term)",
          "Good academic standing",
          "Financial need"
        ],
        "instructions":[
          "Complete the general International Experience Award Application form."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "July 15"
        ],
        "application":[
          "July 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3155,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/rick-haldenby-rome-award"
    },
    {
      "id":459,
      "title":"GHL Consultants 4th Year Fire Safety Award",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award valued at $2,000 is provided annually to a full-time undergraduate student enrolled in the 4th year undergraduate Fire Safety Engineering course in the Department of Mechanical and Mechatronics Engineering. Selection is based on academic achievement (minimum 80% cumulative average) and demonstrated interest in pursuing a career in the area of fire safety engineering. Interested students should submit an application by February 1st. This fund is made possible by a donation from GHL Consultants Ltd.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Mechanical Engineering",
        "Mechatronics Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Four"
        ],
        "eligibility":[
          "Minimum 80% overall average",
          "Must be enrolled in the 4th year undergraduate Fire Safety Engineering course (ME 567)",
          "Demonstrated interest in pursuing a career in the area of fire safety engineering"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria.",
          "A resume is also required."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 1"
        ],
        "application":[
          "February 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3132,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/ghl-consultants-4th-year-fire-safety-award"
    },
    {
      "id":455,
      "title":"Liberation Scholarship Program",
      "status":"Active",
      "value":"The scholarship comprises:One-off grant to cover international travel and initial costs for your stay in the Netherlands;Tuition fee exemption in the Netherlands;Support from your Dutch host university (housing, visa, etc);Membership of the Liberation Scholarship Program alumni network.",
      "type":[
        "International experience awards"
      ],
      "description":"The Liberation Scholarship Program offers 70 scholarships to highly motivated students from Canada who would like to study in the Netherlands for three to twelve months and become part of the long-standing historic ties between the two countries. To celebrate seventy years of liberation and honour the sacrifices Canadian soldiers made for our freedom, the Netherlands launches the Liberation Scholarship Program, as a token of lasting gratitude and friendship",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Two",
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "You have Canadian citizenship.",
          "You apply for a study period of between three and twelve months at one of the participating Dutch higher education institutions.",
          "Your study period in the Netherlands starts before September 1, 2016.",
          "You meet the specific requirements of the institution of your choice.",
          "You must apply directly to one of the participating Dutch higher education institutions before October 1, 2015."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Contact Waterloo International and\/or your Faculty exchange representative to find out about options for studying in the Netherlands.",
          "Apply for the Liberation Scholarship by October 1, 2015.\u00a0 More information about the requirements, the participating Dutch higher education institutions and the application process are available at www.studyinholland.nl\/liberationscholarship"
        ]
      },
      "deadlines":{
        "term":[
          "October 1"
        ],
        "application":[
          "October 1"
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.studyinholland.nl\/liberationscholarship"
      ],
      "contact":"www.studyinholland.nl\/liberationscholarship",
      "vid":3066,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/liberation-scholarship-program"
    },
    {
      "id":454,
      "title":"Gage-Babcock 4th Year Fire Safety Award",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $2,000, is provided annually to a full-time undergraduate student enrolled in the 4th year undergraduate Fire Safety Engineering course in the Department of Mechanical and Mechatronics Engineering. Selection is based on academic achievement (minimum 80% cumulative average) and demonstrated interest in pursuing a career in the area of fire safety engineering. This fund is made possible by a donation from Gage-Babcock &amp; Associates Ltd.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Mechanical Engineering",
        "Mechatronics Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Four"
        ],
        "eligibility":[
          "Minimum 80% overall average",
          "Must be enrolled in the 4th year undergraduate Fire Safety Engineering course (ME 567)",
          "Demonstrated interest in pursuing a career in the area of fire safety engineering"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria.",
          "A resume is also required."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 1"
        ],
        "application":[
          "February 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3058,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/gage-babcock-4th-year-fire-safety-award"
    },
    {
      "id":453,
      "title":"Jim Colvin Scholarship in Computing and Financial Management",
      "status":"Active",
      "value":"$1200",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"A scholarship, valued up to $1,200, will be awarded annually to a full-time undergraduate student enrolled in Year Three or Four of the Computing and Financial Management program. Selection is based on strong academic achievement (minimum overall average of 80%), and leadership abilities as demonstrated through involvement in extra-curricular activities. Interested students must apply by February 1. This fund is made possible by a donation from Jim Colvin, BMath \u201984 (Computer Science).",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computing and Financial Mgmt",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Three",
          "Year Four"
        ],
        "eligibility":[
          "Minimum cumulative average of 80%",
          "Demonstrated leadership abilities"
        ],
        "instructions":[
          "Complete the General Undergraduate Award Application form.",
          "Attach a letter explaining how you meet the award criteria.",
          "A resume is also required."
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 1"
        ],
        "application":[
          "February 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":3053,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/jim-colvin-scholarship-computing-and-financial-management"
    },
    {
      "id":452,
      "title":"Autodesk Canada Capstone Design Award",
      "status":"Active",
      "value":"$5000: The $5,000 award will be divided equally among the winning team members.",
      "type":[
        "Scholarships\/awards"
      ],
      "description":"An award, valued at $5,000, will be provided to an outstanding student group in any program in the Faculty of Engineering completing a Fourth-Year Capstone Design Project with a significant software component. The award will go to the project that, in the opinion of the judges, demonstrates an innovative and practical design solution to a problem. Interested groups must submit an application, available through the Faculty of Engineering website, to their departmental Capstone Coordinator and a faculty committee will make the final selection. All award funds will be divided equally among the winning team members. This fund is made possible by a donation from Autodesk Canada Inc.",
      "citizenship":[
        "Canadian citizen",
        "Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Biomedical Engineering",
        "Chemical Engineering",
        "Civil Engineering",
        "Computer Engineering",
        "Electrical Engineering",
        "Environmental Engineering",
        "Geological Engineering",
        "Management Sciences",
        "Mechanical Engineering",
        "Mechatronics Engineering",
        "Nanotechnology Engineering",
        "Software Engineering",
        "Systems Design Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Year Four"
        ],
        "eligibility":[
          "Selection based on Fourth-Year Capstone Design Project",
          "The project must have a significant software component"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Apply through the Faculty of Engineering - Autodesk Canada Capstone Design Award"
        ]
      },
      "deadlines":{
        "term":[
          "Varies"
        ],
        "application":[
          "Varies"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/engineering\/entrepreneurship\/capstone-design\/autodesk-canada-capstone-design-award"
      ],
      "contact":"More information is available through the Faculty of Engineering - Autodesk Canada Capstone Design Award",
      "vid":3043,
      "link":"https:\/\/uwaterloo.ca\/student-awards-financial-aid\/undergraduate-awards\/autodesk-canada-capstone-design-award"
    }
  ]
}
```


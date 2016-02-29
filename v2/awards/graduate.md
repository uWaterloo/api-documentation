# Get all graduate awards and scholarships

```
GET /awards/graduate.{format}
```

## Description

> This method returns a a list of all graduate awards, bursaries and scholarships available to students

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
    <td>1777</td>
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
GET /awards/graduate.{format}
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
GET /awards/graduate.{format}
```

- **https://api.uwaterloo.ca/v2/awards/graduate.json**
- **https://api.uwaterloo.ca/v2/awards/graduate.xml**
- **https://api.uwaterloo.ca/v2/awards/graduate.json?callback=myResponse**


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
    <td>Type of award (scholarship, bursary, grant etc)</td>
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
    "requests":811393,
    "timestamp":1453151064,
    "status":200,
    "message":"Request successful",
    "method_id":1777,
    "method":{
      
    }
  },
  "data":[
    {
      "id":1270,
      "title":"AWARD   Faculty of Applied Health Sciences Teaching Assistant Awards-School of Public Health &amp; Health Systems",
      "status":"Active",
      "value":"$500: Two awards per year, each valued at $500",
      "type":[
        "Scholarships"
      ],
      "description":"Two awards per year, each valued at $500, will be offered to TAs within the School of Public Health &amp; Health Systems.\u00a0 Nominations are to be submitted electronically to the SPHHS TA Award web site https:\/\/uwaterloo.ca\/public-health-and-health-systems\/teaching-research\/teaching-assistant-excellence-award.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Demonstrates\u00a0a strong commitment to the overall learning, academic and personal growth of students;",
          "Exhibits\u00a0excellent \u00a0communication skills;",
          "Provides\u00a0thorough feedback on course work and assignments;",
          "Responds to students in a timely manner;",
          "Presents and discusses\u00a0course material with intellectual rigour, enthusiasm and integrity;",
          "Has a notable, positive influence on students;",
          "Shows sensitivity to the needs of students; and",
          "Demonstrates\u00a0high-quality teaching and facilitation of student learning, e.g., in tutorials or in one-on-one meetings with students.",
          "Any current graduate student in school of Public Health and Health Systems who serves, or has served, as a Teaching Assistant for at least one course within the September to August academic year is eligible.",
          "Nominations may come from instructors, students, and other teaching assistants.\u00a0 A SPHHS \u00a0\u00a0\u00a0award committee comprised of professors and graduate students will choose the winning TAs based on the students meeting at least two of the following criteria:\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Each recipient of the $500 award and plaque will be asked to address the AHS Graduate Teaching Assistant Training Day."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/public-health-and-health-systems\/teaching-research\/teaching-assistant-excellence-award"
      ],
      "contact":"For information contact the School of Public Health &amp; Health Systems Graduate Coordinator",
      "vid":10928,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/faculty-applied-health-sciences-teaching-assistant-awards-1"
    },
    {
      "id":1269,
      "title":"Faculty of Applied Health Sciences Teaching Assistant Awards-Department of Recreation and Leisure Studies",
      "status":"Active",
      "value":"$500: Two awards per year, each valued at $500",
      "type":[
        "Scholarships"
      ],
      "description":"Two awards per year, each valued at $500, will be offered to TAs within Recreation and Leisure Studies. Nominations can be submitted at any time during the year to the Associate Chair, Graduate Studies in the Department of Recreation and Leisure Studies. Those received by August 20 will be considered for the previous academic year. Recipients will be notified by the Faculty shortly after the selection is made.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Demonstrates\u00a0a strong commitment to the overall learning, academic and personal growth of students;",
          "Exhibits\u00a0clear communication skills during tutorials and office hours;",
          "Responds\u00a0to emails in a timely manner;",
          "Provides\u00a0thorough feedback on assignments;",
          "Discusses\u00a0course material with intellectual rigour, enthusiasm and integrity;",
          "Has\u00a0a favourable and significant influence on students;",
          "Shows\u00a0sensitivity to the needs of students; and",
          "Demonstrates\u00a0high-quality teaching and student learning, either in tutorials or in one-on-one meetings with students.",
          "Any current graduate student in Department of Recreation and Leisure Studies who serves, or has served, as a Teaching Assistant for at least one course within the September to August calendar year is eligible.",
          "Nominations may come from instructors, students, and other teaching assistants. If not nominated by the course instructor, a support letter from him\/her is encouraged. A Recreation and Leisure Studies award committee comprised of professors and graduate students will choose the winning TAs based on the students meeting at least two of the following criteria:\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Each recipient of the $500 award and plaque will be asked to address the AHS Graduate Teaching Assistant Training Day."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"For more information contact the Recreation and Leisure Studies Graduate Department Coordinator.",
      "vid":10927,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/faculty-applied-health-sciences-teaching-assistant-awards-0"
    },
    {
      "id":1268,
      "title":"Faculty of Applied Health Sciences Teaching Assistant Awards-Department of Kinesiology",
      "status":"Active",
      "value":"$500: Two awards per year, each valued at $500",
      "type":[
        "Scholarships"
      ],
      "description":"Two awards per year, each valued at $500, will be offered to TAs within Kinesiology. Nominations will be submitted to the Associate Chair, Graduate Studies Department of Kinesiology by August 1 for the previous calendar year. Recipients will be notified by the Faculty shortly after the selection is made, announced at the AHS Grad TA Training Day, and at a Fall Faculty Council Meeting.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Kinesiology"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Demonstrates\u00a0a strong commitment to the overall learning, academic and personal growth of students;",
          "Exhibits\u00a0excellent \u00a0communication skills;",
          "Provides\u00a0thorough feedback on course work and assignments;",
          "Presents and discusses\u00a0course material with intellectual rigour, enthusiasm and integrity;",
          "Demonstrates\u00a0high-quality teaching and responsiveness to student learning, e.g., in tutorials, labs or in one-on-one meetings with students.",
          "Any current graduate student in Department of Kinesiology who serves, or has served, as a Teaching Assistant for at least one course within the September to August academic year is eligible.",
          "Nominations may come from instructors, students, and other teaching assistants.\u00a0 A Kinesiology \u00a0\u00a0\u00a0award committee comprised of professors and graduate students will choose the winning TAs based on the students meeting at least two of the following criteria:\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Each recipient of the $500 award and plaque will be asked to address the AHS Graduate Teaching Assistant Training Day."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"For information contact the Kinesiology Graduate Department Coordinator.",
      "vid":10926,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/faculty-applied-health-sciences-teaching-assistant-awards"
    },
    {
      "id":1266,
      "title":"African Institute for Mathematical Sciences (AIMS) Entrance Scholarship",
      "status":"Active",
      "value":"$20000: $10,000 per year for 2 years",
      "type":[
        "Scholarships"
      ],
      "description":"Up to two AIMS Entrance Scholarships valued at $10,000\/year for up to two years will be awarded annually to students completing their Bachelor's or Master's degree at the African Institute of Mathematical Sciences. Recipients will be selected on the basis of scholastic excellence and a demonstrated interest in research. Scholarships will be awarded primarily to students entering a doctoral program in the Faculty of Mathematics.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Completed or expect to complete in the next year a Bachelor's or Master's degree form AIMS",
          "Applied to the MMath or PhD program in the Faculty of Math",
          "Minimum 80% cumulative GPA (in most recently completed program)",
          "Recipients can concurrently hold other awards"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"For more information contact your Department Graduate Coordinator.",
      "vid":10898,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/african-institute-mathematical-sciences-aims-entrance"
    },
    {
      "id":1252,
      "title":"Hira and Kamal Ahuja Graduate Engineering Award",
      "status":"Active",
      "value":"$6000: The value and\/or number of Awards may change from year to year.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"An award, valued up to $6,000 will be awarded annually to a graduate student registered full-time in a Master\u2019s or Doctoral program in the Faculty of Engineering.Students must be in good academic standing with demonstrated financial need as determined by UW. To be considered, students must complete the Graduate Student Award Application available from the Graduate Studies Office website and demonstrate their cultural contributions to the Indian community. This fund is made possible by a donation from Professor Hira Ahuja, a Waterloo Engineering alumnus to encourage students to pursue graduate studies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Students must be Ontario residents (as defined by OSAP) and must adhere to Ontario Trust for Student Support (OTSS) program guidelines.",
          "Selection will be based on Financial Need."
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          "Applicants must demonstrate their cultural contribution to the Indian community in the personal letter portion of their application."
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
        "https:\/\/uwaterloo.ca\/engineering\/about\/people"
      ],
      "contact":"Contact the Manager, Faculty fo Engineering Graduate Office for further details.",
      "vid":10691,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/hira-and-kamal-ahuja-graduate-engineering-award"
    },
    {
      "id":1249,
      "title":"Cindy Ditner Award in Public Accounting",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships"
      ],
      "description":"An award, valued at approximately $1,500 will be awarded annually to a full-time graduate student registered in the Master\u2019s of Accounting program in the School of Accounting and Finance in the Faculty of Arts. To be considered, students must complete an application form including a statement demonstrating an interest in pursuing a career in public accounting (specifically in the area of assurance and\/or accounting) and demonstrate their involvement in extracurricular activities. Recipients are selected annually in March by the School of Accounting and Finance.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Full-time graduate students registered in the Master\u2019s of Accounting (MAcc) program in the School of Accounting and Finance (SAF) in the Faculty of Arts",
          "Strong preference will be given to a student interested in pursuing a career in public practice in the area of assurance and\/or accounting and who is registered in the MAcc equivalents of the CPA Professional Education Program Assurance and Tax Electives (ACC 650 and ACC 607 respectively at the time of writing).",
          "Preference will be given to applicants who can demonstrate extracurricular involvement such as volunteer activities and\/or sports"
        ],
        "instructions":[
          "Award\/bursary application:",
          "Letter explaining how you meet the award criteria",
          "Resume required"
        ],
        "additional":[
          "In addition to the application include a cover letter outlining why the student feels they are a candidate for the scholarship, extracurricular involvement, and interest in a career in public accounting (specifically in the assurance and\/or accounting area); a resume; and a copy of a recent grade report.\u00a0"
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
        
      ],
      "contact":"Contact the School of Accounting and Finance Graduate Coordinator for further information.",
      "vid":10860,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/cindy-ditner-award-public-accoutning"
    },
    {
      "id":1243,
      "title":"Canadian Institutes of Health Research (CIHR) Doctoral Awards",
      "status":"Active",
      "value":"The maximum amount per award is $35,000 for up to one year. This funding is non-renewable",
      "type":[
        "Scholarships"
      ],
      "description":"The CIHR Doctoral Research Awards consist of two programs administered through a single application:\n\nThe Frederick Banting and Charles Best Canada Graduate Scholarships Doctoral Awards (CGS-D) program provides special recognition and support to students who are pursuing a doctoral degree in a health-related field in Canada.\n\n\t\tSome Canada Graduate Scholarship recipients may be considered for the honour of having their scholarship named a \u201cCanada Graduate Scholarship to Honour Nelson Mandela\u201d, should CIHR deem their application to be aligned with at least one of five themes championed by Mandela: national unity; democracy; freedom and human rights; leadership; children\u2019s participation in society; and children\u2019s health.\n\t\t\n\tThe Doctoral Foreign Study Award (DFSA) provides special recognition and support to students who are pursuing a doctoral degree in a health-related field abroad.\nApplicants apply to the CIHR Doctoral Research Awards competition and top-ranked applicants are awarded a CGS-D or DFSA depending on the proposed location where the doctoral degree will be pursued and granted. Note: Changes from proposed location from Canada to abroad or the opposite will not be considered by CIHR.\n\nAll applicants are expected to have an exceptionally high potential for future research achievement and productivity.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Eligibility and Selection Criteria please visit our CIHR Dcotoral webpage."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Applicants submit their application through ResearchNet by the agency deadline."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.sshrc-crsh.gc.ca\/funding-financement\/programs-programmes\/fellowships\/cgs_mandela-besc_mandela-eng.aspx",
        "https:\/\/uwaterloo.ca\/graduate-studies\/awards-funding\/external-awards\/canadian-institutes-health-research-cihr-doctoral-research",
        "https:\/\/uwaterloo.ca\/graduate-studies\/awards-funding\/external-awards\/tri-agency-cihr-nserc-sshrc-canada-graduate-scholarships"
      ],
      "contact":"For further information on applying visit our CIHR Dcotoral webpage.",
      "vid":10577,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/canadian-institutes-health-research-cihr-doctoral-awards"
    },
    {
      "id":1242,
      "title":"Devani Charities Graduate Engineering Enrance Scholarship",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships",
        "Entrance awards"
      ],
      "description":"A scholarship values at $1,500 will be awarded annually to a graduate student registered full-time in the first year of a thesis-based Master's program in the Faulty of Engineering. The scholarship will be awarded on the basis of scholastic excellence (minimum 1st class cumulative average required in the last program completed). Preference will be given to International student who previously received a formal education in India. The Faulty of Engineering will identify candidates and select recipients each Fall. A scholarship application is not required. This fund is made possible by a donation from Devani Charities in memory of Pradeep Anand, MASc 1974 Electrical Engineering alumnus.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Contact your Engineering Department Graduate Coordinator for more information.",
      "vid":10563,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/devani-charities-graduate-engineering-enrance-scholarship"
    },
    {
      "id":1241,
      "title":"G.A. Paper International Graduate Scholarship",
      "status":"Active",
      "value":"$5000: To be paid (normally) as the matching portion of an OGS or a QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $5,000 will be awarded annually to a full-time UW Master's or Doctoral student registered in the Chemical Engineering program in the Faulty fo Engineering. The scholarship will be awarded to a graduate student on the basis of scholastic excellence (minimum 80%). Preference will be given to a student who holds an Ontario Graduate Scholarship (OGS) or other major external scholarship that requires a matching or enhancement component. If the match or enhancement becomes unavailable or a suitable recipient cannot be found, the funds will be paid out as a regular gradate scholarship. This scholarship has been established by Dr. Ibrahim Elgammal, the President of G.A. Paper International and a Waterloo Engineering alumnus to honour his and his son Tarek's time at Waterloo and to encourage students to pursue graduate studies.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Chemical Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The Faculty fo Engineering will identify candidates and normally select recipients in the Spring term."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Contact your Chemical Engineering Department Graduate Coordinator for further information.",
      "vid":10562,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ga-paper-international-graduate-scholarship"
    },
    {
      "id":1235,
      "title":"Faculty of Arts Departmental Graduate Scholarship",
      "status":"Active",
      "value":"Value varies between $500-$9,000",
      "type":[
        "Scholarships"
      ],
      "description":"The Faculty of Arts Departmental Graduate Scholarships have been established to administer graduate student funding contributions received as part of the graduate funding package in Arts. Students must be registered full-time in a master's or doctoral program in the Faculty of Arts. Eligible students must have a minimum of 80% cumulative average in their current program or over the last two full-time academic years and be within the time limits of their program. Students must not concurrently hold a major scholarship such as OGS, CIHR, NSERC or SSHRC. These scholarships are automatically awarded by the department and Faculty and are normally awarded at the beginning of each term.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Anthropology (Public issues)",
        "Arts",
        "Classical Studies",
        "Digital Experience Innovation",
        "Economics",
        "English",
        "Fine Arts",
        "French Studies",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Contact your Faulty of Arts Department Graduate Coordinator for further information.",
      "vid":10251,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/faculty-arts-departmental-graduate-scholarship"
    },
    {
      "id":1196,
      "title":"Student Life Centre Management Board Bursary",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"A bursary fund established by the Student Life Centre Management Board (formerly Campus Centre Board) is available to graduate and undergraduate students experiencing financial difficulties.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Accounting",
        "Applied Health Science",
        "Applied Mathematics",
        "Architecture",
        "Biology",
        "Catholic Thought",
        "Environment &amp; Business",
        "Health Studies\/Gerontology",
        "Anthropology (Public issues)",
        "Arts",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "MBET",
        "Theological Studies",
        "Chemical Engineering",
        "Classical Studies",
        "Computational Mathematics",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Public Health",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Digital Experience Innovation",
        "Environment",
        "Pharmacy",
        "Planning",
        "Recreation &amp; Leisure Studies",
        "Economics",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Mathematics for Teachers",
        "Physics",
        "Social Innovation",
        "English",
        "Management Sciences",
        "Physics and Astronomy",
        "Pure Mathematics",
        "Science",
        "Fine Arts",
        "Mechanical &amp; Mechatronics Eng",
        "Quantitative Finance",
        "Theology",
        "Vision Science",
        "French Studies",
        "Statistics &amp; Actuarial Science",
        "Systems Design Engineering",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the SAFA office for further information.",
      "vid":10035,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/student-life-centre-management-board-bursary"
    },
    {
      "id":1194,
      "title":"Paul Niessen-Teck Award",
      "status":"Active",
      "value":"$1500: Medal plus $1,500",
      "type":[
        "Medals"
      ],
      "description":"This award is in memory of Professor Paul Niessen, a distinguished member of the Department of Mechanical Engineering who had a long association with Cominco Ltd. This award, consisting of a medal and $1,500 is awarded annually to one or two students who demonstrate leadership and skill in the Materials Science and Manufacturing Laboratories of the Department. Candidates should be enrolled in a Mechanical Engineering graduate program in the year preceding the award. Nominations should be submitted to the Chair of Mechanical Engineering in January of each year.\n\n\n\t\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Scholarship Coordinator for further information regarding this award.",
      "vid":10564,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/paul-niessen-teck-award"
    },
    {
      "id":1193,
      "title":"Angus Kerr-Lawson Essay Prize in Philosophy",
      "status":"Active",
      "value":"$200",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $200 will be awarded annually to a full-time graduate or undergraduate student enrolled in any program at the University of Waterloo who has submitted the best essay in American philosophy or philosophical naturalism, with a preference for essays bearing on the work of Jorge Santayana. \u00a0Decisions will be made based on Professors' submissions of student essays drawn from University of Waterloo courses, research areas or dissertations that the professors teach or supervise by each winter term.\u00a0 This fund is made possible by a donation from the Hall and Kerr-Lawson families in memory of Agus Kerr-Lawson.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Philosophy"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact the Philosophy Department Graduate Coordinator for further information regarding this award.",
      "vid":10032,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/angus-kerr-lawson-essay-prize-philosophy"
    },
    {
      "id":1192,
      "title":"Perimeter Institute PhD Award",
      "status":"Active",
      "value":"$20000: The goal is to provide each PhD student who is normally resident at PI and who is supervised by a faculty member at PI, an award valued at up to $7,000 payable across 3 terms to ensure the net amount each student receives after tuition and fees is $20,000.",
      "type":[
        "Scholarships"
      ],
      "description":"Waterloo PhD students who have completed the Perimeter Scholars International program (or equivalent), have secured a faculty member at Perimeter Institute as a supervisor, and who will be resident at PI, are eligible for the Perimeter Institute PhD Award.\u00a0 The department of Physics &amp; Astronomy will consult with PI in the selection of recipients.\u00a0 The award value varies depending on tuition costs and other awards and funding received by the student.\u00a0 The goal is to ensure that all students receive total annual funding, including the PI PhD award, of $20,000 after tuition and fees.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Physics",
        "Physics and Astronomy",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Physics Department Scholarship Coordinator for further information regarding this award.",
      "vid":10031,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/perimeter-institute-phd-award"
    },
    {
      "id":1191,
      "title":"Ping Yang Memorial Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $5,000 will be awarded annually to a full-time graduate student registered in the Master\u2019s or Doctoral program in the Department of Applied Mathematics in the Faculty of Mathematics who is conducting research in Mathematical Oncology.\u00a0 Selection will be made on the basis of academic excellence (minimum 80%).\u00a0 This fund is made possible by donations from friends and family to honour Ping Yang, the late wife of Barry Henderson BMATH, \u201969.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the Applied Mathematics Department Graduate Coordinator for further information regarding this award.",
      "vid":10030,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ping-yang-memorial-graduate-scholarship"
    },
    {
      "id":1190,
      "title":"AECOM Graduate Scholarship in Water Research",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"Two Scholarships, valued at $5,000 each, will be awarded to full-time University of Waterloo graduate students. One scholarship will be awarded to a student in the Faculty of Science and the other will be awarded to a student in the Faculty of Engineering. The scholarship will be awarded on the basis of scholastic excellence and demonstrated success in water research. This scholarship is generously supported by AECOM.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Biology",
        "Chemistry",
        "MBET",
        "Chemical Engineering",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Pharmacy",
        "Electrical &amp; Computer Eng",
        "Physics",
        "Management Sciences",
        "Physics and Astronomy",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Vision Science",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Complete the Water Institute graduate scholarships application form found on our forms webpage and submit to the Water Institute."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/water.uwaterloo.ca\/graduate-studies\/water.uwaterloo.ca\/"
      ],
      "contact":"Please contact Water Institute for further information regarding this award.",
      "vid":10566,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/aecom-graduate-scholarship-water-research"
    },
    {
      "id":1189,
      "title":"The Bartholomew Entrepreneurship Scholarship",
      "status":"Active",
      "value":"$25000: The value of the award will be $12,500 annually. The donor\u2019s contributions of $12,500 will be matched each year by the Faculty of Engineering.",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $25,000 is awarded annually to a full-time graduate student enrolled in first year of the MBET program in the Conrad Business, Entrepreneurship, and Technology Centre in the Faculty of Engineering on the basis of academic achievement\/excellence (minimum 80%) and strong entrepreneurial background, and a well presented business opportunity as outlined in a business plan\/case. Interested students should submit an application by May 31st.This fund is made possible by a donation from Gary R. Bartholomew, matched by the faculty of Engineering.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "This scholarship will be awarded based on the submission of a mini business plan."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the CBET Department Scholarship Coordinator for further information regarding this award.",
      "vid":10028,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/bartholomew-entrepreneurship-scholarship"
    },
    {
      "id":1188,
      "title":"Murray Martin Prize for the Best Research Paper by a Mathematics Graduate Student",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"A prize, valued at $5,000, is presented annually to a graduate student or team of students enrolled in the Faculty of Mathematics who has authored or co-authored an outstanding research paper as of January 31st each year. Students must be nominated by their supervisor. This fund is made possible by a donation from Pitney Bowes Inc. to honour Dr. Murray martin, their retired Chair, President, C.E.O. and Director whose continuous investment in research and development has ensured its industry leadership.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Mathematics Department Scholarship Coordinator for further information regarding this award.",
      "vid":10027,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/murray-martin-prize-best-research-paper-mathematics-graduate"
    },
    {
      "id":1187,
      "title":"University of Waterloo - China Graduate Scholarship",
      "status":"Active",
      "value":"Up to $30,000 for Master\u2019s and $21,000 for Doctoral students. 2 awards per year",
      "type":[
        "Scholarships"
      ],
      "description":"Two scholarships will be awarded annually to graduate students who have valid Canadian study permits at the University of Waterloo and who have been living in China prior to being admitted to the graduate program at the University of Waterloo. Scholarships will be valued at $30,000 per year for up to two years (6 terms) for Master's students and $21,000 per year for up to three years (9 terms) for Doctoral students. Preference will be given to students who received a previous degree from Tsinghua University or the other excellent Chinese Universities identified by the University of Waterloo and nominators prior to being admitted into a full time master's or doctoral program at Waterloo. The candidates will be recommended by Professor Emeritus Andrew Wong (the nominator) to the Associate Chair of Graduate Studies for Systems Design. The scholarship will be awarded on the basis of scholastic excellence and statement of interest as determined by their application for admission to their graduate program at Waterloo.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Anthropology (Public issues)",
        "Arts",
        "Engineering",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the Systems Design Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":10026,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/university-waterloo-china-graduate-scholarship"
    },
    {
      "id":1186,
      "title":"Lijiang Fang Graduate Scholarship in Computer Science",
      "status":"Active",
      "value":"$5000: Up to two scholarships valued at $5,000 each.",
      "type":[
        "Scholarships"
      ],
      "description":"Up to two scholarships valued at $5,000 each are awarded annually to full-time graduate students enrolled in Year One of the Masters (thesis option) or Doctoral program in the Cheriton School of Computer Science in the Faculty of Mathematics on the basis of academic excellence (minimum 80% cumulative average).\u00a0 This scholarship has been established to help the Cheriton School of Computer Science in the Faculty of Mathematics continue to attract top students world-wide. This fund is made possible by a donation from Microsoft in honour of Lijiang Fang, BMath and MMath whose work along with his team at his company awarded him with an Outstanding Technical Achievement Award from Microsoft.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your David R. Cheriton School of Computer Science Graduate Coordinator for further information regarding this award.",
      "vid":10025,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/lijiang-fang-graduate-scholarship-computer-science"
    },
    {
      "id":1185,
      "title":"Energy Council of Canada Energy Policy Research Fellowship",
      "status":"Active",
      "value":"Up to $15,000 for Master's students and up to $25,000 for Doctoral students.",
      "type":[
        "Scholarships"
      ],
      "description":"Annual fellowships valued at up to $15000 for Master's students and\u00a0 up to $25,000 for Doctoral students will be awarded to eligible full-time graduate students registered at the University of Waterloo.\u00a0 Students must demonstrate interest in energy policy research and more specifically be conducting research consistent with the identified Energy Policy Research Topic(s) defined annually by the Waterloo Institute for Sustatinble Energy (WISE) in conjunction with the Energy Council of Canada (ECC).\u00a0 Selection will also be based on academic excellence (minimum cumulative average of 80%).\u00a0 Current and prospective students interested in applying for this fellowship must complete the application found at the WISE website.\u00a0 A Selection Committee will review the applications and select recipients by April.\u00a0 This fund is made possible by a donation from the Energy Council of Canada.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Environment &amp; Business",
        "Chemistry",
        "Environment &amp; Resource Studies",
        "MBET",
        "Chemical Engineering",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Civil &amp; Environmental Eng",
        "Environment",
        "Pharmacy",
        "Planning",
        "Electrical &amp; Computer Eng",
        "Physics",
        "Social Innovation",
        "Management Sciences",
        "Physics and Astronomy",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          "Complete the application found on the WISE website."
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
        "https:\/\/wise.uwaterloo.ca\/contact\/staff1"
      ],
      "contact":"Please contact\u00a0 the WISE Administrative Assistant for further information about this award.",
      "vid":10565,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/energy-council-canada-energy-policy-research-fellowship"
    },
    {
      "id":1184,
      "title":"RBC Water Scholars Graduate Entrance Scholarship",
      "status":"Active",
      "value":"$5000 for Master's students and $10,000 for Doctoral students",
      "type":[
        "Entrance awards"
      ],
      "description":"Entrance scholarships, valued at $5,000 for Master\u2019s students and $10,000 for Doctoral students, will be awarded annually to full-time graduate students registered at the University of Waterloo who are conducting research in water and are registered in the collaborative Integrated Water Management Program.Recipients will be selected based on their commitment to a water-focused program of study and academic excellence (minimum 80% average in each of the last two years of full-time academic study).\u00a0 This fund is made possible by a donation from the Royal Bank Financial Group to support and facilitate excellence in integrated water management.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Biology",
        "Arts",
        "Environment &amp; Resource Studies",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Civil &amp; Environmental Eng",
        "Environment",
        "Economics",
        "Mathematics",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10023,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rbc-water-scholars-graduate-entrance-scholarship"
    },
    {
      "id":1200,
      "title":"Women&#039;s Health Scholars Award",
      "status":"Active",
      "value":"\u25feMaster\u2019s Awards - $18,000 plus $1,000 research allowance\n\u25feDoctoral Awards - $20,0000 plus $2,000 research allowance\n\u25fePostdoctoral Award - $40,000 plus $5,000 research allowance",
      "type":[
        "Scholarships"
      ],
      "description":"The Ontario Women\u2019s Health Scholars Award is administered by the Ontario Council of Graduate Studies (OCGS) on behalf of Ontario government ministries. It is open to Master\u2019s students, Doctoral students, and Post Doctoral Fellows. Funded by the Ontario Ministry of Health and Long-Term Care, a Scholar Awards Program in Women's Health has been established to ensure that Ontario attracts and retains pre-eminent women's health\n\tscholars. The community of women's health scholars fostered by this Awards program will excel, according to internationally accepted standards of scientific excellence, in the creation of new knowledge about women's health and its translation into improved health for women, more effective health services and products for women, and a strengthened health care system.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Accounting",
        "Applied Health Science",
        "Applied Mathematics",
        "Architecture",
        "Biology",
        "Catholic Thought",
        "Environment &amp; Business",
        "Health Studies\/Gerontology",
        "Anthropology (Public issues)",
        "Arts",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "MBET",
        "Theological Studies",
        "Chemical Engineering",
        "Classical Studies",
        "Computational Mathematics",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Public Health",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Digital Experience Innovation",
        "Environment",
        "Pharmacy",
        "Planning",
        "Recreation &amp; Leisure Studies",
        "Economics",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Mathematics for Teachers",
        "Physics",
        "Social Innovation",
        "English",
        "Management Sciences",
        "Physics and Astronomy",
        "Pure Mathematics",
        "Science",
        "Fine Arts",
        "Mechanical &amp; Mechatronics Eng",
        "Quantitative Finance",
        "Theology",
        "Vision Science",
        "French Studies",
        "Statistics &amp; Actuarial Science",
        "Systems Design Engineering",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "To be eligible for a Postdoctoral Award, applicants must be engaged in full-time research at an Ontario university at the time of taking up the award (i.e., September 1, 2013), and must have completed all requirements for the doctoral degree by the application deadline (i.e., January 30, 2013) and within 36 months of the application deadline (i.e., no earlier than January 31, 2010). If a longer period of time has passed, for example for child rearing, applicants must submit a rationale for the delay in application.",
          "Holders of Women's Health Scholars are precluded from holding any other major award during the term of this award.",
          "Any publication of any kind, written or oral, related to the research undertaken by the successful applicants contain an acknowledgement of the Ontario Ministry of Health and Long Term Care\u2019s role in supporting the Project as follows:",
          "To be eligible for a Master\u2019s or Doctoral Award, applicants must be registered full time in a Master\u2019s or Doctoral graduate program at an Ontario university at the time of taking up the award (i.e., the fall term of 2013-14), and must remain registered full-time throughout the term of the award. Master\u2019s students remain eligible to the end of their sixth term of full-time study, and doctoral students to the end of their fifteenth term of full-time study."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Scholarship Coordinator for further information regarding this award.",
      "vid":10039,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/womens-health-scholars-award"
    },
    {
      "id":1203,
      "title":"Architecture Awards",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"There are several awards created by various donors to provide funds to assist Architecture students at the University of Waterloo. Some examples of these include:\n\nM1 Studio Design Award\n\tMarj Schaefer Prize\n\tRon Sims Purchase Prize",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The eligibility and selection criteria varies by award."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Contact the School of Architecture Department Graduate Coordinator for further information.",
      "vid":10257,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/architecture-awards"
    },
    {
      "id":1212,
      "title":"Jack Gray Fellowship",
      "status":"Active",
      "value":"$3500",
      "type":[
        "Scholarships"
      ],
      "description":"Jack Gray is a deceased former faculty member in English who donated substantially to the Graduate Scholarship in English fund and is honored with a yearly award from that fund.\n\nThis award is given out once a year to a student with the highest average which is not receiving any external awards.\u00a0 It is paid out in the Fall term but presented at an awards ceremony that usually takes place in March each year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be second-year PhD students\u00a0",
          "Not have external funding",
          "Have demonstrated academic excellence",
          "Recipients will:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department of English Graduate Coordinator for further information regarding this award.",
      "vid":10259,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jack-gray-fellowship"
    },
    {
      "id":1208,
      "title":"Doctoral Thesis Completion Awards",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"A limited number of awards are available each academic term to support doctoral students who are within the last two terms of completing their program (term of award plus one additional term). These awards are made possible with funds provided by the Vice-President, Academic and Provost, the Graduate Studies Endowment Fund (GSEF), and the Graduate Studies Office (GSO) and are intended to assist highly qualified, full-time doctoral students to complete their thesis writing and defence. This is a one-term award valued at $5,000.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Doctoral"
        ],
        "eligibility":[
          "Doctoral students (active in a PhD program)",
          "Enrolled full time",
          "In good academic standing",
          "Recipients must defend and submit the final version of their thesis within two terms of application",
          "During the term in which the award is paid, it is to be used in lieu of a Teaching Assistantship and Research Assistantship; however a student may hold a Research Studentship",
          "Recipients must not hold full-time or part-time employment during the term in which they receive this award",
          "Recipients must not hold any external awards during the term in which they receive this award"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your department\/program for further information regarding this award.",
      "vid":10312,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/doctoral-thesis-completion-awards"
    },
    {
      "id":1202,
      "title":"Accounting Alumni Award for Excellence in Accounting",
      "status":"Active",
      "value":"$0: Gold Medal - value varies",
      "type":[
        "Medals"
      ],
      "description":"One gold medal is awarded annually, usually in October, to the student graduating from the Master of Accounting program who has the highest marks in all required and elective accounting courses. The gold medal value varies, and is made available through donations from Accounting alumni.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Must be graduating from the Master of Accounting program with the highest marks in all required and elective accounting courses."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your School of Accounting Graduate Coordinator for further information regarding this award.",
      "vid":10863,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/accounting-alumni-award-excellence-accounting"
    },
    {
      "id":1204,
      "title":"Bishop Arthur Brown Award",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This award was created to recognize the strong commitment of Bishop Arthur Brown, Chancellor Emeritus of Renison University College.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Sociology and Legal Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Be accepted to the Bachelor\u2019s of Social Work or Master\u2019s of Social Work program",
          "Be registered full or part time",
          "Have a minimum overall average of 75%.\u00a0",
          "Have active experience in community service and care giving areas in their community",
          "Demonstrate financial need",
          "Applicants must:"
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          "Applicants must complete an award application form and expand on their activity and involvement in community service and caregiving."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the Sociology Department Graduate Coordinator for further information regarding this award.",
      "vid":10355,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/bishop-arthur-brown-award"
    },
    {
      "id":1206,
      "title":"David Johnston International Student Entrance Scholarship",
      "status":"Active",
      "value":"$5000: The value of each scholarship will be $5,000.",
      "type":[
        "Entrance awards"
      ],
      "description":"The David Johnston International Experience Awards will pay lasting tribute to David\u2019s unparalleled leadership as president of the University of Waterloo. These awards will celebrate his exemplary service to Canada, and will honour his commitment to promoting a better understanding among peoples of all nations.\n\nThis fund was made possible by generous donations from many individuals and corporations who wished to honour David Johnston for his remarkable achievements during his 11-year term as president of the University of Waterloo.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "These scholarships are open to all incoming international undergraduate and graduate students admitted into the first year of their program in any Faculty at Waterloo, with priority given to students enrolling in thesis-based programs",
          "Only international students, with a valid Study Permit, who are assessed international student tuition fees will be eligible.",
          "International students admitted with an admission average of 80% or above will be considered.",
          "Normally, students who are receiving major financial support (ie. in excess of $7,000 per year for undergraduates or $20,000 for graduate students, not including IMSA and IDSA funding) will not be eligible for this scholarship"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10224,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-johnston-international-student-entrance-scholarship"
    },
    {
      "id":1148,
      "title":"Ardeth Wood Memorial Graduate Bursary in Philosophy",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"The Department of Philosophy at the University of Waterloo is privileged to establish the Ardeth Wood Memorial Graduate Bursary. It will be presented yearly to a graduate student (preference will be given to female graduate students) in the Department of Philosophy based on merit, involvement in the graduate community, and proven financial need.\n\tApplicants are to apply in the Fall term by using the Graduate Student Award Application form found online.\u00a0 Applications are to be submitted to the Graduate Studies Office in Needles Hall. The final selection will be made by the Philosophy Department.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "Philosophy"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their graduate program."
        ],
        "instructions":[
          "Graduate Award Application:"
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Financial Aid &amp; Awards in the Graduate Studies Office for further information regarding this award.",
      "vid":10740,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ardeth-wood-memorial-graduate-bursary-philosophy"
    },
    {
      "id":1149,
      "title":"UW Staff Association Graduate Award",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships"
      ],
      "description":"The University of Waterloo Staff Association has made available three awards of $500 each.\u00a0 These awards are provided to deserving full or part-time graduate students in a degree program at the University of Waterloo in each of the Spring, Fall and Winter terms.\u00a0 A recipient must be a current member of the University of Waterloo Staff Association or be the child, spouse, grandchild or dependant of a current member.\u00a0 The recipient must be in good academic standing (70%minimum).\u00a0 Financial need may be considered in the selection process.\u00a0 Application forms are available on the Graduate Studies\u00a0website and on the Staff Association website and must be submitted by the appropriate deadline.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The student may only receive this award once within an academic year."
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/staff-association\/"
      ],
      "contact":"Please contact the University of Waterloo Staff Association for further information regarding this award.",
      "vid":9988,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-staff-association-graduate-award"
    },
    {
      "id":1150,
      "title":"Graduate Experience Awards",
      "status":"Active",
      "value":"Varies.",
      "type":[
        "Scholarships"
      ],
      "description":"This award is intended to provide financial support for full-time graduate students who acquire experience as a Teaching Assistant during the course of their graduate degree program in one of the specified departments\/faculties.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Applied Health Science",
        "Applied Mathematics",
        "Biology",
        "Environment &amp; Business",
        "Health Studies\/Gerontology",
        "Anthropology (Public issues)",
        "Arts",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "Classical Studies",
        "Computational Mathematics",
        "Earth &amp; Environmental Sciences",
        "Geography &amp; Environmental Mgmt",
        "Public Health",
        "Computer Science",
        "Digital Experience Innovation",
        "Environment",
        "Pharmacy",
        "Planning",
        "Recreation &amp; Leisure Studies",
        "Economics",
        "Mathematics",
        "Mathematics for Teachers",
        "Physics",
        "Social Innovation",
        "English",
        "Physics and Astronomy",
        "Pure Mathematics",
        "Science",
        "Fine Arts",
        "Quantitative Finance",
        "Vision Science",
        "French Studies",
        "Statistics &amp; Actuarial Science",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Each department department\/faculty may have their own criteria for administering this award."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9989,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/graduate-experience-awards"
    },
    {
      "id":1151,
      "title":"W.B. Pearson Medal",
      "status":"Active",
      "value":"Medal",
      "type":[
        "Medals"
      ],
      "description":"This medal was created to honour Professor W.B. Pearson in recognition of his contribution to the University of Waterloo and to Canada as a research scientist and teacher. One medal will normally be awarded annually to a doctoral student from each department in the Faculty of Science at the discretion of the department concerned in recognition of creative research as presented in the student's thesis.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Earth &amp; Environmental Sciences",
        "Pharmacy",
        "Physics",
        "Physics and Astronomy",
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/science\/graduate-students"
      ],
      "contact":"Contact the Faculty of Science Graduate Studies Office for further information.",
      "vid":10077,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/wb-pearson-medal"
    },
    {
      "id":1147,
      "title":"David Johnston International Experience Awards",
      "status":"Active",
      "value":"$2500: The value of the award will be based on the type of experience and\/or the costs and length of the experience. Varies from $2,500 to $10,000.",
      "type":[
        "International experience awards"
      ],
      "description":"Several awards will be provided annually to full-time undergraduate and graduate students in any Faculty who wish to participate in an international experience, including a minimally-paid or volunteer international co-op work placement, a volunteer placement, an academic exchange or a study\/research term related to academic requirements.\u00a0 Awards are valued at $2,500 - $10,000 and will be given on the basis of academic achievement and the location and duration of the international experience.\u00a0 Students in any Faculty, in good academic standing (normally a minimum 70% average at the undergraduate level; normally a minimum 75% average at the graduate level), who are planning to participate in an international experience are eligible to apply.\u00a0 Preference will be given to students who will be travelling to an unfamiliar country where they will experience a different culture in a new learning environment.\u00a0 Award selection will take place once per semester.\u00a0 Students should apply as soon as they are able to confirm the details of their intended experience by one of the following deadlines:\u00a0 July 15, November 15, or March 15.\u00a0 These awards were established through the generous support of donors in honour of former Waterloo President David Johnston as a lasting tribute to his 11-year service to this university and in recognition of his passion for international opportunities for students.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "In addition to this award for travel anywhere, there are several awards which fall under this award category, including awards specifically for travel to Israel (see Lebovic) or to developing countries (see McCall MacBain).",
          "The international experience must normally be for a minimum 8 weeks to be considered."
        ],
        "instructions":[
          "International Graduate Experience Award application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "application":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Graduate Studies Office Coordinator, Financial Aid &amp; Awards for further information regarding this award.",
      "vid":10223,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-johnston-international-experience-awards"
    },
    {
      "id":1146,
      "title":"Walrus Award in Political Science",
      "status":"Active",
      "value":"$500",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"This award was established to commemorate the spirit of the (1974) Walrus activities by a group of former graduate students of the Department of Political Science, University of Waterloo, who annually gather to salute their past association with graduate work. The recipient of this award must demonstrate a combination of good academic standing and financial need.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "Political Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Demonstrate good academic standing",
          "Demonstrate financial need",
          "Have resided in Ontario for 12 months prior to beginning their post - secondary education.",
          "Be Canadian or Permanent Residents",
          "Registered full time in the department of Political Science",
          "Applicants must:"
        ],
        "instructions":[
          "Graduate Award Application:"
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35",
        "https:\/\/uwaterloo.ca\/political-science\/about\/people"
      ],
      "contact":"Please contact the Coordinator, Graduate Financial Aid &amp; Awards  for further information regarding this award.",
      "vid":10248,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/walrus-award-political-science"
    },
    {
      "id":1145,
      "title":"David Johnston International Experience Awards - Lebovic",
      "status":"Active",
      "value":"$2500: The value of the award will be based on the type of experience and\/or the costs and length of the experience. Varies from $2,500 to $10,000",
      "type":[
        "International experience awards"
      ],
      "description":"Several awards will be provided annually to full-time undergraduate and graduate students in any Faculty who wish to participate in an international experience, including a minimally-paid volunteer international co-op work placement, a volunteer placement, an academic exchange or a study term related to academic requirements.\u00a0 These awards were established through the generous support of donors in honour of former Waterloo President David Johnston as a lasting tribute to his 11-year service to this university and in recognition of his passion for international opportunities for students.\u00a0 Students in any Faculty, in good academic standing (normally a minimum of 70% average at the undergraduate level; normally a minimum 75% average at the graduate level), who are planning to participate in an international experience are eligible to apply.\u00a0 Preference will be given to students who will be travelling to an unfamilar country where they will experience a different culture in a new learning environment. *Certain awards under the \"umbrella\" of the David Johnston International Experience Awards have their own specific criteria (e.g. one award is meant for students to only travel to developing countries; another award is for students to travel specifically to Israel for an international experience).\n\tAward selection will take place once per semester.\u00a0 Students should apply as soon as they are able to confirm the details of their intended experience by one of the following deadlines:\u00a0 July 15 for the Fall term; November 15 for the Winter term; March 15 for the Spring term.\u00a0 These scholarships were established through the generous support of the Joseph and Wolf Lebovic Foundation in honour of former Waterloo President David Johnston, as a lasting tribute to his 11-year service to this university and in recognition of his passion for international opportunities for students.\n\tAwards are valued at $2,500 - $10,000 and will be given on the basis of academic achievement and the location and duration of the international experience.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Recipients must be travelling to Israel for international experience."
        ],
        "instructions":[
          "International Graduate Experience Award application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "application":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Graduate Studies Office Coordinator, Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9984,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-johnston-international-experience-awards-lebovic"
    },
    {
      "id":1134,
      "title":"Wesley M. Nicol MBET Scholarship",
      "status":"Active",
      "value":"$5000: The payout is matched annually by the Faculty of Engineering for a total scholarship of $10,000.",
      "type":[
        "Scholarships"
      ],
      "description":"Wesley Nicol is a lawyer, entrepreneur, and philanthropist who has, over his lifetime, made a profound impact on his native city of Ottawa. He has brought his keen intelligence, drive and insight into the spheres of business, education, politics, and housing through professional and volunteer engagement on many levels. Wesley Nicol is passionate about the importance of education, family and strong communities in the lives of young people. In recognition of the calibre of the faculty and enthusiasm of students at the University of Waterloo, Mr. Nicol has established the Wesley M. Nicol MBET Scholarship for outstanding students at the University's Centre for Business, Entrepreneurship &amp; Technology (CBET).\n\nThe Wesley M. Nicol MBET Scholarship, with a minimum value of $10,000, will be awarded annually to one student (or divided evenly between two students) who are full-time University of Waterloo graduate students in the Faculty of Engineering's CBET program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your MBET Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9973,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/wesley-m-nicol-mbet-scholarship"
    },
    {
      "id":1135,
      "title":"William Tutte Postgraduate Scholarship",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"This scholarship has been established in honour of Professor William Tutte (1917- 2002), OC, FRS, FRSC, in recognition of his fundamental contributions to mathematics. The scholarship is awarded annually, if suitable candidates exist, to full-time graduate students in the Department of Combinatorics and Optimization who show promise of excellence in research, preferably in combinatorics and\/or graph theory and who would not be able to attend graduate school without financial support.\n\nThe value of the scholarship will be determined annually by the Department and the scholarship is tenable for up to four years.\n\nApplicants are to apply using the Graduate Studies Award Application form. The final selection will be made by the Combinatorics &amp; Optimization Departmental Graduate Committee.\n\nThe terms of this award may be redefined by the Departmental Graduate Committee.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Combinatorics &amp; Optimization",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be Canadian Citizens or Permanent Residents",
          "Must have resided in Ontario for 12 months prior to beginning their post - secondary education",
          "There are two types of awards;",
          "For the award which requires demonstrated financial need, students must submit a Graduate Application Form (see below). These applicants must also:",
          "One that requires demonstrated financial need and;",
          "One that does not"
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "June 1"
        ],
        "application":[
          "June 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Combinatorics &amp; Optimization Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10495,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/william-tutte-postgraduate-scholarship"
    },
    {
      "id":1136,
      "title":"The Institute for Polymer Research Scholarship",
      "status":"Active",
      "value":"$600: The goal will be to provide one scholarship valued at $600 annually.",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship will be awarded annually to graduate students registered full-time in a Master\u2019s or Doctoral program in the Faculty of Engineering or Science who are conducting research in the area of polymer science and engineering. Selection will be based on a combination of academic and research performance, as determined by the academic members of the Institute for Polymer Research. The goal will be to provide one scholarship valued at $1,000 annually. If there is more than one eligible candidate, the department may decide to give two awards valued at $600 each. The application guidelines and form are available on the Institute for Polymer Research website and are due by the Friday of the second week of January each year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Chemical Engineering",
        "Engineering",
        "Physics",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Access the application on the Institute for Polymer Research website.",
          "Complete the applicable application."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/uwaterloo.ca\/institute-polymer-research\/",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10900,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/institute-polymer-research-scholarship"
    },
    {
      "id":1137,
      "title":"School of Optometry of 1948 Graduate Scholarship Endowment",
      "status":"Active",
      "value":"Varies from $2,250 to $4,500",
      "type":[
        "Scholarships"
      ],
      "description":"The School of Optometry Class of 1948 Graduate Scholarship Endowment is awarded annually to a full-time UW School of Optometry graduate student whose research focuses on areas that will benefit the vision related needs of society in general, with priority given to students who have a special emphasis on the issues that affect those who are without professional optometric care. When applicable the students will hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST).\n\nThe selection will be made by the Associate Dean, Graduate Studies in conjunction with the School of Optometry\u2019s Graduate Office. Award recipients must be Canadian and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Vision Science Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9976,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/school-optometry-1948-graduate-scholarship-endowment"
    },
    {
      "id":1138,
      "title":"Sharon &amp; David Johnston Award",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"Awards will be given annually to students registered full-time at the University of Waterloo who have achieved a minimum overall average of 80% and have documented financial need.\u00a0 Candidates must be Canadians\/permanent residents and a resident of Ontario.\u00a0 In selecting the recipients, preference will be given to graduate students; female students who had more obstacles than usual in proceeding to graduate studies; Canadian Aboriginal students with special financial need.\u00a0\n\nThe fund is made possible by a donation from former University of Waterloo President David Johnston and his wife Dr. Sharon Johnston.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "October 15"
        ],
        "application":[
          "October 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact\u00a0Coordinator, Graduate Financial Aid &amp; Awards in the Graduate Studies Office for further information regarding this award.",
      "vid":10244,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/sharon-david-johnston-award"
    },
    {
      "id":1139,
      "title":"Desmond Fonn Contact Lens Research Award",
      "status":"Active",
      "value":"$4000",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"One or more awards valued at up to $4,000 each, will be given annually to full-time graduate student(s) enrolled in the Masters\/Doctoral Vision Science graduate program within the Centre for Contact Lens Research (CCLR) at the School of Optometry, whose research provides basic or clinical information pertaining to contact lenses or a related field.\u00a0 The Desmond Fonn Contact Lens Research Award was established in his honour through the support of family, friends and the contact lens industry to celebrate his illustrious academic and research career while at the UW School of Optometry.\u00a0 This Award recognizes his leadership role as Founding Director, of the Centre for Contact Lens Research (CCLR) and his innovative and collaborative spirit which has helped position the CCLR as one of the premier research centres of its kind in the world.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact The School of Optometry Graduate Coordinator for further information regarding this award.",
      "vid":9978,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/desmond-fonn-contact-lens-research-award"
    },
    {
      "id":1141,
      "title":"UW International Experience Award",
      "status":"Active",
      "value":"$2500: $2500-$10000",
      "type":[
        "International experience awards"
      ],
      "description":"There is funding available for students going on an international experience as part of their program.\u00a0 Some awards are restricted to students who are Ontario residents and have demonstrated financial need, while others are not.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Please see application form for full details.",
          "The international experience must normally be for a minimum of 8 weeks, however experiences lasting at least 4 weeks may be considered and awarded a reduced value."
        ],
        "instructions":[
          "International Graduate Experience Award application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "application":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Financial Aid &amp; Awards for further details.",
      "vid":9980,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-international-experience-award"
    },
    {
      "id":1142,
      "title":"Ontario Women&#039;s Health Scholars Award",
      "status":"Active",
      "value":"Masters Awards - $18,000 plus $1,000 research allowance\nDoctoral Awards - $20,000 plus $2,000 research allowance\nPostdoctoral Awards - $40,000 plus $5,000 research allowance",
      "type":[
        "Scholarships"
      ],
      "description":"Funded by the Ontario Ministry of Health and Long-Term Care, a Scholar Awards Program in Women's Health has been established to ensure that Ontario attracts and retains pre-eminent women's health scholars. The community of women's health scholars fostered by this Awards program will excel, according to internationally accepted standards of scientific excellence, in the creation of new knowledge about women's health and its translation into improved health for women, more effective health services and products for women, and a strengthened heath care system.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "For complete details\u00a0 and the application please visit Ontario\u00a0Women's Health Scholars Awards web site."
        ]
      },
      "deadlines":{
        "term":[
          "December 1"
        ],
        "application":[
          "December 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Financial Aid &amp; Awards in the Graduate Studies Office for further information regarding this award, including the University of Waterloo's deadline and application procedures.",
      "vid":10393,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ontario-womens-health-scholars-award"
    },
    {
      "id":1143,
      "title":"Autism Scholars Award",
      "status":"Active",
      "value":"$18,000 for Master's students\n\n$20,000 for doctoral students",
      "type":[
        "Scholarships"
      ],
      "description":"With the support of the Ministry of Training, Colleges and Universities, a Scholar Awards Program in Autism has been established to ensure that Ontario attracts and retains pre-eminent scholars.\u00a0 The community of autism scholars fostered by this Awards Program will excel, according to internationally accepted standards of scientific excellence, in the creation of new knowledge concerning child autism, and its translation into improved health for children, more effective services and products for children with autism, and increase the province\u2019s capacity in diagnosis and assessment of autism and a strengthened treatment system.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Environment &amp; Business",
        "Health Studies\/Gerontology",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "Geography &amp; Environmental Mgmt",
        "Public Health",
        "Environment",
        "Planning",
        "Recreation &amp; Leisure Studies",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "For full details regarding this award, please refer to the external Autism Scholars Award web site."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "The application and instructions can be found on the Autism Scholars Awards web site."
        ]
      },
      "deadlines":{
        "term":[
          "December 1"
        ],
        "application":[
          "December 1"
        ],
        "extended":null
      },
      "links":[
        "http:\/\/cou.on.ca\/about\/awards\/autism-scholars\/",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Financial Aid &amp; Awards in the Graduate Studies Office for further information regarding this award, including the University of Waterloo's deadline and application procedures.",
      "vid":10338,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/autism-scholars-award"
    },
    {
      "id":1144,
      "title":"David Johnston International Experience Awards - McCall MacBain",
      "status":"Active",
      "value":"$2500: The value of the award will be based on the type of experience and\/or the costs and length of the experience. Varies from $2,500 to $10,000",
      "type":[
        "International experience awards"
      ],
      "description":"Several awards will be provided annually to full-time undergraduate and graduate students in any Faculty who wish to participate in an international experience, including a minimally-paid or volunteer international co-op work placement, a volunteer placement, an academic exchange or a study term related to academic requirements.\u00a0 Awards are valued at $2,500 - $10,000 and will be given on the basis of academic achievement and the location and duration of the international experience.\u00a0 Students in any Faculty, in good academic standing (normally a minimum 70% average at the undergraduate level; normally a minimum 75% average at the graduate level), who are planning to participate in an international experience are eligible to apply.\u00a0 Preference will be given to students who will be travelling to an unfamilar country where they will experience a different culture in a new learning environment.\u00a0 Award selection will take place once per semester.\u00a0 Students should apply as soon as they are able to confirm the details of their intended experience by one of the following deadlines:\u00a0 July 15, November 15, or March 15.\u00a0 These awards were established through the generous support of donors in honour of former Waterloo President David Johnston as a lasting tribute to his 11-year service to this university and in recognition of his passion for international opportunities for students.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "This award is specifically intended for students who plan on travelling to a developing country.",
          "The international experience must normally be for a minimum of 8 weeks to be considered."
        ],
        "instructions":[
          "International Graduate Experience Award application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "application":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Graduate Studies Office Coordinator, Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9983,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-johnston-international-experience-awards-mccall"
    },
    {
      "id":1174,
      "title":"Barry Goodison Graduate Scholarship for Cryospheric Research",
      "status":"Active",
      "value":"$5000: Paid as the university match to an OGS or QEI-GSST.",
      "type":[
        "Research specific awards"
      ],
      "description":"The Barry Goodison Graduate Scholarship for Cryospheric Research will be awarded annually to one full-time University of Waterloo graduate student enrolled in the Faculty of Environmental Studies interested in Cryospheric research, who holds an OGS.\u00a0 The recipient is chosen by the Associate Dean of Graduate Studies, Environmental Studies with consultation from Professors Ellsworth LeDrew, Richard Kelly or Claude Duguay.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The recipient will hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). This award will be paid as the institutional matching funds for the OGS or QEII-GSST."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Environmental Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":10013,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/barry-goodison-graduate-scholarship-cryospheric-research"
    },
    {
      "id":1175,
      "title":"Andrew and Margaret Stephens Graduate Scholarship in Chemical Engineering",
      "status":"Active",
      "value":"$25000: The scholarship is valued at a total of $25,000 and is comprised of $10,000 from this scholarship, $10,000 from the faculty supervisor and $5,000 from the university.",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $25,000, will be awarded annually to a full-time University of Waterloo graduate student in the Faculty of Engineering who intends to pursue the MASc and PhD degrees in Chemical Engineering.\u00a0 Preference will be given to those with an undergraduate degree from Canadian universities, including the University of Waterloo. The scholarship will be renewable over the four year period 2009 to 2012. The first scholarship will be awarded in March\/April 2009.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemical Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/pilots.uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact the Chemical Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":10014,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/andrew-and-margaret-stephens-graduate-scholarship-chemical"
    },
    {
      "id":1176,
      "title":"Iris Yuzdepski Memorial Graduate Award",
      "status":"Active",
      "value":"$2500",
      "type":[
        "Scholarships"
      ],
      "description":"Up to three award valued at up to $2500 each will be provided in the Spring term to graduate students registered full time in the 3rd term of their Master's program at Waterloo. Recipients will be selected based on academic excellence (min. 80% overall average of current program) as well as financial need as determined by submission of an award application. This fund is made possible by a very generous donation from the late Ian Williams in honour and memory of his partner in life Iris Yuzdepski.\u00a0 Iris achieved her BA with a major in Anthropology from the University of Waterloo in May, 1971.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Anthropology (Public issues)",
        "Arts"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Please complete the application and submit it to the department of Anthropology."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Decisions are made in March each year. Please contact the Anthropology Department Graduate Coordinator for information on applying.",
      "vid":10652,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/iris-yuzdepski-memorial-graduate-award"
    },
    {
      "id":1177,
      "title":"David Johnston International Student Entrance Scholarships - Isreal",
      "status":"Active",
      "value":"\u00a0$5,000 - $10,000 each",
      "type":[
        "Entrance awards"
      ],
      "description":"These awards, valued at $5,000 - $10,000 each, will be provided annually on the basis of academic excellence to outstanding undergraduate or graduate students who have been living in Israel and are entering Year One in any Faculty.\u00a0 Students admitted with an admission average of 80% or above will be considered at the time of program admission.\u00a0 Selection will be based on academic achievement combined with any other Faculty-specific scholarship criteria.\u00a0 No application is required.\u00a0 These awards were established through the generous support of the Joseph and Wolf Lebovic Foundation in honour of former Waterloo President David Johnston, as a lasting tribute to his 11-year service to this university and in recognition of his passion for international opportunities for students.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10016,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-johnston-international-student-entrance-scholarships"
    },
    {
      "id":1179,
      "title":"Women in Mathematics Graduate Scholarship",
      "status":"Active",
      "value":"$3000: Each award will be a minimum of $3,000.",
      "type":[
        "Scholarships"
      ],
      "description":"One or more scholarships, valued at $3,000 each will be awarded to outstanding female graduate students in either a Masters or PhD program in the Faculty of Mathematics at the University of Waterloo.\u00a0 Total donations, of varying amounts, will dictate the number of scholarships awarded each year.\u00a0 The minimum value of each scholarship will be $3,000.\u00a0 Scholarships will be selected by the Associate Dean, Graduate Studies in the Faculty of Mathematics.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Students must have a first class standing to be considered"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Math Department Graduate Coordinator for further information regarding this award.",
      "vid":10018,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/women-mathematics-graduate-scholarship"
    },
    {
      "id":1180,
      "title":"The Don Craig Memorial Award in Masters of Accounting",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Entrance awards"
      ],
      "description":"Two awards, valued at $5,000 will be awarded to\u00a0full-time University of Waterloo Masters of Accounting students registered in School of Accounting and Finance programs in the Faculty of Arts .\u00a0 In reflection of Don\u2019s commitment to community and to the profession, the scholarship award will be awarded given to a graduate student on the basis of scholastic excellence and community involvement and\/or leadership. As Don was a tireless local volunteer and recipient of the Kitchener-Waterloo Citizen of the year in 1994, preference will be given to a student who has demonstrated community involvement or leadership within organizations based in the Waterloo region. One award per year will go to a student entering the MAcc program from the Bachelor of Accounting and Financial Management program and one from the BMath CA program. This scholarship has been established by Marilyn Craig in honour of her late husband, alumnus Donald Craig.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Letter explaining how you meet the award criteria",
          "Resume required"
        ],
        "additional":[
          "Include a copy of a recent grade report with your application."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the School of Accounting Graduate Coordinator for further information regarding this award.",
      "vid":10858,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/don-craig-memorial-award-masters-accounting"
    },
    {
      "id":1181,
      "title":"Barbara Hayes-Roth Award for Women in Math and Computer Science",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $3000 for September 2012 and $5000 annually from September 2013 to September 2016, will be awarded annually to a full-time female graduate student enrolled in a Master\u2019s or Doctoral program in the Faculty of Mathematics.\u00a0 The award will be given out on the basis of academic excellence. This fund is made possible by a gift from an anonymous donor to support a future female generation of excellence in graduate studies and research.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Math Department Graduate Coordinator for further information regarding this award.",
      "vid":10020,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/barbara-hayes-roth-award-women-math-and-computer-science"
    },
    {
      "id":1182,
      "title":"Isaac Newton Chair Graduate Research Scholarship",
      "status":"Active",
      "value":"$20000: Up to $20,000 per year.",
      "type":[
        "Research specific awards"
      ],
      "description":"University of Waterloo graduate students and visiting graduate students in the department of Physics &amp; Astronomy selected for this Award will work under the supervision of a University of Waterloo faculty member at the Perimeter Institute and will be resident at PI.\u00a0 Students may be nominated by a faculty member at Perimeter who is also a faculty member at the University of Waterloo. A selection committee consisting of the holder of the Isaac Newton Chair at the Perimeter institute, the Director of Academic Programs at Perimeter, and the Director of Guelph-Waterloo Physics institute, will choose the Award winners, who will be selected on the basis of their potential for enhancing the research programs of the Institute and of the Department of Physics &amp; Astronomy.\u00a0 The award value and duration of award will be determined by the selection committee and will vary depending on costs of tuition and fees, and any other funding received by the student.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Physics",
        "Physics and Astronomy",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Physics &amp; Astronomy Department Graduate Coordinator for further information regarding this award.",
      "vid":10021,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/isaac-newton-chair-graduate-research-scholarship"
    },
    {
      "id":1183,
      "title":"The Cecilia and the late George Piller Graduate Research Award",
      "status":"Active",
      "value":"$4000",
      "type":[
        "Research specific awards"
      ],
      "description":"Two awards valued at $4,000 each are presented annually to excellent full-time graduate students in the department in the Faculty of Arts, who conduct research on German language, culture, history and\/or society. Faculty members of the Waterloo Centre for German Studies will nominate students annually in January\u00a0 and inform them of the nomination. Students are required to submit a one-page research project proposal and CV to the Centre for adjudication. The submissions will be adjudicated based on the merit of the proposal and its contribution to the mandate of the Centre as well as the student's record of graduate study and research.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "German\/Russian"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Students are nominated by the department and are then required to submit a 1 page research project proposal and CV"
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/graduate-awards\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the German Department Graduate Coordinator for further information regarding this award.",
      "vid":10022,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/cecilia-and-late-george-piller-graduate-research-award"
    },
    {
      "id":1140,
      "title":"Toyota Canada Automotive Safety Graduate Scholarship",
      "status":"Active",
      "value":"$10000",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $10,000, is awarded annually to full-time graduate students enrolled in a Master\u2019s or Doctoral program in the Faculty of Engineering who are studying in an area of Automotive Safety. Selection will be based on academic excellence (minimum 80%). Interested students should submit an application by May 15th. This fund is made possible by a donation from Toyota Canada Inc.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "May 15"
        ],
        "application":[
          "May 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9979,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/toyota-canada-automotive-safety-graduate-scholarship"
    },
    {
      "id":1173,
      "title":"CIGI Junior Fellowships",
      "status":"Active",
      "value":"$15000: 15 fellowships are awarded per year.",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"These fellowships are to be awarded solely to graduate students in the Master's of Global Governance on the basis of academic merit. In addition to the three-term scholarships, recipients will participate in a research and professional development program designed and delivered in collaboration with CIGI that is intended to develop and enhance their professional skills and knowledge to complement their academic preparation. The CIGI Junior fellowship will be awarded once during their program. Recipients will be selected by a committee chaired by the Associate Dean of Graduate Studies, Faculty of Arts.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Global Governance"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the Global Governance Department Graduate Coordinator for further information regarding this award.",
      "vid":10012,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/cigi-junior-fellowships"
    },
    {
      "id":1172,
      "title":"Cotton Family Women in Mathematics Graduate Scholarship",
      "status":"Active",
      "value":"$3000: Value and number of awards may vary.",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship will be awarded annually to a full-time female graduate student enrolled in a Master\u2019s or Doctoral program in the Faculty of Mathematics on the basis of academic excellence in their studies and\/or research.\u00a0 The value of the award will be determined by the income generated by the fund each year, however, the goal is to provide at least one award valued at $3,000 annually.\n\tThe award is made possible by a $100,000 donation from Cathy and Paul Cotton to assist female Waterloo scholars in their pursuit of advanced degrees in mathematics.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Math Department Graduate Coordinator for further information regarding this award.",
      "vid":10011,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/cotton-family-women-mathematics-graduate-scholarship"
    },
    {
      "id":1160,
      "title":"David Johnston Waterloo Awards for Refugee Students",
      "status":"Active",
      "value":"Value varies depending on financial need.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"Funding is available each year to support undergraduate and graduate refugee students who are sponsored by the World University Service of Canada at Waterloo (WUSC) or any other students who are recognized by the Canadian government as being refugees or protected persons.\u00a0 Candidates may be enrolled in any Faculty\/program at Waterloo.\u00a0 The funds are intended to assist students who are no longer receiving sponsorship support and who have a demonstrated financial need.\u00a0 Candidates must be in satisfactory academic standing.\u00a0\n\nStudents interested in applying for this award must complete an award application and submit it to the Graduate Studies Office, Needles Hall by June 15th for the Spring term, October 15th for the Fall term, and February 15th for the Winter term.\u00a0\n\nThe value of each award will vary depending on financial need and available funds.\u00a0 These awards were established through the generous support of donors in honour of former Waterloo President David Johnston as a lasting tribute to his 11-year service to this university and in recognition of his passion for international opportunities for students.",
      "citizenship":[
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 15",
          "June 15",
          "October 15"
        ],
        "application":[
          "February 15",
          "June 15",
          "October 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact Graduate Studies Office Coordinator, Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9999,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-johnston-waterloo-awards-refugee-students"
    },
    {
      "id":1165,
      "title":"Walter Metzger Memorial Awards",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"Several awards are granted annually to full-time undergraduate and graduate students enrolled in Year 2 of their program of study who are in good academic standing and have demonstrated financial need.\u00a0 To be considered, students should complete the UW Full-time Bursary\/Award application.\u00a0 These awards are made possible by a generous gift from the late Walter Metzger.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Resided in Ontario for 12 months prior to beginning their post - secondary education",
          "Good academic standing",
          "Proven financial need",
          "Recipients must have:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Access the application on our Forms page.",
          "Application details",
          "Complete a Bursary\/Award Application form."
        ]
      },
      "deadlines":{
        "term":[
          "March 1",
          "June 15",
          "November 1"
        ],
        "application":[
          "March 1",
          "June 15",
          "November 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/about\/people"
      ],
      "contact":"Please contact the Undergraduate Awards Assistant if you have questions about this award.",
      "vid":10249,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/walter-metzger-memorial-awards"
    },
    {
      "id":1166,
      "title":"Applied Health Sciences Emergency Loan Fund",
      "status":"Active",
      "value":"Between $100 - $500 loan can be requested.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"Loans up to $500.00 for a maximum 120 days\/one term are available to full-time graduate students in the Faculty of Applied Health Sciences. To be eligible for an emergency loan a graduate student must be experiencing short-term financial difficulties, and provide proof of an acceptable form of repayment.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology",
        "Kinesiology",
        "Public Health",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be in good academic standing and provide proof of an acceptable form of repayment.",
          "Be registered in a full-time graduate program in the Faculty of AHS.",
          "To be eligible students must:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Access the application on the Finance web page.",
          "Print out and submit the completed application the Graduate Studies Office.",
          "Attach a letter outlining your financial circumstances and also proof of repayment.",
          "Complete the Emergency Loan web form."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Assistant Director, Graduate Financial Aid &amp; Awards in the Graduate Studies Office for further information regarding this loan.",
      "vid":10005,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/applied-health-sciences-emergency-loan-fund"
    },
    {
      "id":1167,
      "title":"Amit &amp; Meena Chakma Awards for Exceptional Teaching by a Student",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"The Amit &amp; Meena Chakma Awards for Exceptional Teaching by a Student were established through a generous gift by Dr. &amp; Mrs. Chakma to recognize and promote teaching excellence of our next generation of educators. The Awards are given in recognition of excellence in teaching of all kinds by registered students and are open to all students who have a formal teaching role (e.g. teaching assistant, laboratory demonstrator, sessional lecturer) at the University of Waterloo or its federated and affiliated university\/college. Recipients are to be chosen from among nominees by a Selection Committee of faculty and students. They will present up to four awards each year valued in the range of $1000 each.\u00a0 Dr. &amp; Mrs. Chakma established these awards to recognize and promote teaching excellence of our next generation of educators.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The selection Committee will look for intellectual rigor and communication skills in the interpretation and presentation of subject matter. Concern for and sensitivity to the academic need of the student is an important criterion."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
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
        "https:\/\/uwaterloo.ca\/centre-for-teaching-excellence\/grad-awards"
      ],
      "contact":"Please contact the Centre for Teaching Excellence for further information regarding this award.",
      "vid":10006,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/amit-meena-chakma-awards-exceptional-teaching-student"
    },
    {
      "id":1168,
      "title":"John Charles Polanyi Prizes",
      "status":"Active",
      "value":"$20000",
      "type":[
        "Scholarships"
      ],
      "description":"In honour of the achievement of John Charles Polanyi, recipient of the 1986 Nobel Prize in Chemistry, the Government of the Province of Ontario has established a fund to provide annually up to five prizes to outstanding researchers in the early stages of their career who are continuing to post-doctoral studies or have recently started a faculty appointment at an Ontario university. The prizes are typically valued at $20,000 each and are available in the areas broadly defined as Physics, Chemistry, Physiology or Medicine, Literature, and Economic Science.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Doctoral"
        ],
        "eligibility":[
          "For complete details please visit Waterloo's John Charles Polanyi Prizes web site.\n\t\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
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
        "https:\/\/uwaterloo.ca\/postdoctoral\/funding-and-awards\/john-charles-polanyi-prizes",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Scholarships in the Graduate Studies Office for further information regarding this award.",
      "vid":10007,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/john-charles-polanyi-prizes"
    },
    {
      "id":1169,
      "title":"Outstanding Achievement in Graduate Studies Designation",
      "status":"Active",
      "value":"This is a special designation in liu of a medal.",
      "type":[
        "Medals"
      ],
      "description":"Each year, nominees for the Alumni Gold Medal and Governor General\u2019s Gold Medal are considered for a designation of \u201cOutstanding Achievement in Graduate Studies - Master\u2019s or Doctoral\u201d. Nominees who do not receive a medal may be awarded the Outstanding Achievement in Graduate Studies designation. Recipients will be selected by the Advisory Committee on Graduate Scholarships and Awards and the Associate Provost, Graduate Studies and will receive a certificate.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Scholarships in the Graduate Studies Office for further information regarding this award.",
      "vid":10075,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/outstanding-achievement-graduate-studies-designation"
    },
    {
      "id":1170,
      "title":"Governor General\u2019s Gold Medal",
      "status":"Active",
      "value":"Gold Medal (value varies) and personalized certificate signed by the Governor General.",
      "type":[
        "Medals"
      ],
      "description":"The Governor General's Academic Medals are awarded at four distinct levels: Bronze at the secondary school level; Collegiate Bronze at the post-secondary, diploma level; Silver at the undergraduate level; and Gold at the graduate level. Medals are presented on behalf of the Governor General by participating educational institutions, along with personalized certificates signed by the Governor General to recognize outstanding scholastic achievements.\n\nAt the University of Waterloo, the Governor General's Academic Gold Medals for graduate studies will be awarded at Spring Convocation. Students who graduate in spring or graduate in the fall of the previous calendar year will be eligible for nomination.\n\nThe Graduate Studies Office administers the nomination and selection process. Each Faculty may nominate one student at the master's level and one at the doctoral level. Faculty nominations and final selection byt he Advisory Committee on Graduate Scholarships and Awards, and the Associate Provost, Graduate Studies will use the following general criteria:\n\na) Scholarship\/Research - in the form of publications, major research papers, presentations (normalized for research area); evidence of creativity\/originality should be identified in some way (e.g., external examiner's report, or report from supervisor of research paper).\n\nb) Letters of support - these may be wide-ranging and may include comments from the faculty advisor, thesis committee, external examiner, Department Chair, Faculty Associate Dean, as appropriate.\n\nc) Grades \u2013 a minimum of first class standing (80%)",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Scholarships in the Graduate Studies Office for further information regarding this award.",
      "vid":10074,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/governor-generals-gold-medal"
    },
    {
      "id":1171,
      "title":"Alumni Gold Medal",
      "status":"Active",
      "value":"Gold Medal (value varies)",
      "type":[
        "Medals"
      ],
      "description":"The Office of Alumni Affairs recognizes top graduating students for academic achievement, by awarding the Alumni Gold Medal at convocation.\u00a0 The ten carat, solid gold medal is embossed with the university crest on the front and the student\u2019s name and Faculty are inscribed on the back. At fall convocation, the award is presented to a master\u2019s and a doctoral student to recognize their academic excellence.\u00a0 Students who graduate in spring or fall of the calendar year will be eligible for nomination.\n\nThe Graduate Studies Office administers the nomination and selection process.\u00a0 Each Faculty may nominate one student at the master\u2019s level and one for the doctoral level.\u00a0 Faculty nominations and final selection by the Advisory Committee on Graduate Scholarship and Awards, and the Associate Provost, Graduate Studies will use the following general criteria:\u00a0\n\na) Scholarship\/Research - in the form of publications, major research papers, presentations (normalized for research area); evidence of creativity\/originality should be identified in some way (e.g., external examiner's report, or report from supervisor of research paper).\n\nb) Letters of support - these may be wide-ranging and may include comments from the faculty advisor, thesis committee, external examiner, Department Chair, Faculty Associate Dean, as appropriate.\n\nc) Grades \u2013 a minimum of first class standing (80%)",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Scholarships in the Graduate Studies Office for further information regarding this award.",
      "vid":10071,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/alumni-gold-medal"
    },
    {
      "id":1101,
      "title":"Don E. Irish Graduate Award",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at up to $2,000 is awarded annually to full-time graduate students completing their graduate degree in the department of Chemistry in the Faculty of Science on the basis of demonstrated excellence.\u00a0 This fund is made possible by a donation from Hilda Buckingham Irish, sister-in-law to the late Don E. Irish (former chair of the department of Chemistry).",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Coordinator for further information regarding this award.",
      "vid":9940,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/don-e-irish-graduate-award"
    },
    {
      "id":1100,
      "title":"Donald J. &amp; Kathleen D. McDougall Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $5,000 will be awarded annually to a full-time University of Waterloo graduate student registered in the School of Pharmacy in the Faculty of Science. The scholarship will be awarded to a graduate student on the basis of scholastic excellence and commitment to service in their community.\n\nThis scholarship has been established by Janet McDougall, BSc\u201971 to honour her parents, Donald Joseph and Kathleen (Kay) Donihee McDougall. Don was a practicing pharmacist from 1934 through 1993, and loved his profession.\u00a0 Both Don and Kay were community leaders, dedicated volunteers, and civic activists.\u00a0 This award honours their contributions and their belief in service to the community.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Pharmacy",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Pharmacy Department Graduate Coordinator for further information regarding this award.",
      "vid":9939,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/donald-j-kathleen-d-mcdougall-graduate-scholarship"
    },
    {
      "id":1099,
      "title":"Donald J. Clough Memorial Award",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships"
      ],
      "description":"Professor Clough, whose achievements this award commemorates, greatly influenced engineering education and was the founding Chair of the Department of Management Sciences at UW.\u00a0 This award has been established by the Sandford Fleming Foundation from donations made in memory of Professor Clough.\u00a0 Recipients of the award will display superior academic achievement and will be enrolled in the first year of graduate studies in Management Sciences at UW.\u00a0 The recipient of the award will be chosen by the Department of Management Sciences.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Management Sciences"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Management Sciences Department Graduate Coordinator for further information regarding this award.",
      "vid":10825,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/donald-j-clough-memorial-award"
    },
    {
      "id":1098,
      "title":"Dr. Derick Wood Graduate Scholarship in Computer Science",
      "status":"Active",
      "value":"$2000: Varies from $2,000 to $10,000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $2,000 - $10,000 awarded annually to full-time graduate students enrolled in the masters\/doctoral program in the David R. Cheriton School of Computer Science in the Faculty of Mathematics on the basis of scholastic excellence and evidence of research potential, as indicated by publications and letters of reference.\u00a0 Preference will be given to PhD students and to students whose research area is Algorithms and Complexity. It is renewable and open to both Canadian and international students holding a student visa.\u00a0This fund is made possible by the donations of family, friends and colleagues in memory of Derick Wood.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the David R. Cheriton School of Computer Science Graduate Coordinator for further information regarding this award.",
      "vid":10710,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-derick-wood-graduate-scholarship-computer-science"
    },
    {
      "id":1102,
      "title":"Richard &amp; Elizabeth Madter Graduate Award in Electrical &amp; Computer Engineering - OGS\/QEII-GSST Match",
      "status":"Active",
      "value":"This award is paid out as on OGS and has no additional value.",
      "type":[
        "Scholarships"
      ],
      "description":"Richard and Elizabeth Madter, Alumni of the University of Waterloo have established two research scholarships for graduate students in the Department of Electrical and Computer Engineering at the University of Waterloo. The students will hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST).\n\nThe selection will be made by the Associate Dean, Graduate Studies in conjunction with the Department Associate Chair for Graduate Studies.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Electrical &amp; Computer Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Electrical &amp; Computer Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9941,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/richard-elizabeth-madter-graduate-award-electrical-computer"
    },
    {
      "id":1103,
      "title":"Richard and Elizabeth Madter Graduate Award in Electrical and Computer Engineering",
      "status":"Active",
      "value":"$25000",
      "type":[
        "Scholarships"
      ],
      "description":"Two graduate scholarships that will be presented to full time graduate students who have been accepted into the Graduate program in Electrical &amp; Computer Engineering.\u00a0 The value of the scholarships will be $25,000 comprising of $10,000 from the payout of the endowment, $10,000 from the faculty supervisor of the graduate student and $5000 from the University.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Electrical &amp; Computer Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact the Electrical &amp; Computer Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9942,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/richard-and-elizabeth-madter-graduate-award-electrical-and"
    },
    {
      "id":1104,
      "title":"Robert A. Fern Memorial Award",
      "status":"Active",
      "value":"One award of up to $400 annually.",
      "type":[
        "Scholarships"
      ],
      "description":"One award will be made to a senior undergraduate or graduate student in the Department of RLS who has made a significant contribution in either volunteer work with persons with disabilities or applied research which has relevance to the lives of persons with disabilities.\u00a0 Interested graduate students are invited to apply by October 1st.\n\nThis award honours the memory of Robert A. Fern, an employee of Parks Canada and the Department of Canadian Heritage, who was recognized world wide as a leader in advancing accessibility and participation by persons with disabilities in all aspects of society.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Graduate Award Application:"
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
      "contact":"Please contact the Recreation &amp; Leisure Studies Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9943,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/robert-fern-memorial-award"
    },
    {
      "id":1105,
      "title":"Roberta and Lonsdale Schofield Graduate Scholarship in Architecture",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The Roberta and Lonsdale Schofield Graduate Scholarship in Architecture will be awarded annually to an outstanding student entering the professional master of Architecture Program. Normally it will be awarded in conjunction with an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). The endowment was established by Roberta and Lonsdale Schofield in recognition of the relocation of the School of Architecture to Cambridge.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Architecture Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9944,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/roberta-and-lonsdale-schofield-graduate-scholarship"
    },
    {
      "id":1107,
      "title":"Sally Weaver Graduate Scholarship",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"Dr. Sally Weaver was the former chair of UW Anthropology department and an authority on Canadian First Nations.\u00a0 She came to UW in 1966.\u00a0 Sally was the author of extensive work about Native peoples in North America, dating back to Medicine and Politics among the Grand River Iroquois in 1972 and Making Canadian Indian Policy in 1981.\n\nThe value of the annual award is determined by the endowment interest each year.\u00a0 The scholarship(s) will be awarded annually to a full-time University of Waterloo graduate student(s) in the Department of Anthropology on the basis of scholastic excellence and the student's proposal for anthropological research.\u00a0 Selection will be made by the Chair and the Associate Chair after consultation with members of the Department.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Anthropology (Public issues)",
        "Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9946,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/sally-weaver-graduate-scholarship"
    },
    {
      "id":1108,
      "title":"Savvas Chamberlain Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship will be presented to a full-time graduate student who has been awarded an Ontario Graduate Scholarship and has been accepted into the Graduate program in the Department of Electrical and Computer Engineering.\u00a0 The scholarship recipient will be pursuing a graduate degree with a concentration in electronics, microelectronics, semiconductor devices and integrated circuits.\u00a0The Associate Chair of Graduate Studies in the Department of Electrical and Computer Engineering through the departmental scholarship committee will come up with a name or short list of eligible candidates.\u00a0 The name or short list of candidates will be presented to the scholarship committee of the Faculty of Engineering to select the candidate.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Electrical &amp; Computer Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Electrical and Computer Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9947,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/savvas-chamberlain-graduate-scholarship"
    },
    {
      "id":1097,
      "title":"Dr. Emerson Woodruff Graduate Scholarship in Paediatrics",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at approximately $1,000, is awarded annually to full-time graduate students enrolled in the Masters\/Doctoral program in the School of Optometry Vision Science graduate program whose research provides basic or clinical information pertaining to the developing visual system in infants and children.\u00a0 The Dr. Emerson Woodruff Graduate Scholarship was established in his memory, through the support of family and friends, to honour this former Professor and Director of the UW School of Optometry for his many contributions to optometric education and the profession.\u00a0 This scholarship recognizes his leadership role in the establishment of the School's Vision Science program and his passion for paediatrics research.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact teh Vision Science Department Graduate Coordinator for further information regarding this award.",
      "vid":9936,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-emerson-woodruff-graduate-scholarship-paediatrics"
    },
    {
      "id":1096,
      "title":"Recreation &amp; Leisure Studies Alumni Scholarship of Graduate Studies",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships",
        "Entrance awards"
      ],
      "description":"An award may be given annually on entrance to the MA program when a student, admitted directly from the University of Waterloo Department of Recreation and Leisure Studies honour's program to the master's program, is judged to be outstanding. The criteria will include community service and overall academic excellence. The selection will be made by the Recreation and Leisure Graduate Studies Committee at the time of admission to the MA program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your\u00a0Recreation and Leisure Studies Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9935,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/recreation-leisure-studies-alumni-scholarship-graduate"
    },
    {
      "id":1095,
      "title":"Dr. Erlane F. Soares Scholarship in Civil &amp; Environmental Engineering",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $5000 will be awarded annually to a full-time University of Waterloo doctoral student registered in department of Civil Engineering in the Faculty of Engineering.\u00a0 The scholarship will be awarded on the basis of scholastic excellence.\u00a0 Preference will be given to a student who holds an Ontario Graduate Scholarship (OGS) or another major external scholarship that requires a matching or enhancement component.\u00a0 If the match or enhancement becomes unavailable or a suitable recipient cannot be found, the funds will be paid out as a regular graduate scholarship. This scholarship has been established by Christine Winkelmann Soares in memory of her husband Dr. Erlane F. Soares who completed his Phd. in Civil Engineering in 1976 from Waterloo Engineering.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "The recipient may hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) in which case the award will be paid as the institutional matching funds for the OGS or QEII-GSST."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Civil &amp; Environmental Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9934,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-erlane-f-soares-scholarship-civil-environmental"
    },
    {
      "id":1085,
      "title":"R.N. Farvolden Endowment Scholarship",
      "status":"Active",
      "value":"Varies.",
      "type":[
        "Scholarships"
      ],
      "description":"One annual award will be given to a graduate student in September of each year; the amount will depend on investment income. The graduate student must be enrolled in the groundwater program in the Department of Earth Sciences. The student must have chosen to pursue a research topic concerning groundwater in a developing country or on the topic of regional hydrogeology in Canada.\n\nNo application is necessary; the Award Selection Committee will determine eligibility in consultation with professors within the department.\n\nThis scholarship was founded in 1990 to commemorate the 20th anniversary of Dr. Robert Farvolden's arrival at the University of Waterloo and his initiation of the groundwater research program. The endowment has been established from the proceeds of a short course on Dense Non-Aqueous Phase Liquids organized by a group including graduate students and professors in the Department of Earth Sciences.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Earth &amp; Environmental Sciences",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Earth Sciences Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9924,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rn-farvolden-endowment-scholarship"
    },
    {
      "id":1086,
      "title":"Fong Computational Mathematics Graduate Award",
      "status":"Active",
      "value":"One scholarship valued at $7,500; OR two scholarships each valued at $3,750",
      "type":[
        "Scholarships"
      ],
      "description":"The goal will be to provide one scholarship valued at $7,500 or two scholarships each valued at $3,750 annually to full-time graduate students entering graduate studies in the Computational Mathematics Graduate Program in the Faculty of Mathematics.\u00a0 This fund is made possible by a donation from the Fong Education Foundation Limited.\u00a0 Mr. Eddie Fong (BMath \u201980) has enjoyed an extremely successful career and is pleased to support his alma mater.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computational Mathematics",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Selection will be made on the basis of academic excellence (minimum 80%) as well as demonstrated interest in computational and\/or industrial mathematics."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact teh Computational Mathematics Department Graduate Coordinator for further information regarding this award.",
      "vid":9925,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/fong-computational-mathematics-graduate-award"
    },
    {
      "id":1087,
      "title":"Fairfax Financial Academic All-Canadian Awards",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"Four awards, valued at $1,000 each, are presented annually to the top male and female graduate and undergraduate student athletes.\u00a0 These awards are funded by a donation made possible by Fairfax Financial Holdings Limited.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Each recipient must have been a qualified student athlete during the preceding academic year, and must not previously have been granted this award or the Fairfax Financial Athlete Leadership Scholarship.\u00a0 Candidates will be identified by the Department of Athletics and selection will be made by the Department of Athletics in consultation with the Student Awards &amp; Financial Aid Office, or the Graduate Studies Office, as applicable."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.athletics.uwaterloo.ca\/staff.aspx?tab=staffdirectory"
      ],
      "contact":"Please contact the Athletics and Recreation for more information.",
      "vid":9926,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/fairfax-financial-academic-all-canadian-awards"
    },
    {
      "id":1088,
      "title":"F.W. Karasek Scholarship (A.J. Carty)",
      "status":"Active",
      "value":"$600",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship, administered by (GWC)2, has been donated by Professor F.W. Karasek, Distinguished Professor Emeritus of the Chemistry Department at the University of Waterloo. It is awarded annually (as long as the funding is continued) on a competitive basis and is worth $1000. This competition is open to all graduate students registered in the Guelph-Waterloo Centre. Candidates will be considered on the basis of overall abilities, including both research and coursework. Nominations will be solicited from Centre faculty and the graduate officers by the deadline date each year and the scholarship will be presented at the Annual Seminar of the Centre.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Chemistry Department Graduate Coordinator for further information regarding this award.",
      "vid":9927,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/fw-karasek-scholarship-aj-carty"
    },
    {
      "id":1089,
      "title":"Evelyn Guderian Graduate Scholarship in Germanic &amp; Slavic Studies",
      "status":"Active",
      "value":"$750",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at a minimum of $750 will be awarded annually to a full-time current or incoming graduate student enrolled in the Master\u2019 s or Doctoral program in the Department of Germanic &amp; Slavic Studies in the Faculty of Arts on the basis of academic achievement and excellence n the area of German studies.\u00a0 Students will be nominated by the Associate Chair in Graduate Studies in the Department of Germanic &amp; Slavic Studies in February and the recipient selected in the Winter term. This fund is made possible by a donation from Evelyn Guderian for support of continued scholarship in the area of German studies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "German\/Russian"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/graduate-awards\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Germanic &amp; Slavic Studies Department ScGraduate Coordinator for further information regarding this award.",
      "vid":9928,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/evelyn-guderian-graduate-scholarship-germanic-slavic-studies"
    },
    {
      "id":1090,
      "title":"R.S. Dorney Memorial Fellowship",
      "status":"Active",
      "value":"Number of awards and amounts may vary from year to year.",
      "type":[
        "Scholarships"
      ],
      "description":"This award commemorates the pioneering work of Dr. R.S. Dorney, a founding member of the School of Planning (1967 - 1987), who worked in the field of applied urban and regional human ecology and environmental management. He applied the science of ecology to further our understanding of the human environment. The award is for a PhD student enrolled in the Faculty of Environmental Studies who will be studying in the field pioneered by Dr. Dorney.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Must be enrolled full-time in a Faculty of Environment graduate program",
          "Must be within their allowable time limits",
          "Must not be supported by a major external scholarship such as the OGS, NSERC or SSHRC"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Faculty of Environment Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9929,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rs-dorney-memorial-fellowship"
    },
    {
      "id":1091,
      "title":"Employers&#039; Advocacy Council, Canadian Manfacturers and Exporters, and the Industrial Accident Prevention Association Occupational Health and Safety Research Scholarship",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships"
      ],
      "description":"The Employers\u2019 Advocacy Council, the Canadian Manufacturers, and the Industrial Accident Prevention Association, in a unique partnership, have established a research scholarship for a graduate student entering the 2nd year of the Master of Science in Kinesiology, Faculty of Applied Health Science. The scholarship will be awarded on the basis of scholastic excellence and a demonstrated ability to conduct research. The research topic will be in the area of occupational health and safety, specifically the advancement of safe work places, prevention of occupational disease in the future, compensating and assisting workers and survivors affected by occupational disease, or another suitable area of study. Special consideration will be given to those applicants who themselves have been injured\/disabled as a result of a workplace injury or occupational disease or have had a close family member injured or disabled from similar circumstances. This scholarship is open to Canadian and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Kinesiology"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact Kinesiology Department Graduate Coordinator for further information regarding this award.",
      "vid":9930,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/employers-advocacy-council-canadian-manfacturers-and"
    },
    {
      "id":1092,
      "title":"EB (Ted) Cross MBET Scholarship",
      "status":"Active",
      "value":"$10000",
      "type":[
        "Scholarships"
      ],
      "description":"Founded by Ted Cross - a pioneer in the development of technology transfer activities at the University of Waterloo - one scholarship will be presented\u00a0to an outstanding student entering the Master of Business, Entrepreneurship and Technology program. Selection will be made by the MBET Admissions Committee, based on previous academic accomplishments, financial need and the ability to demonstrate, during an interview process, the entre(intra)-preneurial attributes required to successfully complete the program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Please visit the\u00a0Conrad Business Entrepreneurship Technology website for application information."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your CBET Department Graduate Coordinator for further information regarding this award.",
      "vid":9931,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/eb-ted-cross-mbet-scholarship"
    },
    {
      "id":1093,
      "title":"Dr. Noel Hynes Memorial Graduate Scholarship",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships"
      ],
      "description":"An annual scholarship valued at $2,000 will be awarded annually to a full-time graduate student enrolled in the department of Biology in the Faculty of Science, working in the area of ecology. Preference will be given to students who do not hold another major award. This fund is made possible by the family and friends of Dr. Noel Hynes, first permanent Chair of the Department of Biology.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Biology Department Graduate Coordinator for further information regarding this award.",
      "vid":9932,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-noel-hynes-memorial-graduate-scholarship"
    },
    {
      "id":1094,
      "title":"Ram and Lekha Tumkur Memorial Graduate Scholarship",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established by Dr. and Mrs. Nagraj Tumkur in memory of their children: Rammohan and Chitralekha, who were killed in the Air-India flight 182 that crashed in June 1985 with no survivors. It will be awarded annually, if a suitable candidate exists, for postgraduate study leading to a Master of Science degree in any field of biology. The recipient will be a MSc candidate in the Department of Biology, University of Waterloo.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Biology Department Graduate Scholarship Coordinator for further information regarding this award. \u00a0",
      "vid":9933,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ram-and-lekha-tumkur-memorial-graduate-scholarship"
    },
    {
      "id":1084,
      "title":"Fred &amp; Ruth Stork Awards in German Studies",
      "status":"Active",
      "value":"Varies from $500 to $1,500:\n\nWCGS Intercultural German Studies Awards, valued at up to $2000 per student.\n\tWCGS International Opportunities uWaterloo Travel Grants valued from $500 up to $1,500 per student.\n\tWCGS International Opportunities Canadian Travel Grants, valued from $500 to $1,500 per student.",
      "type":[
        "Scholarships"
      ],
      "description":"Three awards are awarded annually based on the students\u2019 participation in a recognized institutional Canadian-organized German language or cultural studies program abroad:\n\t1. The WCGS Intercultural German Studies Awards, valued at up to $2000 per student, are awarded annually to full-time graduate students enrolled in the Joint Intercultural German Studies degree program.\n\t2. The WCGS International Opportunities Waterloo Travel Grants, valued at $1000 per student, are awarded annually to full-time undergraduate or graduate students registered within the first four years of their program within the Faculty of Arts at the University of Waterloo and taking at least one Germanic and Slavic Studies course. Interested students must complete an application found at http:\/\/www.wcgs.ca\/www\/index.php\/sponsorship\/exchange.html by March 1st.\n\t3. WCGS International Opportunities Canadian Travel Grants, valued at $500 per student, are awarded annually to full-time undergraduate or graduate students registered within the first four years of their program at a Canadian University. Interested students must complete an application found at http:\/\/www.wcgs.ca\/www\/index.php\/sponsorship\/exchange.html by March 1.\n\tThese awards are made possible by a donation from Fred and Ruth Stork, and their children Michael and Marion, as loyal friends and supporters of the University of Waterloo, the Kitchener-Waterloo community and the Waterloo Centre for German Studies (WCGS).",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Please visit the WCGS website\u00a0for application information."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/centre-for-german-studies\/scholarships\/fred-ruth-stork-awards-german-studies",
        "http:\/\/www.wcgs.ca\/www\/index.php\/sponsorship\/exchange.html",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact the Germanic &amp; Slavic Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":9923,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/fred-ruth-stork-awards-german-studies"
    },
    {
      "id":1109,
      "title":"Schlegel Award for Research in Aging in Applied Health Sciences",
      "status":"Active",
      "value":"Varies from $4,000 to $6,000",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"In 2004, Dr. Ron Schlegel, former faculty member and long-time friend and supporter of the University of Waterloo, established an annual research award for students studying in the area of aging within the graduate program in Applied Health Sciences.\u00a0\n\nThis award will be awarded to outstanding students with financial need.\u00a0 Academic merit will be based on first year graduate studies standing.\u00a0 This is an Ontario Student Opportunities Trust Fund (OSOTF) Award, open to Ontario residents.\u00a0\n\nThe final selection will be made by the Applied Health Sciences Associate Dean, Graduate Studies and Research.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology",
        "Kinesiology",
        "Public Health",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "June 1"
        ],
        "application":[
          "June 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your AHS Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10243,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/schlegel-award-research-aging-applied-health-sciences"
    },
    {
      "id":1123,
      "title":"UW Alumni @ Microsoft Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"Scholarship(s) will be awarded on a rotating basis in the Faculty of Engineering, Faculty of Mathematics, the Cheriton School of Computer Science, and university-wide. The university will make every effort to match this award with government programs.\u00a0 For instance, when matched 2:1 by an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) the total value of the scholarship is $15,000. It could also be used as a top-up for the NSERC CGS or PGS scholarships. If this is not feasible, the scholarships will be valued and awarded at $5,000 each. The scholarship will be awarded on the basis of scholastic excellence.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Awardees will normally be recipients of an OGS or a QEII-GSST."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9962,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-alumni-microsoft-graduate-scholarship"
    },
    {
      "id":1124,
      "title":"UW Fluid Mechanics Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The UW Fluid Mechanics Graduate Scholarship will be presented to a full-time graduate student who has been awarded an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) and has been accepted into the Graduate program in the Department of Mechanical Engineering. The scholarship recipient will be pursuing a graduate degree with a concentration in Fluid Mechanics. Eligibility for the scholarship should be based both on academic merit and demonstrated excellence in research through hands on applications.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Awardees will hold an OGS or a QEII-GSST in the department of Mechanical &amp; Mechatronics Engineering."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9963,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-fluid-mechanics-graduate-scholarship"
    },
    {
      "id":1125,
      "title":"UW Graduate Studies Fund Scholarship",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"A University of Waterloo Graduate Studies Fund has been established in the Graduate Studies Office to (i) administer contributions received under the Senate Graduate Scholarships program and designated to graduate studies, (ii) to serve as a general account for funds donated for graduate studies without specific administrative requirements and (iii) to create a graduate scholarship fund to honour the memory of people associated with the university, i.e., alumni, faculty, friends, retirees, and staff. (Existence of this fund does not preclude the creation of other memorial funds named for individuals.)\u00a0\n\nAwards will initially be made, as funds permit, under the terms of the Senate Graduate Scholarships: students must have a B+ standing and normally be registered full-time.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9964,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-graduate-studies-fund-scholarship"
    },
    {
      "id":1126,
      "title":"UW Provost Graduate Scholarship",
      "status":"Active",
      "value":"$15000",
      "type":[
        "Scholarships",
        "Entrance awards"
      ],
      "description":"Scholarships valued at $15,000 each will be provided as an entrance scholarship to students who will be registered full-time in research-based Master\u2019s or Doctoral programs at the University of Waterloo.\u00a0 The scholarship will be paid across three academic terms.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Students must be Canadian Citizens or Permanent Residents and demonstrate academic excellence (minimum 80% over the last 20 academic credits\/2 year\u2019s full-time study)."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9965,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-provost-graduate-scholarship"
    },
    {
      "id":1127,
      "title":"UW Retirees&#039; Graduate Scholarship",
      "status":"Active",
      "value":"This award is paid as an OGS award. There is no additional value.",
      "type":[
        "Scholarships"
      ],
      "description":"Scholarship(s) are presented annually to outstanding graduate student(s) on a rotating basis through the faculties. Recipients must hold either an Ontario Graduate Scholarship (OGS), or an Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). The selection will be made by the Associate Dean, Graduate Studies. These scholarships are made possible by the support of the University of Waterloo retirees.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9966,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-retirees-graduate-scholarship"
    },
    {
      "id":1128,
      "title":"W.F. Forbes Entrance Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships",
        "Entrance awards"
      ],
      "description":"The award will be given to a student registered full-time who is beginning a Master's program in Statistics with Biostatistics specialization.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Mathematics",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "The recipient must be entering with at least an 80% (A) average."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9967,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/wf-forbes-entrance-award"
    },
    {
      "id":1129,
      "title":"W.J. Beynon Memorial MBET Scholarship",
      "status":"Active",
      "value":"$10000: Up to $10,000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at up to $10,000 is awarded annually to a full-time graduate student enrolled in the Masters of Business, Entrepreneurship &amp; Technology (MBET) program in the Faculty of Engineering on the basis of academic achievement.\u00a0 Preference will be given to students who have a minimum admission average of 80%.\u00a0 This fund is made possible by donations from the Beynon Family in honour of W.J. Beynon.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Only full-time students enrolled in the Masters of Business, Entrepreneurship &amp; Technology (MBET) program in the Faculty of Engineering are eligible for this award.",
          "Preference will be given to students who are residents of Lambton Country, Ontario"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9968,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/wj-beynon-memorial-mbet-scholarship"
    },
    {
      "id":1130,
      "title":"Water Institute Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"A scholarship, valued at $5,000 is awarded annually to a full-time University of Waterloo graduate student. The scholarship will be awarded on the basis of scholastic excellence and a demonstrated commitment in water research. This scholarship has been established by Platinum Level External Partners of the Water Institute.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The Water Institute will manage the scholarship selection process and normally select recipients each Fall term, based on the following eligibility and selection criteria:",
          "Applicants must be full-time University of Waterloo graduate students.",
          "Applicants must have a demonstrated commitment to water-related research.",
          "Applicants must have obtained a first class average (80%) over the last two completed years of study.",
          "Applicants holding major scholarships (in excess of $25,000 cumulative) in the year of competion are not eligible to apply.",
          "Applicants that have previously been awarded a Water Institute Graduate Scholarship are not eligible to apply."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Complete the Water Institute graduate scholarships application form found on our forms webpage and submit to the Water Institute."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/water.uwaterloo.ca\/"
      ],
      "contact":"Please contact the Water Institute for further information regarding this award.",
      "vid":10511,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/water-institute-graduate-scholarship"
    },
    {
      "id":1131,
      "title":"Warren Ober Award for Outstanding Teaching by Graduate Students Within the Faculty of Arts",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships"
      ],
      "description":"The Warren Ober Awards for Outstanding Teaching by a Graduate Student may be granted to graduate students who have made significant contributions to teaching within the Faculty of Arts. The amount of the awards may vary depending on the annual endowment yield. The award is open to individuals who are currently involved, or have recently been involved, in teaching University of Waterloo undergraduate students while themselves pursuing a course of study leading to a graduate degree within the Faculty of Arts. The awards were initiated with funds provided to Dr. Warren Ober, a now retired Professor of English, as an early recipient of the Distinguished Teacher Award. Students must be nominated in February by a faculty member.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Anthropology (Public issues)",
        "Arts",
        "Classical Studies",
        "Digital Experience Innovation",
        "Economics",
        "English",
        "Fine Arts",
        "French Studies",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Recipients will be currently or recently involved, in teaching University of Waterloo undergraduate students while pursuing an Arts graduate degree."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9970,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/warren-ober-award-outstanding-teaching-graduate-students"
    },
    {
      "id":1132,
      "title":"Waterloo Pioneers of Microbiology Graduate Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $1,000 is given annually to a graduate student in the first year of their Master\u2019s or Doctoral program in the Department of Biology in the Faculty of Science.\u00a0 The award recipient must have demonstrated research ability, scholastic aptitude, and an interest in pursuing microbiology or related field under the supervision of a Waterloo Biology Faculty member.\u00a0 This Award was initiated by Dr. Joan P. Torrie and made possible by donations from the friends, family and colleagues of Professor Alan Kempton, Professor William Inniss and Professor Colin Mayfield; the founders of the Microbiology Department at the University of Waterloo.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Graduate students registered in the first year of their Master\u2019s or Doctoral program in the Department of Biology in the Faculty of Science.",
          "Selection to be based on demonstrated research ability, scholastic aptitude, and an interest in microbiology research.",
          "Faculty members in the Department of Biology will nominate candidates.",
          "Recipients will be selected annually by the selection committee within the Department."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9971,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/waterloo-pioneers-microbiology-graduate-award"
    },
    {
      "id":1133,
      "title":"Waterloo Special Graduate Student Entrance Award (also known as New Faculty Award)",
      "status":"Active",
      "value":"$5500: Up to a maximum of $5500 per faculty member.",
      "type":[
        "Scholarships"
      ],
      "description":"The purpose of this award is to encourage new faculty members to undertake supervision of new full\u2010time graduate students in keeping with Waterloo\u2019s vision for Graduate Expansion. On the recommendation of a new faculty member, the student will receive a $5,500 award. (This proposal is applicable to faculty members who started their appointments after May 1, 2005).",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The new full\u2010time faculty member must hold a professorial tenured or tenure track appointment or cross\u2010appointment in a department with a graduate program and have been hired within the last two years.",
          "The faculty member must be eligible to supervise a graduate student who is working on a thesis.",
          "The maximum funds per faculty member are $5,500, to be used exclusively to support one or more newly admitted full\u2010time graduate students (preferably domestic) in term one or two of their graduate program."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9972,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/waterloo-special-graduate-student-entrance-award-also-known"
    },
    {
      "id":1122,
      "title":"Urban Strategies Inc. Graduate Award",
      "status":"Active",
      "value":"Up to $5,000",
      "type":[
        "Scholarships"
      ],
      "description":"This award was established by Urban Strategies Inc. which is a planning and urban design firm based in Toronto.\u00a0\n\nOne award will be presented annually to a graduate student in the School of Architecture who architectural thesis best exemplifies excellence in Urban Design. The selection will be based on merit and made by the Director of the School of Architecture and Urban Strategies Inc.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9961,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/urban-strategies-inc-graduate-award"
    },
    {
      "id":1121,
      "title":"University Staff &amp; Faculty Endowment Fund Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"This fund was established by UW staff and faculty to enrich UW's scholarship program, recognize academic excellence and provide opportunities for children of UW faculty and staff. The funds available each year will be used for graduate scholarships that, whenever possible, will generate external matching funds. While the Ontario Graduate Scholarship (OGS) and the Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) programs are in place, only holders of OGS or QEII-GSST scholarships for study at UW are eligible; and priority will be given to children of UW faculty and staff. Approximately $350,000 (which will generate $17,500 annually) has been contributed to this endowment fund as a result of the demutualization of the company that managed UW's life insurance plan.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9960,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/university-staff-faculty-endowment-fund-graduate-scholarship"
    },
    {
      "id":1110,
      "title":"Schneider Foods Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The Schneider Foods Graduate Scholarship will be presented to a full-time graduate student who has been awarded into the Graduate program in Engineering, Environment or Science.\u00a0 The scholarship recipient must be pursuing a graduate degree with a concentration in water resources and treatment. The Graduate Studies Office will review the list of eligible candidates and will make the final decision regarding the recipient of the scholarship.\u00a0 Students must hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST).",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Architecture",
        "Biology",
        "Environment &amp; Business",
        "Chemistry",
        "Environment &amp; Resource Studies",
        "MBET",
        "Chemical Engineering",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Civil &amp; Environmental Eng",
        "Environment",
        "Pharmacy",
        "Planning",
        "Electrical &amp; Computer Eng",
        "Physics",
        "Social Innovation",
        "Management Sciences",
        "Physics and Astronomy",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Vision Science",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9949,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/schneider-foods-graduate-scholarship"
    },
    {
      "id":1111,
      "title":"Sinclair Graduate Scholarship",
      "status":"Active",
      "value":"$1000: The award value varies from year to year, typically ranging from $1000 and up.",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established by a gift of Joyce Sinclair (B.Math. 1976, C&amp;O) and Bill Sinclair (B.Sc. 1976, Physics). Scholarships are awarded annually, if suitable candidates exist, to full-time graduate students in Combinatorics and Optimization who have demonstrated excellence in academic and\/or research work. Values of the scholarships and recipients will be determined annually by the Chair of the Department of Combinatorics and Optimization in consultation with the departmental graduate committee. The terms of this award may be redefined should the department determine a need to do so.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Combinatorics &amp; Optimization",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact the\u00a0Combinatorics and Optimization Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9950,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/sinclair-graduate-scholarship"
    },
    {
      "id":1112,
      "title":"Statistics &amp; Actuarial Science Graduate Award",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"The statistics and Actuarial Science Graduate Award fund has been established to (i) receive contributions received under the Senate Graduate Scholarships program and designated to the Department of Statistics and Actuarial Science, (ii) to serve as a general account for different awards set up by the department of Statistics and Actuarial Science.\n\nThis includes the following awards:\n\nComprehensive Examination Scholarship\n\tOutstanding Academic Performance Award\n\tTeaching Assistant Award\n\tAdditional scholarships as funds permit\nGraduate students can obtain information from the Graduate Officer or Graduate Secretary of the Department of Statistics and Actuarial Sience.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Mathematics",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Statistics &amp; Actuarial Science Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9951,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/statistics-actuarial-science-graduate-award"
    },
    {
      "id":1113,
      "title":"Sprott Scholarship",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"This award is named after Professor D.A. Sprott, the founding Chair of the Department of Statistics and Actuarial Science, and is made annually to a registered full-time student who has been recognized by the Department as having shown particular promise in research in the PhD program prior to the final approval of their thesis. The selection will be made by the Awards subcommittee of the Statistics and Actuarial Science Graduate Committee. The Graduate Committee can decide not to award the Sprott Scholarship in any year. The Department can agree to change the terms of the award at any time.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Mathematics",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Statistics &amp; Actuarial Science Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9952,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/sprott-scholarship"
    },
    {
      "id":1114,
      "title":"Susan Pearce &amp; Leslie Harwood Endowment",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship will be awarded annually to a full-time graduate student registered in the Faculty of Applied Health Sciences on the basis of scholastic excellence and a demonstrated interest in research related to aging and older populations, including Alzheimer's disease and dementia.\n\nThe goal is that this scholarship will be awarded in conjunction with major external scholarships that require a matching or enhancement component (e.g. OGS, NSERC, SSHRC, CIHR) as long as these programs are in effect.\u00a0 If the match or enhancement becomes unavailable or a suitable recipient cannot be found, the funds may be paid out as a regular graduate scholarship.\u00a0 This fund is made possible through donations from Ken Murray and his daughters, Susan Pearce and Leslie Harwood.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology",
        "Kinesiology",
        "Public Health",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your AHS Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9953,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/susan-pearce-leslie-harwood-endowment"
    },
    {
      "id":1115,
      "title":"Sylvia Knight Award in Fine Arts",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established by family and friends in memory of Sylvia Knight, a graduate of the University of Waterloo, who specialized in Fine Arts and was a long time supporter of the Department of Fine Arts. It will be awarded annually to a graduate student in the Master of Fine Arts program who has maintained at least a B+ average, and who has demonstrated excellence in studio work. The selection will be made by the Graduate Committee of the Department of Fine Arts each year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Fine Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Fine Arts Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9954,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/sylvia-knight-award-fine-arts"
    },
    {
      "id":1116,
      "title":"TD Bank Graduate Scholarship in the Environment",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The TD Bank Graduate Scholarships in the Environment are awarded annually to full-time UW graduate students who hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) and are enrolled in the faculties of Engineering, Environment or Science and in an area of study with a strong environmental focus.\n\nRecipients are chosen by each Faculty\u2019s Associate Dean of Graduate Studies. There are six awards valued at $5,000 each, two awards per faculty. Open to Canadian citizens and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Architecture",
        "Biology",
        "Environment &amp; Business",
        "Chemistry",
        "Environment &amp; Resource Studies",
        "MBET",
        "Chemical Engineering",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Civil &amp; Environmental Eng",
        "Environment",
        "Pharmacy",
        "Planning",
        "Electrical &amp; Computer Eng",
        "Physics",
        "Social Innovation",
        "Management Sciences",
        "Physics and Astronomy",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Vision Science",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9955,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/td-bank-graduate-scholarship-environment"
    },
    {
      "id":1117,
      "title":"Systems Design Engineering Memorial Award",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"These awards honour deceased students, alumni, faculty, staff and friends of the Department of Systems Design Engineering. Awards are made, as funds permit, to full-time undergraduate or graduate students in the Department of Systems Design Engineering on the basis of academic achievement. Selection will be made by the Associate Dean of Engineering, Graduate Studies and Research. Donations have been received in memory of: Professor Muthu Chandrashekar.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9956,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/systems-design-engineering-memorial-award"
    },
    {
      "id":1118,
      "title":"TD Graduate Bursary in the Environment",
      "status":"Active",
      "value":"$1,500-$5,000 - The value of each award will vary depending on financial need and available funds.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"Bursaries will be awarded annually to full-time or part-time graduate students in the Faculty of Environment who are in good academic standing and who have a demonstrated financial need as determined by Waterloo.\u00a0 The value of each award will vary depending on financial need and available funds.\u00a0 To be considered, students must complete the Waterloo Graduate Student Award application. This fund is made possible by a generous gift from TD Bank Group.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 1",
          "June 1",
          "October 1"
        ],
        "application":[
          "February 1",
          "June 1",
          "October 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Faculty of Environment Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10245,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/td-graduate-bursary-environment"
    },
    {
      "id":1119,
      "title":"The Frank and Azniv Lochan Family Foundation Award",
      "status":"Active",
      "value":"$2500: At least one award valued at $2,500 annually. The value and\/or number of awards may change from year to year.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"An award, valued at approximately $2,500 is awarded annually to a full-time or part-time graduate student enrolled in the Master of Taxation program in the School of Accounting and Finance in the Faculty of Arts who demonstrates strong and consistent academic performance and who has a demonstrated financial need as determined by UW.\u00a0\n\nFull-time students must have completed four courses during their fall term and be enrolled in four courses for spring term. Part-time students must have completed two courses in each of the fall and winter terms and be enrolled in two courses for the spring term.\n\nTo be considered, students must complete the Graduate Student Award Application and attach a short reflection (maximum 500 words) describing their learning experience in the program and why they are a candidate for this award.\u00a0\n\nThis fund is made possible by a donation from the Frank and Azniv Lochan Family Foundation.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "Taxation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Be an Ontario resident"
        ],
        "instructions":[
          "Graduate Award Application:"
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Taxation Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10497,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/frank-and-azniv-lochan-family-foundation-award"
    },
    {
      "id":1120,
      "title":"University of Waterloo Senate Graduate Scholarship",
      "status":"Active",
      "value":"Values vary but as a general rule, awards valued between $500 - $2,000.",
      "type":[
        "Scholarships"
      ],
      "description":"The Senate Graduate Scholarship program provides funds to match scholarship designated contributions made by faculty, staff, and retirees to graduate programs at the University of Waterloo.\u00a0 The spirit of the award is to give deserving students who are in good academic standing (minimum B+ standing), registered full-time within the time limits of their program, and who would not be in receipt of a major external scholarship (ie. OGS, tri-council) an award to help them out.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9959,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/university-waterloo-senate-graduate-scholarship"
    },
    {
      "id":1064,
      "title":"Bruker Biospin Graduate Scholarship",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Research specific awards"
      ],
      "description":"All graduate students registered in the Guelph-Waterloo Centre for Graduate Work in Chemistry, (GWC)2, during the year of nomination, whose research is in the field of chemical instrumentation. Chemical instrumentation shall be taken to include both the development and exploitation of instruments for solving chemical problems.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The awardee shall be selected on the basis of the quality of a research paper in the field of chemical instrumentation, published or in press, which was authored or co-authored by the student while registered in (GWC)2.",
          "Attention will be focused on the degree of exploitation of instrumental techniques, the scientific impact of the work, and on the student's participation in the design, execution and in particular in the writing up of the cited research. The scholarship is awarded for one year only. A previous scholar is not eligible for re-award for work in the same specialty."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Application or nomination to the selecting committee by deadline date each year. The application materials will include four copies of the paper in question and a letter from the student's supervisor documenting the degree of his\/her contribution to this work."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9903,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/bruker-biospin-graduate-scholarship"
    },
    {
      "id":1065,
      "title":"BlackBerry Scholarships in English Language and Literature",
      "status":"Active",
      "value":"Varies from $5,000 - $15,000.\u00a0 MA students will be eligible for one-year awards only.\u00a0 PhD students will be eligible for awards of one, two of three years' duration.",
      "type":[
        "Scholarships"
      ],
      "description":"BlackBerry is a leading designer, manufacturer and marketer of innovative wireless solutions for the worldwide mobile communications market.\u00a0 BlackBerry's portfolio of award-winning products, services and embedded technologies include BlackBerry wireless platform, the BlackBerry Wireless Handheld product line, software development tools, and software\/hardware licensing agreements.\u00a0 BlackBerry believes that it is important to give back to the local, national and international communities in which it operates.\u00a0 BlackBerry has a successful history of hiring graduates of the University of Waterloo's English Language and Literature department.\u00a0 The BlackBerry Graduate Scholarships in English Language and Literature are intended to promote the study of English literature, rhetoric, and digitial media and to provide financial support to students.\u00a0 Awards will be made to selected graduate students on the basis of their academic achievement and potential.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be enrolled full-time in a Masters or PhD in the English Language and Literature department.",
          "Be within the time limits of their program.",
          "Must be pursuing studies and research in the areas of Literacy Studies, Rhetoric and Communication Design, and Experimental Digital Media.",
          "Selection will be made by the associate chair for Graduate Studies in English Language and Literature, in consultation with the Departmental Graduate Committee.\u00a0 All eligible graduate students registered in the program will be automatically considered, without the need for a separate application.",
          "Selection and amount of scholarship will be based on the student's achievement and potential as a graduate student, as manifested in the student's existing academic record and in his or her graduate application for admission."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your English Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9904,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/blackberry-scholarships-english-language-and-literature"
    },
    {
      "id":1066,
      "title":"Beltz Essay Award",
      "status":"Active",
      "value":"$250",
      "type":[
        "Scholarships"
      ],
      "description":"Two awards, one each for M.A. and Ph.D. students. These prizes go to the best essays submitted in a course taken during the past calendar year by graduate students enrolled at some time during that year. Faculty nominations only. Two judges.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be enrolled in the Faculty of Arts, Department of English",
          "Have submitted an essay to a course taken the previous calendar year",
          "Applicants must:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your English Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9905,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/beltz-essay-award"
    },
    {
      "id":1067,
      "title":"Arthur F. Church Graduate Scholarship in Mechanical Engineering",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The Arthur F. Church Graduate Scholarships will be awarded annually to three full-time UW graduate students enrolled in Mechanical Engineering who hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). The recipients are chosen by the Associate Dean of Graduate Studies, Engineering.\u00a0 Students must be Canadian or permanent residents.\n\nThese scholarships are open to Canadian and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Mechanical &amp; Mechatronics Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9906,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/arthur-f-church-graduate-scholarship-mechanical-engineering"
    },
    {
      "id":1068,
      "title":"(GWC)2 Poster Prize",
      "status":"Active",
      "value":"1st prize $100 and 2nd prize $50.",
      "type":[
        "Scholarships"
      ],
      "description":"The Guelph-Waterloo Centre for Graduate Work in Chemistry and Biochemistry (GWC)2 provides a $100 First Prize and a $50 Second Prize for posters presented by current (GWC)2 MSc or PhD students at the (GWC)2 Annual General Meeting.\u00a0 The decision to give out the prizes is dependent on the availability of funds.\u00a0 The monetary prize will be determined by a selection committee as designated by the (GWC)2 Director and will be based on the candidates' poster presentation of their research.\u00a0 These prizes are open to all students who present posters during the (GWC)2 Annual General Meeting.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award",
      "vid":9907,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/gwc2-poster-prize"
    },
    {
      "id":1063,
      "title":"Charles S. Humphrey Graduate Fellowship in Chemistry",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship is administered by (GWC)2 and is awarded annually on a competitive basis. The monetary value of this award is $5,000 subject to the availability of funds. This competition is open to Canadian citizens who are registered in a full-time PhD program in the centre, preferably in organic chemistry. Candidates will be considered on the basis of their academic record. The graduate officers of (GWC)2 will bring to the co-ordinating committee the names of all eligible students on each campus of (GWC)2 by June 1 each year and the scholarship will be presented at the annual Saturday seminar of the centre. No application is necessary.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "The awardee shall be selected on the basis of a demonstration of ability and promise in research and his\/her performance in at least two graduate courses, with particular emphasis being placed on the former.",
          "The scholarship is awarded for one year only, but a previous scholar is eligible for a re-award of this scholarship.",
          "Special consideration will be given to outstanding students who do not currently hold other major awards."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9902,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/charles-s-humphrey-graduate-fellowship-chemistry"
    },
    {
      "id":1062,
      "title":"David Holden Memorial Scholarship",
      "status":"Active",
      "value":"$750",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship, administered by Guelph-Waterloo Centre for Graduate Work in Chemistry (GWC)2, is in memory of the late Professor David A. Holden and was established from funds donated by Professor Holden's friends, family and colleagues. It is awarded annually on a competitive basis and is open to all graduate students registered in the Guelph\/Waterloo Centre. Candidates will be considered on the basis of overall abilities, including both research and teaching components with special emphasis to be given to outstanding performance in Chem 794 (MSc Seminar), and to evidence of breadth of interest in areas outside chemistry, such as art and music.\u00a0Nominations will be solicited from Centre faculty and the graduate officers by November 15th of each year, and the scholarship will be presented at the Annual Saturday Seminar of the Centre. The scholarship will be presented at the Annual Saturday Seminar of the Centre.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The scholarship is awarded for one year only.",
          "A previous scholar is eligible for a re-award of this scholarship."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9901,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-holden-memorial-scholarship"
    },
    {
      "id":1061,
      "title":"Department of Chemistry Scholarship for Graduate Student Excellence",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $1,000, will be awarded annually to graduate students registered full-time in the Master\u2019s\/Doctoral program in the Department of Chemistry in the Faculty of Science.\u00a0 Selection will made annually in the Spring term by the Chemistry department on the basis of academic achievement and scholarly success in research.\n\nSelection will be based on scholastic excellence (minimum 80% cumulative average in their current program or over the last two full-time academic years) and demonstrated scholarly success in research.\u00a0 An application is not required; the department will identify candidates and select recipients normally each Spring.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The scholarship is awarded for one year only, but a previous scholar is eligible for a re-award of this scholarship.",
          "Special consideration will be given to outstanding students who do not currently hold other major awards."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10977,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/department-chemistry-scholarship-graduate-student-excellence-0"
    },
    {
      "id":1060,
      "title":"R.H.F. Manske Prize",
      "status":"Active",
      "value":"$750",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, administered by the Guelph-Waterloo Centre for Graduate Work in Chemistry (GWC)2, is in memory of the late Professor R.H.F. Manske and was established in 1983. It is awarded annually on a competitive basis and is open to all graduate students registered in the Guelph-Waterloo Centre. Candidates will be considered on the basis of overall abilities, including both research and course work. Nominations will be solicited from Centre faculty and the graduate officers by November 15th of each year. The scholarship will be presented at the Annual Awards Banquet of the Centre.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The scholarship is awarded for one year only, but a previous scholar is eligible for a re-award of this scholarship.",
          "Special consideration will be given to outstanding students who do not currently hold other major awards."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9899,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rhf-manske-prize"
    },
    {
      "id":1059,
      "title":"Mary Bales Graduate Scholarship in Arts",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"In 2002, Mary Bales, MA English 1972, MA Philosophy 1973 and 2002 recipient of the Arts Alumni Achievement Award, established a scholarship for graduate students in the Faculty of Arts. The student will hold an Ontario Graduate Scholarship (OGS). The Graduate Studies Committees in Arts, in consultation with the Associate Dean, Graduate Studies and Research, will make the selection.\n\nThis scholarship is open to Canadian citizens and permanent residents. Candidates will be selected based upon academic achievement and value of research to the Canadian economy and society.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Accounting",
        "Anthropology (Public issues)",
        "Arts",
        "Classical Studies",
        "Digital Experience Innovation",
        "Economics",
        "English",
        "Fine Arts",
        "French Studies",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Faculty of Arts Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9898,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/mary-bales-graduate-scholarship-arts"
    },
    {
      "id":1058,
      "title":"Lyle S. Hallman Graduate Research Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The Lyle S. Hallman Graduate Research Scholarship has been established for a student entering a graduate studies program in Applied Health Sciences. This award has been made possible through a donation from Lyle S. Hallman OC, LL.D.\u00a0 Mr. Hallman was a major benefactor of the University of Waterloo, local philanthropist and business leader.\n\nThe student will hold a major external award that has a matching or enhancement component. The selection will be made by the Associate Dean, Graduate Studies and Research and the three departmental Graduate Studies Officers. This scholarship is open to Canadian and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology",
        "Kinesiology",
        "Public Health",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Applied Health Sciences Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9897,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/lyle-s-hallman-graduate-research-scholarship"
    },
    {
      "id":1057,
      "title":"Kevin Kimsa MBET Graduate Scholarship",
      "status":"Active",
      "value":"$10000",
      "type":[
        "Scholarships"
      ],
      "description":"The Kevin Kimsa MBET Graduate Scholarship, valued at $10,000 per year, will be given to an eligible recipient entering the MBET program.\u00a0 The recipient will be selected by the MBET admissions committee based on previous academic accomplishments and the ability to demonstrate, during an interview process, the entre(intra)preneurial attributes required to successfully complete the program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          ""
        ],
        "enrollment_year":[
          ""
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Scholarship Coordinator for further information regarding this award.",
      "vid":9896,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/kevin-kimsa-mbet-graduate-scholarship"
    },
    {
      "id":1056,
      "title":"Keith and Winifred Shantz Master of Fine Arts Internship",
      "status":"Active",
      "value":"$7000",
      "type":[
        "Scholarships"
      ],
      "description":"This internship was originally funded through generous donations from the late Winifred Shantz followed by a generous donation from the estate of Keith Shantz (Winfred\u2019s late husband). Each year, M.F.A students who have completed a minimum of two terms of study spend at least six weeks of the summer months working as assistants in a professional artist\u2019s studio. On completion of internship the students devote the balance of the term to developing their work in their own studios. The Keith and Winifred Shantz Master of Fine Arts Internship Fund will provide at least one internship with a value of at least $7,000 to cover the accommodation, living and travel expenses and tuition for that term.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Fine Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Full-time graduate students registered in the Master of Fine Arts program in the Faculty of Arts, typically in their third term.",
          "UW Department of Fine Arts faculty will identify candidates and select recipients."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Fine Arts Department Gradaute Scholarship Coordinator for further information regarding this award.",
      "vid":9895,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/keith-and-winifred-shantz-master-fine-arts-internship"
    },
    {
      "id":1069,
      "title":"(GWC)2 Graduate Seminar Prize",
      "status":"Active",
      "value":"$100",
      "type":[
        "Scholarships"
      ],
      "description":"The prize, administered by Guelph-Waterloo Centre for Graduate Work in Chemistry (GWC)2, was established in 1984. It is awarded annually to any graduate student who presents his\/her MSc or PhD Seminar in the previous academic year. The seminar prize is presented to two students on each campus each year. The nomination by the supervisory committee at the time of seminar presentation is to be based on the assessment of the supervisory committee and of the member of the MSc\/PhD class attending that seminar.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Scholarship Coordinator for further information regarding this award",
      "vid":9908,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/gwc2-graduate-seminar-prize"
    },
    {
      "id":1070,
      "title":"Bonnie Ho Memorial Award in Masters of Accounting",
      "status":"Active",
      "value":"$2000: At least one award valued at $2,000 annually. The value and\/or number of awards may change as funds permit.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"This scholarship was established in loving memory of Bonnie Ho, a Bachelor of Arts '02 and Masters of Accounting '03 graduate, respectively. An award, valued at $2,000 is awarded annually to a full-time student entering the Masters of Accounting program at the School of Accountancy that has a minimum overall average of 80% and has demonstrated financial need. In reflection of Bonnie's finest attributes, this student must also demonstrate academic excellence, professionalism, compassion and have an interest in athletics, community service or other student activities.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:",
          "Letter explaining how you meet the award criteria",
          "Resume required"
        ],
        "additional":[
          "In addition to the application include a\u00a0 copy of a recent grade report."
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
        
      ],
      "contact":"Please contact the School of Accounting Graduate Coordinator for further information regarding this award",
      "vid":10862,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/bonnie-ho-memorial-award-masters-accounting"
    },
    {
      "id":1082,
      "title":"Gage-Babcock Graduate Fire Safety Award",
      "status":"Active",
      "value":"$4000",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $4,000 will be awarded annually to a graduate student enrolled in the MEng, MASc or PhD programs in Mechanical Engineering (Fire Safety) in the Faculty of Engineering.\u00a0 Selection will be based on academic achievement (minimum 80% cumulative) and a proven interest and involvement in fire safety research.\u00a0 Preference will be given to those students not already employed in the Fire Safety industry. Interested students should submit an application by September 30th. This fund is made possible by a donation from Gage-Babcock Associates Limited.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Interested students should submit an application to the Graduate Coordinator, Department of Mechanical and Mechatronics Engineering by September 30th"
        ]
      },
      "deadlines":{
        "term":[
          "September 30"
        ],
        "application":[
          "September 30"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Mechanical &amp; Mechatronics Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":10675,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/gage-babcock-graduate-fire-safety-award"
    },
    {
      "id":1081,
      "title":"QNX Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The QNX Graduate Scholarships were created by Mr. Dan Dodge, founder of QNX Software Systems to create opportunities for graduate students similar to those he received as an undergraduate and graduate student at the University of Waterloo.\n\nScholarships valued at $15,000 each, will be awarded annually to full-time University of Waterloo graduate students in the Faculty of Mathematics, School of Computer Science, the Faculty of Engineering and the Faculty of Science, Department of Physics, who hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). It is the intention to award these scholarships in conjunction with OGS or QEII-GSST, however, if this is not feasible, the scholarships will then be valued and awarded at $5,000 each.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Physics",
        "Management Sciences",
        "Physics and Astronomy",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9920,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/qnx-graduate-scholarship"
    },
    {
      "id":1080,
      "title":"Psychology Memorial Award",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"Awards honour deceased students, alumni, staff, faculty and friends of the Department of Psychology. Contributions have been received in memory of: D.M. Amoroso, K.S. Bowers, M. Briedenbaugh, M.P. Bryden, Z. Kunda, and R.H. Walters. Awards are made, as funds permit, to outstanding graduate and\/or Honours undergraduate students in Psychology based on academic excellence. Selection will be made by the department in consultation with the graduate and undergraduate Chairs.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Psychology"
      ],
      "application":{
        "type":[
          ""
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Scholarship Coordinator for further information regarding this award.",
      "vid":9919,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/psychology-memorial-award"
    },
    {
      "id":1079,
      "title":"Professor M.Z. Cohn Graduate Scholarship",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $1,000 will be awarded annually to a Waterloo graduate student registered full-time in the department of Civil &amp; Environmental Engineering.\u00a0 Preference will be given to students conducting research in the area of Structures, Mechanics and Construction Engineering. The scholarship will be awarded to a graduate student on the basis of scholastic excellence. This scholarship has been established through a generous donation by the late Professor Mircea Z. Cohn.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Civil and Environmental Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9918,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/professor-mz-cohn-graduate-scholarship"
    },
    {
      "id":1078,
      "title":"Peter F. Bronfman Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"Bob Harding, Linda Young and the Edper Foundation have established a scholarship fund in the name of Mr. Peter F. Bronfman for graduate students at the University of Waterloo. The students will hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). The selection will be made by the Associate Dean, Graduate Studies in conjunction with Faculty Associate Deans for Graduate Studies. This scholarship is open to Canadian and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9917,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/peter-f-bronfman-graduate-scholarship"
    },
    {
      "id":1077,
      "title":"Perimeter Scholars International Award",
      "status":"Active",
      "value":"$30000",
      "type":[
        "Scholarships"
      ],
      "description":"Students accepted into the Perimeter Scholars International Program will be eligible for full financial support of their program.\u00a0 UW will provide tuition scholarships and Perimeter Institute will provide awards intended to cover expenses related to travel, housing, food, textbooks and reference material, student services fees, and incidental stipends as assessed by PI.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Earth &amp; Environmental Sciences",
        "Pharmacy",
        "Physics",
        "Physics and Astronomy",
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "All students accepted to the Perimeter Scholars International Program are eligible and will receive the award."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Science Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9916,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/perimeter-scholars-international-award"
    },
    {
      "id":1076,
      "title":"Peggy and Tom Mulligan Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The Peggy and Tom Mulligan Scholarship will be awarded alternate years to a full-time UW graduate student in the dept of Civil Engineering or the School of Computer Science who holds an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). The first scholarship will be awarded to a graduate student in Civil Engineering and therefore in the second year to a graduate student in the School of Computer Science. The recipient is chosen by the Associate Dean of Graduate Studies, Faculty of Engineering or Mathematics depending on the year. There is one award valued at $15,000 ($5,000 from the endowment and $10,000 from government matching funds). \u00a0\n\tThe scholarship is open to Canadian residents. The scholarship will be awarded from the endowment fund starting in 2008.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9915,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/peggy-and-tom-mulligan-graduate-scholarship"
    },
    {
      "id":1075,
      "title":"Paul Seligman Memorial Scholarship",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established in memory of Professor Paul Seligman. It will be awarded annually to a first year graduate student in Philosophy. Special consideration will be given to students who have already demonstrated excellence in the areas that Professor Paul Seligman had worked in, most notably ancient philosophy, Jewish thought, and the philosophy of religion. All newly-admitted first-year graduate students in Philosophy will be eligible for the award. Announcement of the award is expected by June 30 each year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Philosophy",
        "Religious Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Philosophy Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9914,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/paul-seligman-memorial-scholarship"
    },
    {
      "id":1074,
      "title":"Nantes Graduate Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $1,000 will be provided annually to a full-time graduate student registered in the Master\u2019s or Doctoral program in the Department of French Studies in the Faculty of Arts at the University of Waterloo.The student must be working as a Teaching Assistant at the University of Nantes in France, or in some cases when this is not possible, the student will create a cultural report during their time in Nantes.\n\nThis fund is made possible by donations from alumni and faculty to the French Department trust fund.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "French Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Selection to be based on students in good standing, and working at the University of Nantes, France.",
          "An application is not required.",
          "The decision will be based on merit, a minimum cumulative average of 80%, and progress in the program, related to the completion of program exams.",
          "The Chair of the French Department will identify the candidate(s) and select recipient(s) each Fall and\/or Winter."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your French Studies Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9913,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/nantes-graduate-award"
    },
    {
      "id":1073,
      "title":"Patricia M. Rowe and M. Philip Bryden Psychology Travel Award",
      "status":"Active",
      "value":"$500: One award of $500 will be awarded each term.",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $500, is provided three times annually to graduate students registered full-time in the Department of Psychology in the Faculty of Arts. The purpose of the award is to assist with travel expenses students may incur when attending and presenting their research findings at national and international conferences or when traveling to engage in professional development activities.\n\nThis fund is made possible by a donation from Dr. Patricia M. Rowe. Dr. Rowe and her late husband Dr. M. Philip Bryden both served as faculty members in the department of Psychology at the University of Waterloo. It is Dr. Rowe\u2019s wish to provide future generations of graduate students in Psychology the opportunity to share their research and develop professionally with the national and international psychology community.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Psychology"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Full-time graduate students registered in the master\u2019s or doctoral program in the Psychology Department in the Faculty of Arts at the University of Waterloo",
          "Students must be beyond the first year (term 3.0) of their graduate program",
          "Student must use the funds for travel to present at a regional or international conference or to participate in professional development activities",
          "In Spring or Fall term, preference will be given to students traveling to present at a conference and students will be considered for this award at the time they apply for a GSO Travel Assistantship award; selection to be based on criteria for the GSO Travel Assistantship fund",
          "In Winter term, preference will be given to students traveling for professional development activities (separate application available in the department of Psychology); should there be no eligible Winter term professional development applicants the award will be given to a student traveling to present at a conference in accordance with the GSO Travel Assistantship award",
          "Preference will be given to students who have not previously received this Award"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "March 15th for Spring term travel",
          "July 15th\u00a0 for Fall term travel",
          "November 15th for Winter term travel",
          "Interested students should submit their travel assistantship application to the department of Psychology by the appropriate deadline:",
          "Based on applicaitons, the department of Psychology will identify candidates and make the selection every term.",
          "This award may be used to replace the Psychology department\u2019s funding contribution to the student\u2019s GSO Travel Assistantship award, but not necessarily the Faculty and\/or supervisor\u2019s contribution"
        ]
      },
      "deadlines":{
        "term":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "application":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Psychology Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9912,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/patricia-m-rowe-and-m-philip-bryden-psychology-travel-award"
    },
    {
      "id":1072,
      "title":"Bob Graham Memorial Scholarship",
      "status":"Active",
      "value":"Varies.",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"This scholarship was established by the friends and family of the late Bob Graham, an Associate Professor in Recreation and Leisure Studies, and a doctoral student in the School of Planning.\n\nGraduate students in their second year of Applied Health Sciences or Environmental Studies with an overall average of B+, and financial need are eligible to apply. The area of study must be terrestrial and marine parks and conservation, especially the integration of social science and natural science information, cooperative management, interpretation\/environmental education or customary and traditional ecological knowledge.\n\nIt is desirable that students have evidence of volunteer commitment or employment with the following parks and conservation organizations: Parks Canada, Ontario Ministry of Natural Resources, Natural Wildlife Areas, conservation authorities, Canada Parks and Wilderness Society, Federation of Ontario Naturalists, World Wildlife Fund Canada, cooperating associations, or similar organizations.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Environment &amp; Business",
        "Health Studies\/Gerontology",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "Geography &amp; Environmental Mgmt",
        "Public Health",
        "Environment",
        "Planning",
        "Recreation &amp; Leisure Studies",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/group\/35"
      ],
      "contact":"Please contact the Coordinator, Graduate Financial Aid &amp; Awards in the Graduate Studies Office for further information regarding this award.",
      "vid":10236,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/bob-graham-memorial-scholarship"
    },
    {
      "id":1071,
      "title":"Mik Pintar Scholarship in MRI Applications",
      "status":"Active",
      "value":"$2000: Award value can vary.",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $2,000, will be awarded annually to a full-time UW graduate student registered in the Faculty of Science engaged in research involving porous media and\/or medical applications of NMR or MRI.\u00a0 Students studying in the area of biophysics may also be considered.\u00a0 The scholarship will be awarded on the basis of scholastic excellence.\u00a0 Students must be Canadian citizens or permanent residents of Canada.\u00a0 This scholarship has been established by Sandra Burt in commemoration of the many contributions that Mik Pintar (Professor of Physics, 1967-2002) made to Nuclear Magnetic Research, and to the teaching and training of students at the University of Waterloo.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Earth &amp; Environmental Sciences",
        "Pharmacy",
        "Physics",
        "Physics and Astronomy",
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Faculty of Science Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9910,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/mik-pintar-scholarship-mri-applications"
    },
    {
      "id":1083,
      "title":"Frederick W. Bent Memorial Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established by family and friends in honour of Frederick W. Bent (October 30, 1968 - September 29, 2003) to provide assistance to students enrolled in the Faculty of mathematics, computer science programs.\u00a0 Fred graduated with honours in 1994, with a Master's in Mathematics, Computer Science.\u00a0 He went on to become a successful executive for a local firm before his untimely death.\u00a0 He will always be remembered for his quick and dry wit, his sense of honour, his kindness and selfless generosity.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "This scholarship be paid as the institutional matching funds for a recipient of an Ontario Graduate Scholarship (OGS) or Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) in the David R. Cheriton School of Computer Science.\u00a0",
          "The selection will be made by the Associate Chair\/Graduate Officer of Computer Science.\u00a0",
          "Preference will be given to students from the Golden Triangle area."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the David R. Cheriton School of Computer Science Graduate Coordinator for further information regarding this award.",
      "vid":9922,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/frederick-w-bent-memorial-graduate-scholarship"
    },
    {
      "id":1055,
      "title":"Gladys Srivastava Graduate Award",
      "status":"Active",
      "value":"$5000: This award will be paid as the institutional matching funds for the OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship valued at $5,000 will be awarded every other year to a full-time University of Waterloo graduate student in the Department of English Language and Literature with a focus on Literary, Rhetorical, or Digital-Media Studies in the Faculty of Arts. The scholarship will be awarded to a graduate student on the basis of scholastic excellence and a demonstrated interest in English Language and Literature, Rhetoric and\/or Digital Media. Preference will be given to a student who holds an Ontario Graduate Scholarship (OGS) or another major external scholarship that requires a matching or enhancement component. If the match or enhancement becomes unavailable or a suitable recipient cannot be found, the funds will be paid out as a regular graduate scholarship. This scholarship has been established by The Srivastava Family in honour and with fond memories of Gladys Srivastava.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your English Department Graduate Coordinator for further information regarding this award.",
      "vid":9894,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/gladys-srivastava-graduate-award"
    },
    {
      "id":1054,
      "title":"Golder Associates Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"Two scholarships, valued at $5,000, will be awarded to full-time University of Waterloo graduate students.\u00a0 One scholarship will be awarded to a student in the Faculty of Science and the other scholarship will be awarded university-wide.\u00a0 The scholarships will be awarded to graduate students on the basis of scholastic excellence and demonstrated success in Water Research.\u00a0 This scholarship has been established by Golder Associates, a leader in ground engineering, and environmental services.\u00a0 Their stated mission is to use their skills and experience to \u201cEngineer Earth\u2019s development while preserving Earth\u2019s integrity\u201d.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Complete the Water Institute graduate scholarships application form found on our forms webpage and submit to the Water Institute."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/water.uwaterloo.ca\/"
      ],
      "contact":"Please contact Water Institute for further information regarding this award.",
      "vid":10514,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/golder-associates-graduate-scholarship"
    },
    {
      "id":1042,
      "title":"James E. Curtis Memorial Scholarship",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships"
      ],
      "description":"One scholarship, valued at $2,000 awarded annually to an outstanding full-time graduate student who also demonstrates leadership while helping to exemplify the spirit and direction of Professor Curtis' work and career, including service to the community and to other students.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Sociology and Legal Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Awarded to a full-time graduate student normally registered in Sociology.\u00a0 Students from other programs whose research and approaches embody the spirit of the work of Professor Curtis are also eligible to apply."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Interested candidates should submit visit the Sociology and Legal Studies Website for details."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Sociology &amp; Legal Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":9881,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/james-e-curtis-memorial-scholarship"
    },
    {
      "id":1041,
      "title":"Jon W. Mark Graduate Scholarship in Communication",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The Jon W. Mark Graduate Scholarship in Communication at the Department of Electrical and Computer Engineering is established to honor the significant accomplishments and contribution of Dr. Mark, including serving as form Chair of the Department of Electrical and Computer Engineering, being recognized as a Distinguished Professor Emeritus, Life Fellow of IEEE, Fellow of the Canadian Academy of Engineering, and Founder and Director of the Centre for Wireless Communications, in company with more than forty years of services as an eminent teacher, distinguished researcher, and mentor to hundreds of engineers, faculty and staff.\n\nThis scholarship is established to honor Dr. Jon Mark and continue his legacy, while paying the way for the successful careers of new graduates in the Department of Electrical and Computer Engineering in the area of Communication.\n\nFive scholarships valued at $5,000 each will be awarded annually to graduate students in the Faculty of Engineering's Electrical &amp; Computer Engineering department, with preference given to students involved with communication research.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Electrical &amp; Computer Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Full Time UW Graduate students enrolled in the Faculty of Engineering (Electrical and Computer Engineering), with preference given to students specializing in the communication research area.",
          "The selection will be made by the Associate Dean, Graduate Studies, Faculty of Engineering, in consultation with the Department of Electrical and Computer Engineering."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Electrical &amp; Computer Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9880,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jon-w-mark-graduate-scholarship-communication"
    },
    {
      "id":1040,
      "title":"Joseph Wai-Hung Liu Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $5,000 will be awarded annually to a full-time University of Waterloo graduate student registered in any unit of the Faculty of Mathematics.\u00a0 The scholarship will be awarded to a graduate student on the basis of scholastic excellence who holds an Ontario Graduate Scholarship (OGS) or another major external scholarship that requires a matching or enhancement component.\u00a0 If the match or enhancement becomes unavailable or a suitable recipient cannot be found, the funds will be paid out as a regular graduate scholarship.\u00a0 This scholarship has been established by Waterloo graduate Dr. Joseph Liu, MMath 1972, PhD Computer Science, 1976.\u00a0 Dr. Liu was a professor of Computer Science at York University, his two sons graduated from Waterloo in Software Engineering and Systems Design Engineering and he has a strong commitment to graduate education and to the Faculty of Mathematics at the University of Waterloo.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Mathematics Department GraduateCoordinator for further information regarding this award.",
      "vid":9879,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/joseph-wai-hung-liu-graduate-scholarship"
    },
    {
      "id":1039,
      "title":"Kenneth Stollery Memorial Graduate Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"An award, valued at a minimum of $1000 will be awarded (when funds permit), to a graduate student enrolled in the Masters or PhD program in the Department of Economics, Faculty of Arts who demonstrates academic excellence and financial need. Applicants are to apply using the Graduate Student Award Application form found online.\n\nApplications are to be submitted to the Graduate Studies Office, Needles Hall. The final selection will be made by the Chair and Associate Chair\/Graduate Officer in the Department of Economics.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "Economics"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 15"
        ],
        "application":[
          "February 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Economics Department Graduate Coordinator for further information regarding this award.",
      "vid":10240,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/kenneth-stollery-memorial-graduate-award"
    },
    {
      "id":1037,
      "title":"Lea Vogel-Nimmo English Graduate Professionalization Award",
      "status":"Active",
      "value":"$750",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship will be provided annually to full-time graduate students registered in the Master\u2019s or PhD program in the Department of English language and Literature in the Faculty of Arts on the basis of academic excellence (minimum 80%) and merit of professionalization activities (e.g. research travel costs or conference attendance). Students will be chosen by the Associate Chair for Graduate Studies in English Language and Literature, in consultation with the Department Graduate Committee. This fund is made possible by a donation from David Clarence Nimmo in memory of his late wife Lea Vogel-Nimmo who, via the generosity of others, was given opportunities to develop her artistic talent and reach her professional goals.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Selection will be made by the Associate Chair for Graduate Studies in English Language and Literature, in consultation with the Departmental Graduate Committee."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "An application is required:",
          "The student must submit, to the English department, a short (250 word) description of how the professionalization funds will be used e.g. research travel costs, conference attendance or special research expenditures."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the English Department Graduate Coordinator for further information regarding this award.",
      "vid":9876,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/lea-vogel-nimmo-english-graduate-professionalization-award"
    },
    {
      "id":1036,
      "title":"McNeil Graduate Scholarship Award in Natural Products Chemistry",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"The McNeil Graduate Scholarship Award in Natural Products Chemistry is available to a full-time graduate student registered in the PhD program of the Guelph-Waterloo Centre for Graduate Work in Chemistry (GWC)2, provided that the research lies in the area of structural elucidation\/synthesis of biologically significant compounds. Nominations will be solicited from the (GWC)2 faculty and the Graduate Officers by November 15th of each year. The coordinating committee of (GWC)2, or a subcommittee thereof appointed by the Director, to include a representative from McNeil Consumer Products Company, will make the selection of the award.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Biology Department Graduate Coordinator for further information regarding this award.",
      "vid":9875,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/mcneil-graduate-scholarship-award-natural-products-chemistry"
    },
    {
      "id":1034,
      "title":"Merck Frosst Biochemistry Award",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"The Merck Frosst Biochemistry scholarship will be awarded annually. All graduate students currently registered at the Guelph-Waterloo Centre for Graduate Work in Chemistry (GWC)2 are eligible provided that their research is in the field of biochemistry. The awardee shall be selected on the basis of a demonstration of ability and promise in research and his\/her performance in at least two graduate courses, with particular emphasis being placed on the former. The selection committee will be made up of the Coordinating Committee of the Guelph-Waterloo Centre for Graduate Work in Chemistry, or a subcommittee thereof appointed by the Director. Nominations will be solicited from Centre faculty and the Graduate Officers by June 1 of each year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Biology or Chemistry Department Graduate Coordinator for further information regarding this award.",
      "vid":9873,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/merck-frosst-biochemistry-award"
    },
    {
      "id":1043,
      "title":"James &amp; Elise Devitt Graduate Scholarship",
      "status":"Active",
      "value":"$5000: Two scholarships annually, valued at up to $5,000 each.",
      "type":[
        "Scholarships"
      ],
      "description":"Two scholarships, valued at up to $5,000 each, will be awarded annually to full-time University of Waterloo graduate students in any UW graduate program.\u00a0 The fund is made possible by a donation from Elise Devitt, UW retired staff member, in memory of her husband, T. James Devitt.\n\tThe scholarship will be awarded on the basis of scholastic excellence and financial need and a demonstrated interest in graduate studies.\u00a0 Recipients must be an Ontario resident. The selection will be made by the Graduate Studies Office on a university-wide rotating basis.\n\nStudents will apply using a Graduate Student Award Application form found online.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for the 12 months prior to their post-secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "October 15"
        ],
        "application":[
          "October 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Coordinator, Graduate Awards &amp; Financial Aid for further information regarding this award.",
      "vid":10238,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/james-elise-devitt-graduate-scholarship"
    },
    {
      "id":1044,
      "title":"Jack Young Bursary",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"A bursary fund has been established by Jack Young, the first Chair of the Regional Municipality of Waterloo, to assist full-time undergraduate and\/or graduate School of Urban and Regional Planning students. Funds will be allocated based on financial need and a minimum Planning average of 70%.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Environment",
        "Planning"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "This bursary is administered by Student Awards Office - students must apply on graduate bursary application by bursary deadline.\u00a0"
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/"
      ],
      "contact":"Please contact your the Student Awards &amp; Financial Aid Office for further information about this award.",
      "vid":9883,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jack-young-bursary"
    },
    {
      "id":1053,
      "title":"Graduate Student Instructor Award in Philosophy",
      "status":"Active",
      "value":"$200",
      "type":[
        "Scholarships"
      ],
      "description":"One award valued at $200 will be given annually to a Philosophy graduate student to acknowledge excellence as a Graduate Student Instructor in the Department of Philosophy.\u00a0 Students who were Student Instructors in any of the three terms in the previous year are eligible to be considered for this award.\u00a0 Selection is made by the Faculty annually in May and will be based on teaching evaluation scores, professional development courses completed, student comments, and track record of competent and successful administration of courses.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Philosophy"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9892,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/graduate-student-instructor-award-philosophy"
    },
    {
      "id":1052,
      "title":"Graduate Student Teaching Assistant Award in Philosophy",
      "status":"Active",
      "value":"$200",
      "type":[
        "Scholarships"
      ],
      "description":"One award valued at $200 will be given annually to a Philosophy graduate student to acknowledge excellence as a Teaching Assistant in the Department of Philosophy.\u00a0 Students who were Teaching Assistants in any of the three terms in the previous year are eligible to be considered for this award.\u00a0 Selection is made by the Faculty annually in May and will be based on evidence of good teaching as determined by faculty members who have worked with the TAs.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Philosophy"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9891,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/graduate-student-teaching-assistant-award-philosophy"
    },
    {
      "id":1051,
      "title":"Guy Poirier Graduate Dissertation Award in French Studies",
      "status":"Active",
      "value":"$1200",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship will be presented annually to a graduate student in the Department of French Studies who has the best dissertation for the year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "French Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your French Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":9890,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/guy-poirier-graduate-dissertation-award-french-studies"
    },
    {
      "id":1050,
      "title":"H.G. McLeod Scholarship",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"This scholarship, administered by (GWC)2, has been donated by Professor F.W. Karasek, Distinguished Professor Emeritus of the Chemistry Department at University of Waterloo. It is awarded annually (as long as the funding is continued) on a competitive basis. This competition is open to all graduate students registered in the Guelph-Waterloo Centre, provided that their research is in the field of physical chemistry. Candidates will be considered on the basis of overall abilities, including both research and coursework. Nominations will be solicited from Centre faculty and the graduate officers by the deadline date each year. The scholarship will be presented at the Annual Seminar of the Centre.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Chemistry Department Graduate Coordinator for further information regarding this award.",
      "vid":9889,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/hg-mcleod-scholarship"
    },
    {
      "id":1049,
      "title":"Hertha Brichta Award for German Studies",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"This prize is normally awarded annually to a graduate student who is registered in either the MA or PhD program at the University of Waterloo or an outstanding applicant to one of these programs. Students who have achieved excellent results in her\/his academic studies during the previous calendar year and who are Canadian citizens\/permanent residents are eligible. Students must be nominated by a faculty member in February. The prize will be adjudicated by the German faculty of the Department of Germanic and Slavic Studies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "German\/Russian"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your German Department Graduate Coordinator for further information regarding this award.",
      "vid":9888,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/hertha-brichta-award-german-studies"
    },
    {
      "id":1048,
      "title":"Hira and Kamal Ahuja International Graduate Scholarship",
      "status":"Active",
      "value":"$20000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship, valued at $20,000 will be provided annually to a full-time graduate student with a valid Canadian study permit enrolled in the Masters or Doctoral program in the Faculty of Engineering on the basis of academic excellence (minimum 80%). Preference will be given to students who either completed their undergraduate degree at Thapar University in Punjab or graduated from an Indian Institute of Technology (IIT) and who have been living in India. This scholarship is made possible by a donation from Professor Hira Ahuja. Students must be full-time graduate student with a valid Canadian study permit enrolled in the Masters or Doctoral program in the Faculty of Engineering on the basis of academic excellence (minimum 80%). Preference will be given to students who either completed their undergraduate degree at Thapar University in Punjab or graduated from an Indian Institute of Technology (IIT) and who have been living in India.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9887,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/hira-and-kamal-ahuja-international-graduate-scholarship"
    },
    {
      "id":1047,
      "title":"Innovation Showcase MBET Awards",
      "status":"Active",
      "value":"1st Prize = $1,500\n\n2nd Prize = $1,000\n\nPeople\u2019s Choice Award = $500\n\nAll award values split between team members",
      "type":[
        "Scholarships"
      ],
      "description":"The Innovation Showcase MBET Awards are open to students registered in the Masters of Business, Entrepreneurship and Technology program.\u00a0 Students work in teams throughout the year to bring a new venture through the commercialization process \u2013 seed, development, launch.\u00a0\u00a0 Teams with the best investor pitches, as determined by their instructor, are invited to compete in the Innovation Showcase Pitch Competition in June.\u00a0\u00a0 Adjudicated by members of the entrepreneurial community, teams are given scores based on the venture and product; the competition and market; financials; teamwork; and, presentation delivery.\u00a0 The team with the highest score wins $1500 and the team with the second highest score wins $1000.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your CBET Department Graduate Coordinator for further information regarding this award.",
      "vid":9886,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/innovation-showcase-mbet-awards"
    },
    {
      "id":1046,
      "title":"Jack Rosen Memorial Award for Environmental Innovation",
      "status":"Active",
      "value":"One Grand Prize, valued at $1,000, is awarded for the best idea as determined by an independent panel of judges.\u00a0 The winning student(s) of the Grand Prize may also receive a consultation with an industry or business expert.\u00a0 One submission will be awarded a $500 People's Choice Award, as determined by ballots cast while submission s are on display.\u00a0 At the discretion of the judging panel up to two Honourable Mentions of $500 each may be awarded.\u00a0",
      "type":[
        "Scholarships"
      ],
      "description":"Award funding is available annually to full time undergraduate or graduate students enrolled in the Faculty of Environment.\u00a0 The successful students or student teams (up to three individuals, all from the Faculty of Environment) will have demonstrated an innovative idea aimed at solving environmental challenges or issues.\u00a0\n\nInterested student(s) will design a digital poster that describes their environmental idea and submit it to https:\/\/uwaterloo.ca\/environment\/jack-rosen-award\/apply.\u00a0 The best ten posters, as selected by judges will be put on display for one week in March where students or visitors will have the opportunity to vote for their favourite concept.\u00a0 One Grand Prize, valued at $1,000, is awarded for the best idea as determined by an independent panel of judges.\u00a0 The winning student(s) of the Grand Prize may also receive a consultation with an industry or business expert.\u00a0 One submission will be awarded a $500 People's Choice Award, as determined by ballots cast while submission s are on display.\u00a0 At the discretion of the judging panel up to two Honourable Mentions of $500 each may be awarded.\u00a0\n\nThis award is sponsored by the Jack and Honey Rosen Charitable Foundation in recognition of Jack Rosen's extraordinary vision and commitment to environmental issues in the K-W area and across the country.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/environment\/jack-rosen-award\/apply.\u00a0",
        "https:\/\/uwaterloo.ca\/graduate-studies\/graduate-awards\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Environment Department Graduate Coordinator for further information regarding this award.",
      "vid":9885,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jack-rosen-memorial-award-environmental-innovation"
    },
    {
      "id":1045,
      "title":"Jack Wiseman Award",
      "status":"Active",
      "value":"Varies from $500 - $1,000",
      "type":[
        "Scholarships"
      ],
      "description":"One award of $500 is presented annually to an outstanding third or fourth year undergraduate student or a graduate student in Civil Engineering who demonstrates a commitment to Construction or Project Management through course work, project work or work term job experience.\u00a0 The same student is not eligible to receive this award more than once.\u00a0 Students should apply by October 31 each year.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Access the application on the SAFA Forms page."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact teh Civil &amp; Environmental Department Graduate Coordinator for further information regarding this award.",
      "vid":9884,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jack-wiseman-award"
    },
    {
      "id":998,
      "title":"Davis Memorial Scholarship in Ecology",
      "status":"Active",
      "value":"$5000: $5,000 each split across the Fall and Winter terms.",
      "type":[
        "Scholarships"
      ],
      "description":"Scholarships have been established in memory of Robert M. and Doreen M. Davis. The scholarships will be awarded annually to outstanding University of Waterloo graduate students in the field of ecology. Payments will be made in the Fall and Winter terms. Selection will be made by the Advisory Committee on Graduate Scholarships and Awards. Students must have a first-class average (80%) in the last two completed years of study.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award. Each department will set their own deadline.",
      "vid":10313,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/davis-memorial-scholarship-ecology"
    },
    {
      "id":999,
      "title":"David Zaharchuk Memorial Bursary",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"This award has been established in memory of David Zaharchuk, a doctoral student in the Department of Chemical Engineering. The University of Waterloo wished to honour David, and at the request of David's family, the bursary was established. Full-time graduate students registered in any discipline at the University of Waterloo may apply. The students need to be in good standing with proven financial need. This bursary will be adjudicated in the Fall term. Students must complete the Graduate Student Award Application found online.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to post-secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "October 15"
        ],
        "application":[
          "October 15"
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Coordinator, Graduate Awards &amp; Financial Aid for further information regarding this award.",
      "vid":10237,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-zaharchuk-memorial-bursary"
    },
    {
      "id":1000,
      "title":"Canadian Water Resources Association (CWRA) Scholarship in Water Resources",
      "status":"Active",
      "value":"5 scholarships annually:\n\nDillon Consulting Scholarship - $5,000 - awarded to the highest ranked applicant. Funding is provided by Dillon Consulting Ltd. on an annual basis\n\tKen Thomson Scholarship - $2,000 - awarded to the second highest ranked applicant. Awarded from a special fund set up in his honour. \u2022 CWRA Memorial Scholarship - $1,500 - a tribute to CWRA Members remembered by their colleagues donations to the Scholarship Fund\n\t2 Scholarships - $1,500 each funded from the general funds of the Canadian Water Resources Association",
      "type":[
        "Scholarships"
      ],
      "description":"CWRA's\u00a0strategic direction is guided by the following:\n\nMission - Promoting effective water management.\n\nVision -Water resources are managed with a commitment to environmental, economic and social sustainability.\n\nObjectives\n\nto stimulate awareness and understanding of Canada\u2019s water resources\n\tto encourage recognition of the high priority and value of water\n\tto provide a forum for the exchange of information and opinion relating to the management of Canada\u2019s water\n\tto participate with appropriate agencies in international water management activities.\nThe Canadian Water Resources Association annually offers five scholarships awarded to graduate students whose programs of study focus on applied, natural, or social science aspects of water resources.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Academic excellence",
          "Project relevance to water management and development",
          "Available to graduate students whose programs of study focus upon applied, natural, or social science aspects of water resources.",
          "Awarded primarily on:",
          "The scholarships are open to Canadian citizens or landed immigrants attending a Canadian university or college who are enrolled in full-time graduate studies in any discipline in both Fall and Winter terms of 2015-2016 academic year.",
          "All applicants will receive a one-year membership in the Canadian Water Resources Association."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "A completed application form",
          "A 500-word statement which outlines the applicant\u2019s research project and its relevance to sustainable water resources. This statement should focus on the research methods of the project. It should specify the type of data and analysis and state the expected outcomes (i.e. answer the question 'how?'). The project description should be reader-friendly to non-specialists and contain as little jargon as possible.",
          "Two reference letters in signed sealed envelopes",
          "All official undergraduate and graduate transcripts",
          "Application packages must be submitted to your Department Graduate Coordinator and must include:",
          "Students are responsible for retrieving their official transcripts from other institutions."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your\u00a0your Department Graduate Coordinator for further information regarding this award.",
      "vid":9839,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/canadian-water-resources-association-cwra-scholarship-water"
    },
    {
      "id":1001,
      "title":"Canada Graduate Scholarships \u2013 Michael Smith Foreign Study Supplements (CGS-MSFSS) Program",
      "status":"Active",
      "value":"$6000: The value of the CGS-MSFSS award is up to $6,000, based on the information and budget justification provided in the application.",
      "type":[
        "Scholarships",
        "International experience awards"
      ],
      "description":"The CGS-MSFSS Program supports high calibre Canadian graduate students in building global linkages and international networks through the pursuit of exceptional research experiences at research institutions abroad. By accessing international scientific research and training, CGS-MSFSS recipients will contribute to strengthening the potential for collaboration between Canadian universities and affiliated research institutions and universities, or other research institutions outside of Canada.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be Canadian citizens or permanent residents of Canada by the application deadline dates (June 10th and October 10th);",
          "Be registered at an eligible Canadian institution at the time of application;",
          "Have accepted or currently hold a CGS Master\u2019s or Doctoral, or an eligible Vanier CGS award administered by one of the granting agencies\u00a0",
          "Ensure that their scholarship will still be active at the time the research study period abroad begins;",
          "Undertake the proposed trip abroad no earlier than the competition deadline date; and",
          "Not currently hold, or have not held, any other CGS-MSFSS during the course of their graduate studies.",
          "To be eligible to apply for this program, applicants must:",
          "To remain eligible, a successful applicant must:\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Application details can be found on the Graduate Studies Awards &amp; Financial Aid Website."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Coordinator, Graduate Scholarships for further information regarding this award.",
      "vid":9840,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/canada-graduate-scholarships-michael-smith-foreign-study"
    },
    {
      "id":1002,
      "title":"CAGS\/UMI Distinguished Dissertation Awards",
      "status":"Active",
      "value":"$1500: They include a $1,500 prize, a Citation Certificate, and travel expenses of up to $1,500 to attend the 2015 CAGS Annual Conference.",
      "type":[
        "Scholarships"
      ],
      "description":"The CAGS\/UMI Distinguished Dissertation Awards recognize Canadian doctoral dissertations that make unusually significant and original contributions to their academic field. They were established in 1994 and are presented annually. There are two awards: one for engineering, medical sciences and natural sciences; and one for fine arts, humanities\n\tand social sciences. The Awards are granted by the Canadian Association for Graduate Studies (CAGS) and are sponsored by Proquest-UMI (University Microfilms International).",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "A dissertation in any discipline in engineering, medical sciences and natural sciences completed and accepted by the Graduate School between January 1st and December 31st.",
          "A dissertation in any discipline in the fine arts, humanities and social sciences completed and accepted by the Graduate School between January 1st and December 31.",
          "Eligible Dissertations:",
          "In interdisciplinary domains or in fields that overlap the two broad areas in which the prizes are given, the dean of graduate studies must decide for which prize it is appropriate to submit the dissertation."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Nomination packages will be solicited from each appropriate Faculty and 1 nominee in each of 2 fields of study will be forwarded to CAGS for consideration."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.cags.ca\/cagsumi.php"
      ],
      "contact":"Please visit the CAGS website for further information.",
      "vid":9841,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/cagsumi-distinguished-dissertation-awards"
    },
    {
      "id":1003,
      "title":"Borys and Rose Boritz Accounting Graduate Scholarship",
      "status":"Active",
      "value":"$2500",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $2,500 is provided annually to a full-time graduate student enrolled in the Master of Accounting program at the School of Accounting and Finance in the Faculty of Arts on the basis of academic achievement (based on an excellent academic record at the undergraduate level). Preference will be given to applicants with a minor in International Studies. Interested students must submit an application each year.\u00a0 Applicants should contact the School of Accounting and Finance for more details. This scholarship was established in honour of Borys and Rose Boritz and is made possible by a donation from Efrim Boritz.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Letter explaining how you meet the award criteria",
          "Resume required"
        ],
        "additional":[
          "In addition to your application, provide a copy of a recent grade report."
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
        
      ],
      "contact":"Contact the School of Accounting and Finance Graduate Coordinator for further information regarding this award.",
      "vid":10861,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/borys-and-rose-boritz-accounting-graduate-scholarship"
    },
    {
      "id":1004,
      "title":"W.K. Thomas Graduate Scholarship",
      "status":"Active",
      "value":"$5000: Will normally be paid as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"One scholarship valued at $5,000 will be awarded annually to a full-time University of Waterloo graduate student in the Faculty of Arts, Department of English who holds an OGS unless there are no appropriate candidates.\u00a0 The scholarship will be awarded in subsequent years.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the English Department Graduate Coordinator for further information regarding this award.",
      "vid":9843,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/wk-thomas-graduate-scholarship"
    },
    {
      "id":1006,
      "title":"UW Alumni @ Stantec Graduate Scholarship",
      "status":"Active",
      "value":"$5000: May be paid as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"One scholarship valued at $5,000 will be awarded annually to a full-time Canadian or Permanent Resident graduate student in the Departments of Chemical, Civil, Mechanical, or E&amp;CE. The university will make every effort to match these awards through government programs. For instance, when matched with OGS the total value of each scholarship will be $15,000 annually.\u00a0 If this is not feasible, the scholarships will then be valued and awarded at $5,000 each. The scholarship selection will be made by the Associate Dean, Graduate Studies in the Faculty of Engineering.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9845,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-alumni-stantec-graduate-scholarship"
    },
    {
      "id":1007,
      "title":"Curwin Friesen\/Tim Jackson MBET Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $5,000 is awarded annually to full-time graduate students enrolled in the MBET program in the Faculty of Engineering on the basis of academic excellence (minimum 80%).\u00a0 This fund is made possible by donations from Curwin Friesen and Tim Jackson.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the CBET Graduate Coordinator Graduate Coordinator for further information regarding this award.",
      "vid":9846,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/curwin-friesentim-jackson-mbet-scholarship"
    },
    {
      "id":1008,
      "title":"Three Minute Thesis (3MT) Competition",
      "status":"Active",
      "value":"$1000: One award of $1,000 and another of $500.",
      "type":[
        "Scholarships"
      ],
      "description":"The Three Minute Thesis (3MT) Competition is an annual university-wide competition for research-based master's and doctoral students at the University of Waterloo. Competitors have one static slide and three minutes to explain the breadth and significance of their research to a non-specialist audience. Winners of the First Place and Runner Up Awards will be selected by a panel of judges at the university-wide 3MT final competition. The first Place winner will receive an award of $1,000 and the Runner Up will receive an award of $500.\n\nThe Award is funded by the Graduate Student Endowment Fund.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Participation in the 3MT is required to be eligible to receive one of the awards. Selection is made by a judging panel at the institutional 3MT finals each year."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Coordinator, Graduate &amp; Postdoctoral Events &amp; Communications for further information on these awards.",
      "vid":9847,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/three-minute-thesis-3mt-competition"
    },
    {
      "id":997,
      "title":"International Master&#039;s and Doctoral Student Awards (IMSA \/ IDSA)",
      "status":"Active",
      "value":"IMSA - the value is approximate to one-half of the differential fee per term\n\nIDSA - the value is approximate to the full differential fee per term\n\nIDSA4 - the value is approximate to the full differential fee per term",
      "type":[
        "Scholarships"
      ],
      "description":"Eligible students must be enrolled full-time in research-based graduate degree programs at the University of Waterloo and hold a valid Canadian study permit.\u00a0 Students must meet the academic progress requirements of their program, and not have outstanding probationary admission requirements, or be concurrently receiving external awards or sponsorships.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "International graduate students registered full-time in a MA, MASC, MES, MFA, MMATH (except coursework) or MSC degree program will receive an IMSA for 2 years (up to term 6.0).",
          "International graduate students registered full-time in a research-based PhD program will receive an IDSA for 3 years (up to term 9.0).",
          "International graduate students registered full-time in a research-based PhD program and who were admitted from a master's degree will receive an International Doctoral Student Award Year 4 (IDSA4) for year 4 (terms 10 to 12).",
          "\u00a0",
          "For information on payment of the IMSA\/IDSA, please visit the Graduate Studies International Funding webpage."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/awards-funding\/international-funding",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9836,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/international-masters-and-doctoral-student-awards-imsa-idsa"
    },
    {
      "id":996,
      "title":"K-W Third Age Learning Bursary",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"The Kitchener-Waterloo Third Age Learning Bursary will be awarded annually. The bursary will be awarded to students engaged in gerontology studies, who have financial need.\n\tInterested students are to apply to the Graduate Studies Office. The final selection will be made by the Department of Health Studies &amp; Gerontology.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Health Studies &amp; Gerontology Department Scholarship Coordinator for further information regarding this award.",
      "vid":10241,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/k-w-third-age-learning-bursary"
    },
    {
      "id":995,
      "title":"James and Nora Nelson Bursary in Environmental Planning",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"This bursary is in memory of James and Nora Nelson and is awarded to a graduate student with a proven financial need whose program of study or research is in Environmental Planning including land use, ecological, institutional, or other approaches to planning for the environment. The Associate Dean, Graduate Studies of Environmental Studies can be consulted for further information. Eligible students must have resided in Ontario for twelve months prior to beginning their post - secondary education.\n\tApplications for the bursary must be submitted with a proposal outlining a program of study or research in Environmental Planning including land use, ecological, institutional or other approaches to planning for the environment.\n\tApplicants are to apply using the Graduate Student Award Application form. Applications are to be submitted to the Graduate Studies Office, 2nd floor Needles Hall. The final selection will be made by the Faculty of Environmental Studies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "June 1"
        ],
        "application":[
          "June 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"For further information contact the School of Planning Graduate Coordinator.",
      "vid":10239,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/james-and-nora-nelson-bursary-environmental-planning"
    },
    {
      "id":985,
      "title":"J. William and Sarah Dyck Scholarship for Russian Mennonite Studies",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship, valued at $1,000, is provided annually to undergraduate or graduate students enrolled in studies at Conrad Grebel University College. The successful candidate will demonstrate an ongoing, active academic interest in and have produced a substantive research paper contributing to the understanding of the Mennonite experience. Preference will go to students who paper focuses on the Russian Mennonite experience. This fund is made possible by a donation from J. William and Sarah Dyck.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Theological Studies",
        "Theology",
        "Peace &amp; Conflict Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Demonstrated an ongoing, active academic interest in Mennonite Studies with a preference for Russian Mennonite studies; and",
          "Produced a substantive paper contributing to the understanding of the Mennonite experience with a preference to the Russian Mennonite experience. The subject of papers may be chosen from a variety of disciplines, e.g., Religion, Music, Education, History, Literature, Peace and Conflict Studies, etc.",
          "Recipients of the award(s) will be chosen by the Academic Dean of Conrad Grebel University College upon recommendation of professors at the College.",
          "Selection will be based on academic merit.",
          "Recipients of the award(s) will be graduate or undergraduate students who have:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9824,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/j-william-and-sarah-dyck-scholarship-russian-mennonite"
    },
    {
      "id":986,
      "title":"Senior Women Academic Administrators of Canada Graduate Student Awards of Merit(SWAAC)",
      "status":"Active",
      "value":"$5000: 2015 - Ontario = 5 awards at $5000 each.",
      "type":[
        "Scholarships"
      ],
      "description":"At least three awards, each in the amount of $2500, will be awarded annually to the women graduate students who have demonstrated outstanding leadership in the university or general community while maintaining exemplary academic records.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Ontario (2015) \u2013 5 awards",
          "Quebec [2016] - 4 awards",
          "Western Provinces (2017) - 4 awards",
          "Atlantic Provinces (2018) - 3 awards",
          "Ontario (2019) - ?",
          "Eligibility\n\tWomen registered in Master's or PhD programs at any\u00a0Member Institution of AUCC\u00a0within a designated region are eligible to be nominated. Regions and number of awards are defined as follows, and eligibility shall rotate among them:",
          "Criteria\n\t1. Outstanding academic performance.\n\t2. Evidence of leadership, including but not limited to such things as:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "For more details see the SWAAC website."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.aucc.ca\/about_us\/membership\/ourmemb_e.html",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Please contact the Coordinator, Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9825,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/senior-women-academic-administrators-canada-graduate-student"
    },
    {
      "id":987,
      "title":"Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST)",
      "status":"Active",
      "value":"The scholarship value will be $5,000 per term to a maximum of $15,000 annually. Consistent with the 2:1 ratio of government funding to institutional funding for this program, the Ontario government portion of the award to an individual student will be to a maximum of $10,000 annually, or $3,333 per term. The remaining funds are to be provided by the institution. Awards must be for a minimum of two and a maximum of three sequential academic terms.",
      "type":[
        "Scholarships"
      ],
      "description":"The Ontario Graduate Scholarship (OGS) and the Queen Elizabeth II Graduate Scholarship in Science and Technology (QEII-GSST) programs encourage excellence in graduate studies at publicly-assisted universities in Ontario. Since 1975, the OGS program has been providing merit-based scholarships to Ontario\u2019s best graduate students in all disciplines of academic study. In 1998, the Ontario government introduced the QEII-GSST, a merit-based scholarship program targeted specifically toward graduate students in science and technology.\n\nBoth scholarships are jointly funded by the Ontario government and participating institutions. The government contributes two-thirds of the value of the awards and the university provides the remaining one-third.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Applied Mathematics",
        "Biology",
        "Health Studies\/Gerontology",
        "Arts",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "Chemical Engineering",
        "Computational Mathematics",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Environment",
        "Pharmacy",
        "Planning",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Physics",
        "Management Sciences",
        "Physics and Astronomy",
        "Pure Mathematics",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Vision Science",
        "Statistics &amp; Actuarial Science",
        "Systems Design Engineering",
        "Psychology"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "A Canadian citizen, Permanent Resident, or Protected Person [under subsection 95(2) of the Immigration and Refugee Protections Act (Canada)] at the time of the application deadline date.",
          "Enrolled at a publicly-assisted university in Ontario in a full-time program of study that leads to a graduate degree and is approved for operating grant purposes by the ministry.",
          "Enrolled in 60% or more of a full course load as defined by the university, or 40% or more for students with permanent disabilities.",
          "Enrolled in a research master's or doctoral program in a science and technology discipline.",
          "In order to be considered for an QEII-GSST, students must be:",
          "The applicant must, at minimum, meet the following OGS academic requirements:",
          "*Universities may require applicants to meet more rigorous academic requirements as they deem appropriate.",
          "Eligibility Conditions:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Beginning with the 2016\/2017 QEII-GSST awards, in order to be considered for a QEII-GSST you must have applied for an OGS for the same award year."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10902,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/queen-elizabeth-ii-graduate-scholarship-science-technology"
    },
    {
      "id":988,
      "title":"Ontario Trillium Scholarship (OTS)",
      "status":"Active",
      "value":"$40000: Each OTS is valued at $40,000 annually and is automatically renewable for an additional three years provided the recipient maintains good academic standing and continues to meet recipient eligibility requirements.",
      "type":[
        "Scholarships",
        "Entrance awards"
      ],
      "description":"In 2010, the Ontario government announced the introduction of the OTS program as a significant initiative to attract more of the best qualified international students to Ontario for PhD studies.\n\nThe OTS are to be awarded to international PhD recipients for a maximum of four years. These scholarships are to be automatically awarded to the student for each of the three years following the first year provided the student maintains good academic standing and continues to meet recipient eligibility requirements.\n\nEach Faculty will nominate one student and one alternate in the Winter term for Fall admission.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Recipients must be international students who hold a valid Canadian study permit and who do not qualify for an exemption to the higher international tuition and fees per the Fee Schedule; should an OTS recipient obtain permanent residency status after the beginning of the first term of study, s\/he will continue to be eligible for the OTS for the balance of his\/her renewable OTS for a total of four years;",
          "Recipients must be intending to pursue full-time graduate studies at the doctoral level in a degree granting program;",
          "Recipients must have achieved a first-class average in each of the two years of full-time study prior to being awarded the OTS;",
          "Recipients must not have completed a previous degree at an Ontario post secondary institution at the undergraduate or graduate level immediately prior to being admitted to the PhD program; recipients must not be currently studying at an Ontario post secondary institution at the undergraduate or graduate level (students currently registered in a PhD program are not eligible)",
          "Recipients must not have concurrently accepted a scholarship from NSERC (ie. IPS) or OGS and must not concurrently be receiving significant external sponsorships or scholarships (for example, in excess of $10,000)",
          "Recipients who withdraw, transfer to part-time status or fail to complete the term without prior consultation with the Graduate Studies Office may be required to repay the award."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/gradcalendar.uwaterloo.ca\/page\/GSO-Fee-Schedule-Tuition-Assessment-Information",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Coordinator, Financial Aid &amp; Awards in the Graduate Studies Office for more information.",
      "vid":9827,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ontario-trillium-scholarship-ots"
    },
    {
      "id":989,
      "title":"James Downey Grad Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship will be awarded annually to a full-time University of Waterloo graduate student who holds an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). This scholarship has been made possible by the generosity of Trina McQueen who is an honourary alumna of the University.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9828,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/james-downey-grad-scholarship"
    },
    {
      "id":990,
      "title":"Ontario Graduate Scholarships (OGS) Program",
      "status":"Active",
      "value":"The scholarship value will be $5,000 per term to a maximum of $15,000 annually. Consistent with the 2:1 ratio of government funding to institutional funding for this program, the Ontario government portion of the award to an individual student will be to a maximum of $10,000 annually, or $3,333 per term. The remaining funds are to be provided by the institution. Awards must be for a minimum of two sequential academic terms.",
      "type":[
        "Scholarships"
      ],
      "description":"Since 1975, the Ontario government, in partnership with Ontario\u201fs publicly-assisted universities, has encouraged excellence in graduate studies at the master\u201fs and doctoral levels through the awarding of Ontario Graduate Scholarships (OGS). OGS awards are merit-based scholarships available to students in all disciplines of academic study. The OGS program is jointly funded by the Province of Ontario and Ontario universities. The Province of Ontario contributes two-thirds of the value of the award and the university provides one-third.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "A Canadian citizen, Permanent Resident, or Protected Person [under subsection 95(2) of the Immigration and Refugee Protections Act (Canada)] at the time of the OGS application deadline date.",
          "Enrolled in an eligible post secondary institution in Ontario (one offering graduate programs).",
          "Taking an eligible program on a full time basis.",
          "In order to be considered for an OGS, students must be:",
          "The applicant must, at minimum, meet the following OGS academic requirements:",
          "Universities may require applicants to meet more rigorous academic requirements as they deem appropriate.",
          "Eligibility Conditions\n\tMaster\u201fs students can receive the scholarship for a maximum of two years and doctoral students for a maximum of four years, subject to a lifetime maximum of six years per student.",
          "In addition, lifetime maximums of six (6) years of government-funded student awards must have not have been exceeded by the applicant.",
          "For full details, please visit Waterloo's OGS website."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "The Waterloo application and further information on applying for OGS at Waterloo can be found on our OGS website.",
          "OGS awards are not portable to other institutions."
        ]
      },
      "deadlines":{
        "term":[
          "December 1"
        ],
        "application":[
          "December 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9829,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ontario-graduate-scholarships-ogs-program"
    },
    {
      "id":991,
      "title":"Jean and William Leach Memorial Scholarship",
      "status":"Active",
      "value":"$1250",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established in loving memory of Jean and William Leach by their daughter's family.\u00a0 The award will be presented to a graduate student currently registered full-time in the Health Studies MSc or PhD program.\u00a0 The selection will be made annually by the Graduate Studies Committee of the Department of Health Studies and Gerontology.\u00a0 The scholarship will be awarded on the basis of the student's first year standing as of May 31st.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Health Studies and Gerontology Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9830,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jean-and-william-leach-memorial-scholarship"
    },
    {
      "id":992,
      "title":"Jim &amp; Diane Ohi Memorial Award",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established in memory of Jim and Diane Ohi. Jim was a graduate student in Electrical and Computer Engineering; Diane was a graduate of the Systems Design Engineering program. Both were killed in an automobile accident on August 6, 1993. This award will be granted annually, if a suitable candidate exists, to a graduate student in the Department of Electrical and Computer Engineering who demonstrates the qualities of leadership and a high level of academic achievement. Nominations are to be forwarded to the office of the Associate Chair of Graduate Studies in the Electrical and Computer Engineering department.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Electrical &amp; Computer Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Electrical &amp; Computer Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9831,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/jim-diane-ohi-memorial-award"
    },
    {
      "id":993,
      "title":"J. Alan George Leadership Award",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Entrance awards"
      ],
      "description":"The J. Alan George Student Leadership Award is presented to an entering graduate student, chosen from among students within three terms of first receipt of a\u00a0 Provost Doctoral Entrance Award for Women and based on a record of student leadership. Selection will be made by the Advisory Committee on Graduate Scholarships and Awards. If the Provost Doctoral Entrance Award for Women ceases, the terms of this award will be redefined.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be in their first year of graduate studies at Waterloo",
          "Be registered full\u2010time",
          "Have received a Graduate Provost Doctoral Entrance Award for women",
          "Demonstrate outstanding leadership",
          "Applicants must:",
          "Selection will be made by the Advisory Committee on Graduate Scholarships and Awards."
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Coordinator, Financial Aid &amp; Awards for further information regarding this award. Each department will set their own deadline.",
      "vid":10314,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/j-alan-george-leadership-award"
    },
    {
      "id":994,
      "title":"John E. Thompson Biology Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $5,000 will be awarded annually to a full-time University of Waterloo graduate student registered in the Department of Biology in the Faculty of Science.\u00a0 The scholarship will be awarded on the basis of scholastic excellence to a graduate student who holds an Ontario Graduate Scholarship (OGS), Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) or another major external scholarship that requires a matching or enhancement component.\u00a0 If the match or enhancement becomes unavailable or a suitable recipient cannot be found, the funds will be paid out as a regular graduate scholarship.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Biology",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Biology Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9833,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/john-e-thompson-biology-graduate-scholarship"
    },
    {
      "id":984,
      "title":"Social Sciences &amp; Humanities Research Council Doctoral and Canada Graduate Scholarship Doctoral (SSHRC Doc\/CGSD)",
      "status":"Active",
      "value":"The agency determines the value and duration of the award during the national adjudication based on the number of months of full-time study.\u00a0 The CGS-D scholarship is valued at $35,000 per year for up to 36 months while the Doctoral Fellowship is valued at $20,000 annually for anywhere from 12 months to 48 months.\u00a0 Specific details can be found on the official SSHRC Doctoral website.",
      "type":[
        "Scholarships"
      ],
      "description":"The Joseph-Armand Bombardier CGS Doctoral Scholarships and the SSHRC Doctoral Fellowships programs seek to develop research skills and assist in the training of highly qualified personnel by supporting students in the social sciences and humanities who demonstrate a high standard of achievement in undergraduate and graduate studies in the social sciences and humanities.\u00a0 There are two types of SSHRC Doctoral awards available through a single application:\n\nJoseph-Armand Bombardier Canada Graduate Scholarships Doctoral (CGS-D) - for study in Canada\n\tSSHRC Doctoral Fellowship - for study in Canada or abroad",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Canadian citizens and permanent residents are eligible to be considered for the SSHRC Doctoral scholarship.\u00a0 As an interested applicant, it is your responsibility to confirm you satisfy the minimum eligibility criteria of this award before you begin the application process.\u00a0 To confirm you are eligible to apply, as well as how you will be evaluated, you must review the official eligibility criteria and evaluation criteria on the official SSHRC Doctoral Awards website."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Contact your Department Graduate Coordinator for the deadline to submit your application. Visit our SSHRC webpage for details on how to apply."
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
        "http:\/\/www.sshrc-crsh.gc.ca\/funding-financement\/programs-programmes\/fellowships\/doctoral-doctorat-eng.aspx#a4",
        "http:\/\/www.sshrc-crsh.gc.ca\/funding-financement\/programs-programmes\/fellowships\/doctoral-doctorat-eng.aspx#a6",
        "http:\/\/www.sshrc-crsh.gc.ca\/funding-financement\/programs-programmes\/fellowships\/doctoral-doctorat-eng.aspx",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Contact your Department Graduate Coordinator for further information.",
      "vid":10582,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/social-sciences-humanities-research-council-doctoral-and"
    },
    {
      "id":1033,
      "title":"Mike and Ophelia Lazaridis Fellowships",
      "status":"Active",
      "value":"$20000",
      "type":[
        "Scholarships"
      ],
      "description":"The Institute for Quantum Computing and the University of Waterloo are pleased to announce annual Mike and Ophelia Lazaridis Fellowships to be awarded to international graduate students based on their outstanding promise for excellence of research in Quantum Information Science. The fellowships will be awarded annually to students pursuing their studies with a member of the IQC in a program at UW. The awards include a yearly stipend of up to $20,000 per year, subject to adjustment annually for inflation, and renewable for a maximum period of four years provided the recipient maintains a satisfactory academic standing in his or her program; in addition, each recipient will receive a UW award to cover their tuition. The selection will be made by a committee organized by the Director, Institute for Quantum Computing.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Engineering",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Physics",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your IQC Department Graduate Coordinator for further information regarding this award.",
      "vid":9872,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/mike-and-ophelia-lazaridis-fellowships"
    },
    {
      "id":1023,
      "title":"Pragma Council Graduate Student Award",
      "status":"Active",
      "value":"$250",
      "type":[
        "Scholarships"
      ],
      "description":"The Pragma Council Student Award, valued at $250, is awarded to a graduate student who has made a significant contribution to the general well-being of the School of Planning and that of their fellow students, while maintaining a strong academic record. One award is presented at the Spring and Fall Pragma Council Conferences.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment",
        "Planning"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact Teh School of Planning Graduate Coordinator for further information regarding this award.",
      "vid":9862,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/pragma-council-graduate-student-award"
    },
    {
      "id":1024,
      "title":"Plumtree Graduate Scholarship in Mechanical &amp; Mechatronics Engineering",
      "status":"Active",
      "value":"$5000: This Scholarship will be paid as institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships",
        "Research specific awards"
      ],
      "description":"The scholarship will be awarded annually to a full-time University of Waterloo graduate student in the Faculty of Engineering who holds an OGS.\u00a0 Preference will be given to a graduate student whose area of research is engineering materials.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Mechanical &amp; Mechatronics Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9863,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/plumtree-graduate-scholarship-mechanical-mechatronics"
    },
    {
      "id":1025,
      "title":"Phyllis Young Forsyth Graduate Scholarship in Classical Studies",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships"
      ],
      "description":"One scholarship, valued at $1500, will be awarded annually to a full-time University of Waterloo graduate student in the Faculty of Arts, Classical Studies.\u00a0 The scholarship will be given to one graduate student who has the highest academic standing upon entry into the graduate program in Classical Studies.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Classical Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Classical Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":9864,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/phyllis-young-forsyth-graduate-scholarship-classical-studies"
    },
    {
      "id":1026,
      "title":"Penelope Glasser Mature Science Graduate Student Scholarship",
      "status":"Active",
      "value":"$5000: This award will normally be paid as the institutional matching funds for the OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"Scholarship(s) valued at $5,000 will be awarded annually to a full-time University of Waterloo mature graduate student in the Faculty of Science on the basis of scholastic excellence and financial need.\n\nThe value of the annual award is determined by the endowment interest each year.\u00a0 The goal is to provide scholarship(s) with a value of $5,000.\u00a0 The value and\/or number of scholarships may change as funds permit.\u00a0 The university will make every effort to match this award with government programs.\u00a0 For instance, when matched 2:1 by the OGS, the total value of the scholarship is $15K.\u00a0 It could also be used as a top-up for the NSERC scholarships.\u00a0 If this is not feasible, the scholarships will be valued and awarded at $5,000 each.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Earth &amp; Environmental Sciences",
        "Pharmacy",
        "Physics",
        "Physics and Astronomy",
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Science Department Graduate Coordinator for further information regarding this award.",
      "vid":9865,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/penelope-glasser-mature-science-graduate-student-scholarship"
    },
    {
      "id":1027,
      "title":"Ontario Graduate Scholarship - UWaterloo",
      "status":"Active",
      "value":"$5000: The Scholarship will be paid as the institutional matching portion of an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship valued at $5,000 will be awarded annually to a full-time University of Waterloo graduate student registered in a Master\u2019s or Doctoral program.\u00a0 The scholarship will be awarded to a graduate student on the basis of academic excellence and who holds an Ontario Graduate Scholarship (OGS) or Queen Elizabeth II Graduate Scholarship in Science and Technology (QEII-GSST).\u00a0 The scholarship will be used to match up to three terms of the student\u2019s OGS or QEII-GSST for a total value of $15,000 over three consecutive academic terms.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9866,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ontario-graduate-scholarship-uwaterloo"
    },
    {
      "id":1028,
      "title":"Keith &amp; Debbie Geddes Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"Dr. Geddes and his wife Debbie established this research scholarship for a graduate student in the Faculty of Mathematics, with priority given to students with a concentration in Computational Math.\u00a0 In the event that a suitable candidate is not found in Computational Math, the scholarship will be awarded to a student in the School of Computer Science.\n\nSelection of the recipient will be made by the Associate Dean of Graduate Studies in the Faculty of Mathematics, on the recommendation of the Computational Math Steering Committee.\n\nRecipients must be Canadian or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Computational Mathematics",
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Recipients will normally hold an Ontario Graduate Scholarship (OGS) or a\u00a0 Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST) within the Faculty of Mathematics."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Computer Science Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":9867,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/keith-debbie-geddes-graduate-scholarship"
    },
    {
      "id":1029,
      "title":"Norman Esch Graduate Scholarship",
      "status":"Active",
      "value":"$10000",
      "type":[
        "Scholarships"
      ],
      "description":"Two scholarships valued at $10,000 each will be awarded annually to full time graduate students on the basis of academic excellence (minimum overall average of 80%), and students possessing a strong entrepreneurial outlook with business concepts that have the potential to become viable businesses.\u00a0 Preference will be given to students with financial need.\u00a0 Interested students should apply with a mini-business plan submitted to the Graduate Coordinator by April 30 or June 30.\n\nThis fund is made possible by a donation from The Esch Foundation's Norman Esch Entrepreneurial Challenge in Engineering Fund.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Interested students should submit a mini-business plan to the Graduate Coordinator by April 30 or June 30."
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
        "https:\/\/uwaterloo.ca\/graduate-studies\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your CBET Graduate Coordinator for further information regarding this award.",
      "vid":9868,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/norman-esch-graduate-scholarship"
    },
    {
      "id":1031,
      "title":"Nanotechnology Fellowships",
      "status":"Active",
      "value":"$10000",
      "type":[
        "Scholarships"
      ],
      "description":"A major endowment has been established to annually award 42 graduate Fellowships in Nanotechnology.\u00a0 Fellowships can be held simultaneously with other graduate awards.\u00a0 These prestigious fellowships are open to both graduate students currently pursuing nano-research at Waterloo and to new students applying for admission.\u00a0 Applicants must satisfy the general eligiblity requirement for the University of Waterloo Graduate Scholarships.\u00a0 Special consideration will be given to students intending to pursue projects involving cross-disciplinary collaboration in nanotechnology.\u00a0 Selection of recipients for the fellowships will be made by a committee chair by the Executive Director of the Waterloo Institute for Nanotechnology.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemical Engineering",
        "Engineering",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Minimum 80% academic average",
          "Registered full-time in a nanotechnology gradate program"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Visit the Waterloo Institute for Nanotechnology website for details on applying."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9870,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/nanotechnology-fellowships"
    },
    {
      "id":1032,
      "title":"NA Engineering Associates Inc. Research Travel Award in Hellenistic Studies",
      "status":"Active",
      "value":"$1500: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"An award, valued at up to $1500 is awarded annually to full-time graduate students who are Canadian citizens\/permanent residents and a resident of Ontario.\u00a0 Students must be enrolled in the graduate program in the Department of Classical Studies in the Faculty of Arts who can demonstrate a need for travel to Greece in order to enhance their research, and who have demonstrated financial need. The award will be based on a demonstrated research interest in the study of Greece and Classical Greek heritage and relevant to the Waterloo Institute for Hellenistic Studies.\u00a0\n\nThis fund is made possible by a donation from NA Engineering Associates Inc. in support of the Waterloo Institute for Hellenistic Studies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Arts",
        "Classical Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be a full-time undergraduate or graduate student who is enrolled in a program in the Department of Classical Studies in the Faculty of Arts.",
          "Show demonstrated research interest in the study of Greece and Classical Greek heritage.",
          "Be a Canadian Citizen or Permanent Resident.",
          "Must have resided in Ontario for 12 months prior to beginning their post - secondary education.",
          "Be able to demonstrate financial need.",
          "Applicants must:"
        ],
        "instructions":[
          "Graduate Award Application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 15"
        ],
        "application":[
          "February 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact your Classical Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":10247,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/na-engineering-associates-inc-research-travel-award"
    },
    {
      "id":1022,
      "title":"Professor Thammaiah Viswanatha Memorial Graduate Award in Biochemistry",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"An award, valued at up to $1,000 is awarded annually to a full-time graduate student currently registered in the Guelph-Waterloo Centre for Graduate Work in Chemistry (GWC)2, which a research focus in the field of biochemistry.\u00a0 The awardee shall be selected on the basis of a demonstration of ability and promise in research and his\/her performance in at least two graduate courses, with particular emphasis being placed on the former.\u00a0 The selection committee will be made up of the Coordinating Committee of (GWC)2, or a subcommittee thereof appointed by the Director.\u00a0 Nominations will be solicited from Centre faculty and the Graduate Officers in the Fall term each year.\u00a0 This fund is made possible by donations from family and friends for Professor Thammaiah Viswanatha (TV) in honour of his lifelong dedication to teaching and research.\u00a0 TV served as a biochemistry professor from 1964 until his retirement in 1995.\u00a0 As Distinguished Professor Emeritus, he remained very active in research until his death at the age of 82.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Biology or Chemistry Department Graduate Coordinator for further information regarding this award.",
      "vid":9861,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/professor-thammaiah-viswanatha-memorial-graduate-award"
    },
    {
      "id":1021,
      "title":"R.G. Goel Memorial Graduate Scholarship",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship, administered by the Guelph-Waterloo Centre for Graduate Work in Chemistry and Biochemistry (GWC)2, is in memory of the late Prof. R.G. Goel and was established by friends and colleagues and the Hindu Cultural Society. Eligible students must be registered in the (GWC)2 program and pursuing research in the field of inorganic or organometallic chemistry. Candidates will be considered on the basis of their academic record and potential in research. Nominations, including a letter of recommendation from the applicant\u2019s supervisor, will be provided to the selection committee by June 1st each year. No application is necessary.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact teh Biology or Chemistry Department Graduate Coordinator for further information regarding this award.",
      "vid":9860,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rg-goel-memorial-graduate-scholarship"
    },
    {
      "id":1020,
      "title":"Rai Mathematics Graduate Scholarship",
      "status":"Active",
      "value":"$5000: This scholarship will be paid as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established by Mr. Satish Rai, a graduate of the Faculty of Mathematics.\n\nTwo scholarships valued at $5,000 will be awarded annually to students pursuing graduate studies in the Faculty of Mathematics at the University of Waterloo.\u00a0 Students must be Canadian citizens or permanent residents.\u00a0 The awards will be gvien based on academic excellence, with preference given to students who hold an Ontario Graduate Scholarship (OGS) or Queen Elizabeth II Graduate Scholarship in Science and Technology (QEII-GSST).",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Mathematics Department Graduate Coordinator for further information regarding this award.",
      "vid":9859,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rai-mathematics-graduate-scholarship"
    },
    {
      "id":1010,
      "title":"Susan and Janos Aczel Graduate Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"An award, valued at up to $2,000 is awarded annually to full-time graduate students enrolled in the Faculty of Mathematics who are in good academic standing.\u00a0 Preference will be given to students specializing in mathematical analysis.\u00a0 This fund is made possible by donations from family and friends of Susan and Janos Aczel in loving memory of Susan, and in honour of Waterloo distinguished professor emeritus Janos Azcel (Pure Math) who was employed at the University of Waterloo between 1965 and 1993.\u00a0 This scholarship is an expression of the gratitude Susan and Janos Aczel felt for the scholarship support they received as a young married student couple.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Mathematics Department Graduate Coordinator for further information regarding this award.",
      "vid":9849,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/susan-and-janos-aczel-graduate-scholarship"
    },
    {
      "id":1011,
      "title":"Suncor Fellowships in Social Innovation",
      "status":"Active",
      "value":"$21000: Two awards valued at $21,000 plus additional support for up to $4,000 per student may also be available for research travel or attending conference.",
      "type":[
        "Scholarships"
      ],
      "description":"An Award valued at $21,000 each will be made available to two doctoral students registered full-time in any discipline at the University of Waterloo. The award is to provide funding to assist the students in conducting research related to social innovation in order to increase knowledge about the dynamics of complex social and environmental systems. This fund is made possible by a donation from Suncor Energy Inc.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Students will come from any discipline and in any year of a PhD program.\u00a0",
          "Students must have some degree of knowledge in:",
          "The following criteria will be considered when reviewing potential applicants:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9850,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/suncor-fellowships-social-innovation"
    },
    {
      "id":1012,
      "title":"Steven Fritz Memorial Scholarship",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships"
      ],
      "description":"Dr. Eric Reardon has donated funds and is organizing a campaign to solicit additional funds from donors in memory of Steven Fritz, post-doctoral fellow in the Department of Earth Sciences during the 1970's and more recently professor at Purdue University.\u00a0 This scholarship, valued at $500, will be awarded annually to a full-time graduate student in the Department of Earth and Environmental Sciences.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Earth &amp; Environmental Sciences",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Earth &amp; Environmental Sciences Department Graduate Coordinator for further information regarding this award.",
      "vid":9851,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/steven-fritz-memorial-scholarship"
    },
    {
      "id":1013,
      "title":"Stantec Graduate Scholarship in Civil Engineering",
      "status":"Active",
      "value":"$4000: May be paid out as the institutional matching funds for an OSG or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship, valued at $4,000, is presented annually for 5 years to an outstanding student entering the first year of a postgraduate program in the Department of Civil Engineering.\u00a0 This award was established by Stantec in recognition of the on-going contribution of Stantec to engineering in Canada, and Stantec\u2019s commitment to graduate education.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Civil &amp; Environmental Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9852,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/stantec-graduate-scholarship-civil-engineering"
    },
    {
      "id":1014,
      "title":"SNC-Lavalin Grad Schlp in Engineering",
      "status":"Active",
      "value":"$5000: Will normally be paid as the institutional matching funds for an OGS aor QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"Four scholarships valued at $5000 each will be awarded to full-time University of Waterloo graduate students in the Department of Civil Eng, conducting research in the following areas of specialization:\u00a0 Geotechnical Engineering; Structures, Mechanics, and Construction Engineering; Transportation Engineering; or Water Resources and Environmental Engineering.\u00a0 The awards are to be used to match OGS whenever possible.\u00a0 If this is not feasible, the scholarships will then be valued and awarded at $5000 each.\u00a0 The scholarship selection will be made by the Associate Dean, Graduate Studies and International Agreements in the Faculty of Engineering.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Civil &amp; Environmental Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9853,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/snc-lavalin-grad-schlp-engineering"
    },
    {
      "id":1015,
      "title":"Rotary Peace Scholarship",
      "status":"Active",
      "value":"$10000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship will be awarded to a full-time graduate student entering the 1st year of the Masters of Global Governance program in the Faculty of Arts at the University of Waterloo on the basis of academic excellence. The recipient must be conducting research that focuses broadly on questions of peace and they must have a demonstrated record of service to the cause of peace. Applicants will be selected by the Program Directorship following consultation with the admissions committee. This fund is made possible by the donation from the KW Cluster of Rotary Clubs.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Global Governance"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Global Governance Department Graduate Coordinator for further information regarding this award.",
      "vid":9854,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rotary-peace-scholarship"
    },
    {
      "id":1016,
      "title":"Ross and Doris Dixon MBET Scholarship",
      "status":"Active",
      "value":"$6000",
      "type":[
        "Scholarships"
      ],
      "description":"Founded by Ross and Doris Dixon, one scholarship will be presented to an outstanding student entering the Master of Business, Entrepreneurship and Technology program. Selection will be made by the MBET Admissions Committee, based on previous academic accomplishments and the ability to demonstrate, during an interview process, the entre(intra)-preneurial attributes required to successfully complete the program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the CBET Department Graduate Coordinator for further information regarding this award.",
      "vid":9855,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ross-and-doris-dixon-mbet-scholarship"
    },
    {
      "id":1017,
      "title":"Ross and Doris Dixon Charitable Foundation Graduate Scholarships in Applied Health Sciences",
      "status":"Active",
      "value":"$5000: This Scholarship will normally be paid as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"Ross and Doris Dixon, long-time friends and supporters of the University of Waterloo, have established this annual research scholarship for students in the graduate program in Applied Health Sciences.\u00a0 Preference will be given who hold hold an Ontario Graduate Scholarship (OGS) or a Queen Elizabeth II Graduate Scholarship in Science &amp; Technology (QEII-GSST). This award will be paid as the institutional matching funds for the OGS or QEII-GSST.\n\nThe final selection will be made by the Applied Health Sciences Associate Dean, Graduate Studies and Research. This scholarship is open to Canadian citizens and permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology",
        "Kinesiology",
        "Public Health",
        "Recreation &amp; Leisure Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Applied Health Sciences Department Graduate Coordinator for further information regarding this award.",
      "vid":9856,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ross-and-doris-dixon-charitable-foundation-graduate"
    },
    {
      "id":1018,
      "title":"Robbert Hartog Graduate Scholarship",
      "status":"Active",
      "value":"$5000: This scholarship will be paid as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established by Robbert Hartog who founded and was chair and CEO of Waltec Incorporated.\u00a0 He has actively promoted the growth and development of Canadian industry through his involvement with the Industrial Research and Development Institute (IRDI).\u00a0 IRDI is a non-profit corporation which serves as the national centre for research and development in material shaping industries, founded in 1992; currently members include leading companies involved in aerospace, automotive, fabrication, forming, packaging, rubber and plastic parts.\n\tTwo or more scholarships valued at $5000 will be awarded annually to full-time University of Waterloo graduate students in the Faculty of Engineering to students conducting research in materials or material shaping in the Department of Mechanical Engineering, who hold an\u00a0Ontario Graduate Scholarships (OGS).",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Mechanical &amp; Mechatronics Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9857,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/robbert-hartog-graduate-scholarship"
    },
    {
      "id":1019,
      "title":"Reinhold M. Schuster Graduate Scholarship",
      "status":"Active",
      "value":"$5000: This award may be paid as a scholarship or as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"Scholarship(s) valued at $5,000 will be awarded annually to a full-time University of Waterloo graduate student in the Department of Civil and Environmental Engineering who enter the Structures, Mechanics and Construction research area with preference for those doing cold-formed steel research.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact Civil &amp; Environmental Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9858,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/reinhold-m-schuster-graduate-scholarship"
    },
    {
      "id":951,
      "title":"Conrad Grebel University College - Theological Studies Award",
      "status":"Active",
      "value":"$10000: Up to $10,000 per term.",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established to serve as a general all-compassing award for various awards set up by Conrad Grebel University College.\u00a0 Subject to change, currently, these include awards such as:\n\nFull-time Tuition Award\n\tMagdalena Coffman Scholarship\n\tClifford Snyder Memorial Bursary\n\tJacob H. Janzen Memorial Bursary\n\tWomen of Mennonite Church Eastern Canada Theological Studies Award\n\tGraduate Student Support Fund\n\tA. James Reimer Award at the Toronto Mennonite Theological Centre\n\tStephen Family Theological Studies Entrance Award\n\tThe Reimer Scholarship in Theological Studies",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Catholic Thought",
        "Arts",
        "Theological Studies",
        "Theology",
        "Religious Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/theological-studies\/about\/people\/bmoscinski"
      ],
      "contact":"Information about the specific criteria for each of the awards can be obtained from the Master of Theological Studies (MTS) Administrative Assistant.",
      "vid":9790,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/conrad-grebel-university-college-theological-studies-award"
    },
    {
      "id":950,
      "title":"Conrad Grebel University College \u2013 MPACS Award",
      "status":"Active",
      "value":"$10000: Up to $10,000 per term.",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established to serve as a general all-compassing award for various awards set up by Conrad Grebel University College.\u00a0 Subject to change, currently, these include awards such as:\n\nWilliam Dick Peace &amp; Conflict Studies Field Study Award\n\tBecky Frey Student Scholarship\n\tGlobal Conflict Management and Transformation Award\n\tMary and Walter Hougham PACS Award\n\tThe Vick and Rita Krueger Family PACS Award\n\tMennonite Central Committee Peace Award\/PACS Internships\n\tElliot C. McLoughry Fund Scholarship\n\tPeter C. and Elisabeth Williams Memorial Fund Scholarship\n\tLina Wohlgemut Award",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Peace &amp; Conflict Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Be enrolled in the Master of Peace &amp; Conflict Studies (MPACS) program at the University of Waterloo - Conrad Grebel University College.",
          "Applicants must:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/master-peace-conflict-studies\/about\/people"
      ],
      "contact":"Information about the specific criteria for each of the awards can be obtained from the Peace and Conflict Studies Coordinator.",
      "vid":9789,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/conrad-grebel-university-college-mpacs-award"
    },
    {
      "id":948,
      "title":"Dan Watt Scholarship",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships"
      ],
      "description":"Daniel G. Watt who was a member of the University of Waterloo's Laurel Society, bequeathed funds to the University of Waterloo. The Laurel Society recognizes individuals who make planned gifts to the University. Interest from the endowment will fund the Dan Watt Scholarships. The scholarships will be awarded annually to students with the highest averages entering the University of Waterloo, Department of History graduate program.\n\nThe Department Graduate Studies Committee will make the selection. The number of scholarships will depend on the interest earned on the endowment.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "History"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the History Department Graduate Coordinator for further information regarding this award.",
      "vid":9787,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dan-watt-scholarship"
    },
    {
      "id":947,
      "title":"Daytech Manufacturing Ltd. Prize",
      "status":"Active",
      "value":"Award amount varies.",
      "type":[
        "Scholarships"
      ],
      "description":"Prize for students enrolled in post-graduate studies in Vision Science at the School of Optometry.\u00a0 It will be awarded to the student(s) presenting the best seminar as part of the Graduate Seminar Milestone as judged by 5 Optometry faculty members using a predetermined criterion.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the\u00a0 School of Optometry Graduate Coordinator for further information regarding this award.",
      "vid":9786,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/daytech-manufacturing-ltd-prize"
    },
    {
      "id":952,
      "title":"Conrad Family MBET Scholarships",
      "status":"Active",
      "value":"$20000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $20,000 is awarded to up to 15 full-time graduate students enrolled in the Master of Business, Entrepreneurship and Technology (MBET) program in The Conrad Business, Entrepreneurship and Technology Centre in the Faculty of Engineering.\u00a0 Applicants must be Canadian citizens or permanent residents and will be selected on the basis of the applicant\u2019s entrepreneurial orientation, quality of their business plan, and record of academic achievement. The scholarships will be part of CBET\u2019s celebrations of the 10th cohort of MBET students.\u00a0 Interested students should contact MBET for deadlines. This fund is made possible by a donation from the Conrad family.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Recipients will be selected on the basis of the applicant\u2019s entrepreneurial orientation, quality of their business plan, and record of academic achievement."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Once you are offered admission into the MBET program, you will be invited to apply for the Conrad Family Scholarships by submitting a mini-business plan.",
          "Scholarship recipients will be selected by a panel of faculty members based on entrepreneurial passion, quality of the business plan and record of academic achievement."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9791,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/conrad-family-mbet-scholarships"
    },
    {
      "id":953,
      "title":"Confucius China Study Plan",
      "status":"Active",
      "value":"$0: Varies. May include: in China research fund, tuition, lodging and living stipend, library stipend, in-China health and accident insurance, as well as expenditures for attending academic conference in related areas (one time per year), round-trip international transportation, and other living and work condition support provided by the Chinese and\/or oversea universities hosting the program.",
      "type":[
        "Scholarships"
      ],
      "description":"In order to foster deep understanding of China and the Chinese culture among young elites from around the world, enable the prosperous growth of China studies, promote the sustainable development of Confucius Institutes, and enhance the friendly relationship between China and the people of other countries, the Confucius Institute Headquarters (the Headquarters) has set up the \u201cConfucius China Study Plan\u201d.\n\nThe plan consists of six subprograms:\n\nSino-foreign Joint PhD\n\tPhD in China\n\t\"Understanding China\" Visiting Scholar\n\tYoung Leaders\n\tInternational Conference\n\tPublishing",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Non-Chinese nationality",
          "In good health condition",
          "Have necessary Chinese communication competence. Candidates of outstanding Chinese proficiency will be given priority over other competitors of similar qualifications.",
          "Students registered at Confucius Institute or applicants from universities that host a Confucius Institute will have priority in application and admission.",
          "Applicants who are currently participating in Chinese Government Scholarship are not eligible to apply for this Plan."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/renison\/people-profiles\/yan-li"
      ],
      "contact":"Please contact Yan Li at Renison University College for further information.",
      "vid":9792,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/confucius-china-study-plan"
    },
    {
      "id":954,
      "title":"Chemical Engineering Medal (Park Reilly Medal)",
      "status":"Active",
      "value":"Silver Medal - value varies",
      "type":[
        "Medals"
      ],
      "description":"This award was established by Dr. and Mrs. Park M. Reilly to recognize skill in research as measured by analysis of an engineering problem, planning an efficient solution of the problem and achieving the solution with superior insight into the science and\/or engineering involved. All doctoral graduates in the Department of Chemical Engineering are eligible.\n\nThe nomination of a student must originate with the PhD Examining Committee, which will submit the nomination to the Chemical Engineering Graduate Review Committee.\n\nSupporting documents including a recommendation from the supervisor(s) and in particular the external examiner should accompany the nomination. The Graduate Review Committee will consider all nominations and submit a single nomination to a regular monthly meeting of the Department for approval.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemical Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Contact the Chemical Engineering Department Graduate Coodinator for further information.",
      "vid":10073,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/chemical-engineering-medal-park-reilly-medal"
    },
    {
      "id":956,
      "title":"Carl Pollock Postgraduate Fellowship in Engineering",
      "status":"Active",
      "value":"$0: The value placed of this award will be the equivalent of the NSERC PGS D award, as of September 1st of the awarding year.",
      "type":[
        "Scholarships"
      ],
      "description":"The value placed on this award will be the equivalent of the NSERC PGS D award, as of September 1st of the awarding year.\u00a0 Application is made on the NSERC form 200.\n\tCompleted applications (Form 200, two references, an unofficial transcript and C.V.) are due in the Faculty of Engineering Graduate Studies Office (PHY 3003).\u00a0 See your department for deadlines.\n\tOpen to any graduate of the University of Waterloo Faculty of Engineering undergraduate program who is intending to pursue doctoral studies at the University of Waterloo.\u00a0 This fellowship will be awarded to a student undertaking doctoral research in one of the University of Waterloo Engineering Departments.\n\tOne fellowship is granted annually and is tenable only at the University of Waterloo.\u00a0 This fellowship is granted for a one-year period and must commence September 1st of the year awarded.\u00a0 The award is not automatically renewed. However, a recipient may re-apply and be considered for a further one-year period.\u00a0 This award cannot be held concurrently with another major scholarship, i.e. NSERC, OGS, etc.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Open to any graduate of the University of Waterloo Faculty of Engineering undergraduate program who is intending to pursue doctoral studies at the University of Waterloo.\u00a0",
          "This fellowship will be awarded to a student undertaking doctoral research in one of the University of Waterloo Engineering Departments."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.nserc-crsng.gc.ca\/OnlineServices-ServicesEnLigne\/pdf\/F200_e.pdf",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Enginering Department Graduate Coordinator for further information regarding this award.",
      "vid":9795,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/carl-pollock-postgraduate-fellowship-engineering"
    },
    {
      "id":957,
      "title":"Canadian Friends of the Hebrew University Travel Award",
      "status":"Active",
      "value":"$10000: Awards range from $1,000 - $15,000, depending on the length of the experience and the level of financial need.",
      "type":[
        "International experience awards"
      ],
      "description":"The Canadian Friends of the Hebrew University of Jerusalem has established a fund to assist University of Waterloo students who are approved to participate in a study abroad program at the Hebrew University of Jerusalem or the Rothberg International School and who have demonstrated financial need.\u00a0 Undergraduate and graduate students in all faculties and programs, who are in good academic standing, are invited to apply.\u00a0 Candidates must be Canadian citizens or permanent residents and have lived in Ontario for the entire 12-month period prior to beginning their post-secondary education.\u00a0 Awards range from $1,000 - $15,000, depending on the length of the experience and the level of financial need.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be approved to participate in a study abroad program at the Hebrew University of Jerusalem or the Rothberg International School",
          "Demonstrate financial need\u00a0\u00a0",
          "Be Canadian citizens or permanent residents",
          "Have lived in Ontario for the entire 12-month period prior to beginning their post-secondary education",
          "Applicants must:"
        ],
        "instructions":[
          "International Graduate Experience Award application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "application":[
          "March 15",
          "July 15",
          "November 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/overseas.huji.ac.il\/welcome-to-ris",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Coordinator, Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9796,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/canadian-friends-hebrew-university-travel-award"
    },
    {
      "id":946,
      "title":"Donald &amp; Geraldine Beam Award",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This award will be made annually to the student in the Master of Taxation program who best demonstrates aptitude and proficiency in the process, methodology, techniques and skills of original research in the TAX 638-Master's Research Paper.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the School of Accounting Graduate Coordinator for further information regarding this award.",
      "vid":9785,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/donald-geraldine-beam-award"
    },
    {
      "id":945,
      "title":"Dr. M. Chandrashekar Memorial Award in Sustainable Energy",
      "status":"Active",
      "value":"$5000: The award may be supplemented by an OGS or QEII-GSST, or any other appropriate award.",
      "type":[
        "Scholarships"
      ],
      "description":"This award was established in memory of the late M. Chandrashekar, a Professor in the Department of Systems Design Engineering for more than twenty-five years. It is expected that the awardee be a full-time graduate student at the University of Waterloo at the time of application. He\/she may not be beyond the third term in the Masters program or the ninth term in the PhD program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Each applicant should write a letter to the Dean of Engineering explaining how the applicant meets the criteria and how his or her research program relates to the purpose of the award. The application form and a curriculum vitae (CV) should accompany the letter. The CV should contain, aside from the typical items, information on scholarships received, publications, and extra-curricular activities while at the University of Waterloo.",
          "Selection will be made jointly by the Dean and Associate Dean, Graduate Studies."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9784,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-m-chandrashekar-memorial-award-sustainable-energy"
    },
    {
      "id":944,
      "title":"E.B. Dumbroff Award",
      "status":"Active",
      "value":"Amount varies.",
      "type":[
        "Scholarships"
      ],
      "description":"This award was established by colleagues and former graduate students of Professor Erwin B. Dumbroff in recognition of his contribution to plant science research and his training of graduate students and postdoctoral fellows. The award will be given to a graduate student for research excellence in any aspect of plant science and will consist of a monetary amount and a certificate and other forms of recognition, if appropriate. It will be awarded annually or less frequently (if there are no suitable candidates) as deemed appropriate by a Department of Biology Awards Committee.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Biology Department Graduate Coordinator for further information regarding this award.",
      "vid":9783,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/eb-dumbroff-award"
    },
    {
      "id":934,
      "title":"H. Winston Algate Scholarship",
      "status":"Active",
      "value":"Varies.",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship is to be used to support Vision Science graduate students. The award is made annually in the Fall term and is based upon academic excellence and financial need. Selection will be made by the School of Optometry and Vision Science.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Academic excellence",
          "Financial need",
          "Recipients will be registered the in Vision Science program at the graduate level. Selection will be made based on:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your School of Optometry Graduate Coordinator for further information regarding this award.",
      "vid":9773,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/h-winston-algate-scholarship"
    },
    {
      "id":935,
      "title":"Gustave O. Arlt Award in the Humanities",
      "status":"Active",
      "value":"$1000: The Award, made at the time of the CGS Annual Meeting, carries a stipend of $1,000, a certificate and reasonable travel expenses to attend the annual meeting in Seattle, Washington, December 2-5, 2015.",
      "type":[
        "Scholarships"
      ],
      "description":"Gustave O. Arlt (1895-1986) was the first president of the Council of Graduate Schools, former faculty member and Dean of the Graduate School at UCLA, and a scholar of German language and literature. In 1971 he established the award that bears his name to provide recognition, each year, to a young scholar who has written a book that represents an outstanding contribution to scholarship in the humanities.\n\nSubjects fields are selected annually. Awards have been made in literature, history, linguistics, foreign languages, philosophy, archaeology and musicology.\n\n2015\/2016's field is:\u00a0 Religious Studies",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Anthropology (Public issues)",
        "Arts",
        "Classical Studies",
        "English",
        "French Studies",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "The recipient must have received the doctorate within seven years of the award, and currently be teaching at a North American university.",
          "The recipient must have taken the degree at a North American university.",
          "The book being considered must have been published within seven years of the award. The book must have been written in or translated into English.",
          "The book must represent an outstanding contribution to scholarship in the field."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.cgsnet.org\/cgs-gustave-o-arlt-award-humanities"
      ],
      "contact":"Please see the\u00a0 Council of Graduate Studies website for further information regarding this award.",
      "vid":9774,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/gustave-o-arlt-award-humanities"
    },
    {
      "id":936,
      "title":"M Moo-Young Biochemical Engineering",
      "status":"Active",
      "value":"$1000: Varies from $1,000 to $2,000",
      "type":[
        "Scholarships"
      ],
      "description":"The endowment was established from revenues generated by an international biotechnology conference for which Dr. Murray Moo-Young served as Vice-Chair of the organizing committee. One or more scholarships will be awarded annually. Recipients will be selected by the Department of Chemical Engineering from new and continuing graduate students in the Biochemical Engineering (Biotechnology) option.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Chemical Engineering",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Chemical Engineering Department SGraduate Coordinator for further information regarding this award.",
      "vid":9775,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/m-moo-young-biochemical-engineering"
    },
    {
      "id":937,
      "title":"Irene Marguerite McLeod Postgraduate Scholarship",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established by Dr. Norman W. McLeod, FRSC, in honour of his wife, Irene Marguerite McLeod. It will be awarded annually, if suitable candidates exist, for postgraduate research in (1) bituminous materials, including recycling; (2) flexible pavement design; (3) any phase of land transportation by vehicles, excluding railroads, in order of preference. The recipient will normally be a graduate student in the Transport Group of the Department of Civil Engineering.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Civil &amp; Environmental Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9776,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/irene-marguerite-mcleod-postgraduate-scholarship"
    },
    {
      "id":938,
      "title":"Mackenzie King Scholarships",
      "status":"Active",
      "value":"$10500: The Open Scholarship is valued at $8,500 The Traveling Scholarships are valued at $10,500 each. Both award amounts are subject to change.",
      "type":[
        "Scholarships"
      ],
      "description":"The Mackenzie King Scholarships were established as an independent trust under the will of the late Rt. Hon. William Mackenzie King (1874-1950).\n\nTwo classes of Mackenzie King Scholarship are available to graduates of Canadian universities: the Open Scholarship and the Travelling Scholarship. Both are to support graduate study.\n\nThe Travelling Scholarship is available to graduates of Canadian universities who pursue graduate study in the United States or the United Kingdom in the areas of international or industrial relations.\u00a0\n\nThe Open Scholarship is available to graduates of Canadian universities who pursue graduate study in any discipline, in Canada or elsewhere.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The awards will be based on high academic achievements (typically all A\u2019s or very nearly so), personal qualities, and demonstrated aptitudes. Consideration will also be given to the applicant\u2019s proposed program of study.",
          "The awards will be made by, and at the sole discretion of, the Board of Scholarship of Trustees."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "See the Mackanzie King Scholarships website for further information and application instructions."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Scholarships Coordinator in the Graduate Studies Office for further information regarding this award.",
      "vid":9777,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/mackenzie-king-scholarships"
    },
    {
      "id":939,
      "title":"Fraser Award for Graduate Student Research",
      "status":"Active",
      "value":"Amount varies.",
      "type":[
        "Scholarships"
      ],
      "description":"The Fraser Award for Graduate Student Research is awarded yearly to the winner of the Management Sciences student research paper competition. It will be awarded in the Spring term to the student who wrote the best research paper in the previous three terms (Spring, Fall, Winter).\n\nSubmissions must be papers completed while the author was a student in the Management Sciences graduate program, and must reflect research carried out primarily in the Management Sciences Department. The student must be the main author of the paper, although the award may be shared among several Management Sciences student co-authors. The best paper will be chosen on the basis of overall research quality, taking into account the experience and field of the individual student. Submissions for the competition will be judged by a panel of professors within the Department, chosen by the Chair to reflect the various research interests of the Department of Management Sciences.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Management Sciences"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Management Sceicnes Department Graduate Coordinator for further information regarding this award.",
      "vid":9778,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/fraser-award-graduate-student-research"
    },
    {
      "id":941,
      "title":"Environment Graduate Student Scholarship",
      "status":"Active",
      "value":"Variable between $1,000 and $5,000.",
      "type":[
        "Scholarships"
      ],
      "description":"Awards valued between $1,000 and $5,000 will be provided to eligible graduate students who are registered full-time in the following programs in the Faculty of Environment: Master of Climate Change, Master of Development Practice, PhD.\u00a0 Students will be recommended by the Graduate Officer or Program Director to the Associate Dean of Graduate Studies, Faculty of Environment for selection.\u00a0 To be considered, students must be in good standing with a minimum overall average of B+ in their respective programs.\u00a0 Awards are typically made in the first year of a master's student's program of study and in the fourth year for students registered in a Doctoral program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Faculty fo Environment Departmental Graduate Coordinator for further information regarding this award.",
      "vid":9780,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/environment-graduate-student-scholarship"
    },
    {
      "id":942,
      "title":"El Gabbani Scholarship",
      "status":"Active",
      "value":"Amount varies.",
      "type":[
        "Scholarships"
      ],
      "description":"The El Gabbani Scholarship is awarded yearlyer to a deserving international student entering the Master of Applied Science Program in the Department of Management Sciences. This scholarship is named in honour of the El Gabbani family. It has been endowed in recognition of the value of the Management Sciences program in training foreign individuals, who, upon their return to their home countries use their acquired knowledge to improve the conditions of their people. The recipient of the award will be chosen by the Department of Management Sciences.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Management Sciences"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Preference will be given to international students with high academic potential and financial need."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Management Sciences Department Graduate Coordinator for further information regarding this award.",
      "vid":9781,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/el-gabbani-scholarship"
    },
    {
      "id":943,
      "title":"Economic Development Program Graduate Scholarship",
      "status":"Active",
      "value":"Amount varies.",
      "type":[
        "Scholarships"
      ],
      "description":"This award has been established for students enrolled in the Master of Applied Environmental Studies program in Industrial Development by the Economic Development Program, Faculty of Environmental Studies.\u00a0 The recipient of the award will be selected by the Admissions Committee for the MAES in Industrial Development.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Environment Department Graduate Coordinator for further information regarding this award.",
      "vid":9782,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/economic-development-program-graduate-scholarship"
    },
    {
      "id":958,
      "title":"Creative Writing Award",
      "status":"Active",
      "value":"$100",
      "type":[
        "Scholarships"
      ],
      "description":"One award for the best submission of either prose or poetry. It is a voluntary entry award.\u00a0 Students submit their work to the department for consideration.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Applicants must submit a piece of original work, either prose or poetry, to the English department."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the English Department Graduate Coordinator for further information regarding this award.",
      "vid":9797,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/creative-writing-award"
    },
    {
      "id":959,
      "title":"Ross and Muriel Cheriton Graduate Scholarship",
      "status":"Active",
      "value":"$5000: Will be paid as the institutional matching funds for an OGS or QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"Dr. David R. Cheriton established this research scholarship for a graduate student in the Faculty of Mathematics, School of Computer Science with preference given to students with concentration in the broad areas of computer systems and\/or computer networking. The student will hold an Ontario Graduate Scholarship (OGS). The final selection will be made by the Director of Graduate Studies in the School of Computer Science. This scholarship is open to Canadian and\/or permanent residents.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Contact the David R. Cheriton School of Computer Science Graduate Coordinator for further information regarding this award.",
      "vid":9798,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ross-and-muriel-cheriton-graduate-scholarship"
    },
    {
      "id":960,
      "title":"David R. Cheriton Graduate Scholarships in Computer Science",
      "status":"Active",
      "value":"$10,000- $20,000",
      "type":[
        "Scholarships"
      ],
      "description":"The David R. Cheriton Graduate Scholarships are valued at between $10,000 and $20,000 and will be awarded annually to forty to seventy-five full-time University of Waterloo graduate students in the David R. Cheriton School of Computer Science on the basis of scholastic excellence, evidence of research potential, as indicated by publications, letters of reference, and a demonstrated interest in research that addresses problems associated with designing and implementing efficient and reliable computing systems, along with their effective integration.\n\tThese scholarships are open to Canadian and International students holding a student visa.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your School of Computer Science Scholarship Coordinator for further information regarding this award.",
      "vid":9799,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-r-cheriton-graduate-scholarships-computer-science"
    },
    {
      "id":973,
      "title":"University of Waterloo Graduate Student Birth &amp; Parental Leave Bursary",
      "status":"Active",
      "value":"$8000: The maximum value of the bursary is $5,000 for the first term and $3,000 for the second term.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"The University of Waterloo will provide an eight-month birth and parental leave (includes adoption) bursary to eligible graduate students. The bursary, together with any other continuing support, is intended to maintain income at about 95% of the average level of income received by the student during the three previous academic terms, less tuition.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be a full or part time graduate student in good academic standing (and with no outstanding fees) who has been registered as such for at least two academic terms prior to the start of the leave;",
          "Be receiving financial support (ie. TA, RA, scholarship, bursary, sponsorships);",
          "Be taking a parental leave"
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Assistant Director Graduate Financial Aid &amp; Awards for further information regarding this award.",
      "vid":10590,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/university-waterloo-graduate-student-birth-parental-leave"
    },
    {
      "id":974,
      "title":"Millennium Graduate Bursary",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"The purpose of the bursary is to provide short term financial assistance for qualified international graduate students who will be registered full\u2010time in an approved graduate degree program. *Financial assistance is to cover basic needs and educational expenses only and is not normally given to students in the first term of their program.\n\t**Please note, students, who are Canadian Citizens or permanent residents, requiring financial assistance must apply for a bursary through the Student Awards and Financial Aid Office.",
      "citizenship":[
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Show evidence of financial need as determined by the completion of this application form.",
          "Be current full\u2010time graduate students in good standing with a valid Canadian Study Permit.",
          "Applicants must:"
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "February 15",
          "June 15",
          "October 15"
        ],
        "application":[
          "February 15",
          "June 15",
          "October 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Assistant Director Graduate Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9813,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/millennium-graduate-bursary"
    },
    {
      "id":975,
      "title":"University of Waterloo Day Care Bursary",
      "status":"Active",
      "value":"The value is assessed based on income, expenses, and number of children requiring day care.",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"The Graduate Student Association is pleased to support funding, through the Provost\u2019s Graduate Incentive Fund, for day care bursaries to graduate students. The bursaries are awarded each term to subsidize resources and are awarded based on financial need.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be registered full\u2010time graduate students",
          "Demonstrate financial need as determined based on the completion of this application",
          "Have the lowest net income in the family"
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Assistant Director Graduate Financial Aid &amp; Awards for further information regarding this award.",
      "vid":9814,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/university-waterloo-day-care-bursary"
    },
    {
      "id":976,
      "title":"Natural Sciences Engineering Research Council Postgraduate &amp; Canada Graduate Scholarships Doctoral (NSERC PGSD\/CGSD)",
      "status":"Active",
      "value":"Values are $21,000 for PGS-D and $35,000 for CGS-D annually.",
      "type":[
        "Scholarships"
      ],
      "description":"NSERC Canada Graduate Scholarships (CGS) and NSERC Postgraduate Scholarships (PGS) provide financial support to high-calibre scholars who are engaged in master\u2019s or doctoral programs in the natural sciences or engineering.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Applied Health Science",
        "Applied Mathematics",
        "Architecture",
        "Biology",
        "Environment &amp; Business",
        "Health Studies\/Gerontology",
        "Arts",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Environment &amp; Resource Studies",
        "Kinesiology",
        "MBET",
        "Chemical Engineering",
        "Computational Mathematics",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Geography &amp; Environmental Mgmt",
        "Public Health",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Environment",
        "Pharmacy",
        "Planning",
        "Recreation &amp; Leisure Studies",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Mathematics for Teachers",
        "Physics",
        "Social Innovation",
        "Management Sciences",
        "Physics and Astronomy",
        "Pure Mathematics",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Quantitative Finance",
        "Vision Science",
        "Statistics &amp; Actuarial Science",
        "Systems Design Engineering",
        "Psychology"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "See the NSERC Doctoral website for information on eligibility and selection."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Students must submit their application through the NSERC online application system by the deadline."
        ]
      },
      "deadlines":{
        "term":[
          "October 15"
        ],
        "application":[
          "October 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/awards-funding\/external-awards\/natural-sciences-engineering-research-council-nserc-doctoral",
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Contact your Department Graduate Coordinator for further information.",
      "vid":10585,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/natural-sciences-engineering-research-council-postgraduate"
    },
    {
      "id":983,
      "title":"Iron Ring Graduate Scholarship",
      "status":"Active",
      "value":"Varies",
      "type":[
        "Scholarships"
      ],
      "description":"Open to any graduate of the University of Waterloo Faculty of Engineering or Conestoga College undergraduate program.\u00a0 This scholarship will be awarded to a student undertaking Master's research in one of the University of Waterloo's Engineering departments.\u00a0 It will be awarded to the successful applicant in the first year of their program.\u00a0 The value of the scholarship is determined from time to time by the Office of the Dean of Engineering.\n\tThe applicant must maintain full time status throughout the tenure of the scholarship, in one of the Engineering departments at UW.\u00a0 Applicants will be evaluated based on 2 main criteria:\u00a0\u00a0 a) academic excellence, and b) leadership.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Engineering Department Graduate Scholarship Coordinator for further information regarding this award.",
      "vid":10899,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/iron-ring-graduate-scholarship"
    },
    {
      "id":979,
      "title":"Wayne Fox Graduate Scholarship",
      "status":"Active",
      "value":"$5000: Normally paid as the institutional matching funds for an OGS or a QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"The Wayne C. Fox scholarship was established to attract the very best students to the Faculty of Arts and to recognize the achievements of outstanding young scholars. The scholarships will be awarded on a rotating basis within the faculty to students who have received an Ontario Graduate Scholarship (OGS). The selection will be made by the Faculty Associate Dean, Graduate Studies.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Anthropology (Public issues)",
        "Arts",
        "Classical Studies",
        "Digital Experience Innovation",
        "Economics",
        "English",
        "Fine Arts",
        "French Studies",
        "German\/Russian",
        "Global Governance",
        "History",
        "Peace &amp; Conflict Studies",
        "Philosophy",
        "Political Science",
        "Psychology",
        "Public Service",
        "Religious Studies",
        "Sociology and Legal Studies",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9818,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/wayne-fox-graduate-scholarship"
    },
    {
      "id":980,
      "title":"Vanier Canada Graduate Scholarships (Vanier CGS)",
      "status":"Active",
      "value":"$50000: $50,000 per year for up to three years.",
      "type":[
        "Scholarships"
      ],
      "description":"The Vanier Canada Graduate Scholarships (Vanier CGS) program was created to attract and retain world-class doctoral students and to establish Canada as a global centre of excellence in research and higher learning. Vanier Scholars demonstrate leadership skills and a high standard of scholarly achievement in the social sciences and humanities, natural sciences and engineering, and health-related fields. Canadian and international students are eligible to be nominated for a Vanier Scholarship",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Doctoral"
        ],
        "eligibility":[
          "Be nominated by only one Canadian university, which must have received a Vanier CGS allocation;",
          "Be seeking financial support to pursue your first doctoral degree (or combined MA\/PhD or MD\/PhD). Note that only the PhD portion of a combined degree is eligible for funding;",
          "Intend to pursue, in the summer semester or the academic year following the announcement of results, full-time doctoral (or combined MA\/PhD or MD\/PhD) studies and research at the nominating university; Note that only the PhD portion of a combined degree is eligible for funding;",
          "Have completed no more than 20 months of doctoral studies as of May 1, (see Calculating Months of Doctoral Studies below);",
          "Have achieved a first-class average, as determined by your university, in each of the last two years of full-time study or equivalent. Applicants are encouraged to contact the university for its definition of a first-class average; and",
          "Not have already received a doctoral-level scholarship or fellowship from CIHR, NSERC or SSHRC to undertake or complete a doctoral degree.",
          "To be considered for a Vanier CGS, you must:",
          "The Graduate Studies Office will organize a University-wide Vanier CGS Selection Committee comprised of Waterloo faculty members to review nominations submitted by graduate departments and select Waterloo's nominees for the national competition. Once submitted to the appropriate granting agency, each nomination is evaluated by an agency-specific selection committee (CIHR, NSERC, SSHRC). Canadian universities each have a limit to the number of nominations they may submit to the Vanier Scholarship competition."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "See the GSO Vanier website for application instructions and further information."
        ]
      },
      "deadlines":{
        "term":[
          "September 30"
        ],
        "application":[
          "September 30"
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.cihr-irsc.gc.ca\/",
        "http:\/\/www.nserc-crsng.gc.ca\/",
        "http:\/\/www.sshrc-crsh.gc.ca\/",
        "http:\/\/www.vanier.gc.ca\/eng\/allocations_by_university-liste_d_attributions.aspx"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10573,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/vanier-canada-graduate-scholarships-vanier-cgs"
    },
    {
      "id":981,
      "title":"Trudeau Foundation Doctoral Scholarships",
      "status":"Active",
      "value":"$60000: The annual value is up to $60,000 per Scholar (including an annual travel allowance of $20,000) for up to four years.",
      "type":[
        "Scholarships"
      ],
      "description":"Each year, the Pierre Elliott Trudeau Foundation rewards outstanding doctoral candidates who are enrolled or about to be enrolled in a social sciences and humanities program and who are doing research in areas related to our four themes. This award, the most prestigious of its type in Canada, has continuously attracted the very best scholars in the social sciences and humanities, individuals with a passion for public engagement and who are likely to become leading national and international figures.\n\nThe award supports interdisciplinary research and original fieldwork by providing a substantial yearly allowance for research and travel, enabling the Scholars to gain first-hand contact with the diverse communities that can enrich their studies. Moreover, each Scholar is paired with a distinguished Trudeau Mentor selected by the Foundation among the most eminent Canadian practitioners in all sectors of public life. The Scholarship also offers the opportunity to interact with an exceptional community of leaders and committed individuals in every field of the social sciences and humanities, to participate in events organized by the Foundation and to hold their own workshops, through available financial support.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Be a Canadian citizen or landed immigrant applying to a doctoral program in the social sciences and humanities or registered full-time in the first or second year of such a program at a Canadian university",
          "Candidates are evaluated based on their academic achievement, which must be on par with the highest standards of the world\u2019s most prestigious doctoral scholarship programs. Future scholars must also demonstrate an ability to engage in lively exchange with other researchers and scholars, and have an expressed desire to contribute to public dialogue.",
          "ELIGIBILITY",
          "OR",
          "OR"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "A call for nominations will be sent to departments by the Graduate Studies Office in the Fall term. Interested students must complete an on-line application in the PORTAL by the Graduate Studies Office provided deadline."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10570,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/trudeau-foundation-doctoral-scholarships"
    },
    {
      "id":982,
      "title":"Liberation Scholarship",
      "status":"Active",
      "value":"You will receive a one-off scholarship to cover international travel and initial costs for your stay in the Netherlands, which you will receive one month after the start of your study period in the Netherlands.",
      "type":[
        "Scholarships",
        "International experience awards"
      ],
      "description":"To celebrate seventy years of liberation and to honour the sacrifices Canadian soldiers made for our freedom, the Netherlands introduces the Liberation Scholarship Program in 2015. As a token of lasting gratitude and friendship, seventy highly motivated Canadian students with a strong academic background will receive a scholarship to study at a Dutch university (of applied sciences) for 3 to 12 months between 2015-2017.\n\nThe Liberation Scholarship Program is offered by the Ministry of Foreign Affairs and the Ministry of Education, Culture and Science of the Netherlands, EP-Nuffic, 23 Dutch higher education institutions and a select group of Dutch and Dutch-Canadian companies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "You have Canadian citizenship.",
          "You apply for a study period of between three and twelve months at one of the participating Dutch higher education institutions.",
          "Your study period in the Netherlands starts before 1 September 2016.",
          "You meet the specific requirements of the institution of your choice."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "University of Humanistic Studies",
          "Leiden University",
          "VU University Amsterdam",
          "Hanze University of Applied Sciences",
          "The Hague University of Applied Sciences",
          "University of Groningen",
          "Tilburg University",
          "Apply directly at one of the participating Dutch higher education institutions before October 1st:"
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
      "contact":"For further information visit the Study in Holland website.",
      "vid":9821,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/liberation-scholarship"
    },
    {
      "id":972,
      "title":"Rhodes Scholarship",
      "status":"Active",
      "value":"A Rhodes Scholarship includes tuition, college fees, and a stipend covering living expenses for two and possibly three years of study at the University of Oxford.",
      "type":[
        "Scholarships"
      ],
      "description":"The Rhodes Scholarship is a postgraduate scholarship supporting exceptional students at the University of Oxford in England. Established in the will of Cecil Rhodes in 1902, the Rhodes is the oldest and perhaps most prestigious international scholarship program in the world which aims to nurture public-spirited world leaders.\n\nBasic Selection Criteria\n\tThe following 4 criteria are used in the election of scholars:\n\nLiterary and scholastic attainments\n\tEnergy to use one\u2019s talents to the fullest\n\tTruth, courage, devotion to duty, sympathy for and protection of the weak, kindliness, unselfishness and fellowship\n\tMoral force of character and instincts to lead and to take an interest in one\u2019s fellow beings for their intellectual distinction, physical vigour, character, commitment to service, and leadership",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Citizenship and residency- Candidates must be Canadian citizens or permanent residents of Canada; candidates may apply either in the province in which they are ordinarily resident (some exceptions apply) or in the province in which they have attended university.",
          "Age - Candidates must have reached their 19th birthday and not have passed their 25th birthday by October 1st, 2016; they must have been born after September 30, 1991 and October 1, 1997.",
          "Education - Applicants must have received an undergraduate degree before taking up the scholarship."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Assistant Director Awards &amp; Financial Aid in the Graduate Studies Office for further details.",
      "vid":10569,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/rhodes-scholarship"
    },
    {
      "id":971,
      "title":"Emergency Loan",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships",
        "Financial need awards\/bursaries"
      ],
      "description":"Interest-free emergency loans are available to full-time graduate students who are experiencing short-term financial difficulty; they are not meant to provide funding for arranging fees in order to become registered.\n\nLoans must be re-paid by the end of the term, and proof of an acceptable form of repayment must be provided.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Submit an electronic application and forward a copy via email to the Assistant Director, Financial Aid &amp; Awards in the Graduate Studies Office"
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Contact Assistant Director, Financial Aid &amp; Awards in the Graduate Studies Office\u00a0for further information.",
      "vid":9810,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/emergency-loan"
    },
    {
      "id":949,
      "title":"D.A. Sprott Entrance Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Entrance awards"
      ],
      "description":"The award will be made annually to a new entrant of the full-time MMath or PhD program in Statistics or Actuarial Science. The recipient must be entering with at least an 80% (A) average. The selection will be made by the Awards subcommittee of the Statistics and Actuarial Science Graduate Committee. The Department can agree to change the terms of the award at any time.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Mathematics",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the Statistics &amp; Actuarial Sciences Department Graduate Coordinator for further information regarding this award.",
      "vid":9788,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/da-sprott-entrance-award"
    },
    {
      "id":961,
      "title":"Norma Brown Award",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"This award was established in memory of Norma Brown, late wife of Chancellor Emeritus Bishop Arthur Brown.\u00a0 As a social worker, Norma fully understood the need for educated, trained personnel in the profession.\n\nStudents who have been accepted into the Bachelor\u2019s of Social Work or Master\u2019s of Social Work program may be considered for this award.\u00a0 Students can be registered full or part time and must have a minimum overall average of 75%.\u00a0 Applicants must have active experience in community service and caregiving areas in their community. Applicants must demonstrate financial need.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Sociology and Legal Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Sociology and Legal Studies Department Graduate Coordinator for further information regarding this award.",
      "vid":9800,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/norma-brown-award"
    },
    {
      "id":962,
      "title":"English - Independent Graduate Instructor Award for Excellence in Teaching",
      "status":"Active",
      "value":"$250",
      "type":[
        "Scholarships"
      ],
      "description":"Mentoring or supervising professors will nominate outstanding student teachers.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the English Department Scholarship Coordinator for further information regarding this award.",
      "vid":9801,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/english-independent-graduate-instructor-award-excellence"
    },
    {
      "id":963,
      "title":"Grade Average Award (English)",
      "status":"Active",
      "value":"$200",
      "type":[
        "Scholarships"
      ],
      "description":"This award is administered by English department. Selection is\n\tbased on performance in MA and PhD English programmes in the Faculty of Arts.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the English Department Scholarship Coordinator for further information regarding this award.",
      "vid":9802,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/grade-average-award-english"
    },
    {
      "id":964,
      "title":"English TA Award for Excellence in Teaching",
      "status":"Active",
      "value":"$250",
      "type":[
        "Scholarships"
      ],
      "description":"Mentoring or supervising professors will nominate outstanding student teachers in the English department.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the English Department Scholarship Coordinator for further information regarding this award.",
      "vid":9803,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/english-ta-award-excellence-teaching"
    },
    {
      "id":965,
      "title":"English Professional Writing Award",
      "status":"Active",
      "value":"$100",
      "type":[
        "Scholarships"
      ],
      "description":"This prize goes to the writer of a piece of professional writing (journalism, technical writing, on-line help, etc); maximum length 10 standard pages.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the English Department Graduate Coordinator for further information regarding this award.",
      "vid":9804,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/english-professional-writing-award"
    },
    {
      "id":966,
      "title":"Dr. T.E. Unny Memorial Award",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"The late T.E. Unny contributed significantly to the development of stochastic and statistical methods in hydrology and environmental engineering during his long and distinguished career. During his career as a professor in Civil Engineering and Systems Design Engineering at the University of Waterloo (1965-1991), Dr. Unny supervised many graduate students. Accordingly, the purpose of the award is to provide financial support for graduate students in the Faculty of Engineering who are working in the field of stochastic and statistical methods in hydrology and environmental engineering (evidence of the quality of your work in this field is required as part of your application).\n\nSelection will be made in the Department of Systems Design Engineering Graduate Office.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9805,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-te-unny-memorial-award"
    },
    {
      "id":967,
      "title":"Dr. Murray Brown Psychology Graduate Memorial Award",
      "status":"Active",
      "value":"$3000: May be paid as the institutional matching funds for an OGS or a QEII-GSST.",
      "type":[
        "Scholarships"
      ],
      "description":"The award, valued at a minimum of $3,000 will be awarded annually to a full-time UW graduate student registered in the department of Psychology in the Faculty of Arts. The scholarship can be awarded to a student who holds an Ontario Graduate Scholarship (OGS) or Queen Elizabeth II Graduate Scholarship in Science and Technology (QEII-GSST) which requires a matching component or can be given to a student on the basis of scholastic excellence and who is not concurrently receiving Tri-Agency funding (i.e. CIHR, NSERC, SSHRC). This scholarship has been established in memory of Dr. Murray Brown whose generous estate gift provided the funds to endow this award and support future psychology graduate students at the University of Waterloo.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Psychology"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Psychology Department Graduate Coordinator for further information regarding this award.",
      "vid":9806,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/dr-murray-brown-psychology-graduate-memorial-award"
    },
    {
      "id":968,
      "title":"Donald E. Grierson Memorial Award",
      "status":"Active",
      "value":"$1000: 1 award annually valued at $1,000 (minimum)",
      "type":[
        "Scholarships"
      ],
      "description":"The awards, valued at a minimum of $1,000 will be provided annually to a full-time doctoral student registered in the Department of Civil and Environmental Engineering in the Faculty of Engineering at the University of Waterloo who has demonstrated financial need who is in good academic standing (minimum 80%). Preference will be given to international students.\n\nStudents must complete the Graduate Student Award Application form (found on the Gradate Studies Awards website) and attach a one page summary on how their research in structural engineering aims to advance the analytical and\/or numerical technologies and has the greatest potential for impact either at the societal or theoretical level. Applications must be submitted to the Graduate Studies Office by February 1st.\n\nThis scholarship has been established by the past students, friends and family in memory of Professor Donald E. Grierson.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Graduate Award Application:"
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
        "https:\/\/uwaterloo.ca\/civil-environmental-engineering\/about\/people"
      ],
      "contact":"Please contact the department of Civil and Environmental Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9807,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/donald-e-grierson-memorial-award"
    },
    {
      "id":969,
      "title":"David Nimmo English Graduate Scholarship",
      "status":"Active",
      "value":"$2000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship will be provided annually to full-time graduate students registered in the Master\u2019s or Doctoral program in the Department of English language and Literature in the Faculty of Arts on the basis of academic excellence (minimum 80%). Students will be chosen by the Associate Char for Gradate Studies in English Language and Literature, in consultation with the Department Granduate Committee. This fund is made possible by a donation from David Clarence Nimmo in recognition of his formative years spent as an undergraduate student at the University of Waterloo in the Department of English Language and Literature.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "English"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10712,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/david-nimmo-english-graduate-scholarship"
    },
    {
      "id":901,
      "title":"Science Graduate Student Award",
      "status":"Active",
      "value":"$6.000 p.a for domestic doctoral students; $3,000 p.a. for domestic masters students; $3,000 for international doctoral and masters students.",
      "type":[
        "Scholarships"
      ],
      "description":"The purpose of this award is to support graduate students in the Faculty of Science, in the Departments of Biology, Chemistry and Earth and Environmental Sciences, and the Schools of Optometry and Vision Science, and Pharmacy, who are engaged in research-based programs.\u00a0 It is also aimed at reducing RA funding requirements from supervisors to encourage greater capacity for graduate students, and at encouraging students and supervisors to work together to ensure timely completion of their programs.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Earth &amp; Environmental Sciences",
        "Pharmacy",
        "Physics",
        "Physics and Astronomy",
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Be enrolled in a full-time thesis-based Masters or Doctoral program in the Faculty of Science, except those enrolled in the Department of Physics and Astronomy (those students are being funded separately through a separate award in Physics and Astronomy).",
          "Normally be of high academic standing in their program.",
          "Not hold another award greater than the value of this award (except entrance awards and IDSA\/IMSA).",
          "Be within the first 12 terms of a doctoral program, or within the first 6 terms of a thesis-based masters program.",
          "Applicants must:",
          "Masters students who direct transfer to doctoral studies after term 3 will have 3 terms of masters level support, followed by 12 terms of doctoral level support.\u00a0 If direct transfer happens later than term 4, doctoral level funding will start in the first term of doctoral registration, but not extend beyond a total of 15 terms of funding."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Science Department Graduate Coordinator for further information regarding this award.",
      "vid":9740,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/science-graduate-student-award"
    },
    {
      "id":900,
      "title":"UW Retirees&#039; Award",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"The University of Waterloo Retirees' Association has established this award fund to assist students who have proven financial need. Bursaries are awarded to full- or part-time graduate students enrolled in any discipline at the University of Waterloo.\n\nThis bursary will be adjudicated with in the Fall term by the Student Awards &amp; Financial Aid Office.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Recipients must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/home"
      ],
      "contact":"Please contact your Student Awards &amp; Financial Aid Office for further information regarding this award.",
      "vid":10246,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/uw-retirees-award"
    },
    {
      "id":902,
      "title":"Science FunMat Award",
      "status":"Active",
      "value":"$30000: Up to $30,000 p.a. for students enrolled in the IDS FunMat program.",
      "type":[
        "Scholarships"
      ],
      "description":"The goal of this award is to support graduate students, registered full-time in a Doctoral program in the Faculty of Science.\u00a0 Eligible students must be registered under the IDS FunMat program with the University of Bordeaux.\u00a0 This award provides University of Waterloo support in addition to the contributions from other partners.\u00a0 Students will be automatically considered for this award throughout their eligibility period and nominated by their departments to the Graduate Studies Associate Dean, Faculty of Science.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Biology",
        "Chemistry",
        "Earth &amp; Environmental Sciences",
        "Pharmacy",
        "Physics",
        "Physics and Astronomy",
        "Science",
        "Vision Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "To be considered students must be enrolled in a full-time thesis-based Doctoral program in the Faculty of Science under the IDS FunMat program with the University of Bordeaux."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Science Department Graduate Coordinator for further information regarding this award.",
      "vid":9741,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/science-funmat-award"
    },
    {
      "id":903,
      "title":"School of Accounting &amp; Finance PhD Scholarship",
      "status":"Active",
      "value":"Subject to the discretion of the Director or CoDirector of the PhD program, the amount of the scholarship may be adjusted on a year-to-year basis between the amount promised on admission and the ceiling of$10,000. \u00b7",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship is to be awarded to excellent students who have been admitted to the PhD program in accounting at the University of Waterloo. Up to 12 scholarships will be granted per year (this may vary). The amount of the scholarship will be used to reduce tuition for the year until that amount has been reduced to zero. The excess will be paid during that term.\n\tEach scholarship is for a maximum of four years, subject to the student remaining in satisfactory academic standing. Recipients will be selected by the Director or Co-Director of the PhD program in the School of Accounting and Finance.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Accounting Graduate Coordinator for further information regarding this award.",
      "vid":9742,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/school-accounting-finance-phd-scholarship"
    },
    {
      "id":904,
      "title":"Roman Baldur Memorial Engineering Award",
      "status":"Active",
      "value":"$2520",
      "type":[
        "Scholarships"
      ],
      "description":"The scholarship, valued at $2520 will be awarded annually to a full-time University of Waterloo graduate student registered in the Department of Mechanical and Mechatronics Engineering in the Faculty of Engineering.\u00a0 The scholarship will be awarded to a graduate student on the basis of scholastic excellence and a demonstrated interest in innovation.\u00a0 This scholarship has been established in memory of Roman Baldur by Vivienne and Roy Ojala, family, and friends of Roman Baldur.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Mechanical &amp; Mechatronics Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Mechanical &amp; Mechatronics Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9743,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/roman-baldur-memorial-engineering-award"
    },
    {
      "id":905,
      "title":"Renison Town and Gown Society Award",
      "status":"Active",
      "value":"$500: Two awards of $500 annually.",
      "type":[
        "Scholarships"
      ],
      "description":"Two awards valued at $500 each will be offered by the Renison Town and Gown Society, a network of active and involved women from the local community.\u00a0 They are meant to encourage students embarking upon their degrees in either Social Development Studies or the Bachelor or Master\u2019s of Social Work program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Sociology and Legal Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "In order to be considered for the award, students must be registered part-time, have a minimum overall average of 75% in the previous Fall term, and demonstrate financial need.\u00a0 Preference will be given to students who entered university from a non-traditional route (ie. community college, previous careers, parenting).\u00a0 Students must be able to show a record of involvement in community service."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9744,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/renison-town-and-gown-society-award"
    },
    {
      "id":906,
      "title":"Provost Doctoral Entrance Award (PDEA) for Women",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Entrance awards"
      ],
      "description":"The main purpose of this award is to provide any outstanding full-time female doctoral student (Canadian citizen, permanent resident or student on a study permit) an entrance scholarship in the amount of $5,000 for one year. The award is normally paid across two terms.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Eligible students must have a first-class (80%) standing, as well as an outstanding record of research accomplishments and\/or references citing significant future potential in research. The student must be willing to compete for all external awards for which she is eligible and must aspire to pursue a career in higher education and research."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9745,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/provost-doctoral-entrance-award-pdea-women"
    },
    {
      "id":907,
      "title":"Paul Jeffrey Mesbur Memorial Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"This award, valued at $1,000, is available to full-time or part-time students in the Bachelor of Social Work and Master\u2019s of Social Work programs.\u00a0 Applicants must be in good academic standing and be able to show financial need.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Sociology and Legal Studies"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-awards\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9746,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/paul-jeffrey-mesbur-memorial-award"
    },
    {
      "id":908,
      "title":"Ontario Graduate Fellowships",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"The fellowships, valued at no more than $4,000 per student per term will be awarded annually to full-time University of Waterloo graduate students registered in a degree-granting program in any Faculty.\u00a0 The fellowship will be awarded to graduate students on the basis of the student's achievement and potential as a graduate student, as manifested in the student's existing academic record and in his or her graduate application for admission.\u00a0 Students will be required to maintain the minimum average in their coursework as determined by their program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9747,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/ontario-graduate-fellowships"
    },
    {
      "id":887,
      "title":"George Mulamoottil Graduate Scholarship",
      "status":"Active",
      "value":"$1500: The value and number of awards may change from year to year. The goal is to provide at least one award valued at $1,500 annually.",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $1,500 will be awarded annually to a full-time graduate student enrolled in a Master\u2019s of Doctoral program in the Faculty of Environment on the basis of academic achievement of 80% over the last two completed years of study and demonstrated research or interest in environment planning more broadly.\n\nInterested students should submit an application to the Faculty of Environment Associate Dean\u2019s office by February 1st. This fund is made possible by a donation from Dean and Rose Ann Mutrie in honor of Professor George Mulamoottil, a Professor who helped Dean start his early career in Environmental Planning.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Environment &amp; Business",
        "Environment &amp; Resource Studies",
        "Geography &amp; Environmental Mgmt",
        "Environment",
        "Planning",
        "Social Innovation"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Faculty fo Environment Department Graduate Coordinator for further information regarding this award.",
      "vid":9726,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/george-mulamoottil-graduate-scholarship"
    },
    {
      "id":888,
      "title":"General Senate Graduate Scholarships",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Scholarships"
      ],
      "description":"The interest from this fund will be used to support graduate scholarships.\u00a0 The departments will select finalists by August 31, and the scholarships will normally be awarded at the beginning of the Fall term.\u00a0 These scholarships will be awarded to high quality graduate students at the MA or PhD levels.\u00a0 Students supported from this fund must be enrolled full-time in the graduate program, must be within their allowable time limits, and must not be supported by a major external scholarship such as the OGS, NSERC or SSHRC.\u00a0 Number of awards and amounts may vary from year to year.\u00a0",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9727,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/general-senate-graduate-scholarships"
    },
    {
      "id":889,
      "title":"GO-Bell Scholarships",
      "status":"Active",
      "value":"$12000: Up to $4,000 per term, for a total of up to $12,000 per year.",
      "type":[
        "Scholarships"
      ],
      "description":"The recipient must be enrolled as a full-time PhD student.\u00a0 Students are automatically considered when they apply for the PhD program.\u00a0 Current practice awards these scholarships for two years at up to $12,000 per year.\u00a0 These awards are funded by an endowment established by the Government of Ontario and Bell Emergis (from C.S. website).",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Faculty of Mathematics Department Graduate Coordinator for further information regarding this award.",
      "vid":9728,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/go-bell-scholarships"
    },
    {
      "id":891,
      "title":"Balsillie Doctoral Fellowships",
      "status":"Active",
      "value":"$25000: 12 scholarships offered per year",
      "type":[
        "Scholarships"
      ],
      "description":"The recipients of the Balsillie Doctoral Fellowship, valued at $25,000 per year, will be expected to involve themselves in research and policy-oriented CIGI events pertaining to their work.\u00a0 The Balsillie Doctoral Fellowship is renewable beyond one year for a maximum of four years, but renewal is not automatic.\u00a0 Each year a new application must be submitted.\u00a0 Selection will be made by the appropriate program directors in consultation with CIGI representatives and the respective University offices.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Global Governance",
        "Peace &amp; Conflict Studies",
        "Political Science",
        "Public Service"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Be enrolled in the Faculty of Arts, majoring in an international public policy-related program of study",
          "Demonstrate academic excellence",
          "Students must:"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9730,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/balsillie-doctoral-fellowships"
    },
    {
      "id":927,
      "title":"IQC Entrance Award",
      "status":"Active",
      "value":"$5000: Several awards valued at $5,000 will be available each term.",
      "type":[
        "Entrance awards"
      ],
      "description":"These awards are supported by a variety of sources including the Bell Family Fund and Industry Canada. The awards are made to graduate students entering studies in quantum information at the University of Waterloo, based on academic excellence and potential for research as determined by grades, research statements, and reference letters.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Engineering",
        "Computer Science",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Physics",
        "Physics and Astronomy",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The awards are given to graduate students entering studies in quantum information at the University of Waterloo, based on academic excellence and potential for research. All students applying to IQC will automatically be considered for this scholarship. Decisions will be made by the Institute for Quantum Computing Scholarship Committee, and will be based on grades, research statements, and references."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Visit the IQC website for further details."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9766,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/iqc-entrance-award"
    },
    {
      "id":886,
      "title":"Social Sciences &amp; Humanities Research Council Joseph-Armand Bombardier Canada Graduate Scholarships Master\u2019s (SSHRC CGSM)",
      "status":"Active",
      "value":"The Joseph-Armand Bombardier CGS Master's Scholarships funding opportunity offers one-time, non-renewable, 12-month awards, valued at $17,500.",
      "type":[
        "Scholarships"
      ],
      "description":"The Joseph-Armand Bombardier CGS Master's Scholarships funding opportunity seeks to develop research skills and assist in the training of highly qualified personnel by supporting students in the social sciences and humanities who demonstrate a high standard of achievement in undergraduate and early graduate studies.\n\nThis funding opportunity, together with the SSHRC Doctoral Awards, the Vanier CGS, the SSHRC Postdoctoral Fellowships and the Banting Postdoctoral Fellowships, help train Canada's researchers and leaders of tomorrow.\n\nTenable only at eligible Canadian universities, Joseph-Armand Bombardier CGS Master\u2019s Scholarships are open to applicants who will be registered as full-time students in a master's or combined undergraduate\/graduate program, or in the first year of a combined MA\/PhD program, and in a discipline supported by SSHRC.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Eligibility and Selection Criteria please visit our Tri-Agency (CIHR, NSERC, SSHRC) Canada Graduate Scholarships Master's (CGSM) webpage."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Visit our CGSM website for details on applying."
        ]
      },
      "deadlines":{
        "term":[
          "December 1"
        ],
        "application":[
          "December 1"
        ],
        "extended":null
      },
      "links":[
        "http:\/\/www.sshrc-crsh.gc.ca\/funding-financement\/programs-programmes\/fellowships\/doctoral-doctorat-eng.aspx",
        "http:\/\/www.vanier.gc.ca\/",
        "http:\/\/www.sshrc-crsh.gc.ca\/funding-financement\/programs-programmes\/fellowships\/postdoctoral-doctorat-eng.aspx",
        "http:\/\/banting.fellowships-bourses.gc.ca\/",
        "http:\/\/www.sshrc-crsh.gc.ca\/about-au_sujet\/policies-politiques\/statements-enonces\/list_eligible_institutions-liste_etablissements-admissibles-eng.aspx",
        "https:\/\/uwaterloo.ca\/graduate-studies\/awards-funding\/external-awards\/tri-agency-cihr-nserc-sshrc-canada-graduate-scholarships"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10587,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/social-sciences-humanities-research-council-joseph-armand"
    },
    {
      "id":909,
      "title":"Mathematics Domestic Graduate Student Award",
      "status":"Active",
      "value":"$6000: Doctoral students: $6,000 per year (split over 3 terms) Master's students: $3,000 per year (split over 3 terms)",
      "type":[
        "Scholarships"
      ],
      "description":"The goal of this award is to support domestic graduate students in the Faculty of Mathematics who are engaged in research-based (thesis) programs. It is also aimed at reducing RA funding requirements from supervisors to encourage grater capacity for domestic graduate students and at encouraging students and supervisors to work together to ensure timely completion of their programs.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Combinatorics &amp; Optimization",
        "Computational Mathematics",
        "Computer Science",
        "Mathematics",
        "Mathematics for Teachers",
        "Pure Mathematics",
        "Quantitative Finance",
        "Statistics &amp; Actuarial Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Canadian citizens or permanent residents",
          "Enrolled full-time in a thesis based Master's of Doctoral program in the Faculty of Mathematics",
          "Must have designated thesis supervisor(s)",
          "Must not hold any tri-agency award (CIHR, NSERC, SSHRC), Ontario Graduate Scholarship (OGS), Ontario Trillium Scholarship",
          "Must maintain a minimum average of 80%",
          "MMath thesis students must be within the fist 6 terms of their thesis-based Master's program",
          "Doctoral students admitted from a bachelor directly must be within 18 terms of their doctoral program",
          "Doctoral students admitted after obtaining a Master's degree must be within the first 12 terms of their doctoral program",
          "Master's students who transfer to doctoral studies will start in the first term of their doctoral registration but will not extend beyond a total (master's and doctoral) of 18 terms of funding\n\t\t\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Mathematics Department Graduate Coordinator for further information regarding this award.",
      "vid":9748,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/mathematics-domestic-graduate-student-award"
    },
    {
      "id":923,
      "title":"Graduate Excellence Award in Computer Science",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Entrance awards"
      ],
      "description":"The Graduate Excellence Award in Computer Science, valued at $5,000 per year, will be awarded to doctoral students registered full time in the School of Computer Science at the University of Waterloo. Applicants for the David R. Cheriton Graduate Scholarship in Computer Science will be automatically considered for this award.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Computer Science",
        "Mathematics"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          "Doctoral students registered full-time in the School of Computer Science at the University of Waterloo with a minimum cumulative average of 80%.\u00a0"
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the David R. Cheriton School of Computer Science Graduate Coordinator for further information regarding this award.",
      "vid":9762,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/graduate-excellence-award-computer-science"
    },
    {
      "id":924,
      "title":"Health Studies &amp; Gerontology Special Studentship Award",
      "status":"Active",
      "value":"$500",
      "type":[
        "Scholarships"
      ],
      "description":"The HSG Special Studentship Award is awarded each term (F,W,S)\n\tby the HSG Grad Committee (Grad Officer) to selected full-time graduate students in the HSG MSc and PhD programs.\n\tIt is meant as a supplement to other types of graduate support (not a scholarship or bursary).",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Health Studies\/Gerontology"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Must be full-time graduate students in the HSG MSc and PhD programs."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your\u00a0 AHS Department Graduate Coordinator for further information regarding this award.",
      "vid":9763,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/health-studies-gerontology-special-studentship-award"
    },
    {
      "id":925,
      "title":"Iris Yuzdepski Memorial Graduate Entrance Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"One entrance scholarship valued at up to $5,000 will be awarded annually in the Fall term to a graduate student entering the Masters of Anthropology program at the University of Waterloo.\u00a0 The award recipient will be selected based on academic excellence (min. 80% overall average of undergraduate program) and application for admission to the program.\u00a0 This fund is made possible by a very generous donation from the late Ian Williams in honour and memory of his partner in life Iris Yuzdepski.\u00a0 Iris achieved her BA with a major in Anthropology from the University of Waterloo in May, 1971.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Anthropology (Public issues)",
        "Arts"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact the Anthropology Department Graduate Coordinator for further information regarding this award.",
      "vid":9764,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/iris-yuzdepski-memorial-graduate-entrance-scholarship"
    },
    {
      "id":926,
      "title":"IQC David Johnston Award for Scientific Outreach",
      "status":"Active",
      "value":"$2500: Up to three awards valued at $2,500 will be given annually to current graduate students at the Institute for Quantum Computing (IQC) at the University of Waterloo",
      "type":[
        "Scholarships"
      ],
      "description":"This award was created to celebrate David Johnston\u2019s pivotal contributions to IQC at University of Waterloo, his passion for leadership and his enthusiasm for continuous learning, innovation and achievement. David Johnston was President at the University of Waterloo from 1999 to 2010.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Engineering",
        "Computer Science",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Physics",
        "Physics and Astronomy",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Full-time current graduate students at the Institute for Quantum Computing (IQC) at University of Waterloo",
          "Selection to be based on an illustrated outstanding commitment to scientific outreach and community engagement through volunteerism",
          "Selection will recognize students who are dedicated to promoting public awareness of quantum information research, general science and IQC in industry or the scientific and local communities",
          "Selection will celebrate students who have engaged the community to provide educational experiences that embody a culture of continuous learning and promote interest in scientific research",
          "This Award is intended to be in addition to any Research or Teaching Assistantship support from the department or a supervising Faculty Member",
          "This Award can be held simultaneously with other graduate awards (subject to the requirements of other scholarships\/awards)",
          "The award will be administered in accordance with University of Waterloo policies and practices (and the external scholarship programs as applicable) as amended from time to time."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Complete the application on the IQC website."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/institute-for-quantum-computing\/programs\/graduate-studies\/scholarships\/iqc-david-johnston-award-scientific-outreach",
        "https:\/\/services.iqc.uwaterloo.ca\/people\/"
      ],
      "contact":"Please contact the Institute for Quantum Computing for further information regarding this award.",
      "vid":9765,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/iqc-david-johnston-award-scientific-outreach"
    },
    {
      "id":928,
      "title":"IQC Achievement Award",
      "status":"Active",
      "value":"$5000: Several awards valued at $5,000 are available each term. These awards are supported by a variety of sources including the Bell Family Fund and Industry Canada.",
      "type":[
        "Scholarships"
      ],
      "description":"The awards are given to UW graduate students working on quantum information at the Institute for Quantum Computing, based on exceptional achievement in research. Decisions will be made by the IQC scholarship committee and will be based on grades, research statements, and references.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "Engineering",
        "Computer Science",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Physics",
        "Physics and Astronomy",
        "Science"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "The awards are made to UW graduate students working on quantum information at the University of Waterloo, based on academic\n\texcellence and potential for research as determined by grades, research statements, and reference letters."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Applications should include published papers or pre-prints of relevant work done while an IQC student, explain their contributions to the results, and describe the significance and potential impact of the work.",
          "Visit the IQC website for further details."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9767,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/iqc-achievement-award"
    },
    {
      "id":929,
      "title":"Greg Kiessling MBET Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship has been established to encourage excellence, attract outstanding students, and enhance the profile of the University of Waterloo's Master of Business, Entrepreneurship and Technology (MBET) program.\u00a0 The scholarship will be awarded to an outstanding student entering the MBET program.\u00a0 The recipient will be selected by the MBET admissions committee based on previous academic accomplishments and the ability to demonstrate, during an interview process, the entre(intra)preneurial attributes required to successfully complete the program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "MBET",
        "Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the CBET Department Graduate Coordinator for further information regarding this award.",
      "vid":9768,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/greg-kiessling-mbet-scholarship"
    },
    {
      "id":931,
      "title":"Hugh MacKinnon Graduate Scholarship",
      "status":"Active",
      "value":"$1200",
      "type":[
        "Entrance awards"
      ],
      "description":"Two awards will be made annually by the Department of History to incoming graduate students on a one-time basis. The criteria will include community service and work experience among the pool of admissible candidates. The selection will be made by the History Graduate Studies Committee.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "History"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the History Department Graduate Coordinator for further information regarding this award.",
      "vid":9770,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/hugh-mackinnon-graduate-scholarship"
    },
    {
      "id":932,
      "title":"Graduate Studies Research Travel Assistantship",
      "status":"Active",
      "value":"$500: Up to $500",
      "type":[
        "Scholarships"
      ],
      "description":"A small fund is available each term for the purpose of assisting University of Waterloo graduate students to attend professional conferences, and present their research. Students will normally be the first author, and must be a conference presenter. Graduate Studies Office travel funds are normally awarded to a graduate student only once per year. The application form and regulations are available on the GSO website.",
      "citizenship":[
        "Canadian\/Permanent resident",
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
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "April 1",
          "August 1",
          "December 1"
        ],
        "application":[
          "April 1",
          "August 1",
          "December 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Graduate Financial Officer &amp; Analyst for further information.",
      "vid":11059,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/graduate-studies-research-travel-assistantship"
    },
    {
      "id":933,
      "title":"Marie Curie Graduate Student Award (Marie Curie GSA)",
      "status":"Active",
      "value":"$6000: Up to $6000 per year for doctoral and masters students (taking into account students\u2019 funding, including internal and external funding)",
      "type":[
        "Scholarships"
      ],
      "description":"The goal of this award is to support graduate students registered full-time in the Department of Physics and Astronomy, Faculty of Science, who are engaged in research-based programs. \u00a0\n\nStudents must be within the first 12 terms of a doctoral program (extended to 15 terms if entered from a bachelor\u2019s degree), or within the first 6 terms of a thesis-based master\u2019s program.\u00a0 Masters students who directly transfer to doctoral studies will be eligible for 15 terms of funding starting from the admission into the Masters program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Physics and Astronomy",
        "Science"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Physics &amp; Astronomy Department Graduate Coordinator for further information regarding this award.",
      "vid":9772,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/marie-curie-graduate-student-award-marie-curie-gsa"
    },
    {
      "id":922,
      "title":"Hira and Renu Ahuja International Graduate Scholarship",
      "status":"Active",
      "value":"$20000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship, valued at $20,000 will be provided annually to a full-time graduate student with a valid Canadian study permit enrolled in the Masters or Doctoral program in the Faculty of Engineering on the basis of academic excellence (minimum 80%).\u00a0 Preference will be given to students who either completed their undergraduate degree at Thapar University in Punjab or graduated from an Indian Institute of Technology (IIT) and who have been living in India. This scholarship is made possible by a donation from Professor Hira Ahuja.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact your Engineering Department Graduate Coordinator for further information regarding this award.",
      "vid":9761,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/hira-and-renu-ahuja-international-graduate-scholarship"
    },
    {
      "id":921,
      "title":"Indian Institutes of Technology (IIT) Doctoral Entrance Scholarship",
      "status":"Active",
      "value":"$5000",
      "type":[
        "Entrance awards"
      ],
      "description":"Effective May 1, 2014, the IIT Doctoral Entrance Scholarship, valued at $5,000, will be awarded to international students admitted into a full-time doctoral program at Waterloo, who have previously received either their Bachelor\u2019s or Master\u2019s degree from an Indian Institute of Technology prior to being admitted. Students must hold a valid Canadian study permit and have achieved a first-class average in each of the last two years of full-time study. Only students admitted to the Faculty of Engineering, the Faculty of Mathematics or the Faculty of Science will be considered.\u00a0 Each department will review the applications for admission to their doctoral program each year and submit a ranked list of nominated candidates to the Faculty Associate Dean of Graduate Studies for final selection in March.\n\nNote: This scholarship will be discontinued as of May 1st, 2016.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Applied Mathematics",
        "Architecture",
        "Biology",
        "Chemistry",
        "Combinatorics &amp; Optimization",
        "MBET",
        "Chemical Engineering",
        "Computational Mathematics",
        "Earth &amp; Environmental Sciences",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Computer Science",
        "Pharmacy",
        "Electrical &amp; Computer Eng",
        "Mathematics",
        "Mathematics for Teachers",
        "Physics",
        "Management Sciences",
        "Physics and Astronomy",
        "Pure Mathematics",
        "Science",
        "Mechanical &amp; Mechatronics Eng",
        "Quantitative Finance",
        "Vision Science",
        "Statistics &amp; Actuarial Science",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":10906,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/indian-institutes-technology-iit-doctoral-entrance"
    },
    {
      "id":910,
      "title":"Master&#039;s of Arts in Global Governance Internship Award",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships"
      ],
      "description":"Students in the Master\u2019s of Arts in Global Governance who are not currently in receipt of a Balsillie Fellowship or who hold a Balsillie Felllowship and choose not to use the Balsillie Fellowship toward the internship component of the degree may be eligible for consideration of this award valued at a maximum of $1,500. Decisions relating to the allocation of internship awards, and the amounts awarded to each recipient are made by the Director of the Master\u2019s of Arts in Global Governance program. Decisions are based on the anticipated costs associated with a particular placement, considerations related to financial need, as well as the availability of awards. Priority will be given to students who do not hold paid internships.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Global Governance"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact teh Global Governance Graduate Coordinator for further information regarding this award.",
      "vid":9749,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/masters-arts-global-governance-internship-award"
    },
    {
      "id":911,
      "title":"Master of Taxation (MTax) Graduate Entrance Scholarship",
      "status":"Active",
      "value":"$3500",
      "type":[
        "Entrance awards"
      ],
      "description":"This entrance scholarship will be awarded to full-time students with the a 90% or above average mark in selected tax courses in an undergraduate program at a participating university. Scholarships of 50% of the first term's tuition will be awarded. Up to four entrance scholarships will be awarded annually in the Fall term.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Students admitted to the full-time stream of the Master of Taxation program who have completed a 4-year honours undergraduate degree within the past five school years may be considered for this award.\u00a0",
          "Students must have completed two advanced-level tax courses as part of their degree requirements.\u00a0 The advanced level tax courses will normally be a 3rd year personal tax course and 4th year corporate tax course as recognized by the Institute of Chartered Accountants of Ontario (ICAO) as qualifying for their 51 credit-hour requirement.\u00a0 These courses will generally be taken as part of the student\u2019s undergraduate degree requirements and should be half-credit courses of 12 weeks in length in a classroom setting (not on-line learning)."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people\/departmentprogram-graduate-co-ordinators"
      ],
      "contact":"Please contact The Master of Taxation Graduate Coordinator for further information regarding this award.",
      "vid":9750,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/master-taxation-mtax-graduate-entrance-scholarship"
    },
    {
      "id":912,
      "title":"Master of Public Service Internship Award",
      "status":"Active",
      "value":"Decisions relating to the allocation of internship awards, and the amounts awarded to each recipient, are made by the Director of the Master of Public Service program. Decisions are based on the anticipated costs associated with a particular internship, considerations related to financial need, as well as the availability of awards. The maximum award a student would receive is $3,000 per term.",
      "type":[
        "Scholarships"
      ],
      "description":"Students in the Master of Public Service program who have arranged an internship are eligible to be considered for this award, valued at a maximum of $3,000. Decisions relating to the allocation of internship awards, and the amounts awarded to each recipient, are made by the Director of the Master of Public Service program. Decisions are based on the anticipated costs associated with a particular internship,considerations related to financial need, as well as the availability of awards.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Public Health"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Students in the Master of Public Service program who are unable to secure paid co-op employment, and who have arranged an unpaid internship, are eligible to be considered for this award."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Students must submit to the MPS Program Officer an application that describes the internship and provides an estimate of costs for the term. The application form is available on the MPS Learn site and is due on the last business day of the first month of the internship term."
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Public Service Graduate Coordinator for further information regarding this award.",
      "vid":9751,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/master-public-service-internship-award"
    },
    {
      "id":913,
      "title":"Master of Public Health (MPH) Practicum Award",
      "status":"Active",
      "value":"Many practicum sites are unable to offer the students any kind of financial support for the work that they provide. In these cases the Dept of HSG through the Chair has indicated that support will be provided to a maximum of$6000 (approx. TA amount). It was also decided that if students are being paid for their practicum term by the host site but are incurring additional expenses in order to take a practicum at a distant location, this award can be applied to support relocation expenses.",
      "type":[
        "Scholarships"
      ],
      "description":"The MPH Practicum Award is an award that MPH students can apply to receive before they begin their practicum term, generally Winter term in their final year of this graduate program.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Public Health"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Contact the Public Health Department Graduate Coordinator for application information.",
      "vid":9752,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/master-public-health-mph-practicum-award"
    },
    {
      "id":914,
      "title":"Master of Public Health (MPH) Graduate Award",
      "status":"Active",
      "value":"Each award is valued between $100 to $1,000. The value awarded to each student will be determined by the department chair in consultation with the MPH Leader and program committee. The value and total number of awards offered in a given year may be subject to the availability of department funds. The award will not be granted to MPH students carrying another University graduate award\/scholarship or external graduate award\/scholarship if the overall value of the other award(s) and scholarship(s) exceeds $17,500 per year. For MPH students who receive another award\/scholarship less than $17,500 per year, all or a portion of the MPH award will be granted so as not to exceed an overall total limit of $17,500 per year.",
      "type":[
        "Scholarships"
      ],
      "description":"The purpose of this award is to recognize dedication to the field of public health and enhance more equitable access to the Masters of Public Health degree.\n\tAwards range in value between $100 and $1000 and will be distributed to awardees after successful completion of their first term and\/or during their final term 111 the MPH program. The students must be registered in their second term of the first year and\/or in their final term of the MPH program before this award will be issued.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Applied Health Science",
        "Public Health"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          "Students must have successfully completed their first term in the MPH program, including successful completion of PHS 60 I, and be registered in a current term within the first year of the MPH program before this award will be issued.",
          "The award may be granted to full-time and part-time graduate students enrolled in good standing in the program. Students on\n\tacademic probation or reduced load in a given term are not eligible for the award without the express consent of the MPH Director.",
          "The award will not be granted to MPH students carrying another University graduate award\/scholarship or external graduate award\/scholarship if the overall value of the other award(s) and scholarship(s) exceeds $17,500 per year. For MPH students who receive another award\/scholarship less than $17,500 per year, all or a portion of the MPH award will be granted so as not to exceed an overall total limit of $17,500 per year."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        
      ],
      "contact":"Please contact the Public Health Department Graduate Coordinator for further information regarding this award.",
      "vid":9753,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/master-public-health-mph-graduate-award"
    },
    {
      "id":915,
      "title":"Lorne H. Russwurm Memorial Award",
      "status":"Active",
      "value":"$0: Varies",
      "type":[
        "Financial need awards\/bursaries"
      ],
      "description":"This award has been established in memory of Lorne Russwurm, an internationally known researcher and Professor of Geography 1967-1987.\u00a0 Recipients of this award will normally be undergraduate geography students entering 2nd, 3rd, or 4th year who began studies as a mature student, have above average academic standing and who have demonstrated a need for financial assistance.\u00a0 Consideration may be given to mature graduate students and to undergraduate Geography students in general.\u00a0 Preference will be given to students who have actively participated in student, community or other organizations.\u00a0 Applications are available from the SAFA office.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Geography &amp; Environmental Mgmt",
        "Environment"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Applicants must have resided in Ontario for 12 months prior to beginning their post - secondary education."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "October 15"
        ],
        "application":[
          "October 15"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/student-awards-financial-aid\/"
      ],
      "contact":"Please contact the Student Awards &amp; Financial Aid Office for further information regarding this award.",
      "vid":10242,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/lorne-h-russwurm-memorial-award"
    },
    {
      "id":917,
      "title":"Laurence Hamlin Memorial Award",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"This annual award has been established in memory of Laurence Hamlin, BASc 94, MASc 96 (Civil), in recognition of the significant contributions to classroom teaching being made by graduate students within the Faculty of Engineering's Civil Engineering program and specifically the environmental and water resources area. The awards, consisting of a cash prize and a citation, are open to individuals who are currently involved, or have recently been involved, in teaching UW undergraduate students in the Environmental Engineering (Civil) program while pursuing a course of study leading to a graduate degree within the Faculty of Engineering. Selection will be made annually by the Civil Engineering Undergraduate Chair.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Engineering",
        "Civil &amp; Environmental Eng"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Civil &amp; Environmental Department Graduate Coordinator for further information regarding this award.",
      "vid":9756,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/laurence-hamlin-memorial-award"
    },
    {
      "id":918,
      "title":"Lalit Chugh and Hira Ahuja International Graduate Scholarship",
      "status":"Active",
      "value":"$20000",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at up to $20,000 will be provided annually to a full-time graduate student enrolled in a Master\u2019s or Doctoral program in the Faculty of Engineering on the basis of academic excellence (minimum 80%).\u00a0 Master\u2019s students may receive this award for a maximum of two years and Doctoral students for a maximum of four years provided they maintain good academic standing (minimum 80%) and continue to remain registered full time in their program.\u00a0 Recipients must be international students who hold a valid Canadian study permit.\u00a0 Preference will be given to students who have lived in India and who completed their undergraduate studies at Thapar Engineering University in Punjab. This scholarship is made possible by a donation from Professor Hira Ahuja in memory of his daughter Lalit Chugh.",
      "citizenship":[
        "International\/study permit student"
      ],
      "programs":[
        "Architecture",
        "MBET",
        "Chemical Engineering",
        "Engineering",
        "Civil &amp; Environmental Eng",
        "Electrical &amp; Computer Eng",
        "Management Sciences",
        "Mechanical &amp; Mechatronics Eng",
        "Systems Design Engineering"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts"
      ],
      "contact":"Please contact your Department Graduate Coordinator for further information regarding this award.",
      "vid":9757,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/lalit-chugh-and-hira-ahuja-international-graduate"
    },
    {
      "id":919,
      "title":"John Waterhouse PhD Scholarship",
      "status":"Active",
      "value":"$1000",
      "type":[
        "Scholarships"
      ],
      "description":"This scholarship is named in honour of Dr. John Waterhouse, Director of the School of Accountancy from 1991 to 1997, to mark his special interest in the School's PhD program and its students. One scholarship will be awarded each academic year to support the dissertation research of a PhD student for travel, data gathering, or any other research-related activity. Selection will be made by the Director of the PhD program in the School of Accountancy.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts",
        "Taxation"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          ""
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          ""
        ],
        "application":[
          ""
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about-graduate-studies\/graduate-studies-department-contacts\/scholarship-co-ordinators"
      ],
      "contact":"Please contact the Taxation Graduate Coordinator for further information regarding this award.",
      "vid":9758,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/john-waterhouse-phd-scholarship"
    },
    {
      "id":920,
      "title":"John M. Harper and William J. Harper Scholarship",
      "status":"Active",
      "value":"$2500",
      "type":[
        "Scholarships"
      ],
      "description":"A scholarship valued at $2,500 is provided annually to a full-time graduate student enrolled in the Master of Accounting program at the School of Accounting and Finance in the Faculty of Arts on the basis of academic achievement and extracurricular involvement in the KW region. Interested students must submit an application each year. Applicants should contact the School of Accounting and Finance for more details. This fund is made possible by a donation from the family and friends of John M. and Jim Harper in recognition of their support to the University of Waterloo.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Accounting",
        "Arts"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Letter explaining how you meet the award criteria",
          "Resume required"
        ],
        "additional":[
          "Include a copy of a recent grade report with your application."
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
        
      ],
      "contact":"Please contact the School of Accounting Graduate Coordinator for further information regarding this award.",
      "vid":10859,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/john-m-harper-and-william-j-harper-scholarship"
    },
    {
      "id":885,
      "title":"Canadian Institutes of Health Research Master&#039;s Award (CIHR CGSM)",
      "status":"Active",
      "value":"The maximum amount per award is $17,500 for up to one year. This funding is non-renewable",
      "type":[
        "Scholarships"
      ],
      "description":"The Tri-Agency CGS-M Award provides financial support to high caliber scholars who are engaged in eligible Master\u2019s or, in some cases, doctoral programs in Canada. This support allows these scholars to fully concentrate on their studies in their chosen fields.\u00a0 The objective of this scholarship program is to help develop research skills and assist in the training of highly qualified personnel by supporting students who demonstrate a high standard of achievement in undergraduate and early graduate studies.",
      "citizenship":[
        "Canadian\/Permanent resident"
      ],
      "programs":[
        "Open to any program"
      ],
      "application":{
        "type":[
          "Application required"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          "Eligibility and Selection Criteria please visit our Tri-Agency (CIHR, NSERC, SSHRC) Canada Graduate Scholarships Master's (CGSM) webpage."
        ],
        "instructions":[
          ""
        ],
        "additional":[
          "Visit our CGSM website for details on applying."
        ]
      },
      "deadlines":{
        "term":[
          "December 1"
        ],
        "application":[
          "December 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/awards-funding\/external-awards\/tri-agency-cihr-nserc-sshrc-canada-graduate-scholarships"
      ],
      "contact":"For further information on applying for a CIHR CGSM visit our CGSM website.",
      "vid":10589,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/canadian-institutes-health-research-masters-award-cihr-cgsm"
    },
    {
      "id":884,
      "title":"Briarhurst Travel &amp; Research Award",
      "status":"Active",
      "value":"$1500",
      "type":[
        "Scholarships"
      ],
      "description":"An award valued at $1,500, will be provided annually to a graduate student registered full-time Global Governance or Environment and Resource Studies.\u00a0 The purpose of this award is to assist students with travel costs associated with conducting research for their final dissertation.\u00a0 Selection will be based on academic excellence (minimum cumulative average of 80% in the current graduate program) and on the estimated travel costs associated with the field research as determined through the completion of the Briarhurst Travel and Research Award Application.\u00a0 Interested students should apply to the Graduate Studies Office.\u00a0 This fund is made possible by a donation from Drs. Thomas Homer-Dixon and Sarah Wolfe and is intended to assist with the cost of completing field research.",
      "citizenship":[
        "Canadian\/Permanent resident",
        "International\/study permit student"
      ],
      "programs":[
        "Arts",
        "Environment &amp; Resource Studies",
        "Environment",
        "Global Governance"
      ],
      "application":{
        "type":[
          "Student selected automatically by Faculty\/Department"
        ],
        "enrollment_year":[
          "Masters",
          "Doctoral"
        ],
        "eligibility":[
          
        ],
        "instructions":[
          "Award\/bursary application:"
        ],
        "additional":[
          
        ]
      },
      "deadlines":{
        "term":[
          "March 1"
        ],
        "application":[
          "March 1"
        ],
        "extended":null
      },
      "links":[
        "https:\/\/uwaterloo.ca\/graduate-studies\/about\/people"
      ],
      "contact":"Please contact the Graduate Financial Officer &amp; Analyst in the Graduate Studies Office for more information.",
      "vid":10901,
      "link":"https:\/\/uwaterloo.ca\/graduate-studies\/awards\/briarhurst-travel-research-award"
    }
  ]
}
```


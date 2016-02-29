# List of UW employees with salaries more than $100k/yr

```
GET /resources/sunshinelist.{format}
```

## Description

> This method returns a list of all UW employees that earn more than $100k/yr

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
    <td>1427</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>resources</td>
    <td><b>Service ID</b></td>
    <td>229</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>IAP</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Currently the data exists for all years: 1996-2014
- This endpoint contains the University's salary disclosures (as required by the Public Sector Salary Disclosure Act, 1996). It does not include any addendum data.
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/tree/master/Salaries
- http://www.fin.gov.on.ca/en/publications/salarydisclosure/pssd/


## Parameters

```
GET /resources/sunshinelist.{format}
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
    <td><b>year</b></td>
    <td>filter</td>
    <td><i>no</i></td>
    <td>Four digit year representation</td>
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
GET /resources/sunshinelist.{format}
```

- **https://api.uwaterloo.ca/v2/resources/sunshinelist.json**
- **https://api.uwaterloo.ca/v2/resources/sunshinelist.xml**
- **https://api.uwaterloo.ca/v2/resources/sunshinelist.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>employer</b></td>
    <td>string</td>
    <td>Name of Employer (UW)</td>
  </tr>
  <tr>
    <td><b>surname</b></td>
    <td>string</td>
    <td>Last name of the employee</td>
  </tr>
  <tr>
    <td><b>given_name</b></td>
    <td>string</td>
    <td>Given name of the employee</td>
  </tr>
  <tr>
    <td><b>position</b></td>
    <td>string</td>
    <td>Employee's position at the University</td>
  </tr>
  <tr>
    <td><b>salary_paid</b></td>
    <td>number</td>
    <td>Salary paid per annum in dollars</td>
  </tr>
  <tr>
    <td><b>taxable_benefits</b></td>
    <td>number</td>
    <td>Employee's taxable benefits in dollars</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":789779,
    "timestamp":1451857662,
    "status":200,
    "message":"Request successful",
    "method_id":1427,
    "method":{
      "year_min":1996,
      "year_max":2014,
      "year_displaying":2014
    }
  },
  "data":[
    {
      "employer":"University of Waterloo",
      "surname":"AAGAARD",
      "given_name":"MARK",
      "position":"Associate Professor",
      "salary_paid":"$159,754.44",
      "taxable_benefits":"$434.84"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ABDEL-RAHMAN",
      "given_name":"EIHAB",
      "position":"Associate Professor",
      "salary_paid":"$147,738.88",
      "taxable_benefits":"$240.88"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ABOUEE MEHRIZI",
      "given_name":"HOSSEIN",
      "position":"Assistant Professor",
      "salary_paid":"$128,636.99",
      "taxable_benefits":"$192.64"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ABUKHDEIR",
      "given_name":"NASSER MOHIEDDI",
      "position":"Assistant Professor",
      "salary_paid":"$121,006.52",
      "taxable_benefits":"$468.52"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ACHESON",
      "given_name":"KATHERINE",
      "position":"Associate Professor",
      "salary_paid":"$143,134.18",
      "taxable_benefits":"$572.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ACTON",
      "given_name":"CAROL",
      "position":"Associate Professor, St. Jerome's University",
      "salary_paid":"$121,102.72",
      "taxable_benefits":"$334.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ADAIR",
      "given_name":"WENDI L.",
      "position":"Associate Professor",
      "salary_paid":"$131,631.20",
      "taxable_benefits":"$509.60"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ADCOCK",
      "given_name":"JAMES",
      "position":"Lecturer",
      "salary_paid":"$101,095.56",
      "taxable_benefits":"$244.44"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AFSHORDI",
      "given_name":"NIYAYESH",
      "position":"Assistant Professor",
      "salary_paid":"$103,055.84",
      "taxable_benefits":"$285.00"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AGER",
      "given_name":"SHEILA L",
      "position":"Associate Professor",
      "salary_paid":"$171,606.40",
      "taxable_benefits":"$279.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AGNEW",
      "given_name":"GORDON",
      "position":"Associate Professor",
      "salary_paid":"$154,935.84",
      "taxable_benefits":"$256.96"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AKHUNDOV",
      "given_name":"ILHAM",
      "position":"Lecturer",
      "salary_paid":"$114,602.20",
      "taxable_benefits":"$171.96"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ALENCAR",
      "given_name":"PAULO S",
      "position":"Professor",
      "salary_paid":"$144,171.48",
      "taxable_benefits":"$276.30"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ALLEN",
      "given_name":"JOE",
      "position":"Manager, Enterprise Systems",
      "salary_paid":"$106,669.40",
      "taxable_benefits":"$177.04"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AL-MAYAH",
      "given_name":"ADIL",
      "position":"Assistant Professor",
      "salary_paid":"$127,953.56",
      "taxable_benefits":"$353.88"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDERSON",
      "given_name":"BRITT",
      "position":"Associate Professor",
      "salary_paid":"$107,131.20",
      "taxable_benefits":"$296.24"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDERSON",
      "given_name":"DANIEL",
      "position":"Director, Police Services",
      "salary_paid":"$122,364.32",
      "taxable_benefits":"$473.76"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDERSON",
      "given_name":"WILLIAM A.",
      "position":"Professor",
      "salary_paid":"$169,017.52",
      "taxable_benefits":"$631.04"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDERSON",
      "given_name":"WILLIAM B.",
      "position":"Associate Professor",
      "salary_paid":"$128,447.48",
      "taxable_benefits":"$497.20"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDRE",
      "given_name":"ROBERT",
      "position":"Lecturer",
      "salary_paid":"$114,570.56",
      "taxable_benefits":"$190.12"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDREWS",
      "given_name":"DOUGLAS",
      "position":"Lecturer",
      "salary_paid":"$138,103.92",
      "taxable_benefits":"$495.96"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDREY",
      "given_name":"JEAN",
      "position":"Interim Dean, Environment",
      "salary_paid":"$172,174.44",
      "taxable_benefits":"$269.92"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANDRIGHETTI",
      "given_name":"RICHARD E",
      "position":"Lecturer",
      "salary_paid":"$118,755.12",
      "taxable_benefits":"$197.00"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANGERILLI",
      "given_name":"NELLO",
      "position":"Associate Vice-President, International",
      "salary_paid":"$231,298.96",
      "taxable_benefits":"$818.00"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANNABLE",
      "given_name":"WILLIAM K",
      "position":"Associate Professor",
      "salary_paid":"$132,845.20",
      "taxable_benefits":"$514.28"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ANTHONY",
      "given_name":"KELLY K",
      "position":"Lecturer",
      "salary_paid":"$101,571.92",
      "taxable_benefits":"$443.36"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ARAVENA",
      "given_name":"RAMON O",
      "position":"Professor",
      "salary_paid":"$137,000.04",
      "taxable_benefits":"$227.16"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ARMITAGE",
      "given_name":"DEREK R",
      "position":"Associate Professor",
      "salary_paid":"$141,918.36",
      "taxable_benefits":"$548.04"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ARMITAGE",
      "given_name":"HOWARD M",
      "position":"Special Advisor to the President, Entrepreneurship",
      "salary_paid":"$204,985.64",
      "taxable_benefits":"$178.55"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ARMITAGE",
      "given_name":"SUMAN",
      "position":"Director, Communications & Marketing",
      "salary_paid":"$100,526.92",
      "taxable_benefits":"$389.20"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AROCHA",
      "given_name":"JOSE",
      "position":"Associate Professor",
      "salary_paid":"$126,962.28",
      "taxable_benefits":"$501.52"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ATKINSON",
      "given_name":"J. LOGAN",
      "position":"University Secretary & General Counsel",
      "salary_paid":"$235,986.08",
      "taxable_benefits":"$888.53"
    },
    {
      "employer":"University of Waterloo",
      "surname":"ATLEE",
      "given_name":"JOANNE",
      "position":"Professor",
      "salary_paid":"$169,372.76",
      "taxable_benefits":"$281.04"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AUCOIN",
      "given_name":"MARC",
      "position":"Associate Professor",
      "salary_paid":"$138,650.36",
      "taxable_benefits":"$515.80"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AURINI",
      "given_name":"JANICE",
      "position":"Assistant Professor",
      "salary_paid":"$100,397.80",
      "taxable_benefits":"$388.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"AZIZ",
      "given_name":"HANY",
      "position":"Professor",
      "salary_paid":"$160,313.84",
      "taxable_benefits":"$620.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BACKHOUSE",
      "given_name":"CHRIS",
      "position":"Professor",
      "salary_paid":"$173,223.40",
      "taxable_benefits":"$286.36"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BACON",
      "given_name":"DENISE",
      "position":"Regional Manager, Greater Toronto Area East",
      "salary_paid":"$103,926.12",
      "taxable_benefits":"$402.28"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BADER",
      "given_name":"DIANNE",
      "position":"Director, Operations",
      "salary_paid":"$129,178.04",
      "taxable_benefits":"$214.36"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BAGHERI",
      "given_name":"SAEED SYRUS",
      "position":"Technology Transfer Officer",
      "salary_paid":"$108,684.32",
      "taxable_benefits":"$420.84"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BAIN",
      "given_name":"E.TREVOR",
      "position":"Manager, Infrastructure Communication",
      "salary_paid":"$110,140.92",
      "taxable_benefits":"$426.40"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BAJCSY",
      "given_name":"MICHAL",
      "position":"Assistant Professor",
      "salary_paid":"$125,073.27",
      "taxable_benefits":"$189.52"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BALKA",
      "given_name":"PETER",
      "position":"Lecturer",
      "salary_paid":"$111,370.56",
      "taxable_benefits":"$431.20"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BALOGH",
      "given_name":"MICHAEL M.L.",
      "position":"Associate Professor",
      "salary_paid":"$116,463.52",
      "taxable_benefits":"$491.80"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BAN",
      "given_name":"DAYAN D.",
      "position":"Professor",
      "salary_paid":"$152,101.20",
      "taxable_benefits":"$584.00"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BANDYOPADHYAY",
      "given_name":"SATIPRASAD",
      "position":"Associate Professor",
      "salary_paid":"$164,078.68",
      "taxable_benefits":"$615.88"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BANKINER",
      "given_name":"WILLIAM",
      "position":"Legal Counsel, Research Services",
      "salary_paid":"$121,609.10",
      "taxable_benefits":"$201.06"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BANSAL",
      "given_name":"HARVIR S.",
      "position":"Associate Professor",
      "salary_paid":"$175,704.72",
      "taxable_benefits":"$680.28"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARANOSKI",
      "given_name":"GLADIMIR",
      "position":"Associate Professor",
      "salary_paid":"$160,863.32",
      "taxable_benefits":"$606.64"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARBY",
      "given_name":"JAMES A",
      "position":"Associate Professor",
      "salary_paid":"$177,614.28",
      "taxable_benefits":"$279.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARDELCIK",
      "given_name":"ALEX",
      "position":"Research Associate",
      "salary_paid":"$108,950.04",
      "taxable_benefits":"$350.49"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARDWELL",
      "given_name":"KIM",
      "position":"Director of Advancement, Faculty of Arts",
      "salary_paid":"$116,625.48",
      "taxable_benefits":"$193.44"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARKER",
      "given_name":"ANDREW",
      "position":"Director, Institutional Research",
      "salary_paid":"$126,597.58",
      "taxable_benefits":"$338.08"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARNETT",
      "given_name":"JAMES",
      "position":"Lecturer",
      "salary_paid":"$189,267.24",
      "taxable_benefits":"$297.36"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BARRA",
      "given_name":"MONICA",
      "position":"Associate Professor",
      "salary_paid":"$143,617.12",
      "taxable_benefits":"$238.20"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BASIR",
      "given_name":"OTMAN",
      "position":"Professor",
      "salary_paid":"$143,594.44",
      "taxable_benefits":"$617.28"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BASKERVILLE",
      "given_name":"NEILL BRUCE",
      "position":"Associate Professor",
      "salary_paid":"$139,253.76",
      "taxable_benefits":"$539.08"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BASU",
      "given_name":"DIPANJAN",
      "position":"Assistant Professor",
      "salary_paid":"$120,834.28",
      "taxable_benefits":"$200.60"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BASU",
      "given_name":"NANDITA",
      "position":"Assistant Professor",
      "salary_paid":"$103,701.97",
      "taxable_benefits":"$194.72"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BATTEN",
      "given_name":"ALICIA",
      "position":"Associate Professor, Conrad Grebel University College",
      "salary_paid":"$122,717.96",
      "taxable_benefits":"$225.31"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BATTY",
      "given_name":"CHRISTOPHER",
      "position":"Assistant Professor",
      "salary_paid":"$112,873.32",
      "taxable_benefits":"$187.28"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BAUCH",
      "given_name":"CHRISTOPHER",
      "position":"Professor",
      "salary_paid":"$154,527.04",
      "taxable_benefits":"$243.88"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BAUGH",
      "given_name":"JONATHAN",
      "position":"Associate Professor",
      "salary_paid":"$126,315.63",
      "taxable_benefits":"$178.52"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BEAN",
      "given_name":"DAVID",
      "position":"Associate Director, Systems",
      "salary_paid":"$106,661.91",
      "taxable_benefits":"$171.68"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BEAZELY",
      "given_name":"MICHAEL",
      "position":"Assistant Professor",
      "salary_paid":"$119,954.36",
      "taxable_benefits":"$474.36"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BECKER",
      "given_name":"BYRON WEBER",
      "position":"Lecturer",
      "salary_paid":"$129,784.12",
      "taxable_benefits":"$502.44"
    },
    {
      "employer":"University of Waterloo",
      "surname":"BECKS",
      "given_name":"DARREN",
      "position":"Vice-President, Administration, St. Jerome's University",
      "salary_paid":"$144,265.53",
      "taxable_benefits":"$547.76"
    },
    {
      "employer":"University of Waterloo",
      "surname":"HAMDULLAHPUR",
      "given_name":"FERIDUN",
      "position":"President",
      "salary_paid":"$399,999.96",
      "taxable_benefits":"$3,667.96"
    }
  ]
}
```


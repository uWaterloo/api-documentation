# Employer Info Sessions by Term

```
GET /terms/{term}/infosessions.{format}
```

## Description

> This method returns the schedule for employer information sessions of a given term

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
    <td>1489</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>terms</td>
    <td><b>Service ID</b></td>
    <td>241</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>CECA</td>
    <td><b>Data Type</b></td>
    <td>Scraped</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Weekly</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/tree/master/EmployerInfoSessions


## Parameters

```
GET /terms/{term}/infosessions.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>term</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Four digit term representation</td>
  </tr>
  <tr>
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>The format of the output</td>
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
GET /terms/{term}/infosessions.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.json**
- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.xml**
- **https://api.uwaterloo.ca/v2/terms/1141/infosessions.json?callback=myResponse**


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
    <td>Information session id</td>
  </tr>
  <tr>
    <td><b>employer</b></td>
    <td>string</td>
    <td>Name of employer hosting session</td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>string</td>
    <td>Date of session</td>
  </tr>
  <tr>
    <td><b>start_time</b></td>
    <td>string</td>
    <td>Start time of session</td>
  </tr>
  <tr>
    <td><b>end_time</b></td>
    <td>string</td>
    <td>End time of session</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Location of session</td>
  </tr>
  <tr>
    <td><b>website</b></td>
    <td>string</td>
    <td>Employer's website</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>string</td>
    <td>Target audience of session</td>
  </tr>
  <tr>
    <td><b>programs</b></td>
    <td>string</td>
    <td>Programs of study relevant to employer</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Description of employer</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":480,
    "timestamp":1396735964,
    "status":200,
    "message":"Request successful",
    "method_id":1489,
    "method":{
      
    }
  },
  "data":[
    {
      "id":"2174",
      "employer":"Actv8 Marketing",
      "date":"January 7, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ALL - Business",
      "description":""
    },
    {
      "id":"2247",
      "employer":"Mozilla",
      "date":"January 7, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"careers.mozilla.org\/",
      "audience":"Co-op Students",
      "programs":"ENG - Software, MATH - Information Technology Management, MATH - Computer Science",
      "description":""
    },
    {
      "id":"2255",
      "employer":"Facebook",
      "date":"January 7, 2014",
      "start_time":"2:00 PM",
      "end_time":"4:00 PM",
      "location":"TC 2218",
      "website":"facebook.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2219",
      "employer":"Audatex Canada",
      "date":"January 7, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"MATH - Information Technology Management, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2307",
      "employer":"Amazon",
      "date":"January 7, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH - Festival Room",
      "website":"www.amazon.com\/college",
      "audience":"Co-op Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2248",
      "employer":"Enflick",
      "date":"January 8, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - MATH faculty, ENG - System Design, ENG - Architecture, ALL - ENG faculty, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical",
      "description":""
    },
    {
      "id":"2218",
      "employer":"Facebook",
      "date":"January 8, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"FACEBOOK.COM",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Computer, ENG - Electrical, ENG - Mechatronics, ENG - Software, ENG - System Design",
      "description":""
    },
    {
      "id":"2168",
      "employer":"Deloitte",
      "date":"January 8, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH - Festival Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Math & Business, MATH - Information Technology Management, MATH - Bioinformatics, ALL - MATH faculty, ENG - System Design, ENG - Software, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ALL - ENG faculty,  ALL - Info Tech",
      "description":""
    },
    {
      "id":"2216",
      "employer":"CPP Investment Board",
      "date":"January 9, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"CPPIB.COM",
      "audience":"Co-op Students",
      "programs":"SCI - Science & Business, MATH - Statistics, MATH - Pure Mathematics, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Math & Business, MATH - Financial Analysis & Risk Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Computational Mathematics, MATH - Combinatorics & Optimization, MATH - Business Administration, ALL - MATH faculty, MATH - Actuarial Science, ENG - System Design, ENG - Management, ENG - Computer, CA - Chartered Accounting, ARTS - Financial Management, ARTS - Economics, ARTS - Arts & Business,  ALL - Info Tech,  ALL - Business",
      "description":""
    },
    {
      "id":"2169",
      "employer":"Dropbox",
      "date":"January 9, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC 1302",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ENG - Software, MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2236",
      "employer":"Bloomberg",
      "date":"January 9, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, SCI - Physics, ENG - Mechatronics, ENG - Mechanical, ALL - MATH faculty, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Math & Business, ENG - Management, MATH - Information Technology Management,  ALL - Info Tech, ALL - ENG faculty, ENG - Electrical, MATH - Computer Science, ENG - Computer, MATH - Computational Mathematics, ENG - Civil, ENG - Chemical, MATH - Applied Mathematics",
      "description":""
    },
    {
      "id":"2284",
      "employer":"EY (formerly known as Ernst &Young)",
      "date":"January 10, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"www.ey.com\/ca\/apply",
      "audience":"Co-op Students",
      "programs":"MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Information Technology Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Bioinformatics, ALL - MATH faculty, MATH - Math & Business, ENG - System Design, ENG - Software, ENG - Mechatronics, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ALL - ENG faculty, CA - All,  ALL - Info Tech,  ALL - Business, CA - Chartered Accounting,  ALL - Accounting",
      "description":""
    },
    {
      "id":"2243",
      "employer":"Blue Coat Systems",
      "date":"January 13, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"MATH - Scientific Computation, MATH - Computer Science, ENG - Computer, ENG - Software, ENG - System Design",
      "description":""
    },
    {
      "id":"2292",
      "employer":"Loyalty One",
      "date":"January 13, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"SCH - Laurel Room",
      "website":"",
      "audience":"Co-op Students",
      "programs":"SCI - Science & Business, MATH - Statistics, MATH - Pure Mathematics, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Information Technology Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Business Administration, MATH - Actuarial Science, MATH - Math & Business, ENV - Environment & Resource Studies, ENV - Environment & Business, ENG - Software, ARTS - Accounting & Financial Management, ARTS - Economics, ARTS - Economics,  ALL - Info Tech,  ALL - Business, CA - Chartered Accounting,  ALL - Accounting",
      "description":""
    },
    {
      "id":"2213",
      "employer":"BlackBerry",
      "date":"January 13, 2014",
      "start_time":"4:30 PM",
      "end_time":"6:30 PM",
      "location":"SCH - Festival Room",
      "website":"www.blackberry.com",
      "audience":"Co-op Students",
      "programs":"ALL - SCI faculty, MATH - Math & Business, MATH - Computer Science, ALL - MATH faculty, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Management, ENG - Electrical, ENG - Computer,  ALL - Business",
      "description":"The \\'for sale\\' sign has been taken down and we are here to stay. The BlackBerry student program has been further refined. Each of our opportunities offers meaningful, hands on experience working alongside industry experts.                                                                                                 As students at BlackBerry, you are an important part of our culture and integral in the success of our business.  BlackBerry provides you the opportunity to be amazing! We offer a dynamic work environment where you are encouraged to achieve your highest potential.    Bring your resume and join us on campus at our information session, where you will have a chance to network with BlackBerry professionals and find out more about what we have to offer. Please RSVP if you will be attending this session or cancel the session if you have registered for this and no longer want to attend it."
    },
    {
      "id":"2172",
      "employer":"Palantir Technologies",
      "date":"January 13, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH Festival Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, MATH - Actuarial Science, ENG - Software, ENG - Computer",
      "description":"Some of our favourite comfort food & drinks will be provided. Enter raffle to win a prize!  Please join Palantir Technologies to learn about Raven, Palantir\\'s high-scale geoanalytical platform. Our software engineers will talk through Raven\\'s role in the Typhoon Haiyan relief effort and discuss some of the technical challenges involved in making a map product interactive with millions of geographic features. View a live demo of our data fusion platforms, and learn how you can be a part of our mission. www.palantir.com We are hiring! http:\/\/www.palantir.com\/careers\/OpenPositionLanding"
    },
    {
      "id":"2300",
      "employer":"Microsoft Canada Co.",
      "date":"January 13, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"",
      "audience":"Co-op Students",
      "programs":"MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Financial Analysis & Risk Management, ENV - Environment & Business, ARTS - Political Science, ARTS - Human Resources Management, ALL - ARTS faculty,  ALL - Info Tech,  ALL - Business,  ALL - Accounting",
      "description":""
    },
    {
      "id":"2229",
      "employer":"CIBC Technology",
      "date":"January 14, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ALL - Info Tech",
      "description":""
    },
    {
      "id":"2296",
      "employer":"Suncor Energy",
      "date":"January 14, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1302",
      "website":"www.suncor.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Mechanical, ENG - Electrical, ENG - Civil, ENG - Chemical",
      "description":"You want to learn more about a key industry in Canada - the energy sector - come join us at our Info Session! You\\'ll hear first hand from hiring managers and ex co-ops about the challenging projects, and the well established student program at Suncor\\'s Ontario and Alberta regions.   You will be impressed by our interesting projects, community spirit, and dynamic environment.   See you then!"
    },
    {
      "id":"2266",
      "employer":"Big Viking Games",
      "date":"January 14, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"Bombshelter",
      "website":"www.bigvikinggames.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Computer",
      "description":""
    },
    {
      "id":"2215",
      "employer":"LinkedIn",
      "date":"January 14, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ENG - Computer, MATH - Computer Science, ENG - Software",
      "description":""
    },
    {
      "id":"2295",
      "employer":"Suncor Energy",
      "date":"January 14, 2014",
      "start_time":"5:30 PM",
      "end_time":"7:30 PM",
      "location":"DC 1302",
      "website":"www.suncor.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - Business",
      "description":"You want to learn more about a key industry in Canada - the energy sector - come join us at our Info Session! You\\'ll hear first hand from hiring managers and ex co-ops about the challenging projects, and the well established student program at Suncor\\'s Ontario and Alberta regions.   You will be impressed by our interesting projects, community spirit, and dynamic environment.   See you then!"
    },
    {
      "id":"2223",
      "employer":"VMware",
      "date":"January 14, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2176",
      "employer":"Bazaarvoice",
      "date":"January 15, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"bazaarvoice.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Electrical, MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2359",
      "employer":"Actv8 Marketing",
      "date":"January 15, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"www.actv8.com",
      "audience":"Co-op Students",
      "programs":"ALL - Business",
      "description":""
    },
    {
      "id":"2166",
      "employer":"Microsoft",
      "date":"January 15, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH- Festival Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, MATH - Pure Mathematics, ENG - Mechatronics, ENG - Mechanical, ALL - MATH faculty, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Bioinformatics, MATH - Math & Business, ENG - Management,  ALL - Info Tech, ENG - Geological, ENG - Environmental, ALL - ENG faculty, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical",
      "description":""
    },
    {
      "id":"2354",
      "employer":"Muskoka Roastery Coffee Co",
      "date":"January 16, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"www.muskokaroastery.com",
      "audience":"Co-op Students",
      "programs":"SCI - Science & Business, MATH - Math & Business, ENV - Environment & Business, ARTS - Arts & Business, AHS - Recreation & Leisure Studies, AHS - Recreation & Business Management,  ALL - Business",
      "description":"The Muskoka Roastery Coffee Co. is located in Huntsville, Ontario. Our mission is to handcraft the best coffee, and celebrate and protect the natural splendour of Muskoka.  Our Brand Activation Specialists will be conducting, demonstrations and events at grocery stores, cafes and around the community to raise awareness of the brand, stimulate trial and build relationships with customers and consumers."
    },
    {
      "id":"2285",
      "employer":"DBRS Global Technology",
      "date":"January 16, 2014",
      "start_time":"2:00 PM",
      "end_time":"4:00 PM",
      "location":"DC 1302",
      "website":"www.dbrs.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Teaching, MATH - Statistics for Health, MATH - Statistics, MATH - Scientific Computation, MATH - Pure Mathematics, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Information Technology Management, MATH - Financial Analysis & Risk Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Computational Mathematics, MATH - Combinatorics & Optimization, MATH - Business Administration, MATH - Bioinformatics, MATH - Applied Mathematics, MATH - Actuarial Science, ALL - MATH faculty, MATH - Math & Business, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty,  ALL - Info Tech",
      "description":"Like solving engineering and product challenges? Does the idea of working in a lean, start-up oriented team within the finance space sound interesting? Do you like pushing yourself on full-stack bleeding edge technology? Join DBRS Global Technology at our info session to find out more! www.facebook.com\/DBRSGlobalTechnology"
    },
    {
      "id":"2165",
      "employer":"Twitter",
      "date":"January 16, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"QNC - Seminar Room (0101)",
      "website":"twitter.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2167",
      "employer":"Google",
      "date":"January 16, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SCH - Festival Room",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Electrical, MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2245",
      "employer":"FreshBooks - **CANCELLED**",
      "date":"January 17, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1301",
      "website":"freshbooks.com\/jobs\/",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty",
      "description":""
    },
    {
      "id":"2302",
      "employer":"Pulse Energy",
      "date":"January 17, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1304",
      "website":"www.pulseenergy.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Statistics, MATH - Mathematical Economics, MATH - Computer Science, MATH - Applied Mathematics, ARTS - Digital Arts Communication,  ALL - Info Tech",
      "description":""
    },
    {
      "id":"2254",
      "employer":"CGI",
      "date":"January 20, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"www.cgi.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - Business, ALL - ENG faculty, ARTS - Financial Management,  ALL - Info Tech, ALL - MATH faculty",
      "description":""
    },
    {
      "id":"2298",
      "employer":"Fairfax Financial Holdings Ltd",
      "date":"January 20, 2014",
      "start_time":"3:30 PM",
      "end_time":"5:00 PM",
      "location":"TC 2218",
      "website":"co-op.fairfax.ca",
      "audience":"Co-op Students",
      "programs":"MATH - Teaching, MATH - Statistics for Health, MATH - Statistics, MATH - Scientific Computation, MATH - Pure Mathematics, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Math & Business, MATH - Information Technology Management, MATH - Financial Analysis & Risk Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Computational Mathematics, MATH - Combinatorics & Optimization, MATH - Business Administration, MATH - Bioinformatics, MATH - Applied Mathematics, ALL - MATH faculty, MATH - Actuarial Science, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty, ARTS - Political Science, ARTS - Accounting & Financial Management, ARTS - Human Resources Management, ARTS - Financial Management, ARTS - Economics, ARTS - Arts & Business, ALL - ARTS faculty,  ALL - Business",
      "description":""
    },
    {
      "id":"2222",
      "employer":"KIK Interactive",
      "date":"January 20, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"Bombshelter",
      "website":"",
      "audience":"Co-op Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2312",
      "employer":"GE Canada",
      "date":"January 20, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ENG - Software, ENG - Mechanical, ENG - Electrical, ENG - Computer, ENG - Chemical, CA - All,  ALL - Info Tech,  ALL - Business",
      "description":"Your Future Works  www.campuscareers.ge.ca"
    },
    {
      "id":"2257",
      "employer":"Facebook",
      "date":"January 21, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ENG - Electrical, ENG - Computer, MATH - Computer Science, ALL - MATH faculty",
      "description":""
    },
    {
      "id":"2372",
      "employer":"Maple Reinders Constructors",
      "date":"January 21, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC - 1302",
      "website":"www.maple.ca",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Mechanical, ENG - Environmental, ENG - Civil",
      "description":""
    },
    {
      "id":"2339",
      "employer":"Plex Systems",
      "date":"January 21, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"DC 1301",
      "website":"www.plex.com",
      "audience":"Co-op Students",
      "programs":"MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2177",
      "employer":"Electronic Arts",
      "date":"January 21, 2014",
      "start_time":"5:30 PM",
      "end_time":"7:30 PM",
      "location":"TC 2218",
      "website":"careers.ea.com\/students",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty, MATH - Computer Science, MATH - Applied Mathematics, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2214",
      "employer":"Zynga",
      "date":"January 21, 2014",
      "start_time":"8:00 PM",
      "end_time":"9:30 PM",
      "location":"TC 2218",
      "website":"www.ZYNGA.COM\/STUDENTS",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Management, MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2171",
      "employer":"Desire2Learn",
      "date":"January 22, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Computer, MATH - Computer Science, ENG - Electrical, ENG - Software, ENG - System Design",
      "description":"Desire2Learn is helping to transform the way the world learns! We are in a period of rapid expansion and require the best of the best to help us design and deliver on our upcoming products. If you are looking for a chance to truly have an impact on a learning system used by over 10 million people worldwide (including University of Waterloo), visit our Networking Session to find out where you fit into our growth!"
    },
    {
      "id":"2291",
      "employer":"OANDA",
      "date":"January 22, 2014",
      "start_time":"3:00 PM",
      "end_time":"5:00 PM",
      "location":"TC 2218",
      "website":"jobs.oanda.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Computer,  ALL - Info Tech",
      "description":""
    },
    {
      "id":"2161",
      "employer":"McRae Integration",
      "date":"January 22, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC 1301",
      "website":"www.mcreaintegration.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Computer, ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical",
      "description":""
    },
    {
      "id":"2225",
      "employer":"Nurun Inc.",
      "date":"January 22, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"www.nurun.com\/en\/",
      "audience":"Graduating Students",
      "programs":"MATH - Information Technology Management, MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer",
      "description":"Nurun is a global design and technology consultancy that works with some of the world\\'s most innovative companies. We create products and services for the connected world through a combination of human insight, new technology, and smart thinking. Clients include Adidas, BBVA, Bouygues Telecom, Coca-Cola, Electronic Arts, General Electric, Google, The Home Depot, Tesla Motors, Sony, and Wal-Mart.   Specialties Design Research, Transactional Platforms, Digital Products, User Interfaces, Service Design, Post-PC Ecosystems"
    },
    {
      "id":"2212",
      "employer":"Southeast University",
      "date":"January 23, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Geological, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty",
      "description":""
    },
    {
      "id":"2350",
      "employer":"Audible.com, An Amazon Company",
      "date":"January 23, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"DC - 1301",
      "website":"www.audible.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Information Technology Management, MATH - Computer Science, ENG - Software, ENG - Computer,  ALL - Info Tech",
      "description":""
    },
    {
      "id":"2360",
      "employer":"Uken Games",
      "date":"January 23, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC - 1301",
      "website":"www.uken.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":"Itching to Start a Company?"
    },
    {
      "id":"2249",
      "employer":"A Thinking Ape",
      "date":"January 23, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"athinkingape.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":"Build Stuff NowPizza, swag & drinks will be provided"
    },
    {
      "id":"2384",
      "employer":"Thalmic Labs",
      "date":"January 27, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1301",
      "website":"www.thalmic.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Mechanical, ENG - Electrical, ENG - Computer, ENG - Software, ENG - Mechatronics, MATH - Computer Science, ENG - System Design",
      "description":""
    },
    {
      "id":"2299",
      "employer":"SMART Technologies",
      "date":"January 27, 2014",
      "start_time":"3:30 PM",
      "end_time":"5:00 PM",
      "location":"DC 1301",
      "website":"www.smartech.com",
      "audience":"Co-op Students",
      "programs":"ENG - Computer, ENG - Electrical, ENG - Software, ENG - System Design, MATH - Computer Science",
      "description":""
    },
    {
      "id":"2224",
      "employer":"Khan Academy",
      "date":"January 27, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ALL - MATH faculty, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Environmental, ENG - Electrical, ENG - Computer, ENG - Civil, ENG - Chemical, ENG - Architecture, ALL - ENG faculty,  ALL - Info Tech",
      "description":"Khan Academy at Waterloo on Hacking School at Scale: Dylan Vassallo, a software developer at Khan Academy, will talk about the challenges and benefits of developing an educational website that scales to millions of learners every day."
    },
    {
      "id":"2220",
      "employer":"Yelp",
      "date":"January 27, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1302",
      "website":"www.yelp.com\/careers",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2268",
      "employer":"Magnet Forensics",
      "date":"January 28, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1304",
      "website":"www.magnetforensics.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Management, ENG - Computer",
      "description":""
    },
    {
      "id":"2226",
      "employer":"Yext",
      "date":"January 28, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"www.yext.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software",
      "description":""
    },
    {
      "id":"2282",
      "employer":"Arista Networks",
      "date":"January 29, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1301",
      "website":"www.aristanetworks.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Mechanical, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2309",
      "employer":"Motorola Mobility",
      "date":"January 29, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"DC 1301",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2227",
      "employer":"ThoughtWorks **CANCELLED**",
      "date":"January 29, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC 1301",
      "website":"www.thoughtworks.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software",
      "description":""
    },
    {
      "id":"2313",
      "employer":"XL Group plc",
      "date":"January 29, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"SCH - Laurel Room",
      "website":"www.xlgroup.com\/",
      "audience":"Co-op Students",
      "programs":"MATH - Financial Analysis & Risk Management, MATH - Business Administration, MATH - Actuarial Science, ARTS - Financial Management",
      "description":""
    },
    {
      "id":"2305",
      "employer":"Newton North America",
      "date":"January 29, 2014",
      "start_time":"5:30 PM",
      "end_time":"7:00 PM",
      "location":"DC 1302",
      "website":"www.newton-na.com",
      "audience":"Graduating Students",
      "programs":"ENG - Nanotechnology, ENG - Mechatronics, ENG - Mechanical, ENG - Management, ENG - Electrical",
      "description":""
    },
    {
      "id":"2333",
      "employer":"Noom",
      "date":"January 29, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"noom.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ALL - MATH faculty, ENG - System Design, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2290",
      "employer":"EY (formerly known as Ernst &Young)",
      "date":"January 30, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"CA - All,  ALL - Accounting",
      "description":"EY is a global professional services organization providing advisory, assurance, tax and transaction services. We are committed to doing our part in building a better working world for our people, our clients and our communities. And we are united by our shared values and a dedication to delivering exceptional client service.  We would like to invite you to come out and learn about our firm and our student programs. Our campus recruiting team will be on site to provide information on our upcoming Global Perspectives Series (GPS) and Emerging Leaders Program (ELP). These programs are happening in the next few month and we would love for you to get involved!  This event is aimed at first year students looking to pursue a CA\/CPA designation.  Dress Code - Casual"
    },
    {
      "id":"2301",
      "employer":"Maplesoft",
      "date":"January 30, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1301",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Statistics for Health, MATH - Statistics, MATH - Scientific Computation, MATH - Pure Mathematics, MATH - Mathematical Studies, MATH - Mathematical Physics, MATH - Mathematical Optimization, MATH - Mathematical Finance, MATH - Mathematical Economics, MATH - Information Technology Management, MATH - Financial Analysis & Risk Management, MATH - Computing & Financial Management, MATH - Computer Science, MATH - Computational Mathematics, MATH - Combinatorics & Optimization, MATH - Business Administration, MATH - Bioinformatics, MATH - Applied Mathematics, MATH - Actuarial Science, ALL - MATH faculty, MATH - Math & Business",
      "description":""
    },
    {
      "id":"2325",
      "employer":"Facebook",
      "date":"January 30, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"DC - 1301",
      "website":"",
      "audience":"Co-op Students",
      "programs":"ALL - MATH faculty, ENG - System Design, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2217",
      "employer":"Cisco SF",
      "date":"January 30, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC 1301",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Software, ALL - MATH faculty, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2280",
      "employer":"A9, Subsidiary of Amazon",
      "date":"January 30, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op Students",
      "programs":"MATH - Statistics, MATH - Computer Science, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2228",
      "employer":"Counsyl",
      "date":"January 31, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"Laurel Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2321",
      "employer":"Cigna Corporation",
      "date":"February 3, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC- 1301",
      "website":"www.cigna.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Financial Analysis & Risk Management, MATH - Business Administration, ALL - MATH faculty, MATH - Actuarial Science, MASTERS - Actuarial Science",
      "description":""
    },
    {
      "id":"2367",
      "employer":"PDT Partners, LLC **CANCELLED**",
      "date":"February 3, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"TC 2218",
      "website":"www.pdtpartners.com",
      "audience":"Co-op Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Mechatronics, ENG - Computer",
      "description":""
    },
    {
      "id":"2259",
      "employer":"IBM Canada Ltd, Enterprise Wide Technology",
      "date":"February 3, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"www.ibm.com\/start",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Math & Business, MATH - Information Technology Management, MATH - Computing & Financial Management, MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Nanotechnology, ENG - Mechatronics, ENG - Management, ENG - Electrical, ENG - Computer",
      "description":"What to expect? Evening of learning, networking, refreshments & mingling.  Learn about the amazing opportunities and variety of roles IBM has to offer to both students and new grads. Hear about Watson, new directions and new initiatives from a long standing technology company!"
    },
    {
      "id":"2314",
      "employer":"Cisco",
      "date":"February 4, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"",
      "audience":"Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2315",
      "employer":"National Instruments",
      "date":"February 4, 2014",
      "start_time":"2:30 PM",
      "end_time":"4:30 PM",
      "location":"SCH - Laurel Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"SCI - Physics, ENG - Electrical, ENG - Computer, ALL - ENG faculty",
      "description":""
    },
    {
      "id":"2253",
      "employer":"Nulogy",
      "date":"February 4, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC 1301",
      "website":"nulogy.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer,  ALL - Info Tech",
      "description":""
    },
    {
      "id":"2237",
      "employer":"TripAdvisor",
      "date":"February 4, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - MATH faculty, MATH - Mathematical Studies, MATH - Mathematical Optimization, MATH - Mathematical Finance, ENG - Software, MATH - Pure Mathematics, MATH - Mathematical Economics, ENG - Electrical, MATH - Computer Science, ENG - Computer, MATH - Applied Mathematics",
      "description":""
    },
    {
      "id":"2393",
      "employer":"Lookout Mobile Security",
      "date":"February 5, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"www.lookout.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Computer",
      "description":""
    },
    {
      "id":"2246",
      "employer":"Apple",
      "date":"February 5, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"SLC - Multipupose Room",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Mechanical, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2323",
      "employer":"SCOR Global Life Americas",
      "date":"February 6, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC - 1301",
      "website":"www.scor.com",
      "audience":"Co-op Students",
      "programs":"MATH - Mathematical Finance, MATH - Financial Analysis & Risk Management, MATH - Applied Mathematics, MATH - Actuarial Science, MASTERS - Actuarial Science",
      "description":""
    },
    {
      "id":"2394",
      "employer":"Canadian Security Intelligence Service",
      "date":"February 6, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1302",
      "website":"www.csiscareers.ca",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - ENG faculty, CA - Chartered Accounting, ARTS - Political Science, ARTS - Human Resources Management, ARTS - Arts & Business",
      "description":""
    },
    {
      "id":"2297",
      "employer":"Pinterest",
      "date":"February 6, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"www.pinterest.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software",
      "description":""
    },
    {
      "id":"2327",
      "employer":"Ultimate Software",
      "date":"February 6, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"www.ultimatesoftwa",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, MATH - Computational Mathematics, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2326",
      "employer":"WSP Group",
      "date":"February 7, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"www.wspgroup.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - ENG faculty",
      "description":""
    },
    {
      "id":"2310",
      "employer":"Lime Connect",
      "date":"February 10, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - All",
      "description":"Learn about Lime Connect and their programs for students who happen to have a disability as well as Whether, When and How to discuss disability in an employment situation. Location: Tatham Centre 2240"
    },
    {
      "id":"2322",
      "employer":"ContextLogic Inc",
      "date":"February 10, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"www.wish.com\/company",
      "audience":"Co-op Students",
      "programs":"MATH - Computing & Financial Management, MATH - Computer Science, ENG - Software",
      "description":""
    },
    {
      "id":"2320",
      "employer":"Tata Consultancy Services Canada Inc.",
      "date":"February 11, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"www.tcs.com",
      "audience":"Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Mechatronics, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2351",
      "employer":"Broadcom Corporation",
      "date":"February 11, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC - 1301",
      "website":"www.broadcom.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - System Design, ENG - Software, ENG - Mechatronics, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2368",
      "employer":"Information Technology Industry Panel",
      "date":"February 11, 2014",
      "start_time":"5:30 PM",
      "end_time":"7:30 PM",
      "location":"TC 2218",
      "website":"",
      "audience":"Students",
      "programs":"MATH - Math & Business, MATH - Information Technology Management, MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Management, ENG - Electrical, ENG - Computer,  ALL - Info Tech,  ALL - Business",
      "description":"What is the IT world like outside the Silicon Valley? Please sign up soon as space is limited."
    },
    {
      "id":"2406",
      "employer":"Microsoft Canada",
      "date":"February 12, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1301",
      "website":"www.microsoft.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Information Technology Management, MATH - Computer Science, ALL - ENG faculty",
      "description":"You may have heard about Windows Azure (you know Microsoft\\'s cloud offering) but wrote it off because you don\\'t do .NET or even use Windows. Well in this lunch and learn you\\'ll see how wrong you are. Windows Azure has support for Node.js, php, python, Linux VMs and more. You\\'ll be shown quick and practical demos on using git to deploy your sites, how to setup a Linux VMs with SSH key authentication and more. You\\'ll also learn about BizSpark, a program from Microsoft for all tech startups that includes free software, $150 a month for 3 years in hosting and even a one-time $5,000 a month for a year offer for select startups. Oh and there will be pizza too!"
    },
    {
      "id":"2306",
      "employer":"Genesys Telecommunications Laboratories Inc.",
      "date":"February 12, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"DC 1301",
      "website":"",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Computer",
      "description":"Join Genesys and save the world from bad customer service! Genesys is the world\\'s leading provider of customer service and contact software - with more than 2,000 customers in 80 countries. On February 12th, from 5-7pm in the Davis Center Fishbowl, we invite co-op students of all levels to come out to this information session where you will have the opportunity to ask current and past co-ops as well as employers and current engineers about the different positions that are available. Please RSVP soon; pizza and drinks will be provided and swag will be given out."
    },
    {
      "id":"2331",
      "employer":"Rl Solutions",
      "date":"February 12, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"www.rlsolutions.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - ARTS faculty, ALL - SCI faculty, ALL - MATH faculty, ALL - ENV faculty, ALL - ENG faculty",
      "description":"RL Solutions is a healthcare software company where good people are doing great things. We invite co-op students and new graduates to join us to see what it is like to be a part of the RL team. You\\'ll have the opportunity to hear from and speak with previous and current co-op students as well as other full-time staff. Plus, we have some amazing giveaways and tasty snacks. We hope you can join us!"
    },
    {
      "id":"2374",
      "employer":"Nascent",
      "date":"February 13, 2014",
      "start_time":"12:30 PM",
      "end_time":"2:30 PM",
      "location":"SCH - Laurel Room",
      "website":"www.nascentdigital.com",
      "audience":"Co-op Students",
      "programs":"MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2232",
      "employer":"Infusion",
      "date":"February 13, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"www.infusion.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Computer",
      "description":""
    },
    {
      "id":"2398",
      "employer":"ModiFace",
      "date":"February 14, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC - 1301",
      "website":"modiface.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Electrical, ENG - Computer",
      "description":""
    },
    {
      "id":"2414",
      "employer":"The Jonah Group **CANCELLED**",
      "date":"February 25, 2014",
      "start_time":"5:30 PM",
      "end_time":"7:00 PM",
      "location":"DC 1301",
      "website":"www.jonahgroup.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer",
      "description":"Come find out what life is like at the Jonah Group. You\\'ll have a chance to learn more about our business, work culture, what makes us unique (aka the people) and the life of a developer at Jonah. Here\\'s a chance to schmooze with us and see if we are a good fit for you. Drinks and pizza will be provided."
    },
    {
      "id":"2389",
      "employer":"Architech",
      "date":"February 26, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"www.architech.ca",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ENG - Software, ENG - Computer",
      "description":"Perks of working at Architech:  Check us out at architech.ca, and discover more about how we bring great ideas to life, faster."
    },
    {
      "id":"2387",
      "employer":"Grip Limited",
      "date":"February 27, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1301",
      "website":"www.griplimited.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Math & Business, MATH - Computer Science, MATH - Business Administration, ENG - Computer",
      "description":""
    },
    {
      "id":"2402",
      "employer":"CH2M Hill Ltd.",
      "date":"February 27, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"SCH - Laurel Room",
      "website":"www.ch2mhill.com",
      "audience":"Co-op and Graduating Students",
      "programs":"ENG - Mechanical, ENG - Environmental, ENG - Civil, ENG - Chemical",
      "description":"CH2M HILL is looking forward to seeing you at our info session event. This is an opportunity for you to learn more about CH2M HILL and the exciting career opportunities we have to offer; including fulltime, internship and co-op positions. Stop by and meet our CH2M HILL representatives!"
    },
    {
      "id":"2412",
      "employer":"Yahoo",
      "date":"March 4, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"DC 1302",
      "website":"www.careers.yahoo.com",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Information Technology Management, MATH - Computer Science, ENG - System Design, ENG - Software, ENG - Computer",
      "description":"Yahoo: Insane Scalability. At Yahoo we deal with tons of traffic and data. We need to move fast, with quality. At this talk we will cover Yahoo Advertising and Data Platforms - our architecture and how we address various problems that arise with high traffic and data volume. You will have the opportunity to talk to engineers and recruiters about internships and full-time opportunities. Bring a resume! Lunch provided."
    },
    {
      "id":"2376",
      "employer":"Deloitte",
      "date":"March 4, 2014",
      "start_time":"4:30 PM",
      "end_time":"6:30 PM",
      "location":"SCH - Festival Room",
      "website":"",
      "audience":"Co-op Students",
      "programs":"CA - Chartered Accounting",
      "description":""
    },
    {
      "id":"2288",
      "employer":"Toyota",
      "date":"March 6, 2014",
      "start_time":"4:00 PM",
      "end_time":"8:00 PM",
      "location":"Sedra Student Design Centre, E5-1001",
      "website":"www.tmmc.ca",
      "audience":"Co-op and Graduating Students",
      "programs":"ALL - SCI faculty, ALL - MATH faculty, ALL - ENV faculty, ALL - ENG faculty, ALL - ARTS faculty, ALL - AHS faculty",
      "description":"To all UWaterloo Co-op and Graduating students, come and join us in an informal networking session and get to know some team members from Toyota Motor Manufacturing Inc. (TMMC): We will have a number of former UW Co-op students and recruitment team members, to meet with you and chat about TMMC Co-op work terms and the opportunities that await you upon graduation."
    },
    {
      "id":"2408",
      "employer":"Rogers Ventures **CANCELLED**",
      "date":"March 11, 2014",
      "start_time":"4:00 PM",
      "end_time":"5:00 PM",
      "location":"SCH - Laurel Room",
      "website":"www.vicinityrewards.ca",
      "audience":"Co-op and Graduating Students",
      "programs":"CA - Chartered Accounting, CA - Accounting, ARTS - Accounting & Financial Management, ARTS - Arts & Business",
      "description":""
    },
    {
      "id":"2390",
      "employer":"TransCanada",
      "date":"March 13, 2014",
      "start_time":"5:30 PM",
      "end_time":"7:30 PM",
      "location":"Engineering 5 - Room 3102 (LiveLink)",
      "website":"http:\/\/transcanada.com\/",
      "audience":"Co-op Students",
      "programs":"ALL - ENG faculty",
      "description":""
    },
    {
      "id":"2435",
      "employer":"Centerline (Windsor) Limited",
      "date":"March 21, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"www.cntrline.com",
      "audience":"Graduating Students",
      "programs":"ENG - Mechatronics, ENG - Mechanical, ENG - Electrical",
      "description":"Attention Engineering students (Mechanical, Weld, Electrical) and Materials Science students - come and join Centerline (Windsor) Limited for an information and networking session. You will have the opportunity to learn about our company and talk about coop work terms and full time careers that are available. Pizza and refreshments will be served."
    },
    {
      "id":"2422",
      "employer":"PwC",
      "date":"March 24, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"TC 2218",
      "website":"www.pwc.com",
      "audience":"Co-op Students",
      "programs":"CA - Chartered Accounting, CA - Accounting, ARTS - Financial Management",
      "description":"The opportunity of a lifetime. Your career is just that, yours. You choose it. You live it. You make it happen. To get the best from it, you need the best opportunities. That\\'s why opportunities are at the heart of PwC careers. Opportunities to grow as an individual, to work flexibly, to build lasting relationships and make an impact in a place where people, quality and value mean everything. If you\\'re in your first or second year of an undergraduate business program looking to specialize in accounting, then this is your opportunity of a lifetime. Apply now to experience PwC\\'s Talent Academy held June 16-18, 2014. We guarantee that this event will help you shine during fall CPA recruiting. This is an opportunity to connect with our people from our CEO and leadership partners, to our staff from offices across Canada during our networking events and fun activities. Sharpen your leadership, teamwork and communication skills via experiential learning activities, interactive workshops and team-based challenges."
    },
    {
      "id":"2413",
      "employer":"KPMG LLP",
      "date":"March 25, 2014",
      "start_time":"5:00 PM",
      "end_time":"7:00 PM",
      "location":"SCH - Festival Room",
      "website":"",
      "audience":"Co-op Students",
      "programs":"CA - Chartered Accounting, CA - Accounting, ARTS - Financial Management",
      "description":"Executive Look is an exclusive event hosted at our downtown Toronto office that connects today\\'s best and brightest student leaders to members of KPMG\\'s executive management teams. It is available to top students nationally; and if selected, you will be introduced to our functions, the programs we offer, KPMG executives and you will get the opportunity to participate in interactive workshops, team activities and roundtable discussions. By participating in Executive Look you can cultivate relationships with top students from across Canada and with KPMG professionals. By immersing yourself in the event you will get an inside look at what a career with KPMG may hold, and find that it\\'s a great place for you to discover your potential."
    },
    {
      "id":"2425",
      "employer":"CIBC Technology",
      "date":"March 25, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"DC 1301",
      "website":"www.cibc.com\/careers",
      "audience":"Graduating Students",
      "programs":"ALL - MATH faculty, ALL - ENG faculty",
      "description":"Attention Math and Engineering graduating students - come and meet CIBC\\'s Distribution Technology & Channel Strategy team and learn about our Mobile Developer new graduate opportunities!"
    },
    {
      "id":"2437",
      "employer":"RDA Insurance",
      "date":"March 26, 2014",
      "start_time":"11:30 AM",
      "end_time":"1:30 PM",
      "location":"TC 2218",
      "website":"www.rdainsurance.com",
      "audience":"Graduating Students",
      "programs":"SCI - Science & Business, MATH - Mathematical Economics, MATH - Business Administration, ARTS - Arts & Business, ALL - ARTS faculty",
      "description":""
    },
    {
      "id":"2438",
      "employer":"Maluuba",
      "date":"March 27, 2014",
      "start_time":"7:30 PM",
      "end_time":"9:00 PM",
      "location":"TC 2218",
      "website":"http:\/\/www.maluuba.com\/",
      "audience":"Co-op and Graduating Students",
      "programs":"MATH - Computer Science, ALL - MATH faculty, ENG - System Design, ENG - Software, ALL - ENG faculty",
      "description":"At Maluuba, we\\'re developing revolutionary search technology at the forefront of the Natural Language Processing (NLP) movement used by millions of people around the world. We solve new problems every day in a fun, fast-paced environment. The atmosphere is friendly and lighthearted while remaining productive. If you look around our office, you\\'ll see lots of food and drinks alongside a huge variety of the latest gadgets and devices. When we\\'re not heads-down and hard at work, our employees often play ping-pong or foosball in the office. We even have weekly Maluuba soccer games and movie nights.  As a Software Engineer, you will directly impact our core products and services and will be working in either (i) Labs\/Mobile, (ii) Platform, (iii) NLP, or (iv) Machine Learning, depending on your background and experience. Come join us and help invent the future!"
    }
  ]
}
```


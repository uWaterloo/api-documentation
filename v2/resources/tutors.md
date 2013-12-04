# List of student tutors available

```
GET /v2/resources/tutors.{format}
```

## Description

> This method returns a list of all the tutors available to help for a course for a given term

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
    <td>1481</td>
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
    <td>SSO</td>
    <td><b>Data Type</b></td>
    <td>Direct feed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>As the data updates by SSO</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- Any value can be `null`


### Sources



## Parameters

```
GET /v2/resources/tutors.{format}
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
GET /v2/resources/tutors.{format}
```

- **https://api.uwaterloo.ca/v2/resources/tutors.json**
- **https://api.uwaterloo.ca/v2/resources/tutors.xml**
- **https://api.uwaterloo.ca/v2/resources/tutors.json?callback=myResponse**


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
    <td>Subject acronym</td>
  </tr>
  <tr>
    <td><b>catalog_number</b></td>
    <td>string</td>
    <td>Course catalog number</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Course title</td>
  </tr>
  <tr>
    <td><b>tutors_count</b></td>
    <td>integer</td>
    <td>Total number of tutors available for that course</td>
  </tr>
  <tr>
    <td><b>contact_url</b></td>
    <td>string</td>
    <td>Link to get tutor contact details</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":477,
    "timestamp":1386184862,
    "status":200,
    "message":"Request successful",
    "method_id":1481,
    "method":{
      
    }
  },
  "data":[
    {
      "subject":"ACTSC",
      "catalog_number":"463",
      "title":"Introduction to Property and Casualty Loss Reserving",
      "tutors_count":1,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1861"
    },
    {
      "subject":"AFM",
      "catalog_number":"101",
      "title":"Introduction to Financial Accounting",
      "tutors_count":9,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1863"
    },
    {
      "subject":"AFM",
      "catalog_number":"123",
      "title":"Accounting Information for Managers",
      "tutors_count":1,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1864"
    },
    {
      "subject":"AFM",
      "catalog_number":"131",
      "title":"Introduction to Business in North America",
      "tutors_count":6,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1865"
    },
    {
      "subject":"AFM",
      "catalog_number":"273",
      "title":"Managerial Finance 1",
      "tutors_count":1,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1869"
    },
    {
      "subject":"AFM",
      "catalog_number":"291",
      "title":"Intermediate Financial Accounting 1",
      "tutors_count":1,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1871"
    },
    {
      "subject":"AMATH",
      "catalog_number":"231",
      "title":"Calculus 4",
      "tutors_count":3,
      "contact_url":"https:\/\/uwaterloo.ca\/student-success\/tutoring\/search-tutor-result?field_profile_courses_target_id%5B%5D=1891"
    }
  ]
}
```


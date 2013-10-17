# Code Lookups for Groups

```
GET /codes/groups.{format}
```

## Description

> This method returns a list of all code lookups for groups.

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
    <td>1229</td>
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
- In Quest, there are units and groups. Units are inside groups. A unit is like a department and a group is like a faculty. Reason: not all units and departments and not all groups are faculties.
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/Quest/AcademicGroups.csv


## Parameters

```
GET /codes/groups.{format}
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
GET /codes/groups.{format}
```

- **https://api.uwaterloo.ca/v2/codes/groups.json**
- **https://api.uwaterloo.ca/v2/codes/groups.xml**
- **https://api.uwaterloo.ca/v2/codes/groups.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>group_code</b></td>
    <td>string</td>
    <td>Group Code</td>
  </tr>
  <tr>
    <td><b>group_short_name</b></td>
    <td>string</td>
    <td>Group Short Name</td>
  </tr>
  <tr>
    <td><b>group_full_name</b></td>
    <td>string</td>
    <td>Full group name</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":145,
    "timestamp":1382023751,
    "status":200,
    "message":"Request successful",
    "method_id":1229,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "group_code":"AHS",
      "group_short_name":"Applied Health Sciences",
      "group_full_name":"Faculty of Applied Health Sciences"
    },
    {
      "group_code":"ART",
      "group_short_name":"Arts",
      "group_full_name":"Faculty of Arts"
    },
    {
      "group_code":"CGC",
      "group_short_name":"Conrad Grebel",
      "group_full_name":"Conrad Grebel University College"
    },
    {
      "group_code":"ENG",
      "group_short_name":"Engineering",
      "group_full_name":"Faculty of Engineering"
    },
    {
      "group_code":"ENV",
      "group_short_name":"Environment",
      "group_full_name":"Faculty of Environment"
    },
    {
      "group_code":"GRAD",
      "group_short_name":"Graduate Studies",
      "group_full_name":"Graduate Studies"
    },
    {
      "group_code":"IS",
      "group_short_name":"Independent Studies",
      "group_full_name":"Independent Studies"
    },
    {
      "group_code":"MAT",
      "group_short_name":"Mathematics",
      "group_full_name":"Faculty of Mathematics"
    },
    {
      "group_code":"REN",
      "group_short_name":"Renison",
      "group_full_name":"Renison University College"
    },
    {
      "group_code":"SCI",
      "group_short_name":"Science",
      "group_full_name":"Faculty of Science"
    },
    {
      "group_code":"STJ",
      "group_short_name":"St. Jeromes",
      "group_full_name":"St. Jerome's University"
    },
    {
      "group_code":"STP",
      "group_short_name":"St. Pauls",
      "group_full_name":"St. Paul's University College"
    },
    {
      "group_code":"THL",
      "group_short_name":"Theology",
      "group_full_name":"Theology"
    },
    {
      "group_code":"VPA",
      "group_short_name":"Interdisciplinary",
      "group_full_name":"Interdisciplinary Studies"
    }
  ]
}
```


# API Changelog

```
GET /api/changelog.{format}
```

## Description

> This method returns list of changes made to the API

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
    <td>No</td>
  </tr>
  <tr>
    <td><b>Method ID</b></td>
    <td>1117</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>api</td>
    <td><b>Service ID</b></td>
    <td>223</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>UW OpenData</td>
    <td><b>Data Type</b></td>
    <td>Direct DB Connection</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every request (live)</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Calling this method does not affect usage
- Any value can be `null`


### Sources

- https://api.uwaterloo.ca


## Parameters

```
GET /api/changelog.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>The format of the output</td>
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
GET /api/changelog.{format}
```

- **https://api.uwaterloo.ca/v2/api/changelog.json**
- **https://api.uwaterloo.ca/v2/api/channgelog.xml**
- **https://api.uwaterloo.ca/v2/api/changelog.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>string</td>
    <td>Y-m-d date of published changes</td>
  </tr>
  <tr>
    <td><b>changes</b></td>
    <td>list</td>
    <td>List of published changes</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":86,
    "timestamp":1381935097,
    "status":200,
    "message":"Request successful",
    "method_id":1117,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "date":"2013-10-14",
      "changes":[
        "Published schedule endpoint",
        "Published courses endpoint",
        "Published course from buildings endpoint"
      ]
    },
    {
      "date":"2013-06-13",
      "changes":[
        "Added ability to ban api keys",
        "Added error code 403 for banned api keys",
        "Updated exam schedule"
      ]
    },
    {
      "date":"2013-06-05",
      "changes":[
        "JSON output pretty prints",
        "Enabled request logging for all requests (authenticated and unauthenticated)"
      ]
    },
    {
      "date":"2013-06-02",
      "changes":[
        "Changed \/foodservices\/product to \/foodservices\/products"
      ]
    },
    {
      "date":"2013-05-27",
      "changes":[
        "Added jsonp ?callback= functionality",
        "Added XML output format"
      ]
    },
    {
      "date":"2013-05-25",
      "changes":[
        "Added \/foodservices\/menu method",
        "Added \/foodservices\/notes method",
        "Added \/foodservices\/announcements method"
      ]
    },
    {
      "date":"2013-05-23",
      "changes":[
        "Added \/buildings\/list method",
        "Added \/resources\/printers method"
      ]
    },
    {
      "date":"2013-05-21",
      "changes":[
        "Added parameters key to \/api\/methods"
      ]
    },
    {
      "date":"2013-05-20",
      "changes":[
        "Added changelog endpoint",
        "Added api version endpoint",
        "Bumped API to version 2.03"
      ]
    }
  ]
}
```


# API Methods List

```
GET /api/methods.{format}
```

## Description

> This method returns all api endpoint methods available to use

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
    <td>1103</td>
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

- Usage won't increase for calling this method
- Any value can be `null`


### Sources

- https://api.uwaterloo.ca


## Parameters

```
GET /api/methods.{format}
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
GET /api/methods.{format}
```

- **http://api.uwaterloo.ca/v2/api/methods.json**
- **http://api.uwaterloo.ca/v2/api/methods.xml**
- **http://api.uwaterloo.ca/v2/api/methods.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>method_id</b></td>
    <td>integer</td>
    <td>API assigned method ID</td>
  </tr>
  <tr>
    <td><b>method_url</b></td>
    <td>string</td>
    <td>API assigned method endpoint url</td>
  </tr>
  <tr>
    <td><b>service_id</b></td>
    <td>integer</td>
    <td>API assigned method's parent service's id</td>
  </tr>
  <tr>
    <td><b>service_name</b></td>
    <td>string</td>
    <td>API assigned method's parent service's name</td>
  </tr>
  <tr>
    <td><b>parameters</b></td>
    <td>list</td>
    <td>String of acceptable method parameters</td>
  </tr>
</table>


## Output

#### JSON

```json
{
  "meta":{
    "requests":3768,
    "timestamp":1381898202,
    "status":200,
    "message":"Request successful",
    "method_id":1103,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "method_id":1081,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/api\/services.{format}",
      "service_id":223,
      "service_name":"api",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1087,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/server\/time.{format}",
      "service_id":227,
      "service_name":"server",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1091,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/server\/codes.{format}",
      "service_id":227,
      "service_name":"server",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1093,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/server\/admin.{format}",
      "service_id":227,
      "service_name":"server",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1097,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/api\/usage.{format}",
      "service_id":223,
      "service_name":"api",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1103,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/api\/methods.{format}",
      "service_id":223,
      "service_name":"api",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1109,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/api\/versions.{format}",
      "service_id":223,
      "service_name":"api",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1117,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/api\/changelog.{format}",
      "service_id":223,
      "service_name":"api",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1123,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/resources\/printers.{format}",
      "service_id":229,
      "service_name":"resources",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1129,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/resources\/infosessions.{format}",
      "service_id":229,
      "service_name":"resources",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1153,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/courses\/{department}.{format}",
      "service_id":239,
      "service_name":"courses",
      "parameters":[
        "department",
        "format"
      ]
    },
    {
      "method_id":1163,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/courses\/{department}\/{number}.{format}",
      "service_id":239,
      "service_name":"courses",
      "parameters":[
        "department",
        "number",
        "format"
      ]
    },
    {
      "method_id":1171,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/courses\/{department}\/{number}\/schedule.{format}",
      "service_id":239,
      "service_name":"courses",
      "parameters":[
        "department",
        "number",
        "format"
      ]
    },
    {
      "method_id":1181,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/courses\/{subject}\/{number}\/prerequisites.{format}",
      "service_id":239,
      "service_name":"courses",
      "parameters":[
        "subject",
        "number",
        "format"
      ]
    },
    {
      "method_id":1187,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/terms\/{term}\/examschedule.{format}",
      "service_id":241,
      "service_name":"terms",
      "parameters":[
        "term",
        "format"
      ]
    },
    {
      "method_id":1193,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/terms\/{term}\/{subject}\/{number}\/schedule.{format}",
      "service_id":241,
      "service_name":"terms",
      "parameters":[
        "term",
        "subject",
        "number",
        "format"
      ]
    },
    {
      "method_id":1213,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/buildings\/list.{format}",
      "service_id":257,
      "service_name":"buildings",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1217,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/buildings\/{building}.{format}",
      "service_id":257,
      "service_name":"buildings",
      "parameters":[
        "building",
        "format"
      ]
    },
    {
      "method_id":1223,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/buildings\/{building}\/{room}\/courses.{format}",
      "service_id":257,
      "service_name":"buildings",
      "parameters":[
        "building",
        "room",
        "format"
      ]
    },
    {
      "method_id":1229,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/quest\/groups.{format}",
      "service_id":263,
      "service_name":"quest",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1231,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/quest\/organizations.{format}",
      "service_id":263,
      "service_name":"quest",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1237,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/quest\/subjects.{format}",
      "service_id":263,
      "service_name":"quest",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1249,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/quest\/terms.{format}",
      "service_id":263,
      "service_name":"quest",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1259,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/quest\/instructions.{format}",
      "service_id":263,
      "service_name":"quest",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1277,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/products\/{id}.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "id",
        "format"
      ]
    },
    {
      "method_id":1279,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/products\/search.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1283,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/outlets.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1289,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/watcard.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1291,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/{year}\/{week}\/{id}\/menu.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "year",
        "week",
        "id",
        "format"
      ]
    },
    {
      "method_id":1297,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/{year}\/{week}\/{id}\/notes.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "year",
        "week",
        "id",
        "format"
      ]
    },
    {
      "method_id":1301,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/{year}\/{week}\/{id}\/announcements.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "year",
        "week",
        "id",
        "format"
      ]
    },
    {
      "method_id":1303,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/menu.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1307,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/notes.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1319,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/announcements.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    },
    {
      "method_id":1321,
      "method_url":"http:\/\/api.uwaterloo.ca\/v2\/foodservices\/diets.{format}",
      "service_id":269,
      "service_name":"foodservices",
      "parameters":[
        "format"
      ]
    }
  ]
}
```


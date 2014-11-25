# API Services List

```
GET /api/services.{format}
```

## Description

> This method returns all api services available to use

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
    <td>1081</td>
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

- Usage won't increase if no data is returned
- Any value can be `null`


### Sources

- https://api.uwaterloo.ca


## Parameters

```
GET /api/services.{format}
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
GET /api/services.{format}
```

- **https://api.uwaterloo.ca/v2/api/services.json**
- **https://api.uwaterloo.ca/v2/api/services.xml**
- **https://api.uwaterloo.ca/v2/api/services.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>service_id</b></td>
    <td>integer</td>
    <td>API assigned service ID</td>
  </tr>
  <tr>
    <td><b>service_name</b></td>
    <td>string</td>
    <td>API assigned service name</td>
  </tr>
  <tr>
    <td><b>service_url</b></td>
    <td>string</td>
    <td>API assigned service endpoint url</td>
  </tr>
  <tr>
    <td><b>methods</b></td>
    <td>list</td>
    <td>Available endpoints under the service<br><table>
  <tr>
    <td><b>method_id</b></td>
    <td>string</td>
    <td>API assigned method under service id</td>
  </tr>
  <tr>
    <td><b>method_url</b></td>
    <td>string</td>
    <td>API assigned method endpoint under service</td>
  </tr>
</table>
</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":3798,
    "timestamp":1381933867,
    "status":200,
    "message":"Request successful",
    "method_id":1081,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "service_id":223,
      "service_name":"api",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/api",
      "methods":[
        {
          "method_id":1081,
          "method_url":"\/services.{format}"
        },
        {
          "method_id":1097,
          "method_url":"\/usage.{format}"
        },
        {
          "method_id":1103,
          "method_url":"\/methods.{format}"
        },
        {
          "method_id":1109,
          "method_url":"\/versions.{format}"
        },
        {
          "method_id":1117,
          "method_url":"\/changelog.{format}"
        }
      ]
    },
    {
      "service_id":227,
      "service_name":"server",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/server",
      "methods":[
        {
          "method_id":1087,
          "method_url":"\/time.{format}"
        },
        {
          "method_id":1091,
          "method_url":"\/codes.{format}"
        },
        {
          "method_id":1093,
          "method_url":"\/admin.{format}"
        }
      ]
    },
    {
      "service_id":229,
      "service_name":"resources",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/resources",
      "methods":[
        {
          "method_id":1123,
          "method_url":"\/printers.{format}"
        },
        {
          "method_id":1129,
          "method_url":"\/infosessions.{format}"
        },
        {
          "method_id":1229,
          "method_url":"\/academics\/groups.{format}"
        },
        {
          "method_id":1231,
          "method_url":"\/academics\/organizations.{format}"
        },
        {
          "method_id":1237,
          "method_url":"\/academics\/subjects.{format}"
        },
        {
          "method_id":1249,
          "method_url":"\/academics\/terms.{format}"
        },
        {
          "method_id":1259,
          "method_url":"\/academics\/instructions.{format}"
        }
      ]
    },
    {
      "service_id":239,
      "service_name":"courses",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/courses",
      "methods":[
        {
          "method_id":1153,
          "method_url":"\/{department}.{format}"
        },
        {
          "method_id":1163,
          "method_url":"\/{department}\/{number}.{format}"
        },
        {
          "method_id":1171,
          "method_url":"\/{department}\/{number}\/schedule.{format}"
        },
        {
          "method_id":1181,
          "method_url":"\/{subject}\/{number}\/prerequisites.{format}"
        }
      ]
    },
    {
      "service_id":241,
      "service_name":"terms",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/terms",
      "methods":[
        {
          "method_id":1187,
          "method_url":"\/{term}\/examschedule.{format}"
        },
        {
          "method_id":1193,
          "method_url":"\/{term}\/{subject}\/{number}\/schedule.{format}"
        }
      ]
    },
    {
      "service_id":257,
      "service_name":"buildings",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/buildings",
      "methods":[
        {
          "method_id":1213,
          "method_url":"\/list.{format}"
        },
        {
          "method_id":1217,
          "method_url":"\/{building}.{format}"
        },
        {
          "method_id":1223,
          "method_url":"\/{building}\/{room}\/courses.{format}"
        }
      ]
    },
    {
      "service_id":269,
      "service_name":"foodservices",
      "service_url":"https:\/\/api.uwaterloo.ca\/v2\/foodservices",
      "methods":[
        {
          "method_id":1277,
          "method_url":"\/products\/{id}.{format}"
        },
        {
          "method_id":1279,
          "method_url":"\/products\/search.{format}"
        },
        {
          "method_id":1283,
          "method_url":"\/outlets.{format}"
        },
        {
          "method_id":1289,
          "method_url":"\/watcard.{format}"
        },
        {
          "method_id":1291,
          "method_url":"\/{year}\/{week}\/{id}\/menu.{format}"
        },
        {
          "method_id":1297,
          "method_url":"\/{year}\/{week}\/{id}\/notes.{format}"
        },
        {
          "method_id":1301,
          "method_url":"\/{year}\/{week}\/{id}\/announcements.{format}"
        },
        {
          "method_id":1303,
          "method_url":"\/menu.{format}"
        },
        {
          "method_id":1307,
          "method_url":"\/notes.{format}"
        },
        {
          "method_id":1319,
          "method_url":"\/announcements.{format}"
        },
        {
          "method_id":1321,
          "method_url":"\/diets.{format}"
        }
      ]
    }
  ]
}
```


# Annual Holidays

```
GET /events/holidays.{format}
```

## Description

> This method returns a list of holidays for the current year

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
    <td>1423</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>events</td>
    <td><b>Service ID</b></td>
    <td>271</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>UW API</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every year</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/Holidays/holidays.csv


## Parameters

```
GET /events/holidays.{format}
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
GET /events/holidays.{format}
```

- **https://api.uwaterloo.ca/v2/events/holidays.json**
- **https://api.uwaterloo.ca/v2/events/holidays.xml**
- **https://api.uwaterloo.ca/v2/events/holidays.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Name of the holiday</td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>date</td>
    <td>Y-m-d formatted holiday date</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":4867,
    "timestamp":1384192338,
    "status":200,
    "message":"Request successful",
    "method_id":1423,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"New Year's Day",
      "date":"2013-01-01"
    },
    {
      "name":"Family Day",
      "date":"2013-02-18"
    },
    {
      "name":"Good Friday",
      "date":"2013-03-29"
    },
    {
      "name":"Victoria Day",
      "date":"2013-05-20"
    },
    {
      "name":"Canada Day",
      "date":"2013-07-01"
    },
    {
      "name":"Civic Holiday",
      "date":"2013-08-05"
    },
    {
      "name":"Labour Day",
      "date":"2013-09-02"
    },
    {
      "name":"Thanksgiving",
      "date":"2013-10-14"
    },
    {
      "name":"Christmas",
      "date":"2013-12-25"
    },
    {
      "name":"Boxing Day",
      "date":"2013-12-26"
    },
    {
      "name":"Additional Days",
      "date":"2013-12-24"
    },
    {
      "name":"Additional Days",
      "date":"2013-12-27"
    },
    {
      "name":"Additional Days",
      "date":"2013-12-30"
    },
    {
      "name":"Additional Days",
      "date":"2013-12-31"
    }
  ]
}
```


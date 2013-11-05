# Food Services Menu Notes

```
GET /foodservices/notes.{format}
```

## Description

> This method returns additional notes regarding food served in the current week

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
    <td>1297</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>foodservices</td>
    <td><b>Service ID</b></td>
    <td>269</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Food Services</td>
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

- Usage won't increase if there is not data returned
- We cannot modify the data from this method
- The results are only for this current week (where the week starts on Monday)
- Any value can be `null`


### Sources

- https://uwaterloo.ca/food-services/


## Parameters

```
GET /foodservices/notes.{format}
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
GET /foodservices/notes.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/notes.json**
- **http://api.uwaterloo.ca/v2/foodservices/notes.xml**
- **http://api.uwaterloo.ca/v2/foodservices/notes.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>date</b></td>
    <td>object</td>
    <td>Menu date object</td>
  </tr>
  <tr>
    <td><b>outlet_name</b></td>
    <td>string</td>
    <td>Outlet name as per /foodservices/outlets</td>
  </tr>
  <tr>
    <td><b>outlet_id</b></td>
    <td>integer</td>
    <td>Outlet ID as per /foodservices/outlets</td>
  </tr>
  <tr>
    <td><b>note</b></td>
    <td>object</td>
    <td>Note</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":138,
    "timestamp":1381961643,
    "status":200,
    "message":"Request successful",
    "method_id":2,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "date":"2013-10-14",
      "outlet_name":"REVelation",
      "outlet_id":7,
      "note":"Closed \"Happy Thanksgiving\""
    },
    {
      "date":"2013-10-15",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    },
    {
      "date":"2013-10-16",
      "outlet_name":"Mudie's",
      "outlet_id":5,
      "note":"\"Oktoberfest Dinner\""
    },
    {
      "date":"2013-10-16",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    },
    {
      "date":"2013-10-17",
      "outlet_name":"Mudie's",
      "outlet_id":5,
      "note":"\"Don's Do Dinner\""
    },
    {
      "date":"2013-10-17",
      "outlet_name":"REVelation",
      "outlet_id":7,
      "note":"\"Don's Do Dinner\""
    },
    {
      "date":"2013-10-18",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    }
  ]
}
```


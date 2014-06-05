# Food Services Menu Notes Filtered by Week

```
GET /foodservices/{year}/{week}/notes.{format}
```

## Description

> This method returns additional notes regarding food served in the week specified

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

- Usage won't increase if there is no data returned
- We cannot modify the data from this method
- The results are only for the week specified (where the week starts on Monday)
- Any value can be `null`


### Sources

- https://uwaterloo.ca/food-services/


## Parameters

```
GET /foodservices/{year}/{week}/notes.{format}
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
    <td>input</td>
    <td><i>yes</i></td>
    <td>Number representing year</td>
  </tr>
  <tr>
    <td><b>week</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Number representing week</td>
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
GET /foodservices/{year}/{week}/notes.{format}
```

- **https://api.uwaterloo.ca/v2/foodservices/2014/2/notes.json**
- **https://api.uwaterloo.ca/v2/foodservices/2014/2/notes.xml**
- **https://api.uwaterloo.ca/v2/foodservices/2014/2/notes.json?callback=myResponse**


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
    "requests":7151,
    "timestamp":1401973635,
    "status":200,
    "message":"Request successful",
    "method_id":1297,
    "method":{
      
    }
  },
  "data":[
    {
      "date":"2014-01-06",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    },
    {
      "date":"2014-01-07",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    },
    {
      "date":"2014-01-08",
      "outlet_name":"Mudie's",
      "outlet_id":5,
      "note":"\"Welcome Back Dinner\""
    },
    {
      "date":"2014-01-08",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    },
    {
      "date":"2014-01-08",
      "outlet_name":"REVelation",
      "outlet_id":7,
      "note":"\"Welcome Back Dinner\"\nLobster Bisque, Apple Blossoms and Ice Cream\nDads Rootbeer, Orangina"
    },
    {
      "date":"2014-01-09",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    },
    {
      "date":"2014-01-10",
      "outlet_name":"Festival Fare",
      "outlet_id":6,
      "note":"Daily Fish"
    }
  ]
}
```


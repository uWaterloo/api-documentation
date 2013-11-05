# Food Services Outlets

```
GET /foodservices/outlets.{format}
```

## Description

> This method returns a list of all outlets and their unique IDs, names and breakfast/lunch/dinner meal service indicators

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
    <td>1283</td>
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
- Any value can be `null`


### Sources

- https://uwaterloo.ca/food-services/


## Parameters

```
GET /foodservices/outlets.{format}
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
GET /foodservices/outlets.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/outlets.json**
- **http://api.uwaterloo.ca/v2/foodservices/outlets.xml**
- **http://api.uwaterloo.ca/v2/foodservices/outlets.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>outlet_id</b></td>
    <td>integer</td>
    <td>Outlet ID number</td>
  </tr>
  <tr>
    <td><b>outlet_name</b></td>
    <td>string</td>
    <td>Outlet name</td>
  </tr>
  <tr>
    <td><b>has_breakfast</b></td>
    <td>boolean</td>
    <td>If serves breakfast</td>
  </tr>
  <tr>
    <td><b>has_lunch</b></td>
    <td>boolean</td>
    <td>If serves lunch</td>
  </tr>
  <tr>
    <td><b>has_dinner</b></td>
    <td>boolean</td>
    <td>If serves dinner</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":139,
    "timestamp":1381961771,
    "status":200,
    "message":"Request successful",
    "method_id":2,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "outlet_id":3,
      "outlet_name":"Bon Appetit",
      "has_breakfast":0,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":9,
      "outlet_name":"Bookends",
      "has_breakfast":1,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":20,
      "outlet_name":"Browser's",
      "has_breakfast":1,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":1,
      "outlet_name":"Brubakers",
      "has_breakfast":0,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":21,
      "outlet_name":"Eye Opener",
      "has_breakfast":1,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":24,
      "outlet_name":"Farm Market",
      "has_breakfast":1,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":6,
      "outlet_name":"Festival Fare",
      "has_breakfast":0,
      "has_lunch":1,
      "has_dinner":0
    },
    {
      "outlet_id":25,
      "outlet_name":"Liquid Assets",
      "has_breakfast":0,
      "has_lunch":1,
      "has_dinner":0
    },
    {
      "outlet_id":5,
      "outlet_name":"Mudie's",
      "has_breakfast":0,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":22,
      "outlet_name":"PAS Lounge",
      "has_breakfast":1,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":23,
      "outlet_name":"Pastry Plus",
      "has_breakfast":1,
      "has_lunch":1,
      "has_dinner":1
    },
    {
      "outlet_id":7,
      "outlet_name":"REVelation",
      "has_breakfast":0,
      "has_lunch":1,
      "has_dinner":1
    }
  ]
}
```


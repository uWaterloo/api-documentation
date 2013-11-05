# Food Services Diets

```
GET /foodservices/diets.{format}
```

## Description

> This method returns a list of all diets

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
    <td>1321</td>
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
GET /foodservices/diets.{format}
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
GET /foodservices/diets.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/diets.json**
- **http://api.uwaterloo.ca/v2/foodservices/diets.xml**
- **http://api.uwaterloo.ca/v2/foodservices/diets.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>diet_id</b></td>
    <td>integer</td>
    <td>Diet ID number</td>
  </tr>
  <tr>
    <td><b>diet_type</b></td>
    <td>string</td>
    <td>Diet type</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":134,
    "timestamp":1381961246,
    "status":200,
    "message":"Request successful",
    "method_id":2,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "diet_id":2,
      "diet_type":"Non Vegetarian"
    },
    {
      "diet_id":5,
      "diet_type":"Vegan"
    },
    {
      "diet_id":6,
      "diet_type":"Vegetarian"
    },
    {
      "diet_id":7,
      "diet_type":"Halal"
    }
  ]
}
```


# Food Services Menu Announcements

```
GET /foodservices/announcements.{format}
```

## Description

> This method returns additional announcements regarding food served in the current week

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
    <td>1301</td>
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
GET /foodservices/announcements.{format}
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
GET /foodservices/announcements.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/2013/2/announcements.json**
- **http://api.uwaterloo.ca/v2/foodservices/2013/2/announcements.xml**
- **http://api.uwaterloo.ca/v2/foodservices/2013/2/announcements.json?callback=myResponse**


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
    <td>Advertisement date object</td>
  </tr>
  <tr>
    <td><b>ad_text</b></td>
    <td>string</td>
    <td>Advertisement text</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":7140,
    "timestamp":1401908828,
    "status":200,
    "message":"Request successful",
    "method_id":1301,
    "method":{
      
    }
  },
  "data":[
    {
      "date":"2013-01-07",
      "ad_text":"Try our newest dining concept on campus...The Chili Pepper - Tex Mex Cuisine."
    }
  ]
}
```


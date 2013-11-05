# List of all WatCard locations

```
GET /foodservices/watcard.{format}
```

## Description

> This method returns a list of all WatCard locations according to Food Services

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
    <td>1289</td>
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
GET /foodservices/watcard.{format}
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
GET /foodservices/watcard.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/watcard.json**
- **http://api.uwaterloo.ca/v2/foodservices/watcard.xml**
- **http://api.uwaterloo.ca/v2/foodservices/watcard.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>vendor_id</b></td>
    <td>integer</td>
    <td>Outlet ID number</td>
  </tr>
  <tr>
    <td><b>vendor_name</b></td>
    <td>string</td>
    <td>Vendor name</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":142,
    "timestamp":1381962116,
    "status":200,
    "message":"Request successful",
    "method_id":2,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "vendor_id":20,
      "vendor_name":"Apple II Hairstylists"
    },
    {
      "vendor_id":21,
      "vendor_name":"Bombshelter for meals"
    },
    {
      "vendor_id":13,
      "vendor_name":"Campus Pizza"
    },
    {
      "vendor_id":17,
      "vendor_name":"Curry in a Hurry"
    },
    {
      "vendor_id":29,
      "vendor_name":"Domino's Pizza"
    },
    {
      "vendor_id":12,
      "vendor_name":"East Side Mario's"
    },
    {
      "vendor_id":11,
      "vendor_name":"Farah Foods"
    },
    {
      "vendor_id":32,
      "vendor_name":"Kabob Hut"
    },
    {
      "vendor_id":27,
      "vendor_name":"McGinnis Front Row"
    },
    {
      "vendor_id":23,
      "vendor_name":"Meetpoint Restaurant"
    },
    {
      "vendor_id":33,
      "vendor_name":"Mr. Panino Beijing House"
    },
    {
      "vendor_id":16,
      "vendor_name":"Pita Pit"
    },
    {
      "vendor_id":14,
      "vendor_name":"Pizza Pizza"
    },
    {
      "vendor_id":24,
      "vendor_name":"Sobey's - Columbia Street"
    },
    {
      "vendor_id":19,
      "vendor_name":"Student Health Pharmacy"
    },
    {
      "vendor_id":10,
      "vendor_name":"Swiss Chalet"
    },
    {
      "vendor_id":25,
      "vendor_name":"The Grill"
    },
    {
      "vendor_id":30,
      "vendor_name":"University Club"
    },
    {
      "vendor_id":18,
      "vendor_name":"Waterloo Taxi"
    },
    {
      "vendor_id":15,
      "vendor_name":"William's Coffee"
    },
    {
      "vendor_id":31,
      "vendor_name":"Wings Up Delivery"
    }
  ]
}
```


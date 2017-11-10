# Building Vending Machines

```
GET /buildings/{building_code}/vendingmachines.{format}
```

## Description

> This method returns list of vending machines available in a given building

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
    <td>1487</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>buildings</td>
    <td><b>Service ID</b></td>
    <td>257</td>
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

- Any value can be `null`


### Sources

- https://uwaterloo.ca/food-services/


## Parameters

```
GET /buildings/{building_code}/vendingmachines.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>building</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Building code</td>
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
GET /buildings/{building_code}/vendingmachines.{format}
```

- **http://api.uwaterloo.ca/v2/buildings/MC/vendingmachines.json**
- **http://api.uwaterloo.ca/v2/buildings/MC/vendingmachines.xml**
- **http://api.uwaterloo.ca/v2/buildings/MHR/vendingmachines.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>building_name</b></td>
    <td>string</td>
    <td>Name of the Building</td>
  </tr>
  <tr>
    <td><b>building_acronym</b></td>
    <td>string</td>
    <td>Building Acronym</td>
  </tr>
  <tr>
    <td><b>vending_machines</b></td>
    <td>list</td>
    <td>Machines list<br><table>
  <tr>
    <td><b>location</b></td>
    <td>string</td>
    <td>Relative machine location inside the bulding</td>
  </tr>
  <tr>
    <td><b>machines</b></td>
    <td>number</td>
    <td>Total machines in that given location</td>
  </tr>
  <tr>
    <td><b>products</b></td>
    <td>list</td>
    <td>List of products/machine type</td>
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
    "requests":796909,
    "timestamp":1452283330,
    "status":200,
    "message":"Request successful",
    "method_id":1487,
    "method":{
      
    }
  },
  "data":{
    "building_name":"Mathematics & Computer Building",
    "building_acronym":"MC",
    "vending_machines":[
      {
        "location":"2nd floor lounge",
        "machines":4,
        "products":[
          "Coca-Cola Products",
          "Dasani products",
          "Snacks"
        ]
      },
      {
        "location":"3rd floor lounge",
        "machines":6,
        "products":[
          "Energy\/Powerade",
          "Coca-Cola Products",
          "Dasani products",
          "Health and Wellness",
          "Snacks",
          "Milk to Go and Snacks"
        ]
      }
    ]
  }
}
```


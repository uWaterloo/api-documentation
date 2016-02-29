# Food Services Vending Machines

```
GET /foodservices/vendingmachines.{format}
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
    <td>1483</td>
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

- Any value can be `null`


### Sources

- https://uwaterloo.ca/food-services/


## Parameters

```
GET /foodservices/vendingmachines.{format}
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
GET /foodservices/vendingmachines.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/vendingmachines.json**
- **http://api.uwaterloo.ca/v2/foodservices/vendingmachines.xml**
- **http://api.uwaterloo.ca/v2/foodservices/vendingmachines.json?callback=myResponse**


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
    "requests":796886,
    "timestamp":1452282366,
    "status":200,
    "message":"Request successful",
    "method_id":1483,
    "method":{
      
    }
  },
  "data":[
    {
      "building_name":"Arts Lecture Hall",
      "building_acronym":"AL",
      "vending_machines":[
        {
          "location":"West entrance",
          "machines":3,
          "products":[
            "Coca-Cola Products",
            "Dasani products",
            "Snacks"
          ]
        }
      ]
    },
    {
      "building_name":"B.C. Matthews Hall",
      "building_acronym":"BMH",
      "vending_machines":[
        {
          "location":"South entrance atrium",
          "machines":2,
          "products":[
            "Coca-Cola Products",
            "Snacks"
          ]
        }
      ]
    },
    {
      "building_name":"Centre for Environmental and Information Technology",
      "building_acronym":"EIT",
      "vending_machines":[
        {
          "location":"Lower level",
          "machines":3,
          "products":[
            "Coca-Cola Products",
            "Dasani products",
            "Snacks"
          ]
        }
      ]
    },
    {
      "building_name":"Columbia Icefield",
      "building_acronym":"CIF",
      "vending_machines":[
        {
          "location":"Ice rink entrance",
          "machines":4,
          "products":[
            "Powerade",
            "Coca-Cola Products",
            "Health and Wellness",
            "Snacks"
          ]
        }
      ]
    },
    {
      "building_name":"Columbia Lake Village",
      "building_acronym":"CLV",
      "vending_machines":[
        {
          "location":"Main floor lounge",
          "machines":3,
          "products":[
            "Coca-Cola Products",
            "Juice",
            "Snacks"
          ]
        }
      ]
    },
    {
      "building_name":"William G. Davis Computer Research Centre",
      "building_acronym":"DC",
      "vending_machines":[
        {
          "location":"Library",
          "machines":1,
          "products":[
            "Stationery"
          ]
        },
        {
          "location":"Lobby",
          "machines":2,
          "products":[
            "Snacks",
            "Health & Wellness"
          ]
        },
        {
          "location":"Main floor hallway",
          "machines":5,
          "products":[
            "Coca-Cola Products",
            "Dasani products",
            "Snacks",
            "Milk to Go and Snacks"
          ]
        }
      ]
    }
  ]
}
```


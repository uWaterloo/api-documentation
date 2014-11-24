# FoodServices Product Details

```
GET /foodservices/products/{product_id}.{format}
```

## Description

> This method returns a product's nutritional information

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
    <td>1277</td>
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
    <td>FoodServices</td>
    <td><b>Data Type</b></td>
    <td>Direct DB connection</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>On request (lib)</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- Any value can be `null`


### Sources

- https://uwaterloo.ca/food-services


## Parameters

```
GET /foodservices/products/{product_id}.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>product_id</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid product ID from menu</td>
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
GET /foodservices/products/{product_id}.{format}
```

- **https://api.uwaterloo.ca/v2/foodservices/products/1386.json**
- **https://api.uwaterloo.ca/v2/foodservices/products/1386.xml**
- **https://api.uwaterloo.ca/v2/foodservices/products/1386.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>product_id</b></td>
    <td>integer</td>
    <td>Food item's numeric id</td>
  </tr>
  <tr>
    <td><b>product_name</b></td>
    <td>string</td>
    <td>Name of the food item</td>
  </tr>
  <tr>
    <td><b>ingredients</b></td>
    <td>string</td>
    <td>Food ingredients</td>
  </tr>
  <tr>
    <td><b>serving_size</b></td>
    <td>string</td>
    <td>Item's service size (in grams or whole)</td>
  </tr>
  <tr>
    <td><b>serving_size_ml</b></td>
    <td>integer</td>
    <td>Serving size in milliliters</td>
  </tr>
  <tr>
    <td><b>serving_size_g</b></td>
    <td>integer</td>
    <td>Serving size in grams</td>
  </tr>
  <tr>
    <td><b>calories</b></td>
    <td>integer</td>
    <td>Food calorie count</td>
  </tr>
  <tr>
    <td><b>total_fat_g</b></td>
    <td>integer</td>
    <td>Total fat in grams</td>
  </tr>
  <tr>
    <td><b>total_fat_percent</b></td>
    <td>integer</td>
    <td>Total fat in percentage</td>
  </tr>
  <tr>
    <td><b>fat_saturated_g</b></td>
    <td>integer</td>
    <td>Total saturated fat in grams</td>
  </tr>
  <tr>
    <td><b>fat_saturated_percent</b></td>
    <td>integer</td>
    <td>Total saturated fat in percentage</td>
  </tr>
  <tr>
    <td><b>fat_trans_g</b></td>
    <td>integer</td>
    <td>Total trans fat in grams</td>
  </tr>
  <tr>
    <td><b>fat_trans_percent</b></td>
    <td>integer</td>
    <td>Total trans fat in percentage</td>
  </tr>
  <tr>
    <td><b>cholesterol_mg</b></td>
    <td>integer</td>
    <td>Total cholesterol in milligrams</td>
  </tr>
  <tr>
    <td><b>sodium_mg</b></td>
    <td>integer</td>
    <td>Sodium in milligrams</td>
  </tr>
  <tr>
    <td><b>sodium_percent</b></td>
    <td>integer</td>
    <td>Sodium in percentage</td>
  </tr>
  <tr>
    <td><b>carbo_g</b></td>
    <td>integer</td>
    <td>Total carbohydrates in grams</td>
  </tr>
  <tr>
    <td><b>carbo_percent</b></td>
    <td>integer</td>
    <td>Carbohydrates as percentage</td>
  </tr>
  <tr>
    <td><b>carbo_fibre_g</b></td>
    <td>integer</td>
    <td>Carbohydrate fibres in grams</td>
  </tr>
  <tr>
    <td><b>carbo_fibre_percent</b></td>
    <td>integer</td>
    <td>Carbohydrates fibers as percentage</td>
  </tr>
  <tr>
    <td><b>carbo_sugars_g</b></td>
    <td>integer</td>
    <td>Carbohydrate sugar in grams</td>
  </tr>
  <tr>
    <td><b>protein_g</b></td>
    <td>integer</td>
    <td>Total protein in grams</td>
  </tr>
  <tr>
    <td><b>vitamin_a_percent</b></td>
    <td>integer</td>
    <td>Total vitamin A percentage</td>
  </tr>
  <tr>
    <td><b>vitamin_c_percent</b></td>
    <td>integer</td>
    <td>Total vitamin C percentage</td>
  </tr>
  <tr>
    <td><b>calcium_percent</b></td>
    <td>integer</td>
    <td>Total calcium percentage</td>
  </tr>
  <tr>
    <td><b>iron_percent</b></td>
    <td>integer</td>
    <td>Total iron percentage</td>
  </tr>
  <tr>
    <td><b>micro_nutrients</b></td>
    <td>string</td>
    <td>Micro nutrients in item</td>
  </tr>
  <tr>
    <td><b>tips</b></td>
    <td>string</td>
    <td>Any eating tips for the item</td>
  </tr>
  <tr>
    <td><b>diet_id</b></td>
    <td>integer</td>
    <td>Foodservices given diet id</td>
  </tr>
  <tr>
    <td><b>diet_type</b></td>
    <td>string</td>
    <td>String representation of the diet_id</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":132,
    "timestamp":1381960356,
    "status":200,
    "message":"Request successful",
    "method_id":1277,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "product_id":1386,
    "product_name":"Maple Thyme Salmon",
    "ingredients":"Salmon, maple syrup, thyme, soy sauce, sesame seeds",
    "serving_size":"467 grams",
    "serving_size_ml":null,
    "serving_size_g":null,
    "calories":850,
    "total_fat_g":41,
    "total_fat_percent":63,
    "fat_saturated_g":10,
    "fat_saturated_percent":50,
    "fat_trans_g":null,
    "fat_trans_percent":null,
    "cholesterol_mg":255,
    "sodium_mg":1150,
    "sodium_percent":48,
    "carbo_g":38,
    "carbo_percent":13,
    "carbo_fibre_g":null,
    "carbo_fibre_percent":null,
    "carbo_sugars_g":33,
    "protein_g":79,
    "vitamin_a_percent":35,
    "vitamin_c_percent":25,
    "calcium_percent":15,
    "iron_percent":20,
    "micro_nutrients":null,
    "tips":null,
    "diet_id":2,
    "diet_type":"Non Vegetarian"
  }
}
```


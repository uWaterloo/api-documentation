# Weekly Food Menu

```
GET /foodservices/menu.{format}
```

## Description

> This method returns current week's food menu.

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
    <td>1303</td>
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
    <td>UW FoodServices</td>
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

- http://foodservices.uwaterloo.ca


## Parameters

```
GET /foodservices/menu.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>format</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>The format of the output</td>
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
GET /foodservices/menu.{format}
```

- **https://api.uwaterloo.ca/v2/foodservices/2013/12/menu.json**
- **https://api.uwaterloo.ca/v2/foodservices/2013/22/menu.xml**
- **https://api.uwaterloo.ca/v2/foodservices/2013/15/menu.json?callback=myResponse**


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
    <td>Menu date object<br><table>
  <tr>
    <td><b>week</b></td>
    <td>integer</td>
    <td>Requested week</td>
  </tr>
  <tr>
    <td><b>year</b></td>
    <td>integer</td>
    <td>Requested year</td>
  </tr>
  <tr>
    <td><b>start</b></td>
    <td>string</td>
    <td>Starting day of the menu (Y-m-d)</td>
  </tr>
  <tr>
    <td><b>end</b></td>
    <td>string</td>
    <td>Ending day of the menu (Y-m-d)</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>outlets</b></td>
    <td>list</td>
    <td>Available outlets<br><table>
  <tr>
    <td><b>outlet_name</b></td>
    <td>string</td>
    <td>Name of the outlet</td>
  </tr>
  <tr>
    <td><b>outlet_id</b></td>
    <td>integer</td>
    <td>Foodservices ID for the outlet</td>
  </tr>
  <tr>
    <td><b>menu</b></td>
    <td>list</td>
    <td>The outlet menu list<br><table>
  <tr>
    <td><b>date</b></td>
    <td>string</td>
    <td>Date of the menu (Y-m-d)</td>
  </tr>
  <tr>
    <td><b>day</b></td>
    <td>string</td>
    <td>Day of the week</td>
  </tr>
  <tr>
    <td><b>meals</b></td>
    <td>object</td>
    <td>All the meals for the day<br><table>
  <tr>
    <td><b>lunch</b></td>
    <td>list</td>
    <td>Lunch menu items<br><table>
  <tr>
    <td><b>product_name</b></td>
    <td>string</td>
  </tr>
  <tr>
    <td><b>diet_type</b></td>
    <td>string</td>
  </tr>
  <tr>
    <td><b>product_id</b></td>
    <td>integer</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>dinner</b></td>
    <td>list</td>
    <td>Dinner menu<br><table>
  <tr>
    <td><b>product_name</b></td>
    <td>string</td>
  </tr>
  <tr>
    <td><b>diet_type</b></td>
    <td>string</td>
  </tr>
  <tr>
    <td><b>product_id</b></td>
    <td>integer</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>notes</b></td>
    <td>string</td>
    <td>Additional announcements for the day</td>
  </tr>
</table>
</td>
  </tr>
</table>
</td>
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
    "requests":136,
    "timestamp":1381961484,
    "status":200,
    "message":"Request successful",
    "method_id":1291,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "date":{
      "week":12,
      "year":2013,
      "start":"2013-03-18",
      "end":"2013-03-22"
    },
    "outlets":[
      {
        "outlet_name":"Bon Appetit",
        "outlet_id":3,
        "menu":[
          {
            "date":"2013-03-18",
            "day":"Monday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Beef with Mushrooms",
                  "product_id":665,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Chicken Wings with BBQ Sauce",
                  "product_id":1964,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-19",
            "day":"Tuesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"General TSO Chicken",
                  "product_id":2453,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Beef with Satay Sauce",
                  "product_id":738,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-20",
            "day":"Wednesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Shrimp Special Sauce",
                  "product_id":2452,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Pork Chop with Lemon Grass",
                  "product_id":1955,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-21",
            "day":"Thursday",
            "meals":{
              "lunch":[
                {
                  "product_name":"King to Pork Chop",
                  "product_id":741,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Chicken with Chili Bean Sauce",
                  "product_id":null,
                  "diet_type":null
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-22",
            "day":"Friday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Chef Special",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":"Closes at 2:30"
          }
        ]
      },
      {
        "outlet_name":"Mudie's",
        "outlet_id":5,
        "menu":[
          {
            "date":"2013-03-18",
            "day":"Monday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Island Jerk Chicken Drums",
                  "product_id":790,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Moroccan Vegetable Ragout",
                  "product_id":2419,
                  "diet_type":"Vegan"
                },
                {
                  "product_name":"Prime Rib Burger w\/ Bacon and Swiss",
                  "product_id":2084,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Chicken stuffed w\/ Cheese and Broccoli",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Pan Fried White Fish w\/ Lemon and Garlic Butter",
                  "product_id":2425,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Vegetable Korma",
                  "product_id":1030,
                  "diet_type":"Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-19",
            "day":"Tuesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Asian Beef Noodles",
                  "product_id":1218,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Grilled Local Eggplant Bruschetta",
                  "product_id":2421,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Korean Taco",
                  "product_id":2420,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Butternut Squash Lasagna w\/ Goat Cheese, Sage and Breadcrumbs",
                  "product_id":2416,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Roasted Ontario Lamb Crusted w\/ Dijon and Rosemary",
                  "product_id":2422,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Veal Parmesan",
                  "product_id":339,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-20",
            "day":"Wednesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Sweet and Sour Pork",
                  "product_id":1844,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Tofu, Broccoli and Cashew Stir Fry",
                  "product_id":2423,
                  "diet_type":"Vegan"
                },
                {
                  "product_name":"Tuscan Baked Ziti",
                  "product_id":2410,
                  "diet_type":"Halal"
                }
              ],
              "dinner":[
                {
                  "product_name":"1\/4 Chicken w\/ Apple Butter and Sage Glaze",
                  "product_id":2409,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Chili-Rubbed New York Steakw\/ Corn and Green Chili Ragout",
                  "product_id":2417,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Portabella Mushroom w\/ Creamy Spinach-Artichoke Filling",
                  "product_id":2415,
                  "diet_type":"Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-21",
            "day":"Thursday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Indian Butter Chicken",
                  "product_id":1343,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Linguine with Roasted Vegetables and Pesto",
                  "product_id":2473,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Waterloo Region Sausage on a Toasted Garlic Bun w\/ Toppings",
                  "product_id":1363,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Local Maple Syrup & Dijon Glazed Salmon",
                  "product_id":2414,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Roasted Ribs w\/ Apple-Bacon BBQ Sauce",
                  "product_id":2408,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Roma Eggplant Parmesan",
                  "product_id":2413,
                  "diet_type":"Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-22",
            "day":"Friday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Chef's Feature",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"English Style Fish",
                  "product_id":2376,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Grilled Polenta w\/ Wild Mushrooms",
                  "product_id":2424,
                  "diet_type":"Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Macaroni and Cheese, O-L",
                  "product_id":1369,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Popcorn Chicken Bowl",
                  "product_id":1520,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"South Asian Beef and Broccoli",
                  "product_id":1382,
                  "diet_type":"Halal"
                }
              ]
            },
            "notes":null
          }
        ]
      },
      {
        "outlet_name":"Festival Fare",
        "outlet_id":6,
        "menu":[
          {
            "date":"2013-03-18",
            "day":"Monday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Chipotle and Lime Roasted Chicken Leg with Indian Harvest Rice",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Forty Creek Pulled Pork Sandwich",
                  "product_id":2445,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Meat Lasagna",
                  "product_id":2491,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Vegetable Lasagna",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":"Daily Fish"
          },
          {
            "date":"2013-03-19",
            "day":"Tuesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Carved Turkey Platter",
                  "product_id":2443,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Cheese and Feta Pie",
                  "product_id":2435,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Chef Creation",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Forty Creek Pulled Pork Sandwich",
                  "product_id":2445,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":"Daily Fish"
          },
          {
            "date":"2013-03-20",
            "day":"Wednesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Daily Fish",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Forty Creek Pulled Pork Sandwich",
                  "product_id":2445,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Pasta Bar",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-21",
            "day":"Thursday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Beef Vindaloo",
                  "product_id":2450,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Big Brunch Plate",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Forty Creek Pulled Pork Sandwich",
                  "product_id":2445,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Tofu Stirred Fried Vegetables with Basmati Rice and Naan Bread",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":"Daily Fish"
          },
          {
            "date":"2013-03-22",
            "day":"Friday",
            "meals":{
              "lunch":[
                {
                  "product_name":"BBQ Day",
                  "product_id":2492,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Forty Creek Pulled Pork Sandwich",
                  "product_id":2445,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Kelp Noodle Salad",
                  "product_id":2446,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Turkey Pot Pie",
                  "product_id":1982,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":"Daily Fish"
          }
        ]
      },
      {
        "outlet_name":"REVelation",
        "outlet_id":7,
        "menu":[
          {
            "date":"2013-03-18",
            "day":"Monday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Chicken Korma",
                  "product_id":1937,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Pork Souvlaki on a Flatbread",
                  "product_id":1320,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Portabella Club on Fresh Baked 5 Grain Bread",
                  "product_id":2353,
                  "diet_type":"Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Bacon Wrapped Turkey w\/ Stuffing",
                  "product_id":2482,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Baked Beans",
                  "product_id":2314,
                  "diet_type":"Vegan"
                },
                {
                  "product_name":"Penne w\/ Meat Sauce",
                  "product_id":1811,
                  "diet_type":"Halal"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-19",
            "day":"Tuesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Buffalo Style Chicken Tenders w\/ Blue Cheese Dressing",
                  "product_id":2167,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Chick Pea Curry, V",
                  "product_id":731,
                  "diet_type":"Vegan"
                },
                {
                  "product_name":"Taco Salad in a Tortilla Bowl",
                  "product_id":1484,
                  "diet_type":"Halal"
                }
              ],
              "dinner":[
                {
                  "product_name":"1\/4 Chicken w\/Hoisin Maple BBQ Sauce",
                  "product_id":2465,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Margarita Goat Cheese Pasta",
                  "product_id":2311,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Pork Schnitzel w\/ Hunter Sauce",
                  "product_id":2475,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-20",
            "day":"Wednesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Breaded Sole w\/ Pico de gallo",
                  "product_id":2471,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Caprese Melt on Foccacia",
                  "product_id":2468,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Chicken Caesar Salad",
                  "product_id":66,
                  "diet_type":"Halal"
                }
              ],
              "dinner":[
                {
                  "product_name":"Country Fried Chicken",
                  "product_id":1757,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Lamb Stew",
                  "product_id":917,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Tofu Parmesan O-L",
                  "product_id":842,
                  "diet_type":"Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-21",
            "day":"Thursday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Beef Quesadilla",
                  "product_id":1241,
                  "diet_type":"Non Vegetarian"
                },
                {
                  "product_name":"Indian Samosa w\/ Tamarind Sauce",
                  "product_id":1388,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Smoked Turkey and Swiss Grilled Cheese w\/ Guacamole",
                  "product_id":2474,
                  "diet_type":"Non Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Channa",
                  "product_id":1472,
                  "diet_type":"Vegan"
                },
                {
                  "product_name":"Roasted Flank Steak and Bok Choy",
                  "product_id":2121,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Waterloo Region Smoked Pork Chop",
                  "product_id":868,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-22",
            "day":"Friday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Chef's Feature",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Fish Taco w\/ Guacamole",
                  "product_id":2495,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Potato Pancakes",
                  "product_id":2059,
                  "diet_type":"Vegetarian"
                }
              ],
              "dinner":[
                {
                  "product_name":"Chicken fettucine Alfredo",
                  "product_id":1330,
                  "diet_type":"Halal"
                },
                {
                  "product_name":"Eggplant Wrap",
                  "product_id":2076,
                  "diet_type":"Vegetarian"
                },
                {
                  "product_name":"Teriyaki Meatballs",
                  "product_id":1521,
                  "diet_type":"Non Vegetarian"
                }
              ]
            },
            "notes":null
          }
        ]
      },
      {
        "outlet_name":"Liquid Assets",
        "outlet_id":25,
        "menu":[
          {
            "date":"2013-03-18",
            "day":"Monday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Falafel with Pineapple Baja Sauce",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Pork Bites with Pineapple Baja Sauce",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-19",
            "day":"Tuesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Curry Beef",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Tofu and Stir Fry Vegetable",
                  "product_id":2499,
                  "diet_type":"Vegan"
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-20",
            "day":"Wednesday",
            "meals":{
              "lunch":[
                {
                  "product_name":"7 Bean Mix",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Italian Sausage and Marinara Sauce",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-21",
            "day":"Thursday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Beef Meatballs with Vindaloo Sauce",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Vegetarian Meatballs with Vindaloo Sauce",
                  "product_id":null,
                  "diet_type":null
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":null
          },
          {
            "date":"2013-03-22",
            "day":"Friday",
            "meals":{
              "lunch":[
                {
                  "product_name":"Chicken Curry",
                  "product_id":null,
                  "diet_type":null
                },
                {
                  "product_name":"Tofu and Stir Fry Vegetable",
                  "product_id":2499,
                  "diet_type":"Vegan"
                }
              ],
              "dinner":[
                
              ]
            },
            "notes":null
          }
        ]
      }
    ]
  }
}
```


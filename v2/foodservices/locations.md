# Food Services Locations and Hours

```
GET /foodservices/locations.{format}
```

## Description

> This method returns a list of all outlets and their operating hour data

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
    <td>1381</td>
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
GET /foodservices/locations.{format}
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
GET /foodservices/locations.{format}
```

- **http://api.uwaterloo.ca/v2/foodservices/locations.json**
- **http://api.uwaterloo.ca/v2/foodservices/locations.xml**
- **http://api.uwaterloo.ca/v2/foodservices/locations.json?callback=myResponse**


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
    <td>Outlet ID number (not always same as outets.json method). Can be null</td>
  </tr>
  <tr>
    <td><b>outlet_name</b></td>
    <td>string</td>
    <td>Outlet name</td>
  </tr>
  <tr>
    <td><b>building</b></td>
    <td>string</td>
    <td>Name of the building the outlet is located</td>
  </tr>
  <tr>
    <td><b>logo</b></td>
    <td>string</td>
    <td>URL of the ouetlet logo (size varies)</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Location latitude coordinate</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Location longitude coordinate</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Location blurb</td>
  </tr>
  <tr>
    <td><b>notice</b></td>
    <td>string</td>
    <td>Outlet specific anouncements</td>
  </tr>
  <tr>
    <td><b>is_open_now</b></td>
    <td>boolean</td>
    <td>Predicts if the location is currently open by taking the current time into account</td>
  </tr>
  <tr>
    <td><b>opening_hours</b></td>
    <td>object</td>
    <td>Weekly operating hours data<br><table>
  <tr>
    <td><b>{day_of_the_week}</b></td>
    <td>object</td>
    <td>Hours for all days of the week<br><table>
  <tr>
    <td><b>opening_hour</b></td>
    <td>time</td>
    <td>Locationns opening time (H:i format)</td>
  </tr>
  <tr>
    <td><b>closing_hour</b></td>
    <td>time</td>
    <td>Location's closing time (H:i format)</td>
  </tr>
  <tr>
    <td><b>is_closed</b></td>
    <td>boolean</td>
    <td>If the location is closed on that day</td>
  </tr>
</table>
</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>special_hours</b></td>
    <td>list</td>
    <td>Special cases for operating hours<br><table>
  <tr>
    <td><b>date</b></td>
    <td>date</td>
    <td>Y-m-d format date for the special case</td>
  </tr>
  <tr>
    <td><b>opening_hour</b></td>
    <td>time</td>
    <td>Location's opening time (H:i format)</td>
  </tr>
  <tr>
    <td><b>closing_hour</b></td>
    <td>time</td>
    <td>Location's closing time (H:i format)</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>dates_closed</b></td>
    <td>list</td>
    <td>Y-m-d format list of dates the outlet is closed</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":158,
    "timestamp":1383683002,
    "status":200,
    "message":"Request successful",
    "method_id":1381,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "outlet_id":3,
      "outlet_name":"Bon App\u00e9tit - Davis Centre",
      "building":"DC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/BA.gif",
      "latitude":43.472839,
      "longitude":-80.543185,
      "description":"Bon App\u00e9tit offers fantastic Chinese food, salads, fruit, beverages, soup, and grill items. Check out the new Waterloo Burger Company featuring a 12oz sirloin burger and loaded fries.",
      "notice":"Chopsticks opens at 10:30am, Jolly Chef at 11am.",
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"10:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"10:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"10:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"10:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"10:30",
          "closing_hour":"14:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":20,
      "outlet_name":"Browsers Caf\u00e9 - Dana Porter Library",
      "building":"DP",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/browsers.gif",
      "latitude":43.469665,
      "longitude":-80.542338,
      "description":"Come and taste our exclusive new coffee roasts from freshly ground Baden Coffee Co. beans.\r\nA selection of pastries, grab n&rsquo; go items, and hot and cold beverages will satisfy your thirst and hungry tummy while you&rsquo;re browsing the books.",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":"11:30",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"11:30",
          "closing_hour":"16:30",
          "is_closed":false
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Tim Hortons - Student Life Centre",
      "building":"SLC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/tims.gif",
      "latitude":43.471324,
      "longitude":-80.545186,
      "description":null,
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":"10:30",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"07:30",
          "closing_hour":"23:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"07:30",
          "closing_hour":"23:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"07:30",
          "closing_hour":"23:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"07:30",
          "closing_hour":"23:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"07:30",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"10:30",
          "closing_hour":"21:00",
          "is_closed":false
        }
      },
      "special_hours":[
        {
          "date":"2013-11-02",
          "opening_hour":"08:30",
          "closing_hour":"21:00"
        }
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"ML\u2019s Coffee Shop - Modern Languages",
      "building":"ML",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/mls.jpg",
      "latitude":43.468897,
      "longitude":-80.542724,
      "description":"Famous for its diner-style menu, ML&rsquo;s will lure your taste buds.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"14:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"14:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"14:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"14:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":1,
      "outlet_name":"Brubakers - Student Life Centre",
      "building":"SLC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/brubakers.gif",
      "latitude":43.472037,
      "longitude":-80.54542,
      "description":"We&rsquo;ve got something for everyone under one roof! You can choose from Pita Pit,&nbsp; Pizza Pizza, Made in Japan Teriyaki, Wild Olive Pasta Bar, Booster Juice, Freestyle Coke Machine, Grab n&rsquo; Go, and lots more.",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        {
          "date":"2013-11-02",
          "opening_hour":"10:30",
          "closing_hour":"15:00"
        }
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Subway - Student Life Centre",
      "building":"SLC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/subway.gif",
      "latitude":43.472138,
      "longitude":-80.545219,
      "description":"Located beside Brubakers.",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"19:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"19:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"19:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"19:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
          "closing_hour":"19:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        {
          "date":"2013-11-02",
          "opening_hour":"11:00",
          "closing_hour":"16:00"
        }
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"CEIT Caf\u00e9 - CEIT Building",
      "building":"EIT",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/ceit.gif",
      "latitude":43.471713,
      "longitude":-80.542231,
      "description":"Look for us under the dinosaur &ndash; we&rsquo;ll be ready to serve you from our selection of fresh pastries, hot soup, specialty beverages, and grab n&rsquo; go foods.",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":21,
      "outlet_name":"Eye Opener Caf\u00e9 - Optometry Building",
      "building":"OPT",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/eye_opener.gif",
      "latitude":43.475552,
      "longitude":-80.545455,
      "description":"Visit our cafe and try one of our Panino sandwiches or start your day off right with a fresh-ground, house blend, coffee.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":25,
      "outlet_name":"Liquid Assets Cafe - Hagey Hall",
      "building":"HH",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/la.gif",
      "latitude":43.468541,
      "longitude":-80.5417,
      "description":"Serving a mix of Asian and Indian noodle bowls and salads. As well as fresh coffee, pastries and Grab n&#39; Go items.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Williams Fresh Cafe - Environment 3",
      "building":"EV3",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/williams_0.gif",
      "latitude":43.468202,
      "longitude":-80.543561,
      "description":null,
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:30",
          "closing_hour":"18:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:30",
          "closing_hour":"18:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:30",
          "closing_hour":"18:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:30",
          "closing_hour":"18:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":6,
      "outlet_name":"Festival Fare - above the Bookstore in South Campus Hall",
      "building":"SCH",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/festivalfare.gif",
      "latitude":43.469222,
      "longitude":-80.54036,
      "description":"A hot entr\u00e9e is available every day and weekly specialty menu items will make this one of your hot spots. It&#39;s one of our best kept secrets! Shhh, don&#39;t tell anyone.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"11:00",
          "closing_hour":"13:45",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"11:00",
          "closing_hour":"13:45",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"11:00",
          "closing_hour":"13:45",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"11:00",
          "closing_hour":"13:45",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"11:00",
          "closing_hour":"13:45",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":5,
      "outlet_name":"Mudie\u2019s - Village 1",
      "building":"V1",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/mudie%27s.gif",
      "latitude":43.471582,
      "longitude":-80.549741,
      "description":"This is a great place to meet your friends! The aroma of fresh baked breads and pastries from our in-house UW Bakery will surely make you take a deep breath. Mudie&rsquo;s offers a large selection of vegetarian foods, grab n&rsquo; go items, salad bar, grill items, made-to-order deli sandwiches and pitas, full breakfast, and convenience foods. A hot entr\u00e9e item and side dishes are available every lunch and dinner hour.",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":"08:00",
          "closing_hour":"00:30",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"07:00",
          "closing_hour":"00:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"07:00",
          "closing_hour":"00:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"07:00",
          "closing_hour":"00:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"07:00",
          "closing_hour":"00:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"07:00",
          "closing_hour":"00:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"08:00",
          "closing_hour":"00:30",
          "is_closed":false
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":22,
      "outlet_name":"PAS Lounge - PAS Building",
      "building":"PAS",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/pas.gif",
      "latitude":43.467077,
      "longitude":-80.5427,
      "description":"Located on the 3rd floor, we offer an assortment of fresh pastries, grab n&rsquo; go items, soup, salads, and sandwiches.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":23,
      "outlet_name":"Pastry Plus - B. C. Matthews Hall",
      "building":"BMH",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/pastryplus.gif",
      "latitude":43.473559,
      "longitude":-80.545648,
      "description":"Although we&rsquo;re small and tucked away &ndash; we offer pastries, hot and cold beverages, soup, and grab n&rsquo; go items for a quick &ldquo;pick-me-up&rdquo; between classes.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:15",
          "closing_hour":"13:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:15",
          "closing_hour":"13:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:15",
          "closing_hour":"13:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:15",
          "closing_hour":"13:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:15",
          "closing_hour":"13:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":23,
      "outlet_name":"Pastry Plus - Needles Hall",
      "building":"NH",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/pastryplus_0.gif",
      "latitude":43.469578,
      "longitude":-80.543599,
      "description":"To save you time, we have grab n&rsquo; go sandwiches, soup, fresh pastries, hot and cold beverages, and convenience items.",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"07:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"07:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"07:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"07:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"07:30",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":23,
      "outlet_name":"Pastry Plus - Tatham Centre",
      "building":"TC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/pastryplus_1.gif",
      "latitude":43.468842,
      "longitude":-80.541171,
      "description":"Open during employer interviews; look for us behind the paging counter. Our selection of snacking foods will invigorate you for your interview.",
      "notice":"Open during employer interviews only.",
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "tuesday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "wednesday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "thursday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "friday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":7,
      "outlet_name":"REVelation - Ron Eydt Village",
      "building":"REV",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/revelation.gif",
      "latitude":43.470296,
      "longitude":-80.554306,
      "description":"Meet your friends and have a fantastic meal at the same time. Our stir-fry meals will entice your taste buds, made-to-order deli sandwiches will be hard to resist, fantastic hot entr\u00e9es will lure you, and a great full breakfast will get your day off to a great start. A vegetarian hot entr\u00e9e is available every lunch and dinner plus there&rsquo;s a large selection of grab n&rsquo; go items to ensure you can always find something to eat.",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":"09:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"07:00",
          "closing_hour":"22:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"07:00",
          "closing_hour":"22:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"07:00",
          "closing_hour":"22:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"07:00",
          "closing_hour":"22:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"07:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"09:00",
          "closing_hour":"19:00",
          "is_closed":false
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Tim Hortons - Modern Languages",
      "building":"ML",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/tims_0.gif",
      "latitude":43.468778,
      "longitude":-80.543153,
      "description":null,
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"15:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"14:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Tim Hortons - Davis Centre",
      "building":"DC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/tims_1.gif",
      "latitude":43.472901,
      "longitude":-80.542992,
      "description":null,
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"07:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"07:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"07:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"07:30",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"07:30",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Tim Hortons - South Campus Hall",
      "building":"SCH",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/tims_2.gif",
      "latitude":43.469183,
      "longitude":-80.540133,
      "description":null,
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"19:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"16:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        {
          "date":"2013-11-02",
          "opening_hour":"09:30",
          "closing_hour":"14:00"
        }
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"University Club",
      "building":"UC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/university-club.gif",
      "latitude":43.472272,
      "longitude":-80.54745,
      "description":"Good food - good times - visit the Club.\r\nReservations recommended.\r\n\tPlease call 888-4567 extension 33801\r\n\t\r\n\tVisit the University Club website to view our daily menu and see what theme events we have happening\r\n\t\r\n\t(WATCARD discounts do not apply at the University Club)",
      "notice":null,
      "is_open_now":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"11:30",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"11:30",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"11:30",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"11:30",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"11:30",
          "closing_hour":"14:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"UW Food Services Administrative Office",
      "building":"UW Food Services Administrative Office",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/foodservices.gif",
      "latitude":43.470682,
      "longitude":-80.552664,
      "description":"519-888-4567, extension 35270",
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    },
    {
      "outlet_id":null,
      "outlet_name":"Tim Hortons - Davis Centre Library",
      "building":"DC",
      "logo":"https:\/\/uwaterloo.ca\/food-services\/sites\/ca.food-services\/files\/tims_1.gif",
      "latitude":43.473115,
      "longitude":-80.542145,
      "description":null,
      "notice":null,
      "is_open_now":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"15:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
          "closing_hour":"18:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ]
    }
  ]
}
```


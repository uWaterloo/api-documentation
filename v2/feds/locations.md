# FEDS Locations and Hours

```
GET /feds/locations.{format}
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
    <td>1721</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>feds</td>
    <td><b>Service ID</b></td>
    <td>311</td>
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

- http://www.feds.ca/operations/


## Parameters

```
GET /feds/locations.{format}
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
GET /feds/locations.{format}
```

- **http://api.uwaterloo.ca/v2/feds/locations.json**
- **http://api.uwaterloo.ca/v2/feds/locations.xml**
- **http://api.uwaterloo.ca/v2/feds/locations.json?callback=myResponse**


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
    <td>Outlet ID number (not always same as outlets.json method). Can be null</td>
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
    <td>URL of the outlet logo (size varies)</td>
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
    <td>Outlet-specific announcements</td>
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
    <td>Location's opening time (H:i format)</td>
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
  <tr>
    <td><b>additional</b></td>
    <td>object</td>
    <td>Key values for any additional data<br><table>
  <tr>
    <td><b>menu_url</b></td>
    <td>string</td>
    <td>URL of the menu, if available</td>
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
    "requests":811353,
    "timestamp":1453149199,
    "status":200,
    "message":"Request successful",
    "method_id":1721,
    "method":{
      
    }
  },
  "data":[
    {
      "outlet_id":1,
      "outlet_name":"The Bombshelter Pub",
      "building":"SLC",
      "logo":null,
      "latitude":43.471476,
      "longitude":-80.544893,
      "description":"The Bombshelter Pub, or as it\u2019s more affectionately known, The Bomber, is the ultimate hang-out on campus!\n\nCome out every Wednesday to one of the longest running bar nights in KW hosted by your very own Federation of Students!",
      "notice":"The Bombshelter Pub will be open for lunch from Dec 14th to the 18th from 11am to 3pm. Every table of 8 gets two free apps!",
      "is_open_now":true,
      "is_24hrs":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"10:00",
          "closing_hour":"20:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"10:00",
          "closing_hour":"01:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"10:00",
          "closing_hour":"02:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"10:00",
          "closing_hour":"23:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"10:00",
          "closing_hour":"20:00",
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
        "2015-12-19",
        "2015-12-20",
        "2015-12-21",
        "2015-12-22",
        "2015-12-23",
        "2015-12-24",
        "2015-12-25",
        "2015-12-26",
        "2015-12-27",
        "2015-12-28",
        "2015-12-29",
        "2015-12-30",
        "2015-12-31",
        "2016-01-01",
        "2016-01-02",
        "2016-01-03"
      ],
      "additional":{
        "menu_url":"http:\/\/www.feds.ca\/wp-content\/blogs.dir\/57\/files\/2012\/08\/Bomber-Menu-Fall-2014-v7-small-size.pdf"
      }
    },
    {
      "outlet_id":2,
      "outlet_name":"The Dispensary",
      "building":"PHR",
      "logo":null,
      "latitude":43.452631,
      "longitude":-80.4988,
      "description":"Located on the main level of the University of Waterloo\u2019s Pharmacy building, The Dispensary is a wonderful place to meet with friends, grab a quick bite to eat or simply relax after a hard day of school. What are you waiting for? Grab yourself a cup of fair trade coffee, cappuccino or one of the many assorted fair trade teas the Dispensary has on the menu. There, you will also find various Grab\u2019N\u2019Go items including:\n\nFreshly made sandwiches*\n\tFreshly made salads*\n\tBagels, donuts, croissants\n\tFreshly baked muffins and cookies\n\tAssorted summer fresh pasta and grain salads\n\tFour different hot entr\u00e9es* daily\n*The Dispensary uses biodegradable containers for its sandwiches, salads and hot entr\u00e9es.",
      "notice":null,
      "is_open_now":true,
      "is_24hrs":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"08:00",
          "closing_hour":"17:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"08:00",
          "closing_hour":"17:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"08:00",
          "closing_hour":"17:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"08:00",
          "closing_hour":"17:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"08:00",
          "closing_hour":"13:00",
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
        
      ],
      "additional":{
        "menu_url":null
      }
    },
    {
      "outlet_id":3,
      "outlet_name":"International News",
      "building":"SLC",
      "logo":null,
      "latitude":43.471433,
      "longitude":-80.545149,
      "description":"A Federation of Students\u2019 commercial service, International News is the on-campus convenience store at the University of Waterloo. It recently replaced Federation Xpress, which served students from 2008 to 2012. International News offers a wide range of products at student-friendly prices including snacks, grab and go items, lottery tickets, beverages, and more.",
      "notice":"We will be closed on December 22, 2015 at 11 p.m. and re-open on January 4, 2016 at 6 a.m",
      "is_open_now":true,
      "is_24hrs":true,
      "opening_hours":{
        "sunday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"00:00",
          "closing_hour":"23:59",
          "is_closed":false
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        "2015-12-23",
        "2015-12-24",
        "2015-12-25",
        "2015-12-26",
        "2015-12-27",
        "2015-12-28",
        "2015-12-29",
        "2015-12-30",
        "2015-12-31",
        "2016-01-01",
        "2016-01-02",
        "2016-01-03"
      ],
      "additional":{
        "menu_url":null
      }
    },
    {
      "outlet_id":4,
      "outlet_name":"Bento Sushi",
      "building":"SLC",
      "logo":null,
      "latitude":43.471541,
      "longitude":-80.544806,
      "description":"Bento Sushi\u00a0is the Feds' own sushi bar! Assorted varieties of sushi are made fresh daily and all at student-friendly prices! Drop by and give sushi a try.",
      "notice":"Bento Sushi will operate on shortened hours starting December 7 to 18 from 10 a.m. to 5 p.m",
      "is_open_now":true,
      "is_24hrs":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"10:00",
          "closing_hour":"17:00",
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
        "2015-12-19",
        "2015-12-20",
        "2015-12-21",
        "2015-12-22",
        "2015-12-23",
        "2015-12-24",
        "2015-12-25",
        "2015-12-26",
        "2015-12-27",
        "2015-12-28",
        "2015-12-29",
        "2015-12-30",
        "2015-12-31",
        "2016-01-01",
        "2016-01-02",
        "2016-01-03"
      ],
      "additional":{
        "menu_url":null
      }
    },
    {
      "outlet_id":5,
      "outlet_name":"Campus Bubble",
      "building":"SLC",
      "logo":null,
      "latitude":43.471446,
      "longitude":-80.54502,
      "description":"Campus Bubble is the place on campus to grab bubble tea! It has an exciting menu with a wide variety of choices including milk tea, bubble tea and fresh fruit smoothies.\n\nStop by and try all of the flavours!",
      "notice":"Campus Bubble will operate on shortened hours starting December 7 to 18 from 10 a.m. to 5 p.m.",
      "is_open_now":true,
      "is_24hrs":false,
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"10:00",
          "closing_hour":"21:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"10:00",
          "closing_hour":"17:00",
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
        "2015-12-19",
        "2015-12-20",
        "2015-12-21",
        "2015-12-22",
        "2015-12-23",
        "2015-12-24",
        "2015-12-25",
        "2015-12-26",
        "2015-12-27",
        "2015-12-28",
        "2015-12-29",
        "2015-12-30",
        "2015-12-31",
        "2016-01-01",
        "2016-01-02",
        "2016-01-03",
        "2016-01-04"
      ],
      "additional":{
        "menu_url":"https:\/\/www.facebook.com\/CampusBubble"
      }
    }
  ]
}
```


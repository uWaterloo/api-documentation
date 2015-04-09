# Get Services for Site

```
GET /v2/services/[site].{format}
```

## Description

> This method returns a sites associated services.

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
    <td>1787</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>services</td>
    <td><b>Service ID</b></td>
    <td>331</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Each individual site's data steward</td>
    <td><b>Data Type</b></td>
    <td>Proxy via WCMS</td>
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
- If you find issues with the data, submit a request [here](https://rt.uwaterloo.ca/SelfService/Forms/IST-General/).
- Any value can be `null`


### Sources

- https://uwaterloo.ca/[site]/services


## Parameters

```
GET /v2/services/[site].{format}
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
    <td><b>site</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid site slug from /resources/sites</td>
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
GET /v2/services/[site].{format}
```

- **http://api.uwaterloo.ca/v2/services/arts-computing.json**
- **http://api.uwaterloo.ca/v2/services/arts-computing.xml**
- **http://api.uwaterloo.ca/v2/services/arts-computing.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Service ID number. Can be null</td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Service name</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Description of service</td>
  </tr>
  <tr>
    <td><b>cost</b></td>
    <td>string</td>
    <td>Description of cost of service</td>
  </tr>
  <tr>
    <td><b>is_open_now</b></td>
    <td>boolean</td>
    <td>Predicts if the location is currently open by taking the current time into account</td>
  </tr>
  <tr>
    <td><b>contact_information</b></td>
    <td>string</td>
    <td>Free form text regarding who to contact for service</td>
  </tr>
  <tr>
    <td><b>notice</b></td>
    <td>string</td>
    <td>Service-specific announcements</td>
  </tr>
  <tr>
    <td><b>services_available</b></td>
    <td>list</td>
    <td>List of services available</td>
  </tr>
  <tr>
    <td><b>request_info</b></td>
    <td>object</td>
    <td>Information on how to request the service<br><table>
  <tr>
    <td><b>procedure</b></td>
    <td>string</td>
    <td>Procedure for requesting the service</td>
  </tr>
  <tr>
    <td><b>completion_time</b></td>
    <td>string</td>
    <td>Information about how long it take for a service to be completed</td>
  </tr>
  <tr>
    <td><b>minimum_notice</b></td>
    <td>string</td>
    <td>Information about lead time required for a service to be completed</td>
  </tr>
</table>
</td>
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
    <td>Service's opening time (H:i format)</td>
  </tr>
  <tr>
    <td><b>closing_hour</b></td>
    <td>time</td>
    <td>Service's closing time (H:i format)</td>
  </tr>
  <tr>
    <td><b>is_closed</b></td>
    <td>boolean</td>
    <td>If the service is not operating on that day</td>
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
    <td>Special cases for service hours<br><table>
  <tr>
    <td><b>date</b></td>
    <td>date</td>
    <td>Y-m-d format date for the special case</td>
  </tr>
  <tr>
    <td><b>opening_hour</b></td>
    <td>time</td>
    <td>Service's opening time (H:i format)</td>
  </tr>
  <tr>
    <td><b>closing_hour</b></td>
    <td>time</td>
    <td>Service's closing time (H:i format)</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>dates_closed</b></td>
    <td>list</td>
    <td>Y-m-d format list of dates the service is nonoperational</td>
  </tr>
  <tr>
    <td><b>location</b></td>
    <td>object</td>
    <td>Location of service delivery<br><table>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Unique id of location</td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Name of location</td>
  </tr>
  <tr>
    <td><b>street</b></td>
    <td>string</td>
    <td>Street address of location</td>
  </tr>
  <tr>
    <td><b>additional</b></td>
    <td>string</td>
    <td>Additional information regarding street address of location</td>
  </tr>
  <tr>
    <td><b>city</b></td>
    <td>string</td>
    <td>Name of city</td>
  </tr>
  <tr>
    <td><b>province</b></td>
    <td>string</td>
    <td>Name of province in two-letter short form</td>
  </tr>
  <tr>
    <td><b>postal_code</b></td>
    <td>string</td>
    <td>Postal code "in L#L #L#" format</td>
  </tr>
  <tr>
    <td><b>country</b></td>
    <td>string</td>
    <td>Full name of country</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>number</td>
    <td>Service location latitude</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>number</td>
    <td>Service location longitude</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>category</b></td>
    <td>string</td>
    <td>Categories related to service</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>list</td>
    <td>Audience targeted by service</td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Full site name as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>site_id</b></td>
    <td>string</td>
    <td>Site slug as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>revision_id</b></td>
    <td>integer</td>
    <td>Unique id of revision of service</td>
  </tr>
  <tr>
    <td><b>additional</b></td>
    <td>string</td>
    <td>Additional information about service</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>URL of service link</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>date</td>
    <td>ISO 8601 formatted updated date</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":396259,
    "timestamp":1428525351,
    "status":200,
    "message":"Request successful",
    "method_id":1787,
    "method":{
      
    }
  },
  "data":[
    {
      "id":291,
      "name":"Printing",
      "description":"Publicly accessible printing services are available for students at the Stratford campus, in PAS 1099 and in the AL lobby using the campus uPrint system We also support graduate student and departmental staff and faculty printing in their areas Read more about printing in the Faculty of Arts",
      "cost":"No charge for printing setup and supportPrinting costs and locations for uPrint",
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Contact the Arts Computing Office (ACO)Staff and faculty may also contact their department's ACO support person",
        "completion_time":"Varies based on request",
        "minimum_notice":"1 business day"
      },
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
        
      ],
      "location":{
        "id":195,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Printing and scanning"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2348,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/printing",
      "updated":"2015-03-05T10:00:54-05:00"
    },
    {
      "id":292,
      "name":"Purchasing advice for faculty and staff",
      "description":"All computing and related equipment purchases in Arts are handled by Arts Computing We strongly recommend that faculty and staff in the Faculty of Arts consult with their ACO departmental contact concerning new computer equipment purchases including servers, printers, workstations, laptops, tablets, and related peripheral equipment and accessories When preparing grant applications that involve technology purchases, ACO staff can provide advice on the systems and software that will best suit your research needs for the length of the project",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Purchases All computing and related equipment purchases in Arts are handled by Barb YanthaPurchasing advice Please consult with your ACO departmental contact",
        "completion_time":null,
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":249,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Printing and scanning"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2490,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/purchasing-advice-faculty-and-staff",
      "updated":"2015-03-18T13:58:38-04:00"
    },
    {
      "id":293,
      "name":"Software for labs and courses",
      "description":"Standard software is installed in Arts Faculty labs Software available on WindowsLocations PsychologyAnthropologySociology (PAS) rooms 1237, 1080 and 1098Software available on MacsLocations PAS 1098, ECH 1205 lab, Stratford campusIf you require additional software for a course to be installed in a lab, see our service on requesting additional lab software",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":"Most labs (with the exception of PAS1237) are open 24 hours lab hours vary by lab",
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
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
        
      ],
      "location":{
        "id":213,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Software"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2399,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/software-labs-and-courses",
      "updated":"2015-03-18T10:27:06-04:00"
    },
    {
      "id":294,
      "name":"Requesting additional lab software for courses",
      "description":"Faculty members and lecturers may request the installation additional software on public or specialty labs, if arranged in advance with the Arts Computing Office Instructors are expected to test the software before it is made generally available See the list of current software available in public labs",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Obtain a legal license to publish a copy of the software on the Waterloo Nexus network from the softwareu2019s vendorPlease contact Scott Paterson oru00a0Nevil Bromley (Windows software), Herbert Balagtas or Keith McGowan (Mac software) OR contact ACOu00a0at least six weeks before the beginning of the term and include The name of the softwareThe lab(s) you would like it available inA copy of the legal licenseA copy of the software",
        "completion_time":"Will vary based on request",
        "minimum_notice":"6 weeks"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":250,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Software"
      ],
      "audience":[
        "Faculty"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2491,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/requesting-additional-lab-software-courses",
      "updated":"2015-03-18T14:00:20-04:00"
    },
    {
      "id":295,
      "name":"Lunchtime information sessions",
      "description":"Each term, the Arts Computing Office hosts a lunchtime session for staff in the Faculty of Arts Topics include information on new technology and upcoming changes andor current timely computing information Past lunchtime session presentations are available for viewing",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        "Termly lunchtime information session for staff"
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
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
        
      ],
      "location":{
        "id":204,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Training"
      ],
      "audience":[
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2378,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/lunchtime-information-sessions",
      "updated":"2015-03-18T10:25:06-04:00"
    },
    {
      "id":296,
      "name":"One on one consultation",
      "description":"Personalized consulting on computing issues related to oncampus activities, including Assistance with setupconfiguration of oncampus resourcesHardwaresoftware purchasesSoftware training",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Contact the Arts Computing Office or staff may contact their ACO departmental contact",
        "completion_time":"Will vary based on request",
        "minimum_notice":"1 business day"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":207,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Training"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2382,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/one-one-consultation",
      "updated":"2015-03-18T10:25:56-04:00"
    },
    {
      "id":297,
      "name":"Website set up and help (WordPress)",
      "description":"Consultations for new and existing WordPress websites in the Faculty of Arts, for faculty members, projects, groups and student societies Assistance available may vary based on Arts Computing Office (ACO) resources NOTE ACO does not provide web site design or maintenance Website content maintenance is the responsibility of the departmentindividualWeb accessibility is a requirement Training is available through IST's Skills for the Electronic Workplace (SEW) program",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Contact the Arts Computing Office",
        "completion_time":"Will vary based on request",
        "minimum_notice":"2+ weeks"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":215,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Web services"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2402,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/website-set-and-help-wordpress",
      "updated":"2015-03-18T10:26:29-04:00"
    },
    {
      "id":298,
      "name":"Waterloo CMS support and help",
      "description":"Consultations for new and existing WCMS websites in the Faculty of Arts, including Assistance with departmental WCMS sites and accessibilityConsulting and web services for research and other needsMigration from old web services to UW supported web servicesAssistance available may vary based on the website and Arts Computing Office (ACO) resources NOTE ACO does not provide website design or maintenance Website content maintenance is the responsibility of the departmentindividual Permission to WCMS system is a requirement to edit web pages and is granted following WCMS training Training is available through IST's Skills for the Electronic Workplace (SEW) program",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Contact the Arts Computing Office",
        "completion_time":"Will vary based on request",
        "minimum_notice":"1 business day"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":218,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Web services"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2432,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/waterloo-cms-support-and-help",
      "updated":"2015-03-18T10:26:51-04:00"
    },
    {
      "id":299,
      "name":"Software for faculty and staff",
      "description":"Support for all software that is installed on Arts faculty computers, as well as for licensed software within departments This includes facilitating the purchase and deployment of specialized software for staff and faculty, as needed",
      "cost":"Software support is free of chargeAdditionalspecialized software costs will vary See the list for Licensed software at the University of Waterloo",
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"For software support, contact the Arts Computing OfficeFor software purchases contact Barb Yantha",
        "completion_time":"Will vary based on request",
        "minimum_notice":"Will vary based on request"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":246,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Software"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2487,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/software-faculty-and-staff",
      "updated":"2015-03-18T13:43:57-04:00"
    },
    {
      "id":300,
      "name":"Lab bookings",
      "description":"Some computing labs in the Faculty of Arts may be booked for Arts faculty needs such as classes, research, or other university functions The following labs are available to be booked PsychologyAnthropologySociology (PAS) 1237East Campus Hall (ECH) 1205Modern Languages (ML) 109, and ML 113See our available software page for information on software available in each lab The labs located in ML are only available for booking by Language instructors ECH 1205 is only available for booking by Fine Arts, English, or Digital Arts Communication instructors",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        "Mac computer lab (ECH 1205)",
        "PC computer labs (PAS 1237, ML 109 & 113)"
      ],
      "request_info":{
        "procedure":"ECHu00a01205u00a0can be booked byu00a0emailingu00a0Sharonu00a0Dahmer View theu00a0ECHu00a01205 scheduleu00a0for booking availabilityu00a0 ML 109 and ML 113u00a0can be booked by contactingu00a0Toddu00a0MarshallTayloru00a0View theu00a0Languageu00a0Lab scheduleu00a0for booking availabilityPASu00a01237u00a0can be booked by contactingu00a0Barb Yanthau00a0View theu00a0PASu00a01237 Scheduleu00a0for booking availability",
        "completion_time":"As soon as possible",
        "minimum_notice":"Will vary based on schedule and lab"
      },
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
        
      ],
      "location":{
        "id":null,
        "name":null,
        "street":null,
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":null,
        "latitude":null,
        "longitude":null
      },
      "category":[
        "Labs"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2371,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/lab-bookings",
      "updated":"2015-03-18T10:22:37-04:00"
    },
    {
      "id":301,
      "name":"Lab facilities and software for undergraduate students",
      "description":"Public labs with both Mac and PC computers are available for use by all undergraduate Arts students See our available software page for information on what is available on our lab computers Public labsWindows 7 Arts Lecture Hall (AL) Thin Clients PsychologyAnthropologySociology (PAS) 1080, 1098, 1099, and 1237 Mac OS East Campus Hall (ECH) 1205 PAS 1098 Hours All labs are are open 247 with the exception of PAS 1237 and ECH 1205, which are available from 900 am430 pm Booking These labs may be booked for classes availability for public use is subject to booking schedules",
      "cost":null,
      "is_open_now":true,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":"Available on a firstcome, firstserved basis"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ],
      "location":{
        "id":null,
        "name":null,
        "street":null,
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":null,
        "latitude":null,
        "longitude":null
      },
      "category":[
        "Software"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2374,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/lab-facilities-and-software-undergraduate-students",
      "updated":"2015-03-18T10:24:44-04:00"
    },
    {
      "id":302,
      "name":"Nexus and email login issues",
      "description":"Support for all questions and concerns with Nexus, WatIAM and campus email accounts This includes problems logging in to any of these services WatIAM (Account used for Quest, Nexus, LEARN, etc)If you have forgotten your WatIAM password, you can reset it at the WatIAM login page by clicking Forgot Password (WatIAM credentials are used for all of Eduroam (wireless), Quest, Jobmine, LEARN, myHRinfo, Nexus, and more) Note If you require a WatIAM account reset due to login difficulties, you must present photo ID in person to ACO Help Desk staff Nexus accountsYour Nexus account allows you to log into any Nexus machine by using your WatIAM credentials All Nexus accounts include 1GB of personal disk space, and access to software on Nexus machine including Microsoft Office More about Nexus If you are having difficulty logging in, see our help page on logging into Nexus, or our Nexus and email login issues service For information on accessing your Nexus account from home, see our computing from home service",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Phone (519)u00a08884567u00a0extu00a033190Email acohelpuwaterloocaOffice location PAS 1077Live chatu00a0",
        "completion_time":"Will vary based on request",
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":206,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":"1077",
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "General computing help"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Future undergraduate students",
        "Current graduate students",
        "Future graduate students",
        "Future students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2381,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/nexus-and-email-login-issues",
      "updated":"2015-03-18T10:25:36-04:00"
    },
    {
      "id":303,
      "name":"Wireless network assistance",
      "description":"Eduroam wireless network support and assistance In order to connect to eduroam, you must select eduroam from your list of WiFi networks available and enter your useriduwaterlooca along with your WatIAM password If you have difficulties getting connected, the eduroam Configuration Assistant Tool (CAT) fixes most connection issues Visit Information Systems & Technology's (IST) documentation for using the CAT NOTE If you have recently changed your WatIAM password, you must reauthenticate eduroam with the new password in order to access eduroam",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Phone (519)u00a08884567u00a0extu00a033190Email acohelpuwaterloocaOffice location PAS 1077Live chat",
        "completion_time":"Will vary based on request",
        "minimum_notice":"Will vary based on request"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":217,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":"1077",
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "General computing help"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2405,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/wireless-network-assistance",
      "updated":"2015-03-18T10:26:39-04:00"
    },
    {
      "id":304,
      "name":"Other campus IT services",
      "description":"Additional resources for you to get help are available at various locations across campus ResourcesInformation Systems & Technology's (IST) Service Desk Afterhours and weekend computing help available at the Davis Center Service DeskSpecialised printing services Contact mediadocOther online resources IST's website",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
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
        
      ],
      "location":{
        "id":null,
        "name":null,
        "street":null,
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":null,
        "latitude":null,
        "longitude":null
      },
      "category":[
        "General computing help"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Future undergraduate students",
        "Current graduate students",
        "Future graduate students",
        "Future students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2384,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/other-campus-it-services",
      "updated":"2015-03-18T10:26:10-04:00"
    },
    {
      "id":305,
      "name":"Computing from home",
      "description":"Support and assistance for faculty, staff and students who need to connect to campus IT resources from off campus ResourcesAccess your email from homeAccess your Nexus 'N' drive from homeInformation Systems & Technology's instructions on setting up a remote desktop for Windows machinesCampus VPN instructions",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Phone (519)u00a08884567u00a0extu00a033190Email acohelpuwaterloocaOffice location PAS 1077Live chat",
        "completion_time":"Will vary based on request",
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":241,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":"1077",
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "General computing help"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2481,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/computing-home",
      "updated":"2015-03-18T13:23:13-04:00"
    },
    {
      "id":306,
      "name":"Arts Computing Office (ACO) Help Desk",
      "description":"Provide faculty, staff, and students in the Faculty of Arts with IT help and support ACO Help Desk services include Software helpGeneral troubleshootingWireless assistancePrinting and scanningLogin issuesDesktop and laptop supportWCMS assistanceAnd more!",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":"Closed for departmental meetings (9301030 on the 2nd and 4th Thursday of the month) and occasional ACO events",
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Phone at (519)u00a08884567u00a0extu00a033190Email at acohelpuwaterloocaRequest FormLive chatVisit us in PAS 1077",
        "completion_time":"Will vary based on request",
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":237,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":"1077",
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Printing and scanning"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2452,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/arts-computing-office-aco-help-desk",
      "updated":"2015-03-18T10:21:19-04:00"
    },
    {
      "id":307,
      "name":"Lab facilities and software for graduate students",
      "description":"Graduate students have a number of options when it comes to finding a place to work Along with having access to all undergraduate lab facilities, they may also have lab facilities available in their departments",
      "cost":null,
      "is_open_now":true,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "monday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        },
        "saturday":{
          "opening_hour":"00:00",
          "closing_hour":"00:00",
          "is_closed":false
        }
      },
      "special_hours":[
        
      ],
      "dates_closed":[
        
      ],
      "location":{
        "id":null,
        "name":null,
        "street":null,
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":null,
        "latitude":null,
        "longitude":null
      },
      "category":[
        "Software"
      ],
      "audience":[
        "Current students",
        "Current graduate students"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2439,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/lab-facilities-and-software-graduate-students",
      "updated":"2015-03-18T10:22:49-04:00"
    },
    {
      "id":308,
      "name":"Scanning and copying",
      "description":"For student convenience, there are scanners and copiers located in Psychology, Anthropology, Sociology (PAS) for general use Scanning There is one Microtrek Scanmaker X6 EL available in PAS 1099 Instructions for its use are posted on the wall next to it CopyingA photocopier is available in PAS 1099 It requires a WatCard with sufficient funds You can add money to your WatCard online or visit at any Food Services location, Graphics Copy Centre, the Turnkey Desk, or the WatCard office",
      "cost":"To use the copier, you must have sufficient funds on your WatCard",
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
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
        
      ],
      "location":{
        "id":209,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Printing and scanning"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2389,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/scanning-and-copying",
      "updated":"2015-03-18T10:28:06-04:00"
    },
    {
      "id":309,
      "name":"Laptop loans",
      "description":"Provision of loaner laptops for up to two business days for universityrelated purposes",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Contact Barb Yantha of the Arts Computing Office to request a loaner laptop",
        "completion_time":"Will vary based on availability",
        "minimum_notice":"2 business days"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":203,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Desktop and laptop support"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2376,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/laptop-loans",
      "updated":"2015-03-18T10:24:54-04:00"
    },
    {
      "id":310,
      "name":"Desktop rollover program",
      "description":"A desktop computer rollover program for Arts faculty and staff to ensure that faculty and staff have up to date computer equipment Arts staff and faculty with ongoing appointments are eligible for new desktop computers on a rolling basisSessional lecturers and other nonstudent employees will be provided with computers sufficient to their needs for the length of their appointment",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"The Arts Computing Office will contact faculty and staff when they are eligible for a new computer, which occurs approximately once every 4 years",
        "completion_time":null,
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":244,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Desktop and laptop support"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2485,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/desktop-rollover-program",
      "updated":"2015-03-18T13:36:27-04:00"
    },
    {
      "id":311,
      "name":"Software assistance",
      "description":"Assistance and support for the installation, setup, and use of software on universityowned computers Instructors may request installation or modification of software on public lab workstations as described here",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":248,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Software"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2489,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/software-assistance",
      "updated":"2015-03-18T13:48:57-04:00"
    },
    {
      "id":312,
      "name":"Desktop and laptop assistance",
      "description":"Assistance with departmental and personal desktop and laptop computers (eg software installation, troubleshooting issues, virusmalware removal)",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Phone (519)u00a08884567u00a0extu00a033190Email acohelpuwaterloocaOffice location PAS 1077Live chat",
        "completion_time":"Will vary based on request",
        "minimum_notice":"Will vary based on request"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":200,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "General computing help"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2367,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/desktop-and-laptop-assistance",
      "updated":"2015-03-18T10:21:53-04:00"
    },
    {
      "id":313,
      "name":"Account creation, change, removal",
      "description":"Assistance with the creation, setup, usage, and removal of computing accounts in Arts, including Nexus accountsemail and calendar accountsweb site accountsaccess to departmental or group sharesvisitors, temporary employees, and generic accountsMore information on Arts accounts including Nexus, email, calendar, web and LEARN accounts",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Consult your department support person or ask your department's administrative coordinator submit a request using our account request form (only authorized people will be able to submit this form)",
        "completion_time":"Will vary based on request",
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":240,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Computing accounts (Nexus\/email\/calendar\/mail lists)"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2480,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/account-creation-change-removal",
      "updated":"2015-03-18T13:21:32-04:00"
    },
    {
      "id":315,
      "name":"Email and calendar support",
      "description":"Support for managing your email account and calendar, as well as for suspected phishing attempts ResourcesExchangeconnect (email and calendar)Using Microsoft Outlook 2013IST's Exchange calendar pageGeneral email helpMailservices (email)Forwarding your myWaterloo emailGeneral email helpSpamphishingAvoiding spamphishing",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":null,
        "completion_time":null,
        "minimum_notice":null
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":222,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "General computing help"
      ],
      "audience":[
        "Current students",
        "Current undergraduate students",
        "Current graduate students",
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2436,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/email-and-calendar-support",
      "updated":"2015-03-18T10:22:23-04:00"
    },
    {
      "id":316,
      "name":"Mailing list setup and management",
      "description":"The Faculty of Arts creates and maintains various email lists for faculty and staff using Mailman, a webbased email list manager List owners can easily modify lists, addremove subscribers and moderate email sent to the lists",
      "cost":null,
      "is_open_now":false,
      "contact_information":"Arts Computing Office",
      "notice":null,
      "services_available":[
        
      ],
      "request_info":{
        "procedure":"Contact the Arts Computing Office",
        "completion_time":"2 business days",
        "minimum_notice":"2 business days"
      },
      "opening_hours":{
        "sunday":{
          "opening_hour":null,
          "closing_hour":null,
          "is_closed":true
        },
        "monday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "tuesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "wednesday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "thursday":{
          "opening_hour":"09:00",
          "closing_hour":"16:30",
          "is_closed":false
        },
        "friday":{
          "opening_hour":"09:00",
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
        
      ],
      "location":{
        "id":242,
        "name":"PAS - Psychology, Anthropology, Sociology",
        "street":"200 University Avenue West",
        "additional":null,
        "city":null,
        "province":null,
        "postal_code":null,
        "country":"Canada",
        "latitude":43.466995,
        "longitude":-80.542515
      },
      "category":[
        "Computing accounts (Nexus\/email\/calendar\/mail lists)"
      ],
      "audience":[
        "Faculty",
        "Staff"
      ],
      "site_name":"Arts Computing Office",
      "site_id":"arts-computing",
      "revision_id":2482,
      "additional":{
        
      },
      "link":"https:\/\/uwaterloo.ca\/arts-computing\/services\/mailing-list-setup-and-management",
      "updated":"2015-03-18T13:25:09-04:00"
    }
  ]
}
```


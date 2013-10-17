# List of Campus Printer

```
GET /resoruces/printers.{format}
```

## Description

> This method returns a list of printer on campus

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
    <td>1123</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>resources</td>
    <td><b>Service ID</b></td>
    <td>229</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Institution of Analysis & Planning (IAP)</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- This data is community curated on github
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/tree/master/Printers


## Parameters

```
GET /resoruces/printers.{format}
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
GET /resoruces/printers.{format}
```

- **https://api.uwaterloo.ca/v2/resources/printers.json**
- **https://api.uwaterloo.ca/v2/resources/printers.xml**
- **https://api.uwaterloo.ca/v2/resources/printers.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>printer</b></td>
    <td>string</td>
    <td>Name of the printer</td>
  </tr>
  <tr>
    <td><b>ad</b></td>
    <td>string</td>
    <td>Printers active directory id</td>
  </tr>
  <tr>
    <td><b>server</b></td>
    <td>string</td>
    <td>Printer server name</td>
  </tr>
  <tr>
    <td><b>comment</b></td>
    <td>string</td>
    <td>Additional comments on the printer</td>
  </tr>
  <tr>
    <td><b>driver</b></td>
    <td>string</td>
    <td>Printer driver information</td>
  </tr>
  <tr>
    <td><b>room</b></td>
    <td>string</td>
    <td>Printer's physical room location</td>
  </tr>
  <tr>
    <td><b>faculty</b></td>
    <td>string</td>
    <td>Faculty the printer belongs to</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":147,
    "timestamp":1382027585,
    "status":200,
    "message":"Request successful",
    "method_id":1123,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "printer":"deancopy",
      "ad":"CN=AHSCOSERV-deancopy;CN=ahscoserv;OU=AHSCO;OU=GROUPS;OU=AHS;OU=Domain Member Servers;DC=NEXUS;DC=UWATERLOO;DC=CA",
      "server":"AHSCOSERV",
      "comment":"Redeployed June 12; 2012",
      "driver":"Xerox Global Print Driver PCL",
      "room":"3rd Floor",
      "faculty":"AHS"
    },
    {
      "printer":"hsgprt2IP",
      "ad":"CN=AHSCOSERV-hsgprt2IP;CN=ahscoserv;OU=AHSCO;OU=GROUPS;OU=AHS;OU=Domain Member Servers;DC=NEXUS;DC=UWATERLOO;DC=CA",
      "server":"AHSCOSERV",
      "comment":"-",
      "driver":"HP LaserJet 4250 PS",
      "room":"HSG Grad",
      "faculty":"AHS"
    },
    {
      "printer":"recprt2IP",
      "ad":"CN=AHSCOSERV-recprt2IP;CN=ahscoserv;OU=AHSCO;OU=GROUPS;OU=AHS;OU=Domain Member Servers;DC=NEXUS;DC=UWATERLOO;DC=CA",
      "server":"AHSCOSERV",
      "comment":"Created June 4; 2010",
      "driver":"HP LaserJet 4250 PS",
      "room":"RLS Grad",
      "faculty":"AHS"
    },
    {
      "printer":"p_arts-mps-admin",
      "ad":"CN=NXSARTSAPP-p_arts-mps-admin;CN=NXSARTSAPP;OU=Psych has permissions;OU=Arts;OU=Domain Member Servers;DC=NEXUS;DC=UWATERLOO;DC=CA",
      "server":"NXSARTSAPP",
      "comment":"Master of Public Service - Admin Printer",
      "driver":"Xerox GPD PS V2.1",
      "room":"180 King",
      "faculty":"Arts"
    }
  ]
}
```


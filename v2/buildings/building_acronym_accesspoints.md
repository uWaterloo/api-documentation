# Building WiFi Access Points

```
GET /buildings/{building_code}/accesspoints.{format}
```

## Description

> This method returns list of all access points in that given building

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
    <td>1453</td>
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
    <td>Institution of Analysis & Planning (IAP)</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Once a day</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Lat/Long information is not available for every endpoint
- Any value can be `null`


### Sources



## Parameters

```
GET /buildings/{building_code}/accesspoints.{format}
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
GET /buildings/{building_code}/accesspoints.{format}
```

- **http://api.uwaterloo.ca/v2/buildings/MC/accesspoints.json**
- **http://api.uwaterloo.ca/v2/buildings/MC/accesspoints.xml**
- **http://api.uwaterloo.ca/v2/buildings/MHR/accesspoints.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>ap_name</b></td>
    <td>string</td>
    <td>Name of the Access Point</td>
  </tr>
  <tr>
    <td><b>aruba_ap_model</b></td>
    <td>string</td>
    <td>Model number of the Aruba AP</td>
  </tr>
  <tr>
    <td><b>ip_address</b></td>
    <td>string</td>
    <td>IP Address of the AP</td>
  </tr>
  <tr>
    <td><b>mac_address</b></td>
    <td>string</td>
    <td>MAC Address of the AP</td>
  </tr>
  <tr>
    <td><b>ssid</b></td>
    <td>string</td>
    <td>Wifi SSID of the AP</td>
  </tr>
  <tr>
    <td><b>building_code</b></td>
    <td>string</td>
    <td>Building Acronym</td>
  </tr>
  <tr>
    <td><b>mac_address_secondary</b></td>
    <td>string</td>
    <td>Secondary Address of the AP</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>AP's latitude</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>AP's longitude</td>
  </tr>
  <tr>
    <td><b>floor</b></td>
    <td>number</td>
    <td>Floor location of the API</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":789805,
    "timestamp":1451858866,
    "status":200,
    "message":"Request successful",
    "method_id":1453,
    "method":{
      
    }
  },
  "data":[
    {
      "ap_name":"AM-TRUNK-MC",
      "ssid":"",
      "ip_address":"172.16.49.67",
      "mac_address":"001A1EC546E2",
      "mac_address_secondary":"001A1ED46E20",
      "aruba_ap_model":"61",
      "latitude":null,
      "longitude":null,
      "floor":null,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"eduroam",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170AC8",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"eduroam",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170AC0",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"uw-nsd",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170ACB",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"uw-nsd",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170AC3",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"uw-nsd2",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170ACA",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"uw-nsd2",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170AC2",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"uw-unsecured",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170AC9",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1052-A",
      "ssid":"uw-unsecured",
      "ip_address":"172.16.49.4",
      "mac_address":"D8C7C8C970AC",
      "mac_address_secondary":"D8C7C8170AC1",
      "aruba_ap_model":"105",
      "latitude":43.4723466981,
      "longitude":-80.5439485105,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"eduroam",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AA8",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"eduroam",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AA0",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"uw-nsd",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AAB",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"uw-nsd",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AA3",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"uw-nsd2",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AAA",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"uw-nsd2",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AA2",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"uw-unsecured",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AA9",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    },
    {
      "ap_name":"AS-AP-MC-1056-A",
      "ssid":"uw-unsecured",
      "ip_address":"172.16.49.5",
      "mac_address":"D8C7C8C970AA",
      "mac_address_secondary":"D8C7C8170AA1",
      "aruba_ap_model":"105",
      "latitude":43.4722807293,
      "longitude":-80.5441428619,
      "floor":1,
      "building_code":"MC"
    }
  ]
}
```


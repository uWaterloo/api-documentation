# UWaterloo Whitepages Directory Search

```
GET /directory/{user_id}.{format}
```

## Description

> This method returns user information for a given WatIAM ID

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
    <td>1201</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>directory</td>
    <td><b>Service ID</b></td>
    <td>251</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>IST Department</td>
    <td><b>Data Type</b></td>
    <td>LDAP Database</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Realtime LDAP lookup</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- All calls on this endpoint are logged as a security measure
- Reverse searching or indexing this catalogue is not permitted
- Any value can be `null`


### Sources

- http://watiam.uwaterloo.ca/search/app/


## Parameters

```
GET /directory/{user_id}.{format}
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
GET /directory/{user_id}.{format}
```

- **https://api.uwaterloo.ca/v2/directory/ktalwar.json**
- **https://api.uwaterloo.ca/v2/directory/kartik.talwar.xml**
- **https://api.uwaterloo.ca/v2/directory/lwsmith.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>full_name</b></td>
    <td>string</td>
    <td>Full Name</td>
  </tr>
  <tr>
    <td><b>given_name</b></td>
    <td>string</td>
    <td>Given Name</td>
  </tr>
  <tr>
    <td><b>last_name</b></td>
    <td>string</td>
    <td>Last Name</td>
  </tr>
  <tr>
    <td><b>user_id</b></td>
    <td>string</td>
    <td>User's WatIAM user ID</td>
  </tr>
  <tr>
    <td><b>department</b></td>
    <td>string</td>
    <td>User's Department/Faculty Association</td>
  </tr>
  <tr>
    <td><b>common_names</b></td>
    <td>list</td>
    <td>Other names of the user</td>
  </tr>
  <tr>
    <td><b>offices</b></td>
    <td>list</td>
    <td>Office(s) of the user</td>
  </tr>
  <tr>
    <td><b>telephone_numbers</b></td>
    <td>list</td>
    <td>All telephone numbers of the user with phone extension</td>
  </tr>
  <tr>
    <td><b>homepage</b></td>
    <td>string</td>
    <td>User's personal/department website from their profile</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":789770,
    "timestamp":1451857158,
    "status":200,
    "message":"Request successful",
    "method_id":1201,
    "method":{
      
    }
  },
  "data":{
    "full_name":"Kartik Talwar",
    "given_name":"Kartik",
    "last_name":"Talwar",
    "user_id":"ktalwar",
    "department":"SCI\/Science",
    "common_names":[
      "Kartik Talwar"
    ],
    "email_addresses":[
      "ktalwar@uwaterloo.ca",
      "kartik.talwar@uwaterloo.ca"
    ],
    "offices":[
      "EC2 2033"
    ],
    "telephone_numbers":[
      "519-888-4567 x41238"
    ],
    "homepage":"http:\/\/science.uwaterloo.ca\/~ktalwar\/"
  }
}
```


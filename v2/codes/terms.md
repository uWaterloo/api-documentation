# Code Lookups for Terms

```
GET /codes/terms.{format}
```

## Description

> This method returns a list of all code lookups for terms.

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
    <td>1249</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>codes</td>
    <td><b>Service ID</b></td>
    <td>263</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Institution of Analysis & Planning (IAP)</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>When updated by steward/via pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- This data is community curated on github
- Any value can be `null`


### Sources

- https://github.com/uWaterloo/Datasets/blob/master/Quest/Terms.csv


## Parameters

```
GET /codes/terms.{format}
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
GET /codes/terms.{format}
```

- **https://api.uwaterloo.ca/v2/codes/terms.json**
- **https://api.uwaterloo.ca/v2/codes/terms.xml**
- **https://api.uwaterloo.ca/v2/codes/terms.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>abbreviation</b></td>
    <td>string</td>
    <td>Term</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Description of term</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":128,
    "timestamp":1381958213,
    "status":200,
    "message":"Request successful",
    "method_id":1249,
    "version":2.07,
    "method":{
      
    }
  },
  "data":[
    {
      "abbreviation":"F",
      "description":"Fall"
    },
    {
      "abbreviation":"S",
      "description":"Spring"
    },
    {
      "abbreviation":"W",
      "description":"Winter"
    },
    {
      "abbreviation":"J",
      "description":"Summer; first half; July"
    },
    {
      "abbreviation":"A",
      "description":"Summer; second half; August"
    },
    {
      "abbreviation":"M",
      "description":"Summer; both terms; July, August"
    }
  ]
}
```


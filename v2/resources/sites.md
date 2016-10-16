# The list of all sites available via the WCMS site

```
GET /resources/sites.{format}
```

## Description

> This method returns a list of all the sites available from the UWaterloo WCMS site

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
    <td>1523</td>
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
    <td>SSO</td>
    <td><b>Data Type</b></td>
    <td>Direct feed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>As new sites are created by the WCMS team</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Usage won't increase if there is no data returned
- Any value can be `null`


### Sources

- Datasets / Sites / sites.csv on https://github.com/uWaterloo/


## Parameters

```
GET /resources/sites.{format}
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
GET /resources/printers.{format}
```

- **https://api.uwaterloo.ca/v2/resources/sites.json**
- **https://api.uwaterloo.ca/v2/resources/sites.xml**
- **https://api.uwaterloo.ca/v2/resources/sites.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>name</b></td>
    <td>string</td>
    <td>Official name of WCMS site</td>
  </tr>
  <tr>
    <td><b>slug</b></td>
    <td>string</td>
    <td>URL Slug (part of a URL identifying the page using human-readable keywords)</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>Complete Link to WCMS site</td>
  </tr>
  <tr>
    <td><b>group_code</b></td>
    <td>string</td>
    <td>Unit's parent group</td>
  </tr>
  <tr>
    <td><b>unit_code</b></td>
    <td>string</td>
    <td>Organizational Unit code</td>
  </tr>
  <tr>
    <td><b>unit_short_name</b></td>
    <td>string</td>
    <td>Organizational Units short name</td>
  </tr>
  <tr>
    <td><b>owner_type</b></td>
    <td>string</td>
    <td></td>
  </tr>
</table>


Any value can be `null`


## Output

#### JSON

```json
{
  "meta": {
    "requests": 1330,
    "timestamp": 1476569686,
    "status": 200,
    "message": "Request successful",
    "method_id": 1523,
    "method": {
      
    }
  },
  "data": [
    {
      "name": "3D Print Centre",
      "slug": "3d-print-centre",
      "url": "https://uwaterloo.ca/3d-print-centre",
      "group_code": "ENG",
      "unit_code": "ENG",
      "unit_short_name": "Engineering",
      "owner_type": "service-it"
    },
    {
      "name": "About Waterloo",
      "slug": "about",
      "url": "https://uwaterloo.ca/about",
      "group_code": null,
      "unit_code": "VP-UREL",
      "unit_short_name": "Vice-President University Relations",
      "owner_type": null
    },
    {
      "name": "Academic Integrity",
      "slug": "academic-integrity",
      "url": "https://uwaterloo.ca/academic-integrity",
      "group_code": null,
      "unit_code": "AP-RESO",
      "unit_short_name": "Associate Provost, Resources",
      "owner_type": "service-academic"
    }
  ]
}
```


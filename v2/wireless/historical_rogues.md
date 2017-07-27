# Historical wireless rogues statistics

```
GET /wireless/historical/rogues.{format}
```

## Description

> This method returns historical statistics about rogue access points.

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
    <td>10003</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>wireless</td>
    <td><b>Service ID</b></td>
    <td>1000</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Information Systems & Technology</td>
    <td><b>Data Type</b></td>
    <td>Database</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every 15 minutes</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Historical data only available for the past 2 months.
- Any value can be `null`


### Sources

- https://uwaterloo.ca/information-systems-technology/statistics/wifi-charts


## Parameters

```
GET /wireless/historical/rogues.{format}
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
    <td>Valid API key</td>
  </tr>
  <tr>
    <td><b>callback</b></td>
    <td>filter</td>
    <td><i>no</i></td>
    <td>JSONP callback format</td>
  </tr>
  <tr>
    <td><b>from</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Timestamp of start time (in ISO 8601 format)</td>
  </tr>
  <tr>
    <td><b>to</b></td>
    <td>filter</td>
    <td><i>yes</i></td>
    <td>Timestamp of end time (in ISO 8601 format)</td>
  </tr>
</table>

**Output Formats**

- json
- xml


## Examples

```
GET /wireless/historical/rogues.{format}
```

- **https://api.uwaterloo.ca/v2/wireless/historical/rogues.json?from=2017-07-18T160000-0400&to=2017-07-19T235959-0400**
- **https://api.uwaterloo.ca/v2/wireless/historical/rogues.xml**
- **https://api.uwaterloo.ca/v2/wireless/historical/rogues.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>count</b></td>
    <td>string</td>
    <td>Number of rogue access points</td>
  </tr>
  <tr>
    <td><b>last_updated</b></td>
    <td>string</td>
    <td>Timestamp of last collection</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
    "meta": {
        "requests": 1016635,
        "timestamp": 1501170373,
        "status": 200,
        "message": "Request successful",
        "method_id": 10008,
        "method": []
    },
    "data": [
        {
            "count": 1771,
            "last_updated": "2017-07-18T16:00:00-04:00"
        },
        {
            "count": 1775,
            "last_updated": "2017-07-18T16:15:00-04:00"
        },
        {
            "count": 1777,
            "last_updated": "2017-07-18T16:30:00-04:00"
        },
        {
            "count": 1779,
            "last_updated": "2017-07-18T16:45:00-04:00"
        },
        {
            "count": 1784,
            "last_updated": "2017-07-18T17:00:00-04:00"
        },
        {
            "count": 1784,
            "last_updated": "2017-07-18T17:15:00-04:00"
        },
        {
            "count": 1786,
            "last_updated": "2017-07-18T17:30:00-04:00"
        },
        {
            "count": 1787,
            "last_updated": "2017-07-18T17:45:00-04:00"
        },
        {
            "count": 1788,
            "last_updated": "2017-07-18T18:00:00-04:00"
        },
        {
            "count": 1789,
            "last_updated": "2017-07-18T18:15:00-04:00"
        },
        {
            "count": 1789,
            "last_updated": "2017-07-18T18:30:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-18T18:45:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-18T19:00:00-04:00"
        },
        {
            "count": 1793,
            "last_updated": "2017-07-18T19:15:00-04:00"
        },
        {
            "count": 1793,
            "last_updated": "2017-07-18T19:30:00-04:00"
        },
        {
            "count": 1787,
            "last_updated": "2017-07-18T19:45:00-04:00"
        },
        {
            "count": 1787,
            "last_updated": "2017-07-18T20:00:00-04:00"
        },
        {
            "count": 1787,
            "last_updated": "2017-07-18T20:15:00-04:00"
        },
        {
            "count": 1789,
            "last_updated": "2017-07-18T20:30:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-18T20:45:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-18T21:00:00-04:00"
        },
        {
            "count": 1792,
            "last_updated": "2017-07-18T21:15:00-04:00"
        },
        {
            "count": 1792,
            "last_updated": "2017-07-18T21:30:00-04:00"
        },
        {
            "count": 1792,
            "last_updated": "2017-07-18T21:45:00-04:00"
        },
        {
            "count": 1793,
            "last_updated": "2017-07-18T22:00:00-04:00"
        },
        {
            "count": 1793,
            "last_updated": "2017-07-18T22:15:00-04:00"
        },
        {
            "count": 1794,
            "last_updated": "2017-07-18T22:30:00-04:00"
        },
        {
            "count": 1794,
            "last_updated": "2017-07-18T22:45:00-04:00"
        },
        {
            "count": 1795,
            "last_updated": "2017-07-18T23:00:00-04:00"
        },
        {
            "count": 1795,
            "last_updated": "2017-07-18T23:15:00-04:00"
        },
        {
            "count": 1796,
            "last_updated": "2017-07-18T23:30:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-18T23:45:00-04:00"
        },
        {
            "count": 1794,
            "last_updated": "2017-07-19T00:00:00-04:00"
        },
        {
            "count": 1797,
            "last_updated": "2017-07-19T00:15:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T00:30:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T00:45:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T01:00:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T01:15:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T01:30:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T01:45:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T02:00:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T02:15:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T02:30:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T02:45:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T03:00:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T03:15:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T03:30:00-04:00"
        },
        {
            "count": 1789,
            "last_updated": "2017-07-19T03:45:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-19T04:00:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-19T04:15:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-19T04:30:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-19T04:45:00-04:00"
        },
        {
            "count": 1790,
            "last_updated": "2017-07-19T05:00:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-19T05:15:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-19T05:30:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-19T05:45:00-04:00"
        },
        {
            "count": 1792,
            "last_updated": "2017-07-19T06:00:00-04:00"
        },
        {
            "count": 1792,
            "last_updated": "2017-07-19T06:15:00-04:00"
        },
        {
            "count": 1794,
            "last_updated": "2017-07-19T06:30:00-04:00"
        },
        {
            "count": 1795,
            "last_updated": "2017-07-19T06:45:00-04:00"
        },
        {
            "count": 1796,
            "last_updated": "2017-07-19T07:00:00-04:00"
        },
        {
            "count": 1796,
            "last_updated": "2017-07-19T07:15:00-04:00"
        },
        {
            "count": 1796,
            "last_updated": "2017-07-19T07:30:00-04:00"
        },
        {
            "count": 1791,
            "last_updated": "2017-07-19T07:45:00-04:00"
        },
        {
            "count": 1793,
            "last_updated": "2017-07-19T08:00:00-04:00"
        },
        {
            "count": 1794,
            "last_updated": "2017-07-19T08:15:00-04:00"
        },
        {
            "count": 1796,
            "last_updated": "2017-07-19T08:30:00-04:00"
        },
        {
            "count": 1796,
            "last_updated": "2017-07-19T08:45:00-04:00"
        },
        {
            "count": 1798,
            "last_updated": "2017-07-19T09:00:00-04:00"
        },
        {
            "count": 1799,
            "last_updated": "2017-07-19T09:15:00-04:00"
        },
        {
            "count": 1805,
            "last_updated": "2017-07-19T09:30:00-04:00"
        },
        {
            "count": 1810,
            "last_updated": "2017-07-19T09:45:00-04:00"
        },
        {
            "count": 1812,
            "last_updated": "2017-07-19T10:00:00-04:00"
        },
        {
            "count": 1813,
            "last_updated": "2017-07-19T10:15:00-04:00"
        },
        {
            "count": 1817,
            "last_updated": "2017-07-19T10:30:00-04:00"
        },
        {
            "count": 1817,
            "last_updated": "2017-07-19T10:45:00-04:00"
        },
        {
            "count": 1818,
            "last_updated": "2017-07-19T11:00:00-04:00"
        },
        {
            "count": 1820,
            "last_updated": "2017-07-19T11:15:00-04:00"
        },
        {
            "count": 1822,
            "last_updated": "2017-07-19T11:30:00-04:00"
        },
        {
            "count": 1819,
            "last_updated": "2017-07-19T11:45:00-04:00"
        },
        {
            "count": 1820,
            "last_updated": "2017-07-19T12:00:00-04:00"
        },
        {
            "count": 1824,
            "last_updated": "2017-07-19T12:15:00-04:00"
        },
        {
            "count": 1825,
            "last_updated": "2017-07-19T12:30:00-04:00"
        },
        {
            "count": 1826,
            "last_updated": "2017-07-19T12:45:00-04:00"
        },
        {
            "count": 1830,
            "last_updated": "2017-07-19T13:00:00-04:00"
        },
        {
            "count": 1831,
            "last_updated": "2017-07-19T13:15:00-04:00"
        },
        {
            "count": 1833,
            "last_updated": "2017-07-19T13:30:00-04:00"
        },
        {
            "count": 1834,
            "last_updated": "2017-07-19T13:45:00-04:00"
        },
        {
            "count": 1835,
            "last_updated": "2017-07-19T14:00:00-04:00"
        },
        {
            "count": 1836,
            "last_updated": "2017-07-19T14:15:00-04:00"
        },
        {
            "count": 1838,
            "last_updated": "2017-07-19T14:30:00-04:00"
        },
        {
            "count": 1841,
            "last_updated": "2017-07-19T14:45:00-04:00"
        },
        {
            "count": 1841,
            "last_updated": "2017-07-19T15:00:00-04:00"
        },
        {
            "count": 1844,
            "last_updated": "2017-07-19T15:15:00-04:00"
        },
        {
            "count": 1851,
            "last_updated": "2017-07-19T15:30:00-04:00"
        },
        {
            "count": 1842,
            "last_updated": "2017-07-19T15:45:00-04:00"
        },
        {
            "count": 1846,
            "last_updated": "2017-07-19T16:00:00-04:00"
        },
        {
            "count": 1849,
            "last_updated": "2017-07-19T16:15:00-04:00"
        },
        {
            "count": 1851,
            "last_updated": "2017-07-19T16:30:00-04:00"
        },
        {
            "count": 1855,
            "last_updated": "2017-07-19T16:45:00-04:00"
        },
        {
            "count": 1858,
            "last_updated": "2017-07-19T17:00:00-04:00"
        },
        {
            "count": 1860,
            "last_updated": "2017-07-19T17:15:00-04:00"
        },
        {
            "count": 1860,
            "last_updated": "2017-07-19T17:30:00-04:00"
        },
        {
            "count": 1861,
            "last_updated": "2017-07-19T17:45:00-04:00"
        },
        {
            "count": 1861,
            "last_updated": "2017-07-19T18:00:00-04:00"
        },
        {
            "count": 1867,
            "last_updated": "2017-07-19T18:15:00-04:00"
        },
        {
            "count": 1867,
            "last_updated": "2017-07-19T18:30:00-04:00"
        },
        {
            "count": 1869,
            "last_updated": "2017-07-19T18:45:00-04:00"
        },
        {
            "count": 1869,
            "last_updated": "2017-07-19T19:00:00-04:00"
        },
        {
            "count": 1869,
            "last_updated": "2017-07-19T19:15:00-04:00"
        },
        {
            "count": 1869,
            "last_updated": "2017-07-19T19:30:00-04:00"
        },
        {
            "count": 1857,
            "last_updated": "2017-07-19T19:45:00-04:00"
        },
        {
            "count": 1857,
            "last_updated": "2017-07-19T20:00:00-04:00"
        },
        {
            "count": 1858,
            "last_updated": "2017-07-19T20:15:00-04:00"
        },
        {
            "count": 1858,
            "last_updated": "2017-07-19T20:30:00-04:00"
        },
        {
            "count": 1860,
            "last_updated": "2017-07-19T20:45:00-04:00"
        },
        {
            "count": 1863,
            "last_updated": "2017-07-19T21:00:00-04:00"
        },
        {
            "count": 1863,
            "last_updated": "2017-07-19T21:15:00-04:00"
        },
        {
            "count": 1863,
            "last_updated": "2017-07-19T21:30:00-04:00"
        },
        {
            "count": 1864,
            "last_updated": "2017-07-19T21:45:00-04:00"
        },
        {
            "count": 1867,
            "last_updated": "2017-07-19T22:00:00-04:00"
        },
        {
            "count": 1868,
            "last_updated": "2017-07-19T22:15:00-04:00"
        },
        {
            "count": 1871,
            "last_updated": "2017-07-19T22:30:00-04:00"
        },
        {
            "count": 1873,
            "last_updated": "2017-07-19T22:45:00-04:00"
        },
        {
            "count": 1875,
            "last_updated": "2017-07-19T23:00:00-04:00"
        },
        {
            "count": 1876,
            "last_updated": "2017-07-19T23:15:00-04:00"
        },
        {
            "count": 1879,
            "last_updated": "2017-07-19T23:30:00-04:00"
        },
        {
            "count": 1877,
            "last_updated": "2017-07-19T23:45:00-04:00"
        }
    ]
}
```


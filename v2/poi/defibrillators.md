# List of defibrillators (AEDs) across campus

```
GET /v2/poi/defibrillators.{format}
```

## Description

> This method returns list of defibrillators across campus.

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
    <td>1879</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>poi</td>
    <td><b>Service ID</b></td>
    <td>349</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Campus Map Team</td>
    <td><b>Data Type</b></td>
    <td>CSV</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Upon pull request</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- http://github.com/uWaterloo/datasets


## Parameters

```
GET /v2/poi/defibrillators.{format}
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
- geojson
- xml


## Examples

```
GET /v2/poi/defibrillators.{format}
```

- **https://api.uwaterloo.ca/v2/poi/defibrillators.json**
- **https://api.uwaterloo.ca/v2/poi/defibrillators.geojson**
- **https://api.uwaterloo.ca/v2/poi/defibrillators.xml**
- **https://api.uwaterloo.ca/v2/poi/defibrillators.json?callback=myResponse**


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
    <td>Name of the location</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Location description</td>
  </tr>
  <tr>
    <td><b>note</b></td>
    <td>string</td>
    <td>Any additional notes</td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Latitude of the parking lot</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Longitude of the parking lot</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811625,
    "timestamp":1453159147,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":null,
      "description":"Between the male and female washrooms (across from the front desk)",
      "note":"Columbia Lake Village (CLV)",
      "latitude":43.47082,
      "longitude":-80.56244
    },
    {
      "name":null,
      "description":"Across from the front desk",
      "note":"MacKenzie King Village (MKV)",
      "latitude":43.47118,
      "longitude":-80.55202
    },
    {
      "name":null,
      "description":"By cafeteria computers",
      "note":"Ron Eydt Village (REV)",
      "latitude":43.47025,
      "longitude":-80.55402
    },
    {
      "name":null,
      "description":"By cafeteria computers (across from the front desk)",
      "note":"University of Waterloo Place (UWP) - Beck Hall Community Centre",
      "latitude":43.47078,
      "longitude":-80.53469
    },
    {
      "name":null,
      "description":"By cafeteria computers near the front desk",
      "note":"Student Village 1 (V1)",
      "latitude":43.47173,
      "longitude":-80.55012
    },
    {
      "name":null,
      "description":"Room 7007, off the main entrance to the department",
      "note":"Allen Square - 180 King St. S., Suite 700",
      "latitude":43.46071,
      "longitude":-80.51916
    },
    {
      "name":null,
      "description":"Second floor near entrance to the Amphitheatre (room 271)",
      "note":"Biology 1 (B1)",
      "latitude":43.47108,
      "longitude":-80.54315
    },
    {
      "name":null,
      "description":"Room 1606 in the black cabinet by the sink, Physical Assessment Lab",
      "note":"Lyle S. Hallman Institute for Health Promotion",
      "latitude":43.47321,
      "longitude":-80.54597
    },
    {
      "name":null,
      "description":"Outside Chemistry Office (room 280), near the fire hose",
      "note":"Chemistry 2 (C2)",
      "latitude":43.47194,
      "longitude":-80.54312
    },
    {
      "name":null,
      "description":"Main desk area, near the Arena",
      "note":"Columbia Icefield (CIF)",
      "latitude":43.47551,
      "longitude":-80.54835
    },
    {
      "name":null,
      "description":"By room 112",
      "note":"Commissary (COM)",
      "latitude":43.47416,
      "longitude":-80.54278
    },
    {
      "name":null,
      "description":"Circulation desk (room 229)",
      "note":"Dana Porter Library (LIB)",
      "latitude":43.46963,
      "longitude":-80.54234
    },
    {
      "name":null,
      "description":"Circulation desk (room 1511)",
      "note":"William G. Davis Computer Research Centre (DC)",
      "latitude":43.47259,
      "longitude":-80.54209
    },
    {
      "name":null,
      "description":"Room 128, Receiving Area, Central Stores",
      "note":"East Campus Hall (ECH)",
      "latitude":43.47384,
      "longitude":-80.53907
    },
    {
      "name":null,
      "description":"Ground floor to the right of the elevator",
      "note":"Centre for Environmental and Information Technology (EIT)",
      "latitude":43.47175,
      "longitude":-80.54204
    },
    {
      "name":null,
      "description":"Room 1103",
      "note":"Engineering 5 (E5)",
      "latitude":43.47251,
      "longitude":-80.53986
    },
    {
      "name":null,
      "description":"Across from room 116 by the payphone, near the Theatre Centre",
      "note":"J.G. Hagey Hall of the Humanities (HH)",
      "latitude":43.46803,
      "longitude":-80.54154
    },
    {
      "name":null,
      "description":"103 Urgent Care Room - Health Services",
      "note":"Health Services (HS)",
      "latitude":43.47051,
      "longitude":-80.54617
    },
    {
      "name":null,
      "description":"Second floor by the elevator",
      "note":"Ira G. Needles Hall (NH)",
      "latitude":43.46973,
      "longitude":-80.54361
    },
    {
      "name":null,
      "description":"Administration desk area (room 142), Optometry Clinics",
      "note":"Optometry Building (OPT)",
      "latitude":43.47584,
      "longitude":-80.54559
    },
    {
      "name":null,
      "description":"Tote Desk - Athletics",
      "note":"Physical Activities Complex (PAC)",
      "latitude":43.47245,
      "longitude":-80.54597
    },
    {
      "name":null,
      "description":"Pool area",
      "note":"Physical Activities Complex (PAC)",
      "latitude":43.4726,
      "longitude":-80.54604
    },
    {
      "name":null,
      "description":"First floor outside the security office",
      "note":"Pharmacy (PHR)",
      "latitude":43.45272,
      "longitude":-80.4987
    },
    {
      "name":null,
      "description":"Second floor outside Physics Office, near stairwell across from men's washroom",
      "note":"Physics (PHY)",
      "latitude":43.47064,
      "longitude":-80.54158
    },
    {
      "name":null,
      "description":"Room 2216, beside the kitchen, Institute for Quantum Computing",
      "note":"Mike & Ophelia Lazaridis Quantum-Nano Centre (QNC)",
      "latitude":43.47132,
      "longitude":-80.54445
    },
    {
      "name":null,
      "description":"East corridor, outside room 1809",
      "note":"Research Advancement Centre (RAC)",
      "latitude":43.47881,
      "longitude":-80.5547
    },
    {
      "name":null,
      "description":"East corridor, outside room 1802",
      "note":"Research Advancement Centre 2 (RA2)",
      "latitude":43.47833,
      "longitude":-80.55529
    },
    {
      "name":null,
      "description":"Link area\/reception office",
      "note":"Renison University College (REN)",
      "latitude":43.46864,
      "longitude":-80.54714
    },
    {
      "name":null,
      "description":"Turnkey Desk at Great Hall",
      "note":"Student Life Centre (SLC)",
      "latitude":43.47157,
      "longitude":-80.54565
    },
    {
      "name":null,
      "description":"Campus Response Team, room 2141 (available to attend special events only)",
      "note":"Student Life Centre (SLC)",
      "latitude":43.47209,
      "longitude":-80.54535
    },
    {
      "name":null,
      "description":"Ground floor to the right of the elevator",
      "note":"Engineering 6 (E6)",
      "latitude":43.47312,
      "longitude":-80.53879
    },
    {
      "name":null,
      "description":"Third floor, south corridor by the elevator",
      "note":"Mike & Ophelia Lazaridis Quantum-Nano Centre (QNC)",
      "latitude":43.47113,
      "longitude":-80.54372
    },
    {
      "name":null,
      "description":"Front main desk reception area in a case on the wall behind the desk",
      "note":"William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "latitude":43.46898,
      "longitude":-80.54121
    }
  ]
}
```


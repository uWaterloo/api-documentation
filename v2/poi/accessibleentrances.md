# List of accessible entrances

```
GET /v2/poi/accessibleentrances.{format}
```

## Description

> This method returns list of accessible entrances across campus.

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
GET /v2/poi/accessibleentrances.{format}
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
GET /v2/poi/accessibleentrances.{format}
```

- **https://api.uwaterloo.ca/v2/poi/accessibleentrances.json**
- **https://api.uwaterloo.ca/v2/poi/accessibleentrances.geojson**
- **https://api.uwaterloo.ca/v2/poi/accessibleentrances.xml**
- **https://api.uwaterloo.ca/v2/poi/accessibleentrances.json?callback=myResponse**


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
    "requests":811550,
    "timestamp":1453157888,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Columbia Lake Village (CLV)",
      "description":"Main entrance on Residence Road.",
      "note":"Community Centre",
      "latitude":43.470832858698,
      "longitude":-80.56229194092
    },
    {
      "name":"Columbia Icefield (CIF)",
      "description":null,
      "note":null,
      "latitude":43.475555555556,
      "longitude":-80.548266666667
    },
    {
      "name":"Optometry Building (OPT)",
      "description":null,
      "note":null,
      "latitude":43.475815245449,
      "longitude":-80.545197882959
    },
    {
      "name":"Ron Eydt Village (REV)",
      "description":null,
      "note":null,
      "latitude":43.470490916737,
      "longitude":-80.554268155599
    },
    {
      "name":"Ron Eydt Village (REV)",
      "description":null,
      "note":null,
      "latitude":43.470169582725,
      "longitude":-80.553875576059
    },
    {
      "name":"William Lyon Mackenzie King Village (MKV)",
      "description":null,
      "note":null,
      "latitude":43.471441180143,
      "longitude":-80.551954016034
    },
    {
      "name":"Student Village 1 (V1)",
      "description":null,
      "note":null,
      "latitude":43.471427512785,
      "longitude":-80.550494595497
    },
    {
      "name":"Student Village 1 (V1)",
      "description":null,
      "note":null,
      "latitude":43.471308652618,
      "longitude":-80.549983174876
    },
    {
      "name":"Student Village 1 (V1)",
      "description":null,
      "note":null,
      "latitude":43.471823782117,
      "longitude":-80.549648097941
    },
    {
      "name":"University Club (UC)",
      "description":null,
      "note":null,
      "latitude":43.472323021019,
      "longitude":-80.547627379229
    },
    {
      "name":"Physical Activities Complex (PAC)",
      "description":null,
      "note":null,
      "latitude":43.471874224596,
      "longitude":-80.546140007286
    },
    {
      "name":"Student Life Centre (SLC)",
      "description":null,
      "note":null,
      "latitude":43.471297251142,
      "longitude":-80.545340677641
    },
    {
      "name":"Student Life Centre (SLC)",
      "description":null,
      "note":null,
      "latitude":43.471780090293,
      "longitude":-80.544889346842
    },
    {
      "name":"Student Life Centre (SLC)",
      "description":null,
      "note":null,
      "latitude":43.471640882049,
      "longitude":-80.545717256993
    },
    {
      "name":"B.C. Matthews Hall (BMH)",
      "description":null,
      "note":null,
      "latitude":43.473476155238,
      "longitude":-80.545235468844
    },
    {
      "name":"B.C. Matthews Hall (BMH)",
      "description":null,
      "note":null,
      "latitude":43.473936846928,
      "longitude":-80.545520456241
    },
    {
      "name":"Federation Hall (FED)",
      "description":null,
      "note":null,
      "latitude":43.473258764029,
      "longitude":-80.548222625642
    },
    {
      "name":"Mathematics & Computer Building (MC)",
      "description":null,
      "note":null,
      "latitude":43.471742715393,
      "longitude":-80.543596781666
    },
    {
      "name":"Mathematics 3 (M3)",
      "description":null,
      "note":null,
      "latitude":43.472922169625,
      "longitude":-80.54406409488
    },
    {
      "name":"William G. Davis Computer Research Centre (DC)",
      "description":null,
      "note":null,
      "latitude":43.472770663846,
      "longitude":-80.543089788933
    },
    {
      "name":"William G. Davis Computer Research Centre (DC)",
      "description":null,
      "note":null,
      "latitude":43.472841430895,
      "longitude":-80.541955008515
    },
    {
      "name":"General Services Complex (GSC)",
      "description":null,
      "note":null,
      "latitude":43.473513207512,
      "longitude":-80.54254465893
    },
    {
      "name":"Engineering 3 (E3)",
      "description":null,
      "note":null,
      "latitude":43.47221088799,
      "longitude":-80.541146840665
    },
    {
      "name":"Centre for Environmental and Information Technology (EIT)",
      "description":null,
      "note":null,
      "latitude":43.471810082624,
      "longitude":-80.542335271971
    },
    {
      "name":"Engineering 5 (E5)",
      "description":null,
      "note":null,
      "latitude":43.472788365877,
      "longitude":-80.540164254413
    },
    {
      "name":"Engineering 5 (E5)",
      "description":null,
      "note":null,
      "latitude":43.47291064223,
      "longitude":-80.539740067679
    },
    {
      "name":"East Campus Hall (ECH)",
      "description":null,
      "note":null,
      "latitude":43.473325980326,
      "longitude":-80.539297312471
    },
    {
      "name":"Carl A. Pollock Hall (CPH)",
      "description":null,
      "note":null,
      "latitude":43.470643769027,
      "longitude":-80.538867543705
    },
    {
      "name":"University of Waterloo Place (UWP)",
      "description":null,
      "note":"Eby Hall",
      "latitude":43.470744715559,
      "longitude":-80.535637397126
    },
    {
      "name":"University of Waterloo Place (UWP)",
      "description":null,
      "note":"Waterloo Court",
      "latitude":43.470407064322,
      "longitude":-80.535148132954
    },
    {
      "name":"University of Waterloo Place (UWP)",
      "description":null,
      "note":"Wellesley Court",
      "latitude":43.471334882092,
      "longitude":-80.535171130573
    },
    {
      "name":"Douglas Wright Engineering Building (DWE)",
      "description":null,
      "note":null,
      "latitude":43.469819457122,
      "longitude":-80.540591505362
    },
    {
      "name":"J.R. Coutts Engineering Lecture Hall (RCH)",
      "description":null,
      "note":null,
      "latitude":43.470094726827,
      "longitude":-80.540737036
    },
    {
      "name":"Graduate House (GH)",
      "description":null,
      "note":null,
      "latitude":43.469676276719,
      "longitude":-80.541005768604
    },
    {
      "name":"South Campus Hall (SCH)",
      "description":null,
      "note":null,
      "latitude":43.469388018428,
      "longitude":-80.540286949479
    },
    {
      "name":"William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "description":null,
      "note":null,
      "latitude":43.468929310995,
      "longitude":-80.541107347326
    },
    {
      "name":"William M. Tatham Centre for Co-operative Education & Career Action (TC)",
      "description":null,
      "note":null,
      "latitude":43.468991419163,
      "longitude":-80.541407773664
    },
    {
      "name":"Arts Lecture Hall (AL)",
      "description":null,
      "note":null,
      "latitude":43.469063576871,
      "longitude":-80.541986664808
    },
    {
      "name":"J.G. Hagey Hall of the Humanities (HH)",
      "description":null,
      "note":null,
      "latitude":43.467597156094,
      "longitude":-80.541724368536
    },
    {
      "name":"Environment 2 (EV2)",
      "description":null,
      "note":null,
      "latitude":43.467743509103,
      "longitude":-80.543488920064
    },
    {
      "name":"Modern Languages (ML)",
      "description":null,
      "note":null,
      "latitude":43.469031948178,
      "longitude":-80.54262719214
    },
    {
      "name":"Modern Languages (ML)",
      "description":null,
      "note":null,
      "latitude":43.469083923888,
      "longitude":-80.542949383397
    },
    {
      "name":"Ira G. Needles Hall (NH)",
      "description":null,
      "note":null,
      "latitude":43.469584021414,
      "longitude":-80.54309345101
    },
    {
      "name":"Ira G. Needles Hall (NH)",
      "description":null,
      "note":null,
      "latitude":43.46985550607,
      "longitude":-80.543496322565
    },
    {
      "name":"Biology 2 (B2)",
      "description":null,
      "note":null,
      "latitude":43.470691556589,
      "longitude":-80.54337866424
    },
    {
      "name":"Biology 2 (B2)",
      "description":null,
      "note":null,
      "latitude":43.470697535381,
      "longitude":-80.544183164578
    },
    {
      "name":"St. Jerome's University",
      "description":null,
      "note":null,
      "latitude":43.469544071388,
      "longitude":-80.545637205344
    },
    {
      "name":"St. Jerome's University",
      "description":null,
      "note":null,
      "latitude":43.469425167876,
      "longitude":-80.545383417548
    },
    {
      "name":"St. Jerome's University",
      "description":null,
      "note":null,
      "latitude":43.469153248217,
      "longitude":-80.545619416525
    },
    {
      "name":"St. Jerome's University",
      "description":null,
      "note":null,
      "latitude":43.468950540071,
      "longitude":-80.545731057816
    },
    {
      "name":"St. Jerome's University",
      "description":null,
      "note":null,
      "latitude":43.468783170541,
      "longitude":-80.54560688762
    },
    {
      "name":"Health Services (HS)",
      "description":null,
      "note":null,
      "latitude":43.470431655364,
      "longitude":-80.545914112871
    },
    {
      "name":"Renison University College (REN)",
      "description":null,
      "note":null,
      "latitude":43.468522508247,
      "longitude":-80.546590748643
    },
    {
      "name":"Renison University College (REN)",
      "description":null,
      "note":null,
      "latitude":43.468529053884,
      "longitude":-80.547530074821
    },
    {
      "name":"Renison University College (REN)",
      "description":null,
      "note":null,
      "latitude":43.46879114274,
      "longitude":-80.54740615466
    },
    {
      "name":"St. Paul's University College (STP)",
      "description":null,
      "note":null,
      "latitude":43.468148638445,
      "longitude":-80.546483708004
    },
    {
      "name":"St. Paul's University College (STP)",
      "description":null,
      "note":null,
      "latitude":43.467709128944,
      "longitude":-80.546613391007
    },
    {
      "name":"Conrad Grebel University College (CGR)",
      "description":null,
      "note":null,
      "latitude":43.466080239991,
      "longitude":-80.544735132918
    },
    {
      "name":"Conrad Grebel University College (CGR)",
      "description":null,
      "note":null,
      "latitude":43.466796773858,
      "longitude":-80.545343731545
    },
    {
      "name":"St. Paul's University College (STP)",
      "description":null,
      "note":null,
      "latitude":43.467767741683,
      "longitude":-80.546057932012
    },
    {
      "name":"Physics (PHY)",
      "description":null,
      "note":null,
      "latitude":43.470448536293,
      "longitude":-80.541703176966
    },
    {
      "name":"Centre for Environmental and Information Technology (EIT)",
      "description":null,
      "note":null,
      "latitude":43.471224222847,
      "longitude":-80.542360096543
    },
    {
      "name":"J.G. Hagey Hall of the Humanities (HH)",
      "description":null,
      "note":null,
      "latitude":43.468224405996,
      "longitude":-80.541729246673
    },
    {
      "name":"Dana Porter Library (LIB)",
      "description":null,
      "note":null,
      "latitude":43.469550735713,
      "longitude":-80.542156769145
    },
    {
      "name":"Dana Porter Library (LIB)",
      "description":null,
      "note":null,
      "latitude":43.469835699051,
      "longitude":-80.542018598166
    },
    {
      "name":"William G. Davis Computer Research Centre (DC)",
      "description":null,
      "note":null,
      "latitude":43.472649428662,
      "longitude":-80.542478146937
    }
  ]
}
```


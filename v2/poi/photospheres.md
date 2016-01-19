# List of photospheres across Campus

```
GET /v2/poi/photospheres.{format}
```

## Description

> This method returns list of photospheres across campus.

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
GET /v2/poi/photospheres.{format}
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
GET /v2/poi/photospheres.{format}
```

- **https://api.uwaterloo.ca/v2/poi/photospheres.json**
- **https://api.uwaterloo.ca/v2/poi/photospheres.geojson**
- **https://api.uwaterloo.ca/v2/poi/photospheres.xml**
- **https://api.uwaterloo.ca/v2/poi/photospheres.json?callback=myResponse**


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
    "requests":811562,
    "timestamp":1453158237,
    "status":200,
    "message":"Request successful",
    "method_id":1889,
    "method":{
      
    }
  },
  "data":[
    {
      "name":"Playing fields",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4751268,-80.5533472,3a,75y,90t\/data=!3m7!1e1!3m5!1s-y50ZbOSx43A%2FVEZeksPLZAI%2FAAAAAAAAAdk%2FajLUun5WIpU!2e4!6s%2F%2Flh3.googleusercontent.com%2F-y50ZbOSx43A%2FVEZeksPLZAI%2FAAAAAAAAAdk%2FajLUun5WIpU%2Fw203-h100-k-no%2F!7i7884!8i3520",
      "latitude":43.4751268,
      "longitude":-80.5533472
    },
    {
      "name":"Warrior Field",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4743876,-80.5498358,3a,75y,180h,90t\/data=!3m7!1e1!3m5!1s-QUkOHUqZ41M%2FVEZekgkFAEI%2FAAAAAAAAA1A%2FpDYMLmJiLlQ!2e4!6s%2F%2Flh5.googleusercontent.com%2F-QUkOHUqZ41M%2FVEZekgkFAEI%2FAAAAAAAAA1A%2FpDYMLmJiLlQ%2Fw203-h100-k-no%2F!7i7684!8i3449",
      "latitude":43.4743876,
      "longitude":-80.5498358
    },
    {
      "name":"Bridge to University Colleges",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.4683027,-80.5442997,3a,75y,210h,90t\/data=!3m7!1e1!3m5!1s-QK059_A4c44%2FVJc3NDoMSnI%2FAAAAAAAAA1c%2FcPfzRhBwYMw!2e4!6s%2F%2Flh6.googleusercontent.com%2F-QK059_A4c44%2FVJc3NDoMSnI%2FAAAAAAAAA1c%2FcPfzRhBwYMw%2Fw203-h100-k-no%2F!7i7316!8i3658",
      "latitude":43.4683027,
      "longitude":-80.5442997
    },
    {
      "name":"Warrior Field",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.474465,-80.5496216,3a,75y,90t\/data=!3m7!1e1!3m5!1s-Kvj8etnL-rk%2FVEZekqqIT1I%2FAAAAAAAAAdk%2FNnIHgy5zEmA!2e4!6s%2F%2Flh4.googleusercontent.com%2F-Kvj8etnL-rk%2FVEZekqqIT1I%2FAAAAAAAAAdk%2FNnIHgy5zEmA%2Fw203-h100-k-no%2F!7i7731!8i3458",
      "latitude":43.474465,
      "longitude":-80.5496216
    },
    {
      "name":"Warrior Field",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4739672,-80.5495997,3a,75y,225h,90t\/data=!3m7!1e1!3m5!1s-Y2mmqPN_dYQ%2FVEZekl3RnLI%2FAAAAAAAAAdw%2F7_8KRNQu93s!2e4!6s%2F%2Flh5.googleusercontent.com%2F-Y2mmqPN_dYQ%2FVEZekl3RnLI%2FAAAAAAAAAdw%2F7_8KRNQu93s%2Fw203-h100-k-no%2F!7i7746!8i3471",
      "latitude":43.4739672,
      "longitude":-80.5495997
    },
    {
      "name":"School of Optometry",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4757209,-80.5454584,3a,75y,180h,90t\/data=!3m7!1e1!3m5!1s-PUhfel5hVM0%2FVJc7PYOytKI%2FAAAAAAAABH0%2FhdnxSTqMDVw!2e4!6s%2F%2Flh3.googleusercontent.com%2F-PUhfel5hVM0%2FVJc7PYOytKI%2FAAAAAAAABH0%2FhdnxSTqMDVw%2Fw203-h100-k-no%2F!7i7292!8i3646",
      "latitude":43.4757209,
      "longitude":-80.5454584
    },
    {
      "name":"Museum of Vision Science",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4755418,-80.5456676,3a,75y,210h,90t\/data=!3m7!1e1!3m5!1s-BWf85GBRF6A%2FVJc57FJ3E4I%2FAAAAAAAABE8%2FDY5ND1fnWSo!2e4!6s%2F%2Flh5.googleusercontent.com%2F-BWf85GBRF6A%2FVJc57FJ3E4I%2FAAAAAAAABE8%2FDY5ND1fnWSo%2Fw203-h100-k-no%2F!7i7304!8i3652",
      "latitude":43.4755418,
      "longitude":-80.5456676
    },
    {
      "name":"School of Optometry lounge",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4755438,-80.5454048,3a,75y,180h,90t\/data=!3m7!1e1!3m5!1s-q0FsP_OvcyM%2FVJc5w0lKq-I%2FAAAAAAAAAxM%2F60lSqHIkiHY!2e4!6s%2F%2Flh5.googleusercontent.com%2F-q0FsP_OvcyM%2FVJc5w0lKq-I%2FAAAAAAAAAxM%2F60lSqHIkiHY%2Fw203-h100-k-no%2F!7i7308!8i3654",
      "latitude":43.4755438,
      "longitude":-80.5454048
    },
    {
      "name":"Student lounge, Faculty of Applied Health Sciences",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4736631,-80.5451477,3a,75y,90t\/data=!3m7!1e1!3m5!1s-dpuYZ1zR1-k%2FVL6Z9SHJcoI%2FAAAAAAAABAA%2Fxy8FDbtMl1I!2e4!6s%2F%2Flh4.googleusercontent.com%2F-dpuYZ1zR1-k%2FVL6Z9SHJcoI%2FAAAAAAAABAA%2Fxy8FDbtMl1I%2Fw203-h100-k-no%2F!7i8267!8i3215",
      "latitude":43.4736631,
      "longitude":-80.5451477
    },
    {
      "name":"Math computer lab",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4733054,-80.5439778,3a,75y,90t\/data=!3m7!1e1!3m5!1s-UraeHPiVzbY%2FVJeVIgsuvuI%2FAAAAAAAAA-I%2FOZXjDE-FLh8!2e4!6s%2F%2Flh3.googleusercontent.com%2F-UraeHPiVzbY%2FVJeVIgsuvuI%2FAAAAAAAAA-I%2FOZXjDE-FLh8%2Fw203-h100-k-no%2F!7i7292!8i3646",
      "latitude":43.4733054,
      "longitude":-80.5439778
    },
    {
      "name":"Bloomberg lab",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4732197,-80.543892,3a,75y,90t\/data=!3m7!1e1!3m5!1s-YCu1d-Cf7-0%2FVJeVIncAwgI%2FAAAAAAAAA3g%2FlFXzQiUhyRI!2e4!6s%2F%2Flh5.googleusercontent.com%2F-YCu1d-Cf7-0%2FVJeVIncAwgI%2FAAAAAAAAA3g%2FlFXzQiUhyRI%2Fw203-h100-k-no%2F!7i7320!8i3660",
      "latitude":43.4732197,
      "longitude":-80.543892
    },
    {
      "name":"Bridge between Math and Computers, Math 3, and Davis Centre",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4728071,-80.5440744,3a,75y,220h,90t\/data=!3m7!1e1!3m5!1s-UQ6YcPAPpXw%2FVJcznz0XUvI%2FAAAAAAAAAqw%2FeQkT2fm-V-E!2e4!6s%2F%2Flh5.googleusercontent.com%2F-UQ6YcPAPpXw%2FVJcznz0XUvI%2FAAAAAAAAAqw%2FeQkT2fm-V-E%2Fw203-h100-k-no%2F!7i7272!8i3636",
      "latitude":43.4728071,
      "longitude":-80.5440744
    },
    {
      "name":"Davis Centre atrium",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4727711,-80.5421754,3a,75y,90t\/data=!3m7!1e1!3m5!1s-ouyP5fXSLvk%2FVJczdw4rZ9I%2FAAAAAAAAAqg%2FQSgjDuxu-3s!2e4!6s%2F%2Flh4.googleusercontent.com%2F-ouyP5fXSLvk%2FVJczdw4rZ9I%2FAAAAAAAAAqg%2FQSgjDuxu-3s%2Fw203-h100-k-no%2F!7i7280!8i3640",
      "latitude":43.4727711,
      "longitude":-80.5421754
    },
    {
      "name":"Davis Centre library",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4725968,-80.5420681,3a,75y,200h,90t\/data=!3m7!1e1!3m5!1s-_m1VtTem-Qs%2FVJcrc3b609I%2FAAAAAAAAApY%2FAJSjCeUie1o!2e4!6s%2F%2Flh5.googleusercontent.com%2F-_m1VtTem-Qs%2FVJcrc3b609I%2FAAAAAAAAApY%2FAJSjCeUie1o%2Fw203-h100-k-no%2F!7i7292!8i3646",
      "latitude":43.4725968,
      "longitude":-80.5420681
    },
    {
      "name":"Student Life Centre patio",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.471935,-80.54504,3a,75y,210h,90t\/data=!3m7!1e1!3m5!1s-xpFwMPeukyM%2FVJc4-pVRPaI%2FAAAAAAAAAwY%2Fvp51ceMOe_Q!2e4!6s%2F%2Flh5.googleusercontent.com%2F-xpFwMPeukyM%2FVJc4-pVRPaI%2FAAAAAAAAAwY%2Fvp51ceMOe_Q%2Fw203-h100-k-no%2F!7i7296!8i3648",
      "latitude":43.471935,
      "longitude":-80.54504
    },
    {
      "name":"Mac lab, Faculty of Math",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4718961,-80.5439778,3a,75y,90t\/data=!3m7!1e1!3m5!1s-jhYOsqJGO6I%2FVJeVIv3bE5I%2FAAAAAAAAA3g%2FGtwkPy92Cfk!2e4!6s%2F%2Flh3.googleusercontent.com%2F-jhYOsqJGO6I%2FVJeVIv3bE5I%2FAAAAAAAAA3g%2FGtwkPy92Cfk%2Fw203-h100-k-no%2F!7i7332!8i3666",
      "latitude":43.4718961,
      "longitude":-80.5439778
    },
    {
      "name":"Math building 3rd floor",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4718572,-80.5437525,3a,75y,245h,90t\/data=!3m7!1e1!3m5!1s-dhbckfyn2O0%2FVJczEwLZaNI%2FAAAAAAAAApw%2FeunMm3CXbJg!2e4!6s%2F%2Flh6.googleusercontent.com%2F-dhbckfyn2O0%2FVJczEwLZaNI%2FAAAAAAAAApw%2FeunMm3CXbJg%2Fw203-h100-k-no%2F!7i7304!8i3652",
      "latitude":43.4718572,
      "longitude":-80.5437525
    },
    {
      "name":"Math C&D (coffee and donuts)",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4718646,-80.5435974,3a,75y,90t\/data=!3m7!1e1!3m5!1s-padNtq4L-pw%2FVMk0r-ysDmI%2FAAAAAAAABBU%2F4Wj4v9A_IcM!2e4!6s%2F%2Flh3.googleusercontent.com%2F-padNtq4L-pw%2FVMk0r-ysDmI%2FAAAAAAAABBU%2F4Wj4v9A_IcM%2Fw203-h100-k-no%2F!7i7496!8i3748",
      "latitude":43.4718646,
      "longitude":-80.5435974
    },
    {
      "name":"Tutorial Centre, Faculty of Mathematics",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4719195,-80.543656,3a,75y,90t\/data=!3m7!1e1!3m5!1s-BzgHdFHBOy8%2FVJczXqoXa_I%2FAAAAAAAAAqQ%2FWjw8LssOSn4!2e4!6s%2F%2Flh3.googleusercontent.com%2F-BzgHdFHBOy8%2FVJczXqoXa_I%2FAAAAAAAAAqQ%2FWjw8LssOSn4%2Fw203-h100-k-no%2F!7i7320!8i3660",
      "latitude":43.4719195,
      "longitude":-80.543656
    },
    {
      "name":"Math Society office, Faculty of Mathematics",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4720207,-80.5437203,3a,75y,90t\/data=!3m7!1e1!3m5!1s-hozAQCO1F-g%2FVJeVIj08IBI%2FAAAAAAAAA3g%2FGDJ_kr-xtrI!2e4!6s%2F%2Flh3.googleusercontent.com%2F-hozAQCO1F-g%2FVJeVIj08IBI%2FAAAAAAAAA3g%2FGDJ_kr-xtrI%2Fw203-h100-k-no%2F!7i7336!8i3668",
      "latitude":43.4720207,
      "longitude":-80.5437203
    },
    {
      "name":"Environment 3",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.468221,-80.543538,3a,75y,170h,90t\/data=!3m7!1e1!3m5!1s-JDsBUkDrvM4%2FVJc21-F5-RI%2FAAAAAAAAA2Y%2FUXe9pNQUQsU!2e4!6s%2F%2Flh6.googleusercontent.com%2F-JDsBUkDrvM4%2FVJc21-F5-RI%2FAAAAAAAAA2Y%2FUXe9pNQUQsU%2Fw203-h100-k-no%2F!7i7308!8i3654",
      "latitude":43.468221,
      "longitude":-80.543538
    },
    {
      "name":"Design Studio",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4682755,-80.5433341,3a,75y,15h,90t\/data=!3m7!1e1!3m5!1s-zrpXREjkjVc%2FVJc2NMwNz3I%2FAAAAAAAAA8M%2FBO4dGkByLnM!2e4!6s%2F%2Flh3.googleusercontent.com%2F-zrpXREjkjVc%2FVJc2NMwNz3I%2FAAAAAAAAA8M%2FBO4dGkByLnM%2Fw203-h100-k-no%2F!7i7296!8i3648",
      "latitude":43.4682755,
      "longitude":-80.5433341
    },
    {
      "name":"Environment 3, 2nd floor",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4680583,-80.5434629,3a,75y,220h,90t\/data=!3m7!1e1!3m5!1s-uzxNjOeCKRY%2FVJc3D9fL55I%2FAAAAAAAAA1Q%2FEqWMAm7wMXw!2e4!6s%2F%2Flh3.googleusercontent.com%2F-uzxNjOeCKRY%2FVJc3D9fL55I%2FAAAAAAAAA1Q%2FEqWMAm7wMXw%2Fw203-h100-k-no%2F!7i7300!8i3650",
      "latitude":43.4680583,
      "longitude":-80.5434629
    },
    {
      "name":"Environment 3 foyer",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4681314,-80.5432375,3a,75y,160h,90t\/data=!3m7!1e1!3m5!1s-_H4dpsNDD7M%2FVJc2FBAvzxI%2FAAAAAAAAA1U%2FrNO-CYavyeg!2e4!6s%2F%2Flh3.googleusercontent.com%2F-_H4dpsNDD7M%2FVJc2FBAvzxI%2FAAAAAAAAA1U%2FrNO-CYavyeg%2Fw203-h100-k-no%2F!7i7288!8i3644",
      "latitude":43.4681314,
      "longitude":-80.5432375
    },
    {
      "name":"Environment 1 courtyard",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4683767,-80.5424222,3a,75y,90t\/data=!3m7!1e1!3m5!1s-MMTjdYgGYtU%2FVJc2grwGGfI%2FAAAAAAAAA1o%2FFdOi0FGuWL8!2e4!6s%2F%2Flh5.googleusercontent.com%2F-MMTjdYgGYtU%2FVJc2grwGGfI%2FAAAAAAAAA1o%2FFdOi0FGuWL8%2Fw203-h100-k-no%2F!7i7280!8i3640",
      "latitude":43.4683767,
      "longitude":-80.5424222
    },
    {
      "name":"Knowledge Integration classroom",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4683222,-80.5425938,3a,75y,90t\/data=!3m7!1e1!3m5!1s-C9CcOcU8WIQ%2FVJc2aIrBLQI%2FAAAAAAAAAss%2FnZw35mNrr0g!2e4!6s%2F%2Flh5.googleusercontent.com%2F-C9CcOcU8WIQ%2FVJc2aIrBLQI%2FAAAAAAAAAss%2FnZw35mNrr0g%2Fw203-h100-k-no%2F!7i7300!8i3650",
      "latitude":43.4683222,
      "longitude":-80.5425938
    },
    {
      "name":"Ecology lab, Faculty of Environment",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4682443,-80.5425616,3a,75y,45h,90t\/data=!3m7!1e1!3m5!1s-4GdDIlAcuts%2FVJc2vYPevTI%2FAAAAAAAAA2g%2FnzGHTZQ7g40!2e4!6s%2F%2Flh4.googleusercontent.com%2F-4GdDIlAcuts%2FVJc2vYPevTI%2FAAAAAAAAA2g%2FnzGHTZQ7g40%2Fw203-h100-k-no%2F!7i7344!8i3672",
      "latitude":43.4682443,
      "longitude":-80.5425616
    },
    {
      "name":"Coffee shop and student lounge, Faculty of Environment",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4682833,-80.5428728,3a,75y,230h,90t\/data=!3m7!1e1!3m5!1s-b6FoQYcl-S0%2FVJc2on0FZ6I%2FAAAAAAAAA2U%2FJq8-UUIXWXk!2e4!6s%2F%2Flh3.googleusercontent.com%2F-b6FoQYcl-S0%2FVJc2on0FZ6I%2FAAAAAAAAA2U%2FJq8-UUIXWXk%2Fw203-h100-k-no%2F!7i7320!8i3660",
      "latitude":43.4682833,
      "longitude":-80.5428728
    },
    {
      "name":"Lounge, St. Jerome's University",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4695525,-80.54607,3a,75y,90t\/data=!3m7!1e1!3m5!1s-ecioB89oLpE%2FVJc7cHKI92I%2FAAAAAAAAAyQ%2FG6jx5kgqVrI!2e4!6s%2F%2Flh4.googleusercontent.com%2F-ecioB89oLpE%2FVJc7cHKI92I%2FAAAAAAAAAyQ%2FG6jx5kgqVrI%2Fw203-h100-k-no%2F!7i7288!8i3644",
      "latitude":43.4695525,
      "longitude":-80.54607
    },
    {
      "name":"Double room, St. Jerome's University",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4692137,-80.5452975,3a,75y,90t\/data=!3m7!1e1!3m5!1s-Lz05_HeNrc4%2FVJc4MlI-HeI%2FAAAAAAAAAvs%2F-1KcCJBPKoA!2e4!6s%2F%2Flh5.googleusercontent.com%2F-Lz05_HeNrc4%2FVJc4MlI-HeI%2FAAAAAAAAAvs%2F-1KcCJBPKoA%2Fw203-h100-k-no%2F!7i7308!8i3654",
      "latitude":43.4692137,
      "longitude":-80.5452975
    },
    {
      "name":"Double room, St. Jerome's University",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4691754,-80.5453955,3a,75y,90t\/data=!3m7!1e1!3m5!1s-tzgTsyJyf7o%2FVTuUtdIrr9I%2FAAAAAAAABEg%2FzXoikMmRWy8!2e4!6s%2F%2Flh6.googleusercontent.com%2F-tzgTsyJyf7o%2FVTuUtdIrr9I%2FAAAAAAAABEg%2FzXoikMmRWy8%2Fw203-h100-k-no%2F!7i8330!8i3193",
      "latitude":43.4691754,
      "longitude":-80.5453955
    },
    {
      "name":"Moose room lounge, Renison University College",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.468984,-80.5478188,3a,75y,90t\/data=!3m7!1e1!3m5!1s-i8b9J-dO1Ms%2FVJc4BbPrOxI%2FAAAAAAAAAvc%2FzOZ3YYtvbeE!2e4!6s%2F%2Flh5.googleusercontent.com%2F-i8b9J-dO1Ms%2FVJc4BbPrOxI%2FAAAAAAAAAvc%2FzOZ3YYtvbeE%2Fw203-h100-k-no%2F!7i7308!8i3654",
      "latitude":43.468984,
      "longitude":-80.5478188
    },
    {
      "name":"Double room, Renison University College",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4686726,-80.5469283,3a,75y,90t\/data=!3m7!1e1!3m5!1s-VUbSrLZx01Y%2FVJc3q9bxLYI%2FAAAAAAAAAvM%2FT3ydAvReZzc!2e4!6s%2F%2Flh4.googleusercontent.com%2F-VUbSrLZx01Y%2FVJc3q9bxLYI%2FAAAAAAAAAvM%2FT3ydAvReZzc%2Fw203-h100-k-no%2F!7i7300!8i3650",
      "latitude":43.4686726,
      "longitude":-80.5469283
    },
    {
      "name":"Main foyer, University of Waterloo Stratford Campus",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.367924,-80.9820844,3a,75y,90t\/data=!3m7!1e1!3m5!1s-HJfwrmFWPAM%2FVJeVIqjJEyI%2FAAAAAAAABEw%2F0bXZ1tah2xo!2e4!6s%2F%2Flh3.googleusercontent.com%2F-HJfwrmFWPAM%2FVJeVIqjJEyI%2FAAAAAAAABEw%2F0bXZ1tah2xo%2Fw203-h100-k-no%2F!7i7276!8i3638",
      "latitude":43.367924,
      "longitude":-80.9820844
    },
    {
      "name":"Second floor, University of Waterloo Stratford Campus",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.367885,-80.9820576,3a,75y,90t\/data=!3m7!1e1!3m5!1s-0zexVbyXWTM%2FVJeVIs-sAJI%2FAAAAAAAABFM%2FjKliNTmxo-A!2e4!6s%2F%2Flh3.googleusercontent.com%2F-0zexVbyXWTM%2FVJeVIs-sAJI%2FAAAAAAAABFM%2FjKliNTmxo-A%2Fw203-h100-k-no%2F!7i7296!8i3648",
      "latitude":43.367885,
      "longitude":-80.9820576
    },
    {
      "name":"Engage Lab, University of Waterloo Stratford Campus",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.3677816,-80.9820629,3a,75y,45h,90t\/data=!3m7!1e1!3m5!1s-ymYoj8rooso%2FVJeVIpu5nvI%2FAAAAAAAAA3g%2F_dFKPSjP-6Y!2e4!6s%2F%2Flh4.googleusercontent.com%2F-ymYoj8rooso%2FVJeVIpu5nvI%2FAAAAAAAAA3g%2F_dFKPSjP-6Y%2Fw203-h100-k-no%2F!7i7296!8i3648",
      "latitude":43.3677816,
      "longitude":-80.9820629
    },
    {
      "name":"Computer Lab, University of Waterloo Stratford Campus",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.3677387,-80.9819074,3a,75y,180h,90t\/data=!3m7!1e1!3m5!1s-ZIXewPMGv_E%2FVJeVIsYws-I%2FAAAAAAAABDA%2F4YIyhU60-Ak!2e4!6s%2F%2Flh5.googleusercontent.com%2F-ZIXewPMGv_E%2FVJeVIsYws-I%2FAAAAAAAABDA%2F4YIyhU60-Ak%2Fw203-h100-k-no%2F!7i7300!8i3650",
      "latitude":43.3677387,
      "longitude":-80.9819074
    },
    {
      "name":"Fine Arts studio",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.4735389,-80.5389246,3a,75y,90t\/data=!3m7!1e1!3m5!1s-n41EqJV1k9Y%2FVJc3bpT3WGI%2FAAAAAAAABCM%2F9BDfoiw2TBQ!2e4!6s%2F%2Flh4.googleusercontent.com%2F-n41EqJV1k9Y%2FVJc3bpT3WGI%2FAAAAAAAABCM%2F9BDfoiw2TBQ%2Fw203-h100-k-no%2F!7i7316!8i3658",
      "latitude":43.4735389,
      "longitude":-80.5389246
    },
    {
      "name":"Theatre of the Arts",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/@43.4688916,-80.5431517,3a,75y,90t\/data=!3m7!1e1!3m5!1s-zxACURY7z6k%2FVJc3TEegpVI%2FAAAAAAAABCQ%2Fx7lvkksmsC4!2e4!6s%2F%2Flh4.googleusercontent.com%2F-zxACURY7z6k%2FVJc3TEegpVI%2FAAAAAAAABCQ%2Fx7lvkksmsC4%2Fw203-h100-k-no%2F!7i7296!8i3648",
      "latitude":43.4688916,
      "longitude":-80.5431517
    },
    {
      "name":"Peter Russell Rock Garden",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.471499,-80.5435916,3a,75y,260h,90t\/data=!3m7!1e1!3m5!1s-i7JAGc1Ko7s%2FU9r-GAwOyfI%2FAAAAAAAAAYU%2FdFU_p2QMY5w!2e4!6s%2F%2Flh5.googleusercontent.com%2F-i7JAGc1Ko7s%2FU9r-GAwOyfI%2FAAAAAAAAAYU%2FdFU_p2QMY5w%2Fw203-h100-k-no%2F!7i5579!8i2247",
      "latitude":43.471499,
      "longitude":-80.5435916
    },
    {
      "name":"Mike & Ophelia Lazaridis Quantum Nano Center",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4713277,-80.5441924,3a,75y,100h,90t\/data=!3m7!1e1!3m5!1s-8e1Wp-hXdyY%2FU9r-GBInKwI%2FAAAAAAAAAYU%2F9Ky6-vNyH78!2e4!6s%2F%2Flh6.googleusercontent.com%2F-8e1Wp-hXdyY%2FU9r-GBInKwI%2FAAAAAAAAAYU%2F9Ky6-vNyH78%2Fw203-h100-k-no%2F!7i6219!8i2453",
      "latitude":43.4713277,
      "longitude":-80.5441924
    },
    {
      "name":"Centre for Environmental and Information Technology",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4717443,-80.5421861,3a,75y,250h,90t\/data=!3m7!1e1!3m5!1s-KQKK8XoWGrc%2FU9r-GIpJgzI%2FAAAAAAAAATw%2FSENJGpa1c-Y!2e4!6s%2F%2Flh6.googleusercontent.com%2F-KQKK8XoWGrc%2FU9r-GIpJgzI%2FAAAAAAAAATw%2FSENJGpa1c-Y%2Fw203-h100-k-no%2F!7i6214!8i2451",
      "latitude":43.4717443,
      "longitude":-80.5421861
    },
    {
      "name":"REVelation Cafeteria",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4707901,-80.5543342,3a,75y,90t\/data=!3m7!1e1!3m5!1s-pBByK2G6Epo%2FVEZekg-3wxI%2FAAAAAAAAAdk%2Fyb1gooGEcpo!2e4!6s%2F%2Flh5.googleusercontent.com%2F-pBByK2G6Epo%2FVEZekg-3wxI%2FAAAAAAAAAdk%2Fyb1gooGEcpo%2Fw203-h100-k-no%2F!7i7906!8i3511",
      "latitude":43.4707901,
      "longitude":-80.5543342
    },
    {
      "name":"Mudie's Village 1 Cafeteria",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4714601,-80.550104,3a,75y,90t\/data=!3m7!1e1!3m5!1s-IHr1Od22djM%2FU9r-GItFiTI%2FAAAAAAAAAMw%2FDcsJREn_Dlk!2e4!6s%2F%2Flh3.googleusercontent.com%2F-IHr1Od22djM%2FU9r-GItFiTI%2FAAAAAAAAAMw%2FDcsJREn_Dlk%2Fw203-h100-k-no%2F!7i6394!8i2451",
      "latitude":43.4714601,
      "longitude":-80.550104
    },
    {
      "name":"Renison University College Cafeteria",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4689412,-80.5476364,3a,75y,90t\/data=!3m7!1e1!3m5!1s-bNvsOD_7mPQ%2FU9r-GK9oMGI%2FAAAAAAAAAYU%2FcTaC08cw16M!2e4!6s%2F%2Flh6.googleusercontent.com%2F-bNvsOD_7mPQ%2FU9r-GK9oMGI%2FAAAAAAAAAYU%2FcTaC08cw16M%2Fw203-h100-k-no%2F!7i6258!8i2451",
      "latitude":43.4689412,
      "longitude":-80.5476364
    },
    {
      "name":"Village 1 Cafeteria",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4715924,-80.5500718,3a,75y,90t\/data=!3m7!1e1!3m5!1s-RoAmJIuCO3s%2FU9r-GNEJEDI%2FAAAAAAAAAXE%2FsVTKQUQWr0o!2e4!6s%2F%2Flh4.googleusercontent.com%2F-RoAmJIuCO3s%2FU9r-GNEJEDI%2FAAAAAAAAAXE%2FsVTKQUQWr0o%2Fw203-h100-k-no%2F!7i6301!8i2433",
      "latitude":43.4715924,
      "longitude":-80.5500718
    },
    {
      "name":"St. Paul's University College",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4677035,-80.5467153,3a,75y,260h,90t\/data=!3m7!1e1!3m5!1s-_I1AmRzwhCo%2FU9r-GNKfb9I%2FAAAAAAAAASQ%2FkE9bEmetVbA!2e4!6s%2F%2Flh3.googleusercontent.com%2F-_I1AmRzwhCo%2FU9r-GNKfb9I%2FAAAAAAAAASQ%2FkE9bEmetVbA%2Fw203-h100-k-no%2F!7i6231!8i2475",
      "latitude":43.4677035,
      "longitude":-80.5467153
    },
    {
      "name":"Watson's Eatery",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4676526,-80.5464026,3a,75y,90t\/data=!3m7!1e1!3m5!1s-tHrRB99uNxY%2FU9r-GKmP3SI%2FAAAAAAAAAOE%2FL_zTrti09Os!2e4!6s%2F%2Flh6.googleusercontent.com%2F-tHrRB99uNxY%2FU9r-GKmP3SI%2FAAAAAAAAAOE%2FL_zTrti09Os%2Fw203-h100-k-no%2F!7i5548!8i2142",
      "latitude":43.4676526,
      "longitude":-80.5464026
    },
    {
      "name":"Student Design Centre, Engineering 5",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4730406,-80.5401584,3a,75y,90t\/data=!3m7!1e1!3m5!1s-w1I0F4aU5As%2FU9r-GMZjquI%2FAAAAAAAAATc%2Fbx70IpZbTkA!2e4!6s%2F%2Flh6.googleusercontent.com%2F-w1I0F4aU5As%2FU9r-GMZjquI%2FAAAAAAAAATc%2Fbx70IpZbTkA%2Fw203-h100-k-no%2F!7i6407!8i2385",
      "latitude":43.4730406,
      "longitude":-80.5401584
    },
    {
      "name":"Conrad Grebel University College",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4665391,-80.5453404,3a,75y,90t\/data=!3m7!1e1!3m5!1s-pECVXsQcjtE%2FU9r-GEzTQjI%2FAAAAAAAAAP0%2FwG0dIJiHvpY!2e4!6s%2F%2Flh6.googleusercontent.com%2F-pECVXsQcjtE%2FU9r-GEzTQjI%2FAAAAAAAAAP0%2FwG0dIJiHvpY%2Fw203-h100-k-no%2F!7i5550!8i2189",
      "latitude":43.4665391,
      "longitude":-80.5453404
    },
    {
      "name":"Double room, Conrad Grebel",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4664927,-80.5451596,3a,75y,180h,90t\/data=!3m7!1e1!3m5!1s-aGexAfNOxXw%2FU9r-GA9yBSI%2FAAAAAAAAARE%2FhURfVLX2fYw!2e4!6s%2F%2Flh6.googleusercontent.com%2F-aGexAfNOxXw%2FU9r-GA9yBSI%2FAAAAAAAAARE%2FhURfVLX2fYw%2Fw203-h100-k-no%2F!7i6252!8i2466",
      "latitude":43.4664927,
      "longitude":-80.5451596
    },
    {
      "name":"Earth Sciences Museum",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4715574,-80.5421968,3a,75y,260h,90t\/data=!3m7!1e1!3m5!1s-U43yD0Ahx3A%2FU9r-GEdZQDI%2FAAAAAAAAAYU%2F1qMRcjmuyAg!2e4!6s%2F%2Flh5.googleusercontent.com%2F-U43yD0Ahx3A%2FU9r-GEdZQDI%2FAAAAAAAAAYU%2F1qMRcjmuyAg%2Fw203-h100-k-no%2F!7i6211!8i2467",
      "latitude":43.4715574,
      "longitude":-80.5421968
    },
    {
      "name":"St. Jerome's Courtyard",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4689649,-80.5454975,3a,75y,90t\/data=!3m7!1e1!3m5!1s-gIus7GPPNWM%2FU9r-GOHt4EI%2FAAAAAAAAAPM%2FdBhftRL5rU8!2e4!6s%2F%2Flh6.googleusercontent.com%2F-gIus7GPPNWM%2FU9r-GOHt4EI%2FAAAAAAAAAPM%2FdBhftRL5rU8%2Fw203-h100-k-no%2F!7i6150!8i2494",
      "latitude":43.4689649,
      "longitude":-80.5454975
    },
    {
      "name":"Village 1",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4714838,-80.5505669,3a,75y,180h,90t\/data=!3m7!1e1!3m5!1s-X4E89OjwHrM%2FU9r-GKchVlI%2FAAAAAAAAAU0%2Fr4635ff5K8w!2e4!6s%2F%2Flh4.googleusercontent.com%2F-X4E89OjwHrM%2FU9r-GKchVlI%2FAAAAAAAAAU0%2Fr4635ff5K8w%2Fw203-h100-k-no%2F!7i6290!8i2481",
      "latitude":43.4714838,
      "longitude":-80.5505669
    },
    {
      "name":"Mackenzie King Village",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4715188,-80.5530185,3a,75y,90t\/data=!3m7!1e1!3m5!1s-u0DhmvZhq5g%2FU9sIJxhh26I%2FAAAAAAAAASE%2Fjg7feDVZ5lA!2e4!6s%2F%2Flh4.googleusercontent.com%2F-u0DhmvZhq5g%2FU9sIJxhh26I%2FAAAAAAAAASE%2Fjg7feDVZ5lA%2Fw203-h100-k-no%2F!7i6325!8i2442",
      "latitude":43.4715188,
      "longitude":-80.5530185
    },
    {
      "name":"Mackenzie King Village",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4716707,-80.5526161,3a,75y,90t\/data=!3m7!1e1!3m5!1s-S3eWCIn6zbw%2FU9r-GFjtpPI%2FAAAAAAAAANs%2FxLZOn3KocRE!2e4!6s%2F%2Flh6.googleusercontent.com%2F-S3eWCIn6zbw%2FU9r-GFjtpPI%2FAAAAAAAAANs%2FxLZOn3KocRE%2Fw203-h100-k-no%2F!7i6211!8i2467",
      "latitude":43.4716707,
      "longitude":-80.5526161
    },
    {
      "name":"Ron Eydt Village (REV) residence room",
      "url":"https:\/\/www.google.com\/maps\/contrib\/109625689197700120214\/photos\/@43.4695486,-80.5544814,3a,75y,90t\/data=!3m7!1e1!3m5!1s-U3Lyng3bS0Q%2FVEpFGx1UgAI%2FAAAAAAAAAfE%2F7DIN6QbNoDg!2e4!6s%2F%2Flh5.googleusercontent.com%2F-U3Lyng3bS0Q%2FVEpFGx1UgAI%2FAAAAAAAAAfE%2F7DIN6QbNoDg%2Fw203-h100-k-no%2F!7i7300!8i2858",
      "latitude":43.4695486,
      "longitude":-80.5544814
    }
  ]
}
```


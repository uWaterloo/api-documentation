# List blog posts for a given site

```
GET /blogs/{site}.{format}
```

## Description

> This method returns a list of all blog posts for a given site

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
    <td>1789</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>blogs</td>
    <td><b>Service ID</b></td>
    <td>337</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Each individual site's data steward</td>
    <td><b>Data Type</b></td>
    <td>Direct DB Connection</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Realtime</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources



## Parameters

```
GET /blogs/{site}.{format}
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
    <td>Site ID</td>
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
GET /blogs/{site}.{format}
```

- **https://api.uwaterloo.ca/v2/blogs/student-success.json**
- **https://api.uwaterloo.ca/v2/blogs/student-success.xml**
- **https://api.uwaterloo.ca/v2/blogs/student-success.json?callback=myResponse**


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
    <td>Post id</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Blog post title</td>
  </tr>
  <tr>
    <td><b>teaser_raw</b></td>
    <td>string</td>
    <td>Blog post excerpt with HTML</td>
  </tr>
  <tr>
    <td><b>teaser</b></td>
    <td>string</td>
    <td>Blog post excerpt</td>
  </tr>
  <tr>
    <td><b>publisher</b></td>
    <td>string</td>
    <td>Author name</td>
  </tr>
  <tr>
    <td><b>delegated_author</b></td>
    <td>string</td>
    <td>Delegated author's name</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>Blog post URL</td>
  </tr>
  <tr>
    <td><b>published</b></td>
    <td>datetime</td>
    <td>Date published</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>datetime</td>
    <td>Last updated</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":811464,
    "timestamp":1453154507,
    "status":200,
    "message":"Request successful",
    "method_id":1789,
    "method":{
      
    }
  },
  "data":[
    {
      "id":7721,
      "title":"Student graces St. Paul&#039;s with six-foot-tall artwork",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Rachel Isabelle Hammermueller",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/student-graces-st-pauls-six-foot-tall-artwork",
      "published":"2016-01-14T00:00:00",
      "updated":"2016-01-15T09:29:26-05:00"
    },
    {
      "id":7531,
      "title":"Math student spins deal with a dragon",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/math-student-spins-deal-dragon",
      "published":"2015-12-18T00:00:00",
      "updated":"2016-01-13T08:20:08-05:00"
    },
    {
      "id":7513,
      "title":"Student artist tackles gender binary with Sex Symbol",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/student-artist-tackles-gender-binary-sex-symbol",
      "published":"2015-12-10T00:00:00",
      "updated":"2015-12-10T15:55:37-05:00"
    },
    {
      "id":7499,
      "title":"Step aside Shakespeare - there are new wordsmiths in town",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/step-aside-shakespeare-there-are-new-wordsmiths-town",
      "published":"2015-12-07T00:00:00",
      "updated":"2015-12-08T15:32:11-05:00"
    },
    {
      "id":7473,
      "title":"A picture is worth 1,000 words",
      "teaser_raw":"<p><img alt=\"IEW photo contest winners\" class=\"image-body-500px-wide\" height=\"166\" src=\"\/student-success\/sites\/ca.student-success\/files\/styles\/body-500px-wide\/public\/uploads\/images\/screen_shot_2015-12-03_at_11.40.23_am.png?itok=FIlEJFL5\" width=\"500\" \/>Each year, the <em>Where in the world<\/em> photo contest is one of the highlights of International Education Week. Out of the 16 finalists, <a href=\"https:\/\/uwaterloo.ca\/find-out-more\/programs\/management-engineering\">Management Engineering<\/a> students Juana Attieh and Yahya Wahbeh managed to take first place for their <a href=\"https:\/\/uwaterloo.ca\/co-operative-education\/working-abroad\/international-photo-contest-2015\">submissions<\/a>.<\/p>",
      "teaser":"Each year, the Where in the world photo contest is one of the highlights of International Education Week. Out of the 16 finalists, Management Engineering students Juana Attieh and Yahya Wahbeh managed to take first place for their submissions.",
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/picture-worth-1000-words",
      "published":"2015-12-03T00:00:00",
      "updated":"2015-12-03T11:52:23-05:00"
    },
    {
      "id":7467,
      "title":"M\u00e9tis grad student tackles gender violence in Beijing",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/metis-grad-student-tackles-gender-violence-beijing",
      "published":"2015-12-01T00:00:00",
      "updated":"2015-12-02T08:44:31-05:00"
    },
    {
      "id":7437,
      "title":"UWaterloo muggles organize cross-province Quidditch tournament",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/uwaterloo-muggles-organize-cross-province-quidditch",
      "published":"2015-11-26T00:00:00",
      "updated":"2015-11-27T08:50:46-05:00"
    },
    {
      "id":7422,
      "title":"Playing with time at Unity (1918)",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/playing-time-unity-1918",
      "published":"2015-11-24T00:00:00",
      "updated":"2015-11-24T20:05:32-05:00"
    },
    {
      "id":7379,
      "title":"Jamaican exchange student brings her research to UWaterloo",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/jamaican-exchange-student-brings-her-research-uwaterloo",
      "published":"2015-11-19T00:00:00",
      "updated":"2015-11-19T10:59:26-05:00"
    },
    {
      "id":7360,
      "title":"Student speaks at Canada&#039;s largest chemical physics conference",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/student-speaks-canadas-largest-chemical-physics-conference",
      "published":"2015-11-17T00:00:00",
      "updated":"2015-12-17T10:52:19-05:00"
    },
    {
      "id":7301,
      "title":"UWaterloo Students organize fourth TEDxUW event",
      "teaser_raw":null,
      "teaser":null,
      "publisher":"Aliaksandr Bahdanovich",
      "delegated_author":null,
      "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/uwaterloo-students-organize-fourth-tedxuw-event",
      "published":"2015-11-10T00:00:00",
      "updated":"2015-11-10T15:40:12-05:00"
    }
  ]
}
```


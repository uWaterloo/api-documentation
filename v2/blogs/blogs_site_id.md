# List blog posts details for a given id

```
GET /blogs/{site}/{id}.{format}
```

## Description

> This method returns a blog posts details for a post id

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
    <td>1801</td>
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
GET /blogs/{site}/{id}.{format}
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
    <td><b>id</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Post ID</td>
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
GET /blogs/{site}/{id}.{format}
```

- **https://api.uwaterloo.ca/v2/blogs/student-success/7721.json**
- **https://api.uwaterloo.ca/v2/blogs/student-success/7721.xml**
- **https://api.uwaterloo.ca/v2/blogs/student-success/7721.json?callback=myResponse**


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
    <td><b>description_raw</b></td>
    <td>string</td>
    <td>Blog post content with HTML</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>Blog post content</td>
  </tr>
  <tr>
    <td><b>publisher</b></td>
    <td>string</td>
    <td>Author name</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>list</td>
    <td>Blog post audience tags</td>
  </tr>
  <tr>
    <td><b>delegated_author</b></td>
    <td>string</td>
    <td>Delegated author's name</td>
  </tr>
  <tr>
    <td><b>podcast_url</b></td>
    <td>string</td>
    <td>URL of the podcast audio file (if applicable)</td>
  </tr>
  <tr>
    <td><b>transcript_url</b></td>
    <td>string</td>
    <td>Audio transcript url (if applicable)</td>
  </tr>
  <tr>
    <td><b>publisher</b></td>
    <td>string</td>
    <td>Author watiam id</td>
  </tr>
  <tr>
    <td><b>site_id</b></td>
    <td>string</td>
    <td>Blog post site's id</td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Blog post site's name</td>
  </tr>
  <tr>
    <td><b>revision_id</b></td>
    <td>integer</td>
    <td>Blog post revision identifier</td>
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
    "requests":811472,
    "timestamp":1453154836,
    "status":200,
    "message":"Request successful",
    "method_id":1801,
    "method":{
      
    }
  },
  "data":{
    "id":7721,
    "title":"Student graces St. Paul&#039;s with six-foot-tall artwork",
    "description":"This art piece\u00a0may be a tad too large to hang above your bed.\n\nSOPOR,\u00a0meaning \u201ca deep sleep,\u201d is a massive\u00a0dream catcher made of tulle, rope, twine, PVC tubing, rocks and shells.\u00a0The artist is\u00a0Melissa Johns, an Honours Arts and Business Co-op student majoring in Studio Arts.\u00a0\n\nFor Melissa, creating SOPOR was an opportunity to feel connected to her community and to celebrate her Mohawk and Upper Cayuga heritage.\u00a0At the same time, this piece allowed her to explore deeper questions of identity, tradition and belonging as a\u00a0native person in contemporary Canadian society.\n\n\n\t\u201cThe work revolved around cultural disconnect and anxiety, and I discovered that's actually a really common experience for other students from aboriginal backgrounds.\"\n\n\nPrimarily a digital artist, Melissa has been moving to pieces that include an interactive dimension.\n\n\n\t\u201cI really like pieces that facilitate some kind of personal connection among viewers whether with each other or the work\u201d.\n\n\nAlthough SOPOR now hangs on a wall, its creation was a\u00a0performance art piece and represented Melissa's first foray into this genre of art.\u00a0\n\n\n\t\u201cI began the performance by laying in front of the suspended frame, and then\u00a0wove the rope into a web and decorated it with the rocks and shells.\"\n\n\nAfter an hour and a half of careful work, Melissa laid down under the six-foot\u00a0piece\u00a0to complete the performance.\n\nCurrently in her final year here at the University of Waterloo, Melissa rarely has\u00a0to hunt\u00a0for inspiration when it comes to displaying her creativity.\u00a0\n\n\n\t\u201cI find myself musing a lot on the beauty of flawed things, in intimate and emotive expression between people, and esoteric ritual. Though I work in quite a few different media, a common thread between many of my works is a kind of rooted sentimentality\u201d.\n\n\nSOPOR\u00a0appeared in\u00a0the\u00a0Waterloo Chronicle\u00a0in November\u00a0and\u00a0the artist was recently featured in\u00a0ArtsOnline\u00a0published by the UWaterloo\u00a0Faculty of Arts.\u00a0\n\nCheck out Melissa\u2019s personal\u00a0website to learn more about her artistic process and to view her other work.\u00a0\n\nTo view\u00a0SOPOR\u00a0in person, visit the\u00a0Aboriginal Education Centre\u00a0at\u00a0St. Paul\u2019s University College.\u00a0The Centre\u00a0invites students and community members to join for\u00a0soup and\u00a0bannock\u00a0every Thursday\u00a0from noon to\u00a01pm\u00a0and traditional crafting from\u00a01-3pm.\u00a0",
    "description_raw":"<p><img alt=\"Melissa Johns standing beside dream catcher art piece on wall\" class=\"image-body-500px-wide\" height=\"606\" src=\"\/student-success\/sites\/ca.student-success\/files\/styles\/body-500px-wide\/public\/uploads\/images\/screen_shot_2016-01-08_at_2.16.58_pm.png?itok=mRDR8uzM\" width=\"500\" \/><\/p>\n\n<p>This art piece\u00a0may be a tad too large to hang above your bed.<\/p>\n\n<p>SOPOR,\u00a0m<span>eaning \u201ca deep sleep,\u201d is a massive\u00a0dream catcher made of tulle, rope, twine, PVC tubing, rocks and shells.\u00a0<\/span>The artist is\u00a0Melissa Johns, an <a href=\"https:\/\/uwaterloo.ca\/find-out-more\/programs\/arts-and-business\">Honours Arts and Business<\/a> Co-op student majoring in <a href=\"https:\/\/uwaterloo.ca\/fine-arts\/about\/program-listings\/studio-art\">Studio Arts<\/a>.\u00a0<\/p>\n\n<p>For <span>Melissa<\/span>, creating SOPOR was an opportunity to feel connected to her community and to celebrate her Mohawk and Upper Cayuga heritage.\u00a0At the same time, this piece allowed her to explore deeper questions of identity, tradition and belonging as a\u00a0native person in contemporary Canadian society.<\/p>\n\n<blockquote>\n\t<p>\u201cThe work revolved around cultural disconnect and anxiety, and I discovered that's actually a really common experience for other students from aboriginal backgrounds.\"<\/p>\n<\/blockquote>\n\n<p>Primarily a digital artist, Melissa has been moving to pieces that include an interactive dimension.<\/p>\n\n<blockquote>\n\t<p>\u201cI really like pieces that facilitate some kind of personal connection among viewers whether with each other or the work\u201d.<\/p>\n<\/blockquote>\n\n<p>Although SOPOR now hangs on a wall, its creation was a\u00a0performance art piece and represented Melissa's first foray into this genre of art.\u00a0<\/p>\n\n<blockquote>\n\t<p>\u201cI began the performance by laying in front of the suspended frame, and then\u00a0wove the rope into a web and decorated it with the rocks and shells.\"<\/p>\n<\/blockquote>\n\n<p>After an hour and a half of careful work, Melissa laid down under the six-foot\u00a0piece\u00a0to complete the performance.<\/p>\n\n<p>Currently in her final year here at the University of Waterloo, Melissa rarely has\u00a0to hunt\u00a0for inspiration when it comes to displaying her creativity.\u00a0<\/p>\n\n<blockquote>\n\t<p>\u201cI find myself musing a lot on the beauty of flawed things, in intimate and emotive expression between people, and esoteric ritual. Though I work in quite a few different media, a common thread between many of my works is a kind of rooted sentimentality\u201d.<\/p>\n<\/blockquote>\n\n<p>SOPOR<span>\u00a0appeared in<\/span><span>\u00a0the\u00a0<\/span><a href=\"http:\/\/uwaterloo.ca\/fine-arts\/news\/photograph-fine-arts-student-cover-waterloo-chronicle\">Waterloo Chronicle<\/a><span>\u00a0in November\u00a0and\u00a0<\/span><span>the artist was recently featured in<\/span><span>\u00a0<\/span><a href=\"https:\/\/artsonline.uwaterloo.ca\/stories\/melissa\/\">ArtsOnline<\/a><span>\u00a0published by the UWaterloo\u00a0<\/span><a href=\"https:\/\/uwaterloo.ca\/arts\/\">Faculty of Arts<\/a><span>.\u00a0<\/span><\/p>\n\n<p><span>Check out<\/span><span> Melissa\u2019s <\/span><a href=\"http:\/\/melissajohns.com\/\">personal\u00a0website<\/a><span> to learn more about her artistic process and to view her other work.\u00a0<\/span><\/p>\n\n<p>To view\u00a0SOPOR\u00a0in person, visit the\u00a0<a href=\"http:\/\/uwaterloo.ca\/stpauls\/waterloo-aboriginal-education-centre\">Aboriginal Education Centre<\/a>\u00a0at\u00a0<a href=\"http:\/\/uwaterloo.ca\/stpauls\/\">St. Paul\u2019s University College<\/a>.\u00a0The Centre\u00a0invites students and community members to join for\u00a0<a href=\"https:\/\/uwaterloo.ca\/stpauls\/waterloo-aboriginal-education-centre\/soup-and-bannock-days\">soup and\u00a0bannock<\/a><a href=\"https:\/\/uwaterloo.ca\/stpauls\/waterloo-aboriginal-education-centre\/soup-and-bannock-days\">\u00a0every Thursday<\/a>\u00a0from noon to\u00a01pm\u00a0and traditional crafting from\u00a01-3pm.\u00a0<\/p>",
    "audience":[
      "Current students",
      "Current undergraduate students",
      "Current graduate students",
      "Faculty",
      "Staff"
    ],
    "delegated_author":null,
    "podcast_url":null,
    "transcript_url":null,
    "publisher":"rihammer",
    "site_id":"student-success",
    "site_name":"Student Success Office",
    "revision_id":12710,
    "published":"2016-01-14",
    "updated":"2016-01-15T09:29:26-05:00",
    "link":"https:\/\/uwaterloo.ca\/student-success\/blog\/post\/student-graces-st-pauls-six-foot-tall-artwork"
  }
}
```


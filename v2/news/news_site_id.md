# Get News for Site given id

```
GET news/{site}/{id}.{format}
```

## Description

> Array

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
    <td>1709</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>news</td>
    <td><b>Service ID</b></td>
    <td>307</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Each individual site's data steward</td>
    <td><b>Data Type</b></td>
    <td>Database</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Realtime</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- This is a 'realtime' feed. An item will be available on the api the second its up using Webhooks
- Any value can be `null`


### Sources

- Crawled from all WMCS sites listed at https://api.uwaterloo.ca/v2/resources/sites.{format}


## Parameters

```
GET news/{site}/{id}.{format}
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
    <td><b>site</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid site slug from /resources/sites</td>
  </tr>
  <tr>
    <td><b>id</b></td>
    <td>input</td>
    <td><i>yes</i></td>
    <td>Valid news id</td>
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
GET news/{site}/{id}.{format}
```

- **https://api.uwaterloo.ca/v2/news/science/881.json**
- **https://api.uwaterloo.ca/v2/news/science/881.xml**
- **https://api.uwaterloo.ca/v2/news/science/881.json?callback=myResponse**


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
    <td>Unique news id</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>News title</td>
  </tr>
  <tr>
    <td><b>description</b></td>
    <td>string</td>
    <td>News body</td>
  </tr>
  <tr>
    <td><b>description_raw</b></td>
    <td>string</td>
    <td>Raw news body (includes HTML markup)</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>list</td>
    <td>Audience targeted by news item</td>
  </tr>
  <tr>
    <td><b>image</b></td>
    <td>object</td>
    <td>Image representing the news item<br><table>
  <tr>
    <td><b>id</b></td>
    <td>integer</td>
    <td>Unique id of image</td>
  </tr>
  <tr>
    <td><b>file</b></td>
    <td>string</td>
    <td>Relative link to image file path in filename.{format}</td>
  </tr>
  <tr>
    <td><b>alt</b></td>
    <td>string</td>
    <td>Image alternate text</td>
  </tr>
  <tr>
    <td><b>mime</b></td>
    <td>string</td>
    <td>Image MIME type in "string/{format}"</td>
  </tr>
  <tr>
    <td><b>size</b></td>
    <td>integer</td>
    <td>Image file size in bytes</td>
  </tr>
  <tr>
    <td><b>width</b></td>
    <td>integer</td>
    <td>Image width in pixels</td>
  </tr>
  <tr>
    <td><b>height</b></td>
    <td>integer</td>
    <td>Image height in pixels</td>
  </tr>
  <tr>
    <td><b>url</b></td>
    <td>string</td>
    <td>Full link to image resource</td>
  </tr>
</table>
</td>
  </tr>
  <tr>
    <td><b>site_id</b></td>
    <td>string</td>
    <td>Site slug as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>site_name</b></td>
    <td>string</td>
    <td>Full site name as from https://api.uwaterloo.ca/v2/resources/sites.{format}</td>
  </tr>
  <tr>
    <td><b>revision_id</b></td>
    <td>integer</td>
    <td>Unique id of revision of news item</td>
  </tr>
  <tr>
    <td><b>published</b></td>
    <td>date</td>
    <td>ISO 8601 formatted published date</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>date</td>
    <td>ISO 8601 formatted updated date</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>URL of news link</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
  "meta":{
    "requests":489,
    "timestamp":1399701947,
    "status":200,
    "message":"Request successful",
    "method_id":1709,
    "method":{
      
    }
  },
  "data":{
    "id":881,
    "title":"Do you see what I see? The new frontier of astronomy",
    "description":"Traditionally, astronomy was limited to studying objects we could see, such as the stars and planets. But a new submillimeter telescope the largest, highest and most precise of its kind will soon change that.Many of the most interesting objects in the Universe emit light in the far-infrared and submillimeter range, which is invisible to the naked eye, said astronomer Michel Fich from the University of Waterloo.The Cerro Chajnantor Atacama Telescope (CCAT) will be the largest and most powerful submillimeter telescope in the world.Michel Fich, a professor in the Department of Physics and Astronomy in the Faculty of Science, is leading a group of eight Canadian universities in an international effort to build CCAT a $150-million state-of-the-art submillimeter telescope that ll give astronomers a peek at the Universe as it was 10 to 12 billion years ago.While optical telescopes are great for observing light-emitting objects such as stars, submillimeter telescopes are perfect for probing dark, cold interstellar material in the Universe, such as black holes and primordial radiation emitted after the Big Bang.We're trying to understand our history and the origins of the universe,\" said Fich. \"We live in this galaxy and we really don't know a lot about it.\"The CCAT will help astronomers answer questions about how galaxies collide, merge, interact and evolved. It ll also help scientists learn more about the formation of planets, stars and solar systems.With a dish 25-meters in diameter CCAT is designed to capture a very wide view of space. Although it s not the first submillimeter telescope it will be substantially larger and 100 times more sensitive than its predecessor. Outfitted with a state-of-the-art camera, CCAT is expected to map the sky 1,000 times faster, and with better resolution, than the best detector in the world.The CCAT will be built 5,600 metres above sea level near the summit of Cerro Chajnantor in the Chilean Atacama desert. Submillimeter telescopes are effective only at elevations above 4000 metres as the Earth s atmosphere blocks much of this important wavelength range.In addition to gathering research data this international facility will also serve as a world-class training facility for students from more than 14 universities.CCAT is scheduled to be operational by 2020.",
    "description_raw":"<p><img alt=\"Artist rendition of the Cerro Chajnantor Atacama Telescope.\" class=\"image-sidebar-220px-wide image-right\" height=\"147\" src=\"\/science\/sites\/ca.science\/files\/styles\/sidebar-220px-wide\/public\/uploads\/images\/ccat_rendering.jpg_1.jpeg?itok=mKBlgOI1\" width=\"220\" \/>Traditionally, astronomy was limited to studying objects we could see, such as the stars and planets. But a new submillimeter telescope \u2013 the largest, highest and most precise of its kind \u2013 will soon change that.<\/p>\n<blockquote>\n\t<p>Many of the most interesting objects in the Universe emit light in the far-infrared and submillimeter range, which is invisible to the naked eye,\u201d said astronomer Michel Fich from the University of Waterloo.<\/p>\n<\/blockquote>\n<p>The Cerro Chajnantor Atacama Telescope (CCAT) will be the largest and most powerful submillimeter telescope in the world.<\/p>\n<p><a href=\"https:\/\/uwaterloo.ca\/physics-astronomy\/people-profiles\/michel-fich\">Michel Fich<\/a>, a professor in the <a href=\"https:\/\/uwaterloo.ca\/physics-astronomy\/\">Department of Physics and Astronomy<\/a> in the Faculty of Science, is leading a group of eight Canadian universities in an international effort to build CCAT \u2013 a $150-million state-of-the-art submillimeter telescope that\u2019ll give astronomers a peek at the Universe as it was 10 to 12 billion years ago.<\/p>\n<p>While optical telescopes are great for observing light-emitting objects such as stars, submillimeter telescopes are perfect for probing dark, cold interstellar material in the Universe, such as black holes and primordial radiation emitted after the Big Bang.<\/p>\n<blockquote>\n\t<p>We're trying to understand our history and the origins of the universe,\" said Fich. \"We live in this galaxy and we really don't know a lot about it.\"<\/p>\n<\/blockquote>\n<p>The CCAT will help astronomers answer questions about how galaxies collide, merge, interact and evolved. It\u2019ll also help scientists learn more about the formation of planets, stars and solar systems.<\/p>\n<p>With a dish 25-meters in diameter CCAT is designed to capture a very wide view of space. Although it\u2019s not the first submillimeter telescope it will be substantially larger and 100 times more sensitive than its predecessor. Outfitted with a state-of-the-art camera, CCAT is expected to map the sky 1,000 times faster, and with better resolution, than the best detector in the world.<\/p>\n<p>The CCAT will be built 5,600 metres above sea level near the summit of Cerro Chajnantor in the Chilean Atacama desert. Submillimeter telescopes are effective only at elevations above 4000 metres as the Earth\u2019s atmosphere blocks much of this important wavelength range.<\/p>\n<p>In addition to gathering research data this international facility will also serve as a world-class training facility for students from more than 14 universities.<\/p>\n<p>CCAT is scheduled to be operational by 2020.<\/p>",
    "audience":[
      
    ],
    "image":{
      "id":981,
      "file":"ccat_rendering.jpg_1.jpeg",
      "alt":"Artist rendition of the Cerro Chajnantor Atacama Telescope.",
      "mime":"image\/jpeg",
      "size":2403204,
      "width":2304,
      "height":1536,
      "url":"https:\/\/uwaterloo.ca\/science\/sites\/ca.science\/files\/uploads\/images\/ccat_rendering.jpg_1.jpeg"
    },
    "site_id":"science",
    "site_name":"Science",
    "revision_id":6543,
    "published":"2014-05-09T00:00:00-04:00",
    "updated":"2014-05-09T13:51:36-04:00",
    "link":"https:\/\/uwaterloo.ca\/science\/news\/do-you-see-what-i-see-new-frontier-astronomy"
  }
}
```


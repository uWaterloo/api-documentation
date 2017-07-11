# Important dates by term

```
GET /terms/{term_id}/importantdates.{format}
```

## Description

> This method returns all important dates for the requested term.

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
    <td>1188</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>terms</td>
    <td><b>Service ID</b></td>
    <td>241</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>Registrar</td>
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

- Any value can be `null`


### Sources

- https://uwaterloo.ca/quest/undergraduate-students/important-dates


## Parameters

```
GET /terms/{term_id}/importantdates.{format}
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
</table>

**Output Formats**

- json
- xml


## Examples

```
GET /terms/{term_id}/importantdates.{format}
```

- **https://api.uwaterloo.ca/v2/terms/1179/importantdates.json**
- **https://api.uwaterloo.ca/v2/terms/1179/importantdates.xml**
- **https://api.uwaterloo.ca/v2/terms/1179/importantdates.json?callback=myResponse**


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
    <td>Important date ID</td>
  </tr>
  <tr>
    <td><b>title</b></td>
    <td>string</td>
    <td>Title of the important date</td>
  </tr>
  <tr>
    <td><b>body</b></td>
    <td>string</td>
    <td>Description of the important date</td>
  </tr>
  <tr>
    <td><b>body_raw</b></td>
    <td>string</td>
    <td>Description of the important date (without HTML tags removed)</td>
  </tr>
  <tr>
    <td><b>special_notes</b></td>
    <td>string</td>
    <td>Special notes for the important date</td>
  </tr>
  <tr>
    <td><b>special_notes_raw</b></td>
    <td>string</td>
    <td>Special notes for the important date (without HTML tags removed)</td>
  </tr>
  <tr>
    <td><b>audience</b></td>
    <td>list<string></td>
    <td>Audience for the important date</td>
  </tr>
  <tr>
    <td><b>term</b></td>
    <td>string</td>
    <td>Term name (e.g. `"Fall 2017"`) that the important date applies to</td>
  </tr>
  <tr>
    <td><b>term_id</b></td>
    <td>integer</td>
    <td>Term ID (e.g. `1179`) that the important date applies to</td>
  </tr>
  <tr>
    <td><b>start_date</b></td>
    <td>string</td>
    <td>Start date of the important date</td>
  </tr>
  <tr>
    <td><b>end_date</b></td>
    <td>string</td>
    <td>End date of the important date</td>
  </tr>
  <tr>
    <td><b>date_tbd</b></td>
    <td>boolean</td>
    <td>If the date of the important date is *To be determined*</td>
  </tr>
  <tr>
    <td><b>date_na</b></td>
    <td>boolean</td>
    <td>If the important date is *Not Applicable* for this term</td>
  </tr>
  <tr>
    <td><b>link</b></td>
    <td>string</td>
    <td>Link to the WCMS page containing the important date</td>
  </tr>
  <tr>
    <td><b>site</b></td>
    <td>string</td>
    <td>Site slug representing the source of the important date</td>
  </tr>
  <tr>
    <td><b>vid</b></td>
    <td>integer</td>
    <td>Version ID of the important date</td>
  </tr>
  <tr>
    <td><b>updated</b></td>
    <td>string</td>
    <td>Timestamp of when data was last updated</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json
{
    "meta": {
        "requests": 1011870,
        "timestamp": 1499801401,
        "status": 200,
        "message": "Request successful",
        "method_id": 1188,
        "method": {
            "disclaimer": "Review the 'No Warranty' section of the University of Waterloo Open Data License before using this data. If building services upon this data, please inform your users of the inherent risks (as a best practice)",
            "license": "https:\/\/uwaterloo.ca\/open-data\/university-waterloo-open-data-license-agreement-v1"
        }
    },
    "data": [
        {
            "id": 568,
            "title": "Course selection period",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-05-23",
            "end_date": "2017-05-29",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/567",
            "site": "important-dates-ro",
            "vid": 79053,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 570,
            "title": "Course selection period",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-07-04",
            "end_date": "2017-07-10",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/567",
            "site": "important-dates-ro",
            "vid": 79055,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 578,
            "title": "Drop\/add period begins",
            "body": "View appointment time for the beginning of drop\/add.",
            "body_raw": "<p><a href=\"https:\/\/uwaterloo.ca\/quest\/help\/students\/how-do-i\/view-my-appointment-time-beginning-drop-add\">View appointment time for the beginning of drop\/add.<\/a><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-07-20",
            "end_date": "2017-07-20",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/577",
            "site": "important-dates-ro",
            "vid": 79062,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 580,
            "title": "Drop\/add period begins",
            "body": "View appointment time for the beginning of drop\/add.",
            "body_raw": "<p><a href=\"https:\/\/uwaterloo.ca\/quest\/help\/students\/how-do-i\/view-my-appointment-time-beginning-drop-add\">View appointment time for the beginning of drop\/add.<\/a><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-07-24",
            "end_date": "2017-07-24",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/577",
            "site": "important-dates-ro",
            "vid": 79064,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 588,
            "title": "Fees due date",
            "body": "If you are not \"Fees Arranged\", your access to LEARN may be affected. View more information.",
            "body_raw": "<p><em>If you are not <a href=\"https:\/\/uwaterloo.ca\/finance\/student-financial-services\/how-become-fees-arranged\">\"Fees Arranged\"<\/a>, your access to LEARN may be affected. <a href=\"https:\/\/uwaterloo.ca\/finance\/student-financial-services\">View more information.<\/a><\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-08-23",
            "end_date": "2017-08-23",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/587",
            "site": "important-dates-ro",
            "vid": 78955,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 595,
            "title": "Late fees begin",
            "body": "View more information.",
            "body_raw": "<p><a href=\"https:\/\/uwaterloo.ca\/finance\/student-financial-services\">View more information.<\/a><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-08-24",
            "end_date": "2017-08-24",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/594",
            "site": "important-dates-ro",
            "vid": 78969,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 609,
            "title": "Orientation week",
            "body": "View Orientation website for students enrolling for the first time at Waterloo.",
            "body_raw": "<p>View <a href=\"https:\/\/uwaterloo.ca\/orientation\/\">Orientation website<\/a> for students enrolling for the <strong>first time<\/strong> at Waterloo.<\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-03",
            "end_date": "2017-09-09",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/608",
            "site": "important-dates-ro",
            "vid": 79011,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 25,
            "title": "Labour Day",
            "body": "University holiday",
            "body_raw": "<p><em><a href=\"https:\/\/uwaterloo.ca\/human-resources\/support-employees\/payroll\/paid-holidays\">University holiday<\/a><\/em><\/p>",
            "special_notes": "(M)",
            "special_notes_raw": "<p>(M)<\/p>",
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-04",
            "end_date": "2017-09-04",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/24",
            "site": "important-dates-ro",
            "vid": 78843,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 602,
            "title": "Co-operative work term begins",
            "body": "Actual dates may vary depending on employer or student requirements.",
            "body_raw": "<p><em>Actual dates may vary depending on employer or student requirements<\/em>.<\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-05",
            "end_date": "2017-09-05",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/601",
            "site": "important-dates-ro",
            "vid": 79018,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 623,
            "title": "Lectures or classes begin at UWaterloo",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-07",
            "end_date": "2017-09-07",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/622",
            "site": "important-dates-ro",
            "vid": 79039,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 616,
            "title": "Lectures or classes begin at Laurier",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-07",
            "end_date": "2017-09-07",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/615",
            "site": "important-dates-ro",
            "vid": 79032,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 638,
            "title": "Last day to select examination centres for online courses.",
            "body": "View in Quest.",
            "body_raw": "<p><em>View in <a href=\"https:\/\/uwaterloo.ca\/quest\/home\">Quest<\/a><\/em>.<\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-17",
            "end_date": "2017-09-17",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/637",
            "site": "important-dates-ro",
            "vid": 79141,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 645,
            "title": "Add period ends",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-20",
            "end_date": "2017-09-20",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/644",
            "site": "important-dates-ro",
            "vid": 79071,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 652,
            "title": "New Waterloo Science students English Language Proficiency exam dates.",
            "body": "View details on the Communication Requirement website.",
            "body_raw": "<p><em>View details on the <a href=\"https:\/\/uwaterloo.ca\/communication-requirement\/writing-english-language-proficiency-exam\/elpe-dates\">Communication Requirement<\/a> website<\/em>.<\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-22",
            "end_date": "2017-09-23",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/651",
            "site": "important-dates-ro",
            "vid": 78983,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 666,
            "title": "New Waterloo Arts students in programs from GBDA, AFM, and CFM departments, FALL term English Language Proficiency exam date",
            "body": "View details on the Communication Requirement website",
            "body_raw": "<p><em>View details on the <a href=\"https:\/\/uwaterloo.ca\/communication-requirement\/writing-english-language-proficiency-exam\/elpe-dates\">Communication Requirement<\/a> website<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-23",
            "end_date": "2017-09-23",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/665",
            "site": "important-dates-ro",
            "vid": 78997,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 659,
            "title": "New Waterloo Engineering students FALL term English Language Proficiency exam date",
            "body": "View details on the Communication Requirement website",
            "body_raw": "<p><em>View details on the <a href=\"https:\/\/uwaterloo.ca\/communication-requirement\/writing-english-language-proficiency-exam\/elpe-dates\">Communication Requirement<\/a> website<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-23",
            "end_date": "2017-09-23",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/658",
            "site": "important-dates-ro",
            "vid": 78990,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 673,
            "title": "Drop, no penalty period ends",
            "body": "Deadline to withdraw from courses with 100% tuition refund.",
            "body_raw": "<p><em><a href=\"https:\/\/uwaterloo.ca\/finance\/student-financial-services\">Deadline to withdraw from courses with 100% tuition refund.<\/a><\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-27",
            "end_date": "2017-09-27",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/672",
            "site": "important-dates-ro",
            "vid": 79078,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 680,
            "title": "Drop, penalty 1 period begins",
            "body": "WD (Withdrew, no credit granted) grade assigned for course(s) dropped during this period",
            "body_raw": "<p><em>WD (Withdrew, no credit granted) <\/em><em>grade assigned <\/em><em>for course(s) dropped<\/em><em> during this period<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-09-28",
            "end_date": "2017-09-28",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/679",
            "site": "important-dates-ro",
            "vid": 79085,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 28,
            "title": "Thanksgiving Day",
            "body": "University holiday",
            "body_raw": "<p><em><a href=\"https:\/\/uwaterloo.ca\/human-resources\/support-employees\/payroll\/paid-holidays\">University holiday<\/a><\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-09",
            "end_date": "2017-10-09",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/27",
            "site": "important-dates-ro",
            "vid": 78850,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 687,
            "title": "Study Days",
            "body": "Co-operative employment interviews may continue during these periods.\n\n*Fall term study days also known as \u201cFall Break\u201d\n\n*Winter term study days also known as \"Reading Week\"",
            "body_raw": "<p><em>Co-operative employment interviews may continue during these periods.<\/em><\/p>\n\n<p><em>*Fall term study days also known as \u201cFall Break\u201d<\/em><\/p>\n\n<p><em>*Winter term study days also known as \"Reading Week\"<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-10",
            "end_date": "2017-10-11",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/686",
            "site": "important-dates-ro",
            "vid": 78948,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 694,
            "title": "Make-up day for October 10",
            "body": "The loss of a Tuesday class on October 10 (study day) will be made up by following a Tuesday schedule on October 12.",
            "body_raw": "<p><em>The loss of a Tuesday class on October 10 (study day) will be made up by following a Tuesday schedule on October 12.<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-12",
            "end_date": "2017-10-12",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/693",
            "site": "important-dates-ro",
            "vid": 78864,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 697,
            "title": "Make-up day for October 11",
            "body": "The loss of a Wednesday class on October 11 (study day) will be made up by following a Wednesday schedule on October 13.",
            "body_raw": "<p><em>The loss of a Wednesday class on October 11 (study day) will be made up by following a Wednesday schedule on October 13.<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-13",
            "end_date": "2017-10-13",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/696",
            "site": "important-dates-ro",
            "vid": 78871,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 710,
            "title": "Opportunity to adjust your online course exam location",
            "body": "View: How do I view my online course exam schedule?",
            "body_raw": "<p><em>View: <a href=\"https:\/\/uwaterloo.ca\/quest\/help\/students\/how-do-i\/online-exam-schedule\">How do I view my online course exam schedule?<\/a><\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-18",
            "end_date": "2017-10-23",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/709",
            "site": "important-dates-ro",
            "vid": 79148,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 703,
            "title": "Final exam schedules released",
            "body": "View on-campus and online schedules",
            "body_raw": "<p><em>View <a href=\"https:\/\/uwaterloo.ca\/registrar\/final-examinations\/exam-schedule\">on-campus<\/a> and <a href=\"https:\/\/uwaterloo.ca\/quest\/help\/students\/how-do-i\/online-exam-schedule\">online<\/a> schedules<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-18",
            "end_date": "2017-10-18",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/702",
            "site": "important-dates-ro",
            "vid": 79113,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 713,
            "title": "Fall 2017 Convocation",
            "body": "View the Convocation web page",
            "body_raw": "<p><em>View the <a href=\"https:\/\/uwaterloo.ca\/registrar\/convocation\">Convocation web page<\/a><\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-20",
            "end_date": "2017-10-21",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/712",
            "site": "important-dates-ro",
            "vid": 79190,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 719,
            "title": "Last day for online students to change their examination location",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-23",
            "end_date": "2017-10-23",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/718",
            "site": "important-dates-ro",
            "vid": 79155,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 726,
            "title": "Deadline for 50% tuition refund",
            "body": "View Student Financial Services\u00a0website",
            "body_raw": "<p><em>View<\/em> <em><a href=\"https:\/\/uwaterloo.ca\/finance\/student-financial-services\">Student Financial Services<\/a><\/em>\u00a0<em>website<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-25",
            "end_date": "2017-10-25",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/725",
            "site": "important-dates-ro",
            "vid": 78976,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 733,
            "title": "Fee arrangement deadline",
            "body": "A \"Late Fees Arrangement\" form required to become fees arranged after these dates.",
            "body_raw": "<p><em>A \"<a href=\"https:\/\/uwaterloo.ca\/forms\/undergraduate-studies\/late-fees-arrangement\">Late Fees Arrangement<\/a>\" form required to become <a href=\"https:\/\/uwaterloo.ca\/finance\/student-financial-services\">fees arranged<\/a> after these dates.<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-10-31",
            "end_date": "2017-10-31",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/732",
            "site": "important-dates-ro",
            "vid": 78962,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 740,
            "title": "Drop, penalty 1 period ends",
            "body": "WD (Withdrew, no credit granted) grade assigned for course(s) dropped",
            "body_raw": "<p><em>WD (Withdrew, no credit granted) <\/em><em>grade assigned <\/em><em>for course(s) dropped<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-11-20",
            "end_date": "2017-11-20",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/739",
            "site": "important-dates-ro",
            "vid": 79092,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 747,
            "title": "Drop, penalty 2 period begins",
            "body": "WF (Withdrew\/Failure, no credit granted, value 32) grade assigned for course(s) dropped (Engineering students: Visit course load and withdrawal in the calendar for specific regulations.)",
            "body_raw": "<p><em>WF (Withdrew\/Failure, no credit granted, value 32) grade assigned for course(s) dropped (<\/em><strong><em>Engineering students<\/em><\/strong><em>: Visit <\/em><em><a href=\"http:\/\/ugradcalendar.uwaterloo.ca\/page\/ENG-Examinations-and-Promotions-Rules\">course load<\/a> and <a href=\"http:\/\/ugradcalendar.uwaterloo.ca\/page\/ENG-Voluntary-Withdrawals-1\">withdrawal<\/a> in the calendar for specific regulations.)<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-11-21",
            "end_date": "2017-11-21",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/746",
            "site": "important-dates-ro",
            "vid": 79099,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 760,
            "title": "Lectures or classes end",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-04",
            "end_date": "2017-12-04",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/759",
            "site": "important-dates-ro",
            "vid": 79046,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 754,
            "title": "Make-up day for Thanksgiving Day",
            "body": "The loss of a Monday class on October 9\u00a0will be made up by following a Monday schedule on December 4.",
            "body_raw": "<p><em>The loss of a Monday class on October 9\u00a0will be made up by following a Monday schedule on December 4.<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-04",
            "end_date": "2017-12-04",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/753",
            "site": "important-dates-ro",
            "vid": 78857,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 767,
            "title": "Pre-examination study days",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-05",
            "end_date": "2017-12-06",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/766",
            "site": "important-dates-ro",
            "vid": 79120,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 774,
            "title": "Drop, penalty 2 period ends",
            "body": "WF (Withdrew\/Failure, no credit granted, value 32) grade assigned for course(s) dropped; last day to drop a course without a petition",
            "body_raw": "<p><em>WF (Withdrew\/Failure, no credit granted, value 32) grade assigned for course(s) dropped; l<\/em><em>ast day to drop a course without a petition<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-06",
            "end_date": "2017-12-06",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/773",
            "site": "important-dates-ro",
            "vid": 79106,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 795,
            "title": "Grades due",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-07",
            "end_date": "2018-01-02",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/794",
            "site": "important-dates-ro",
            "vid": 79176,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 788,
            "title": "On-campus examinations begin",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-07",
            "end_date": "2017-12-07",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/787",
            "site": "important-dates-ro",
            "vid": 79127,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 802,
            "title": "Online course examination days",
            "body": null,
            "body_raw": null,
            "special_notes": "Dec 9",
            "special_notes_raw": "<p>Dec 9<\/p>",
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-08",
            "end_date": "2017-12-08",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/801",
            "site": "important-dates-ro",
            "vid": 79162,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 816,
            "title": "On-campus examinations end",
            "body": null,
            "body_raw": null,
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-21",
            "end_date": "2017-12-21",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/815",
            "site": "important-dates-ro",
            "vid": 79134,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 823,
            "title": "Unofficial grades begin to appear in Quest",
            "body": "Beginning this date, registered students can view their unofficial term grades in Quest. (Not all grades will appear.)",
            "body_raw": "<p><em>Beginning this date, registered students can view their unofficial term grades in <a href=\"https:\/\/uwaterloo.ca\/quest\/\">Quest<\/a>. (Not all grades will appear.)<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-22",
            "end_date": "2017-12-22",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/822",
            "site": "important-dates-ro",
            "vid": 79169,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 809,
            "title": "Co-operative work term ends",
            "body": "Actual dates may vary depending on employer or student requirements",
            "body_raw": "<p><em>Actual dates may vary depending on employer or student requirements<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-22",
            "end_date": "2017-12-22",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/808",
            "site": "important-dates-ro",
            "vid": 79025,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 527,
            "title": "University holiday closure",
            "body": "University holidays",
            "body_raw": "<p><em><a href=\"https:\/\/uwaterloo.ca\/human-resources\/support-employees\/payroll\/paid-holidays\">University holidays<\/a><\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2017-12-25",
            "end_date": "2017-12-29",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/526",
            "site": "important-dates-ro",
            "vid": 78878,
            "updated": "2017-07-04T10:18:05-04:00"
        },
        {
            "id": 830,
            "title": "Standings and official grades are available in Quest",
            "body": "Beginning this date, registered students can view their official term grades in Quest. This is the date when official and complete term grades will appear along with academic standings and when official transcripts that have been ordered will be released. Averages do not appear on the official transcript.",
            "body_raw": "<p><em>Beginning this date, registered students can view their official term grades in <a href=\"https:\/\/uwaterloo.ca\/quest\/\">Quest<\/a>. This is the date when official and complete term grades will appear along with academic standings and when official transcripts that have been ordered will be released. Averages do not appear on the official transcript.<\/em><\/p>",
            "special_notes": null,
            "special_notes_raw": null,
            "audience": [
                "New Waterloo students",
                "Returning Waterloo students"
            ],
            "term": "Fall 2017",
            "term_id": 1179,
            "start_date": "2018-01-19",
            "end_date": "2018-01-19",
            "date_tbd": false,
            "date_na": false,
            "link": "https:\/\/wms-feeds.uwaterloo.ca\/important-dates-ro\/field-collection\/field-single-important-date\/829",
            "site": "important-dates-ro",
            "vid": 79183,
            "updated": "2017-07-04T10:18:05-04:00"
        }
    ]
}
```


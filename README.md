[![] (https://api.uwaterloo.ca/static/banner.png)](https://api.uwaterloo.ca)


The University of Waterloo API allows anyone to build applications using data from the uWaterloo websites.
The API currently features more than 40 methods of accessing various datasets across the University network.

If you find an error in the documentation, file an issue or send a pull request.

## Disclaimer

Review the 'No Warranty' section of the University of Waterloo ODL before using this data. If building services upon this data, please inform your users of the inherent risks (as a best practice).

## Accessing the API

All calls are made to the following URL with the required parameters for a given service.

```
https://api.uwaterloo.ca/v2/
```
In order to make an API call, you must have a valid [API Key](https://api.uwaterloo.ca/#!/keygen).
The data is returned in `json` and `xml` where the output format can be specified in the request URL

## Client Libraries

* [UWaterlooAPI](https://bitbucket.org/amjoconn/uwaterlooapi) (Python)
* [UWAPI](https://www.npmjs.org/package/uwapi) (NodeJS)
* [UWaterlooAPI](https://rubygems.org/gems/uwaterlooapi) (Ruby)
* [UWaterlooAPI](https://github.com/RobinsonMann/UWaterlooApi) (C#)
* [UWAPI.go](https://github.com/SaintDako/uwAPI.go) (Golang)
* [UW-Open-Data-API](https://github.com/zainh96/UW-Open-Data-API) (Java)

## Endpoints


### Food Services

- **[/foodservices/menu](v2/foodservices/menu.md)**
- **[/foodservices/notes](v2/foodservices/notes.md)**
- **[/foodservices/diets](v2/foodservices/diets.md)**
- **[/foodservices/outlets](v2/foodservices/outlets.md)**
- **[/foodservices/locations](v2/foodservices/locations.md)**
- **[/foodservices/watcard](v2/foodservices/watcard.md)**
- **[/foodservices/announcements](v2/foodservices/announcements.md)**
- **[/foodservices/products/{product_id}](v2/foodservices/products_product_id.md)**
- **[/foodservices/{year}/{week}/menu](v2/foodservices/year_week_menu.md)**
- **[/foodservices/{year}/{week}/notes](v2/foodservices/year_week_notes.md)**
- **[/foodservices/{year}/{week}/announcements](v2/foodservices/year_week_announcements.md)**

### Course

- **[/courses/{subject}](v2/courses/subject.md)**
- **[/courses/{course_id}](v2/courses/course_id.md)**
- **[/courses/{class_number}/schedule](v2/courses/class_number_schedule.md)**
- **[/courses/{subject}/{catalog_number}](v2/courses/subject_catalog_number.md)**
- **[/courses/{subject}/{catalog_number}/schedule](v2/courses/subject_catalog_number_schedule.md)**
- **[/courses/{subject}/{catalog_number}/prerequisites](v2/courses/subject_catalog_number_prerequisites.md)**
- **[/courses/{subject}/{catalog_number}/examschedule](v2/courses/subject_catalog_number_examschedule.md)**
- [See **Terms** endpoint for bulk data](https://github.com/uWaterloo/api-documentation#terms)
- [See **Codes** endpoint for subject listings](https://github.com/uWaterloo/api-documentation#definitions-and-codes)

### Events

- **[/events](v2/events/events.md)**
- **[/events/{site}](v2/events/events_site.md)**
- **[/events/{site}/{id}](v2/events/events_site_id.md)**
- **[/events/holidays](v2/events/holidays.md)**


### News

- **[/news](v2/news/news.md)**
- **[/news/{site}](v2/news/news_site.md)**
- **[/news/{site}/{id}](v2/news/news_site_id.md)**

### Services

- **[/services/{site}](v2/services/services_site.md)**

### Weather

- **[/weather/current](v2/weather/current.md)**

### Terms

- **[/terms/list](v2/terms/list.md)**
- **[/terms/{term}/examschedule](v2/terms/term_examschedule.md)**
- **[/terms/{term}/{subject}/schedule](v2/terms/term_subject_schedule.md)**
- **[/terms/{term}/{subject}/{catalog_number}/schedule](v2/terms/term_subject_catalog_number_schedule.md)**
- **[/terms/{term}/infosessions](v2/terms/term_infosessions.md)**


### Resources

- **[/resources/tutors](v2/resources/tutors.md)**
- **[/resources/printers](v2/resources/printers.md)**
- **[/resources/infosessions](v2/resources/infosessions.md)**
- **[/resources/goosewatch](v2/resources/goosewatch.md)**

### Definitions and Codes

- **[/codes/units](v2/codes/units.md)**
- **[/codes/terms](v2/codes/terms.md)**
- **[/codes/groups](v2/codes/groups.md)**
- **[/codes/subjects](v2/codes/subjects.md)**
- **[/codes/instructions](v2/codes/instructions.md)**

### Building

- **[/buildings/list](v2/buildings/list.md)**
- **[/buildings/{building_code}](v2/buildings/building_acronym.md)**
- **[/buildings/{building}/{room}/courses](v2/buildings/building_acronym_room_number_courses.md)**

### Parking

- **[/parking/watpark](v2/parking/watpark.md)**

### API

- **[/api/usage](v2/api/usage.md)**
- **[/api/services](v2/api/services.md)**
- **[/api/methods](v2/api/methods.md)**
- **[/api/versions](v2/api/versions.md)**
- **[/api/changelog](v2/api/changelog.md)**

### Server

- **[/server/time](v2/server/time.md)**
- **[/server/codes](v2/server/codes.md)**


## Contributing

If you would like to offer your suggestions or report any misfindings regarding the API data, simply create a new issue on the **issues** tab of the **[OpenData Repository](https://github.com/uWaterloo/OpenData/issues)** and assign it an appropriate label.



**Categories**

- [Bug](https://github.com/uWaterloo/OpenData/issues?labels=bug&page=1&state=open)
- [Enhancement](https://github.com/uWaterloo/OpenData/issues?labels=enhancement&page=1&state=open)
- [Question](https://github.com/uWaterloo/OpenData/issues?labels=question&page=1&state=open)
- [Data Request](https://github.com/uWaterloo/OpenData/issues?labels=data+request&page=1&state=open)


## Restrictions

### Usage

Currently, the API requests are restricted to **25,000** calls per month for a given key. This number may increase in the future.

*If your implementation of the API requires additional requests, feel free to contact us regarding the removal of your limit.*

### Data

The intent of data offered through this API is limited to publicly visible data only.
Private data such as student specific information is out of the API's scope.

## Contact ##

If you have any inquiries or suggestions, please feel free to contact us at [opendata.api@uwaterloo.ca](mailto:opendata.api@uwaterloo.ca).

Please consider subscribing to our [mailing list](https://lists.uwaterloo.ca/mailman/listinfo/opendata) in order to receive updates on the API and follow discussions.

## License
- <a href="https://uwaterloo.ca/open-data/university-waterloo-open-data-license-agreement-v1">University of Waterloo Open Data Licensing (ODL) Agreement v1</a>


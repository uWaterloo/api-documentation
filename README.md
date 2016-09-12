[![] (https://api.uwaterloo.ca/static/banner.png)](https://uwaterloo.ca/api/)


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
In order to make an API call, you must have a valid [API Key](https://uwaterloo.ca/api/register).
The data is returned in `json` and `xml` where the output format can be specified in the request URL

## Client Libraries (Community supported)
Please address any customer service issues regarding client libraries to the community developers of the libraries. If you would like your library to be added, please make a pull request.
* [UWaterlooAPI](https://bitbucket.org/amjoconn/uwaterlooapi) (Python)
* [UWAPI](https://www.npmjs.org/package/uwapi) (NodeJS)
* [UWaterlooAPI](https://rubygems.org/gems/uwaterlooapi) (Ruby)
* [UWaterlooAPI](https://github.com/RobinsonMann/UWaterlooApi) (C#)
* [UWAPI.go](https://github.com/SaintDako/uwAPI.go) (Golang)
* [UW-Open-Data-API](https://github.com/zainh96/UW-Open-Data-API) (Java)
* [UWaterloo-API](https://github.com/sanchitgera/node-uwaterloo-api) (NodeJS)
* [WatSwift](https://github.com/meteochu/WatSwift) (Swift)
* [UWAPI-PHP](https://github.com/hkwu/uwapi-php) (PHP)

## Endpoints


### Food Services

- **[/foodservices/menu](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/menu.md)**
- **[/foodservices/notes](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/notes.md)**
- **[/foodservices/diets](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/diets.md)**
- **[/foodservices/outlets](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/outlets.md)**
- **[/foodservices/locations](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/locations.md)**
- **[/foodservices/watcard](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/watcard.md)**
- **[/foodservices/announcements](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/announcements.md)**
- **[/foodservices/products/{product_id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/products_product_id.md)**
- **[/foodservices/{year}/{week}/menu](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/year_week_menu.md)**
- **[/foodservices/{year}/{week}/notes](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/year_week_notes.md)**
- **[/foodservices/{year}/{week}/announcements](https://github.com/uWaterloo/api-documentation/blob/master/v2/foodservices/year_week_announcements.md)**


### FEDS

- **[/feds/events](https://github.com/uWaterloo/api-documentation/blob/master/v2/feds/events.md)**
- **[/feds/events/{id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/feds/events_id.md)**
- **[/feds/locations](https://github.com/uWaterloo/api-documentation/blob/master/v2/feds/locations.md)**


### Course

- **[/courses](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/courses.md)**
- **[/courses/{subject}](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/subject.md)**
- **[/courses/{course_id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/course_id.md)**
- **[/courses/{class_number}/schedule](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/class_number_schedule.md)**
- **[/courses/{subject}/{catalog_number}](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/subject_catalog_number.md)**
- **[/courses/{subject}/{catalog_number}/schedule](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/subject_catalog_number_schedule.md)**
- **[/courses/{subject}/{catalog_number}/prerequisites](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/subject_catalog_number_prerequisites.md)**
- **[/courses/{subject}/{catalog_number}/examschedule](https://github.com/uWaterloo/api-documentation/blob/master/v2/courses/subject_catalog_number_examschedule.md)**
- [See **Terms** endpoint for bulk data](https://github.com/uWaterloo/api-documentation#terms)
- [See **Codes** endpoint for subject listings](https://github.com/uWaterloo/api-documentation#definitions-and-codes)


### Awards/Scholarships

- **[/awards/graduate](https://github.com/uWaterloo/api-documentation/blob/master/v2/awards/graduate.md)**
- **[/awards/undergraduate](https://github.com/uWaterloo/api-documentation/blob/master/v2/awards/undergraduate.md)**


### Events

- **[/events](https://github.com/uWaterloo/api-documentation/blob/master/v2/events/events.md)**
- **[/events/{site}](https://github.com/uWaterloo/api-documentation/blob/master/v2/events/events_site.md)**
- **[/events/{site}/{id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/events/events_site_id.md)**
- **[/events/holidays](https://github.com/uWaterloo/api-documentation/blob/master/v2/events/holidays.md)**


### Blogs

- **[/blogs/{site}](https://github.com/uWaterloo/api-documentation/blob/master/v2/blogs/blogs_site.md)**
- **[/blogs/{site}/{id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/blogs/blogs_site_id.md)**


### News

- **[/news](https://github.com/uWaterloo/api-documentation/blob/master/v2/news/news.md)**
- **[/news/{site}](https://github.com/uWaterloo/api-documentation/blob/master/v2/news/news_site.md)**
- **[/news/{site}/{id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/news/news_site_id.md)**


### Opportunities/Jobs

- **[/opportunities](https://github.com/uWaterloo/api-documentation/blob/master/v2/opportunities/opportunities.md)**
- **[/opportunities/{site}](https://github.com/uWaterloo/api-documentation/blob/master/v2/opportunities/opportunities_site.md)**
- **[/opportunities/{site}/{id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/opportunities/opportunities_site_id.md)**


### Services

- **[/services/{site}](https://github.com/uWaterloo/api-documentation/blob/master/v2/services/services_site.md)**


### Weather

- **[/weather/current](https://github.com/uWaterloo/api-documentation/blob/master/v2/weather/current.md)**


### Terms

- **[/terms/list](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/list.md)**
- **[/terms/{term}/courses](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_courses.md)**
- **[/terms/{term}/examschedule](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_examschedule.md)**
- **[/terms/{term}/{subject}/schedule](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_subject_schedule.md)**
- **[/terms/{term}/{subject}/{catalog_number}/schedule](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_subject_catalog_number_schedule.md)**
- **[/terms/{term}/enrollment](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_enrollment.md)**
- **[/terms/{term}/{subject}/enrollment](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_subject_enrollment.md)**
- **[/terms/{term}/infosessions](https://github.com/uWaterloo/api-documentation/blob/master/v2/terms/term_infosessions.md)**


### Resources

- **[/resources/tutors](https://github.com/uWaterloo/api-documentation/blob/master/v2/resources/tutors.md)**
- **[/resources/printers](https://github.com/uWaterloo/api-documentation/blob/master/v2/resources/printers.md)**
- **[/resources/infosessions](https://github.com/uWaterloo/api-documentation/blob/master/v2/resources/infosessions.md)**
- **[/resources/goosewatch](https://github.com/uWaterloo/api-documentation/blob/master/v2/resources/goosewatch.md)**
- **[/resources/sunshinelist](https://github.com/uWaterloo/api-documentation/blob/master/v2/resources/sunshinelist.md)**


### Definitions and Codes

- **[/codes/units](https://github.com/uWaterloo/api-documentation/blob/master/v2/codes/units.md)**
- **[/codes/terms](https://github.com/uWaterloo/api-documentation/blob/master/v2/codes/terms.md)**
- **[/codes/groups](https://github.com/uWaterloo/api-documentation/blob/master/v2/codes/groups.md)**
- **[/codes/subjects](https://github.com/uWaterloo/api-documentation/blob/master/v2/codes/subjects.md)**
- **[/codes/instructions](https://github.com/uWaterloo/api-documentation/blob/master/v2/codes/instructions.md)**


### Building

- **[/buildings/list](https://github.com/uWaterloo/api-documentation/blob/master/v2/buildings/list.md)**
- **[/buildings/{building_code}](https://github.com/uWaterloo/api-documentation/blob/master/v2/buildings/building_acronym.md)**
- **[/buildings/{building}/{room}/courses](https://github.com/uWaterloo/api-documentation/blob/master/v2/buildings/building_acronym_room_number_courses.md)**
- **[/buildings/{building_code}/accesspoints](https://github.com/uWaterloo/api-documentation/blob/master/v2/buildings/building_acronym_accesspoints.md)**
- **[/buildings/{building_code}/vendingmachines](https://github.com/uWaterloo/api-documentation/blob/master/v2/buildings/building_acronym_vendingmachines.md)**


### Points of Interest


- **[/poi/atms](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/atms.md)**
- **[/poi/greyhound](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/greyhound.md)**
- **[/poi/helplines](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/helplines.md)**
- **[/poi/libraries](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/libraries.md)**
- **[/poi/photospheres](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/photospheres.md)**
- **[/poi/defibrillators](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/defibrillators.md)**
- **[/poi/constructionsites](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/constructionsites.md)**
- **[/poi/accessibleentrances](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/accessibleentrances.md)**
- **[/poi/visitorinformation](https://github.com/uWaterloo/api-documentation/blob/master/v2/poi/visitorinformation.md)**



### Parking

- **[/parking/watpark](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/watpark.md)**
- **[/parking/lots/meter](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/meter.md)**
- **[/parking/lots/permit](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/permit.md)**
- **[/parking/lots/visitor](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/visitor.md)**
- **[/parking/lots/shortterm](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/shortterm.md)**
- **[/parking/lots/accessible](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/accessible.md)**
- **[/parking/lots/motorcycle](https://github.com/uWaterloo/api-documentation/blob/master/v2/parking/motorcycle.md)**


### Transit

- **[/transit/grt](https://github.com/uWaterloo/api-documentation/blob/master/v2/transit/grt.md)**
- **[/transit/grt/stops](https://github.com/uWaterloo/api-documentation/blob/master/v2/transit/agency_stops.md)**


### People Directory Search

- **[/directory/{user_id}](https://github.com/uWaterloo/api-documentation/blob/master/v2/directory/search.md)**


### API

- **[/api/usage](https://github.com/uWaterloo/api-documentation/blob/master/v2/api/usage.md)**
- **[/api/services](https://github.com/uWaterloo/api-documentation/blob/master/v2/api/services.md)**
- **[/api/methods](https://github.com/uWaterloo/api-documentation/blob/master/v2/api/methods.md)**
- **[/api/versions](https://github.com/uWaterloo/api-documentation/blob/master/v2/api/versions.md)**
- **[/api/changelog](https://github.com/uWaterloo/api-documentation/blob/master/v2/api/changelog.md)**


### Server

- **[/server/time](https://github.com/uWaterloo/api-documentation/blob/master/v2/server/time.md)**
- **[/server/codes](https://github.com/uWaterloo/api-documentation/blob/master/v2/server/codes.md)**


## Contributing

If you would like to offer your suggestions or report any problems regarding the API, simply create a new issue on the **issues** tab of the **[OpenData Repository](https://github.com/uWaterloo/OpenData/issues)** and assign it an appropriate label.



**Categories**

- [Bug](https://github.com/uWaterloo/OpenData/issues?labels=bug&page=1&state=open)
- [Enhancement](https://github.com/uWaterloo/OpenData/issues?labels=enhancement&page=1&state=open)
- [Question](https://github.com/uWaterloo/OpenData/issues?labels=question&page=1&state=open)
- [Data Request](https://github.com/uWaterloo/OpenData/issues?labels=data+request&page=1&state=open)


## Restrictions

### Usage

The API is now free to use with unlimited calls!


### Data

The intent of data offered through this API is limited to publicly visible data only.
Private data such as student specific information is out of the API's scope.

## Contact ##

If you have any inquiries or suggestions, please feel free to contact us at [https://uwaterloo.ca/api/contact-us](https://uwaterloo.ca/api/contact-us).

Please consider subscribing to our [mailing list](https://lists.uwaterloo.ca/mailman/listinfo/opendata) in order to receive updates on the API and follow discussions.

## License
- <a href="https://uwaterloo.ca/open-data/university-waterloo-open-data-license-agreement-v1">University of Waterloo Open Data Licensing (ODL) Agreement v1</a>


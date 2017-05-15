[![](https://api.uwaterloo.ca/static/banner.png)](https://uwaterloo.ca/api/)


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
* [UWaterlooAPI](https://github.com/albertoconnor/uwaterlooapi) (Python)
* [UWAPI](https://www.npmjs.org/package/uwapi) (NodeJS)
* [UWaterlooAPI](https://rubygems.org/gems/uwaterlooapi) (Ruby)
* [UWaterlooAPI](https://github.com/RobinsonMann/UWaterlooApi) (C#)
* [UWAPI.go](https://github.com/SaintDako/uwAPI.go) (Golang)
* [UWaterloo-API](https://github.com/endercrest/UWaterloo-API) (Java)
* [UW-Open-Data-API](https://github.com/zainh96/UW-Open-Data-API) (Java)
* [UWaterloo-API](https://github.com/sanchitgera/node-uwaterloo-api) (NodeJS)
* [WatSwift](https://github.com/meteochu/WatSwift) (Swift)
* [UWAPI-PHP](https://github.com/hkwu/uwapi-php) (PHP)
* [uwaterloo-api](https://github.com/cdeange/uwaterloo-api) (Java)

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


### FEDS

- **[/feds/events](v2/feds/events.md)**
- **[/feds/events/{id}](v2/feds/events_id.md)**
- **[/feds/locations](v2/feds/locations.md)**


### Course

- **[/courses](v2/courses/courses.md)**
- **[/courses/{subject}](v2/courses/subject.md)**
- **[/courses/{course_id}](v2/courses/course_id.md)**
- **[/courses/{class_number}/schedule](v2/courses/class_number_schedule.md)**
- **[/courses/{subject}/{catalog_number}](v2/courses/subject_catalog_number.md)**
- **[/courses/{subject}/{catalog_number}/schedule](v2/courses/subject_catalog_number_schedule.md)**
- **[/courses/{subject}/{catalog_number}/prerequisites](v2/courses/subject_catalog_number_prerequisites.md)**
- **[/courses/{subject}/{catalog_number}/examschedule](v2/courses/subject_catalog_number_examschedule.md)**
- [See **Terms** endpoint for bulk data](https://github.com/uWaterloo/api-documentation#terms)
- [See **Codes** endpoint for subject listings](https://github.com/uWaterloo/api-documentation#definitions-and-codes)


### Awards/Scholarships

- **[/awards/graduate](v2/awards/graduate.md)**
- **[/awards/undergraduate](v2/awards/undergraduate.md)**


### Events

- **[/events](v2/events/events.md)**
- **[/events/{site}](v2/events/events_site.md)**
- **[/events/{site}/{id}](v2/events/events_site_id.md)**
- **[/events/holidays](v2/events/holidays.md)**


### Blogs

- **[/blogs/{site}](v2/blogs/blogs_site.md)**
- **[/blogs/{site}/{id}](v2/blogs/blogs_site_id.md)**


### News

- **[/news](v2/news/news.md)**
- **[/news/{site}](v2/news/news_site.md)**
- **[/news/{site}/{id}](v2/news/news_site_id.md)**


### Opportunities/Jobs

- **[/opportunities](v2/opportunities/opportunities.md)**
- **[/opportunities/{site}](v2/opportunities/opportunities_site.md)**
- **[/opportunities/{site}/{id}](v2/opportunities/opportunities_site_id.md)**


### Services

- **[/services/{site}](v2/services/services_site.md)**


### Weather

- **[/weather/current](v2/weather/current.md)**


### Terms

- **[/terms/list](v2/terms/list.md)**
- **[/terms/{term}/courses](v2/terms/term_courses.md)**
- **[/terms/{term}/examschedule](v2/terms/term_examschedule.md)**
- **[/terms/{term}/{subject}/schedule](v2/terms/term_subject_schedule.md)**
- **[/terms/{term}/{subject}/{catalog_number}/schedule](v2/terms/term_subject_catalog_number_schedule.md)**
- **[/terms/{term}/enrollment](v2/terms/term_enrollment.md)**
- **[/terms/{term}/{subject}/enrollment](v2/terms/term_subject_enrollment.md)**
- **[/terms/{term}/infosessions](v2/terms/term_infosessions.md)**


### Resources

- **[/resources/tutors](v2/resources/tutors.md)**
- **[/resources/infosessions](v2/resources/infosessions.md)**
- **[/resources/goosewatch](v2/resources/goosewatch.md)**
- **[/resources/sunshinelist](v2/resources/sunshinelist.md)**


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
- **[/buildings/{building_code}/accesspoints](v2/buildings/building_acronym_accesspoints.md)**
- **[/buildings/{building_code}/vendingmachines](v2/buildings/building_acronym_vendingmachines.md)**


### Points of Interest


- **[/poi/atms](v2/poi/atms.md)**
- **[/poi/greyhound](v2/poi/greyhound.md)**
- **[/poi/helplines](v2/poi/helplines.md)**
- **[/poi/libraries](v2/poi/libraries.md)**
- **[/poi/photospheres](v2/poi/photospheres.md)**
- **[/poi/defibrillators](v2/poi/defibrillators.md)**
- **[/poi/constructionsites](v2/poi/constructionsites.md)**
- **[/poi/accessibleentrances](v2/poi/accessibleentrances.md)**
- **[/poi/visitorinformation](v2/poi/visitorinformation.md)**



### Parking

- **[/parking/watpark](v2/parking/watpark.md)**
- **[/parking/lots/meter](v2/parking/meter.md)**
- **[/parking/lots/permit](v2/parking/permit.md)**
- **[/parking/lots/visitor](v2/parking/visitor.md)**
- **[/parking/lots/shortterm](v2/parking/shortterm.md)**
- **[/parking/lots/accessible](v2/parking/accessible.md)**
- **[/parking/lots/motorcycle](v2/parking/motorcycle.md)**


### Transit

- **[/transit/grt](v2/transit/grt.md)**
- **[/transit/grt/stops](v2/transit/agency_stops.md)**


### People Directory Search

- **[/directory/{user_id}](v2/directory/search.md)**


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


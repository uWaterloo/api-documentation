[![] (https://api.uwaterloo.ca/static/banner.png)](https://api.uwaterloo.ca)


The University of Waterloo API allows anyone to build applications using data from the uWaterloo websites.
The API currently features more than 30 methods of accessing various datasets accross the University network.

If you find an error in the documentation, file an issue or send a pull request.


## Accessing the API

All calls are made to the following URL with the required parameters for a given service.

```
https://api.uwaterloo.ca/v2/
```
In order to make an API call, you must have a valid [API Key](https://api.uwaterloo.ca/#!/keygen).
The data is returned in `json` and `xml` where the output format can be specified in the request URL

## Endpoints


### Food Services

- **[/foodservices/menu]()**
- **[/foodservices/notes]()**
- **[/foodservices/announcements]()**
- **[/foodservices/diets]()**
- **[/foodservices/outlets]()**
- **[/foodservices/watcard]()**
- **[/foodservices/products/{product_id}]()**
- **[/foodservices/{year}/{week}/menu]()**
- **[/foodservices/{year}/{week}/notes]()**
- **[/foodservices/{year}/{week}/announcements]()**

### Course

- **[/courses/{subject}]()**
- **[/courses/{subject}/{catalog_number}]()**
- **[/courses/{subject}/{catalog_number}/schedule]()**
- **[/courses/{subject}/{catalog_number}/prerequisites]()**

### Resources

- **[/resources/printers]()**
- **[/resources/infosessions]()**
- **[/academics/groups]()**
- **[/resources/academics/subjects]()**
- **[/resources/academics/terms]()**
- **[/resources/academics/organizations]()**
- **[/resources/academics/instructions]()**

### Building

- **[/buildings/list]()**
- **[/buildings/{building_acronym}]()**
- **[/buildings/{building_acronym}/{room_number}/courses]()**

### API

- **[/api/services](v2/api/services.md)**
- **[/api/methods](v2/api/methods.md)**
- **[/api/usage]()**
- **[/api/versions]()**
- **[/api/changelog]()**

### Server

- **[/server/time]()**
- **[/server/codes]()**


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

## Licensing

The data from the API is offered under the [Open Data License Agreement v1.0](https://uwaterloo.ca/open-data/university-waterloo-open-data-license-agreement-v1) for the University of Waterloo.

## Contact ##

If you have any inquiries or suggestions, please feel free to contact us at [opendata.api@uwaterloo.ca](mailto:opendata.api@uwaterloo.ca).

Please consider subscribing to our [mailing list](https://lists.uwaterloo.ca/mailman/listinfo/opendata) in order to receive updates on the API and follow discussions.



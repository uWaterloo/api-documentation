# Current Weather

```
GET /weather/current.{format}
```

## Description

> This method returns the current weather details from the University of Waterloo Weather Station. http://weather.uwaterloo.ca

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
    <td>No</td>
  </tr>
  <tr>
    <td><b>Method ID</b></td>
    <td>1451</td>
    <td><b>Enabled</b></td>
    <td>Yes</td>
  </tr>
  <tr>
    <td><b>Service Name</b></td>
    <td>weather</td>
    <td><b>Service ID</b></td>
    <td>277</td>
  </tr>
  <tr>
    <td><b>Information Steward</b></td>
    <td>UW Weather Station</td>
    <td><b>Data Type</b></td>
    <td>XML Feed</td>
  </tr>
  <tr>
    <td><b>Update Frequency</b></td>
    <td>Every 15 minutes</td>
    <td><b>Cache Time</b></td>
    <td>0 seconds</td>
  </tr>
</table>


### Notes

- Any value can be `null`


### Sources

- http://weather.uwaterloo.ca/waterloo_weather_station_data.xml


## Parameters

```
GET /weather/current.{format}
```

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Type</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
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
GET /weather/current.{format}
```

- **https://api.uwaterloo.ca/v2/weather/current.json**
- **https://api.uwaterloo.ca/v2/weather/current.xml**
- **https://api.uwaterloo.ca/v2/weather/current.json?callback=myResponse**


## Response

<table>
  <tr>
    <td><b>Field Name</b></td>
    <td><b>Type</b></td>
    <td><b>Value Description</b></td>
  </tr>
  <tr>
    <td><b>latitude</b></td>
    <td>float</td>
    <td>Station's latitude</td>
  </tr>
  <tr>
    <td><b>longitude</b></td>
    <td>float</td>
    <td>Station's longitude</td>
  </tr>
  <tr>
    <td><b>elevation_m</b></td>
    <td>float</td>
    <td>Station elevation in meters</td>
  </tr>
  <tr>
    <td><b>observation_time</b></td>
    <td>string</td>
    <td>iso8601 timestamp of weather recordings</td>
  </tr>
  <tr>
    <td><b>temperature_current_c</b></td>
    <td>float</td>
    <td>Current temperature in celsius</td>
  </tr>
  <tr>
    <td><b>humidex_c</b></td>
    <td>float</td>
    <td>Humidex temperature in celsius</td>
  </tr>
  <tr>
    <td><b>windchill_c</b></td>
    <td>float</td>
    <td>Windchill in celsius</td>
  </tr>
  <tr>
    <td><b>temperature_24hr_max_c</b></td>
    <td>float</td>
    <td>24 hour maximum temperature in celsius</td>
  </tr>
  <tr>
    <td><b>temperature_24hr_min_c</b></td>
    <td>float</td>
    <td>24 hour minimum temperature in celsius</td>
  </tr>
  <tr>
    <td><b>precipitation_15min_mm</b></td>
    <td>float</td>
    <td>Precipitation reading for 15 minute interval in mm</td>
  </tr>
  <tr>
    <td><b>precipitation_1hr_mm</b></td>
    <td>float</td>
    <td>Precipitation reading for 1 hour interval in mm</td>
  </tr>
  <tr>
    <td><b>precipitation_24hr_mm</b></td>
    <td>float</td>
    <td>Precipitation reading for every 24 hour interval in mm</td>
  </tr>
  <tr>
    <td><b>relative_humidity_percent</b></td>
    <td>float</td>
    <td>Relative humidity in percentage</td>
  </tr>
  <tr>
    <td><b>dew_point_c</b></td>
    <td>float</td>
    <td>Dew point in celsius</td>
  </tr>
  <tr>
    <td><b>wind_speed_kph</b></td>
    <td>float</td>
    <td>Wind speed in km per hour</td>
  </tr>
  <tr>
    <td><b>wind_direction_degrees</b></td>
    <td>float</td>
    <td>Wind direction in degrees</td>
  </tr>
  <tr>
    <td><b>pressure_kpa</b></td>
    <td>float</td>
    <td>Pressure in kilo Pascals</td>
  </tr>
  <tr>
    <td><b>pressure_trend</b></td>
    <td>float</td>
    <td>Word description of the current pressure trend</td>
  </tr>
  <tr>
    <td><b>incoming_shortwave_radiation_wm2</b></td>
    <td>float</td>
    <td>Incomig radiation in watts per meter square</td>
  </tr>
</table>


Any value can be `null`

## Output

#### JSON

```json

{
  "meta":{
    "requests":476,
    "timestamp":1384890871,
    "status":200,
    "message":"Request successful",
    "method_id":1451,
    "version":2.07,
    "method":{
      
    }
  },
  "data":{
    "latitude":43.4738,
    "longitude":-80.5576,
    "elevation_m":334.4,
    "observation_time":"2013-11-19T14:45:00-05:00",
    "temperature_current_c":1,
    "humidex_c":null,
    "windchill_c":-3,
    "temperature_24hr_max_c":3,
    "temperature_24hr_min_c":-0.5,
    "precipitation_15min_mm":null,
    "precipitation_1hr_mm":0,
    "precipitation_24hr_mm":1,
    "relative_humidity_percent":80.4,
    "dew_point_c":-2,
    "wind_speed_kph":9.2,
    "wind_direction_degrees":45,
    "pressure_kpa":102.5,
    "pressure_trend":"Rising",
    "incoming_shortwave_radiation_wm2":317.8
  }
}
```


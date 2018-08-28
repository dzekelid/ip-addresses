---
swagger: "2.0"
x-collection-name: Weatherbit.io
x-complete: 0
info:
  title: Weatherbit Get IP
  description: Returns a geolocation object. Given an IP address. If no IP supplied,
    will use request IP address.
  version: 2.0.0
host: api.weatherbit.io
basePath: /v2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /bulk/history/daily?ip={ip}:
    get:
      summary: Get Bulk History Daily IP
      description: Returns Historical Observations - Given IP Address, or auto.
      operationId: returns-historical-observations--given-ip-address-or-auto
      x-api-path-slug: bulkhistorydailyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: ip
        description: IP Address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Bulk
      - History
      - Daily
      - Ip
      - Ip
  /bulk/history/hourly?ip={ip}:
    get:
      summary: Get Bulk History Hourly IP
      description: Returns Historical Observations - Given IP Address, or auto.
      operationId: returns-historical-observations--given-ip-address-or-auto
      x-api-path-slug: bulkhistoryhourlyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: ip
        description: IP Address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Bulk
      - History
      - Hourly
      - Ip
      - Ip
  /current?ip={ip}:
    get:
      summary: Get Current IP
      description: Returns a Current Observation - Given an IP address, or auto.
      operationId: returns-a-current-observation--given-an-ip-address-or-auto
      x-api-path-slug: currentipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback - Example - callback=func
      - in: path
        name: ip
        description: IP Address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: marine
        description: Marine stations only (buoys, oil platforms, etc)
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Current
      - Ip
      - Ip
  /forecast/3hourly?ip={ip}:
    get:
      summary: Get Forecast 3hourly IP
      description: Returns a 3-hourly forecast, where each point represents a three
        hour   period. Every point has a datetime string in the format "YYYY-MM-DD:HH".
        Time is UTC.
      operationId: returns-a-3hourly-forecast-where-each-point-represents-a-three-hour---period-every-point-has-a-datet
      x-api-path-slug: forecast3hourlyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: days
        description: Number of days to return
      - in: path
        name: ip
        description: IP address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Forecast
      - 3hourly
      - Ip
      - Ip
  /forecast/daily?ip={ip}:
    get:
      summary: Get Forecast Daily IP
      description: '**(REQUIRED: Basic Plan or Higher)** Returns a daily forecast,
        where each point represents one day (24hr) period. Every point has a datetime
        string in the format "YYYY-MM-DD". One day begins at 00:00 UTC, and ends at
        23:59 UTC.'
      operationId: required-basic-plan-or-higher-returns-a-daily-forecast-where-each-point-represents-one-day-24hr-peri
      x-api-path-slug: forecastdailyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: days
        description: Number of days to return
      - in: path
        name: ip
        description: IP address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Forecast
      - Daily
      - Ip
      - Ip
  /forecast/hourly?ip={ip}:
    get:
      summary: Get Forecast Hourly IP
      description: '**(REQUIRED: Developer Plan or Higher)** Returns an hourly forecast,
        where each point represents a one hour period. Every point has a datetime
        string in the format "YYYY-MM-DD:HH". Time is UTC.'
      operationId: required-developer-plan-or-higher-returns-an-hourly-forecast-where-each-point-represents-a-one-hour-
      x-api-path-slug: forecasthourlyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: days
        description: Number of days to return
      - in: query
        name: hours
        description: Number of hours to return
      - in: path
        name: ip
        description: IP address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Forecast
      - Hourly
      - Ip
      - Ip
  /history/daily?ip={ip}:
    get:
      summary: Get History Daily IP
      description: Returns Historical Observations - Given IP Address, or auto. **(LIMIT
        1 day for Low Volume plans. LIMIT 7 days for Basic/Developer. LIMIT 30 days
        for Advanced/Advanced+/Enterprise)**
      operationId: returns-historical-observations--given-ip-address-or-auto-limit-1-day-for-low-volume-plans-limit-7-d
      x-api-path-slug: historydailyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: ip
        description: IP Address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - History
      - Daily
      - Ip
      - Ip
  /history/hourly?ip={ip}:
    get:
      summary: Get History Hourly IP
      description: Returns Historical Observations - Given IP Address, or auto. **(LIMIT
        1 day for Low Volume plans. LIMIT 7 days for Basic/Developer. LIMIT 30 days
        for Advanced/Advanced+/Enterprise)**
      operationId: returns-historical-observations--given-ip-address-or-auto-limit-1-day-for-low-volume-plans-limit-7-d
      x-api-path-slug: historyhourlyipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: end_date
        description: End Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: path
        name: ip
        description: IP Address, or auto
      - in: query
        name: key
        description: Your registered API key
      - in: query
        name: lang
        description: 'Language (Default: English) See language field description'
      - in: query
        name: start_date
        description: Start Date (YYYY-MM-DD or YYYY-MM-DD:HH)
      - in: query
        name: units
        description: Convert to units
      responses:
        200:
          description: OK
      tags:
      - Weather
      - History
      - Hourly
      - Ip
      - Ip
  /ip?ip={ip}:
    get:
      summary: Get IP
      description: Returns a geolocation object. Given an IP address. If no IP supplied,
        will use request IP address.
      operationId: returns-a-geolocation-object-given-an-ip-address-if-no-ip-supplied-will-use-request-ip-address
      x-api-path-slug: ipipip-get
      parameters:
      - in: query
        name: callback
        description: Wraps return in jsonp callback
      - in: query
        name: exclude
        description: exclude=all => return IP address only
      - in: query
        name: format
        description: '&format=none => return IP address as string'
      - in: path
        name: ip
        description: IP address
      - in: query
        name: key
        description: Your registered API key
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Ip
      - Ip
      - Ip
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
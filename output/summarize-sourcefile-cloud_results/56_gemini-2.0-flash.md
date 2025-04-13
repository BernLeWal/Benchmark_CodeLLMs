This is a Spring Boot application written in Java, designed to manage weather data for different cities.

**Functionality and Usage:**

1.  **Accessing Data:** The `/city/{id}` endpoint (GET request) retrieves weather information for a specific city using its ID.  The ID is passed as a path variable. The returned format is a list of `Record` objects.

2.  **Adding Data:** The `/city/add` endpoint (GET request) is intended to add new weather data.  However, it is currently unimplemented and throws an `UnsupportedOperationException`. It should accept a `Record` object in the request body.

3.  **Updating Data:** The `/city/update/{id}` endpoint (GET request) is intended to update weather data for a specific city. It's currently flawed, as it retrieves the old data and sets it into a new `Record` instance.

**Implementation Details:**

*   The application uses an in-memory `weatherRecords` list to store weather data. This data is initialized during the `WeatherApplication` constructor.
*   The `Record` is a Java record, a concise way to define data classes.

**Problems:**

*   The `/city/add` endpoint is not implemented.
*   The `/city/update/{id}` endpoint has a flawed implementation that doesn't actually update the values.
*   The constructor of `WeatherApplication` trhows a `NullPointerException` because `weatherRecords` is not instantiated.
*   The HTTP Methods are used wrong. `addRecord` and `updateRecords` should be implemented with `POST` and `PUT` or `PATCH`

**Quality and Functionality:**

The code demonstrates basic Spring Boot structure but has significant functionality gaps and errors.

**Score: 35/100**

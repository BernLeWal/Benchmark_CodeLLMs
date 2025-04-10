This Java application uses Spring Boot to create a RESTful API for managing weather data.  It utilizes an in-memory `HashMap` as a data store.

**Functionality and Usage:**

1. **Data Persistence:** Uses an in-memory HashMap; data is lost on application restart.  A persistent data store (database) is needed for production use.

2. **REST Endpoints:** Provides endpoints for retrieving weather data by ID (`GET /city/{id}`), retrieving all weather data (`GET /city`), adding new weather data (`POST /city/add`), updating existing data (`PUT /city/update/{id}`), and deleting data (`DELETE /city/delete/{id}`).

3. **HTTP Status Codes:** Uses appropriate HTTP status codes (e.g., 200 OK, 404 Not Found) to indicate success or failure of requests.

4. **Data Representation:** Uses a `WeatherRecord` record class to represent weather data.

5. **Application Startup:**  Starts using `SpringApplication.run()`.


**Code Quality and Functionality:**

The code is well-structured and easy to understand, demonstrating good use of Spring Boot annotations. However, the lack of persistent storage is a significant limitation. Error handling is basic but functional.

**Quality Score:** 75/100.  The functionality is good for a simple example, but the lack of persistence and more robust error handling prevents a higher score.

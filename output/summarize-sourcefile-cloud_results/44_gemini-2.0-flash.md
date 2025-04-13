This Java application, built with Spring Boot, provides a simple weather service. It uses a `HashMap` to store weather data for different cities. The application exposes REST endpoints for retrieving, adding, updating, and deleting weather records.

To use the application, send HTTP requests to the `/city` endpoint.
*   `GET /city/{id}` retrieves weather data for a specific city by its ID.
*   `GET /city` retrieves weather data for all cities.
*   `POST /city/add` adds new weather data, requiring a JSON payload with the `WeatherRecord` structure.
*   `PUT /city/update/{id}` updates weather data for a specific city ID, also requiring a JSON payload.
*   `DELETE /city/delete/{id}` deletes weather data for a specific city ID.

The application initializes with weather data for Vienna, Prague, Berlin and Munich.

Potential problems include the lack of data validation and proper error handling, as well as the in-memory data storage, which makes the data non-persistent. The update method creates a temporary record instead of directly using the updated record.

Quality and Functionality Score: 75/100

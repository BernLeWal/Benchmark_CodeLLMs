This Java code implements a simple REST API for managing weather records using Spring Boot. It defines a `Record` data class to store weather information (id, city, weather, temperature, date).

The application provides three endpoints:

1.  `GET /city/{id}`: Retrieves a weather record by its ID. Access via a web browser or tool like curl using `http://<host>:<port>/city/1` (replace 1 with the desired ID).
2.  `POST /city/add`: Adds a new weather record. Send a JSON payload representing the `Record` object in the request body, using tools like curl or Postman.
3.  `PUT /city/update/{id}`: Updates an existing weather record by its ID. Send a JSON payload representing the updated `Record` in the request body to `http://<host>:<port>/city/update/1` (replace 1 with the desired ID).

The weather records are stored in an in-memory `ArrayList`.  A constructor initializes the list with some sample data.

Potential issues:
*   `getRecords` method does not handle out-of-bounds `id` values gracefully (IndexOutOfBoundsException).
*   Error handling is minimal.
*   No persistence mechanism; data is lost on application restart.

**Quality and Functionality Score: 65/100**

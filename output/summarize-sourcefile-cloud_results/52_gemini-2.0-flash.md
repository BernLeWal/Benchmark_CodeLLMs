This Java Spring Boot application provides a basic weather data service. It uses a `Record` class to store weather information (city, weather, temperature, date).

**Functionality:**

1.  **Retrieval:** `GET /city/{id}` retrieves weather records by index. The index does not match the ID of the record.
2.  **Creation (Not Implemented):** `POST /city/add` is intended to add new weather records, but currently throws an `UnsupportedOperationException`.
3.  **Update:** `PUT /city/update/{id}` updates a weather record at a specific index (`id` - 1) with the data from the `updatedRecord` object.

**Usage:**

*   The application starts a web server.
*   Retrieve data via `GET /city/{id}` (e.g., `/city/1`).
*   The `POST` and `PUT` endpoints are available, but `POST` is not implemented.

**Problems:**

*   `POST /city/add` is unimplemented.
*   `GET /city/{id}` uses the index of the record instead of the ID.
*   `PUT /city/update/{id}` uses the index of the record instead of the ID.
*   No error handling

**Quality and Functionality:** 55/100.

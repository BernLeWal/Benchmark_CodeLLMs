# Weather Service Application Summary

This is a Java Spring Boot REST API for managing weather data by city. It provides:

1. CRUD operations for weather records via HTTP endpoints:
   - GET `/city/{id}` - Retrieves weather data for a specific city by ID
   - GET `/city` - Lists all weather records
   - POST `/city/add` - Adds new weather data
   - PUT `/city/update/{id}` - Updates existing weather data
   - DELETE `/city/delete/{id}` - Removes weather data

2. Each weather record contains:
   - ID, city name, weather condition, temperature, and date

3. The application initializes with sample data for Vienna, Prague, Berlin, and Munich.

4. To use:
   - Run the application (Spring Boot)
   - Access endpoints via HTTP requests
   - Send/receive JSON weather records

5. Implementation uses:
   - Spring Boot framework
   - Records for data modeling
   - HashMap for in-memory storage
   - RESTful design principles
   - Proper HTTP status codes for responses

Evaluation: 75/100
- Good RESTful structure and error handling
- Lacks data validation, persistence, documentation
- In-memory storage not suitable for production
- Method naming could be more consistent with REST conventions
The provided source code is implemented in Java using the Spring Boot framework. The program serves as a basic weather application that manages weather records for various cities.

**Usage Instructions:**
1. **Run the Application:** Execute the `main` method to start the Spring Boot application, which will display "Hello World!" in the console.
2. **Retrieve Weather Records:** Send a GET request to `/city/{id}` to get the weather record for a specific city based on its ID.
3. **Add Weather Record:** A POST request to `/city/add` is intended to add a new weather record, but this functionality is currently not implemented and throws an exception.
4. **Update Weather Record:** Send a PUT request to `/city/update/{id}` to update a specific city's weather record, though this method does not correctly update the data due to incomplete implementation.

**Evaluation of Quality and Functionality:**
The code has several issues:
- The list of `weatherRecords` is not initialized, leading to a NullPointerException.
- The `addRecord` method is incomplete and not functional.
- The `updateRecords` method does not properly utilize the `updatedRecord` parameter.
- Incorrect HTTP methods are used for adding and updating records which typically should be POST and PUT respectively.

Considering these issues, I would rate the code's quality and functionality at **40/100**.

# REST Exercise

Implement a basic REST-based application in Java Spring Boot.

## Scenario

You want to build a weather service. The application should be designed as a REST-based API, so that
different clients can access and update your data.

There are two use cases:
1. Clients want to know the current temperature for a specific city
2. Weather stations want to send you data

Design a REST-based API for these use cases.

## Note

You don’t have to implement a fully functioning application. Just create the controllers and routes
and write a describing comment on each function.

## Example

```java
@RestController
public class BookController {
    /**
    * This route will return all books.
    * The GET method is used because no book data will be
    * altered on the server.
    */
    @GetMapping("/books")
    public Book readBooks() {
        // placeholder
        return nul
    }
}
```

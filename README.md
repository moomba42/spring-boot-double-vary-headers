# spring-boot-double-vary-headers #
When you enable the spring security cors filter, and then request a static file with the GET method,
then the Vary headers will be duplicated in the response.

To reproduce the bug, run the project, then execute this curl command:

`curl -I 'localhost:8080/test.json'`

You will now be able to see duplicate `Vary` headers, which is an unwanted behavior.
This problem also happens when using Spring Boot 2.3.0 M3

### Dependencies

This project has the following dependencies:
 - Spring Boot 2.2.6
 - Spring Web
 - Spring Security
 - Java 8

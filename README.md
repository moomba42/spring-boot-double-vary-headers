# spring-boot-double-vary-headers
To reproduce the bug, run the project, then execute this curl command:

`curl -I 'localhost:8080/test.json'`

You will now be able to see duplicate `Vary` headers, which is unwanted behavior.

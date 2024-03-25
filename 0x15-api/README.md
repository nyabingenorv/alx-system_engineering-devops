# API

**API** stands for Application Programming Interface. At some point or another, most large companies have built APIs for their customers, or for internal use.

**REST** is an acronym for Representational State Transfer — an almost meaningless description of the most-used web service technology! A REST API is a way for two computer systems to communicate using the HTTP technologies found in web browsers and servers.

- APIs helps in communication between systems by providing an interface for them to talk to each other.

- REST is simply a widely adopted style of API that we use to communicate with internal and external parties in a consistent and predictable way. It can be compared with how we used to send a letter with a postage stamp, address, and envelope in a certain way to ensure it gets delivered and read.

#### A RESTful web service request contains

1. *An Endpoint URL*. An application implementing a RESTful API will define one or more URL endpoints with a domain, port, path, and/or query string — for example, <https://mydomain/user/123?format=json>.

2. *The HTTP method*. Differing HTTP methods can be used on any endpoint which map to application create, read, update, and delete (CRUD) operations:
|HTTP method| CRUD |Action|
|-----------|------|------|
GET |read| returns requested data|
POST| create| creates a new record|
PUT or PATCH| update| updates an existing record|
DELETE| delete| deletes an existing record|

Examples:

a GET request to /user/ returns a list of registered users on a system
a POST request to /user/ creates a user with the ID 123 using the body data (see 4. below). The response returns the ID.
a PUT request to /user/123 updates user 123 with the body data (see 4. below)
a GET request to /user/123 returns the details of user 123
a DELETE request to /user/123 deletes user 123
HTTP headers. Information such as authentication tokens or cookies can be contained in the HTTP request header.
Body Data. Data is normally transmitted in the HTTP body in an identical way to HTML <form> submissions or by sending a single JSON-encoded data string.

# Inter-Service Communication

- a microservices-­based application can be considered a distributed system running multiple services on
different network locations.

- A given service runs on its own process. So microservices
interact using inter-process or inter-service communication styles.

- In monolithic applications, business functionalities of different bussiness components are invoked using function calls


- in microservices, there is no such restriction 
to use a specific communication pattern and message format. 

- The most common type of communication
styles used in microservices are synchronous and asynchronous.

## Synchronous Communication:
 - The client sends a request and waits for a
response from the service. Both parties have to keep the connection open until the client
receives the response. The execution logic of the client cannot proceed without the response.


## NB: 
synchronous and blocking communication are two different things. We can use a non-blocking IO implementation,
which registers a callback function once the service responds back, and the client thread can be returned without blocking on a particular response. the
synchronous communication style can be built on top of a non-blocking asynchronous implementation. but whatever it's client has to wait response.


### Rest :
 - is most famous synchronus communication and HTTP is the most famous used protocol.


### Richardson Maturity Model:
- ### **Level 0 – Swamp of PoX**:  if a service has one url "http://xyz/api/dosomething" and it gets what it should do from the message content we call that level 0. Hence, we dont consider that a restful.

- ### **Level 1 – Resource URIs:**  A service is considered to be at this level
when it has individual URIs for each resource, but the message still, means all operations for order entity is just /order and you consider what you do from the content, but /customers is different api as it's a different resource. It has no http status code response.

- ### **Level 2 – HTTP Verbs**: Instead of using the message content to
determine the operation, we can use an HTTP verb instead. Also, the proper HTTP status codes
should be supported.

- ### ** Level 3 – Hypermedia Controls **: you cant just send data but you can send actions accompained to this resource: 

{

    "item": {
        "name": "example1"
    },

    "_links": {
        "self":"http://localhost/items/1"
        "search" "http://localhost/items/search" // href to search item.
    
}


-----------------------------
## gRPC:
- 


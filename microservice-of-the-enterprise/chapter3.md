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


## Rest :
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
- gRPC uses protocol buffers "TODO: check this later" , Google’s mature open source mechanism for serializing structured data.

## A Glimpse of HTTP2:
  
### The main limitations of HTTP 1.1:
- **Blocking**: handle one request at a time
- **Overhead**: In HTTP 1.1, many headers are repeated
across multiple requests. For example, headers such as User-Agent and Cookie are sent over and over, which is a waste of bandwidth. HTTP 1.1 defines the GZIP format to compress the payload, but that
doesn’t apply to the headers.

---------------------------
Http2 is backward compatible. HTTP2 defines
the concept of a stream, which is a bidirectional flow of bytes within an established connection, which may carry one or more messages.

Frame is the smallest unit of
communication in HTTP2, and each frame contains a frame header, this frame header at a minimum
identifies the stream to which the frame belongs. A message is a complete sequence of
frames that map to a logical HTTP message, such as a request or response, which consists
of one or more frames.

HTTP2 avoids header repetition and introduces header compression to optimize
the use of bandwidth. It also introduces a new feature of sending server push messages
without using the request-response style messages. 

---------------
## Graphql:
- GraphQL provides a query language for APIs and a runtime for fulfilling those queries with your existing data, gives clients the power to ask for exactly what they need and nothing more. The client has full control over the data it gets. The typical REST APIs require
loading from multiple URLs, but GraphQL-based services get all the data your app needs
in a single request.
```
{
  hero {
    name
  }
}

{
  "data": {
    "hero": {
      "name": "R2-D2"
    }
  }
}
```


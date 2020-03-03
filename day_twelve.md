### Tuesday 3rd March 

## Process Modelling

Sequence diagram 

## Battle Challenge

### The Web  

The whole web is built on client-server relationships. There are different kinds of clients and servers but the relationship is roughly the same: the client is dependent on the server for providing and managing information. Anything that can request a resource from a server can be called a client.

Challenge - setup using httpie 
``` brew install httpie ```

### The Hypertext Transfer Protocol (HTTP)

Usually, clients and servers talk to each other using the HyperText Transfer Protocol. A client makes a request to a server and gets back a response. It is called a "protocol" because it has a defined structure for requests and responses.

#### URLs

At the heart of web communications is the request message, which are sent via Uniform Resource Locators (URLs).

>http://www.domain.com:1234/path/to/resource?a=b&x=y

```
http = protocol
www.domain.com = host    
1234 = port
path/to/resource = resource path
?a=b%x=y = query
```

### HTTP: Parameters

Within HTTP, we call data sent from a client to a server a parameter. Just like Ruby's hashes, parameters come as key-value pairs and a request can contain multiple parameters. One way of sending a parameter to a server is to pass it in the query string. The query string is a string that can be appended to an URL. It has a special set of formatting conventions.

### HTTP: Verbs

- **GET**: fetch an existing resource. The URL contains all the necessary information the server needs to locate and return the resource. 
- **POST**: create a new resource. POST requests usually carry a payload that specifies the data for the new resource. 
- **PUT**: update an existing resource. The payload may contain the updated data for the resource. 
- **DELETE**: delete an existing resource. 

The above four verbs are the most popular, and most tools and frameworks explicity expose these request verbs. ```PUT``` and ```DELETE``` are sometimes considered specialised versions of the ```POST``` verbm and they may be packaged as ```POST``` requests with the payload containing the exact action: *create, update* or *delete.*


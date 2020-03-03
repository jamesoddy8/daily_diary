### Tuesday 3rd March ###

## Mocks, Stubs & Expectations in Ruby ###

- Mocks are objects that have a similar interface as something else
- Stubs are fake methods and return a specific answer




## Process Modelling ##

Sequence diagram

## Battle Challenge ##

### The Web ###

The whole web is built on client-server relationships. There are different kinds of clients and servers but the relationship is roughly the same: the client is dependent on the server for providing and managing information. Anything that can request a resource from a server can be called a client.

Challenge - setup using httpie
``` brew install httpie ```

### The Hypertext Transfer Protocol (HTTP) ###

Usually, clients and servers talk to each other using the HyperText Transfer Protocol. A client makes a request to a server and gets back a response. It is called a "protocol" because it has a defined structure for requests and responses.

#### URLs ###

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

### HTTP: Status Codes

With URLs and verbs, the client can initiate requests to the server. In return, the server responds with status codes and message payloads. The status code is important and tells the client how to interpret the server response. The HTTP spec defines certain number ranges for specific types of responses.

1xx: Informational Messages

2xx: Successful

3xx: Redirection

4xx: Client Error

5xx: Server Error

### POST / redirect /GET pattern

#### Session

> A ```session``` is a short-term information store that lives on the server. It's very small, but it allows the server to store basic pieces of information, like the names of the current user, across multiple requests. In Sinatra, ```session``` is a Hash, and you can set values for its keys. ```session``` is most often used to store detauls of a logged in user. 
#### Redirect

>```redirect '/route'``` will issue an 'internal GET request' within the server. Check your sever logs when you submit the form: you will see a POST request with the form params, followed by a GET request (the redirect). That internal GET request will activate the ```play.erb``` view. 

## Params 

### Overview

In the context of HTTP requests, parameters provide a way for information to be passed from a user to your application Params are used to allow interactivity on a website, for example by allowing form data to be sent.

Params are passed in the form of a hash, a series of key-value pairs. 

There are several types of parameters that you can use to submit information to your app: 

#### Form Params 

Form params are parameters that are passed from a web page to an application via a form submission. Consider the following code: 

```ruby
server.rb

  post ‘/form’ do
    @username = params[:username]
    puts params
    erb :form
  end
 
```
``` ruby
form.erb
  <form name="input" action=“/form” method=“post”>
  username: <input type=“text” name=“username”>
  password: <input type=“password” name=“password”>

  <input type=“submit” value=“Submit”>
  </form>
  
```
In form.erb you can see the first <form> tag contains 3 attributes: 
  
  - ```name``` - This is the name of the form
  - ```action``` - This is he path to which the form will be sent
  - ```method``` - This is the tyoe of HTTP request via which the form will be sent
  
  



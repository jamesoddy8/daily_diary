### Monday 2nd March 

### Grandma Test  

If you were to give your code to your grandma, would she be able to undertand it?

### Code Review  

If a method is printing strings from an array how do we test for this? E.g. array.each(item) puts item[:price] 

``` 
expect { subject.method }.to output("...").to_stdout 
``` 

Two schools of TDD Chicago & London...

### Why do I not feel any need to use doubles or mocks? ###

London style = use mocks & doubles 
- you get test isolation, if you break one object all the other tests will keep passing
- changes the workflow 
- feature tests 


Chicago style = use mocks & doubles as little as possible

### When to use instance_doubles? ###

Sort of an alternative to feature testing... 

### How do you test a gem? ###

You don't! 

### Goals For The Week  

```
velocity = ( speed / direction ) 

Prioritise direction over speed 
```
By the end of the week you should be able to: 

- Build a simple web app :-1:
- Follow an effective debugging process for web applications :-1:
- Explain the basics of how the web works (e.g. request/response, HTTP, HTML, CSS) :-1:
- Explain the MVC pattern :-1:

Browser | Server
Request
HTTP -> 
TCP/IP 


Response <-
HTML, CSS, JS, IMG
HTTP STATUS codes, such as 404 not found

Developer tools safari/chrome

### Sinatra ###

#### Introducing ```params```

``` rub
get '/random-cat' do
  @name = ["Amigo", "Oscar", "Viking"].sample
  erb:index
end

get '/named-cat' do
  @name = params[:name]
  erb:index
end
```
By using params you enter the parameters into the url so http://localhost:9393/named-cat?name=fuzzy (name = fuzzy)

### Process ###

> Observation
planning was clear
testing process for rspec was well explained
commit stages timed correctly 
thought process for next test/TDD in general was fluid
Refactoring was done at the right time

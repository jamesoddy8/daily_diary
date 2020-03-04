# Wednesday 4th March #

## Params (continued)

### Query String Params 

Query string parameters are passed to the application through the address bar, using a ? as so: 

``` http://localhost:9393/whatsup?name=bruce&surname=wayne ```

The application can handle these params in the controller as follows: 

```ruby 
get '/whatsup' do
  "Whats up " + params[:name] + " " + params[:surname]"
end
```

Query String params are fantastic because they allow you to have descriptive URLs


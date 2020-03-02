### Monday 2nd March ###

### Grandma Test ### 

If you were to give your code to your grandma, would she be able to undertand it?

### Code Review ### 

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

### When to use instance_doubles?###

Sort of an alternative to feature testing... 

### How do you test a gem? ###

You don't! 



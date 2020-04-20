# Tech Test Checklist

# RUBY

### Basics of TDD 

1. Write the smallest possible test case.
2. Run the test and watch it fail. 
3. Make the test pass.
4. Repeat steps 3 & 4 until it passes. 
5. Refactor your new code, make it as simple and clear (or hard depending on how you want it) as possible while keeping the test green. 

## RSpec Basics

### Setting up RSpec

Create a new directory and initialize bundle within it:

```bundle init```

Now you have a Gemfile created, add RSpec to your Gemfile: 

```bundle add rspec``` 

Initalize a git repository 

```git init``` 

Create a new repository in github & then link the repo: 

```
echo "# bank_tech_test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:jamesoddy8/bank_tech_test.git
git push -u origin master
```

### Writing the First Spec

First create a ```spec``` directory 

```ruby
mkdir spec
```
Then create your first spec file within this folder:

```
touch bank_spec.rb
```

Begin with writing the first spec: 

``` ruby
# spec/string_calculator_spec.rb
describe Bank do
end
```
 
In RSpec, we are always describing the *behaviour* of classes, modules and their methods. The ```describe``` block is always used at the top to put specs in a context. It can accept either a class name, in which case the class needs to exist, or any string you would like.

To run the first spec:

```rspec```

The first test will fail which is expected as the class has not been created yet. 

Create a new directory called ```lib```: 

```ruby
mkdir lib
```
Declare ```Bank``` in ```bank.rb```

```ruby
# lib/bank.rb
class Bank
end
```
And require it in your spec: 

```ruby
# spec/bank_spec.rb
require "bank"

describe Bank do 
end 
```
Running RSpec now passes. 

Let's continue writing some code... 

The simplest thing the bank can do is accept an empty string, in which case we might want it to return a zero. The method that shouls be added first is ```add``` .

```ruby 
# spec/bank_spec.rb
describe Bank do
  
  describe ".add" do 
    context "given an empty string" do 
      it "returns zero" do 
        expect(Bank.add("")).to eq(0)
      end
    end
  end
end 

* By convention, class methods are prefixed with a dot ```(".add")```, and instance methods with a dash ```("#add")```. 

* We are using a ```context``` block to describe the context under which the ```add``` method is expected to return zero. ```context``` is technically the same as ```describe```, but is used in different places, to aid reading of the code. 

* We are using an ```it``` block to describe a specific *example*, which is RSpec's way to say "test case". Generally, every example should be descriptive, and together with the context should form an understandable sentence. This one reads as *"add class method: given an empty string, it returns zero"*.

* ```expect(...).to``` and the negative variant ```expect(...).not_to``` are used to define expected outcomes. The Ruby expression they are given (in our case, ```Bank.add(""))``` is combined with a *matcher* to fully define an *expectation* on a piece of code. The matcher we are using here is ```eq```, a basic equality matcher.







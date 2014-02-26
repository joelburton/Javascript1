Javascript Functions
====================

```javascript

function aFunctionThatAddsAndReturnsTheValue(first, second) {
	return first + second;
}

aFunctionThatAddsAndReturnsTheValue(5,10);
```

A function is really just a variable that contains code, so we can use another syntax to declare a function.  
Use whichever one you're comfortable with.  

```
var aFunctionIsJustAVariableThatContainsCode = function() {
	console.log("hello, I'm a function running a console.log() statement.");
};

console.log(aFunctionIsJustAVariableThatContainsCode);
aFunctionIsJustAVariableThatContainsCode();

```
Whenever you see `function(){}` - this is called a function literal. We can put it wherever we want a function to be.


Javascript functions are special though, because they're secretly **objects** underneath.  

```
> function myFn() {console.log("hello")};
undefined
> myFn();
hello
undefined
> myFn.description = "A function that prints hello";
'A function that prints hello'
> myFn
{ [Function: myFn] description: 'A function that prints hello' };
> myFn();
hello
undefined
> myFn.description;
'A function that prints hello'
```

In Javascript, we can pass functions to other functions as arguments. This is a pretty neat trick, considering we have anonymous functions that can be defined in-place. Check this out:

```javascript

function batman(exclamation){
	console.log("NaNaNaNaNaNaNaNa");
	exclamation();
}

//And then, we can pass a function we have previously declared
function obvious(){
	console.log("Batman!");
}

batman(obvious);

//OR we can declare the function right there:

batman(function(){ 
	console.log("CAT MAN!");
});
```

Python Functions
================
```python
def a_function_that_adds_and_returns_the_value(first, second):
	return first + second

a_function_that_adds_and_returns_the_value(5, 10)

def a_function_is_just_a_variable_that_contains_code():
	print "hello, I'm a function running a print statement."

print a_function_is_just_a_variable_that_contains_code

```
Python doesn't contain function literals, just functions declared the normal way. You can use them like they're variables though.

In Javascript, we can pass functions to other functions as arguments. This is a pretty neat trick, considering we have anonymous functions that can be defined in-place. Check this out:

```python

def batman(exclamation):
	print "NaNaNaNaNaNaNaNa" 
	exclamation()

##And then, we can pass a function we have previously declared
def obvious():
	print "Batman!"

batman(obvious)

## But! We can't declare functions in place. So, no dice, CAT MAN.
```

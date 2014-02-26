
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

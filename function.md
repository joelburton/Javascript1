Javascript Functions
====================

We can make functions in Javascript using "function declarations", like this:

```javascript

function addTwoNumbers(first, second) {
	return first + second;
}
```

(note that there's no semicolon at the end of a function declaration)

We can also create functions using a "function expression", where we create a
function and bind it to a variable. When we do it this way, we typically don't give
the function a name (after the word function and before the parameter list);
this is called an "anonymous function".

Here, we make an anonymous function using a function expression, and assign it
to a new variable:

```javascript

var alsoAddsTwoNumbers = function (first, second) {
    return first + second;
};
```

(note that there is a semicolon at the end of an assignment like this—after all,
this is not all that different than `var i = 7;`, except with a function as
the things-we're-assigning-to-the-variable.)

Both of these create functions that do the same thing, so it's often a matter of
style and taste which style you will you.

Either you, you call them like this:

```javascript

addTwoNumbers(5, 10);        // --> 15
alsoAddsTwoNumbers(5, 10);   // --> 15
```

In Javascript, we can pass functions to other functions as arguments.

```javascript

function batman(exclamation){
	console.log("NaNaNaNaNaNaNaNa");
	exclamation();
}

// And then, we can pass a function we have previously declared
function obvious(){
	console.log("Batman!");
}

batman(obvious);
```

The `obvious` function is called `exclamation` inside of the `batman` function, and
when it gets called, it runs the code inside of `obvious`—printing "Batman!".

You can do this with functions you separately defined, like that, but you can also use
function expressions directly:


```javascript

function batman(exclamation){
	console.log("NaNaNaNaNaNaNaNa");
	exclamation();
}

batman(function () {
	console.log("CAT MAN!");
});
```

This passes the newly-defined, anonymous function to the batman function. The
result is the same, though—it calls that new function `exclamation` and then calls it,
printing, in this case, "CAT MAN!".


Python Functions
================

In Python, we have one traditional way to create functions:

```python
def add_two_numbers(first, second):
	return first + second
```

We can call that function either using named parameters or positional parameters:

```python
add_two_numbers(5, 10)                 # --> 15

add_two_numbers(first=5, second=10)    # --> 15
```

In Python, there's an analogous feature for creating function expressions, called
"lambdas". Lambdas are functions that you create like an expression, but the syntax
is a bit different:

```python
also_adds_two_numbers = lambda first, second: first + second
```

(Lambdas are less powerful than full functions, as they can have only a single
expression as the body, and it's always returned. Therefore, they are not used
for commonly).

You can call a Python function and pass it another function, similar to Javascript:

```python

def batman(exclamation):
	print "NaNaNaNaNaNaNaNa" 
	exclamation()

def obvious():
	print "Batman!"

batman(obvious)
```

Javascript Data Structures
==========================

## Comments

```javascript
// Comments look like this -- everything after // is ignored

/* 
   if you need to make
   a comment haiku then these
   stars are for multi lines
*/
```

## Basic Data Types

```javascript

// (note that Javascript people use 'midCase' spellings for variables--
// in the Python world, 'snake_case` is preferred

// Declaring a variable before it's used
var aVariable;

// Declaring a variable *and* assigning to it
var aVariable = 'hello';

// Number
var aNumber = 5;

// Numbers are the same, whether floating-point or integer
var aFloatingPointNumber = 5.5;

// Strings
var aString = "cats";

// Turning a number into a string, also concatenation
var phrase = "I have " + aFloatingPointNumber + " " + aString;
// --> "I have 5.5 cats"
// (what do you suppose happened there?)
// Also note: no Python-style string interpolation ie, no '"I have %s cats" % aNumber'

// Empty types

var emptyOnPurpose = null;    // Very much like Python's 'None'

var emptyBecauseINeverDeclaredIt = undefined;

console.log(aVariableINeverDeclared);    --> console reads "undefined"

// Boolean (true / false) values

var iHateCats = false;
var catsAreAwesome = true;
```

## More Complex Structures  
### Arrays  

An array literal looks like this: `[]`  

```javascript
// Arrays (similar to Python's lists)
  
var listOfMuppets = ["Kermit", "Dr. Teeth", "Gonzo", "Fozzie", "Animal", "Statler", "Waldorf"];
var fibs = [1, 1, 2, 3, 5, 8, 13, 21, 34];

// Arrays are complex, and contain heterogeneous data types
var multiTypeArray = ["things", 5, ["teeth"], {cats: 5, yaks: 2}];

// Length is a property on arrays

listOfMuppets.length;   // --> 7
fibs.length;            // --> 9

//List Slicing

// All the muppets who play instruments
var musicalMuppets = listOfMuppets.slice(0,5);

// All the muppets that are grouchy critics
var criticalMuppets = listOfMuppets.slice(-2);

// All the muppets that aren't Fozzie
var funnyMuppets = listOfMuppets.slice(0,3).concat(listOfMuppets.slice(4));
```

### Objects  

An object literal looks like this: `{}`

```javascript
// Objects (a bit like Python dictionaries)
var linksAdventures = {
	"The Legend Of Zelda" : "NES",
	"Zelda 2: The Adventure of Link" : "NES",
	"The Legend Of Zelda: A Link to the Past" : "SNES"
};

// You can get an item with square-bracket, quoted-key-name, similar to Python:
console.log(linksAdventures["The Legend Of Zelda"]);  // --> NES

// If your keys are legal identifiers (that is, they're made up of just the characters
// legal Javascript variable names, you don't need to quote the keys. This can be a
// little easier to read:

var computerLanguages = {
    python: "nifty",
    javascript: "cool",
    cobol: "not so fun"
};

// You can get a key like that with "dot notation":
console.log(computerLanguages.javascript);    // --> "cool"

// Objects ( we're still talking about -> {} ) can contain anything, even functions!

var enterprise = {
	printCrew: function() {
		console.log("Captain Jean Luc Picard is the only crew you need to know about.")
	},
	warp: function(bearing, warpFactor) {
		console.log("Heading bearing " + bearing + " at Warp Factor " + warpFactor);
	},
	designation: "NCC-1701-D",
	crewComplement: 1014
};

//You can call the functions (which are really called methods) like this:

enterprise.warp("2, 3, mark 5", 8); // --> "Heading bearing 2, 3 mark 5 at Warp Factor 8"

```

Python Structures
=================

## Comments

```python

# Single Line Comment

""" 
Python doesn't really have multi-line comments, but docstrings are often used to
document functions/classes/modules, and, if you use triple quotes around them, can
be several lines long.
"""
```

## Data Types

```python

# Variables
a_variable

# Numbers
a_number = 5

# Floating point behaves the same
a_floating_point_number = 5.5

# Strings
a_string = "cats"

# turning a number into a string, also concatenation

phrase = "I have " + a_floating_point_number + " " + a_string
# --> I have 5.5 cats.

#  We can interpolate in python though
phrase = "I have %d %s" % (a_floating_point_number, a_string)


# Empty types
# Python doesn't have a "null" - it has "None"

empty_on_purpose = None

## But it does not have an "undefined". If something is undefined:
##
##   print empty_because_I_never_declared_it
##
## We're going to get a NameError because python doesn't automatically handle it for us:
##
## Traceback (most recent call last):
##  File "<stdin>", line 1, in <module>
## NameError: name 'empty_because_I_never_declared_it' is not defined

# Boolean (true / false) values - Same but with caps

i_hate_cats = False
cats_are_awesome = True
```

## More Complex Structures  
### Lists

List literal: `[]`

```python
# Lists

list_of_muppets = ["Kermit", "Dr. Teeth", "Gonzo", "Fozzie", "Animal", "Statler", "Waldorf"]
fibs = [1, 1, 2, 3, 5, 8, 13, 21, 34]

# Lists are just as powerful in Python
multi_type_array = ["things", 5, ["teeth"], {"cats": 5, "yaks": 2}]

# Length is a function called len()

len(list_of_muppets)   # 7
len(fibs)              # 9

# List Slicing

# All the muppets that play instruments
musical_muppets = list_of_muppets[0:5]

# All the muppets that are grouchy critics
critical_muppets = list_of_muppets[-2:]

# All the muppets that aren't Fozzie
funny_muppets = list_of_muppets[0:3].extend(list_of_muppets[4:])

# Poor Fozzie. But, hey, at least Python's list slicing has a step argument!

short_muppets = list_of_muppets[::2]

```

### Dictionaries  

Dictionary literal: `{}`

```python
# Dictionaries (key-value in curly braces) - has to have quotes
links_adventures = {
	"The Legend Of Zelda" : "NES",
	"Zelda 2: The Adventure of Link" : "NES",
	"The Legend Of Zelda: A Link to the Past" : "SNES"
}

# You can only access keys this way:
print links_adventures['The Legend of Zelda']   # --> "NES"

# You can do some sneaky extra stuff in Python because of the .keys() and the .values():
print ( "My experience on the " + " and the ".join(set(links_adventures.values())) +
        " can be summed up as: " + " followed by ".join(links_adventures) )

## (Explanation left as exercise to the reader, as a bonus)

# Dictionaries in Python can still contain functions, but the practice is a little different:

def print_crew():
	print "Captain Jean Luc Picard is the only crew you need to know about."

def warp(bearing, warp_factor):
	print "Heading bearing " + str(bearing) + " at Warp Factor " + str(warp_factor)
	
enterprise = {
	"print_crew": print_crew, 
	"warp": warp,
	"designation": "NCC-1701-D",
	"crew_complement": 1014
}

enterprise["warp"]("2, 3, mark 5", 8)  # --> "Heading bearing 2, 3 mark 5 at Warp Factor 8"

# It's Python, though, this kind of thing is commonly done with a class

class StarShip(object):
	def __init__(self,name, designation, crew_complement):
		self.name = name
		self.designation = designation
		self.crew_complement = crew_complement

	def print_crew(self):
		print "Captain Jean Luc Picard is the only crew you need to know about."

	def warp(self, bearing, warp_factor):
		print "Heading bearing " + bearing + " at Warp Factor " + str(warp_factor)

enterprise = StarShip("enterprise", "NCC-1701-D", "1014")

enterprise.warp("5, 7 mark 8", 5)
print "Make it so."

```

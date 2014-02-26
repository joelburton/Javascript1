Javascript Data Structures
==========================

## Data Types
```javascript
//comments look like this

/* 
if you need to make
a comment haiku then these
stars are for multi lines
*/

//variables
var aVariable;

//numbers
var aNumber = 5;

//numbers are the same, whether float or int
var aFloatingPointNumber = 5.5;

//strings
var aString = "cats";

//turning a number into a string, also concatenation

var phrase = "I have " + aFloatingPointNumber + " " + aString;
// I have 5.5 cats.
// (what do you suppose happened there)
//Also note, no string interpolation in JavaScript

//Empty types

var emptyOnPurpose = null;

var emptyBecauseINeverDeclaredIt = undefined;

console.log(anotherEmptyVariable)

//the console would say:
// undefined


//Boolean (true / false) values

var iHateCats = false;
var catsAreAwesome = true;
```

## More Complex Structures  
### Arrays  

An array literal looks like this: `[]`  

```javascript
//Lists (are called arrays in Javascript)
  
var listOfMuppets = ["Kermit", "Dr. Teeth", "Gonzo","Fozzie", "Animal", "Statler", "Waldorf"];
var fibs = [1,1,2,3,5,8,13,21,34];

//Arrays are complex, and contain multitudes (of types)
var multiTypeArray = ["things", 5, ["teeth"], {cats: 5, cucco: 2}];

//Length is a property on arrays

listOfMuppets.length;
// would output 7
fibs.length;
// would output 9

//List Slicing

//All the muppets that play instruments
var musicalMuppets = listOfMuppets.slice(0,5)

//All the muppets that are jerks
var criticalMuppets = listOfMuppets.slice(-2)

//All the muppets that aren't fozzie
var funnyMuppets = listOfMuppets.slice(0,3).concat(listOfMuppets.slice(4))
//The slice function doesn't take an iteration argument, wakka wakka wakka!

```

### Objects  

An object literal looks like this: `{}`

```javascript
//Dictionaries (are called objects in Javascript (which is terrible))
var lonLonRanch = {
	cuccos : 100,
	horses : 5,
	eponas : 1,
	cows : 5,
	crazyOwners : 1
};
//Note that they don't have quotes around the keys, but otherwise look just like dictionaries. That's because they're pretty much used the same way. You don't have to use quotes when you try to get the key.

console.log(lonLonRanch.cuccos);
//Would write : 100



//You can put quotes, especially if you need spaces:
var linksAdventures = {
	"The Legend Of Zelda" : "NES",
	"Zelda 2: The Adventure of Link" : "NES",
	"The Legend Of Zelda: A Link to the Past" : "SNES"
};

//but then you have to access that property (it's called a property) like this:

console.log(linksAdventures["The Legend Of Zelda"]);

// would output : "NES"

//Objects ( we're still talking about -> {} ) can contain anything, even functions!

var enterprise = {
	printCrew: function() {
		console.log("Capitan Jean Luc Picard is the only crew you need to know about.")
	},
	warp: function(bearing, warpFactor) {
		console.log("Heading bearing " + bearing + " at Warp Factor " + warpFactor);
	},
	designation: "NCC-1701-D",
	crewCompliment: 1014
};
//You can call the functions (which are really called methods) like this:

enterprise.warp("2, 3, mark 5", 8)
//"Heading bearing 2, 3 mark 5 at Warp Factor 8";

```

Python Structures
=================

## Data Types
```python

# Single Line Comment

""" 
Multi Line Comment
"""

# Variables
a_variable

# Numbers
a_number = 5
# Floating point behaves the same
a_floating_point_number = 5.5

#Strings
a_string = "cats"

# turning a number into a string, also concatenation

phrase = "I have " + a_floating_point_number + " " + a_string
#  I have 5.5 cats.
#  We can interpolate in python though
phrase = "I have %d %s" % a_floating_point_number, a_string


# Empty types
## Python doesn't have a "null" - it has "None"
empty_on_purpose = None

## But it does not have an "undefined". If something is undefined:
>>> print empty_because_I_never_declared_it

# We're going to get a NameError because python doesn't automatically handle it for us:
"""
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'empty_because_I_never_declared_it' is not defined
"""


# Boolean (true / false) values - Same but with caps

i_hate_cats = False
cats_are_awesome = True
```

## More Complex Structures  
### Arrays

List literal: `[]`

```python
# Lists

list_of_muppets = ["Kermit", "Dr. Teeth", "Gonzo","Fozzie", "Animal", "Statler", "Waldorf"]
fibs = [1,1,2,3,5,8,13,21,34]

# Lists are just as powerful in Python
multi_type_array = ["things", 5, ["teeth"], {"cats": 5, "cucco": 2}]

# Length is a function called len()

len(list_of_muppets)
#  would output 7
len(fibs)
#  would output 9

# List Slicing

# All the muppets that play instruments
musical_muppets = list_of_muppets[0:5]

# All the muppets that are jerks
critical_muppets = list_of_muppets[-2:]

# All the muppets that aren't fozzie
funny_muppets = list_of_muppets[0:3].extend(list_of_muppets[4:])

#Poor fozzie, at least python has iteration though!

short_muppets = list_of_muppets[::2]

```

### Dictionaries  

Dictionary literal: `{}`

```python
# Dictionaries (key-value in curly braces) - has to have quotes
lon_lon_ranch = {
	"cuccos" : 100,
	"horses" : 5,
	"eponas" : 1,
	"cows" : 5,
	"crazyOwners" : 1
}

# And you can only access it this way
print lon_lon_ranch["cuccos"]
# Would write : 100



# You can put quotes, especially if you need spaces:
links_adventures = {
	"The Legend Of Zelda" : "NES",
	"Zelda 2: The Adventure of Link" : "NES",
	"The Legend Of Zelda: A Link to the Past" : "SNES"
}

# You can do some sneaky extra stuff in python because of the .keys() and the .values(): 
print "My experience on the " + " and the ".join(set(links_adventures.values())) + " can be summed up as: " + " followed by ".join(links_adventures.keys())

## (Explanation left as exercise to the reader, as a bonus)

# Dictionaries in Python ( we're still talking about -> {} ) can still contain functions, but the practice is a little different:

def print_crew():
	print "Capitan Jean Luc Picard is the only crew you need to know about."

def warp(bearing, warpFactor):
	print "Heading bearing " + str(bearing) + " at Warp Factor " + str(warpFactor)
	
enterprise = {
	"print_crew": print_crew, 
	"warp": warp,
	"designation": "NCC-1701-D",
	"crew_complement": 1014
}
# But you're really just storing a reference to the function as a value in the dict.

enterprise["warp"]("2, 3, mark 5", 8)
# "Heading bearing 2, 3 mark 5 at Warp Factor 8";

#It's best to use a class here:

class StarShip():
	def __init__(self,name, designation, crew_complement):
		self.name = name
		self.designation = designation
		self.crew_complement = crew_complement

	def print_crew(self):
		print "Starships can have arbitrary crew, depends on the class of vessel"

	def warp(self, bearing, warpFactor):
		print "Heading bearing " + bearing + " at Warp Factor " + warpFactor

enterprise = StarShip("enterprise", "NCC-1701-D", "1014")

enterprise.warp("5, 7 mark 8", 5)
print "Make it so."

```

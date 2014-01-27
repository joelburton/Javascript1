Javascript Data Structures
==========================

==Data Types==
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

//Empty types

var emptyOnPurpose = null;

var emptyBecauseINeverDeclaredIt = undefined;

console.log(anotherEmptyVariable)

//the console would say:
// undefined


//Boolean (true / false) values

var iHateCats = false;
var catsAreAwesome = true;

//Lists (are called arrays in Javascript)

var listOfMuppets = ["Kermit", "Dr. Teeth", "Gonzo", "Animal"];
var fibs = [1,1,2,3,5,8,13,21,34];

//Arrays are complex, and contain multitudes (of types)
var multiTypeArray = ["things", 5, ["teeth"], {cats: 5, cucco: 2, }];

//Length is a property on arrays

listOfMuppets.length;
// would output 4
fibs.length;
// would output 9


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
Javascript Loops
================

###While###

```javascript
var x = 0;
while (x < 5) {
	console.log(x);
	x++;
}
```

###For###

```javascript
var myLotteryNumbers = [4,8,15,16,23,42];
for (var i=0; i < myLotteryNumbers.length; i++){
	console.log("The next winning number is:" + myLotteryNumbers[i]);
}
console.log("I win the lottery!");

```

###For In###

```javascript
//this is an object
var mysteryActor = {
	"Labyrinth" : "Jareth the Goblin King",
	"Basquiat" : "Andy Warhol",
	"The Prestige" : "Nikola Tesla",
	"Arthur and the Invisibles" : "Emperor Maltazard",
	"SpongeBob SquarePants" : "L.R.H"
};

for (var movie in mysteryActor) {
	console.log("Our mystery actor appeared in " + movie + " as " + mysteryActor[movie] + ".")
}

console.log("Who was our mystery actor?");
```

Python Loops
============

###While###

```python
x = 0
while x < 5: 
	print x
	x += 1

```

###For###

```python
my_lottery_numbers = [4,8,15,16,23,42]
for number in my_lottery_numbers:
	print "The next winning number is: %d" % number

print "I win the lottery!"

```

###For In###

```python
## this is a dictionary
mystery_actor = {
	"Labyrinth" : "Jareth the Goblin King",
	"Basquiat" : "Andy Warhol",
	"The Prestige" : "Nikola Tesla",
	"Arthur and the Invisibles" : "Emperor Maltazard",
	"SpongeBob SquarePants" : "L.R.H"
}

for movie in mystery_actor:
	print "Our mystery actor appeared in %s as %s." % (movie, mystery_actor[movie])

print "Who was our mystery actor?"
```

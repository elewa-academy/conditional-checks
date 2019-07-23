# Conditinal Statements

When setting up a series of conditional checks, it is best to structure them according to the logical relationships between the conditions you are checking for.

Why go through all this extra trouble?
* efficiency:
    - if done correctly, your conditionals should never have to check the same condition twice
* readability:
    - if done correctly, you will arrive at one of the simplest and most readable arrangements of conditional checks
* debugging and maintaining:
    - readable code is fixable code
    - when each condition is only checked in one place, it is easier to make sure you've corrected all bugs

The 3 relationships to consider:
1. Mutually Exclusive
    - the two conditions cannot be true at the same time:
		ie - are you dead? are you alive? have you ever existed?
2. Logical Dependancy
    - the two conditions are related.  knowledge about one condition will effect your decision concerning the other condition:
		ie -  did it rain? is the ground wet?
3. Locigally Independant
	- the two conditions are unrelated.  knowledge of one condition provides no information on the other condition:
		ie - you woke up on time for class.  i am dead.

Each classification calls for a differently structured conditional check:

1. Mutally Exclusive  -  'if'/'else'/'else if' information:
```js
if (it_is_a_ball) {
	roll_it;
} else if (it_is_a_cube) {
	stack_it;
} else {
	learn_more_shapes;
};
```

---

2. Logically Dependant  -  nested if statements:
```js
if (you_are_hungry) {
	if (you_can_cook) {
		make_food;
	} else {
		buy_food;
	};
} else {
	dont_eat;
};
```

---

3. Logically Independant  -  sequential if statements
```js
if (you_are_hungry) {
	if (you_can_cook) {
		make_food;
	} else {
		buy_food;
	};
} else {
	dont_eat;
};
if (it_is_a_ball) {
	roll_it;
} else if (it_is_a_cube) {
	stack_it;
} else {
	learn_more_shapes;
};
```  
	  
___  
### Resources  
  
https://revelry.co/coding-without-if-statements/  


___
___
### <a href="http://elewa.education/blog" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/34921062-506450ae-f97d-11e7-875f-6feeb26ad72d.png" width="100" height="40"/></a>

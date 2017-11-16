### Array's .map() Method

It gets called on an existing array and returns a new array based what's returned from the function that's passed as an argument. Let's take a look:

	const names = ['Michael', 'Ryan', 'Tyler'];

	const nameLengths = names.map( name => name.length );
	
Let's go over what's happening here. The .map() method works on arrays, so we have to have an array to start with:

	const names = ['Michael', 'Ryan', 'Tyler'];
	
We call .map() on the names array and pass it a function as an argument:

	names.map( name => name.length );
	
The arrow function that's passed to .map() gets called for each item in the names array! The arrow function receives the first name in the array, stores it in the name variable and returns its length. Then it does that again for the remaining two names.

.map() returns a new array with the values that are returned from the arrow function:

	const nameLengths = names.map( name => name.length );
	 
So nameLengths will be a new array [7, 4, 5]. This is important to understand; the .map() method returns a new array, it does not modify the original array.

This was just a brief overview of how the .map() method works. For a deeper dive, check out .map() on MDN.



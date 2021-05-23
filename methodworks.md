# method works

# map()

### Description:

applies a function to each array element and creates a new array of the returned values.

### How it works:

- Takes a callback function that is called once for each element.
- Calls the callback function and gets the result of the operation run on the element
- Returns a new array with the results> The .map() method creates a new array and doesn't mutate the old array.

### Time Complexity :

O(n)

### Examples:

Ex1:

const numbers = [65, 44, 12, 4];
const newarray = numbers.map(myFunction)
function myFunction(num) {
  return num * 10;
}

Ex2:

`

let arr = [1,2,3,4];

let newArr = arr.map((v,i,a) => {

return v % 2 === 0 ? v * 2 : v;

})

// newArr = [1,4,3,8];

Ex3:

let arr = [1,2,3,4];

let newArr = arr.map((val, i, arr) => { return {
value: val,
index: i
};});

# reduce()

### Description:

used to apply a function to each element in the array to reduce the array to a single value

### How it works:

the callback would be invoked n times, with the arguments and return values in each call he value returned by reduce() would be that of the last callback invocation.

### Time Complexity :

O(n)

### Example:

Ex1:

const arr1 = [1, 2, 3, 4];

const reducer = (accumulator, currentValue) => accumulator + currentValue;

console.log(arr1.reduce(reducer));

Ex2:

data = [2, 4, 6, 8, 10]

const reducer = (accumulator, currentValue, currentIndex, array) => accumulator + currentValue

result = data.reduce(reducer)

console.log(result)

# filter()

Description:

returns a new array created from all elements that pass a certain test preformed on an original array

### how it works:

- Will take a test function
- Returns a new array containing the elements that matches the set test
- Returns an empty array if there are no matches

### Time Complexity :

O(n)

### Examples:

Ex1:

const names = ['John', 'Peter', 'James', 'Pammy'];

// Filter the array for names having 'am'

const myName = names.filter(name => name.includes('am'));

// Output new array

console.log(myName)

Ex2:

const ages = [14, 12, 18, 21, 10];

// filter array for numbers in a range

const canSeeDeadpool = ages.filter(function(age){

return age >= 18;

})

Ex3:

const students = [

{

name: 'Peter',

score: 50

},

{

name: 'Sarah',

score: 40

},

{

name: 'Andy',

score: 33

},

{

name: 'Grace',

score: 60

}

]

const studentsThatPassed = students.filter(function(student){

return student.score >= 50

# forEach():

### Description:

calls a function once for each element in an array, in order.

### How it works:

- Current Value (required) - The value of the current array element
- Index (optional) - The current element's index number
- Array (optional) - The array object to which the current element belongs

### Time Complexity :

O(n)

### Examples:

Ex1:

let array = [1, 2, 3, 4, 5]

// Double each number and display

array.forEach(function(number){

console.log(number*2)

})

Ex2:

const days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'];

days.forEach(day => {

console.log(day);

})

Ex3:

const students = ['Jerry', 'Mary', 'Brenda', 'John'];

const classA = [];

students.forEach(student => {

classA.push(student)

});

console.log(classA);

# sort():

### Description:

sorts the elements of an array and returns the sorted array

### How it works:

1. First, declare an array
2. Second, sort the array by the length of its element using the sort() method. We output the elements of the array data to the web console whenever the sort() method invokes the comparison function .

### Time Complexity :

O(n log(n))

### Examples:

Ex1:

const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();

Ex2:

Const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});

Ex3:

const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b - a});

# slice():

### description:

returns a shallow copy of a portion of an array into a new array object selected from start to end ( end not included) where start and end represent the index of items in that array.

### How it works:

- The slice() method returns the selected elements in an array, as a new array object.
- The slice() method selects the elements starting at the given *start* argument, and ends at, *but does not include*, the given *end* argument.

### Time Complexity :

O(n)

### Examples:

Ex1:

Const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const  citrus = fruits.slice(1, 3);

Ex2:

const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const myBest = fruits.slice(-3, -1);

Ex3:

const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));

console.log(animals.slice(2, 4));

# pop():

### description:

removes the last element from an array and returns that value to the caller.

### How it works:

N/A

### Time Complexity :

O(1)

### Examples:

Ex1:

const arr = [34, 234, 567, 4];

const popped = arr.pop();

console.log(popped);

console.log(arr);

Ex2:

Const  fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();

Ex3:

const languages = ["JavaScript", "Python", "Java", "C++", "Lua"];

const toBePop = languages.pop();console.log(languages);

console.log(toBePop);

# shift():

### Description:

method removes the **first** element from an array and returns that removed element.

### How it works:

- Removes the element at the beginning of the array.
- Mutates the parent array reducing the length.
- Returns the removed element.

### Time Complexity :

O(n)

### Examples:

Ex1:

const myFish = ['angel', 'clown', 'mandarin', 'surgeon'];

console.log('myFish before:', JSON.stringify(myFish));

const shifted = myFish.shift();

console.log('myFish after:', myFish);

console.log('Removed this element:', shifted);

Ex2:

const names = ["Andrew", "Edward", "Paul", "Chris" ,"John"];

while( typeof (i = names.shift()) !== 'undefined' ) {console.log(i);}

Ex3:

const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();

# push():

### description:

appends one or more value to the last position of an array. This method mutates the array returning the new length of the array.

### How it works:

- Takes a value or values as arguments.
- Adds the value(s) to the end of the array.
- Returns the new length of the array

### Time Complexity :

O(1)

### Examples:

Ex1:

let newArray = [1, 2, 3, 4, 5].push(6)

Ex2:

const names = ['Johnny', 'Pete', 'Sammy']

console.log(names.push('Larry'));

Ex3:

const todos = [{name: 'Clean room', complete: false}];

todos.push({name: 'Cook food', complete: true})

console.log(todos)

# unShift()

### description:

appends a number of values to the start of a given array. It then returns the new length of the array.

### How it works:

will return the length of the array after adding the new elements.

### Time Complexity :

O(n)

### Examples:

Ex1:

let array = [10, 20, 30, 40, 50]

let newLength = array.unshift(2, 5)

console.log(newLength)

console.log(array)

Ex2:

const items = ['Cedar', 'Fruits', 'Table'];

items.unshift('wine', 'glass');

console.log(items);

Ex3:

const cart = [

{

item: "bread",

price: 2000,

},

{

item:"milk",

price: 1000

}

]

cart.unshift({item: "eggs", price: 500})

console.log(cart)

# includes():

### description:

checks if an array contains a given element.

### How it works:

- Takes a value as an argument
- Checks the array if the value exists within the array
- Returns true or false.
- If no argument is provided, it returns false.

### Time Complexity :

O(n)

### Examples:

Ex1:

const classNames = ['amazon', 'facebook', 'google', 'scotch']

let partOfClass = classNames.includes('microsoft')

console.log(partOfClass)

Ex2:

const names = ['Johnny', 'Pete', 'Sammy']

const myName = 'Pete';

const hasMyName = names.includes(myName);

console.log(hasMyName);

Ex3:

const days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'];

const month = 'May';

const isDay = days.includes(month);

console.log(isDay);

# indexOf()

### description:

checks for the first appearance of a provided string argument within the calling string and returns the index. It returns -1 if the string argument can’t be found within the calling String.

### How it works:

- Takes a string argument
- Checks if the provided argument exists within the calling string object
- Returns the index of the first appearance of the provided argument, -1 if it can’t

### Time Complexity :

O(n)

### Examples:

Ex1:

let sentence = "find the index of the first occurrence of me in this sentence"

const keyWord = "me"

let keyWordIndex = sentence.indexOf(keyWord)

console.log(keyWordIndex)

ex2:

const sentence = 'Friday is the last day';

const day = 'Friday';

const hasDay = sentence.indexOf(day);

console.log(hasDay);

# every()

### Description :

checks that each element in an array passes a set test. This method will return true if all the elements pass the set. Once an element that fails the test is found, the method returns false.

### How it works:

- Takes a callback function that implements a test
- Checks if all the elements pass the test
- Returns true if every element passes the test.
- Returns false an element fails test

### Time Complexity :

O(n)

### Examples:

Ex1:

let result = [10, 5, 20, 100].every(function(number){

return number < 150

})

console.log(result)

ex2:

const array = [20, 21, 23, 15, 2]

const isLessThan100 = (number)=> number < 100

let result = array.every(isLessThan100)

ex3:

const ages = [17, 18, 22, 25];

const drivingAge = 16;

let canDrive = ages.every(function(age){return age >= drivingAge;});

console.log(canDrive)
## `Destructuring `
feature in JavaScript that allows you to extract values from arrays and objects and assign them to variables in a more concise and readable way

###### 1. Destructuring Array 

``````js
const colors = ["red", "green", "blue"];
const [firstColor, secondColor, thirdColor] = colors; //destructuring syntax in an array

console.log(firstColor);  // "red"
console.log(secondColor); // "green"
console.log(thirdColor);  // "blue"

``````
also you can skip some values that you may don't want it in your code :

`skipping values`
``````js
const colors = ["red", "green", "blue"];
const [firstColor, , thirdColor] = colors;

console.log(firstColor);  // "red"
console.log(secondColor); // undefined
console.log(thirdColor);  // "blue"
``````


###### 2. Destructuring Object
``````js
const person = { name: "Alice", age: 30 };
const { name, age } = person;

console.log(name); // "Alice"
console.log(age);  // 30
``````
Renaming Variables: You can assign a different variable name when extracting values from an object.
``````js
const { name: fullName, age: personAge } = person;
``````
Default Values: You can provide default values for properties in case they are not present in the object.
``````js
const { name = "Unknown", job = "Unemployed" } = person;
``````
3. Destructuring in Function Parameters:

Destructuring in Function Parameters: You can destructure objects directly within function parameters.
``````js
function printPersonInfo({ name, age }) {
  console.log(`Name: ${name}, Age: ${age}`);
}

const person = { name: "Bob", age: 25 };
printPersonInfo(person); // Outputs: "Name: Bob, Age: 25"
``````
Destructuring Arrays in Function Parameters: Similarly, you can destructure arrays within function parameters.
``````js
function printColors([firstColor, secondColor]) {
  console.log(`Colors: ${firstColor}, ${secondColor}`);
}

const colors = ["red", "blue"];
printColors(colors); // Outputs: "Colors: red, blue"
``````
---
## `For...of loop`
It lets you loop over iterable data structures such as Arrays, Strings, Maps

Basic Syntax :
``````js
for (const element of iterable) {
  // Code to be executed for each element
}
``````
**element**: A variable that represents the current element in each iteration.
**iterable**: An object that has an iterable protocol, such as an array, string, map, set, etc.

###### 1. Iterating over an Array:

``````js
const fruits = ["apple", "banana", "cherry"];

for (const fruit of fruits) {
  console.log(fruit);
}

// Outputs:
// "apple"
// "banana"
// "cherry"
``````
###### 2. Iterating over a String:

``````js
const message = "Hello";

for (const char of message) {
  console.log(char);
}

// Outputs:
// "H"
// "e"
// "l"
// "l"
// "o"
``````
it's alright if you don't understand maps and sits you will find their summary in Data Structure down there 

###### 3. Iterating over a Map:

``````js
const person = new Map();
person.set("name", "Alice");
person.set("age", 30);

for (const [key, value] of person) {
  console.log(`${key}: ${value}`);
}

// Outputs:
// "name: Alice"
// "age: 30"
``````
###### 4. Iterating over a Set:


``````js
const uniqueNumbers = new Set([1, 2, 3, 2, 4, 1]);

for (const number of uniqueNumbers) {
  console.log(number);
}

// Outputs:
// 1
// 2
// 3
// 4
``````
###### 5. Iterating over an object :

for of loop cannot work on an object directly, since an object is not iterable
if you tried to use the basic syntax it will give a type error so we use built-in methods to make the objects iteratable :

1. Object keys 

The Object.keys() method receives an object as its parameter and turns the properities of an object to an array

+ Ex:

``````js
const car2 = {
    speed: 200,
    color: "red"
}
console.log(Object.keys(car2)); // ['speed','color']
``````
with for...of loop :
``````js
const car2 = {
    speed: 200,
    color: "red"
}

for(const key of Object.keys(car2)){
    console.log(`Key:${key}, Value:${car2[key]}` ); 
    // key : speed , value : 200
    // key : color , value : red
}
``````
2. Object values
same as object keys but it outputs the values 
+ Ex:
``````js
const car3 = {
    speed: 300,
    color: "yellow"
}
console.log(Object.values(car3)); // [300, 'yellow']
``````
with for..of loop :
``````js
const car3 = {
    speed: 300,
    color: "yellow",
    };
    for (let val of Object.values(car3)) {
        console.log("Value:",val);
        // output : Value: 300
        //         Value: yellow
    }
``````
3. Object entries

it returns an array with all the key and its corresponding value in a tuple format
+ Ex:

``````js
const car4 = {
    speed: 400,
    color: 'magenta'
}
console.log(Object.entries(car4));
//output : [['speed', 400],['color', 'magenta']]
``````
With For-Of Loop :
``````js
const car5= {
    speed:19876,
    };
    for (let entry of Object.entries(car5) ) {
        console.log('Entry:',entry);// Entry:[ 'speed', 19876 ]
    };
``````
---
## `For...in loop`
The **for…in** statement iterates over *all* properties of an object that are enumerable or own properties. It is also used to iterate

in nutshell it's the same as for...of loop but the difference is that iterates all the properities in the parent class and child class while the for...of loop iterates only the child class properties 

i will explain this difference

Basic Syntax :
``````js
for (const element in iterable) {
  // Code to be executed for each element
}
``````
1. Purpose :

so the difference between both :
**for...of loops** : It is primarily used for iterating over the values of iterable objects ( arrays, strings, maps, sets) and provides direct access to the values.

**for...in Loop**: It is used for iterating over the enumerable properties of objects, including object properties and prototype properties **(parent class)**. It provides access to the property names (keys) rather than the values.

2. Avoiding Prototype Properties:
**for...of Loop**: It does not iterate over prototype properties of objects. It only iterates over the values of the object itself.
**for...in Loop** : iterates over the prototype properties

+ Ex : 

``````js
const car = {
engine: true
}

const sportsCar = Object.create(car);
sportsCar.speed = "fast";
console.log("The sportsCar object: ", sportsCar);

for (prop in sportsCar) {
console.log('', prop); // speed , engine(the prototype property)
}

for (prop of Object.keys (sportsCar)) {
console.log(' ', prop + ": " + sportsCar [prop]); // speed : fast
}
``````
---
## `Template literals`

it's an alternative way for string added in ES6 version it's delimited with backticks `` instead of double quotes " " or single quotes ' ' 

template literals has many features that you can use :

1. variable interpolation
``````js
let greet = "Hello";
let place = "World";
console.log(`${greet} ${place} !`) //display both variables using template literals
``````
2. Multiline strings and string concatenation with backticks
``````js
console.log(`Hello
how can i help 
nice to see you `)
/*  Hello
how can i help 
nice to see you */
``````
---
## `Data Structures`

#### 1.Arrays:

Arrays are ordered collections of values, accessed by numeric indices.
They can hold elements of different data types.
Example:
``````js
const fruits = ["apple", "banana", "cherry"];
``````

also array has some methods that is used to manipulate the array data 

1. `For each`
method is used for iterating over the elements of an array and performing a specified action (callback function) on each element. It doesn't create a new array; instead, it modifies the original array in place.

Example:
``````js
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((element, index) => { //it's an arrow method we use => instead of a callback function
  console.log(`Element at index ${index}: ${element}`);
});
``````
2. `Filter`
method creates a new array by filtering out elements from the original array that meet a specified condition, as defined by a callback function. It returns a new array containing only the elements that satisfy the condition.

Example:

``````js
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((element) => element % 2 === 0);
console.log(evenNumbers); // Outputs: [2, 4]
``````

3. `Maps High order function`
The map() method creates a new array by applying a specified transformation (callback function) to each element of the original array. It returns a new array containing the results of applying the function to each element.

Example:

``````js
const numbers = [1, 2, 3, 4, 5];

const squaredNumbers = numbers.map((element) => element ** 2);
console.log(squaredNumbers); // Outputs: [1, 4, 9, 16, 25]
``````
Objects:

Objects are collections of key-value pairs. Keys are strings (or symbols), and values can be of any data type.
Objects are commonly used for representing complex data structures.
Example:
``````js
const person = {
  name: "Alice",
  age: 30,
};
``````
#### 2.Strings:

Strings are sequences of characters and are immutable (cannot be changed once created).
They have various built-in methods for manipulation.
Example:
``````js
const message = "Hello, World!";
``````
#### 3.Numbers:

JavaScript supports both integers and floating-point numbers.
Numbers are used for arithmetic operations.
Example:
``````js
const price = 19.99;
``````
#### 4.Booleans:

Booleans represent true or false values and are often used in conditional statements.
Example:
``````js
const isTrue = true;
``````
#### 5.Maps:

Maps are collections of key-value pairs that allow any data type as keys.
They maintain the order of insertion and provide efficient key-based retrieval.
Example:
``````js
const map = new Map();
map.set("name", "Alice");
map.get("name") // returns "Alice"
``````
#### 6.Sets:

Sets are collections of unique values (no duplicates).
They are useful for storing unique items and efficiently checking for existence.
Example:
``````js
const uniqueNumbers = new Set([1, 2, 3, 2, 4, 1]);
``````
Arrays and Objects (As Composite Data Structures):

Arrays and objects can be nested within each other to create more complex data structures.
This allows you to represent hierarchical or tabular data.
Example:
``````js
const users = [
  { name: "Alice", age: 30 },
  { name: "Bob", age: 25 },
];
``````
---
## `Spread Operator`
1. Copying Arrays and Objects:

You can use the spread operator to create shallow copies of arrays and objects. This allows you to work with a duplicate without modifying the original data.

Copying an Array:

``````js
const originalArray = [1, 2, 3];
const copyArray = [...originalArray];

console.log(copyArray); // Outputs: [1, 2, 3]
``````
Copying an Object:

``````js
const originalObject = { name: "Alice", age: 30 };
const copyObject = { ...originalObject };

console.log(copyObject); // Outputs: { name: "Alice", age: 30 }
``````
2. Combining Arrays:

You can use the spread operator to combine two or more arrays into a single array.

``````js
const array1 = [1, 2];
const array2 = [3, 4];
const combinedArray = [...array1, ...array2];

console.log(combinedArray); // Outputs: [1, 2, 3, 4]
``````
3. Spreading Elements in Function Arguments:

When calling a function, you can spread an array into its individual elements as arguments.

``````js
function add(a, b, c) {
  return a + b + c;
}

const numbers = [1, 2, 3];
const result = add(...numbers);

console.log(result); // Outputs: 6
``````
4. Creating a Copy with Additions:

You can use the spread operator to create a copy of an array or object while adding new elements or properties.

``````js
const originalArray = [1, 2, 3];
const newArray = [...originalArray, 4, 5];

console.log(newArray); // Outputs: [1, 2, 3, 4, 5]
``````
5. Converting a String to an Array of Characters:

You can use the spread operator to convert a string into an array of its individual characters.

``````js
const text = "Hello";
const charArray = [...text];

console.log(charArray); // Outputs: ["H", "e", "l", "l", "o"]
``````
---
## `Rest operator`
the same as spread operator except you can pass some elements with it for example:
``````javascript
//Destructuring Arrays
const [first, second, ...rest] = [1, 2, 3, 4, 5];

console.log(first); // Outputs: 1
console.log(second); // Outputs: 2
console.log(rest); // Outputs: [3, 4, 5]
``````
``````js
// Destructuring Objects
const { name, age, ...rest } = { name: "Alice", age: 30, country: "USA" };

console.log(name); // Outputs: "Alice"
console.log(age); // Outputs: 30
console.log(rest); // Outputs: { country: "USA" }
``````
---

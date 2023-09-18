## `Functions`
- Functions are fundamental building blocks in programming that encapsulate a set of instructions and can be executed multiple times with different input values.
- They allow you to organize and modularize code, promote reusability, and make your codebase more maintainable. Functions play a crucial role in achieving abstraction and implementing complex logic.

an overview of functions :

you can declare functions using __`function`__ keyword, followed by a function name, a set of parameters within parentheses, and a code block enclosed in curly braces

+ Ex:

        function greet(name) {
            console.log(`Hello `+name+'!');
        }

To execute a function, you call it by using its name followed by parentheses, and provide values (arguments) for its parameters and parameters are the values of the function like **name** in the function above.
+ Output:

        greet(`Alice`) // outputs Hello Alice!

also you can declare function with `return` statement instead of `console.log` that so you can use the returned value in other parts of your code
+ Ex:

        function add(a, b) {
            return a + b;
        }
        const sum = add(3, 5); // sum is 8

you can also assign function to variables and it's called **function expression** these functions can be anonymous or named 

+ Ex(anonymous):

        const multiply = function(x, y) {
            return x * y;
        }; //anonymous function it doesn't have a name
        console.log(multiply) //this is the way you can call it by variable name

+ Ex(named):

        const factorial = function calcFactorial(n) {
            if (n === 0) {
                return 1;
            } else {
                return n * calcFactorial(n - 1);
            }
        };

        const result = factorial(5); // result is 120

---
## `Array`
An array in JavaScript is an ordered list of values. It's like a collection that contains multiple items and each item has its own index number

- values in array are all part of groubs
- values are set in a specific sequence
- values can be accessed through their index number

+ Ex:

Creating  arrays:

    const numbers = [1, 2, 3, 4, 5];
    const names = ['Alice', 'Bob', 'Charlie']; 

Accessing Elements:

    const firstNumber = numbers[0]; // 1
    const secondName = names[1];    // 'Bob'

Modifying Elements:

    numbers[2] = 10;   // numbers is now [1, 2, 10, 4, 5]
    names[0] = 'Eve';  // names is now ['Eve', 'Bob', 'Charlie']

Array Length:

    const length = numbers.length; // 5

Adding and Removing Elements:

    numbers.push(6);       // Add 6 to the end
    names.pop();           // Remove the last element
    numbers.unshift(0);    // Add 0 to the beginning
    names.shift();         // Remove the first element

---
## `Objects`
complex data structures that allow you to store and organize related data and functionality into one single variable or object.

Creating an object has a several ways :

1. Object Literal(simplest way) : 

        const person = {
            firstName: 'Alice',
            lastName: 'Johnson',
            age: 30
        };

2. Constructor function :

        function Person(firstName, lastName, age) {
            this.firstName = firstName;
            this.lastName = lastName;
            this.age = age;
        }
        const person = new Person('Alice', 'Johnson', 30);

Accessing Properties:

    console.log(person.firstName); // Alice and this type of accessing is called dot notation
    console.log(person['lastName']); // Johnson and this one is bracket notation

both dot and bracket do the same function but the bracket notation has a feature that dot doesn't have that it can evaluate expression example :

    var arrOfKeys = ['speed', 'altitude', 'color'];
    var drone = {
        speed: 100,
        altitude: 200,
        color: "red"
    }
    for (var i = 0; i < arrOfKeys.length; i++) {
        console.log(drone[arrOfKeys[i]]) // 100 200 red
    }


Adding and Modifying Properties:

    person.city = 'New York'; // Add new property
    person.age = 31; // Modify existing property

Methods:
You can include functions as object properties, known as methods

    const calculator = {
        add(a, b) {
            return a + b;
        },
        subtract(a, b) {
            return a - b; 
        }
    };
    console.log(calculator.add(3, 5)); // 8

Nesting Objects:
Objects can be nested within other objects, creating a hierarchy.

    const user = {
        name: {
            first: 'John',
            last: 'Doe'
        },
        age: 25
    };
    console.log(user.name.first); // John

---
## `Math object`

### Number constants

The PI number: `Math.PI` which is approximately **3.14159**

The Euler's constant: `Math.E` which is approximately **2.718**

The natural logarithm of 2: `Math.LN2` which is approximately **0.693**

### Rounding methods
These include: 

`Math.ceil()` - rounds up to the closest integer 

`Math.floor()` - rounds down to the closest integer 

`Math.round()` - rounds up to the closest integer if the decimal is .5 or above; otherwise, rounds down to the closest integer 

`Math.trunc()` - trims the decimal, leaving only the integer

### Arithmetic and calculus methods


`Math.pow(2,3)` - calculates the number 2 to the power of 3, the result is 8 

`Math.sqrt(16)` - calculates the square root of 16, the result is 4 

`Math.cbrt(8)` - finds the cube root of 8, the result is 2 

`Math.abs(-10)` - returns the absolute value, the result is 10 

**Logarithmic methods**: `Math.log()`, `Math.log2()`, `Math.log10()` 

Return the minimum and maximum values of all the inputs: `Math.min(9,8,7)` returns 7, `Math.max(9,8,7)` returns 9.

**Trigonometric methods**: `Math.sin()`, `Math.cos()`, `Math.tan()`, etc.

random method : `Math.random()` returns a random number between *0* and *1* like **0.9 or 0.55465**

---
## `String`

a sequence of characters that represents text

#### Creating Strings:
You can create strings in JavaScript using single quotes ('), double quotes ("), or backticks (`). All three methods are valid, but backticks allow for more advanced features like string interpolation.

    const singleQuoted = 'Hello, world!';
    const doubleQuoted = "Hello, JavaScript!";
    const backticks = `Hello, ${language}!`; // Example of string interpolation

#### String Interpolation:
With backticks, you can use string interpolation to embed expressions or variables directly within a string using ${}.

    const name = 'Alice';
    const greeting = `Hello, ${name}!`; // Hello, Alice!

#### Escape Characters:
You can use escape characters to include special characters within strings, such as newline (\n), tab (\t), double quote (\"), and more.


    const message = "This is a \"quoted\" string.";
    const multiline = "Line 1\nLine 2";

#### String Length:
You can find the length of a string using the length property.


    const text = "Hello";
    console.log(text.length); // 5

#### Accessing Characters:
You can access individual characters of a string using square brackets and their index.

    const word = "JavaScript";
    console.log(word[0]); // J
    console.log(word[4]); // S

#### String Methods:
JavaScript provides a wide range of built-in methods for manipulating and working with strings. Some common methods include toUpperCase(), toLowerCase(), charAt(), substring(), split(), indexOf(), and many more.

    const sentence = "Welcome to JavaScript";
    console.log(sentence.toUpperCase()); // WELCOME TO JAVASCRIPT
    console.log(sentence.toLowerCase()); // welcome to javascript
    console.log(sentence.charAt(0)); //W
    console.log(sentence.indexOf("J")); // 11  also there is lastindexof do the same function but backwords
    console.log(sentence.lastIndexOf('JavaScript')) //11
    console.log(sentence.split(" ")) //["Welcome","to", "JavaScript"]
    console.log(sentence.includes('to'));// true if it finds it
    console.log(sentence.concat(" the".concat(" Es").concat("6 ver")).concat("sion"))



#### Immutability:
Strings in JavaScript are immutable, which means that once a string is created, its contents cannot be changed. String methods that appear to modify a string actually return a new string with the modified content.


    let text = "Hello";
    text = text + ", world!"; // Creates a new string 

---
## `Type of Data`

typeof is a function that returns the type of data passed

+ Ex :


        var test = typeof('what is this?'); //returns string the used datatype for words and characters
        var test = typeof(10); // number the used datatype for numbers 
        var test = typeof (3.14); // number the used datatype for numbers 
        var test = typeof(true); // boolean used for choices like true or false , 1 or 0
        var test = typeof(false); // boolean
        var test = typeof(1 < 2); // boolean used for comparison that also return true or false
        var test = typeof([1,2,3]); // object because arrays in js defined as objects
        var test = typeof({ first Property: 1 }); //object because it's an object property
        var test = typeof(function abc(){ console.log('abc'); }); //function because functions in js are all about objects with methods and methods

> **Note**: in javaScript we use for numbers data type number not an int and float just for simplicity and dynamic typing but you can specify it using external libraries 
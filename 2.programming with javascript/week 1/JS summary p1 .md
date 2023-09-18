## `Comments`
Comments are used in javascript to describe the structure of code and the interpreter ignores it 
also the developers use it express or define their own ideas

comments also used for many other situations :
+ Trying to understand how a given piece of code works.

+ Testing different solutions to a coding problem - while not having to delete existing code.

+ Debugging - trying to pin-point why your code is broken or behaving unprediticably.

. Comments can be single line or multi-line comments, which start with two forward slashes (`//`) for a single line comment and (`/*`) for multi-line comments and ends with (`*/`)

+ Syntax :

        // this is single line comment
        /* This is a multi-line comment */

---
## `Semicolon`

In JavaScript, the semi-colon - the ; character - has a similar purpose to (`.`) in English : it is used to clearly delimit parts of the code from some other parts of the code.

in nutshell it's used to terminate the line of code in JS 

---
## `Automatic Semi-colon Insertion(ASI)`

feature in Javascript that makes the browsers filling the blanks if the semi-colon missed 
it makes no difference if a semi-colon is added or not, since the browser is likely to figure it out anyway.

---
## `Console.log`

outputs a message to the web console
can come with different type of syntax structure 

+ Ex:

        console.log("Hello world");
        console.log("%cHello world","font-size:40px;color:red); /* in this syntax we use `%c` so we can style the console It means that it will convert your method's argument as CSS
        console.log("Hello"+"World"+"mate");
        console.log("Hello","World","mate");

---
## `Variables`

Variables allow us to make the exact same code produce different results, making our programs versatile


when you make a variable it goes through many processes

+ Variables declartion

the process that you give the variable a name and declared

        var process; this is how you declare a variable with var
        let person; another way to declare a variable 

the difference between the var and let is var a function scooped variable while let is block scooped variable
+ variables assignment

the process that you give the variable a value

        process = 'first step';
        person = "second step";

+ variable initialization

a process that it's a variable declartion and assignment 

        var process ='first step';
        var person ='second step';

---
## `Data Types`
describe the different types or kinds of data that we use when we declare a variable 
there are a 7 primitive types in javascript

1. Numbers 

(integers) 
- whole numbers like 23456890 (positive & negative), floating point number like .2,.3 etc.. EX:

        var num = 12;
        var floatNum= -12.3 ;

2. Null
is "nothing". It is supposed to be something that doesn't exist.

        var person =null;

3. strings
are textual information. they can contain letters,numbers,special characters but not spaces. EX:

        var str="hello world"


4. boolean
represents two values : true and false

        var x=5;
        var y=6;
        var z=5;
        (x==y) retrun false
        (x==z) return true

5. undefined
a variable without a value, has the value undefined Ex:

        var car; // Value is undefined, type is undefined


6. BigInt
used to store integer values that are too big to be represented by a normal JavaScript Number

        var x = BigInt("123456789012345678901234567890");

7. Symbol
A symbol is an object created using new Symbol() constructor function which represents unique identifier for each property name.

+ Ex :

        const firstName = Symbol('firstName');
        const lastName = Symbol('lastName');
        const age = Symbol('age');

---
## `Operators`
operators are the way a special symbols used to perform operations on operands

operators have three main types :

1. Arithmetic Operator :

        let z = x + y;
        let z = x - y;
        let z = x * y;
        let z = x / y;

2. Comparison Operator :

        x > 8      // x greater than 8
        x < 8      // x less than 8 
        x >= 8     // x greater than or equal to 8
        x <= 8     // x less than or equal to 8
        x == 8     // x equal to 8
        x === 8    // x equal value and equal type to 8
        x != 8     // x not equal to 8
        x !== 5    // x not equal value and equal type to 8

3. logical operators :

        (x < 10 && y > 1)
        (x == 5 || y == 5)
        !(x == y) 

---
## `Numbers`

In JavaScript, numbers are a data type used to represent numeric values. They can be integers or floating-point numbers (decimals). Here's a quick overview with examples:

#### `Integers`:
Whole numbers without decimal points.

+ Ex:

        const age = 25;
        const quantity = -10;
        

#### `floating points`:
Decimal numbers that can have fractional parts.
+ Ex:

        const pi = 3.14159;
        const price = 99.99;

#### `Operators for maths`:
You can perform arithmetic operations on numbers.
+ Ex:


        const sum = 5 + 3;      // Addition
        const difference = 7 - 2; // Subtraction
        const product = 4 * 6;   // Multiplication
        const quotient = 10 / 2; // Division

#### `NaN (Not-a-Number)`:
A special value representing an undefined or unrepresentable value in a mathematical operation.

+ Ex:


        const result = 'Hello' * 2; // NaN
the output will be : <ins>NaN</ins>
#### `Infinity(Positive Infinity)` & `-Infinity(Negative infinity)`:
Special values representing positive and negative infinity.

+ Ex:


        const positiveInfinity = Infinity;
        const negativeInfinity = -Infinity;

#### `Number Methods`:
Numbers have built-in methods for various operations.

+ Ex:


        const num = 8.75;
        const rounded = num.toFixed(1); // Returns '8.8'

#### `Parsing`:
Converting strings to numbers.

+ Ex:

        const strNum = '42';
        const parsedNum = parseInt(strNum); // 42

Numbers are fundamental in JavaScript and are used extensively for mathematical calculations, data manipulation, and various programming tasks.

---
## `Strings` 

 used to represent sequences of characters. They are used to store and manipulate text-based information. Here's a quick overview with examples:

#### `Creating Strings`:
Strings can be created using single quotes, double quotes, or backticks.

+ Ex:


        const name1 = 'Alice';
        const name2 = "Bob";
        const message = `Hello, ${name1} and ${name2}!`;
#### `String Length`:
You can determine the length of a string using the .length property.

+ Ex:


        const text = 'Hello, world!';
        const length = text.length; // 13
#### `String Concatenation`:
Strings can be combined using the + operator.

+ Ex:


        const firstName = 'John';
        const lastName = 'Doe';
        const fullName = firstName + ' ' + lastName; // 'John Doe'
#### `String Methods`:
Strings have built-in methods for various operations.

+ Ex:


        const message = '   Hello, world!   ';
        const trimmedMessage = message.trim(); // 'Hello, world!' trim built in function to remove whitespace before and after the string
#### `String Indexing`:
Individual characters in a string can be accessed using zero-based indexing.

+ Ex:


        const word = 'example';
        const firstChar = word[0]; // 'e'
        const lastChar = word[word.length - 1]; // 'e'
#### `Escape Characters`:
Certain characters like quotes can be included within strings using escape characters.

+ Ex:


        const text = 'She said, "Hello!"';
#### `String Conversion`:
You can convert values to strings using the String() function or the .toString() method.

+ Ex:


        const num = 42;
        const strNum = String(num); // '42'
Strings are a fundamental data type in JavaScript and are used for storing and manipulating text-based information, such as messages, names, and content displayed on web pages.

---
## `Booleans and operators in Depth`

### Boolean Values (`true`, `false`) :
 represents logical values: true or false. Booleans are used for making decisions and controlling the flow of code. Here's a quick overview with examples:

Creating Booleans:
Boolean values are created using the true and false keywords.

+ Ex:


        const isTrue = true;
        const isFalse = false;

Boolean Methods:
Some methods return Boolean values.

+ Ex:


        const text = 'Hello, world!';
        const startsWithHello = text.startsWith('Hello'); // true
Booleans are fundamental in programming, used for making decisions, controlling loops, and creating conditional behaviors in your code.

### `Operators in depth`:

1. The logical AND operator :

symbol (`&&`)
+ Ex:

        var currentTime = 10;
        console.log(currentTime > 9 && currentTime < 17);

it gives __true__ only if the two statements are true anything else returns __false__

2. Logical OR Operator :
symbol (`||`)
+ Ex:

        var currentTime = 7;
        console.log(currentTime < 9 || currentTime > 17);
it gives __false__ only if the two statements are true anything else returns __true__

3. NOT Operator symbol  :
symbol (`!`)
+ Ex:

        var petHungry = true;
        petHungry = !petHungry; //false because it returns the opposite

4. The modulus operator:
symbol (`%`)
also known as remainder it divides two numbers and gets the remainder between them
+ Ex:

        console.log(22 % 5); // returns 2  22/5 => i got 4 and remainder 2  
        console.log(20 % 5); // returns 0  20/5 => i got 4 and remainder 0
        console.log(14 % 4); // returns 2  14/4 => i got 3 and remainder 2

5. the equality operator:
symbol (`==`)
only checks the two values are equal
+ Ex:

        5 == 5 //true
        5 == 10 //false
        5 == '5' //true
        null == undefined// false
        0 == [] // true

6. the inequality operator:
symbol (`!=`)
checks that both operands are not equal to each other

+ Ex:

        5 != 8 //true
        3 != '3' //false
        4 != 2 //true

7. the Strict equality operator:

symbol (`====`)
it compares the  values and data types of the operands

+ Ex: 

        5 === "5" //false it's not equal as equality because they are different types
        5 === 5 //true

8. the strict inequality operator:

symbol(`!==`)
compares the values and data types of operands if they are not equal
+ Ex:

        5 !== "5" //true

        var a=null,b=" ";
        a !== b;//true

9. the `+` operators with strings and numbers :
   1. Combining two strings using the + operator
        used to join string data type together(concatination operator)
   + Ex :

                console.log("Hello "+"World"); //Hello World
                console.log('Hi'+''+'there'); //Hithere

   2. Combining strings and numbers using the + operator
Used for adding numberic value to string
   + Ex:

                365 + " days" // "365 days"
                12 + " months" // "12 months"
                1 + "2" // "12"

    3. The addition assignment operator, +=
used when one wants to accumulate the values stored in a variable.
    + Ex:

                var overtime = 1;
                overtime += 2;
                overtime += 1;
                overtime += 2;
                overtime += 3;
                console.log(overtime); // 9

    4. The concatenation assignment operator, +=

    + Ex:

                var longString = "";
                longString += "Once";
                longString += " upon";
                longString += " a";
                longString += " time";
                longString += "...";
                console.log(longString); // "Once upon a time..."

    5. Operator precedence and associativity
set of rules that determines which operator should be evaluated first and it has two types of periority left-to right or right-to-left.
   + Ex:

                1 * 2 + 3 // left to right associativity
                var num = 10 // right to left associativity








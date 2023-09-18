## `Functional Programming`
programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. It emphasizes immutability, pure functions, and higher-order functions

functional programming has several use cases for programming :

#### 1. Pure Functions:

function where the output value is determined solely by its input parameters, without observable side effects.
+ Ex:

        // Pure function
        function add(a, b) {
          return a + b; // return is way used so you can use the function in other function or object
        }

>**Use Case** : Pure functions are predictable and can be easily tested, as they don't rely on external data or change any state.

#### 2. Higher-Order Functions:

functions that take other functions as arguments or return them as results. They enable abstraction and composition.
+ Ex:


        // Higher-order function
        const fruits = ['kiwi','mango','apple','pear'];
        function appendIndex(fruit, index) {
            console.log(`${index}. ${fruit}`)
        }
        fruits.forEach(appendIndex);

>**Use Case**: Higher-order functions are powerful for creating reusable and composable code.

#### 3. Recursion:

Functional programming often uses recursion to solve problems by breaking them down into smaller, self-contained subproblems.
+ Ex:

        // Recursive function to calculate factorial
        function factorial(n) {
          if (n === 0) return 1;
          return n * factorial(n - 1);
        }
>**Use Case** : Recursion is a powerful technique for solving problems that naturally exhibit recursive behavior.

#### 4. First-class:

It is often said that functions in JavaScript are “first-class citizens which means that a function in JavaScript is just another value that we can:

- pass to other functions

- save in a variable

- return from other functions

which means that function is just another value 

+ Ex:

        function addTwoNums(a, b) {
            console.log(a + b)
        }

        function randomNum() {
            return Math.floor((Math.random() * 10) + 1);
        }
        function specificNum() { return 42 };

        var useRandom = true;

        var getNumber;

        if(useRandom) {
            getNumber = randomNum
        } else {
            getNumber = specificNum
        }

        addTwoNums(getNumber(), getNumber())

---
## `Scoping`

scoping refers to the rules that determine where variables and constants are accessible within your code

the scoping behavior of variables declared with **let**, **var**, and **const** :

#### 1. var Scoping:

**Function Scope**: Variables declared with var are function-scoped. This means they are accessible throughout the function in which they are defined, but not outside of it.

**Hoisting**: Variables declared with var are hoisted, which means they are moved to the top of their containing function or global scope during the compilation phase. However, their assignments remain in place.
+ Ex:

        function exampleVarScope() {
          if (true) {
            var x = 10;
          }
          console.log(x); // Outputs 10
        }
        exampleVarScope();
        console.log(x); // ReferenceError: x is not defined
>**Use Case**: var is best suited for declaring variables with function-level scope and for cases where hoisting behavior is desired.
#### 2. let Scoping:

**Block Scope**: Variables declared with let are block-scoped, meaning they are accessible within the block (enclosed by curly braces) in which they are defined, including loops, conditionals, and functions.

**Hoisting**: Variables declared with let are hoisted to the top of their block but are not initialized until the actual declaration statement is encountered.
+ Ex:

        function exampleLetScope() {
          if (true) {
            let y = 20;
          }
          console.log(y); // ReferenceError: y is not defined
        }
        exampleLetScope();

>**Use Case**: let is suitable for block-scoped variables and is the preferred choice for most variable declarations in modern JavaScript.
#### 3. const Scoping:

**Block Scope**: Variables declared with const are also block-scoped, just like let.
Immutable Values: Unlike let and var, variables declared with const cannot be reassigned after they are declared. However, for objects and arrays declared with const, their properties and elements can still be modified.
**Hoisting**: Similar to let, const variables are hoisted to the top of their block and are not initialized until the declaration statement.
+ Ex:

        function exampleConstScope() {
          const z = 30;
          z = 40; // Error: Assignment to a constant variable
        }

>**Use Case**: const is suitable for declaring constants and for variables that should not be reassigned. It's also block-scoped like let.

---

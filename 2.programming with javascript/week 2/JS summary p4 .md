## `Bugs and errors`
### Bug 
A bug causes a program to run in an unintended way
A common mistake is forgetting the semicolon at the end of your statement, which can cause unexpected results or even crashing programs entirely but the code still works

+ Ex :

        function addNums (a, b) {
        console.log(a + b);
        }
        addNums ("1", 2); 
        console.log("Still running");

in this ex it outputs **12** because adding a number with a string will concatinate them together while it supposed to output **3**

### Error
An error causes a program to stop running.

errors have many types like (Type error, syntax error, reference error etc.)

##### TypeError 
This type of error occurs when the data type is not correct for that particular operation or variable.
+ Ex:

        let num = 5;
        num.toUpperCase();  // num is not a string

in the code above the uppercase is a funciton for strings and 5 is a number data type

##### SyntaxError
Syntax Errors occur when there are mistakes with your JavaScript code's structure such as missing brackets/parentheses, misspelled keywords, or any other

+ Ex:

        if (x === 10 {  // Missing closing parenthesis
          console.log("x is 10");
        }

##### ReferenceError
these errors occur when you try to reference a variable or function that doesn't exist.
+ Ex:

        console.log(y);  // 'y' is not defined

##### RangeError
Range errors happen when an operation expects a certain numerical range but is provided with a value outside that range
+ Ex:

        let arr = [1, 2, 3];
        arr[5] = 10;  // Index 5 is out of range for the array

>**Use Case** : Range errors often occur when working with arrays, strings, or other data structures

---
## `Try and Catch`
It allows you to try a block of code and catch any errors that might occur during its execution. Here's a conclusion regarding the try...catch statement, along with + Exs, use cases, and detailed explanations:

#### 1. Purpose of try...catch:

The try...catch statement is used to handle exceptions (errors) that may occur during the execution of a block of code.
+ Ex:

        try {
          // Code that might throw an error
        } catch (error) {
          // Handle the error
        }

>**Use Case** : It is primarily used to gracefully handle errors and prevent them from crashing your program.

#### 2. Error Propagation:

When an error occurs within the try block, the control is transferred to the catch block, allowing you to handle the error without terminating the entire script.

+ Ex:

        try {
          let result = 10 / 0; // This will throw a division by zero error
        } catch (error) {
          console.error("An error occurred:", error.message);
        }
        console.log("Script continues to run.");

>**Use Case** : Error propagation ensures that your program can continue running despite encountering errors.

#### 3. Error Object:

The catch block receives an error object that contains information about the error, such as its type and message.

+ Ex:

        try {
          JSON.parse("invalid json"); // This will throw a SyntaxError
        } catch (error) {
          console.error("Error Type:", error.name);
          console.error("Error Message:", error.message);
        }

>**Use Case** : You can access properties of the error object to provide more context or log detailed error messages.

#### 4. Multiple catch Blocks:

You can have multiple catch blocks to handle different types of errors.
+ Ex:

        try {
          // Code that might throw different types of errors
        } catch (error1) {
          // Handle the first type of error
        } catch (error2) {
          // Handle another type of error
        }

>**Use Case** : This allows you to handle various error scenarios differently, improving the precision of error handling.

#### 5. finally Block:

You can also include a finally block after try and catch. The code in the finally block always runs, whether an error occurred or not.

+ Ex:

        try {
          // Code that might throw an error
        } catch (error) {
          // Handle the error
        } finally {
          // Code that always runs
        }

>**Use Case** : The finally block is often used for cleanup tasks like closing files or releasing resources.

**In conclusion**, the try...catch statement is a fundamental tool for managing errors in JavaScript. It provides a structured way to handle exceptions, ensuring that your code can gracefully recover from errors and continue to function as expected. By understanding and effectively using try...catch, you can write more robust and reliable JavaScript applications.

---
## `Undefined, Null and Empty`

distinct concepts that are often used in different contexts. Let's explore each of these concepts in detail, provide + Exs, use cases, and explanations:

#### 1. undefined:

special value in JavaScript that represents the absence of a value. It typically occurs when a variable is declared but not assigned a value or when an object property does not exist.
+ Ex:

        let x; // x is undefined
        let obj = { name: "John" };
        console.log(obj.age); // age property is undefined

**Use Cases:**
- When a variable or property has not been initialized.
- As the default return value of functions that don't explicitly return anything.
- To check if a variable exists or if an object property is defined.
#### 2. null:

value that represents the intentional absence of any object value or pointer. It's often used to signify that a variable or property has no value or is explicitly empty.
+ Ex:

        let y = null;
        let person = { name: "Alice", age: null };
**Use Cases:**
- To explicitly indicate the absence of a value.
- In cases where you want to reset a variable or property to an empty state.
#### 3. "Empty" Values:

context-dependent and can refer to different concepts, such as an empty string, empty array, or empty object.
+ Ex:

        let emptyString = "";
        let emptyArray = [];
        let emptyObject = {};
**Use Cases:**
- Empty String: Used when you need a string with no characters.
- Empty Array: Used when you need an array with no elements.
- Empty Object: Used when you need an object with no properties.


**Comparison and Use Cases:**

- undefined is typically used to represent the absence of a value that hasn't been initialized or is missing.
<br>
- null is often used to explicitly indicate that a variable or property is intentionally empty.
<br>
- "Empty" values (empty strings, arrays, objects) are used when you need data structures with no content.
Here's a comparison of how you might use these concepts:
---





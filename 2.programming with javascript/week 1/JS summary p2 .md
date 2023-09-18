## `If-ELse Statements`
 "Conditional" Statements, which are used to perform different actions based on different conditions
 the if-else has these following condotional statements :
1. if: to specify a block of code to be executed, if a specified condition is true
2. else: to specify a block of code to be executed, if the same condition is false
3. else if: to specify a new condition to test, if the first condition is false

+ Ex :

        var age = 10;
        if (age>=65){
            console.log("You get your income from your pension");
        }
        else if (age>=18){
            console.log("You get an allowance");
        }
        else{
            console.log("The value of the age variable is not numerical")
        }
---
## `Switch-case Statements`
Switch Case statement allows you to execute one case or another depending upon the given expression. It can also have multiple cases and default as well.

+ Ex :

        var day = 'friday';
        switch (day){
            case 'sunday':
                console.log('Do something');
                break;
            case 'Monday':
                console.log('Do something');
                break;
            case 'Tuesday':
                console.log('Do something');
                break;
            case 'Wednesday':
                console.log('Do something');
                break;
            case 'Thuresday':
                console.log('Do something');
                break;
            case 'Friday':
                console.log('holiday bro');
                break;
            case 'saturday':
                console.log('Holiday bro');
                break;
                default:
                    console.log('There is no such day');
        }
---
## `Loops `
1. ##### For Loop:
A for loop is a control flow statement used to execute a block of code repeatedly for a specified number of times. It consists of three parts: initialization, condition, and increment/decrement.

+ Syntax :

        for (let i = 0; i < 5; i++) {
          console.log(i); // Output: 0, 1, 2, 3, 4
        }
In this example, the loop starts with i equal to 0, executes the code block while i is less than 5, and increments i by 1 in each iteration.

2. ##### While Loop:
A while loop repeatedly executes a block of code as long as a specified condition is true. It's useful when the number of iterations isn't known beforehand.

+ Syntax :

        let count = 0;
        while (count < 5) {
          console.log(count); // Output: 0, 1, 2, 3, 4
          count++;
        }
In this example, the loop continues as long as count is less than 5, and count is incremented after each iteration.

3. ##### Nested Loops:
Nested loops involve placing one loop inside another. They're used to work with multi-dimensional data structures or to perform repetitive tasks in a hierarchical manner.

+ Syntax :

        for (let i = 1; i <= 3; i++) {
          for (let j = 1; j <= 3; j++) {
            console.log(`i: ${i}, j: ${j}`);
          }
        }
In this example, the outer loop iterates through i from 1 to 3, and for each i, the inner loop iterates through j from 1 to 3. This results in 9 iterations with combinations of i and j.

Summary:

- for loops are commonly used when you know the number of iterations in advance.
- while loops are suitable for situations where you're uncertain about the number of iterations.
- Nested loops allow you to execute one loop inside another and are used for more complex scenarios, like working with matrices or grids.
> __Remember__ : to ensure that the loop's conditions eventually become false, or you risk creating an infinite loop. Additionally, each type of loop has its advantages and  use >cases, so choose the one that best fits the problem you're solving.
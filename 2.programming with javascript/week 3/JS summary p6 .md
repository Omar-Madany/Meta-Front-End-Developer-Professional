## `Object Oriented Programming(OOP)`

In this reading, you'll learn about the benefits of object-oriented programming (OOP) and the OOP principles

#### The Benefits of OOP
There are many benefits to using the object-oriented programming (OOP) paradigm.

OOP helps developers to mimic the relationship between objects in the real world.

- Allows you to write modular code,

- Makes your code more flexible and

- Makes your code reusable.

#### The basic OOP code 

you can create an oop code by two ways :

###### 1. Class Declaration (ES6)

modern way of javascript to make an OOP code it consists of :

1. Class (the main)
``````javascript
class Person {  /* ...class code here... */ }

``````
2. Constructor
used to initialize the object property and set up the initial state for example :
``````js
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
``````
and also constructor is the main purpose to create an instance of the class using two ways :
1. Object.create 

``````js
class Person {
  constructor() {
  }
}
let john = Object.create(person)
``````
2. new operator

``````js
class Person{
    constructor(){
    }
}
const john=new person(); //this will call the constructor function inside the class
``````
3. Methods 
functions of the classes describe the behavior or actions that objects created from the class can perform for example :
``````js
class Person {
    constructor(name){this.nom =name}
    sayHi(){
        console.log(`hi ${nom}`);
        }
        }
        //now we have a method in our class so we need to use that method as below:
        var peter = new Person();//here we are creating an instance from the class
        peter.sayHi();    //calling the method on the created instance
``````

#### The Principles of OOP

The four fundamental OOP principles are inheritance, encapsulation, abstraction and polymorphism 

###### 1. Inheritance

the way that you can make or inherite a class from other is by using **extend** keyword for example :

``````js
//parent class
class Animal {
    constructor (typeOfAnimal) {
        this.typeOfAnimal = typeOfAnimal;}
}
//child class
class Cat extends Animal {}
``````
###### 2. Encapsulation
In the simplest terms, encapsulation has to do with making a code implementation "hidden" from other users, in the sense that they don't have to know how my code works in order to "consume" the code.

For example, when I run the following code:

``````js
"abc".toUpperCase();
``````

I don't really need to worry or even waste time thinking about how the toUpperCase() method works. All I want is to use it, since I know it's available to me. 

###### 3. Abstraction
Abstraction is all about writing code in a way that will make it more generalized.

The concepts of encapsulation and abstraction are often misunderstood because their differences can feel blurry.

It helps to think of it in the following terms: 

- An abstraction is about extracting the concept of what you're trying to do, rather than dealing with a specific manifestation of that concept. 

- Encapsulation is about you not having access to, or not being concerned with, how some implementation works internally.

While both the encapsulation and abstraction are important concepts in OOP, it requires more experience with programming in general to really delve into this topic.

###### 4. polymorophism
The term "polymorphism" means "many forms," and it refers to the ability to use objects of different types in a uniform way. In OOP, polymorphism is closely related to inheritance and method overriding.

in nutshell that you can use one method to do many tasks in different classes and objects for example
``````js
const bicycle = {
    bell: function() {
        return "Ring, ring! Watch out, please!"
    }
}
const door = {
    bell: function() {
        return "Ring, ring! Come here, please!"
    }
}

``````
they both sharing the same method which is bell so instead of that we can use this function :
``````js
function ringTheBell(thing) {
    console.log(thing.bell())
}
``````
---
## `Default Parameters`
Introduced in ECMAScript 6 (ES6), default parameters allow you to specify default values for function parameters directly in the function declaration.
They are used to provide a fallback value for a parameter if the caller doesn't pass a value or passes undefined

Default parameters are defined within the function's parameter list using the = operator

Default parameters are evaluated only when the function is called and the parameter is not provided or is undefined.

Example of Default Parameters:


        function greet(name = "Guest") {
          console.log(`Hello, ${name}!`);
        }

        greet();         // Outputs: Hello, Guest!
        greet("Alice");  // Outputs: Hello, Alice!
        Default Values:

"Default values" is a more general term and can refer to any value that is used as a default when no other value is provided. This concept is not limited to function parameters.
Default values can be used in various contexts, such as when initializing variables or properties with fallback values.

Example of Default Values (Not Specific to Parameters):

        // Default value for a variable
        let username = "Guest";

        // Default value for an object property
        const config = {
          apiUrl: "https://example.com/api",
          timeout: 5000,
        };
In summary, "default parameters" specifically refer to default values assigned to function parameters. They provide a convenient way to ensure that a function has some value to work with even if the caller doesn't explicitly provide one. "Default values" are a broader concept that can apply to various situations where you want to define a fallback or initial value.


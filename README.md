# Sprint Challenge - JavaScript Fundamentals

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in project. This Sprint explored JavaScript Fundamentals. During this Sprint, you studied array methods, this keyword, prototypes, and class syntax. In your challenge this week, you will demonstrate proficiency by completing a survey of JavaScript problems.

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the sprint challenge. 

_You have **three hours** to complete this challenge. Plan your time accordingly._


## Introduction

The index.js file contains all of your challenges. Please review it in full before answering the questions. If you complete the stretch goals please leave them in your file but commented out so that they do not affect the MVP tasks 

In meeting the minimum viable product (MVP) specifications listed below, you should have all tests passing. You can console.log to check your work and ensure you are submitting the correct results 

### Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your team lead as the evaluate your solution.

## Interview Questions
### (please edit this file and write your answer below each question. In addition, you may also review these questions with your mentor)
Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read.

1. Briefly compare and contrast `.forEach` & `.map` (2-3 sentences max)

    Both are array methods that execute a provided function on every element of an array. .forEach will mutate the original array and a return statement is optional (the return values will be discarded) whereas .map will create a new array and a return statement is required. .map is best for when you want to change your data and .forEach may be best when you want to do something with your data (but not change it) - eg saving your data.

2. Explain the difference between a callback and a higher order function.

    A higher order function receives other functions as arguments and a callback function is passed into a higher order function as an argument. 
    For example: 
    
    function higherOrderFunction(callbackFunction){
        return callbackFunction();
    }
    higherOrderFunction(callbackFunction1);

    When higherOrderFunction is invoked on line 42, callbackFunction1 will be passed into the function as an argument and then is called (inside of higherOrderFunction) on line 40. higherOrderFunction would return the value of callbackFunction1.

3. What is closure?

    A closure is the "one way street" that is created when nested a function inside of another function. The function inside the outer function has a global lexical scope, meaning that it has access to all variables defined in its code block (between the curly braces), in the outer function's code block, and in the global scope. The outer function, on the other hand, does not have access to variables declared inside the scope of the inner function. The outer function's lexical scope is defined to its code block and the global scope.

4. Describe the four rules of the 'this' keyword.

    1. Window binding - when "this" has not been given context (ie it is used in the global scope, so not inside an object that is itself inside of the window object, the value of "this" will be the window Object.

    2. Implicit binding - whenever a function is called by using a preceding dot ( eg myObj.function() ), the value of "this" will be the object to the left of the dot. Implicit binding applies specifically to objects with methods.

    3. New binding - When using a constructor function, "this" refers to the new instance of the object that is created by the constructor function. eg if you had a new constructor function: function DogMaker(prop){
      this.name = prop.name,
      this.breed = prop.breed
    }
    and you initialize a new object by: 
    const buddy = new DogMaker({
      name = 'Buddy',
      breed = 'Basset Hound'
    });
    then "this" (in lines 55 and 56) will have the value of the new object that is created using the constructor function (in this example: buddy). So the constructor function would assign the value of this.name (which in this initialization can be thought of as equivalent to buddy.name) to the value of the name key of the object getting passed into the constructor function via the placeholder value "prop".

    4. Explicit binding - You can use explicit binding to explicitly define the value of "this". For example, by using .call(), .apply(), or .bind(), you can override implicit binding and assign the value of this to the arguments that are getting passed into the method. .call() will immediately call the function and pass in arguments one by one, .apply() will immediately call the function and pass in arguments as an array, and .bind() will return a new function that can be invoked later. 

5. Why do we need super() in an extended class?

    super() passes the keys and values (including methods) from the parent down to the child. super() works together with extends to figure out where to grab keys and values from, and then super() passes those on to the child. Together with extends, super() does what Parent.call(this, attributes) (inherit the keys) and Child.prototype = Object.create(Parent.prototype) (inherit the methods) do when using a constructor to function to create a child class without using classes.

You are expected to be able to answer questions in these areas. Your responses contribute to your Sprint Challenge grade. 

## Instructions

### Task 1: Project Set Up

Follow these steps to set up your project:

1. Fork the repo
2. Clone your forked version of the repo
3. cd into your repo and create a branch with your first and last name
NOTE: Tests will run for the JavaScript portion of this challenge only
4. open the terminal in your vs code and type `npm install`
5. next type `npm run test:watch` in your terminal
6. Complete your work making regular commits, once you have all your tests passing and you are ready to submit your work please see canvas for instructions on how to submit

### Task 2: Project Requirements

Your finished project must include all of the following requirements

#### Task A: Closure

This challenge takes a look at closures as well as scope. 
* [ ] Find this challenge in the index.js file. Read the instructions carefully!

#### Task B: Objects and Arrays

Test your knowledge of advanced array methods and callbacks.
* [ ] Find this challenge in the index.js file. Read the instructions carefully!

#### Task C: Prototypes

Create constructors, bind methods, and create cuboids in this prototypes challenge.
* [ ] Find this challenge in the index.js file. Read the instructions carefully!

#### Task D: Classes

Once you have completed the prototypes challenge, it's time to convert all your hard work into classes.
* Find this challenge in the index.js file. Read the instructions carefully!

In your solutions, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

### Task 3: Stretch Goals 

There are a few stretch problems found throughout the files, don't work on them until you are finished with MVP requirements! Please remember to comment out your stretch goals before you submit 

## Submission format

See Canvas for submission instructions 


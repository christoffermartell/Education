<!doctype html>
<html>
	<head>
    <title>JavaScript - Functions</title>
    <meta charset="utf-8">
    <meta name="robots" content="noindex, nofollow">
		<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">

		<link rel="stylesheet" href="../../libs/reveal/css/reset.css">
		<link rel="stylesheet" href="../../libs/reveal/css/reveal.css">
		<link rel="stylesheet" href="../../libs/reveal/css/theme/softhouse.css">

		<link rel="stylesheet" href="../../libs/bootstrap/css/bootstrap.min.css">
		<link rel="stylesheet" href="../../style.css">

		<script src="../../libs/jquery/jquery.min.js"></script>
		<script src="../../libs/bootstrap/js/bootstrap.min.js"></script>


		<!-- Theme used for syntax highlighting of code -->
		<link rel="stylesheet" href="../../libs/reveal/lib/css/monokai.css">
	</head>
	<body>
		<nav class="navbar navbar-expand-lg  navbar-dark bg-dark fixed-top shadow-lg">
			<a class="navbar-brand" href="https://www.softhouse.se">
				<?xml version="1.0" encoding="utf-8"?>
				<!-- Generator: Adobe Illustrator 22.1.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->
				<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
					viewBox="0 0 928 179" style="enable-background:new 0 0 928 179;" xml:space="preserve">
				<style type="text/css">
					.st0{fill:#FFFFFF;}
				</style>
				<g>
					<path class="st0" d="M795,121.4c-9.5,4.3-6.3,24.8-15.8,31.6c-5.3,3.8-31,4-34.3-3.8c-4.7-11.1,30.2-28.8,23.5-38.9
						c-8.6-12.9-58.5-8.8-61.6-18c-1-3.1,7-17.5,17.7-18.8c11.8-1.9,31.6,19.9,48.2,19.4c32.2-1.1,34.9-51.8,58.5-58
						c20.7-5.4,37.6-1.6,38.8,7.3c2.2,17.3-59.7,45.1-55.8,59.8c4.9,18.6,74.6,26.4,73.8,41.5c-0.4,7.2-13.7,12.5-25.1,9.6
						C840.6,147.4,818.1,111,795,121.4 M866.5,166.7c20.8,6.4,53.4,1.7,54.2-13.4c1.5-30.6-93.3-36.1-99.1-53
						c-3.8-11.2,85.4-49.2,83.1-73.3c-1.4-15.1-33.7-18-62.2-12.1C787.6,26,807.3,84,772.8,86.7c-14.9,1.2-32.8-26.1-54.2-26.1
						c-13.9,0-33,25.6-30.3,33.2c5.8,16.9,63.6,6.4,73.2,20.1c5.8,8.2-36,26.9-27.8,45.2c4.6,10.2,40.9,14.6,52.1,5
						c9.3-7.9,4.9-34.5,12.1-37.7C814.7,119,839.5,158.4,866.5,166.7"/>
					<path class="st0" d="M62.8,101.3H21.3v9.8h30.5c9.3,0,12.2,2.2,12.2,11v6.4c0,8.7-2.9,11-12.2,11H11v-8.7h42.7l0-10.7H23.3
						c-9.2,0-12.3-2.2-12.3-11v-5.1c0-8.8,3.1-11,12.3-11h39.4V101.3z"/>
					<path class="st0" d="M571.8,101.3h-41.4v9.8h30.5c9.3,0,12.2,2.2,12.2,11v6.4c0,8.7-2.9,11-12.2,11H520v-8.7h42.7v-10.7h-30.4
						c-9.2,0-12.3-2.2-12.3-11v-5.1c0-8.8,3.1-11,12.3-11h39.4V101.3z"/>
					<path class="st0" d="M81.5,103.9v24.5c0,8.8,2.9,11,12.2,11H130c9.2,0,12.2-2.2,12.2-11v-24.5c0-8.9-3-11-12.2-11H93.7
						C84.5,92.9,81.5,95,81.5,103.9 M93,101.5h37.9v29H93V101.5z"/>
				</g>
				<polygon class="st0" points="159.8,92.9 209.3,92.9 209.3,101.3 171.3,101.3 171.3,113.4 197.2,113.4 197.2,122.1 171.3,122.1
					171.3,139.5 159.8,139.5 "/>
				<polygon class="st0" points="256.5,139.5 245.1,139.5 245.1,101.3 222.6,101.3 222.6,92.9 279.3,92.9 279.3,101.3 256.5,101.3 "/>
				<polygon class="st0" points="292.5,92.9 304,92.9 304,110.6 339.7,110.6 339.7,92.9 351.2,92.9 351.2,139.5 339.7,139.5
					339.7,119.9 304,119.9 304,139.5 292.5,139.5 "/>
				<g>
					<path class="st0" d="M368.6,103.9v24.5c0,8.8,2.9,11,12.2,11h36.3c9.2,0,12.2-2.2,12.2-11v-24.5c0-8.9-3-11-12.2-11h-36.3
						C371.6,92.9,368.6,95,368.6,103.9 M380.1,101.5h37.8v29h-37.8V101.5z"/>
					<path class="st0" d="M458.3,130.8H491V92.9h11.5v35.5c0,8.7-3,11-12.3,11h-31.1c-9.3,0-12.2-2.3-12.2-11V92.9h11.4V130.8z"/>
				</g>
				<polygon class="st0" points="590.5,92.9 640.9,92.9 640.9,101.2 602.1,101.2 602.1,111.3 627.1,111.3 627.1,119.4 602.1,119.4
					602.1,130.8 641.5,130.8 641.5,139.5 590.5,139.5 "/>
				</svg>
			</a>
			<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>

			<div class="collapse navbar-collapse" id="navbarSupportedContent">
				<ul class="navbar-nav m-auto">
					<script src="../../navigation.js"></script>
				</ul>
			</div>
    </nav>
    
		<div class="reveal">
			<div class="slides">

### 5. JavaScript</h3>
##### Functions</h5>

---

#### What is a function?</h4>
          <ul>
            <li>A function is a named section of a program that performs a specific task. In this sense, a function is a type of procedure or routine.</li>
            <li>Functions are one of the fundamental building blocks in JavaScript.</li>
            <li>“A function is a process which takes some input, called arguments, and produces some output called a return value." - <a href="https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976">Eric Elliot</a></li>
          </ul>

---


#### Functions can be used for:</h4>
          <ul>
            <li>Given inputs it produces some output.</li>
            <li>Perform a sequence of steps. The sequence is known as a procedure.</li>
            <li>Functions can communicate with other parts of the system, such as the screen, storage, system logs, or network.</li>
          </ul>

---


#### JavaScript Functions and making a recipe analogy</h4>
          <ul>
            <li>You start with a specific set of ingredients.</li>
            <li>You perform a specific procedure using those ingredients.</li>
            <li>You will get a reliable product at the end.</li>
            <li>A function is also a reusable recipe that performs the same set of actions over and over again on a set of ingredients.</li>
            <li><a href="https://www.codeanalogies.com/javascript-functions-explained">CodeAnalogies ref</a></li>
          </ul>

---


####  JavaScript Functions and making a recipe analogy
            ```JavaScript
            function makeSandwich(lettuce, cheese, bread) {
              var sandwich = lettuce + cheese + bread;
              return sandwich;
            }
            ```
* Every time we want to make a sandwich we can call the function with the ingredients we want and it will return different sandwiches depending on ingredients.



---


####  Basic function
            ```JavaScript
            function sayHello() {
              alert('hello world!');
            };
            ```


---


####  Invoking/calling a function

* When a function is invoked the code inside it will run.

            ```JavaScript
            function sayHello() {
              alert('hello world!')
            };

            // invoking/calling the function
            sayHello();
            ```


---


####  Parameter

            A parameter is a variable in a function definition.

            ```JavaScript
            // word is the parameter
            function saySomething(word) {
              console.log(word);
            };
            ```


---


####  Argument

            When a function is called, the **arguments** are the data you pass into the method as **parameters**.

            ```JavaScript
            // word is the parameter
            function saySomething(word) {
              console.log(word);
            };

            // 'hello world' is the argument
            saySomething('hello world');
            ```


---

        

####  Arguments object

* Arguments is an Array-like object accessible inside functions.
* It contains the values of the arguments passed to that function.

            ```JavaScript
            function saySomething() {
              console.log(arguments);  // {0: 'hello world', 1: 15}
              console.log(arguments[0]);  // 'hello world'
            };

            saySomething('hello world', 15);
            ```


---


####  Invoking/calling a function
            ```JavaScript
            function addValues(val1, val2) {
              console.log(val1 + val2); // 11
            };

            // invoking/calling the function
            addValues(4,7);
            ```


---


####  Get save value returned from function
            ```JavaScript
            function myFunc(myValue) {
              return myValue;
            }

            var value = myFunc(5);
            var value2 = myFunc(10);
            console.log(value);  //5
            console.log(value2); //10
            ```


---


####  Function expression

* An expression is any valid unit of code that resolves to a value.
* Function declarations load before any code is executed while Function expressions load only when the interpreter reaches that line of code.
* Function declarations are hoisted but function expressions are not.

            ```JavaScript
            area(5,7);  // 35

            function area(width, height) {
              console.log(width * height);
            }
            ```

            ```JavaScript
            area(5,7); // area is not a function

            var area = function(width, height) {
              console.log(width * height);
            }
            ```


---


####  Function calling a function

            ```JavaScript
            function sayWord(word) {
              var allWords = word + getWord();
              console.log(allWords);
            }

            function getWord() {
              return ' world!';
            }

            sayWord('hello');
            ```


---


####  Function calling a function

            ```JavaScript
            function addNSub(val1, val2) {
              var added = val1 + val2;

              return sub(added);
            }

            function sub(val) {
              return val - 2;
            }

            var result = add(14, 28);
            console.log(result);
            ```


---


####  Arrow functions
            
* We will look closer on arrow functions later on in the course.
* However you will run into the online before that.
* Arrow functions was introduced with ES6.


---


####  Arrow functions
            ```JavaScript
            // Ordinary function
            const myFunc = function(param){
              return param;
            }

            // Same function as above but as an arrow function
            const myFunc = (param) => {
              return param;
            }

            // Same function as above but with less code (instant return)
            const myFunc = (param) => param;

            // Same function as above but with even less code (instant return)
            const myFunc = param => param;

            var myVal = myFunc(12);
            console.log(myVal);
            ```


---


####  Descriptive Blocks - Commenting Functions

            ```JavaScript
              /**
    * @desc opens a modal window to display a message
    * @param string msg - the message to be displayed
    * @return bool - success or failure
  */
              function modalPopup(msg) {
                return true;
              }
            ```


---


####  Indentations in JavaScript

* There is no "right" way of doing it. Most of the time you and your team or others involved in the project agree on certain rules.
* Most important is to: **Be consistent**
* General rules:
  * Avoid long lines
  * Use tabs/spaces to clarify where stuff belongs

            <a href="https://courses.cs.washington.edu/courses/cse154/17au/styleguide/js/spacing-indentation-js.html">JavaScript Unofficial Style Guide</a>


---
        

### <a href="https://github.com/SofthouseVxo/Education" target="_blank">Github examples!</a></h3>

---

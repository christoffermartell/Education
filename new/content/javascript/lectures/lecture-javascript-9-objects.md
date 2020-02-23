<!doctype html>
<html>
	<head>
    <title>JavaScript - Objects</title>
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

### 9. JavaScript</h3>
##### Objects</h5>

---


#### What is an object?</h4>
          <ul>
            <li>A product that can do things and contains information about its current state.</li>
            <li>Each Object has a purpose and a task.</li>
            <li>Real world examples could be  a <b>lamp</b> or a <b>human</b>.</li>
          </ul>

---


#### <i>In JavaScript, objects are king. If you understand objects, you understand JavaScript.</i> - W3Schools</h4>

---


#### Objects can have <u>Properties</u> and <u>Methods</u></h4>

---

#### Properties</h4>
          <ul>
            <li>A property is a variable connected to a specific object.</li>
            <li>A property contains information about the object.</li>
          </ul>

---


#### Methods</h4>
          <ul>
            <li>A method is a function connected to a specific object.</li>
            <li>Methods are actions that can be performed on objects.</li>
            <li>Methods are used to give an object functionality.</li>
          </ul>

---


#### Real world properties & methods</h4>
          <ul>
            <li>What properties does a human have?</li>
            <li>What methods does a human have?</li>
          </ul>

---


#### Exercise</h4>
          <ul>
            <li>Pair up with the one next to you.</li>
            <li>Pick 2 objects from the real world, could be anything (plants, people, vehicles, furniture).</li>
            <li>Identify properties and methods of all these.</li>
          </ul>

---


####  Objects in JavaScript

* An object consists of a group of values(properties, methods) compiled under one name.
* These are name Value pairs.
* Objects are like variables. But objects can contain many values.

            ```JavaScript
            let obj = { 
              color: 'red', // color = name, red = value
              run: function(){
                console.log('running');
              }
            };
            ```


---


####  Creating an object using an object literal

            ```JavaScript
            let car = { color: 'red' };
            ```


---


####  Creating an object using the **new** keyword

            ```JavaScript
            let car = new Object();
            
            car.color = "red";
            ```


---


####  Accessing an object

            ```JavaScript
            let car = { color: 'red' };

            console.log(car.color); // red "dot notation"
            console.log(car['color']); // red "bracket notation"
            ```


---


          #### Objects - Methods

          * When a function is tied to an object it is called a **Method**.
          
          ```JavaScript
          let person = {
            firstName: 'John',
            lastName: 'Doe',
            // getFullName is a method
            getFullName : function() {
              return this.firstName + " " + this.lastName;
            }
          };
          ```


---


          #### Objects - Calling Methods
          
          ```JavaScript
          let person = {
            firstName: 'John',
            lastName: 'Doe',
            // getFullName is a method
            getFullName : function() {
              return this.firstName + " " + this.lastName;
            }
          };

          let name = person.getFullName(); // John Doe
          let name2 = person['getFullName'](); // John Doe
          ```


---


          #### Dot notation vs bracket notation
          
          ```JavaScript
          const variable = 'name';
          
          const obj = {
            name: 'value'
          };
          
          obj[variable]; // 'value'
          obj.variable; // undefined
          ```


---


          #### <u>Dot</u> notation vs bracket notation
          
          ```JavaScript
          obj.123;        // SyntaxError
          obj.123name;    // SyntaxError
          obj.name123;    // works
          obj.$name;      // SyntaxError
          obj.'name-123'; // SyntaxError
          obj.NAME;       // works
          obj.name;       // works
          ```


---



          #### Dot notation vs <u>bracket</u> notation
          
          ```JavaScript
            obj['123'];        // works
            obj['123value'];     // works
            obj['value123'];     // works
            obj['$value'];       // works
            obj['value'];        // works 
            obj['value value'];  // works 
          ```


---


          #### Dot notation vs <u>bracket</u> notation
          
          ```JavaScript
          let myObj = {};

          for (var i = 0; i < 10; i++) {
            myObj['key' + i] = i;
          }

          console.log(myObj);
          ```


---


####  Adding to an object after declaration

* If the property does not exist from before it will be added.

            ```JavaScript
              let bike = {
                color: 'blue'
              }

              bike.hasFrontLight = true; // { color: 'blue', hasFrontLight: true }
              bike['hasBackLight'] = false; // { color: 'blue', hasFrontLight: true, hasBackLight: false }

            ```


---


####  Removing from an object

* delete will remove the property or method from the object.

            ```JavaScript
              let bike = {
                color: 'blue',
                hasFrontLight:true
              }

              delete bike.hasFrontLight; // { color: 'blue'}
            ```


---


####  Mutating JavaScript Objects
            
* An immutable value is one that, once created, can never be changed.
* Objects are mutable.
* They are also addressed by reference, not by value.

```JavaScript
let bike = { color: 'blue' };

bike.color = 'red';

console.log(bike.color); // red
```


---


          #### Objects - addressed by reference, not by value
          
          ```JavaScript
          let car = { color: 'red', wheels: 4};

          let x = car;  // This will not create a copy of car.
          
          // The object x is not a copy of car. It is car. Both x and car are the same object.
          
          // Any changes to x will also change car, because x and car are the same object.
          
          x.wheels = 8; // This will change both x.wheels and car.wheels 
          
          console.log(x.wheels) // 8
          console.log(car.wheels) // 8
          ```


---


####  Object in an object

            ```JavaScript
            let bike = {
              color: 'blue',
              pedal: function(){
                console.log('I pedal')
              },
              frontLight: {
                color: 'yellow'
              }
            }

            let hasFrontLight = bike.frontLight.color; // yellow
            ```


---


####  Creating many objects: constructor notation

* The **new** keyword followed by a call to a function creates a new Object.
* For every time the **new** keyword is used a new instance of the objects is created.

            ```JavaScript
            function Person(name){
              this.name = name;
            };
            
            let user1 = new Person('John Doe'); // Person { name: 'John Doe' }
            let user2 = new Person('Jane Doe'); // Person { name: 'Jane Doe' }
            ```


---


#### In JavaScript, almost "everything" is an object.</h4>

          <ul>
            <li><b>Booleans, Numbers & Strings</b> can be objects(if they are defined with the **new** keyword)</li>
            <li><b>Dates</b> - are always objects</li>
            <li><b>Maths</b> - are always objects</li>
            <li><b>Regular expressions</b> - are always objects</li>
            <li><b>Arrays</b> - are always objects</li>
            <li><b>Functions</b> - are always objects</li>
            <li><b>Objects</b> - are always objects</li>
          </ul>
          
          <p>All JavaScript values, except primitives, are objects.</p>

---


#### Functions are Objects</h4>
          <ul>
            <li>Functions are a special kind of Object.</li>
            <li>You can attach primitives and other functions.</li>
            <li>Functions have a "code" property which is the code that runs when the function is invoked.</li>
          </ul>

---


          #### Functions are Objects
          
          * Example just to show that it works.

          ```JavaScript
          let greet = function(){
            console.log('Hi!');
          }

          greet.language = 'swedish';

          console.log(greet.language); // swedish
          ```


---


          #### Arrays are a special type of Objects
          
          ```JavaScript
          let users = ['Jane', 'John'];

          // forEach is a method of the Array object
          users.forEach(function(user) {
            console.log(users.length);  // length is a property
          });
          ```


---


          #### Iterating over Objects
          
          * The for...in statement iterates over all non-Symbol, enumerable properties of an object.

          ```JavaScript
          let string1 = "";
          let object1 = {a: 1, b: 2, c: 3};
          
          for (let property1 in object1) {
            string1 += object1[property1];
          }
          
          console.log(string1);  // "123"
          ```

          [MDN reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)


---


### <a href="https://github.com/SofthouseVxo/Education" target="_blank">Github examples!</a></h3>

---

      </div>
    </div>

		<script src="../../libs/reveal/js/reveal.js"></script>
		<script src="../../initialize.js"></script>
	</body>
</html>
#Interview Prep

(Partially from https://github.com/h5bp/Front-end-Developer-Interview-Questions)

Go through all of the following questions and think about how you would respond to each. You should be able to answer many of the questions from memory, but you may have to research a few of them.

**Copy this md file to your homework folder and add a short answer under each item.** You should try to be as concise as possible, and list any handy resources you used to answer the question. This will be useful for studying for interviews after class.

## General Questions

* What did you learn yesterday/this week?
* What excites or interests you about coding?
    What excites me the most about coding is the idea of inventing something that did not exist before and seeing it perform complex tasks.
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
    I always plan for scalability. All major inventions in tech went viral. If you cannot scale your creation then problems ensue.
* Talk about your preferred development environment.
    I am big on keyboard shortcuts and highlighting. That may be an obvious one in the trade. However, combine this with instant-feedback tools such as browser-sync and development can happen very fast.
* Which version control systems are you familiar with?
    I am most familiar with Git/
* Can you describe your workflow when you create a web page?
    There are two major approaches to this. If I am trying a new technology, my main goal is to prototype a working model first. If I am not using a new technology, my design background tells me to flesh out a wireframe, a mood board and some illustrations. With the design out of the way, along with major technical hurtles, it becomes easy to produce or reproduce a page. The coding aspect becomes freeform and works well with major edits / modificaitons.
* If you have 5 different stylesheets, how would you best integrate them into the site?
    I will have to assume that all 5 stylesheets are loaded on one page. If this was the case, I would have to pay close attention to the css specificity of each element. Alongside with modifying the specificity on the css-side if possible.
* Can you describe the difference between progressive enhancement and graceful degradation?
* Describe how you would create a simple slideshow page, without any frameworks (HTML/CSS/JS only).
    Making this as simple as possible, I would do the following:
    Each image would be loaded into a div at 100% width of the screen. 
* If you could master one technology this year, what would it be?
    If Javascript was not a contender, I would choose A-Frame without a second thought. A-Frame allows making 3D VR apps with ease for incoming newbies, but has the complexity for more advanced topics such as D3 graphs and games.
* Explain the importance of standards and standards bodies.

## HTML Questions

* What does a `doctype` do?
    A doctype is a declaration for which kind of format the file is. HTML, XML, Strict, Transitional are all examples of different doctypes.
* What's the difference between HTML and XHTML?
    HTML is the traditional web format while XHTML is for pages that are both XML (extensible) conforming and traditional.
* What are `data-` attributes good for?
    the data- attributes allow developers to store information inside individual html elements on the page. They may be used at later points for a variety of reasons.
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
    SessionStorage & localstorage are relatively new and may not be supported on older browsers.
    Both are the same with exception to sessionstorage only persisting for the current session. All data must be text and multiple key-value pairs can be used.

    Cookies are similar but has security advantages such as being hidden from locally-running javascript to prevent tampering.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
    Not everyone has blazing fast internet. And not all sources load perfectly on time. So while the page is loading, you want the user to see a fully, properly-skinned site. However the user can wait for the javascript and may not even notice the javascript is still loading while they begin their experience on the site.

## CSS Questions

* What is the difference between classes and IDs in CSS?
    There can only be one selected ID on a page, while there is no limit to the number of classes used.
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
    A float is an element taken out of the normal flow of the page and positioned to the left, right, top or bottom of the viewport.
* Describe z-index and how stacking context is formed.
    All elements start with a z-index of zero. If two elements overlap and have the same z-index, the later loaded element is on top. However, the higher the number, the more on top an element will be.
* Have you ever used a grid system, and if so, what do you prefer?
    I prefer the rule of thirds. On a full-screen website, dividing a website into 1/3,1/3,1/3 or 1/3,2/3 looks very pleasing to the eye.
* Have you used or implemented media queries or mobile specific layouts/CSS?
    I have used media queries on a normal bases. When creating sites, I typically shrink the screen during the creating process to see when the page breaks down and then create a media-query to fix it.
* How do you optimize your webpages for print?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
    A brower matches elements based on specificity. The more specific you isolate and choose a specific element, the more likely that element is to override all other styles on the page. 'body' will set all styles on the page until 'body div' comes along. Even then, 'body div .template' will override that.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
    By setting this and adjusting the width and padding of elements, the total width won't change. This is important if you want to play with layouts and not having to worry about child elements modifying the parents.
* List as many values for the display property that you can remember.
    display: flex, inline, inline-block, list-item, none, table, table-row, table-cell
* What's the difference between inline and inline-block?
    The difference is clear when applied to an element. Some elements, such as divs, are always blocks. Other elements such as spans, are not block level elements. So a span would be applied to inline, while inline-block would be used on elements such as divs.
* What's the difference between a relative, fixed, absolute and statically positioned element?
    Static is default.
    Absolute follows the viewport.
    Relative is like static, but in relation to the parent.
    Fixed is like Absolute but starting from 0,0. Meaning it does not follow the viewport.
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
    A brower matches elements based on specificity. The more specific you isolate and choose a specific element, the more likely that element is to override all other styles on the page. 'body' will set all styles on the page until 'body div' comes along. Even then, 'body div .template' will override that.
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
    I have started using Flexbox on a normal bases due to it's extreme ease of use to center elements virtically or horizontally. Something that is typically a challange.
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
    I have worked with retina graphics. To make an element render as retina, use an image that is double the resolution that you need, set the img dimensions to the normal dimensions that you need, but link to the image that is 2x the resolution. Becuase the image is larger, the image will is scaled down. However on a retina screen, there is a physical pixel for every pixel in the image. The image renders perfectly.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
    The lack of control over CSS animations. The lack of triggers and the lack of being able to change the animation dynamically.

## JS Questions

* Explain event delegation
    Instead of binding an event listener to many elements, you can bind a single listener to a parent, and watch for which child is involved in the event.
* Explain how `this` works in JavaScript
    This means nothing by itself. 'this' refers to how you call a function. If you call a function and pass in an object, this will be that object. In instantiated objects, unless otherwise noted, this rerers to that particular instance.
* Explain how prototypal inheritance works
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
    Ternary means three. In a ternary expression, there are three parts: the expression, when true do, and when false do
* What's the difference between a variable that is: `null`, `undefined` or `undeclared`?
    null = nothing, undefined means the object itself lacks defenition in the code, while undeclared lacks declaration.
  * How would you go about checking for any of these states?
    Performing .prop or 'typeof' in javascript will output the property of the object
* What is a closure, and how/why would you use one?
* What's a typical use case for anonymous functions?
    One-off functions that do not need a name as they will not be used again. Typically when you pass a function into another function.
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?
    apply calls a function with an array (of objects) passed into it. Call's list of objects passed into it is diliminated by commas.
* Explain `Function.prototype.bind`.
* What's the difference between feature detection, feature inference, and using the User Agent string?
* Explain AJAX in as much detail as possible.
    Ajax is asyncronous. This means that JS will not stop and wait for the function to complete. Instead a callback function is declared inside to run when the function has complete. Ajax is typically used to aquire data using RESTful routing.
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
    Hoising is the act of making a variable global due to it's declaration being incomplete. Performing 'myvar' instead of 'var myvar' will hoise the variable to global as the JS interpreter cannot determine where scope should be applied.
* Describe event bubbling.
    Lets assume a element on a page has an event listener on it. So does it's parent and grandparent. When clicking on that element, the element itself runs it's callback. The parent's callback also runs. As well as the grandparents. The event propogates upwards on the DOM tree until the top is reached and will execute every event along the way.
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
    It is not a good idea because these changes occur globally throughout not just your application, but if other scripts are also loaded, amongst them as well. Potentially breaking functionality.
* What is the difference between `==` and `===`?
    triple equals is strict equals. This means both the result and the type must match. 3 == '3' : true, 3 === '3' : false
* Explain the same-origin policy with regards to JavaScript.
    The same origin policy states that scripts must run from the same site and protocol. Changing ports, http to https or a different site will be blocked. This security mechanism protects against malicious scripts.
* What is the extent of your experience with Promises and/or their polyfills?
    I have used promises in databases quiet often. Their use is unmeasurable in their use in databases.
* What are the pros and cons of using Promises instead of callbacks?
    They are mostly the same at the end of the day with one key difference. Promises are composible, meaning you can chain them together without much fear of breaking. While chaining callbacks together allows for one problem to break everything.
* What tools and techniques do you use debugging Javascript code?
    The best set of tools is the Chrome inspector. You can view the page like a average user, traverse to the layout, the console and then onto the javascript code which can be stepped through one instruction at a time.
* What language constructions do you use for iterating over object properties and array items?
    for (key in object) {console.log(key)}

## Database Questions

* Design a database schema for Facebook, with at least 4 models, a complete set of attributes for each model, a 1:M association, and a M:M association.

## Ruby/Rails
* What are ruby gems?
    Ruby Gems are packages to install into the current ruby folder to extend functionality.
* What is the difference between a symbol and a string?
    A string is the actual variable containing character data, while a symbole is simply a reference which can point to a string/hash/ect.
* What is the difference between a class method and an instance method?
    Instanced methods use an instantiated object from a class while a class method can be used with just a class name.
* What is the difference between local variables, instance variables, and class variables?
    An instance variable has a independant variable from it's inhereted class. Class variables are shared among all instances of that class. And local variables are available throughout the scope of that function (typically global).
* What is a range?
    A range is a list og numbers starting at a minimum and ending at a maximum; in sequence.
* In ruby, what does attr_accessor do?  
    The Attr_accessor allows specified variables to be accessed outside of that class. By not using this, variables are, by default, set to private.
* What is the purpose of environment files under the config folder in Rails? (development, test, production)
    Environment files, such as variables can change from computer to computer. Not only that, but keys that are not meant to be shared, such as access tokens, can be maintained outside of the shared files of the project more easily.
* What is the purpose of the application.rb file in Rails?
* How can you define a constant?
    const gravityMetersSecond 9.8
* What is the purpose of `yield`?
    Yield allows you to inject a block of code into a function to provide more flexibility and allow you to run slightly different clode functions.
* How do you store API keys when creating an app?
    By storing them in .env files
* How do I send parameters through a url?
    Either by concatinating the string (dirty) or by looking up the documentation for that API and constructing it inside an object and sending that in the call.
* Explain MVC
    Model - Contains the data for the application. Such as a database
    View - The HTML. What the user sees front-end
    Controller - Interacts with model, displays the appropriate view to the user and performs the routing.
* What is a `before_action`? When would you use it?
* What do controllers do in rails?
    A controller is responsible for interacting with model, displays the appropriate view to the user and performs the routing.
* What is RESTful routing?
    Using a predefined & agreed upon approach for performing GET, POST, DELETE and PUT routes. The routes should be the same to fit convention.
* What is a polymorphic association?
    A model that belongs to more than one database model, all with a single association
* What are params?
    params are parameters for a query. This is extra data to provide a server to get back more specific data.
* How do I make a migration to add a column in Rails?
    rails generate migration add_email_to_users email:string
    There is abstraction when choosing a table. add_email_to_users for example.    
* What is CSRF? How does Rails protect an app against this?
* What's the difference between `User.find_by_id(1)` and `User.find(1)`?
    find_by_id happens to be the same as find. Typically the find_by will be followed by a different column name. such as find_by_name
* What's are classes in Ruby? What are modules? And what's the difference?
    A module is a collection of methods and constants.
    Classes are about objects, modules are about functions.
    --HELP--

## Testing Questions

* What are some advantages/disadvantages to testing your code?
    Advantages are that you can see if modifying the code broke it or not. Disadvantages are that you have to write your own tests, and tests are only as good as you write them.
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?
    Linting tools help push coders in the right syntactical direction. Poor programming habbits will not be passed by the linter. Trivial matters such as spacing issues can also be cleaned with linters as well.
* What is End-to-end (E2E) testing? How can it be implemented in frameworks like Angular and Rails?


## Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
    1020

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
    --HELP--

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
    goh angasal a m\'i

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
  One alert of 'Hello World' and an error for an undefined bar. Bar is not defined on the last line.


*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
    2

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
    foo {n: 2}

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
    one, three, two

## Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Do you have any pet projects? What kind?
* How do you like your coffee?

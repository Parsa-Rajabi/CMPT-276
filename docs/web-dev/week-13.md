<!-- markdownlint-disable -->
# Intro to JavaScript + DOM 

As part of this lesson, we'll cover the baiscs of JavaScript and jQuery. JavaScript is a programming language that is used to create interactive effects within web browsers. jQuery is a JavaScript library that simplifies the process of writing JavaScript code.

## Table of Contents

- [Intro to JavaScript + DOM](#intro-to-javascript--dom)
  - [Table of Contents](#table-of-contents)
  - [JavaScript](#javascript)
    - [Client-Side Scripting](#client-side-scripting)
  - [Where Does JavaScript Fit In?](#where-does-javascript-fit-in)
    - [Inline JavaScript](#inline-javascript)
    - [Embedded JavaScript](#embedded-javascript)
    - [External JavaScript](#external-javascript)
  - [JavaScript Basics](#javascript-basics)
    - [Variables](#variables)
    - [JavaScript Output](#javascript-output)
      - [Alert Box](#alert-box)
      - [Confirm Box](#confirm-box)
      - [Prompt Box](#prompt-box)
    - [Data Types](#data-types)
    - [Concatenation](#concatenation)
  - [Conditional Statements](#conditional-statements)
    - [The `if` Statement](#the-if-statement)
    - [The `else` Statement](#the-else-statement)
    - [The `else if` Statement](#the-else-if-statement)
    - [The `switch` Statement](#the-switch-statement)
    - [Comparison and Logical Operators](#comparison-and-logical-operators)
      - [Comparison Operators](#comparison-operators)
      - [Logical Operators](#logical-operators)
  - [Functions](#functions)
    - [Defining a Function](#defining-a-function)
  - [The Document Object Model (DOM)](#the-document-object-model-dom)
    - [DOM Nodes](#dom-nodes)
    - [Document Object](#document-object)
    - [Selection Methods](#selection-methods)
    - [Element Node Object](#element-node-object)
  - [JavaScript Events](#javascript-events)
    - [Event Types](#event-types)
      - [Pop-up Events](#pop-up-events)
      - [Mouse Event](#mouse-event)
      - [Keyboard Event](#keyboard-event)
    - [Event Handlers](#event-handlers)
      - [Assigning Event Handlers](#assigning-event-handlers)
      - [HTML Event Attributes](#html-event-attributes)
      - [DOM Property](#dom-property)
      - [addEventListener Method](#addeventlistener-method)
    - [Example: Handling a Button Click](#example-handling-a-button-click)
    - [Event Object](#event-object)
    - [Preventing Default Behavior](#preventing-default-behavior)


The videos below provide an overview of the topics for this week. You can watch the videos before or after reading the content for this week.

- [What is JavaScript? [4:04]](https://youtu.be/eVVyXoBueb8?si=xuwgsZe1UaWzH-nk)
- [Adding JavaScript to your Project [7:49]](https://youtu.be/B_wvzmjWPoE?si=62iQOOB7zyIF2kt6)
- [JavaScript Syntax and Comments [11:22]](https://youtu.be/y4tWF-wHMCE?si=wN2rftA23twbGpuB)
- [How to Output JavaScript [11:03]](https://youtu.be/0xShDHwdpas?si=EGd9Yn2lmXKqJfV4)
- [JavaScript Variables [11:19]](https://youtu.be/QYYyUjbLr5k?si=eKkcj1A_mvAMlG9B)
- [JavaScript If else Statements [10:49]](https://youtu.be/oUjiIPOZxSk?si=vAp-U4skA422mVFP)
- [Learn DOM Manipulation [18:36]](https://youtu.be/y17RuWkWdn8?si=UiOnx_TyCTt-L6Q2)
- [Overview of JavaScript Events [15:11]](https://youtu.be/YiOlaiscqDY?si=APtfG7yJg9CqC5L9t)

## JavaScript

So, what is JavaScript? It’s an object-based, client-side scripting language interpreted by a web browser. JavaScript is considered to be object-based because it’s used to work with the objects associated with a web page document: the browser window, the document itself, and elements such as forms, images, and links. Because JavaScript is interpreted by a browser, it is considered to be a client-side scripting language. A scripting language is a type of programming language, but no need to worry! You don’t have to be a computer programmer to understand this. 

### Client-Side Scripting

The idea of client-side scripting is an important one in web development. It refers to the client machine (i.e., the browser) running code locally rather than relying on the server to execute code and return the result. There are many client-side languages that have come into use over the past two decades including Flash, VBScript, Java, and JavaScript. Some of these technologies only work in certain browsers, while others require plugins to function (although the majority of them have been deprecated in favor of JavaScript). We will focus on JavaScript due to its browser interoperability (that is, its ability to work/operate on most browsers). The figures below shows how a client machine downloads and executes JavaScript code:

![alt text](images/content/W13/JS-Client-Scripting.png)

![alt text](images/content/W13/JS-Front-Backends.png)


While JavaScript is still predominately used to create user interfaces in browser-based applications, its role has expanded beyond the constraints of the browser, as seen in the figure below.

Thanks in part to Google, Mozilla, and Microsoft, SpiderMonkey, and Chakra (their respective JavaScript engines) as open-source projects that can be embedded into any C++ application, JavaScript has migrated into other non-browser applications. It can be used as the language within server-side runtime environments such as Node.js. Some newer non-relational database systems such as MongoDB use JavaScript as their query language. Complex desktop applications such as Adobe Creative Suite and OpenOffice use JavaScript as their end-user script- ing language. A wide variety of hardware devices such as the Oculus Rift headset and the Arduino and Raspberry Pi microcontrollers make use of an embedded JavaScript engine. Indeed, JavaScript appears poised to be the main language for the emerging Internet of Things.

![alt text](images/content/W13/JS-Usecases.png)

## Where Does JavaScript Fit In?

Just as CSS styles can be inline, embedded, or external, JavaScript can be included in a number of ways. Just as with CSS, these can be combined, but external is the preferred method for simplifying the markup page and ease of maintenance. The example below illustrates the three different ways JavaScript can be added to an HTML page. Notice that JavaScript can appear in both the `<head>` and the `<body>` elements.

![alt text](images/content/W13/JS-locations.png)

### Inline JavaScript

Inline Javascript refers to the practice of including JavaScript code directly within some HTML element attributes, as can be seen above. You may recall that earlier in the course, you were warned that inline CSS is in general a **bad practice** and should be avoided. The **same is true with JavaScript**. In fact, inline JavaScript is much worse than inline CSS, as maintaining inline JavaScript is a real night-mare, requiring maintainers to scan through almost every line of HTML looking for your inline JavaScript. W3C and standard best practices strongly discourage you from using inline JavaScript.

### Embedded JavaScript

Embedded JavaScript refers to the practice of placing JavaScript code within a `<script>` element, as shown above. Like its equivalent in CSS, embedded JavaScript is okay for quick testing and for learning scenarios (e.g., small samples in this book) but is
usually avoided. As with inline JavaScript, embedded scripts can be difficult to maintain.

### External JavaScript

The recommended way to use JavaScript is to place it in an external file. You do this via the `<script>` tag as shown above. By convention, JavaScript external files have the file extension `.js`. Modern websites often have links to several, maybe even dozens, of external JavaScript files (also called libraries). These external files typically contain function definitions, data definitions, and other blocks of JavaScript code.

In the example above, the links to the external JavaScript file appear both in the `<head>` and in the `<body>` elements. Generally speaking, for maintainability reasons, `<script>` elements are usually placed within the `<head>` element (and for performance reasons, after any CSS `<link>` elements). For performance reasons, some scripts are placed at the end of the document, just before the `</body>` closing tag.
Some of the initial examples in this section place the `<script>` tag right before the `</body>` tag for a different reason. Those examples are performing DOM manipulation, which can only occur after the body/document is completely read in. However, once event handling is covered, the `<script>` tag will move back to the `<head>`.

## JavaScript Basics

### Variables

When one learns a new programming language, it is conventional to begin with variables and data types. We will begin with these topics as well.
Variables in JavaScript are **dynamically typed**, meaning that you do not have to declare the type of a variable before you use it. This means that a variable can be a number, and then later a string, then later an object, if so desired. This simplifies variable declarations, since we do not require the familiar data-type identifiers (such as int, char, and String) of programming languages like Java or C#.

> [!TIP]
> JavaScript is a **case-sensitive** language. Thus, these two lines declare and initialize two different variables:
> ```javascript
> let count = 5;
> let Count = 9;
> ```

The example below shows that to declare a variable in JavaScript, as discussed shortly, you can use either the `var`, `const`, or `let` keywords (a keyword is a reserved word with a special meaning within a programming language). If you do not specify an initial value its initial value will be `undefined`. For instance, in the example, the variable `abc` has a value of `undefined`.

![alt text](images/content/W13/JS-Variables.png)

Variables should always be defined using either the `var`, `const`, or `let` keywords. While you can, in fact, define variables without using one of these keywords, doing so may give that variable global scope. As we will discover later, when we discuss functions and scope, this is almost always a mistake. For this reason, get in the practice of always declaring variables with one of these keywords.

You may wonder why there are three different keywords for declaring variables. The `let` and `const` keywords were added in ES6 (a version of JavaScript) and are now usually to be preferred over `var`. The table below provides overview of how these three keywords differ.

**Assignment** can happen at declaration time by appending the value to the declaration, or at runtime with a simple right-to-left assignment, as illustrated in the declartion example above. This syntax should be familiar to those who have programmed in languages like C and Java.
There are several additional things worth noting and expanding upon in th example above. First, notice that each line of JavaScript is terminated with a semicolon. If you forget to add the semicolons, the JavaScript engine will still automatically insert them. While opinions on this vary, we advise you to not rely on this feature and instead get in the habit of always terminating your JavaScript lines with a semicolon.
Second, notice that whitespace around variables, keywords, and other symbols has no meaning. Indeed a single line of JavaScript can span multiple lines.

![alt text](images/content/W13/JS-Var-keyword-table.png)

### JavaScript Output

One of the first things one learns with a new programming language is how to output information. For JavaScript that is running within a browser, there are several options, as shown in the table below.

![alt text](images/content/W13/JS-output-methods.png)

When first learning JavaScript, one often uses the `alert()` function. It instructs the browser to display a pop-up or modal dialog window (that is, the user cannot interact with the page until dismissing the dialog) displaying the string passed to the function. There are two other modal dialog options for outputting data, as can be seen below.

![alt text](images/content/W13/JS-output-method-ex.png)

These pop-ups may appear different to each user depending on their browser configuration. What is universal is that the pop-up obscures the underlying web page, and no actions can be done until the pop-up is dismissed.

Alerts are generally not used in production code but provide a quick way to temporarily display or gather simple information. However, using pop-ups can get tedious quickly. The user has to click `OK` to dismiss the pop-up, and if you use it in a loop, you may spend more time clicking OK than doing meaningful debugging. As an alternative, the examples in this section will often use the `console.log()` method (or one of its related cousins, such as `console.warn()` or `console.dir()`) since console output doesn’t interfere with the display of HTML content 

![alt text](images/content/W13/JS-console.png)

Finally, the `document.write()` method can be a useful way to output markup content from within JavaScript. This method is often used to output markup or to combine markup with JavaScript variables, as shown in the following example:

```javascript
let name = "Alex";
document.write("<h1>Title</h1>");
// this uses the concatenate operator (+)
document.write("Hello " + name + " and welcome");
```

#### Alert Box

An `alert` box is used to display a message to the user. When an alert box pops up, the user must click "OK" to proceed. The `alert` method is straightforward and looks like this:

```javascript
alert('This is an alert message.');
```

When this code is executed, a pop-up box with the message "This is an alert message." will be displayed. The user cannot interact with the rest of the page until they click "OK".

#### Confirm Box

A `confirm` box is used to get a yes/no response from the user. When a confirm box pops up, the user must click either "OK" or "Cancel" to proceed. The `confirm` method returns `true` if the user clicks "OK" and `false` if the user clicks "Cancel":

```javascript
let userConfirmed = confirm('Do you want to proceed?');

if (userConfirmed) {
  console.log('User chose OK');
} else {
  console.log('User chose Cancel');
}
```

In this example, a confirm box with the message "Do you want to proceed?" will be displayed. The user's response will be logged to the console.

#### Prompt Box

A `prompt` box is used to get input from the user. When a prompt box pops up, the user must enter some text and click "OK" or click "Cancel" to proceed. The `prompt` method returns the input value if the user clicks "OK" and `null` if the user clicks "Cancel":

```javascript
let userName = prompt('Please enter your name:');

if (userName !== null) {
  console.log('Hello, ' + userName);
} else {
  console.log('User cancelled the prompt.');
}
```

In this example, a prompt box with the message "Please enter your name:". The user's input will be logged to the console based on their response.

### Data Types

JavaScript has two basic data types: **reference types** (usually referred to as objects) and **primitive types** (i.e., nonobject, simple types). What makes things a bit confusing for new JavaScript developers is that the language lets you use **primitive types** as if they are objects. The reason for this slipperiness is that objects in JavaScript are absolutely crucial. Almost everything within the language is an object, so the language provides easy ways to use primitives as if they were objects.

Primitive types represent simple forms of data. ES2015 (a version of JavaScript) defines six primitives, which can be seen in the table below. JavaScript also has object representations of these primitives, which can be confusing!

![alt text](images/content/W13/JS-data-types.png)

### Concatenation

One of the most basic programming tasks in JavaScript is to combine string literals together with other variables. This is accomplished using the concatenate operator `+`. For instance, the example below demonstrates several simple uses of the concatenate operator.

```javascript
const country = "France";
const city = "Paris";
const population = 67;
const count = 2;

let msg = city + " is the capital of " + country;
msg += " Population of " + country + " is " + population;

let msg2 = population + count;

// what is displayed in the console?
console.log(msg);
console.log(msg2);
```

In JavaScript the meaning of the `+` operator will depend on whether the values on either side of the operator are both numbers or not. If the `+` operator is being used on numbers, then it will perform **arithmetic addition**; if being used on a non-number, then it will perform **string concatenation** instead.

In the example above, the first `console.log` will output `Paris is the capital of France Population of France is 67`, while the second console.log will output `70` (because both sides of the + operator are numbers).

```javascript
const country = "France";
const city = "Paris";
const population = 67;
const count = 3;

let msg = city + " is the capital of " + country;
msg += " Population of " + country + " is " + population;

let msg2 = population + count;

// what is displayed in the console?
console.log(msg);
console.log(msg2);
```

Newer versions of JavaScript have added an alternative technique for concatenation, namely, **template literals**, which can be seen demonstrated below:

```javascript
const country = "France";
const city = "Paris";
let msg = `${city} is the capital of ${country}`;
```

Notice that the literal character in this example is the back-tick ` (located to the left of the 1 key on most North American keyboards). The key benefit of template literals is that you can include variable references within the literal, thereby avoiding using the concatenate operator.


## Conditional Statements

In programming, conditional statements are used to perform different actions based on different conditions. JavaScript supports several types of conditional statements that you can use to make decisions in your code: `if`, `else`, `else if`, and `switch`.

### The `if` Statement

The `if` statement is used to execute a block of code only if a specified condition is true. If the condition evaluates to true, the block of code inside the `if` statement is executed. If the condition is false, the code block is skipped. Here’s an example:

```javascript
let price = 20;

if (price >= 19) {
  console.log("This item costs greater than $19.");
}
```

In this example, the console.log statement will execute because the condition `price >= 19` is true.

### The `else` Statement

The else statement is used to execute a block of code if the condition in the if statement is **false**. It provides an alternative path of execution. Here’s how it works:

```javascript
let speed = 15;

if (speed > 20) {
  console.log("You are speeding because your speed is faster than 20 km/hr.");
} else {
  console.log("Your are not speeding.");
}
```

In this case, the `console.log` statement within the else block will execute because the condition `speed > 15` is **false**.

### The `else if` Statement

The else if statement is used to specify a new condition if the first condition is false. You can chain multiple else if statements together to check for various conditions:

```javascript
let score = 85;

if (score >= 90) {
  console.log("Grade: A");
} else if (score >= 80) {
  console.log("Grade: B");
} else if (score >= 70) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
```

In this example, the `console.log("Grade: B")` statement will execute because the score falls within the range specified by the else if condition `score >= 80`.


Another example of the `else if` statement is shown below:

```javascript
let hourOfDay; // variable to hold hour of day, set it later ... 
let greeting; // variable to hold the greeting message
if (hourOfDay > 4 && hourOfDay < 12) {
  greeting = "Good Morning";
}
else if (hourOfDay >= 12 && hourOfDay < 18)  {
  greeting = "Good Afternoon";
}
else {
  greeting = "Good Evening";
}
```

### The `switch` Statement

The `switch` statement is used to perform different actions based on different conditions, but it is often more convenient than multiple `else if` statements. Here’s how you can use a `switch` statement:

```javascript
let day = 3;
let dayName;

switch (day) {
  case 1:
    dayName = "Monday";
    break;
  case 2:
    dayName = "Tuesday";
    break;
  case 3:
    dayName = "Wednesday";
    break;
  case 4:
    dayName = "Thursday";
    break;
  case 5:
    dayName = "Friday";
    break;
  case 6:
    dayName = "Saturday";
    break;
  case 7:
    dayName = "Sunday";
    break;
  default:
    dayName = "Invalid day";
}

console.log(dayName);
```

In this example, the `console.log(dayName)` statement will output "Wednesday" because the value of `day` is 3.

Here is another example of the `switch` statement in comparison to the `if-else` statement:

```javascript
switch (artType) {
  case  "PT":
     output = "Painting";
     break;
  case  "SC":
     output = "Sculpture";
     break;
  default:
     output = "Other";
}
// equivalent
if (artType == "PT") {
   output = "Painting";
} else if (artType == "SC") {
   output = "Sculpture";
} else {
   output = "Other";
}
```

### Comparison and Logical Operators

In JavaScript, comparison and logical operators are used to create conditions in your code. Understanding these operators is crucial for effectively using conditional statements.

#### Comparison Operators

Comparison operators are used to compare two values. They return a boolean value (`true` or `false`). Here are some common comparison operators:

![alt text](images/content/W13/JS-comparator-operations.png)

```javascript
let x = 10;
let y = "10";

console.log(x == y);  // true
console.log(x === y); // false
```

In this example, `x == y` evaluates to true because the values are equal, but `x === y` evaluates to false because the types are different (number vs. string).

#### Logical Operators

Logical operators are used to combine multiple conditions. They return a boolean value and are essential for constructing more complex conditions:

- `&&` Logical `AND`
- `||` Logical `OR`
- `!` Logical `NOT`

```javascript
let age = 25;
let hasLicense = true;

if (age >= 18 && hasLicense) {
console.log("You can drive.");
} else {
console.log("You cannot drive.");
}
```

In this example, the `console.log("You can drive.")` statement will execute because both conditions `age >= 18` and hasLicense are true.


## Functions

Functions are a fundamental concept in JavaScript. They allow you to define reusable blocks of code that can be executed with different inputs. Functions help you organize your code, reduce repetition, and improve readability.

### Defining a Function

You can define a function using the `function` keyword, followed by a `name`, parentheses `()`, and a block of code `{}`. Here’s an example of a simple function that adds two numbers:

```javascript
function add(a, b) {
return a + b;
}

let result = add(5, 3);
console.log(result); // Output: 8
```

In this example, the add function takes **two parameters**, `a` and `b`, and **returns** their `sum`. The function is called with the **arguments** `5` and `3`, and the result is stored in the `result` variable.

```javascript
function add(a, b) {
return a + b;
}
```

The above is formally called a **function declaration**. Such a declared function can be called or invoked by using the `()` operator.

```javascript
let result = add(5, 3);
```

With new programmers there is often confusion between **defining a function** and **invoking the function**. Remember that when you use the keyword `function`, you are defining what the function does. Later, you can use or invoke that function by using its given name without the function keyword but with the brackets `()`. While the function declaration above returns a value, your functions can simply perform actions and not return any value.



## The Document Object Model (DOM)

While JavaScript is now used in a variety of different contexts, by far the most com- mon is the browser. Within the browser context, JavaScript needs a way to interact with the HTML document in which it is contained. As such, there needs to be some way of programmatically accessing the elements and attributes within the HTML.

According to the W3C, the DOM is a
> platform- and language-neutral interface that will allow programs and scripts to dynamically access and update the content, structure and style of documents.
>

We already know all about the DOM, but by another name. The tree structure from earlier in the course is formally called the **DOM Tree** with the root, or topmost object called the **Document Root**. You already know how to specify the style of documents using CSS; with JavaScript and the DOM, you now can do so dynamically as well at runtime, in response to user events. Thus, we can summarize and say that the DOM provides a standardized, hierarchical (tree-like) way to access and manipulate the contents of an HTML document.

![alt text](images/content/W13/DOM-tree.png)

### DOM Nodes

In the DOM, each element within the HTML document is called a **node**. If the DOM is a tree, then each node is an individual branch. As can be seen in the example below, there are element nodes and text nodes (plus a few other uncommonly encountered ones). 

![alt text](images/content/W13/DOM-tree.png)

All nodes in the DOM share a common set of properties and methods. These properties and methods allow you to retrieve information about the node, manipulate its properties (for instance, changing its CSS properties or retrieving its text content), and even create new content. Some of these properties are available to all nodes; others are only available to, for instance, element nodes. Furthermore, depending on the element, some nodes will have specific properties for the specific element. The table below lists some of the more important properties that all nodes, regardless of type, share.

### Document Object 

The DOM document object is the root JavaScript object representing the entire HTML document. It contains some properties and methods that we will use extensively in our development and is globally accessible via the document object reference.

![alt text](images/content/W13/DOM-node-properties.png)

The properties of this document object cover a wide-range of information about the page. Some of these are read-only, but others are modifiable. Like any other JavaScript object, you can access its properties using either dot notation or square bracket notation, as illustrated in the following example:

```javascript
 // retrieve the URL of the current page
let a = document.URL;
// retrieve the page encoding, for example ISO-8859-1 
let b = document["inputEncoding"];
```

In addition to these properties, there are several essential methods you will use all the time. The last chapter introduced you to one of these, the `document.write()` method. To help us better familiarize ourselves with this object, we will group the methods into these three categories:

- Selection methods
- Family manipulation methods Event methods
- We will cover each of these in the next several sections.

![alt text](images/content/W13/DOM-methods.png)

### Selection Methods

The most important DOM methods are those that allow you to select one or more document elements; they are shown above. The relationship between the first three methods is shown below. The method `getElementById()` is perhaps the most commonly used of these selection methods. It returns a single DOM Element (covered as follows) that matches the id passed as an argument. 

![alt text](images/content/W13/DOM-getElement.png)



Selectors are a powerful mechanism for selecting elements in CSS. `querySelector()` and `querySelectorAll()` are two methods that allow you to use CSS selectors to select elements in the DOM. The `querySelector()` method returns the first element that matches a specified CSS selector, while the `querySelectorAll()` method returns a collection of all elements that match a specified CSS selector. The example below demonstrates how to use these methods:

![alt text](images/content/W13/DOM-querySelector.png)

### Element Node Object

The type of object returned by the methods `getElementById()` and `querySelector()` described in the previous section is an **Element Node object**. This represents an HTML element in the hierarchy, contained between the opening `<>` and closing `</>` tags for this element. As you may already have figured out, an element can itself contain more elements. Every element node has the node properties shown below. It also has a variety of additional properties, the most important of which are shown in the following tables:

```html
<p id="here">hello <span>there</span></p>
<ul>
    <li>France</li>
    <li>Spain</li>
    <li>Thailand</li>
</ul>
<div id="main">
<a href="somewhere.html"><img src="whatever.gif" class="thumb"></a> </div>
<script>
const node = document.getElementById("here"); // outputs: hello <span>there</span> console.log(node.innerHTML);
// outputs: hello there console.log(node.textContent);
    const items = document.getElementsByTagName("li");
    for (let i=0; i<items.length; i++) {
        // outputs: France, then Spain, then Thailand
        console.log(items[i].textContent);
    }
    const link = document.querySelector("#main a");
    // outputs: somewhere.html
    console.log(link.href);
    const img = document.querySelector("#main img");
    // outputs: whatever.gif
    console.log(img.src);
    // outputs: thumb
    console.log(img.className);
</script>
```



![alt text](images/content/W13/DOM-Node-essential-properties.png)

![alt text](images/content/W13/DOM-HTML-Element-properties.png)


## JavaScript Events

Events are an essential part of almost all real-world JavaScript programming. The example below illustrates the four steps involved in JavaScript event processing. You begin by **defining** an event handler which is simply a callback function. That handler is then **registered** with a specific event for a specific element. From a programming perspective, that’s it. The next steps occur at runtime: the specific event is **triggered**, usually by some user action, and then the handler finally **executes**.


![alt text](images/content/W13/JS-event-handling.png)


The example also illustrates the coding involved in implementing a simple event handler. Notice that an event handler is first defined, then registered to an element node object.

Registering an event handler requires passing a **callback** function to the `addEventListener()` method of a single node object. The callback function is executed when the event is triggered. The example below demonstrates how to register an event handler for a button click event in 3 different ways:

```javascript
const btn = document.getElementById("btn");
btn.addEventListener("click", function () {
    alert("used an anonymous function");
});

document.querySelector("#btn").addEventListener("click", function () {
    alert("a different approach but same result");
});

document.querySelector("#btn").addEventListener("click", () => {
   alert("arrow syntax but same result");
});
```



### Event Types

There are many different types of events that can be triggered in the browser. Perhaps the most obvious event is the click event, but JavaScript and the DOM support several others. In actuality, there are several classes of event, with several types of events within each class specified by the W3C. Some of the most commonly used **event types** are mouse events, keyboard events, touch events, form events, and frame events.

#### Pop-up Events

JavaScript provides three types of pop-up boxes: `alert`, `confirm`, and `prompt`. These pop-ups are used to interact with the user, gather input, and display information. They are simple to use and provide basic ways to communicate with the user.

#### Mouse Event

Mouse events are defined to capture a range of interactions driven by the mouse. These can be further categorized as mouse click and mouse move events. The table below lists some of the possible events one can listen for from the mouse.

Interestingly, many mouse events can be sent at a time. The user could be moving the mouse off of one `<div>` and onto another in the same moment, triggering mouseon and mouseout events as well as the mousemove event. 

![alt text](images/content/W13/JS-event-mouse.png)


#### Keyboard Event

Keyboard events are often overlooked by novice web developers, but are important tools for power users. The table below lists the most common keyboard events.

![alt text](images/content/W13/JS-event-keyboard.png)

These events are most useful within input fields. We could, for example, validate an email address, or send an asynchronous request for a dropdown list of suggestions with each key press.

We could listen to key press events for an input box with an `id` of `key` and echo each pressed key back to the user as shown below 


```javascript
document.getElementById("key").addEventListener("keydown",
  function (e) {
    // get the raw key code
    let keyPressed=e.key;
    // convert to string
    let character=String.fromCharCode(keyPressed); 
    alert("Key " + character + " was pressed");
});
```

### Event Handlers

Event handlers are functions that are executed in response to an event. An event handler is embedded in an HTML tag as an `attribute` and indicates some JavaScript code to execute when the event occurs. Event handlers use the event name with the prefix “on”. The table below shows the event handlers that correspond to the events described earlier. 

For example, the `onload` event is triggered when browser renders (loads) a web page. When you move your mouse pointer over a text hyperlink, a `mouseover` event occurs and is detected by the browser. If that hyperlink contains an ​ `onmouseover event handler`, the JavaScript code indicated by the event handler will execute. This code might pop up an alert message, display an image, or display a menu. Other event handlers such as `onclick` and `onmouseout` can cause JavaScript code to ​execute when their corresponding event occurs.

| Event        | Description                                                      | Event Handler     |
|--------------|------------------------------------------------------------------|-------------------|
| `click`      | Occurs when the user clicks on an element                        | `onclick`         |
| `mouseover`  | Occurs when the user moves the mouse pointer over an element     | `onmouseover`     |
| `mouseout`   | Occurs when the user moves the mouse pointer out of an element   | `onmouseout`      |
| `keydown`    | Occurs when the user presses a key on the keyboard               | `onkeydown`       |
| `keyup`      | Occurs when the user releases a key on the keyboard              | `onkeyup`         |
| `load`       | Occurs when the page or an image has finished loading            | `onload`          |
| `unload`     | Occurs when the user leaves the page                             | `onunload`        |
| `submit`     | Occurs when a form is submitted                                  | `onsubmit`        |

#### Assigning Event Handlers

Event handlers can be assigned in three main ways:

1. **HTML Event Attributes**
2. **DOM Property**
3. **addEventListener Method**

#### HTML Event Attributes

You can assign an event handler directly in the HTML element using an attribute. Here’s an example:

```html
<button onclick="alert('Button clicked!')">Click me</button>
```

#### DOM Property

You can also assign an event handler using the DOM property of the element. This method is often preferred because it keeps the HTML and JavaScript separate:

```javascript
let button = document.getElementById('myButton');
button.onclick = function() {
  alert('Button clicked!');
};
```

#### addEventListener Method

The `addEventListener` method allows you to assign multiple event handlers to the same event on the same element. It’s the most versatile and recommended approach:

```javascript
let button = document.getElementById('myButton');
button.addEventListener('click', function() {
  alert('Button clicked!');
});
```

### Example: Handling a Button Click

Here’s a complete example of handling a button click event using the `addEventListener` method:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Event Handling Example</title>
  <script>
    document.addEventListener('DOMContentLoaded', function() {
      let button = document.getElementById('myButton');
      button.addEventListener('click', function() {
        alert('Button clicked!');
      });
    });
  </script>
</head>
<body>
  <button id="myButton">Click me</button>
</body>
</html>
```

In this example, an event listener is added to the button with the ID `myButton`. When the button is clicked, an alert message is displayed.

### Event Object

When an event occurs, an event object is automatically created and passed to the event handler function. This object contains useful information about the event, such as the type of event, the element that triggered the event, and the position of the mouse.

```javascript
let button = document.getElementById('myButton');
button.addEventListener('click', function(event) {
  console.log('Event type:', event.type);
  console.log('Element that triggered the event:', event.target);
});
```

In this example, when the button is clicked, information about the event is logged to the console.

### Preventing Default Behavior

Sometimes, you might want to prevent the default behavior of an event. For example, you might want to prevent a form from being submitted when a button is clicked. You can do this using the `preventDefault` method of the event object:

```javascript
let form = document.getElementById('myForm');
form.addEventListener('submit', function(event) {
  event.preventDefault();
  alert('Form submission prevented.');
});
```

In this example, the form submission is prevented, and an alert message is displayed instead.
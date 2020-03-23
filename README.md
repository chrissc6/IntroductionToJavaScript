# IntroductionToJavaScript
:atom:

JavaScript docs:<br/>
[Mozilla] https://developer.mozilla.org/en-US/docs/Web/JavaScript<br/>

VSCode shortcuts:<br/>
[Visual Studio] https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf<br/>
 * All codes: (Ctrl + K & Ctrl + S)<br/>
 * Format code: (Shift + Alt + F)<br/>
 * Comment: (Shift + Alt + A)<br/>
 * Uncomment: (Ctrl + K & Ctrl + U)<br/>

### Lesson 1

The vast majority of Web pages out there right now contain some JavaScript code.<br/>
JavaScript code is executed in the Web browser.<br/>
Web page = content + code<br/>
JavaScript controls how the page behaves or reacts when users click something on the page.<br/>
JavaScript is an interpretive language. (scripting language)<br/>
JavaScript was first developed for the popular Netscape Navigator Web browser. (LiveScript)<br/>
Netscape handed JavaScript over to ECMA International, a global standards organization in 1996.<br/>
The standardized language that the ECMA has created is officially named ECMAScript.<br/>

Basic syntax of JavaScript methods:<br/>
method(parameters)<br/>

JavaScript is case-sensitive<br/>

### Lesson 2

Events are things that happen while a person is viewing and interacting with the page.<br/>
The act of taking control of exactly what happens in response to some event is called event handling.<br/>
To control exactly when a piece of JavaScript code executes, we use event handlers inside HTML tags.

Code between <script> tags executes when the page first opens in the browser.<br/>
Functions are placed between <script> tags in the head section.<br/>
Each function is identified by the word function followed by a name.<br/>
Functions are executed when called by event handlers in tags.

A span is an inline element that's only as wide as the characters contained within it.

In inline JavaScript, the outermost quotation marks after the event handler should match.

Each line of code in a JavaScript can end in a line break, or a semicolon, or both.

Events:
* onmouseover
* onclick
* oncontextmenu
* ondblclick

Basic syntax of JavaScript methods:<br/>
```javascript
function name(){
//code
}
```

Debugging JavaScript:<br/>
The browser will always try to execute your JavaScript code.<br/>
You can use console.log() to display JavaScript values in the debugger window<br/>
You can set breakpoints in the JavaScript code.

Enable JavaScript:<br/>
https://www.enable-javascript.com/

### Lesson 3

JavaScript is object-oriented<br/>
It's designed to allow you to treat a Web page as though it were a collection of actual objects in the real world.

Document Object Model (DOM)<br/>
DOM is essentially a set of rules and words you use to access and manipulate things on a Web page.<br/>
DOM defines the names used to refer to many aspects of the environment in which a Web page is showing.<br/>
A Web page is a document.<br/>
The DOM represents that same document so it can be manipulated.<br/>
Which can be modified with a scripting language such as JavaScript.

Objects:
 * screen
 * window
 * navigator
 * location
 * document

Different objects in the object model have different properties and methods.<br/>
Properties are characteristics of the object.<br/>
Methods are things that the object can do.

Basic syntax of JavaScript properties:<br/>
```javascript
object.property
```

Control refers to any element on the page with which a user can interact.

Textbox control:
```html
<label for="username">Enter Username:</label>
<input type="text" id="username">
```

Button control:<br/>
```html
<input type="button" value="Go" onclick="alert('Hello ' + document.getElementById('username').value)" >
```

A literal is a value that never changes<br/>
A variable is a value that can vary

Variable name rules:
 * must start with a letter or an underscore character
 * after the first character, the name can contain any letters, numbers, an underscore, or a hyphen
 * cannot contain blank spaces
 * only punctuation characters allowed are the hyphen and underscore
 * cannot be a reserved word

### Lesson 4

Strings:<br/>
You can actually store anything as a string.<br/>
Unless you want to perform arithmetic (or date arithmetic).
```javascript
var name="Hello string"
```

Numbers:<br/>
Numbers in JavaScript (and all programming languages) are quantities. (scalar values)<br/>
The term "scalar" comes from linear algebra, where it is used to differentiate a single number from a vector or matrix.<br/>
Which you can perform arithmetic calculations.<br/>
You can only do arithmetic with numbers.<br/>
You can store an invalid number as a string.<br/>
You can't store ZIP codes, Social Security numbers, or phone numbers as numbers, but they're not true numbers in the sense of being scalar values.<br/>

Number rules:
 * can contain digits (0-9) and one decimal point (period)
 * the first character in front of the number can be a hyphen to indicate a negative number
 * cannot contain commas, spaces, parentheses, embedded hyphens, or dollar signs
 * never use quotation marks with numbers

toFixed( ) Function:
```javascript
number.toFixed( value )
```
Used to format a number using fixed-point notation.

Dates:<br/>
You can also do date arithmetic (date x days from now, the number of days between two dates)
```javascript
var name = new Date(1999,0-11,1-31)
var halloween = new Date("October 31 2013")
var valentines = new Date("February 14 2015 18:35:00")
```

When you get down to the level of the actual CPU that's doing the math and managing the lists, it's actually more efficient to use zero-based lists, which in turn make the code run faster.

Boolean Values:<br/>
If you assign a value other than true or false, the value you assign will be converted to true or false.<br/>
Any text in quotation marks to a Boolean value will set the value to true.<br/>
False values: (0, -0, null, "", undefined, NaN), any other value will set the value to true.

if Statements:<br/>
if must be typed in lowercase.

```javascript
if (condition) code to execute;
```

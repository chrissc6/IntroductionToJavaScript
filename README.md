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

Objects:<br/>
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

Textbox control:<br/>
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

Variable name rules:<br/>
 * must start with a letter or an underscore character
 * after the first character, the name can contain any letters, numbers, an underscore, or a hyphen
 * cannot contain blank spaces
 * only punctuation characters allowed are the hyphen and underscore
 * cannot be a reserved word





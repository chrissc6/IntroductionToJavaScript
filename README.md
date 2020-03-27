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

### Lesson 5

String Concatenation:<br/>
we can assign strings to a variable and use concatenation to combine the variable to another string.<br/>
use the + operator
```javascript
let myPet = 'dog';
console.log('My favorite animal is the ' + myPet + '.');
```

URI (Uniform Resource Identifier):<br/>
a string that refers to a resource. (URL)<br/>
URNs, by contrast, refer to a resource by a name, in a given namespace, such as the ISBN of a book

UTF-8 (UCS Transformation Format 8):<br/>
World Wide Web's most common character encoding.<br/>
Each character is represented by one to four bytes.<br/>
UTF-8 is backward-compatible with ASCII and can represent any standard Unicode character.

URLs must contain only a special subset of ASCII characters:<br/>
Alphanumeric-
```
a b c d e f g h i j k l m n o p q r s t u v w x y z A B C D E F G H I J K L M N O P Q R S T U V W X Y Z 0 1 2 3 4 5 6 7 8 9 
```
Unreserved-
```
- _ . ~
```
Reserved-
```
! * ' ( ) ; : @ & = + $ , / ? % # [ ]
```


encodeURIComponent() function:<br/>
makes the text that the user typed more palatable as a URL<br/>
makes the URLs more compatible with older computers that had limited character sets or didn't treat spaces the same as more modern computers do.<br/>
encodes a URI by replacing each instance of certain characters by one, two, three, or four escape sequences representing the UTF-8 encoding of the character<br/>
(will only be four escape sequences for characters composed of two "surrogate" characters)
```javascript
// encodes characters such as ?,=,/,&,:
console.log(encodeURIComponent('?x=шеллы'));
// expected output: "%3Fx%3D%D1%88%D0%B5%D0%BB%D0%BB%D1%8B"

console.log(encodeURIComponent('?x=test'));
// expected output: "%3Fx%3Dtest"


//encodeURI() function encodes special characters, except: , / ? : @ & = + $ #

//encodeURIComponent() function encodes special characters 
//and in additional the characters which encodeURI doesn't encode
```

Drop-Down List:<br/>
select tag placed where you want the control to appear on the page.
```javascript
<select id="dropdown"> 
      <option value="1">Bing</option> 
      <option value="2" selected>Google</option> 
    </select>
```

### Lesson 6

HTML5 lets you play audio from the browser without plug-ins

Two audio formats that are free of any patent encumbrances are MP3 and OGG. <br/>
All HTML5-compatible browsers support at least one of these formats. <br/>
Developers offer two copies of every sound file used by their page or application.<br/>
Public domain sound files you can use freely.

See if the browser supports HTML5 audio<br/>
object detection<br/>
Determine whether or not the user's browser is capable of handling the code you intend to use
```javascript
if (window.HTMLAudioElement) {
}
```
window.HTMLAudioElement property<br/>
returns true if the browser can handle HTML5 audio

define a player for playing audio files<br/>
Creating an audio object
```javascript
var myAudioFile = document.createElement('audio');
```

Determine whether the browser can play MP3 sound files or OGG sound files<br/>
.canPlayType Property<br/>
Determine which type of file the browser can play.<br/>
returns "" (a zero-length string) if the browser can't play that file type. <br/>
Otherwise, it'll return maybe or probably.

MP3<br/>
audio/mpeg
OGG<br/>
audio/ogg; codecs="vorbis"

codec is short for compressor/decompressor<br/>
The component of the format that indicates the algorithm used to compress the file. <br/>
The same algorithm decompresses the file for playback.

setAttribute Method<br/>
lets you set the value of any attribute in any tag via JavaScript<br/>
HTML attributes are things inside HTML tags that provide information about that tag.
```javascript
element.setAttribute(attributename,value)
```
element:<br/>
set or change the attribute or variable for a specific element that's already been identified with a getElementById() attribute
attributename:<br/>
assign a value<br/>
must be a valid attribute for the tag type<br/>
value:<br/>
value you want to assign to the attribute

### Lesson 7

Global Variables<br/>
defined outside of functions<br/>
they can be used by any function without passing them to the function as parameters<br/>
a variable that is declared in the global scope<br/>
a variable that is visible from all other scopes

Local Variable<br/>
defined within functions<br/>
They have local scope, which means that they can only be used within the functions that define them.

Scope (lifespan)<br/>
The current context of execution<br/>
The context in which values and expressions are "visible" or can be referenced.<br/>
The scope of a variable defines what other code on the page can access the contents of a variable. 

Variables and the values assigned to them are stored in memory (RAM).<br/>
You'd need to create thousands of variables in a single page for them to have any noticeable impact on the speed or memory of modern devices.

indexOf method<br/>
finding the starting point of a small string contained within a larger string<br/>
value returned by the indexOf method is -1 if smallstring doesn't exist in the larger string at all<br/>
location is zero-based
```javascript
largestring.indexOf(smallstring)
```

substring<br/>
method returns the part of the string between the start and end indexes, or to the end of the string.
```javascript
string.substr(startposition,length)

const str = 'Mozilla';

console.log(str.substring(1, 3));
// expected output: "oz"

console.log(str.substring(2));
// expected output: "zilla"
```

slice<br/>
method returns a shallow copy of a portion of an array into a new array object selected from begin to end <br/>
(end not included) where begin and end represent the index of items in that array.
```javascript
string.slice(start)
```

parseInt(string)<br/>
Returns the integer portion of string as a number (if possible)<br/>
integer always a whole number with no decimal point<br/>
parseInt function always truncates the decimal portion of a number. <br/>
It never rounds numbers

parseFloat(string)<br/>
Returns the floating point portion of a string as a number (if possible)<br/>
floating point number can have a decimal portion

the string can only be converted to a number if the string starts with a numeric digit (0-9), a hyphen (minus sign), or a dot (decimal point)<br/>
If the string to convert can't be converted to a number, then the function returns NaN, which means "not a number."

Converting Numbers to String<br/>
toString() method returns a string representing the specified Number object
```javascript
function hexColour(c) {
  if (c < 256) {
    return Math.abs(c).toString(16);
  }
  return 0;
}

console.log(hexColour(233));
// expected output: "e9"

console.log(hexColour('11'));
// expected output: "b"
```

You can also concatenate, with a + sign, the number to some string. <br/>
It can even be an empty string

### Lesson 8

Arrays <br/>
a list of items<br/>
Arrays are list-like objects whose prototype has methods to perform traversal and mutation operations. <br/>
Neither the length of a JavaScript array nor the types of its elements are fixed.<br/>
it must start with a letter and cannot contain spaces or special characters<br/>
Make reference to an array element with a subscript (sub) in square brackets.<br/>
starting at 0 (zero) with the first item on the left<br/>
For a multidimensional array, specify additional subscripts.
```javascript
var color = new Array();
color[0]="Red";
color[1]="Green";
color[2]="Blue";

var color2=new Array("Red","Green","Blue");

var color3 = new Array();
var color3=["Red","Green","Blue"];
```

Array Length<br/>
returns a number indicating how many elements are in the array.
```javascript
arrayname.length
```

Array Sort()<br/>
organizes the elements into ascending order (alphabetical order)

Array Reverse()<br/>
reverses whatever order elements happen to be in at the moment<br/>
If you apply a .reverse() right after a .sort(), you'll get a descending sort order, Z-A. 

For Loops<br/>
repeating a loop a predetermined number of times
```javascript
for (start; condition; increment) {
 code to be executed
}
``` 
You can use ++ to increment the value by one, or -- to decrement the value by 1.

While Loops<br/>
loops repeat one or more lines of code as long as some condition remains true
```javascript
while (condition) {
 code to be executed
}
```

do while loop
```javascript
do {
 code to be executed
} while (condition)
```

Switch Statement
```javascript
switch(value)
{
case x1:
  code to execute;
  break;
case x2:
  code to execute;
  break;
default:
  code to execute;
}
```

Ternary Operator<br/>
conditional operator<br/>
shorthand notation for making small, simple if decisions, usually just to assign a value to a variable
```javascript
condition ? return if true : return if false;

var age = 64
var admission = "Your cost: $" + (age < 60 ? "7.50" : "5.00");
```

== operator<br/>
returns true if the values being compared are equal

=== operator<br/>
returns true only if the values and the data types being compared are the same

testing and debugging code<br/>
console.write()<br/>
console.log()<br/>
alert()

### Lesson 9

JavaScript Timers (timing events)<br/>
put time delays on code execution<br/>
passage of time, rather than a mouse click or other user activity, causes the event<br/>
Timing events are also used for slideshows and many kinds of animated transition events.


setTimeout("function", milliseconds)<br/>
Executes the named function once, after waiting the number of seconds specified by milliseconds.<br/>
call some function once, after a time delay.

setInterval("function", milliseconds)<br/>
Executes code or a function repeatedly at specific time intervals. <br/>
It's kind of like a loop but with a time delay each time through the loop.<br/>
call some function repeatedly, with a time delay between each call.

Half a second = 500 milliseconds

```javascript
var name = setInterval("function", milliseconds):

//clearInterval or clearTimeout to stop the timer
clearInterval(name)
clearTimeout(name)
```

window.onload()<br/>
Make sure everything is loaded<br/>
The onload event occurs when an object has been loaded.<br/>
The load event fires when a given resource has loaded.<br/>
call some function or execute some code after the entire Web page has been fully downloaded.
```javascript
window.onload = function() {
   JavaScript code to execute on page load;
}
```

CSS style classes<br/>
transition property that allows you to animate the application of a CSS property by extending the time it takes for the property to be applied.

CSS fadein 
``` CSS
/* Style to fadein */
    .fadein {
      opacity: 1;
      transition: all ease-out 0.25s;
    }
```

CSS fadeout 
``` CSS
/* Style to fadeout */
    .fadeout {
      opacity: 0;
      transition: all ease-out 0.25s;
    }
```

The opacity property specifies the opacity/transparency of an element.
```CSS
img {
  opacity: 0.5;
}

img:hover {
  opacity: 1.0;
}
```

CSS .class Selector<br/>
selects elements with a specific class attribute
```CSS
//class="intro"

.intro {
  background-color: yellow;
}
```

jQuery<br/>
The most famous and most widely-used JavaScript library

### Lesson 10

Downloading jQuery https://jquery.com/download/

Google CDN https://developers.google.com/speed/libraries/devguide#jquery

Microsoft CDN https://www.asp.net/ajax/cdn#jQuery_Releases_on_the_CDN_0


jQuery <br/>
jQuery is a JavaScript library<br/>
make it much easier to use JavaScript<br/>
a library of prewritten JavaScript code that allows you to do more with JavaScript using relative short, simple code<br/>
jQuery's motto is Write less, do more<br/>
jQuery is a free external file of JavaScript code that you can use in your own site for free<br/>
jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code.<br/>
jQuery also simplifies a lot of the complicated things from JavaScript, like AJAX calls and DOM manipulation

The jQuery library contains the following features:<br/>
 * HTML/DOM manipulation
 * CSS manipulation
 * HTML event methods
 * Effects and animations
 * AJAX
 * Utilities

Versions 

Version1<br/>
Versions that start with 1 continue to provide support for Internet Explorer versions 6, 7, and 8

Version2<br/>
Versions starting with 2 offer all the same tools and capabilities that versions starting 1<br/>
Version 2 does not include code that allows all jQuery features to work in those older Internet Explorer versions 6, 7, and 8

MinVersion<br/>
minified or min version<br/>
everything that can be done to minimize the file size has been done<br/>
The production version removes all of the line breaks and indents to make the file smaller and faster

internal JavaScript code <br/>
JavaScript code is "inside" the page in which it's executed 

external JavaScript code<br/>
Any JavaScript code can be stored in an external file and linked to the current page using a <script src="..."> tag<br/>
put the JavaScript code in its own separate file, then just link each page to the external file<br/>
To link to an external JavaScript file, you use a <script> tag with an src (source) attribute
```javascript
<script src="path"></script>
```

CDN (Content Development Network)<br/>
a system of distributed servers (network) that deliver pages and other web content to a user, based on the geographic locations of the user, the origin of the webpage and the content delivery server<br/>
most people use jQuery from a CDN<br/>
As an alternative to downloading and serving the file yourself, you can serve it from a CDN (Content Development Network)
```javascript
//Google's CDN
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js">
</script>

//Microsoft's CDN
<script src="http://ajax.aspnetcdn.com/ajax/jquery/jquery-1.9.1.min.js">
</script>
```

Using jQuery <br/>
use the $ symbol<br/>
Some people think of the dollar sign as meaning using jQuery or get from the jQuery library or just get<br/>
the $ is basically telling the Web browser to look in the jQuery library for the JavaScript code to execute<br/>
it's important that any elements in the page that are affected by jQuery code actually exist in the page, fully rendered on the screen, before jQuery attempts to act on the element.

anonymous function<br/>
one or more lines of code that are executed in sequence<br/>
called an anonymous function because it doesn't have a specific name

document.ready<br/>
Virtually all jQuery code that you write yourself should be placed inside a $(document).ready(function () { . . . }); block. <br/>
jQuery syntax for when the page is fully loaded and ready<br/>
jQuerys way of saying Let the entire page load before trying to execute any jQuery code<br/>
the document.ready code is always the same<br/>
all of the jQuery code on a page is typically placed inside the curly braces and parens of the document.ready block (or its shorthand equivalent)

```javascript
<script>
$(document).ready(function() {
 // jQuery code to execute after page load
});
</script>
```

All the jQuery code for any given page is usually placed inside the curly braces and parentheses of that block to ensure that none of the code tries to execute before the page is ready for code execution

```javascript
<script>
$(function() {
  // jQuery code to execute after page load
});
</script>
```
The longer document.ready() syntax at least gives you some clue as to what the code means.

Writing jQuery Code<br/>
you rely on the $ to call prewritten code from the jQuery library
```javascript
$("selector").event(function(){
  code to execute;
 }); 
```

selector <br/>
the element, or type of element, that will call the code<br/>
having the option to write code that applies to multiple elements on the page is one of jQuery's best features<br/>
you can put just about any CSS selector in place of selector to apply the code to any number of elements on a page, just as you can use CSS selectors to apply

event <br/>
the name of the action that, when performed on the element or element type, will call the code

jQuery Selectors<br/>
describes the element or elements that trigger an event or are acted upon by jQuery<br/>
If the selector matches an element type, then the code applies to all elements of that type<br/>
selector naming scheme similar to CSS<br/>
selector syntax that you use to target the function is the same as the selector syntax that you use for targeting CSS style rules

In CSS, you can use # in a selector to apply the style to the element that has that ID name. <br/>
The same concept applies to jQuery.

best of both worlds with selectors<br/>
write a jQuery function that applies to any one element on the page, or to many elements

jQuery Events<br/>
describes an action that must be performed to fire (execute) the jQuery code

jQuery Special Effects<br/>
built-in effects<br/>
jQuery effects are written to work even with older Web browsers<br/>
The ability to apply JavaScript in much the same way you can apply CSS is one of jQuery's best features
```javascript
$("selector").effect(value);
```
value is optional and can be omitted.<br/>
If included, it has to be a valid jQuery keyword, like slow or fast, or a number expressing the number of milliseconds.

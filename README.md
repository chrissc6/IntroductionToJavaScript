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
# ProfStef-README
Text version of Pharo ProfStef lessons

# Table of Contents
+ [Welcome (1/29)](#welcome-129)
+ [Doing (2/29)](#doing-229)
+ [Printing (3/29)](#printing--3-29-)
+ [Inspecting (4/29)](#inspecting--4-29-)
+ [Basic Types: Numbers (5/29)](#basic-types--numbers--5-29-)
+ [Basic Types: Characters (6/29)](#basic-types--characters--6-29-)
+ [Basic Types: Strings (7/29)](#basic-types--strings--7-29-)
+ [Basic Types: Symbols (8/29)](#basic-types--symbols--8-29-)
+ [Basic Types: Array (9/29)](#basic-types--array--9-29-)
+ [Basic Types: Dynamic Array (10/29)](#basic-types--dynamic-array--10-29-)
+ [Message syntax: Unary messages (11/29)](#message-syntax--unary-messages--11-29-)
+ [Message syntax: Binary messages (12/29)](#message-syntax--binary-messages--12-29-)
+ [Message syntax: Keyword messages (13/29)](#message-syntax--keyword-messages--13-29-)
+ [Message syntax: Execution order (14/29)](#message-syntax--execution-order--14-29-)
+ [Message syntax: Parentheses (15/29)](#message-syntax--parentheses--15-29-)
+ [Mathematical Precendence (16/29)](#mathematical-precendence--16-29-)
+ [Message syntax: cascade (17/29)](#message-syntax--cascade--17-29-)
+ [LOST? (18/29)](#lost---18-29-)
+ [Blocks (19/29)](#blocks--19-29-)
+ [Block assignation (20/29)](#block-assignation--20-29-)
+ [Conditionals (21/29)](#conditionals--21-29-)
+ [Loops (22/29)](#loops--22-29-)
+ [Iterators (23/29)](#iterators--23-29-)
+ [Instantiation (24/29)](#instantiation--24-29-)
+ [Reflection (25/29)](#reflection--25-29-)
+ [Reflection Continued (26/29)](#reflection-continued--26-29-)
+ [Pharo environment (27/29)](#pharo-environment--27-29-)
+ [Debugger (28/29)](#debugger--28-29-)
+ [Tutorial Done (29/29)](#tutorial-done--29-29-)

---
### Welcome (1/29)

Hello! I'm Professor Stef.

You must want me to help you learn Pharo.

So let's go to the first lesson. Select the text below, right-click and choose 'Do it'

```smalltalk
ProfStef next.
```
---
### Doing (2/29)
Cool! (I like to say Cooool :) ). You've just executed a Pharo expression. More precisely, you sent the message 'next' to ProfStef class (it's me!).

Note you can run this tutorial again by evaluating: `ProfStef go`. 
`ProfStef previous` returns to the previous lesson.

You can also Do it using the keyboard shortcut `Ctrl + D` (or `Cmd + D` on MacOS). 

Try to evaluate these expressions:

```smalltalk
StPlayground open. "Opens Pharo code playground"
```
```smalltalk
SmalltalkImage current aboutThisSystem. "Opens 'About Pharo' page"
```

"Then go to the next lesson:"

```smalltalk
ProfStef next.
```
---
### Printing (3/29)
Now you're a Do it master! Let's talk about printing. It's a Do it which prints the result next to the expression you've selected.
For example, select the text below, open the menu and click on 'Print it':

```smalltalk
1 + 2. "Output: 3"
```

You've seen the keyboard keys next to the 'Print it'? It indicates the Ctrl- (or Cmd-) shortcut to execute this command.

Try `Ctrl + P` (or `Cmd + P`) on the following expressions:

```smalltalk
Date today. "Output: 23 January 2022"
```

```smalltalk
Time now.  "Output: 3:35:27.581 pm"
```

The result is selected, so you can erase it using the backspace key. Try it!

```smalltalk
SmalltalkImage current datedVersion. "Output: 'Pharo10.0.0 of 20 January 2022'"
```

```smalltalk
ProfStef next.
```
---
### Inspecting (4/29)
Now you're a Do it and Print it master! Let's talk about inspecting. It's a Do it which opens an Inspector on the result of evaluating the expression you've selected. 
The Inspector is a tool that allows you to have a look inside an object.

For example, select the text below, open the menu and click on 'Inspect it':"

```smalltalk
1 / 2.
```

You've seen the keyboard keys next to the 'Inspect it'? It indicates the Ctrl- (or Cmd-) shortcut to execute this command.

Try `Ctrl + I` (or `Cmd + I`) on the following expressions:

```smalltalk
DateAndTime today.
```
```smalltalk
Float pi.
```
```smalltalk
SystemVersion current.
```
![Inspecting System Version](/img/inspecting.jpg)
```smalltalk
ProfStef next.
```
---
### Basic Types: Numbers (5/29)
You now know how to execute Pharo code. 

Now let's talk about basic objects.

1, 2, 100, 2/3 ... are Numbers, and respond to many messages evaluating mathematical expressions.

Evaluate these ones:
```smalltalk
2. "Output: 2"
```
```smalltalk
20 factorial. "Output: 2432902008176640000"
```
```smalltalk
1000 factorial / 999 factorial. "Output: 1000"
```
```smalltalk 
(1/3). "Output: (1/3)"
```
```smalltalk
(1/3) + (4/5). "Output: (17/15)"
```
```smalltalk
(1/3) asFloat. "Output: 0.3333333333333333"
```
```smalltalk
1 class. "Output: SmallInteger"
```
```smalltalk
1 class maxVal class. "Output: SmallInteger"
```
```smalltalk
(1 class maxVal + 1) class. "Output: LargePositiveInteger"
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Characters (6/29)
A Character can be instantiated using `$` operator:
```smalltalk
$A. "Output: $A"
```
```smalltalk
$A class. "Output: Character"
```
```smalltalk
$B charCode. "Output: 66"
```
```smalltalk
Character cr. "Output: Character cr"
```
```smalltalk
Character space. "Output: Character space"
```
You can print all 256 characters of the ASCII extended set:
```smalltalk
Character allByteCharacters.
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Strings (7/29)
A String is a collection of characters. Use single quotes to create a String object. Print these expressions:
```smalltalk
'ProfStef'. "Output: 'ProfStef'"
```
```smalltalk
'ProfStef' size. "Output: 8"
```
```smalltalk
'abc' asUppercase. "Output: 'ABC'"
```
```smalltalk
'Hello World' reverse. "Output: 'dlroW olleH'"
```
You can access each character using at: message
```smalltalk
'ProfStef' at: 1. "Output: $P"
```
String concatenation uses the comma operator:
```smalltalk
'ProfStef', ' is cool'. "Output: 'ProfStef is cool'"
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Symbols (8/29)
A Symbol is a String which is guaranteed to be globally unique. 

There is one and only one Symbol `#ProfStef`. There may be several 'ProfStef' String objects.

(Message == returns true if the two objects are the SAME)
```smalltalk
'ProfStef' asSymbol. "Output: #ProfStef"
```
```smalltalk
#ProfStef asString. "Output: 'ProfStef'"
```
```smalltalk
(2 asString) == (2 asString). "Output: false"
```
```smalltalk
(2 asString) asSymbol == (2 asString) asSymbol. "Output: true"
```
```smalltalk
(Smalltalk globals at: #ProfStef) next. "Same as ProfStef next."
```
---
### Basic Types: Array (9/29)
Literal arrays are created at parse time and are read-only:

```smalltalk
#(1 2 3). "Output: #(1 2 3)"
```
```smalltalk
#(1 2 3 #(4 5 6)) size. "Output: 4"
```
```smalltalk
#(1 2 4) isEmpty. "Output: false"
```
```smalltalk
#(1 2 3) first. "Output: 1"
```
```smalltalk
#('hello' 'World') at: 2. "Output: 'World'"
```
You can modify a copy
```smalltalk
#('hello' 'World') copy at: 2 put: 'Pharo'; yourself. "Output: #('hello' 'Pharo')"
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Dynamic Array (10/29)
Dynamic Arrays are created at execution time:
```smalltalk
{ (2+3) . (6*6) }. "Output: #(5 36)"
```
```smalltalk
{ (2+3) . (6*6) . 'hello', ' Stef'} size. "Output: 3, because the array is #(5 36 'hello Stef')"
```
```smalltalk
{ ProfStef } first next. "Same as ProfStef next."
```
---
### Message syntax: Unary messages (11/29)
Messages are sent to objects. There are three types of message: unary, binary and keyword.

Unary messages have the following form:
    `anObject aMessage`

You've already sent unary messages. For example:

```smalltalk
1 class. "Output: SmallInteger"
```
```smalltalk
false not. "Output: true"
```
```smalltalk
Time now. "Output: 4:07:28.931 pm"
```
```smalltalk
Date today. "Output: 23 January 2022"
```
```smalltalk
Float pi. "Output: 3.141592653589793"
```
And of course:
```smalltalk
ProfStef next.
```
---
### Message syntax: Binary messages (12/29)
Binary messages have the following form:
    `anObject + anotherObject`
```smalltalk
3 * 2. 6
```
```smalltalk
Date today + 3 weeks. "Output: a Timespan(2022-02-13T00:00:00-05:00D1:00:00:00)"
```
```smalltalk
false | false. "Output: false"
```
```smalltalk
true & true. "Output: true"
```
```smalltalk
true & false. "Output: false"
```
```smalltalk
10 @ 100. "Output: (10@100)"
```
```smalltalk
10 <= 12. "Output: true"
```
```smalltalk
'ab', 'cd'. "Output: 'abcd'"
```
```smalltalk
Date today < Date yesterday. "Output: false"
```
```smalltalk
ProfStef next.
```
---
### Message syntax: Keyword messages (13/29)
Keyword messages are messages with arguments. They have the following form:
    `anObject akey: anotherObject akey2: anotherObject2`
```smalltalk
4 between: 0 and: 10. "Output: true"
```
"The message is between:and: sent to the Number 4"
```smalltalk
1 max: 3. "Output: 3"
```
```smalltalk
Color r:1 g:0 b:0. "Output: Color red"
```
The message is `r:g:b:` implemented on class Color. Note you can also write
```smalltalk
Color
	r:1
	g:1
	b:0. "Output: Color yellow"
```
```smalltalk
ProfStef perform: #next. "Same as ProfStef next."
```
### Message syntax: Execution order (14/29)
Unary messages are executed first, then binary messages and finally keyword messages:
    `Unary > Binary > Keywords`
```smalltalk
2 + 3 squared. "Output: 11"
```
```smalltalk
2 raisedTo: 3 + 2. "Output: 32"
```
```smalltalk
(0@0) class. "Output: Point"
```
```smalltalk
0@0 corner: 100@200. "Output: (0@0) corner: (100@200)"
```
```smalltalk
(0@0 corner: 100@200) class. "Output: Rectangle"
```
Between messages of similar precedence, expressions are executed from left to right
```smalltalk
-3 abs negated reciprocal. "Output: (-1/3)"
```
```smalltalk
ProfStef next.
```
---
### Message syntax: Parentheses (15/29)
Use parentheses to change order of evaluation
```smalltalk
(2 + 3) squared. "Output: 25"
```
```smalltalk
(2 raisedTo: 3) + 2. "Output: 10"
```
```smalltalk
(0@0 extent: 100@200) bottomRight. "Output: (100@200)"
```
```smalltalk
ProfStef next.
```
---
### Mathematical Precendence (16/29)
Traditional precedence rules from mathematics do not apply in Pharo.
```smalltalk
2 * 10 + 2. "Output: 22"
```
Here the message * is sent to 2, which answers 20, then 20 receive the message +

Remember that all messages always follow a simple left-to-right precedence rule, * without exceptions *.
```smalltalk
2 + 2 * 10. "Output: 40"
```
```smalltalk
2 + (2 * 10). "Output: 22"
```
```smalltalk
8 - 5 / 2. "Output: (3/2)"
```
```smalltalk
(8 - 5) / 2. "Output: (3/2)"
```
```smalltalk
8 - (5 / 2). "Output: (11/2)"
```
```smalltalk
ProfStef next.
```
---
### Message syntax: cascade (17/29)
`;` is the cascade operator. It's useful to send message to the SAME receiver.

Open a Transcript (console):
```smalltalk
Transcript open.
```
"Then:"
```smalltalk
Transcript show: 'hello'.
Transcript show: 'Pharo'.
Transcript cr.
```
"is equivalent to:"
```smalltalk
Transcript 
	   show: 'hello';
	   show: 'Pharo' ;
	   cr.
```
Try to go to the next lesson with a cascade of two 'next' messages:
```smalltalk
ProfStef next; next.
```
---
### LOST? (18/29)
Hey, you should not be here!! 

Go back and use a cascade!
```smalltalk
ProfStef previous.
```
---
### Blocks (19/29)
Cascade is cool! Let's talk about blocks.

Blocks are anonymous methods that can be stored into variables and executed on demand.

Blocks are delimited by square brackets: `[]`
```smalltalk
[StPlayground open].
```
does not open a Browser because the block is not executed.

Here is a block that adds 2 to its argument (its argument is named x):
```smalltalk
[:x | x+2].
```
We can execute a block by sending it value messages.
```smalltalk
[:x | x+2] value: 5. "Output: 7"
```
```smalltalk
[StPlayground open] value. "Opens Pharo playground"
```
```smalltalk
[:x | x+2] value: 10. "Output: 12"
```
```smalltalk
[:x :y| x + y] value:3 value:5. "Output: 8"
```
```smalltalk
[ProfStef next] value. "Same as ProfStef next."
```
---
### Block assignation (20/29)
Blocks can be assigned to a variable then executed later.

Note that `|b|` is the declaration of a variable named 'b' and that ':=' assigns a value to a variable.

Select the three lines then Print it:
```smalltalk
|b|
b := [:x | x+2].
b value: 12. "Output: 14"
```
```smalltalk
ProfStef next.
```
---
### Conditionals (21/29)
Conditionals are just messages sent to Boolean objects
```smalltalk
1 < 2
  ifTrue: [100]
  ifFalse: [42]. "Output: 100"
```
Here the message is `ifTrue:ifFalse:`

Try this:
```smalltalk
Transcript open.

3 > 10 
	ifTrue: [Transcript show: 'Maybe there''s a bug ....']
	ifFalse: [Transcript show: 'No: 3 is less than 10']. "Prints 'No: 3 is less than 10' on the Transcript"
```
```smalltalk
3 = 3 ifTrue: [ProfStef next]. "Same as ProfStef next."
```
---
### Loops (22/29)
Loops are high-level collection iterators, implemented as regular methods.

Basic loops:\
&nbsp;&nbsp;`to:do:`\
&nbsp;&nbsp;`to:by:do:`

```smalltalk
1 to: 100 do: [:i | Transcript show: i asString; cr]. "Prints number 1-100 (inclusive) with a newline(cr) after each number on the Transcript"
```
```smalltalk
1 to: 100 by: 3 do: [:i | Transcript show: i asString; cr]. "Prints number 1, 4, 7, 10, ... 100 (inclusive) with a newline(cr) after each number on the Transcript"
```
```smalltalk
100 to: 0 by: -2 do: [:i | Transcript show: i asString; cr]. "Prints number 100, 98, 96, 94, ... 0 (inclusive) with a newline(cr) after each number on the Transcript"
```
```smalltalk
1 to: 1 do: [:i | ProfStef next]. "Same as ProfStef next." 
```
---
### Iterators (23/29)
The message do: is sent to a collection of objects (Array, Set, OrderedCollection), evaluating the block for each element.

Here we want to print all the numbers on the Transcript (a console)
```smalltalk
#(11 38 3 -2 10) do: [:each |
     Transcript show: each printString; cr].
```
Some other really nice iterators
```smalltalk
#(11 38 3 -2 10) collect: [:each | each abs]. "Output: #(11 38 3 2 10)"
```
```smalltalk
#(11 38 3 -2 10) collect: [:each | each odd]. "Output: #(true false true false false)"
```
```smalltalk
#(11 38 3 -2 10) select: [:each | each odd]. "Output: #(11 3)"
```
```smalltalk
#(11 38 3 -2 10) select: [:each | each > 10]. "Output: #(11 38)"
```
```smalltalk
#(11 38 3 -2 10) reject: [:each | each > 10]. "Output: #(3 -2 10)"
```
```smalltalk
#(11 38 3 -2 10) 
     do: [:each | Transcript show: each printString]
     separatedBy: [Transcript show: '.']. "Output: #(11 38 3 -2 10)"
```
```smalltalk
ProfStef allInstances do: [:aPharoTutorial | aPharoTutorial next]. "Same as ProfStef next."
```
---
### Instantiation (24/29)
Objects are instances of their class. Usually, we send the message #new to a class for creating an instance of this class.

The message #allInstances sent to a class answers an Array with all instances of this class.

For example, let's look at how many instances of SimpleButtonMorph exist. Please use only Do it or Print it on this page, not Inspect it.
```smalltalk
SimpleButtonMorph allInstances size. "Output: 0"
```
Now create a new instance of it:
```smalltalk
SimpleButtonMorph new
	label: 'A nice button';
	openCenteredInWorld.
```
See the button centered on the world? The list of all instances should contains one more instance:
```smalltalk
SimpleButtonMorph allInstances size. "Output: 1"
```
Let's play with it:
```smalltalk
SimpleButtonMorph allInstances last 
	label: 'ProfStef is cooooool !';
	color: Color cyan.
```
Let's delete it and ask the system to clean the memory:
```smalltalk
SimpleButtonMorph allInstances last delete.
Smalltalk garbageCollect.
SimpleButtonMorph allInstances size.
```
Click on the button to go to next lesson:
```smalltalk
SimpleButtonMorph new
	label: 'Go to next lesson';
	target: [ProfStef next. 
			   SimpleButtonMorph allInstances last delete];
	actionSelector: #value;
	openCenteredInWorld.
```
![Instantiation](/img/instantiation.jpg)
---
### Reflection (25/29)
You can inspect and change the system at runtime.

Take a look at method `#ifFalse:ifTrue:` source code of class True:
```smalltalk
(True>>#ifFalse:ifTrue:) sourceCode.
```
Or just its comment:
```smalltalk
(True>>#ifFalse:ifTrue:) comment.
```
Here's all the methods I implement:
```smalltalk
ProfStef selectors.
```
Now let's create a new method to go to the next lesson:
```smalltalk
ProfStef class compile:'goToNextLesson
  self next'.
```
Wow! I can't wait to use my new method!
```smalltalk
ProfStef goToNextLesson.
```
---
### Reflection Continued (26/29)
So cool, isn't it? Before going further, let's remove this method:
```smalltalk
ProfStef respondsTo: #goToNextLesson.

ProfStef class removeSelector: #goToNextLesson.

ProfStef respondsTo: #goToNextLesson.
```
Then move forward:
```smalltalk
ProfStef default executeMethod: (ProfStef lookupSelector:#next). "Same as ProfStef next."
```
### Pharo environment (27/29)
Pharo is full of objects. There are windows, text, numbers, dates, colors, points and much more. You can interact with objects in a much more direct way than is possible with other programming languages.

Every object understands the message 'inspect'. As a result, you get an Inspector window that shows details about the object.
```smalltalk
Date today inspect.
````
This shows that the date object consists of a point in time (start) and a duration (one day long).
```smalltalk
ProfStef inspect.
```
You see, ProfStef class has a lot of objects. Let's take a look at my code:
```smalltalk
ProfStef browse.
```
![ProfStef](/img/ProfStef.jpg)
```smalltalk
ProfStef next.
```
---
### Debugger (28/29)
The Debugger may be the most famous tool of Smalltalk environments. It will open as soon as an unmanaged Exception occurs. 

The following code will open the debugger on the message stack, select `PharoSyntaxTutorial>>divideTwoByZero`
```smalltalk
PharoSyntaxTutorial new divideTwoByZero.
```
![Debug](/img/debug.jpg)
---
### Tutorial Done (29/29)
This tutorial is done. Enjoy programming with Pharo. 

Don't forget to read 'Pharo By Example' found here:  

	https://books.pharo.org/updated-pharo-by-example

You can run this tutorial again by evaluating:
```smalltalk
ProfStef go.
```
Do you want to create your own interactive tutorial with ProfStef? That's very easy!! How? There's a ProfStef interactive tutorial for that :D
Just evaluate the following code:
```smalltalk
ProfStef goOn: HowToMakeYourOwnTutorial
```
See you soon!

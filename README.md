# ProfStef-README
Text version of Pharo ProfStef lessons

---
### Welcome (1/29)

"Hello! I'm Professor Stef.

You must want me to help you learn Pharo.

So let's go to the first lesson. Select the text below, right-click and choose 'Do it'"

```smalltalk
ProfStef next.
```
---
### Doing (2/29)
"Cool! (I like to say Cooool :) ). You've just executed a Pharo expression. More precisely, you sent the message 'next' to ProfStef class (it's me!).

Note you can run this tutorial again by evaluating: 'ProfStef go'. 
'ProfStef previous' returns to the previous lesson.

You can also Do it using the keyboard shortcut 'Ctrl + D' (or 'Cmd + D' on MacOS). 

Try to evaluate these expressions:"

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
"Now you're a Do it master! Let's talk about printing. It's a Do it which prints the result next to the expression you've selected.
For example, select the text below, open the menu and click on 'Print it':"

```smalltalk
1 + 2. "Output: 3"
```

"You've seen the keyboard keys next to the 'Print it'? It indicates the Ctrl- (or Cmd-) shortcut to execute this command.

Try 'Ctrl + P' (or 'Cmd + P') on the following expressions:"

```smalltalk
Date today. "Output: 23 January 2022"
```

```smalltalk
Time now.  "Output: 3:35:27.581 pm"
```

"The result is selected, so you can erase it using the backspace key. Try it!"

```smalltalk
SmalltalkImage current datedVersion. "Output: 'Pharo10.0.0 of 20 January 2022'"
```

```smalltalk
ProfStef next.
```
---
### Inspecting (4/29)
"Now you're a Do it and Print it master! Let's talk about inspecting. It's a Do it which opens an Inspector on the result of evaluating the expression you've selected. 
The Inspector is a tool that allows you to have a look inside an object.

For example, select the text below, open the menu and click on 'Inspect it':"

```smalltalk
1 / 2.
```

"You've seen the keyboard keys next to the 'Inspect it'? It indicates the Ctrl- (or Cmd-) shortcut to execute this command.

Try 'Ctrl + I' (or 'Cmd + I') on the following expressions:"

```smalltalk
DateAndTime today.
```
```smalltalk
Float pi.
```
```smalltalk
SystemVersion current.
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Numbers (5/29)
"You now know how to execute Pharo code. 

Now let's talk about basic objects.

1, 2, 100, 2/3 ... are Numbers, and respond to many messages evaluating mathematical expressions.
Evaluate these ones:"
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
"A Character can be instantiated using $ operator:"
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
"You can print all 256 characters of the ASCII extended set:"
```smalltalk
Character allByteCharacters.
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Strings (7/29)
"A String is a collection of characters. Use single quotes to create a String object. Print these expressions:"
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
"You can access each character using at: message"
```smalltalk
'ProfStef' at: 1. "Output: $P"
```
"String concatenation uses the comma operator:"
```smalltalk
'ProfStef', ' is cool'. "Output: 'ProfStef is cool'"
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Symbols (8/29)
"A Symbol is a String which is guaranteed to be globally unique. 

There is one and only one Symbol #ProfStef. There may be several 'ProfStef' String objects.

(Message == returns true if the two objects are the SAME)"
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
"Literal arrays are created at parse time and are read-only:"

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
"You can modify a copy"
```smalltalk
#('hello' 'World') copy at: 2 put: 'Pharo'; yourself. "Output: #('hello' 'Pharo')"
```
```smalltalk
ProfStef next.
```
---
### Basic Types: Dynamic Array (10/29)
"Dynamic Arrays are created at execution time:"
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
"Messages are sent to objects. There are three types of message: unary, binary and keyword.

Unary messages have the following form:
    anObject aMessage 

You've already sent unary messages. For example:"

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
"And of course:"
```smalltalk
ProfStef next.
```
---
### Message syntax: Binary messages (12/29)
"Binary messages have the following form:
    anObject + anotherObject"
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
"Keyword messages are messages with arguments. They have the following form:
    anObject akey: anotherObject akey2: anotherObject2"
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
"The message is r:g::b: implemented on class Color. Note you can also write"
```smalltalk
Color
	r:1
	g:1
	b:0. "Output: Color yellow"
```
```smalltalk
ProfStef perform: #next. "Same as ProfStef next."
```

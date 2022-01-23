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
Character allByteCharacters. "Output: Characters Not supported on README"
```
```smalltalk
ProfStef next.
```
---

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

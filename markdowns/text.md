# Text modifiers

Now, let's see all the text modifiers
* Reset : code 0
* Bold : code 1
* Dim : code 2
* Underlined : code 4
* Blink : code 5
* Highlighted : code 7
* Invisible : code 8

# Let's start

* Memory: empty
* Cursor: first cell
* Input: any

# Process

* For each effect
  * Print escape sequence
  * Print effect name
* Loop

# Code
```
+++++++++[->+++>++++++++++>+++++>++++++++++++>+<<<<<] generate escape sequence
>>+>+++>+>+>>++++++++[-<++++++>]<                       ** part 2 **
+<<<<<.>.>>>>.<<.>>>+++++++++++[->++++++>++           for 1: print Bold
++++++++<<]>.>+.---.--------.<<<<.                      ** part 2 **
<<<<.>.>.>.                                           reset style
>>+<<<<<.>.>>>>.<<.>>>>++.>+++++.++++.<<<<.           for 2: print Dim
<<<<.>.>.>.                                           reset style
>>++<<<<<.>.>>>>.<<.>>>++++[->++++<]>+.>+.---------   for 4: print
-.+.+++++++++++++.------.---.+++++.---------.-.<<<<.     Underlined
<<<<.>.>.>.                                           reset style
>>+<<<<<.>.>>>>.<<.>>>++++[->-----<]>+.>              for 5: print Blink
++++++++.---.+++++.---.<<<<.                            ** part 2 **
<<<<.>.>.>.                                           reset style
>>++<<<<<.>.>>>>.<<.>>>>++++++.>--.--.+.++++          for 7: print Highlight
.---.--.+.++++++++++++.<<<<                             ** part 2 **.
<<<<.>.>.>.                                           reset style
>>+<<<<<.>.>>>>.<<.>>>>+.>------.++++++++.            for 8: print Invisible
-------------.++++++++++.----------.------              ** part 2 **
-.++++++++++.-------.<<<<.                              ** part 3 **
<<<<.>.>.>.                                           reset style
```


# ANSI/VT100 control sequences

So, what the hell is this thing?

Using a special character named `<Esc>`, it is possible to add some format codes that will modify the console text format options.

The ANSI/VT100 commands are the same on any terminal, the only thing that may differ is the way to obtain the Escape char. Let's keep it short and simple : on Bash, it's ASCII code 27.

So, let's just add a `27` char and then play with control sequences.

# Let's start

* Memory: empty
* Cursor: first cell
* Input: any text

# Process

* generate 9
* use this 9 to generate 27, 90, 45 and 108
* change this to 27, 91, 49 and 109
  * this is <Esc>[1m chars
* print those chars : style is bold !!!
* read a char and print while it's not null
* print ASCII code 10 (newline)
* change 49 to 48 and re-print those chars
* style reset to normal

# Code
```
+++++++++[->+++>++++++++++  generate the desired numbers
>+++++>++++++++++++<<<<]      ** part 2 **
>>+>++++>+<<<[.>]           print escape control sequence
,[.,                        print all chars from input]
++++++++++.[-]              print newline
<<-<<[.>]                   print reset escape control sequence
```

# Minified version
```
+++++++++[->+++>++++++++++>+++++>++++++++++++<<<<]>>+>++++>+<<<[.>],[.,]++++++++++.[-]<<-<<[.>]
```

# Final state

* Memory: 0 27 91 48 109 0 0 0 0 0 0
* Cursor: after 109
* Input: empty (read)
* Output: funky bold text

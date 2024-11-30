"The world looks pretty from the skyline  
God it feels good to be on cloud nine  
Heaven is all in your head"
<sup>Last Dinosaurs - Afterlife</sup>

<font color="#ff0000">Red</font> = <font color="#ff0000">Important to Remember!</font>
<font color="#ffff00">Yellow</font> = <font color="#ffff00">Must Read!</font>
<font color="#00b050">Green</font> = <font color="#00b050">Examples</font>
# What is a Program/Software Bug? 

<font color="#ff0000">SoftwareBug:</font>

<font color="#ffff00">An error, flaw, failure, or fault in a computer program or system that causes it to produce an incorrect or unexpected result, or to behave in unintended ways.</font>

A program that contains a large number of bugs, and/or bugs that seriously interfere with its functionality, is said to be buggy. (I mean...Pretty Straightforward)
#### Reason for Bugs to Arise

<font color="#ffff00">Most of them Arise from mistakes and errors made by people in either a program's source  </font>
<font color="#ffff00">code or its design, or in frameworks and operating systems used by such programs, and a  </font>
<font color="#ffff00">few are caused by compilers producing incorrect code.</font>

# The Debugging Process

<font color="#ff0000">Code Debugging:</font>

Is <font color="#ffff00">introduced to a computer program to test for errors or to help determine the cause of an error.</font>

can be as simple as a print command to print the value of a variable at certain points of a program.

# What is a Breakpoint?

<font color="#ffff00">A Breakpoint is an intentional stopping or pausing  place in a program, put in place for debugging purposes.</font> Basically a Pause.

# Debug Mode

#### <font color="#ff0000">Cheat Codes; Debug Mode</font>

Common cheat codes like invincibility, wall clipping, double damage etc. is<font color="#ffff00"> introduced as debug code to allow the programmers and/or testers to skip hindrances that would prevent them from rapidly getting to parts of the game that needed to be tested.</font>

Some games do leave in the cheat codes to enhance the player experience but its best practice to remove the debugging code as it slows the production by some margin.

# Variable Watch

<font color="#ffff00">The process of inspecting a value of a variable while the program is executing in debug mode.</font>

To inspect a variable, you can either hover your mouse over the variable or use quickwatch.

Modern Compilers include a <font color="#ffff00">watch window</font> so that <font color="#ffff00">you can add variables to continually inspect, and these variables will be updated as you step through your program.</font>

# Different Errors that may occur in the Program

We all make mistakes, even the professionals! This makes debugging an application and finding those mistakes an important and integral part of programming.

The Errors are categorized as such:

- <font color="#ff0000">Compilation Errors</font>
- <font color="#ff0000">Run-Time Errors</font>
- <font color="#ff0000">Logic Errors</font>

### <font color="#ff0000">Compilation Error</font>

Compiler Errors <font color="#ffff00">prevent the program from running</font>. Which is a problem that Unity discovers when compiling your C# code.

The <font color="#ffff00">compiler will attempt to interpret the C# code turning it into common intermediate language(Human Language) later converted into Machine Language(Hexadecimals/Binary)</font> that can run on your computer

Common Errors that result in a Compiler Error includes:

<font color="#ff0000">Misspellings:</font>

<font color="#ffff00">Misspelling a C# Keyword </font>

---
<font color="#ff0000">Capitalisation:</font>

Since <font color="#ffff00">C# is a Case-Sensitive Language</font>, variable, Variable and variAble are completely different

---
<font color="#ff0000">Missing semicolons:</font>

A Sentence should naturally end in a punctuation right?
 <font color="#ffff00">C# is the same but with Semi-Colons! Leaving it out often causes an error on the next line.</font>

---
<font color="#ff0000">Missing punctuations and block statements:</font>

<font color="#ffff00">Missing Brackets, Braces(Curly Brackets), Period(Full Stops), Quotation marks and Block Statements or use of Else-If without using If statement first.</font>

---
### <font color="#ff0000">The Attachment and Removal of Scripts</font>

<font color="#ffff00">Happens only when we attempt to attach a script to a GameObject. When the name of a script doesn't match with the class that we are defining in the script we've created.</font>

<font color="#00b050">So if you created a file named Chopper, in the script it would be shown as </font>
<font color="#00b050">Chopper : MonoBehaviour</font>

### <font color="#ff0000">Run-Time Errors</font> (Kinda Explanatory from the name right?)

These errors are errors that only occurs when Unity is actually trying to play the  
project. <font color="#ffff00">occurring when your project attempts an operation that is impossible to carry out.</font>

Occurring when: 

<font color="#ffff00">we have typed everything correctly with no compilation errors yet something is not correct when  </font>
<font color="#ffff00">the code actually runs.</font>

<font color="#00b050">An Example would be using divide by zero:</font>

<font color="#00b050">If you have this formula => Speed = Distance/Time</font>

<font color="#00b050">Lets say time is 0, Division operation fails and causes a run-time error. </font>
<font color="#00b050">In order to be detected the program must run and if the value is more than 0 there be no error at all!</font>

### <font color="#ff0000">Logic Error </font>(Making it Make Sense)

This error<font color="#ffff00"> prevents the program from doing what you need to do/your intended purpose of code.</font>

This means the code may compile and run without error, resulting in an operation that may produce an unexpected result.

<font color="#00b050">For Example:</font>

<font color="#00b050">You might have a variable named FirstName that is initially set to a blank  string. </font>
<font color="#00b050">Later in your program, you might concatenate FirstName with another variable named LastName to display a full name. If you forgot to assign a value to FirstName, only the last name would be displayed, not the full name as you intended.</font>

Logic errors are one of the hardest errors out of the 3 to find and fix!
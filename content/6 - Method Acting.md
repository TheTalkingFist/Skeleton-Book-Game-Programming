
"Visions move all the time, don't get left behind  
This is love, this is faith, this is my design"  
<sup>Last Dinosaurs - Time & Place</sup>

<font color="#ff0000">Red</font> = <font color="#ff0000">Important to Remember!</font>
<font color="#ffff00">Yellow</font> = <font color="#ffff00">Must Read!</font>
<font color="#00b050">Green</font> = <font color="#00b050">Examples</font>
# What is a Method?

<font color="#ff0000">Method Definition: </font>

 The building block of object-oriented programming. It combines related code  
together and makes program easier.

<font color="#ffff00">A method is a code block that contains a series of statements. </font>

<font color="#ffff00">A program causes the statements to be executed by calling the method and specifying any required method arguments. </font>

<font color="#ffff00">In C#, every executed instruction is performed in the context of a method.</font>

**Unity**:

When Unity creates a class it automatically added in void Start() and void  
Update() to the body of the class. 

These two methods are called ***entry points***.

---

# MonoBehaviour Class

This specific class is a class that has several functions!

The several functions includes the Start() and Update() functions, **the two are called upon based on events that happen when your game is running.**

MonoBehaviour scripts are almost always attached to GameObjects in a  
scene, their attached scripts are enabled at the same time they are loaded when you hit  
play.
# <font color="#ff0000">Start()</font>

<font color="#ffff00">Unity calls the Start() method on the first frame where a script is enabled for the first  </font>
<font color="#ffff00"> time, before the Update methods are called for the first time. </font>

<font color="#ffff00">Start() is primarily used to set up variables or perform logic that needs to happen before </font>
<font color="#ffff00">Update() runs for the first time.</font>
# What does a method look like in general?

<font color="#00b050">Example:</font>
```
<Access Modifier> <Return type> <Method Name> (Parameter List)
{
  Method Body
}
```
---
<font color="#ff0000">Access Specifier:</font>

● <font color="#ffff00">This determines the visibility of a variable or a method from another class.  </font>
<font color="#ffff00">Return Type</font>

---
<font color="#ff0000">Return Type:</font>

● <font color="#ffff00">A method may return a value. The return type is the data type of the value the method  </font>
<font color="#ffff00">returns. If the method is not returning any values, then the return type is void.</font>

---
<font color="#ff0000">Method Name:</font>

● <font color="#ffff00">Method name is a unique identifier and it is case sensitive. It cannot be same as any  </font>
<font color="#ffff00">other identifier declared in the class.  </font>
 

---
<font color="#ff0000">Parameter List:</font>

● <font color="#ffff00">Enclosed between parentheses, the parameters are used to pass and receive data from  </font>
<font color="#ffff00">a method. </font>

<font color="#ffff00">The parameter list refers to the type, order, and number of the parameters  </font>
<font color="#ffff00">of a method. Parameters are optional; that is, a method may contain no parameters.  </font>
<font color="#ffff00">Method Body  </font>

---
<font color="#ff0000">Method Body:</font>

● <font color="#ffff00">This contains the set of instructions needed to complete the required activity.</font>

---
<font color="#00b050">Example:</font>
```
public string Describe()
{
  return "This car is" + Color;
}
```

Public - Access Modifier
String - Return Data
Describe - Method Name
No Parameters Defined

---
# Method in a Class

<font color="#00b050">Example:</font>
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

namespace HelloWorldApplication
{
  public class HelloWorld:MonoBehaviour
  { 
    void Start()
    {
      /*My first unity script in C# */
      Debug.Log("Hello World");  
    }
  }
}
```
---
<font color="#ff0000">Using:</font>

<font color="#ffff00">Using, used to include the System name space within the program.</font>

Programs usually have multiple using statements

---
<font color="#ff0000">Namespace Declaration:</font>

<font color="#ffff00">A Namespace is a declaration of classes.</font>

Pulling from the <font color="#00b050">Example</font> above, HelloWorldApplication Namespace contains the Class HelloWorld

---
<font color="#ff0000">Class Declaration:</font>

In the<font color="#00b050"> Example</font>, HelloWorld has the data and methods  that the program would use.

Classes would usually have more than 1 method. <font color="#ff0000">The Methods define the behaviour of the class</font>.

---
<font color="#ff0000">Comments:</font>

If you comment lines, the <font color="#ffff00">commented lines will be ignored by the compiler</font>.

<font color="#ff0000">//</font> is used to <font color="#ffff00">Comment Single lines of codes.</font>

<font color="#ff0000">/**/</font> is used to <font color="#ffff00">Comment Many lines of code.</font>

---
<font color="#ff0000">Debug:</font>

Start(), specifies its behaviour with `Debug.Log("Hello World");` in the <font color="#00b050">Example</font>.

Debug <font color="#ffff00">Logs the message into the console in Unity</font>. 

Debug.Log can be used to print informational messages that helps Debug the application.

For example, you can print a message containing a GameObject.Name and information about the object's current state.

---

Next: [[7 - He's Scripting]]


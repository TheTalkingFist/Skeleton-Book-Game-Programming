"Think I'm on 11, but I'm on a 9  
Guess you don't really know me"
<sup>Sonic Frontiers OST - Undefeatable</sup>

<font color="#ff0000">Red</font> = <font color="#ff0000">Important to Remember!</font>
<font color="#ffff00">Yellow</font> = <font color="#ffff00">Must Read!</font>
<font color="#00b050">Green</font> = <font color="#00b050">Examples</font>
# Why We Create Scripts for our Game Objects

<font color="#ff0000">Reason for Scripting:</font>

Scripting <font color="#ffff00">tells our GameObjects how to behave</font>;
Scripts & Components are <font color="#ff0000">attached to the GameObjects</font>, it is how <font color="#ff0000">they interact with each other which results in the creation of the gameplay</font>.

---
<font color="#ff0000">GameObject and Script:</font>

A<font color="#ff0000"> script must be attached to a GameObject in the scene in order to be called by Unity.</font>

---
# A Script Structure

<font color="#00b050">Example:</font>

```
public class Demoscript: MonoBehaviour 
{
   // Variables
   // Functions
   // Classes

   // Use this initialization

    Void Start ()
    {
      
    }



    //Update is called once per frame
    
    Void Update ()
    {
    
    }
}
```
---
### What is in a Script?

A Script <font color="#ff0000">contains variables, functions and classes</font>.

<font color="#ffff00">Primarily comparing the objects and their current state values, based on the logic determining an outcome or resolution.</font>

---
<font color="#ff0000">Variables:</font>

<font color="#ffff00">Variables hold the values and references to objects</font>.

Analogy Example, Like a box that holds something for you to use.

---
<font color="#ff0000">Methods/Functions:</font>

<font color="#ffff00">These methods/functions are a Collection of codes that compare and manipulate the variables.</font>

Functions <font color="#ffff00">start with an Uppercase.</font>

<font color="#ffff00">We organise codes in functions in order to be easily reused in different parts of the program.</font>

---
<font color="#ff0000">Classes:</font>

Classes, <font color="#ffff00">a way to structure the code to wrap a collection of variables and functions together</font>. This <font color="#ffff00">Creates a template defining the properties of an object</font>.

---

# Variable Visibility, Is it Important?

To declare a variable we would usually declare atop the start() right? 

For example: 
<font color="#ff0000">Public</font> string Isburning;
<font color="#ff0000">Private</font> string Isnotburning;

These variables have the<font color="#ffff00"> visibility</font> of "<font color="#ff0000">Public</font>" or "<font color="#ff0000">Private</font>" followed by the return type and the name.

---
If we create a script for like for <font color="#00b050">Example</font>:

```
public class DemoScript : MonoBehaviour
{
    public light mylight;
    private light myotherlight

}
```

Coming back into Unity and assigning the script to a GameObject, we are able to see that the one declared as <font color="#ff0000">public </font><font color="#ffff00">can be seen in the inspector</font> whereas the one declared as <font color="#ff0000">private</font> <font color="#ffff00">can only be accessed within a particular script, within a particular class.</font>

If we make the other variable <font color="#ff0000">public</font>, it <font color="#ffff00">can then be accessed by other scripts and classes AND can be changed in the inspector panel</font>. Meaning that people can access and change the variable's value

---

# Methods

We know we are able to manipulate the variables using methods. And these are the number of methods that run automatically inside of Unity. <font color="#00b050">Shown Below:</font>

```
/*
    Awake()
    Start()
    Update()
    FixedUpdate()
    LateUpdate()
*/
```

---
<font color="#ff0000">Awake():</font>

<font color="#ffff00">Called only once when the GameObject with that component is instantiated.</font>

Some <font color="#ff0000">Things to note for Awake()</font>: 

○ If a GameObject is inactive, then it will not be  
called until it is made active.  

○ Awake is called even if the GameObject is active  
but the component is not enabled (with the little  
checkbox next to its name).  

○ Use Awake to initialize all the variables.


---
<font color="#ff0000">Start():</font>

Similar to Awake() But, <font color="#ffff00">will be called if a GameObject is active, but only if the component  is</font>
<font color="#ffff00">enabled.</font> 

---
<font color="#ff0000">Update():</font>

<font color="#ffff00">Called once per frame</font>.

Where we put code to <font color="#ffff00">define the logic of the game that runs forever/continously</font>, this <font color="#00b050">includes animations, AI and other parts of the game that has to be constantly updated</font>.

---
<font color="#ff0000">Awake():</font>

Runs <font color="#ffff00">before Start method is called.</font>


---
<font color="#ff0000">FixedUpdate():</font>

<font color="#ffff00">When you want to do Physics work. Runs on every fixed frame-rate, therefore it is independent on a device's framerate, and by proxy, performance capabilities.</font>

---
<font color="#ff0000">LateUpdate():</font>

Similar to update but, <font color="#ffff00">called right at the end of the frame, after Update has been called.</font>

---

# Exception Handling

Exceptions:

<font color="#ff0000">Errors that breaks the application execution unexpectedly.</font>

Exceptions you can expect in C# are:

- <font color="#ff0000"> Null Reference Exception</font>
- <font color="#ff0000"> Divide by Zero Exception</font>
-  <font color="#ff0000">Out of Memory Exception</font>
- <font color="#ff0000"> Index Out of Range Exception</font>
- <font color="#ff0000"> Input-Output Exception</font>

---
<font color="#ff0000">Null Reference Exception:</font>

Occurs <font color="#ffff00">when you try to access a variable without a referencing object  </font>
<font color="#ffff00">value during the runtime.</font>

---
<font color="#ff0000">Divide by Zero Exception:</font>

<font color="#ffff00">When you perform division, dividing a value by zero.</font>

---
<font color="#ff0000">Out of Memory Exception:</font>

<font color="#ffff00">Occurs if your memory has insufficient capacity to maintain the program execution.</font>

---
<font color="#ff0000">Index Out of Range Exception:</font>

<font color="#ffff00">Occurs if you try to access an array element or element of a collection with an invalid index value.</font>

---
<font color="#ff0000">Input-Output Exception:</font>

<font color="#ffff00">Occurs if you perform an input-output operation such as  reading or writing a file</font>. 
<font color="#ffff00">Any error which blocks the IO operation may trigger this exception.</font>

---
<font color="#00b050">Example:</font>

```
Using System;
Using UnityEngine;
Using System.Collections;

public class VFXGameController : MonoBehaviour
{
    void VFXControl()
    {
        try
        {
            //  The code that may result in an Exception
        }
        catch (Exception ex)
        {
            Debug.LogException(ex,this);
        }
    }
}
```

<font color="#ff0000">If there is an Exception, Unity shows it in the Console.</font>

Try-Catch Statements are used to handle exceptions with the Try block containing the codes that might cause an exception.

The catch block looks out for the aforementioned exception. 
For <font color="#00b050">Example</font>:
If the Exception is DivideByZeroException, since we know that is the potential issue, When the DivideByZeroException is thrown, <font color="#ffff00">the catch statement will  handle the exception by executing the codes in its block </font>

and if another type of Exception is thrown, the program will still stop, since we were only trying to  
catch a DivideByZeroException.

---
Logging Exceptions Using Debug.LogException Method: 

<font color="#ff0000">Debug.LogException:</font>

<font color="#ffff00">When we want to record a possible exception that we anticipate from a code block</font>

Similar to Debug.LogError but <font color="#ffff00">makes your code more readable and works  </font>
<font color="#ffff00">with Unity Cloud Diagnostics.</font>

---

Next: [[8 - Bug, Debug]]
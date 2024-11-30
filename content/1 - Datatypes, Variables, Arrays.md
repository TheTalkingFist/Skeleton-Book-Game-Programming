"Roll up for the Magical Mystery Tour, step right this way!"
<sup>The Beatles - Magical Mystery Tour</sup>


# Variables

A Datatype of a variable is the type of data the variable is (No way!), such as float, integer (int), string, etc.

You know these from Python, I hope you remember them.

In addition, C# provides 2 different types of variables: Static and Dynamic, which mainly decides when the computer knows about the variables' data.


Static initialisation is known at compile time, and is fixed as soon as the program is compiled (when our scripts are converted machine language, with 0s and 1s).

e.g: 
```
int a = 15;
```


Dynamic initialisation is known at runtime instead of compile time, meaning that the value of the variable is only known when you run the program. 

e.g:
```
double b = Math.Sqrt(225);
```
<sup>(For later info, "Math" is a class, and "Sqrt" is a method)</sup>


Constant declaration is for when you want a variable to be fixed, and never changed. We can do this with the ```const``` prefix.

```
const double PI = 10;
```


Strings have to be declared in double-quotes ("), while Char has to be declared in single-quotes(')

```
string greeting = "hi";
char end = '!'
```


The C# equivalent of Python's ```print``` is ```Debug.Log()``` (though apparently you can use ```print``` in C# too?)

---

# Datatypes

![[Pasted image 20241003111936.png]]

Value types look for the type of value, while Reference types look for the address of the data.


Look at these tables!
### Numeric Data Types (int, float, decimal, etc.)

![[Pasted image 20241003112256.png]]

These tables show the limits of some datatypes, which is important, as the computer works easier with smaller sizes.

The smaller the size, the quicker the computer works, the quicker the program can run. This makes these datatypes important for optimisation and speed.

The same principle applies to the decimal datatypes (float, double, decimal).


---

### Boolean

Boolean, well... You know already, right?


---

### Enumeration

Defined by ```enum```, Enumerations are basically the C# equivalent of lists.
<sup>(A/N: At least, I think so)</sup>

We use curly brackets to open and close enumerations, like this.

```
enum Days {Sun, Mon, Tues, Wed, Thurs, Fri, Sat}
```


We can call items from the list above, an example being
```
Days.Mon
```

With this, we can also get the position (index) of a certain item with
```
int WeekdayStart = (int)Days.Mon;
```



We can have parameters inside strings with curly brackets, though it will be a bit different.

```
Debug.Log("Monday: {0}", WeekdayStart);

Output:
Monday: 1
```

This takes the index of the WeekdayStart (Mon), and it will return its index.

(god help me im having trouble keeping up lmao)


---

# Class
![[Pasted image 20241003113520.png]]

Classes are... Pretty similar to Python (so far). These are just a group of variables that apply to a specific class.

---

# Other Important C\# Variable types in Unity

**Vector3** is for the positioning of the object in the 3rd dimension.

**Color** is the color of an object (No way!)

**GameObject** is the class of all entities in a Unity scene, and can contain any number of different components.

We could use the "**new**" operator to create a <u>brand new</u> particular object and allocate computer memory for that object. This is how you create objects in scripts.

```
gObj = new GameObject("Hit 3")
```

In the above example, we are creating a new game object `"Hit 3"` and storing it in the variable `gObj`.


---

## Casting

When you declare a type of a variable, you are unable to change the variable data to a type other than what was assigned to it when it was written.

```
int a;
a = "Hello World"
```
This will not work.

This is where casting comes in. Casting allows us to change the variable's datatype whenever we see fit.

```
double da = 1.21;
double db = 1.41;

result = (int)da + (int)db;
```
We have casted the 'int' type to variables 'da' and 'db', allowing the code to run.


Amazingly, we can also convert an string to a number!

```
int a = Convert.ToInt32("34")
```

There are different functions for converting strings to different types. Here they are.
![[Pasted image 20241003114835.png]]


---

## Arrays

Arrays are more like lists, in Python.
~~(i suppose i'll have to fix the enumeration later)~~


We can, for example, create an integer array called "intArray" with:
```
int[] intArray;
```

To declare an array, we will have to declare the datatype and place square brackets right after it.

Without the square brackets, "intArray" will just be a single, sad, normal integer.


To assign values, let's start with an example with a double array called "balance".
```
double[] balance;
```

We can then create a new game object as an array, that will store 10 values.
```
new double[10]
```


We can then store a double value into the first 'slot'.
```
balance[0] = 4500.0;
```


Alternatively, we can declare an array and assign values immediately.

For this example, we will use an integer array called "marks"

```
int[] marks = new int[5] {99, 98, 92, 97, 95};
```

FYI, the location of an element is called an index, just like in Python.


If we do
```
int[] score = marks;
```

then score will have all the properties of marks, like the items, the index of each item, its length, etc.



Again, if we do
```
int[] ages = new int[] {9, 8, 12, 64, 26}
```

where we did not declare the length of the list in the \[], this would mean that the array ```ages``` has no fixed length, and can be added to indefinitely.


We can also, of course, access elements inside the array. If we do this...
```
// Creating an array with size 10 //
int[] n = new int[10]; 

int i, j;

// We haven't 
for (i = 0; i < 10; i++)
{
	n[i] = i + 100;
}
```

---

That's just about it. Next up: Operators.

\- Mikhail


Next: [[2 - Doctor, Operator]]
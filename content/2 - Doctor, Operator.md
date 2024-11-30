"Well, the undertaker drew a heavy sigh, seeing no one else had come. And the bell was ringing in the village square, for the rabbits on the run."
<sup>Paul McCartney, Wings - Band On The Run</sup>

---

# Operators

Operators! We've seen these before and most of them you'll remember from Python. We continue the notebook with operators, of which there are three kinds:

- Arithmetic Operators
	- These are basically normal math functions. Add, subtract, divide, whatever.
- Assignment Operators
	- Kinda like arithmetic operators in that they can do math, but they can also do other assignment functions on a given variable. For example: `int a = 10;`, where we *assign* the value of `10` to variable `a`.
- Relational and Logical Operators
	- These evaluate conditions and compare between two or more values. For example: `a > 5`.

### Arithmetic Operators
- Addition (+)
	- Adds two values
- Subtraction (-)
	- Subtracts the second value from the first
- Multiplication (\*)
	- Multiplies the two values
- Division (/)
	- Divides the first value by the second
- Modulus (%)
	- Divides the two values, but returns the remainder
- *Increment (++)*
	- Increases a value by one
- *Decrement (\--)*
	- Decreases a value by one

#### Increment/Decrement Operators
This one is special, because it can be formatted in a **prefix or postfix** manner, and it will change the way the code is ran.

For example, if we had `a = 0;`, then `a++` would return the value of `a`, which is 0, and then add 1 to it.

However, if we, again, have `a = 0;` but then did `++a`, then it would add 1 to `a`, **and then** return the new value, which is 1.

These distinctions are important as, as stated earlier, it can change the way your code executes.

**Demonstration:**
With **postfix**,
```
a = 0;

// With postfix (a++) //
print("a = " + a++)
print("a = " + a)
```

```
// Output //
a = 0
a = 1
```

Whereas with prefix,
```
a = 0;

// With prefix (++a) //
print("a = " + ++a)
print("a = " + a)
```

```
// Output //
a = 1
a = 1
```




### Assignment Operators
- =
	- Assigns a value from the right side to the left side.
- +=
	- **Adds**, then assigns the total to the left value
- -=
	- **Subtracts**, then assigns the result to the left value
- \*=
	- **Multiplies**, then assigns the total to the left value
- /=
	- **Divides**, then- you know the story by now.
- %=
	- **Divides**, then returns the **remainder** to the left value


### Boolean Operators
== - Equal
!= - Not Equal
< = Lesser Than
\> = Greater Than

&& is only satisfied when **both** operations are true. (Basically ```AND```)

|| is satisfied when **only one** of the operations are true. (Basically ```OR```)

! is satisfied when the operation is **false**. (This is called a ```NOT``` operator)

```
int a = 10;
int b = 20;

bool c = (a != b);

// (a != b) is false, therefore c is false


if (!c)

// as c is false, !c is true
```


Another thing we have is the Ternary/Conditional Operator ```?```. This returns one value or the other, depending on the value of a boolean expression.

```
if (x == 10)
{
	result = 10 * 10;
}

else
{
	result = 50;
}

// Above, converted to using the ternary/conditional operator.

result = (x == 10) ? 10 * 10 : 50
```


---
## If, Else If, Else

These are more or less the same as they were in Python, but there's a few important things to take note of.

For one, ```else if``` has to be spelt in its <u>full form</u>, instead of the ```elif``` we had in Python. 
```
if (a = 10)
	print("wow");
else if (a = 15)
	print("how"):
```


Another thing is that if we have *more than one statement* for any ```if``` condition, we'd need to surround the statements with <u>curly brackets</u> ```{}```

```
if (a = 10)
{
	print("Wow");
	print("You're great~");
}
else if (a = 8)
{
	print("Aww!");
	print("You tried your best~");
}
```

Remember how, in Python, the statements were ordered based on indentation? In C#, we use curly brackets ```{}``` instead. Could be tricky to close, so just watch out of that.

---

That's operators! Control statements are up next.

\- Mikhail

Next: [[3 - Control Statements]]
Previous: [[1 - Datatypes, Variables, Arrays]]


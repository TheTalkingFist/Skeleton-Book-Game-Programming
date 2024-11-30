"Pick up my bag, run to the station. Railman says, he got the wrong location."
<sup>The Beatles - One After 909</sup>


Control Statements are the ifs and the whens and the hows and the whys. Actually, it's only just the ifs.


## If

```if``` checks if a condition. If the condition is met, it runs whatever code we chucked inside of it.

```
int a = 10;

if (a < 20)
{
	print("a is less than 10");
}
```

This code will run, as 10 is less than 20, therefore a is less than 20.

To be more technical, the ```if``` checks for a boolean statement in the condition, in the example above, the condition is ```True```, therefore the block of code inside of the curly brackets will run.


## If... else if... else

We also have `else if`, which is basically a layered `if`.

```
if (a < 20)
{
	print("a is less than 10")
}

else if (a = 10)
{
	print("a is equal to 10")
}

else
{
	print("a is greater than 10")
}
```

## Nested If

In addition, we could also have nested `if` statements, like

```
if (a > 10)
{
	if (a < 20)
	{
		print("a is less than 20 but greater than 10")
	}
}
```



## Switch Statements

This one allows a variable to be tested for equality against a whole list of values. Each value in the list is called a *case*.

Essentially, an easier, more organised way to execute a sequence of `if`s, so we don't end up like YanDev.

```
int a;

switch (a)
{
	case '10':
		print("Welcome to Slaughter Valley.");
		break;
		
	case '20':
		print("How are you?");
		break;
		
	case '30':
		print("Goodbye To Us.");
		break;
}
```

This lays out the structure of what could be a bunch of `else if`s to be quite easily readable. At least, in my opinion.

---

That's it for control statements. I'm going through this pretty quick. Next is Loops!

\- Mikhail

Next: [[4 - Loop-De-Loop-De-Loop-De-Loop-De-Loop-De-Loop-De-Loop-De-Loop-De-Loop...]]
Previous: [[2 - Doctor, Operator]]




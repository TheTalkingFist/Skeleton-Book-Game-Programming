"Somebody, ooh somebody, can anybody find me to love?"
<sup>Queen - Somebody To Love</sup>


Loops! Here they are again.

## While

A while loop repeats a block of code as long as a condition is kept as true.

```
int a = 10;

while (a = 10)
{
	print("Haha, you made an infinity loop and your computer's gonna crash!")
}
```

This will run forever, as `a` is declared as 10 and is not changed throughout.

This means it's probably not a good idea to keep this loop going for long. Of course, this loop will end if you change the value of `a` to something else later down the line.


## For

This one runs for a specified amount of time, as compared to the `while` loop. This one has a specific structure.

```
for (int a = 10; a < 15; a = a + 1)
{
	Debug.Log("Value of a = " + a);
}
```

Let's take a look at that a bit closer.

```
for (int a = 10; a < 15; a = a + 1)
```

Let me break it down for you.

`int a = 10;`
Initialises the variable `i`, giving it the value of `10`.

`a < 15;`
Compares the value of `a` with `15`. As long as `a` is less than `15`, the loop will run.

`a = a + 1;`
After each loop, `a` will increment by one. You could replace this with `a++`.

Essentially, the format goes something like this.
```
for ([initialise  variable with value]; [compare the variable]; [change variable])
```

This is an oversimplification, mostly because any more than this won't fit in one line. Sorry.



## Do... While. 

Practically similar to the while loop, except that it **checks for the condition after each loop is ran**.

```
int a = 10;

do
{
	print(a);
	a++;
} while (a < 20);
```

As stated earlier, since it checks after each loop is ran, which incidentally means that it will always run at least once.


## Foreach (For each)

This one executes a block of code for every element in an array, kinda similar to the way we did it in Python.

Let's say we have an array `numbers`.

```
int[] numbers = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

foreach (int numdex in numbers)
{
	print(numdex)
}
```

`int numdex` is a variable initialisation used to store the current value of the array. This variable *does not need* to be initialised or created before the `foreach` loop was called.

`in numbers` just says which array to use, nothing much to it.

Of course, this would print every number in the `numbers` array.


# Nested Loops

A loop inside a loop! We can do that in C#.

```
while (a = 10)
{
	while (a = 10)
	{
		yada yada yada
	}
}
```

![[Pasted image 20241017113913.png]]

---

Oh, that's it. Alright.

\- Mikhail

Next: [[5 - Hello, Class]]
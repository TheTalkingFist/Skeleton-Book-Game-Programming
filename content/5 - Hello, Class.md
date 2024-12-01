"You reached for the secret too soon... You cried for the moon."
<sup>Pink Floyd - Shine On You Crazy Diamond (Pts. I - V)</sup>


Remember Python? Classes are back!


# Classes
A collection of both variables and methods, all in a single C# object. These are real important when making modern games. Actually, they're important in all of Object-Oriented Programming.

They're often used to represent objects in the world of a game project. Even an entity or character.

![[bugger.png]]
<sup>Don't worry about the IDE, I'm just testing out JetBrains Rider. None of the important stuff is different. If it was, then the world would suck.</sup>


### Properties
Alongside that, we also have `properties`, which are essentially methods [masquerading](https://dictionary.cambridge.org/dictionary/english/masquerade) as variables with the `get` and `set` accessors.
```
public Vector3 pos
{
	get
	{
		return(value.from.another.thing);
	}
	
	set
	{
		value.from.another.thing = true;
	}
}
```
Basically, you can take a variable from another class and change it.

### Classes as Components
Another good thing to note is that Unity treats every class as a component in and of itself. Let's say we have a GameObject called `Player` with a variable `health`. We can use `GetComponent<>()`

```
player = GetComponent(Player)
```

Then, to access the variable,
```
playerhealth.health;
```

---

# Access Specifiers
These essentially dictate how 'accessible' a class member (variable, method, etc.) is, as in whether any external object can take from it. These specifiers are as follows, from public to private:

- Public
- Internal
- Protected
- Internal Protected
- Private

### Public
No restrictions, any object, even outside the namespace, can access the member.

### Internal
Anything with internal can be accessed within the program that contain its declarations, as well as the same assembly, but not anything from another assembly.

### Protected
Accessibility is limited within the class, and everything that's a child of the class.

### Internal Protected
Internal and Protected combined, it can access anything within the same assembly, the same class and everything inherited from the class.

### Private
The least accessible, cannot be accessed from outside the class itself. This is the default access specifier, if none else is declared.

---
# Not In The Slides

This one is about constructors. I'm not exactly sure about how this goes in the theory, since constructors aren't in the slides. But, oh well.


We can use constructors as sort of 'templates' for any object we'd create with it. For example, let's create a constructor `fruit` so we can make different types of, well, fruit.

We could have color, taste and texture for each fruit.

We can do that with parameters, which goes into the brackets.

```
public Fruit(string n, string cl, string tst, string txt)
{
	Name = n;
	Color = cl;
	Taste = tst;
	Texture = txt;
}
```



We now have a fruit base! We can then create a new object with these attributes, using the `Fruit` template.

For starters, we'll make an apple, because *everything* is born from apples.

```
Fruit Apple = new Fruit("Apple", "red", "sweet", "crisp")
```

With `Fruit Apple`, we are making a new object called `Apple` in the `Fruit` class.

Remember, `new` reserves memory in our systems for the object, like how you'd book a seat in a restaurant and they'd save it just for lil' ol' you.

`Fruit(...` makes a new object in the `Fruit` class.

`...("Apple", "red", "sweet", "crisp")` dictates the attributes of the object, based on the order of the attributes we set up when creating the class.

Referring back to the class creation earlier, we can see that it goes in the order of `Name`, `Color`, `Taste` and `Texture`.

We are trying to match this order with the order of the attributes we are stating when creating this new object, so...

```
Name = "Apple"
Color = "red"
Taste = "sweet"
Texture = "crisp"
```

---

And that's it from me! After this, it's all Jeb. This is our last test for the term, so give it all you've got!

\- Mikhail

Next: [[6 - Method Acting]]


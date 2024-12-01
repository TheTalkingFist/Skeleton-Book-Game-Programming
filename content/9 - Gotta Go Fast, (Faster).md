
"Bring a pen and paper and some time to think  
Document our voyage till you're out of ink"
<sup>Last Dinosaurs - Andy</sup>

<font color="#ff0000">Red</font> = <font color="#ff0000">Important to Remember!</font>
<font color="#ffff00">Yellow</font> = <font color="#ffff00">Must Read!</font>
<font color="#00b050">Green</font> = <font color="#00b050">Examples</font>

# Code Optimisation

<font color="#ff0000">Game Optimisation</font>, <font color="#ffff00">enhances the performance of your game, reduce load times, </font>
<font color="#ffff00">ensure smoother and better gameplay, even on less powerful devices.</font>

<font color="#ff0000">Code Optimisation</font> though, <font color="#ffff00">aims to improve the efficiency of a piece of code, making it execute faster and consume less memory or disk storage without altering its output.</font>

In Video Games, particularly mobile games, his process becomes  crucial due to the limited computing power, memory, and processor capabilities of mobile hardware.

# Steps to Optimise a Video Game

1. Set Performance Goals:
   
<font color="#ffff00">Defines specific performance targets which can include, target frame rate, memory usage and load times. Having clear goals will help guide the optimisation efforts.</font>
   
---
2.  Profile the Game: 

Unity has a profiler window that can <font color="#ffff00">help you analyse the performance of  your game in real-time.</font>

Supplying detailed components such as:

- CPU Usage
- Rendering
- Memory Allocation
- Other Performance Metrics

You can use it to <font color="#ffff00">find which parts of your code are taking the most time and resources.</font>
<font color="#ffff00">Helping to pinpoint areas of improvement.</font>

---
3. Optimise Algorithms 

<font color="#ffff00">Focuses on improving the efficiency of critical algorithms used in a game.</font>

This may include: Pathfinding, Collision Detection and Sorting.

Choosing <font color="#ffff00">better algorithms can lead to significant performance gains.</font>

---
4. Code-Level Optimisation

<font color="#ffff00">Reviews and Optimises your code to eliminate unnecessary calculations, reducing function calls, and adding the use of efficient data structures.</font>

<font color="#ffff00">Fine-tuning your code can result in noticeable improvements.</font>

---
5. Texture and Asset Optimisation

<font color="#ffff00">Compresses textures, reducing the asset size and implementing asset streaming to minimise memory usage and loading times.</font>

<font color="#00b050">One such example is:</font>

<font color="#00b050">Sprite Atlas is a feature in Unity that allows you to pack multiple individual sprite images into a single texture atlas. It can help optimise games in Unity, especially when dealing with multiple sprites or UI elements.</font>

Textures <font color="#ffff00">not packed</font> using Sprite Atlas <font color="#ffff00">should have dimensions of power of 2</font>, to<font color="#ff0000"> take advantage of memory handling optimisations on the GPU.</font>

<font color="#ffff00">Longer audio such as background music should have its Load Type in Import Settings set to Streaming rather than Decompress on Load or Compressed in Memory.</font>

The<font color="#ffff00"> trade-off is a potential slight delay in starting</font>, but the benefit is that <font color="#ffff00">only a fraction of RAM is necessary to stream vs. loading and decompressing the entire song in memory.</font>

---
6. Render Batching 

<font color="#ffff00">Minimises the number of draw cells by using render batching techniques to group similar objects together. Reducing CPU overhead and improving GPU performance.</font>

---
7. Use Level of Detail(LOD)
   
Implement LOD techniques to <font color="#ffff00">reduce the level of detail for distant objects, improving rendering performance. </font>

<font color="#ffff00">Distant objects use lower-poly models and simpler textures, reducing the render workload.</font>

---
8. Cull Unseen Objects

Implement occlusion culling and frustum <font color="#ffff00">culling is used to avoid rendering objects that are not visible to the camera.</font>

| Regular Frustum:                                                                                                  | Occlusion Culling:                                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Regular Frustum culling only renders<br>objects within the camera's vie Occlusion culling removes additional objects<br>from within the camera rendering work if they<br>are completely obscured by nearer objects d  k  g  g  g  g  g  g  g  g  g  g  g  g  g  g  g  g  g  g  g  g  |

---
9. <font color="#ff0000">Memory Management</font>

<font color="#ff0000">Object Pooling</font>, <font color="#ffff00">reuses objects and resources whenever possible rather than creating and destroying new ones. Avoiding frequent memory allocations and deallocations, costly in terms of CPU time and memory fragmentation.</font>

This <font color="#00b050">applies to Game Objects frequently created and destroyed which includes</font>: 
bullets, muzzle flashes, and blocks of procedurally unbreakable terrain.

---
# Optimising Loops

<font color="#ffff00">Necessary and crucial aspect of Code-Level optimisation. Unnecessary loop iterations can improve performance gains. </font>

Note that there are <font color="#ffff00">no performance difference between for and while loops</font>.

**Before optimisation:****

C# for loop code:

```
int sum = 0;
for (int i = 0; i <= 10; i++)
{
    if(i%2==0)
    {
        sum+=i;
    }
}
Debug.Log(sum);
```

Some Examples of the iteration of the loop:

| i = 1: 1 % 2 == 1 (false), so sum +=  1 is not executed.                 |
| ------------------------------------------------------------------------ |
| i = 2 : 2 % 2 == 0 (true), so sum += 2. The value of sum is updated to 2 |
Example goes till i = 10

In the above code/example:

i. The variable sum is initialised to 0.  

ii. A for loop is started with the iterator i  
initialised to 1.  

iii. The loop runs as long as i is less than or equal  
to 10.  

iv. Inside the loop, there is an if condition that  
checks if i is even (i.e., i % 2 == 0). 

v. If the condition is true, the value of i is added  
to the sum.  

vi. The loop increments i by 1 in each iteration  
(i++).  

vii. After the loop ends, the value of sum is printed  
using Debug.Log()

## Optimisation Round 1

Since we know we only need to sum up the even numbers, we can update  
the loop to iterate over only even values, this results in the code becoming more  
efficient and optimised compared to the initial version.

This makes it so that there will only be 5 iterations that will be executed, resulting in no need for the if condition

## Optimisation Round 2

int n = 10;
int sum = n*(n+1){<span style="background:#fff88f">even numbers from 1 to n</span>}/2;
Debug.Log(sum);

Further optimisation of the code can be attributed to directly calculating the sum of even numbers  from 1 to 10 without using a loop. Using the formula above, we can find the sum of even numbers since the numbers are consecutive even numbers.

n would be the last even number in this case is 10.

This results in the output which is still 30, with the optimised code we can directly calculate the sum of even numbers without iterating through each numbers in a loop.

# Optimising Game Loops

In Unity Scripts, Since Update() is called once per frame, A typical game loop will like:


```
Void Start()
{
    // initialization code (e.g. Setting up game objects, initialising variables)
}

Void Update()
{
    HandleInput()  //Input Handling
    UpdateGameLogic()   //Update the game state
    Render()   //Render the game graphics
    HandleAudio()   //Handle audio processing 
}
```


If the game is running at 60 frames per second, update() will be called 60 times per second, making optimisation of update() crucial.

1. Each call to GetComponent is relatively expensive, especially if called frequently in update().

We can cache references to components in variables during initialization and reuse them in Update()!
```
private Rigidbody rb;
Void Start()
{
    rb = GetComponent<Rigidbody>();
}

Void Update()
{
    rb.MovePosition(transform.position + Vector3.forward*Time.deltatime);
}
```

2. Use localPosition is generally faster than using position, also true for localRotation.

3. Codes that does not need to run every frame should be encased in a conditional block.
   
   <font color="#00b050">For Example:</font>
<font color="#00b050">   </font>
<font color="#00b050">   if a player is being knocked back after taking damage, we do not need to check the Controller input since they are not able to move on their own this frame.</font>

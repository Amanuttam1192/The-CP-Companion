# :man_technologist:DYNAMIC PROGRAMMING:woman_technologist:

> <h2>  Dynamic programming is basically, recursion plus using common sense. </h2>

<hr>

![DP](https://user-images.githubusercontent.com/77975418/136185104-a0039576-51d1-4e3f-a750-27d8dd21cacc.jpg)


<hr>


> What it means is that recursion allows you to express the value of a function in terms of other values of that function. Common sense tells you that if you implement your function in a way that the recursive calls are done in advance, and stored for easy access, it will make your program faster. 


> This is what we call Memoization - it is memorizing the results of some specific states, which can then be later accessed to solve other sub-problems


<hr>


> 
> - Let us say that we have a machine, and to determine its state at time t, we have certain quantities called state variables. 
> 
> - There will be certain times when we have to make a decision which affects the state of the system, which may or may not be known to us in advance. 
> 
> - These decisions or changes are equivalent to transformations of state variables. The results of the previous decisions help us in choosing the future ones.

<br>

> We need to break up a problem into a series of overlapping sub-problems, and build up solutions to larger and larger sub-problems.
>  
> If you are given a problem, which can be broken down into smaller sub-problems, and these smaller subproblems can still be broken into smaller ones - and if you manage to find out that there are some overlapping subproblems, then you've encountered a DP problem


🎯The intuition behind dynamic programming is that we trade space for time, i.e. to say that instead of calculating all the states taking a lot of time but no space, we take up space to store the results of all the sub-problems to save time later.


<hr>


# A simple lay man illustration

1. Writes down "1+1+1+1+1+1+1+1 =" on a sheet of paper.

2. "What's that equal to?"

3. Counting "Eight!"

4. Writes down another "1+" on the left.

5. "What about that?"

6. "Nine!" " How'd you know it was nine so fast?"

7. "You just added one more!"

8. "So you didn't need to recount because you remembered there were eight! Dynamic Programming is just a fancy way to say remembering stuff to save time later!"


<hr>


<h2> 🎯Let's try to understand this by taking an example of Fibonacci numbers. </h2>

We have already discussed the recursive code for the fibbonacci sequence. But did we talk about its efficiency ?? Let's do it now.

> For this, we might require the **recursion tree** for the recursive code. That is simple as we have discussed already, Just put the input given as the root node and then draw the tree for each function calls.


After drawing the tree  we might have a simple observation, that is,  
**"Why are the function calls for finding the same value again and again ?"** 

Well, let's take an ilustration !

<hr>

![image](https://user-images.githubusercontent.com/77975418/135809244-df122823-2889-4832-87c4-40edc00753e4.png)


<hr>

If you look closely, and analyse the colour patterns, it is clear that the same values are called again and again. For a small number this might seem fine, but for large cases its just a terrible piece of mess. But wait !!

> **Why don't we consider storing the values somewhere, so that we can access it whenever it is needed rather than calling the recursive function again and again ?**

Lets try to understand it !! Of course using an illustration !

<hr>


![image](https://user-images.githubusercontent.com/77975418/135809320-302d767c-ecf3-4a2f-bd92-589a52c9a90f.png)


<hr>

This cocept of breaking the main problem into subproblem, storing the results and then find the further results by using the answers we got from the subproblems can be said as an **Dynammic Programming approach !**

<hr>



```
Fibonacci (n) = 1; if n = 0

Fibonacci (n) = 1; if n = 1

Fibonacci (n) = Fibonacci(n-1) + Fibonacci(n-2)

```

> So, the first few numbers in this series will be: 1, 1, 2, 3, 5, 8, 13, 21... and so on!



<h2> :keyboard:A code for it using pure recursion:</h2>

```
 
 int fib (int n)
 
 {
 
        if (n < 2)
        
            return 1;
            
        return fib(n-1) + fib(n-2);
        
    }
    
```
    
    
<h2> :keyboard:Using Dynamic Programming approach with memoization: </h2>

```

void fib () 

{

        fibresult[0] = 1;
        
        fibresult[1] = 1;
        
        for (int i = 2; i<n; i++)
        
           fibresult[i] = fibresult[i-1] + fibresult[i-2];
           
    }
    
   
```
   
   
<hr>


<h3> :star:Are we using a different recurrence relation in the two codes? No. Are we doing anything different in the two codes? Yes. </h3>

> In the recursive code, a lot of values are being recalculated multiple times. We could do good with calculating each unique quantity only once. Take a look at the image to understand that how certain values were being recalculated in the recursive way:


<hr>



# Majority of the Dynamic Programming problems can be categorized into two types:

1. Optimization problems.

2. Combinatorial problems.

<hr>


**Every Dynamic Programming problem has a schema to be followed:**

- Show that the problem can be broken down into optimal sub-problems.
- Recursively define the value of the solution by expressing it in terms of optimal solutions for smaller sub-problems.
- Compute the value of the optimal solution in bottom-up fashion.
- Construct an optimal solution from the computed information.

<hr>


<h3> For better understanding on DYNAMIC PROGRAMMING, refer the 
 
[Solved Examples](https://github.com/ISTE-VIT/The-CP-Companion/tree/main/DYNAMIC%20PROGRAMMING/SOLVED%20EXAMPLES)</h3>


<hr>

        
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=102)](https://hacktoberfest.digitalocean.com/)&nbsp;
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)]()&nbsp;


<hr>



<h1> <p align ="center"> HAPPY CODING :man_technologist:</p> </h1>

<hr>



<!-- # Bottom up vs. Top Down: -->

<!-- > Bottom Up - I'm going to learn programming. Then, I will start practicing. Then, I will start taking part in contests. Then, I'll practice even more and try to improve. After working hard like crazy, I'll be an amazing coder. -->

<!-- > Top Down - I will be an amazing coder. How? I will work hard like crazy. How? I'll practice more and try to improve. How? I'll start taking part in contests. Then? I'll practicing. How? I'm going to learn programming. -->


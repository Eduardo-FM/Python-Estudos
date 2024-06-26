# What is an Algorithm?
In computer programming terms, an algorithm is a set of well-defined instructions to solve a particular problem. It takes a set of input(s) and produces the desired output. For example,

An algorithm to add two numbers:

1. Take two number inputs

2. Add numbers using the + operator

3. Display the result

> Qualities of a Good Algorithm
> - Input and output should be defined precisely.
> - Each step in the algorithm should be clear and unambiguous.
> - Algorithms should be most effective among many different ways to solve a problem.
> - An algorithm shouldn't include computer code. Instead, the algorithm should be written in such a way that it can be used in different programming languages.


### Examples

- Algorithm 1: Add two numbers entered by the user
```
Step 1: Start
Step 2: Declare variables num1, num2 and sum. 
Step 3: Read values num1 and num2. 
Step 4: Add num1 and num2 and assign the result to sum.
        sum←num1+num2 
Step 5: Display sum 
Step 6: Stop
```

- Algorithm 2: Find the largest number among three numbers

```
Step 1: Start
Step 2: Declare variables a,b and c.
Step 3: Read variables a,b and c.
Step 4: If a > b
           If a > c
              Display a is the largest number.
           Else
              Display c is the largest number.
        Else
           If b > c
              Display b is the largest number.
           Else
              Display c is the greatest number.  
Step 5: Stop
```

- Algorithm 3: Find Roots of a Quadratic Equation ax2 + bx + c = 0

```
Step 1: Start
Step 2: Declare variables a, b, c, D, x1, x2, rp and ip;
Step 3: Calculate discriminant
         D ← b2-4ac
Step 4: If D ≥ 0
              r1 ← (-b+√D)/2a
              r2 ← (-b-√D)/2a 
              Display r1 and r2 as roots.
        Else     
              Calculate real part and imaginary part
              rp ← -b/2a
              ip ← √(-D)/2a
              Display rp+j(ip) and rp-j(ip) as roots
Step 5: Stop             
```

- Algorithm 4: Find the factorial of a number

```
Step 1: Start
Step 2: Declare variables n, factorial and i.
Step 3: Initialize variables
          factorial ← 1
          i ← 1
Step 4: Read value of n
Step 5: Repeat the steps until i = n
     5.1: factorial ← factorial*i
     5.2: i ← i+1
Step 6: Display factorial
Step 7: Stop
```

- Algorithm 5: Check whether a number is prime or not

```
Step 1: Start
Step 2: Declare variables n, i, flag.
Step 3: Initialize variables
        flag ← 1
        i ← 2  
Step 4: Read n from the user.
Step 5: Repeat the steps until i=(n/2)
     5.1 If remainder of n÷i equals 0
            flag ← 0
            Go to step 6
     5.2 i ← i+1
Step 6: If flag = 0
           Display n is not prime
        else
           Display n is prime
Step 7: Stop 
```

- Algorithm 6: Find the Fibonacci series till the term less than 1000

```
Step 1: Start 
Step 2: Declare variables first_term,second_term and temp. 
Step 3: Initialize variables first_term ← 0 second_term ← 1 
Step 4: Display first_term and second_term 
Step 5: Repeat the steps until second_term ≤ 1000 
     5.1: temp ← second_term 
     5.2: second_term ← second_term + first_term 
     5.3: first_term ← temp 
     5.4: Display second_term 
Step 6: Stop
```

# Data Structure and Types

## What are Data Structures?
Data structure is a storage that is used to store and organize data. It is a way of arranging data on a computer so that it can be accessed and updated efficiently.

Depending on your requirement and project, it is important to choose the right data structure for your project. For example, if you want to store data sequentially in the memory, then you can go for the Array data structure.

![alt text](imagens/image.png)

> Note: Data structure and data types are slightly different. Data structure is the collection of data types arranged in a specific order.

## Types of Data Structure
Basically, data structures are divided into two categories:

Linear data structure
Non-linear data structure
Let's learn about each type in detail.

# Linear data structures
In linear data structures, the elements are arranged in sequence one after the other. Since elements are arranged in particular order, they are easy to implement.

However, when the complexity of the program increases, the linear data structures might not be the best choice because of operational complexities.

**Popular linear data structures are:**

## What are Algorithms?
Informally, an algorithm is nothing but a mention of steps to solve a problem. They are essentially a solution.

For example, an algorithm to solve the problem of factorials might look something like this:

**Problem: Find the factorial of n**

```
Initialize fact = 1
For every value v in range 1 to n:
    Multiply the fact by v
fact contains the factorial of n
```

Here, the algorithm is written in English. If it was written in a programming language, we would call it to code instead. Here is a code for finding the factorial of a number in C++.

``` c++
int factorial(int n) {
    int fact = 1;
    for (int v = 1; v <= n; v++) {
        fact = fact * v;
    }
    return fact;
}
```

Programming is all about data structures and algorithms. Data structures are used to hold data while algorithms are used to solve the problem using that data.

Data structures and algorithms (DSA) goes through solutions to standard problems in detail and gives you an insight into how efficient it is to use each one of them. It also teaches you the science of evaluating the efficiency of an algorithm. This enables you to choose the best of various choices.

## Use of Data Structures and Algorithms to Make Your Code Scalable

Time is precious.

Suppose, Alice and Bob are trying to solve a simple problem of finding the sum of the first 1011 natural numbers. While Bob was writing the algorithm, Alice implemented it proving that it is as simple as criticizing Donald Trump.

Algorithm (by Bob)

``` 
Initialize sum = 0
for every natural number n in range 1 to 1011(inclusive):
    add n to sum
sum is your answer
```

Code (by Alice)

``` cpp
int findSum() {
    int sum = 0;
    for (int v = 1; v <= 100000000000; v++) {
        sum += v;
    }
    return sum;
}
```
Alice and Bob are feeling euphoric of themselves that they could build something of their own in almost no time. Let's sneak into their workspace and listen to their conversation.

> Alice: Let's run this code and find out the sum.\
> Bob: I ran this code a few minutes back but it's still not showing the output. What's wrong with it?

Oops, something went wrong! A computer is the most deterministic machine. Going back and trying to run it again won't help. So let's analyze what's wrong with this simple code.

Two of the most valuable resources for a computer program are time and memory.

The time taken by the computer to run code is:

> Time to run code = number of instructions * time to execute each instruction

The number of instructions depends on the code you used, and the time taken to execute each code depends on your machine and compiler.

In this case, the total number of instructions executed (let's say x) are

**x = 1 + (1011 + 1) + (1011) + 1**, which is **x = 2 * 1011 + 3**

Let us assume that a computer can execute y = 108 instructions in one second (it can vary subject to machine configuration). The time taken to run above code is

```mathematica
Time to run y instructions = 1 second
Time to run 1 instruction = 1 / y seconds
Time to run x instructions = x * (1/y) seconds = x / y seconds

Hence,
Time to run the code = x / y 
                     = (2 * 1011 + 3) / 108 (greater than 33 minutes)
```

Is it possible to optimize the algorithm so that Alice and Bob do not have to wait for 33 minutes every time they run this code?

I am sure that you already guessed the right method. The sum of first N natural numbers is given by the formula:

```mathematica
Sum = N * (N + 1) / 2
```

Converting it into code will look something like this:

```cpp
int sum(int N) {
    return N * (N + 1) / 2;
}
```

This code executes in just one instruction and gets the task done no matter what the value is. Let it be greater than the total number of atoms in the universe. It will find the result in no time.

The time taken to solve the problem, in this case, is 1/y (which is 10 nanoseconds). By the way, the fusion reaction of a hydrogen bomb takes 40-50 ns, which means your program will complete successfully even if someone throws a hydrogen bomb on your computer at the same time you ran your code. :)

> Note: Computers take a few instructions (not 1) to compute multiplication and division. I have said 1 just for the sake of simplicity.

## More on Scalability
Scalability is scale plus ability, which means the quality of an algorithm/system to handle the problem of larger size.

Consider the problem of setting up a classroom of 50 students. One of the simplest solutions is to book a room, get a blackboard, a few chalks, and the problem is solved.

But what if the size of the problem increases? What if the number of students increased to 200?

The solution still holds but it needs more resources. In this case, you will probably need a much larger room (probably a theater), a projector screen and a digital pen.

What if the number of students increased to 1000?

The solution fails or uses a lot of resources when the size of the problem increases. This means, your solution wasn't scalable.

What is a scalable solution then?

Consider a site like Khanacademy, millions of students can see videos, read answers at the same time and no more resources are required. So, the solution can solve the problems of larger size under resource crunch.

If you see our first solution to find the sum of first N natural numbers, it wasn't scalable. It's because it required linear growth in time with the linear growth in the size of the problem. Such algorithms are also known as linearly scalable algorithms.

Our second solution was very scalable and didn't require the use of any more time to solve a problem of larger size. These are known as constant-time algorithms.

## Memory is expensive
Memory is not always available in abundance. While dealing with code/system which requires you to store or produce a lot of data, it is critical for your algorithm to save the usage of memory wherever possible. For example: While storing data about people, you can save memory by storing only their date of birth, not their age. You can always calculate it on the fly using their date of birth and current date.

## Examples of an Algorithm's Efficiency
Here are some examples of what learning algorithms and data structures enable you to do:

### Example 1: Age Group Problem
Problems like finding the people of a certain age group can easily be solved with a little modified version of the binary search algorithm (assuming that the data is sorted).

The naive algorithm which goes through all the persons one by one, and checks if it falls in the given age group is linearly scalable. Whereas, binary search claims itself to be a logarithmically scalable algorithm. This means that if the size of the problem is squared, the time taken to solve it is only doubled.

Suppose, it takes 1 second to find all the people at a certain age for a group of 1000. Then for a group of 1 million people,

- the binary search algorithm will take only 2 seconds to solve the problem
- the naive algorithm might take 1 million seconds, which is around 12 days
The same binary search algorithm is used to find the square root of a number.


### Example 2: Rubik's Cube Problem
Imagine you are writing a program to find the solution of a Rubik's cube.

This cute looking puzzle has annoyingly 43,252,003,274,489,856,000 positions, and these are just positions! Imagine the number of paths one can take to reach the wrong positions.

Fortunately, the way to solve this problem can be represented by the graph data structure. There is a graph algorithm known as Dijkstra's algorithm which allows you to solve this problem in linear time. Yes, you heard it right. It means that it allows you to reach the solved position in a minimum number of states.

### Example 3: DNA Problem
DNA is a molecule that carries genetic information. They are made up of smaller units which are represented by Roman characters A, C, T, and G.

Imagine yourself working in the field of bioinformatics. You are assigned the work of finding out the occurrence of a particular pattern in a DNA strand.

It is a famous problem in computer science academia. And, the simplest algorithm takes the time proportional to

> (number of character in DNA strand) * (number of characters in pattern)

A typical DNA strand has millions of such units. Eh! worry not. KMP algorithm can get this done in time which is proportional to

> (number of character in DNA strand) + (number of characters in pattern)

The * operator replaced by + makes a lot of change.

Considering that the pattern was of 100 characters, your algorithm is now 100 times faster. If your pattern was of 1000 characters, the KMP algorithm would be almost 1000 times faster. That is, if you were able to find the occurrence of pattern in 1 second, it will now take you just 1 ms. We can also put this in another way. Instead of matching 1 strand, you can match 1000 strands of similar length at the same time.

And there are infinite such stories...

### Final Words
Generally, software development involves learning new technologies on a daily basis. You get to learn most of these technologies while using them in one of your projects. However, it is not the case with algorithms.

If you don't know algorithms well, you won't be able to identify if you can optimize the code you are writing right now. You are expected to know them in advance and apply them wherever possible and critical.

We specifically talked about the scalability of algorithms. A software system consists of many such algorithms. Optimizing any one of them leads to a better system.

However, it's important to note that this is not the only way to make a system scalable. For example, a technique known as distributed computing allows independent parts of a program to run to multiple machines together making it even more scalable.

# Asymptotic Analysis: Big-O Notation and More
The efficiency of an algorithm depends on the amount of time, storage and other resources required to execute the algorithm. The efficiency is measured with the help of asymptotic notations.

An algorithm may not have the same performance for different types of inputs. With the increase in the input size, the performance will change.

The study of change in performance of the algorithm with the change in the order of the input size is defined as asymptotic analysis.

## Asymptotic Notations
Asymptotic notations are the mathematical notations used to describe the running time of an algorithm when the input tends towards a particular value or a limiting value.

For example: In bubble sort, when the input array is already sorted, the time taken by the algorithm is linear i.e. the best case.

But, when the input array is in reverse condition, the algorithm takes the maximum time (quadratic) to sort the elements i.e. the worst case.

When the input array is neither sorted nor in reverse order, then it takes average time. These durations are denoted using asymptotic notations.

There are mainly three asymptotic notations:

- Big-O notation
- Omega notation
- Theta notation


## Big-O Notation (O-notation)
Big-O notation represents the upper bound of the running time of an algorithm. Thus, it gives the worst-case complexity of an algorithm.

![alt text](https://cdn.programiz.com/sites/tutorial2program/files/big0.png)

Big-O gives the upper bound of a function

``` mathematica
O(g(n)) = { f(n): there exist positive constants c and n0
            such that 0 ≤ f(n) ≤ cg(n) for all n ≥ n0 }
```

The above expression can be described as a function f(n) belongs to the set O(g(n)) if there exists a positive constant c such that it lies between 0 and cg(n), for sufficiently large n.

For any value of n, the running time of an algorithm does not cross the time provided by O(g(n)).

Since it gives the worst-case running time of an algorithm, it is widely used to analyze an algorithm as we are always interested in the worst-case scenario.

## Omega Notation (Ω-notation)
Omega notation represents the lower bound of the running time of an algorithm. Thus, it provides the best case complexity of an algorithm.

![alt text](https://cdn.programiz.com/sites/tutorial2program/files/omega.png)

``` mathematica
Ω(g(n)) = { f(n): there exist positive constants c and n0 
            such that 0 ≤ cg(n) ≤ f(n) for all n ≥ n0 }
```

The above expression can be described as a function f(n) belongs to the set Ω(g(n)) if there exists a positive constant c such that it lies above cg(n), for sufficiently large n.

For any value of n, the minimum time required by the algorithm is given by Omega Ω(g(n)).



## Theta Notation (Θ-notation)
Theta notation encloses the function from above and below. Since it represents the upper and the lower bound of the running time of an algorithm, it is used for analyzing the average-case complexity of an algorithm.

![alt text](https://cdn.programiz.com/sites/tutorial2program/files/theta.png)

Asymptotic Analysis: Theta notation
Theta bounds the function within constants factors
For a function g(n), Θ(g(n)) is given by the relation:

``` mathematica
Θ(g(n)) = { f(n): there exist positive constants c1, c2 and n0
            such that 0 ≤ c1g(n) ≤ f(n) ≤ c2g(n) for all n ≥ n0 }
```

The above expression can be described as a function f(n) belongs to the set Θ(g(n)) if there exist positive constants c1 and c2 such that it can be sandwiched between c1g(n) and c2g(n), for sufficiently large n.

If a function f(n) lies anywhere in between c1g(n) and c2g(n) for all n ≥ n0, then f(n) is said to be asymptotically tight bound.

## Master Theorem
The master method is a formula for solving recurrence relations of the form:

``` mathematica
T(n) = aT(n/b) + f(n),
where,
n = size of input
a = number of subproblems in the recursion
n/b = size of each subproblem. All subproblems are assumed 
     to have the same size.
f(n) = cost of the work done outside the recursive call, 
      which includes the cost of dividing the problem and
      cost of merging the solutions

Here, a ≥ 1 and b > 1 are constants, and f(n) is an asymptotically positive function.
```

An asymptotically positive function means that for a sufficiently large value of n, we have f(n) > 0.

## Master Theorem

If a ≥ 1 and b > 1 are constants and f(n) is an asymptotically positive function, then the time complexity of a recursive relation is given by


``` mathematica
T(n) = aT(n/b) + f(n)

where, T(n) has the following asymptotic bounds:

    1. If f(n) = O(nlogb a-ϵ), then T(n) = Θ(nlogb a).

    2. If f(n) = Θ(nlogb a), then T(n) = Θ(nlogb a * log n).

    3. If f(n) = Ω(nlogb a+ϵ), then T(n) = Θ(f(n)).

ϵ > 0 is a constant.
```

Each of the above conditions can be interpreted as:
![alt text](imagens/image-2.png)

## Solved Example of Master Theorem

``` mathematica
T(n) = 3T(n/2) + n2
Here,
a = 3
n/b = n/2
f(n) = n2

logb a = log2 3 ≈ 1.58 < 2

ie. f(n) < nlogb a+ϵ , where, ϵ is a constant.

Case 3 implies here.

Thus, T(n) = f(n) = Θ(n2) 
```

Master Theorem Limitations
The master theorem cannot be used if:

- T(n) is not monotone. eg. T(n) = sin n
- f(n) is not a polynomial. eg. f(n) = 2n
- a is not a constant. eg. a = 2n
- a < 1


# Divide and Conquer Algorithm
A divide and conquer algorithm is a strategy of solving a large problem by

1. breaking the problem into smaller sub-problems
2. solving the sub-problems, and
3. combining them to get the desired output.

To use the divide and conquer algorithm, recursion is used. Learn about recursion in different programming languages:

- [Recursion in Java](https://www.programiz.com/java-programming/recursion)
- [Recursion in Python](https://www.programiz.com/python-programming/recursion)
- [Recursion in C++](https://www.programiz.com/cpp-programming/recursion)

## How Divide and Conquer Algorithms Work?
Here are the steps involved:

### How Divide and Conquer Algorithms Work?
Here are the steps involved:

1. **Divide**: Divide the given problem into sub-problems using recursion.
2. **Conquer**: Solve the smaller sub-problems recursively. If the subproblem is small enough, then solve it directly.
3. **Combine**: Combine the solutions of the sub-problems that are part of the recursive process to solve the actual problem.
Let us understand this concept with the help of an example.

Here, we will sort an array using the divide and conquer approach (ie. merge sort).

1. Let the given array be:
![alt text](imagens/image-3.png)

2. Divide the array into two halves.
![alt text](imagens/image-4.png)

Again, divide each subpart recursively into two halves until you get individual elements.
![alt text](imagens/image-5.png)

3. Now, combine the individual elements in a sorted manner. Here, conquer and combine steps go side by side.
![alt text](imagens/image-6.png)

## Time Complexity
The complexity of the divide and conquer algorithm is calculated using the master theorem

``` mathematica
T(n) = aT(n/b) + f(n),
where,
n = size of input
a = number of subproblems in the recursion
n/b = size of each subproblem. All subproblems are assumed to have the same size.
f(n) = cost of the work done outside the recursive call, which includes the cost of dividing the problem and cost of merging the solutions
```

Let us take an example to find the time complexity of a recursive problem.

For a merge sort, the equation can be written as:

``` mathematica
T(n) = aT(n/b) + f(n)
     = 2T(n/2) + O(n)
Where, 
a = 2 (each time, a problem is divided into 2 subproblems)
n/b = n/2 (size of each sub problem is half of the input)
f(n) = time taken to divide the problem and merging the subproblems
T(n/2) = O(n log n) (To understand this, please refer to the master theorem.)

Now, T(n) = 2T(n log n) + O(n)
          ≈ O(n log n)
```

## Divide and Conquer Vs Dynamic approach

The divide and conquer approach divides a problem into smaller subproblems; these subproblems are further solved recursively. The result of each subproblem is not stored for future reference, whereas, in a dynamic approach, the result of each subproblem is stored for future reference.

Use the divide and conquer approach when the same subproblem is not solved multiple times. Use the dynamic approach when the result of a subproblem is to be used multiple times in the future.

Let us understand this with an example. Suppose we are trying to find the Fibonacci series. Then,

**Divide and Conquer approach:**

``` cpp
fib(n)
    If n < 2, return 1
    Else , return f(n - 1) + f(n -2)
```

Dynamic approach:

``` cpp
mem = []
fib(n)
    If n in mem: return mem[n] 
    else,     
        If n < 2, f = 1
        else , f = f(n - 1) + f(n -2)
        mem[n] = f
        return f
```

In a dynamic approach, mem stores the result of each subproblem.


## Advantages of Divide and Conquer Algorithm
- The complexity for the multiplication of two matrices using the naive method is O(n3), whereas using the divide and conquer approach (i.e. Strassen's matrix multiplication) is O(n2.8074). This approach also simplifies other problems, such as the Tower of Hanoi.
- This approach is suitable for multiprocessing systems.
- It makes efficient use of memory caches.

## Divide and Conquer Applications
- Binary Search
- Merge Sort
- Quick Sort
- Strassen's Matrix multiplication
- Karatsuba Algorithm
---
layout: post
title:  "Tuple Assignment- Python Tips #1"
date:   2019-01-21 06:00:00
categories: python
permalink: /python/tips/1
---




Python has many cool features. One of them is tuple assignment. This can be used to assign multiple variables in a single line. Not only making code more readable but also simple. The assignment follows simple mechanics where variables on LHS are assigned corresponding elements on RHS. One should also remember that the number of elements on LHS must be equal to RHS as the assignment is element-wise. 

## Examples: 

### Swapping Numbers

A typical code for swapping two numbers would look something as shown below. It required creating a temporary variable and destroying it later. This is some tedious work.

```c
temp = a
a = b 
b = temp 
remove(temp)
```

The same thing can be achieved in python in a single line. 

```python
a,b = b,a
```

This makes the code lot more readable and easy to understand but also beautiful and simple. 


### GCD of two numbers
Swapping numbers is a simple task. Consider code for Calculating GCD (using euclidean algorithm). 

``` python 
def get_gcd(a,b)
	while(b!=0):
		a,b = b, a%b
return b
```
Really cool isn't it? 

### Unpacking from tuple data-structure

You can also perform assignment as follows
```python
name =(surya, prakash, rao)
first_name,last_name,middle_name = name
```

### Assign slices in a list

We can go further and assign indivisual slices of a list as follows.

```python
x = [1,2,3]
y = [3,5,6]
x[0:2] = y[0:2]

# now x =[3,5,3]
```
But be careful when your LHS size is not equal to RHS, it can lead to addition of an extra number which may not be intended. Its important to keep a note of this.
```python
x =[1,2,3]
y = [3,5,6]
x[0:1] =y[0:2]

# now x = [3,5,2,3]
```

## Common mistakes

While the feature is really helpful, people tend to make some common mistakes. One of them is shown below. Where size on both sides is not equal so python is not able to unpack.

```python 
temp = (1,2,3)
a,b = temp
```
Output:
```output
Traceback (most recent call last):
 File "<stdin>", line 1, in <module>
ValueError: too many values to unpack (expected 2)
```
Always remember that you need to have equal number of elements on LHS and RHS to assign properly to avoid this mistake. Below are some tips from zen of python to write good code.

## Zen of Python

Always remember *Zen of Python*:
* Beautiful is better than ugly
* Simple is better than complex
* Readability counts
* If the implementation is hard to explain, it's a bad idea. If the implementation is easy to explain, it may be a good idea.


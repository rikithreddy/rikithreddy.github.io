---
layout: post
title:  "Tuple Assignment- Python Tips #1"
date:   2019-01-21 06:00:00
categories: python
permalink: /python/tips/1
---




Python has many cool features. One of them is tuple assignment which is be used in single line assignment of multiple variables. You would find this feature really interesting as it does not only make your code easy two write but simple to read. The assignment follows simple mechanics where variables on LHS (Left hand side) are assigned corresponding elements on RHS(Right hand side). Its important to note that the number of elements on the LHS should be equal to number of elements on RHS as the assignment is element-wise. Below are few examples on how to use the feature. 

## Examples: 

### Swapping Numbers

A typical code for swapping two numbers looks something as shown below. It involves creating an additional variable to swap the numbers. This temporary variable can be problematic when writing more complex code, making the code difficult to read and understand.

```c
temp = a
a = b 
b = temp 
remove(temp)
```
The same thing can be done in python with tuple assignment, which is more readable and therefore desirable.

```python
a,b = b,a
```
Lets look at something more complex than swapping numbers.

### GCD of two numbers

Below is a simple piece of code you can use to calculate GCD of two numbers. (using euclidean algorithm). 

``` python 
def get_gcd(a,b)
	while(b!=0):
		a,b = b, a%b
return b
```
Really cool isn't it? 

### Unpacking from tuple data-structure

You can also perform assignment using a tuple or a list data structure on the RHS. This can be useful when you want to unpack data of specific format like name as shown below.
```python
name =(surya, prakash, rao)
first_name,middle_name,last_name = name
```

### Assign slices in a list

We can also perform slice assignment in list as show in below. Its simply like a copy paste operation.

```python
x = [1,2,3]
y = [3,5,6]
x[0:2] = y[0:2]
#>> x =[3,5,3]
```
However in this case be careful if LHS size is not equal to RHS, it can lead to addition of an extra number which may not be intended. 
```python
x =[1,2,3]
y = [3,5,6]
x[0:1] =y[0:2]
#>> x = [3,5,2,3]
```
This feature is build following some of the core principle of python dictated by *Zen of python*.

## Zen of Python

Always remember *Zen of Python*:
* Beautiful is better than ugly
* Simple is better than complex
* Readability counts
* If the implementation is hard to explain, it's a bad idea. If the implementation is easy to explain, it may be a good idea.


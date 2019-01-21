---
layout: post
title:  "Tuple Assignment- Python Tips #1"
date:   2019-01-21 06:00:00
categories: python
permalink: /python/tips/1
---




Python has some really cool features. One of them is tuple assignment, which can be used to have multiple variables assigned in a single line. This feature does not only make it easier code but also makes the code more readable. It takes tuple of variables on LHS and assigns them with a tuple of elements *same size*, this operation is performed element wise.

Consider the following example where you want to swap variables. A typical code would look as follows.

```c
temp = a
a = b 
b = temp 
remove(temp)
```

However we can achive the same in python in a single line. This is much more simpler and less tedious.

```python
a,b = b,a
```
Swapping numbers is a simpler task check the code for calculating GCD using euclidean algorithm. Really cool isn't it.

``` python 
def get_gcd(a,b)
	while(b!=0):
		a,b = b, a%b
return b
```

Some other cool uses:
Unpacking a tuple data structure to indivisual variables 
```python
name =(surya, prakash, rao)
first_name,last_name,middle_name = name
```
Slice assignment of lists

```python
x = [1,2,3]
y = [3,5,6]
x[0:2] = y[0:2]

# now x =[3,5,3]
```

While the feature is really helpful people tend to make a common mistake shown below.

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
Always remember that you need to have equal number of elements on LHS and RHS to assign properly to avoid this mistake.

Hope this helps you write better code in python :D
HAPPY CODING!!
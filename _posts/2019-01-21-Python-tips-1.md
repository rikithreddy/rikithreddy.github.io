```c
temp = a
a = b 
b = temp 
remove(temp)
```

```python
a,b = b,a
```


Using euclidean algorithm
``` python 
while(b!=0):
	a,b = b, a%b

```

```python
# name =(surya, prakash, rao)
first_name,last_name,middle_name = name
```

common mistakes
```python 
a,b = (1,2,3)
```

> Traceback (most recent call last):
>  File "<stdin>", line 1, in <module>
> ValueError: too many values to unpack (expected 2)

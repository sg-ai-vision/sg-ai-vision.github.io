```python
# x to the power y
x = 4
y = 2
x**2
```




    16




```python
# Boolean and negatiation
True
not True
```




    False




```python
# and or
True and True
```




    True




```python
True and False
```




    False




```python
# Chaining
1 < 2 < 3
```




    True




```python
# (is vs ==)
a = [1, 2, 3, 4]
b = a
b is a
```




    True




```python
# but if
b = [1, 2, 3, 4]
b is a
```




    False




```python
# but still
b == a
```




    True




```python
# Strings
"Hello" + " World"
```




    'Hello World'




```python
"Hello" " World"
```




    'Hello World'




```python
string = "This is a string."
string[2]
```




    'i'




```python
len(string)
```




    17




```python
# format strings
"{} can be {}".format("Strings", "interpolated")
```




    'Strings can be interpolated'




```python
"{0} is intelligent. {0} is a computer scientist. {0} is a idiot as well.".format("Siddharth", "Siddharth")
```




    'Siddharth is intelligent. Siddharth is a computer scientist. Siddharth is a idiot as well.'




```python
# You can use keywords if you don't if you don't want to count
"{name} wants to eat {food}.".format(food="sandwitch", name="siddharth")
```




    'siddharth wants to eat sandwitch.'




```python
# f-string
name = "Siddharth"
f"he said his name is {name}."
```




    'he said his name is Siddharth.'




```python
f"{name} is {len(name)} characters long."
```




    'Siddharth is 9 characters long.'




```python
# None is an object
None
```


```python
# Don't use == operator to compare objects to none use is instead
"etc" is None

```




    False




```python
None is None
```




    True




```python
# None, 0, empty string "" , [] empty list, dicts tuples all evalues to false
print(bool(0))
print(bool(""))
print(bool([]))
print(bool({}))
print(bool(()))
```

    False
    False
    False
    False
    False



```python
# optional argument to change the end string
print("hello, world", end="!")
```

    hello, world!


```python
# Accessing a previously unassigned variable is an exception
# See control flow to learn more about exception handling
some_unknown_var  # Raises a NameError
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-29-b5451ef97652> in <module>
          1 # Accessing a previously unassigned variable is an exception
          2 # See control flow to learn more about exception handling
    ----> 3 some_unknown_var


    NameError: name 'some_unknown_var' is not defined



```python
# ternary operator in c's equivalant
"yahoo" if 3 > 2 else 2
```




    'yahoo'




```python
# Lists
lst = []
lst.append(2)
print(lst)
lst.append(3)
print(lst)
lst.append(4)
print(lst)
lst.pop()
print(lst)
```

    [2]
    [2, 3]
    [2, 3, 4]
    [2, 3]



```python
# Lists slicing
lst = [1, 2, 3, 4, 5]
lst[1:3] # the start index is included but the end index is not.
print(lst[::2]) # Return list selecting every second entry
print(lst[::-1]) # Return list in reverse order

# lst[start:end:step]
```

    [1, 3, 5]
    [5, 4, 3, 2, 1]



```python
print(lst)
del lst[2] # delete second indexed element from the list
print(lst)
# remove first occurence of a value ==> method
lst.remove(2)
```

    [1, 2, 5]
    [1, 2]



```python
# insert a element at a specific index
lst.insert(2, 6)
print(lst)
```

    [1, 6, 6, 6]



```python
# Get the index of the first item found mathcing the argument
lst.index(1)

# Adding two list
lst1 = [1, 2, 3, 6]
lst2 = [4, 5, 6, 7]
print(lst1 + lst2)
```

    [1, 2, 3, 6, 4, 5, 6, 7]



```python
# concatenate lists with extend()
print(lst1)
print(lst2)
lst1.extend(lst2)   # now lst1 also has the elements of lst2
print(lst1)
print(lst2)
```

    [1, 2, 3, 6]
    [4, 5, 6, 7]
    [1, 2, 3, 6, 4, 5, 6, 7]
    [4, 5, 6, 7]



```python
# item exist in list or not
print(1 in lst1)
print(1 in lst2)
```

    True
    False



```python
# tuples are like list but can't be modified means immutable
tup = (1, 2, 3)
tup1 = ()
tup2 = (1, )
```


```python
# unpacking tuples or lists into variables
a, b, c = (1, 2, 3)
d, e, f = [4, 5, 6]
print(f"{a}, {b}, {c}, {d}, {e}, {f}")
```

    1, 2, 3, 4, 5, 6



```python
# extend unpacking
a, *b, c = (1, 2, 3, 4)
print(a, b, c)
```

    1 [2, 3] 4



```python
# Swapping two values in python3
print(a, b)
a, b = b, a
print(a, b)
```

    [2, 3] 1
    1 [2, 3]



```python
# dictionaries stores mapping from keys to values

dict1 = {'one': 1, 'two': 2}
# keys for dicts have to be immutable type : int floats strings, tuples.
dict2 = {[1, 2, 4]: 2} # raises type error
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-63-735dcc871b75> in <module>
          3 dict1 = {'one': 1, 'two': 2}
          4 # keys for dicts have to be immutable type : int floats strings, tuples.
    ----> 5 dict2 = {[1, 2, 4]: 2} # raises type error


    TypeError: unhashable type: 'list'



```python
dict1['one'] # looking up values using keys
```




    1




```python
dict1.keys()
list(dict1.values())
list(dict1.keys())
```




    ['one', 'two']




```python
# looking for non-existing key gives key-error
dict1["three"]
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    <ipython-input-69-ae90fdd068e7> in <module>
          1 # looking for non-existing key gives key-error
    ----> 2 dict1["three"]


    KeyError: 'three'



```python
# To avoid key error user get()
dict1.get('two')     # if key exists it outputs the values
```




    2




```python
# otherwise it outputs None
print(dict1.get('three'))

# get method also supports a argument in case key not present in the dict
print(dict1.get('one', 3))
print(dict1.get('three', 3))
```

    None
    1
    3



```python
# setdefualt() method => inserts the key into the dict when it is not present
print(dict1)
dict1.setdefault('three', 3)
```

    {'one': 1, 'two': 2}





    3




```python
print(dict1)
# now 'three' key is here
dict1.setdefault('three', 5) # dict['three'] is 3
```

    {'one': 1, 'two': 2, 'three': 3}





    3




```python
# adding to a dictionary
# Method 1:
dict1.update({"four": 4})
print(dict1)
# Method 2:
dict1['five'] = 5
print(dict1['five'])
```

    {'one': 1, 'two': 2, 'three': 3, 'four': 4, 'five': 5}
    5



```python
# removing keys from dicts
del dict1['five']
print(dict1)
```

    {'one': 1, 'two': 2, 'three': 3, 'four': 4}



```python
# Sets
new_set = set()
print(new_set)
type(new_set)
```

    set()





    set




```python
new_set = {1, 2, 3, 6, 5, 6} # sets don't have duplicate item
print(new_set)  # elements of a set have to immutable

invalid_set = {[1], 2}
```

    {1, 2, 3, 5, 6}



    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-89-89822274db58> in <module>
          2 print(new_set)  # elements of a set have to immutable
          3
    ----> 4 invalid_set = {[1], 2}


    TypeError: unhashable type: 'list'



```python
# Adding elements to a set
alpha_set = new_set
alpha_set.add(7)
print(alpha_set)
```

    {1, 2, 3, 5, 6, 7}



```python
## Imp --------------------------------------->
union = {1, 2, 3, 4} | {5, 6, 7, 3} # union
print(union)
```

    {1, 2, 3, 4, 5, 6, 7}



```python
# set difference with -
set_diff = {1, 2, 3, 4} - {1, 4, 5}
print(set_diff)
```

    {2, 3}



```python
# set symmetric difference with ^
sym_diff = {1, 2, 3, 4} ^ {5, 3, 4, 7}
print(sym_diff)
```

    {1, 2, 5, 7}



```python
# checking if set on left is superset of the set on right
{1, 2, 3, 4, 5} >= {3, 4}
```




    True




```python
# checking if set on left is subset of the set on right
{1, 2, 3, 4, 5} <= {3, 4}
```




    False




```python
# existece of element in set
2 in set_diff
```




    True




```python
# make a one layer deep copy
set1 = {1, 2, 3, 4}
set2 = set1.copy()
print(set1 == set2)
print(set1 is set2)
```

    True
    False



```python

```

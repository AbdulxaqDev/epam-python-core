# EPAM(Pyth0n)

## Introduction

1. P**rogramming paradigm**
 (object-oriented, procedural, or functional), 
2. C**onversion type**
 (interpreted or compiled),
3. T**yping style**
 (static or dynamic and strong or weak)

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled.png)

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%201.png)

We have to creaet SSH key that enables gitlab do not ask credentials every time, when we use hitlab.

For thet we have run eval "$(ssh-agent -s)” on gitbash, this generates a SSH key, we can tap Enter, when it asks questions.

And when we go to /c/Users/Abdulkhak/.ssh/ there would be created ida_rsa.pub file, which contains SHH key, we should open it with Notepad and copy the key in it and past it in GitLab on SHH key section and  add the key.

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%202.png)

## M3: Data Types

****L0: Module Introduction****

### ****L1: Data Types Overview****

**Numeric** is the data that has a numeric value. There are three different types in Python: integer, floating-point number, and complex number. Also, Boolean is a subtype of an integer. **Integer type** allows you to work with positive or negative whole numbers. **Float type** provides floating-point representation. **Complex** is specified as (real part) + (imaginary part), for example - 4+5j.

**Code**

`a = 10
b = 10.5
c = 8+3j
print(type(a))
print(type(b))
print(type(c))`

**Result**

`<class 'int'>
<class 'float'>
<class 'complex'>`

**String** is a text sequence of character data.

**Code**

`my_str = "This is string!"
print(type(my_str))`

**Result**

`<class 'str'>`

**List** is a sequence of the elements inside square brackets [ ], separated by commas. The number and type of list elements are not limited.

**Code**

`some_list = [1, 2.5, True, "Str in a list"]
print(type(some_list))`

**Result**

 `<class 'list'>`

**Set** is an unordered collection of exclusive items (no duplicates) separated by commas inside {}.

**Code**

`our_set = {4, 3, 6.6, "Hello"}
print(type(our_set))`

**Result**

 `<class 'set'>`

**Dictionary** is a mapping of key-value pairs separated by commas inside {}.

**Code**

`another_dict = {"message": "Hi!", 33: True}
print(type(another_dict))`

**Result**

 `<class 'dict'>`

****Mutable and Immutable Objects****

**Mutable Objects**

In Python, some objects can change after their creation. They are called **mutable objects**. For example, objects whose type is a list or dictionary are mutable.

Conversely I**mmutable Objects**
 can't change after creation. Examples of immutable types: integer, float, string, tuple, set.

In Python, every object has a unique identifier, and you can use another built-in function id() to get it. As you can see in the example below, after changing, the variable a has another id. That means that the variable name stays the same. But after changing, it refers to another object in memory.

**Code**

`a = 1
print(id(a))

a += 2
print(id(a))`

**Result**

`9756224
9756288`

In another example with the list, the id of the object is the same after appending a new item in a list.

**Code**

`my_list = [1, 2]
print(id(my_list))

my_list.append(3)
print(id(my_list))`

**Result**

`22521882389504
22521882389504`

It is highly recommended you remember the mutable or immutable types because mutable objects can be a reason for complicated mistakes. For example, you can inadvertently change a parameter inside a function, which will affect the value outside the function. This can be unexpected and confusing.

### ****L2: Numbers****

As mentioned before, there are **three different types of numbers in Python: integer, float,**
 and **complex**. All these types are immutable so let's get to know them in more detail.

**Random**

The random module provides functions for generating random numbers, letters, and the random selection of elements from sequences.

You should note that these numbers are not truly random. It calls pseudorandom numbers, which means that the module uses special mathematical algorithms to produce numbers that are "random enough".

Imagine, you want to play DND with friends, but you have lost the cube. No problem, the random module can help you, and this is an example solution:

**Code**

`import random

x = 0
y = 6
print(random.randint(x, y))
print(random.randint(x, y))
print(random.randint(x, y))`

**Result**

`0
2
6`

In the end, take a look at a small list of interesting functions:

- choice(sequence) - returns a random element of a non-empty sequence.
- randrange(start, stop, step) - returns a randomly selected number from a sequence.
- random() – returns a random number from 0 to 1.
- seed([a], version=2) – the initialization of the random number generator. If a is not specified, the system time is used.
- shuffle(sequence, [rand]) - shuffles the sequence (changes the sequence itself). Therefore, the function does not work for immutable objects.
- uniform(x, y) – returns a random floating-point number from x to y.

For more information, discover the documentation at [docs.python.org](https://docs.python.org/3/library/random.html).

# **Lesson Summary**

There are **three different types of numbers in Python: integer, float,** and **complex**. All are immutable.

In Python, zero, positive, or negative integer numbers without a fractional part are type int. Integers have unlimited precision and can take on large values. All integer literals or variables are objects of the int class. The value of the int type is an immutable object.

Floating point numbers (type float) are also called real numbers. They are positive and negative digits with a fractional part denoted by the decimal symbol or the scientific notation E or e.

A complex number consists of two floating-point numbers representing real and imaginary parts. Both parts of the complex object x are read-only and are accessed by the attributes of x. real and x. imag.

Be sure that you are familiar with the variety of arithmetic and assignment operators, and the built-in functions from the Python modules math and random.

### L3: Boolien

Python has three **boolean** operators – **and** **or**, and **not**.

But in Python 3.10, you can use another solution—a match/case construction (pattern matching). It may be more suitable for such cases because the result code is more readable.

`my_operation = "read" 
match my_operation: 
    case "read": 
        print("perform read operation…") 
    case "update": 
        print("perform update operation …") 
    case "insert": 
        print("perform insert operation …") 
    case "delete": 
        print("perform delete operation …") 
    case _: 
        print("wrong variant if operation !!!")`

# **Lesson Summary**

To write some logical expressions, you should combine comparison and boolean operators. The result of logical expressions is always defined as True or False. Usually, logical expressions are used when you want to perform certain operations, but only in case some conditions are satisfied. For this purpose, Python has flow control statements you can combine with logical expressions.

The Boolean type in Python contains only two values: True and False. The Boolean type is represented by the **bool** class. **In Python, everything can be converted to bool.**

### ****L4: Loops****

Python has two different loop constructions/operators: while and for. while construction is used in pair with the condition. The loop runs while the condition expression is True. The second construction that Python allows you to use for loop organizing is the for statement. In Python, the for operator is designed to use sequences and collections. That's why you can use the built-in function range that generates a sequence of numbers.

**The iterator pattern** (or **iterator protocol**) is important because you can use the for statement with any iterable object. In other words, with any object that implements the **iterator** protocol.

### L5: String

This is an example of how to revert a string. The step point is set up to -1. Python interprets the slice like every item from the end to the beginning.

**Code**

`print(my_str[::-1])`

**Result**

`olleH`

**split**

The split method takes another string as a separator and returns a list of parts of the string:

**Code**

`my_str = "Hello-world"
for i in my_str.split("-"):
    print(i)`

**Result**

`Hello
world`

**upper and lower**

The upper and lower methods return strings converted into upper and lower case:

**Code**

`my_str = "Hello-world"
print(my_str.upper())
print(my_str.lower())`

**Result**

`HELLO-WORLD
hello-world`

**find**

The find method searches a specified substring and returns the start position of this substring or -1:

**Code**

`my_str = "Hello-world"
print(my_str.find("world"))`

**Result**

`6`

**strip**

The strip method returns a string without leading and trailing spaces:

**Code**

`my_str = " Hello-world "
print(my_str.strip())`

**Result**

`"Hello-world"`

# **Lesson Summary**

A string in Python is one or more characters enclosed in single or double quotes. Class str represents the data type string in Python. A string is an immutable sequence of characters. You can get characters from a string by index, but you can't change it.

Python has advanced slicing functionality from strings and other sequences such as tuples, lists, ranges, or bytes.

The str class has several methods that can be called simply through a dot with any string.

Even though Python supports string concatenation, it does not work with different types and requires conversion to a string. Therefore, using the format method instead of concatenation is better.

If you need to check the occurrence of one string in another, you can create a conditional construct with the in operator.

### L6: Lists

**len**

Also, you can get the list length by using the common method len:

**Code**

`print(len(some_numbers))`

**Result**

`10`

**extend**

The extend method allows you to add all the items from another iterable object, for example, from another list or string:

**Code**

`some_list = [1, 2, 3]
some_str = "abc"
some_list.extend(some_str)
print(some_list)`

**Result**

`[1, 2, 3, 'a', 'b', 'c']`

**count**

Since the list data type allows for duplication, the count method allows you to count the number of times something appears in the list:

**Code**

`x = 1
some_list = [1, 2, 3, 2, 1, 1]
print(some_list.count(x))`

**Result**

`3`

**pop**

The pop method allows the removal and returning of items from a list by the given index. If an index is not specified, it removes and returns the last item in a list. This method allows the use of a list as a stack:

**Code**

`my_stack = [1, 2, 3]
my_stack.append(4)
my_stack.append(5)
print(my_stack.pop())
print(my_stack.pop())
print(my_stack)`

**Result**

`5
4        
[1, 2, 3]`

# **Lesson Summary**

In general, the list is simple and flexible in use. And in most cases, it will be enough if you need an ordered and dynamic size collection. But you should consider that list is a mutable type.

If you know that you will not change the sequence after its initialization, use an immutable sequence. For example, it could be a tuple that will be reviewed in the next lesson.

Finally, lists can be ineffective with big data sets, for example, millions of items. So, if you have such a case, maybe you should use special libraries like NumPy or Pandas.

### ****L7: Tuples****

# **Packing and Unpacking**

The definition of packing and unpacking is essential to understanding Python. This lesson will only touch on this topic. You will dive deeper into packing and unpacking later in the course, after becoming familiar with dictionaries and functions, where you will meet many new concepts. But this topic is essential for a clear understanding of tuples because tuple packing and unpacking are often done implicitly in Python.

# **Unpacking Operation**

Let's take a look at the example:

*Click the arrows to navigate through the items below.*

**Code**

`(a, b, c) = (40, 56.6, 90)
print(a, b, c)`

**Result**

`40 56.6 90`

It happens because the tuple (40, 56.6, 90) is implicitly split into the separate values - 40, 56.5, and 90.

It is called an **unpacking operation**.

You can reproduce this with a special **unpacking operator ***:

*Click the arrows to navigate through the items below.*

**Code**

`my_tuple = 40, 56.6, 90
print(my_tuple)
print(*my_tuple)`

**Result**

`(40, 56.6, 90)
40 56.6 90`

Please note that in the first case, it was printed exactly as the tuple, so you can see the brackets.

# **Swapping Two Values**

And one more interesting example. Have you ever done a task when you should swap values from two variables?

*Click each tab to see more information.*

**Solution With Additional VariableSolution With Unpacking and Packing**

But in Python, it can be solved much easier thanks to unpacking and packing. Then, only one action instead of three is the best solution.

**Code**

`a, b = 1, 2
print(a, b)

b, a = a, b
print(a, b)`

**Result**

`1 2
2 1`

To create a tuple with one element, you must add an extra comma at the end:

`it_should_be_tuple = (1,)`

You can process tuples as you would lists or strings.

### **L8: Sets**

Also, you can initiate a set using curly braces:

`my_set = {1, 113.5, True, "Some string"}`

But you should consider that you will not get a set if you initialize an empty set with curly braces.

Curly braces without data will initialize a dictionary:

**Code**

`my_set = {}
print(type(my_set))`

**Result**

`<class 'dict'>`

So, for this purpose, you must use the function set.

**Code**

`my_set = set()
print(type(my_set))`

**Result**

`<class 'set'>`

**Sets are iterable……**

You can iterate over the elements of sets with a for loop just as you would with lists or tuples.

`for item in my_set:
    print(item)`

**but there is no access to the elements**

There is no arbitrary access to the elements of sets through indexes because they are unordered.

`print(my_set[1])
>>> TypeError: 'set' object is not subscriptable`

**Hash Value for Tuple**

Because tuple is an immutable type, you can get a hash value for this object:

**Code**

`some_tuple = (1, 2, 3)
print(hash(some_tuple))`

**Result**

`529344067295497451`

**Hash Value for List**

But it does not work, for example, for the list that is a mutable type:

**Code**

`some_list = ["a", "b", "c"]
print(hash(some_list))`

**Result**

`TypeError: unhashable type: 'list'`

As you can see, a hash is just some integer value. Most importantly, this value will be unchanged, even if the internal state of the object has changed.

**Union Operation**

The first set operation **union**, with **operator**:

**Code**

`s1 = {"a", "d", "h"}
s2 = {"n", "b", "c", "d"}
s3 = {"c", "d"}
union = s1 | s2 | s3
print(union)`

And another way with a **method**:

**Code**

`s1 = {"a", "d", "h"}
s2 = {"n", "b", "c", "d"}
s3 = {"c", "d"}
union = s1.union(s2, s3)
print(union)`

For both variants the resulting set contains all the elements from s1, s2, and s3 without duplicates.

**Result**

`{'h', 'a', 'n', 'b', 'd', 'c'}`

Next set operation **intersection**, with **operator**:

**Code**

`s1 = {"a", "d", "h"}
s2 = {"n", "b", "c", "d", "a"}
s3 = {"n", "a", "d"}
my_intersection = s1 & s2 & s3
print(my_intersection)`

And another way with a **method**:

**Code**

`s1 = {"a", "d", "h"}
s2 = {"n", "b", "c", "d", "a"}
s3 = {"n", "a", "d"}
my_intersection = s1.intersection(s2, s3)
print(my_intersection)`

The result set contains the elements presented in each specified set, and it is similar for both variants.

**Result**

`{'a', 'd'}`

And the third set operation **difference**, with **operator**:

**Code**

`s1 = {"a", "d", "h", "c", "j"}
s2 = {"n", "b", "c", "d", "a"}
s3 = {"n", "a", "d"}
my_difference = s1 - s2 - s3
print(my_difference)`

And another way with a **method**:

**Code**

`s1 = {"a", "d", "h", "c", "j"}
s2 = {"n", "b", "c", "d", "a"}
s3 = {"n", "a", "d"}
my_difference = s1.difference(s2, s3)
print(my_difference)`

The result set contains items from the first set that are not presented in other sets.

**Result**

`{'h', 'j'}`

**Update Method**

The update method changes the value of the original set to the union with the specified sets:

**Code**

`s1 = {"a", "b", "k"}
s2 = {"a", "d", "h"}
s3 = {"n", "b", "d"}

s1.update(s2, s3)
print(s1)`

**Result**

`{'d', 'a', 'h', 'b', 'k', 'n'}`

The intersection_update and the difference_update methods work similarly, but with intersection and difference, respectively.

**Add and Remove Methods**

Also, you can just **add** an item to the set, or **remove** it:

**Code**

`s1 = {"a", "d", "h"}
s1.add("some string")
s1.remove("a")
print(s1)`

**Result**

`{'some string', 'd', 'h'}`

### ****L9: Dictionaries****

### **Dictionary Data Type**

A dictionary is a Python implementation of a data structure, commonly known as a hash table or associative array, that will be discussed in detail in the lesson later.

A **dictionary** is an associative array where arbitrary keys are mapped to values. It’s a mutable data type and may contain other data types and other dictionaries as a value.

There are two ways to create a dictionary.

You can use curly braces to create a dictionary. Pairs in the dictionary are separated by commas. And a colon separates the key from the value:

**Code**

`d = {
    "name": "Filip",
    "age": 32,
    "is_registered": False,
    "rate": 12.5,
    "total_score": 200,
    "linked_ids": [1, 45, 98]
}
print(type(d))`

**Result**

`<class 'dict'>`

**Built-In Function dict()**

An alternative way to initialize a dictionary is to use the built-in function dict():

**Code**

`d2 = dict([(1, "foo"), (10, "bar")])
print(d2)`

**Result**

`{1: 'foo', 10: 'bar'}`

The dict() function can receive a sequence of key-value pairs—for example, a list of tuples.

The dictionary supports iteration by for loop:

Here is the example of iteration:

**Code**

`for pair in d.items():
    print(pair)`

**Result**

`('name', 'Filip')
('age', 33)
('is_registered', False)
('rate', 12.5)
('total_score', 200)
('linked_ids', [1, 45, 98])`

The same can be implemented in such a way:

**Code**

`for key, value in d.items():
    print((key, value))`

**Result**

`('name', 'Filip')
('age', 33)
('is_registered', False)
('rate', 12.5)
('total_score', 200)
('linked_ids', [1, 45, 98])`

And membership check:

`if "preferences" in d and d["preferences"]:
    print(d["preferences"])`

**get() method**

The get() method takes a key as a parameter and returns the value by this key. The method doesn't raise an error if the key doesn't exist:

`print(d.get("preferences"))`

By default, it returns None if a key doesn't exist. But you can specify this value with an additional optional parameter:

`print(d.get("preferences", "There is nothing!"))`

**items() method**

The items() method returns the iterable object dict_items where each element is a tuple of the form (key, value):

**Code**

`for pair in d.items():
    print(pair)`

**Result**

`('name', 'Filip')
('age', 33)
('is_registered', False)
('rate', 12.5)
('total_score', 200)
('linked_ids', [1, 45, 98])`

**keys() and values() methods**

The keys() method returns a dict_keys object which contains keys from a dictionary and the values() method returns dict_values object with values of a dictionary. Both these objects are sequence objects:

**Code**

`for key in d.keys():
    print(key)`

**Result**

`name
age
is_registered
rate
total_score
linked_ids`

The update() method takes another dictionary or some collection of key-value pairs as an argument and updates all matching pairs in the original dictionary and adds key-value pairs for keys that don’t exist in the original dictionary:

**Code**

`blank_d = {
    "name": "",
    "age": 0,
    "is_registered": False,
    "rate": 0,
    "total_score": 0,
    "linked_ids": []
}

**d.update(blank_d)**
print(d)`

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%203.png)

## M4: Functions

### **Python Built-In Functions**

Python has several functions built into an interpreter that are always available.

| https://docs.python.org/3/library/functions.html#abshttps://docs.python.org/3/library/functions.html#aiterhttps://docs.python.org/3/library/functions.html#allhttps://docs.python.org/3/library/functions.html#anyhttps://docs.python.org/3/library/functions.html#anexthttps://docs.python.org/3/library/functions.html#ascii
B https://docs.python.org/3/library/functions.html#binhttps://docs.python.org/3/library/functions.html#boolhttps://docs.python.org/3/library/functions.html#breakpointhttps://docs.python.org/3/library/functions.html#func-bytearrayhttps://docs.python.org/3/library/functions.html#func-bytes
C https://docs.python.org/3/library/functions.html#callablehttps://docs.python.org/3/library/functions.html#chrhttps://docs.python.org/3/library/functions.html#classmethodhttps://docs.python.org/3/library/functions.html#compilehttps://docs.python.org/3/library/functions.html#complex
Dhttps://docs.python.org/3/library/functions.html#delattrhttps://docs.python.org/3/library/functions.html#func-dicthttps://docs.python.org/3/library/functions.html#dirhttps://docs.python.org/3/library/functions.html#divmod | Ehttps://docs.python.org/3/library/functions.html#enumeratehttps://docs.python.org/3/library/functions.html#evalhttps://docs.python.org/3/library/functions.html#exec
Fhttps://docs.python.org/3/library/functions.html#filterhttps://docs.python.org/3/library/functions.html#floathttps://docs.python.org/3/library/functions.html#formathttps://docs.python.org/3/library/functions.html#func-frozenset
Ghttps://docs.python.org/3/library/functions.html#getattrhttps://docs.python.org/3/library/functions.html#globals
Hhttps://docs.python.org/3/library/functions.html#hasattrhttps://docs.python.org/3/library/functions.html#hashhttps://docs.python.org/3/library/functions.html#helphttps://docs.python.org/3/library/functions.html#hex
Ihttps://docs.python.org/3/library/functions.html#idhttps://docs.python.org/3/library/functions.html#inputhttps://docs.python.org/3/library/functions.html#inthttps://docs.python.org/3/library/functions.html#isinstancehttps://docs.python.org/3/library/functions.html#issubclasshttps://docs.python.org/3/library/functions.html#iter | Lhttps://docs.python.org/3/library/functions.html#lenhttps://docs.python.org/3/library/functions.html#func-listhttps://docs.python.org/3/library/functions.html#locals
Mhttps://docs.python.org/3/library/functions.html#maphttps://docs.python.org/3/library/functions.html#maxhttps://docs.python.org/3/library/functions.html#func-memoryviewhttps://docs.python.org/3/library/functions.html#min
Nhttps://docs.python.org/3/library/functions.html#next
Ohttps://docs.python.org/3/library/functions.html#objecthttps://docs.python.org/3/library/functions.html#octhttps://docs.python.org/3/library/functions.html#openhttps://docs.python.org/3/library/functions.html#ord
Phttps://docs.python.org/3/library/functions.html#powhttps://docs.python.org/3/library/functions.html#printhttps://docs.python.org/3/library/functions.html#property | Rhttps://docs.python.org/3/library/functions.html#func-rangehttps://docs.python.org/3/library/functions.html#reprhttps://docs.python.org/3/library/functions.html#reversedhttps://docs.python.org/3/library/functions.html#round
Shttps://docs.python.org/3/library/functions.html#func-sethttps://docs.python.org/3/library/functions.html#setattrhttps://docs.python.org/3/library/functions.html#slicehttps://docs.python.org/3/library/functions.html#sortedhttps://docs.python.org/3/library/functions.html#staticmethodhttps://docs.python.org/3/library/functions.html#func-strhttps://docs.python.org/3/library/functions.html#sumhttps://docs.python.org/3/library/functions.html#super
Thttps://docs.python.org/3/library/functions.html#func-tuplehttps://docs.python.org/3/library/functions.html#type
Vhttps://docs.python.org/3/library/functions.html#vars
Zhttps://docs.python.org/3/library/functions.html#zip
—https://docs.python.org/3/library/functions.html#import__ |
| --- | --- | --- | --- |

### ****L3: Design Concept****

### **Isolation**

The function should be independent of outside things. Arguments and return statements are used for external dependencies to a small number of well-known places in your code.

### **Mutable Arguments**

Don’t change mutable arguments unless the main idea of the function is to change it. Functions that change passed objects create lots of coupling.

### **Single Purpose**

Each function should do one thing that can be described in a simple sentence. Suppose that sentence is comprehensive ("the function implements the whole program") or contains lots of conjunctions (e.g., "this function does one thing and one more"). Then, you better think about splitting it into separate and simpler functions. Otherwise, it might not be easy to re-use it.

### **Relatively Small**

The function should be relatively small. If your functions start spanning multiple pages or have several hundred code lines, it's probably time to split them.

### **Lesson Summary**

You learned the main rules of task decomposing and how big in size functions should be:

- The function should be independent of outside things.
- Each function should do one thing.
- The function should be relatively small.

### ****L4: Lambda Functions****

### ***What is a Lambda Function?***

In some cases, you might need one statement function used only in one place in your program. There is a lambda function in Python for such situations.

The **lambda function** is an anonymous inline function consisting of a single expression which is evaluated when the function is called*.*

*Example:*

```python
nums = [2, 4,  85, 89 ,8, 16, 12]
divider_lambda = lambda n: n/2
divider = lambda nums: [divider_lambda(n) for n in nums]
print(divider(nums))
```

**map(function, iterable)**

map(function, iterable) returns an iterator that applies a function to every item of the iterable.

Imagine you need to square all elements of the list

```python
>>> nums = [48, 6, 9, 21, 1]
>>> square_all = map(lambda num: num ** 2, nums)
>> square_all  # map returns an iterable object
<map object at 0x000002951E273CA0>

>>> list(square_all)
[2304, 36, 81, 441, 1]
```

**filter(function, iterable)**

filter(function, iterable) returns an iterator from elements of the iterable for which the function returns True. If the function is None, the identity function is assumed; that is, all elements of the iterable that are false are removed.

Please, note the differences between filter(function, iterable) and filter(None, iterable):

- filter(function, iterable) is equivalent to the condition [item for item in the iterable if function(item)].
- filter(None, iterable) is equivalent to the condition [item for item in the iterable if item].

For example, let’s get only even numbers from the list.

```python
>>> nums = [48, 6, 9, 21, 1, 35, 16, 12, 0, -1]
>>> list(filter(lambda num: num % 2 == 0, nums))
[48, 6, 16, 12, 0]
```

In case you provide None as a function, there will be the following result:

```python
>>> list(filter(None, nums))
[48, 6, 9, 21, 1, 35, 16, 12, -1]  # 0 was removed
```

### **Lesson Summary**

In some cases, you might need one statement function used only in one place in your program. There is a **lambda function** in Python for such situations. As a regular function, lambda receives a set of arguments as input. A statement is a legal Python expression. By default, lambda returns a result of the statement. If the function gets a callable input argument (function), you can easily leverage a lambda for this argument. For example, sort, map, reduce, or filter.

### ****L5: Recursions****

Devide and concure

### ****L6: Namespaces****

In Python **a namespace**
 is the place where a variable is stored. Namespaces are implemented as dictionaries, where keys are the object names, and the values are the objects themselves.

Python itself maintains a namespace in the form of a Python dictionary, where keys are the object names, and the values are the objects themselves.

In Python, there are four types of namespaces:

- Build-in
- Global
- Enclosed
- Local

### **Built-In Namespace**

Namespaces have differing lifetimes. As Python executes a program, it creates namespaces as necessary and deletes them when they're no longer needed. So typically, many namespaces will exist at any given time.

**The built-in namespace** contains the names of all of Python's built-in objects.

It is created when you start the Python interpreter and exists as long as it runs. Names from this namespace are available at all times when Python is running. You can observe objects from the built-in namespace with the command dir(__builtins__).

### **Global Namespace**

The global namespaces are created when the main program body starts and remains until the interpreter terminates.

**The global namespaces** contain names at the level of the main program.

The interpreter also creates a global namespace for any module your program loads with the import statement. Different namespaces can exist at the same time and be completely isolated. Hence, the same name that may exist in different modules doesn't collide.

collide - to’qnashmoq

### **Enclosed and Local NameSpaces**

For each function, the interpreter creates a new namespace that is local to that function and exists until the function terminates. As you remember, the function is a named set of statements. It means you can also define one function inside another.

### **LEGB Rule**

So, multiple separate namespaces can exist during program execution. Therefore, you can conclude that several instances of a particular symbolic variable name can exist simultaneously in different namespaces during the program execution. Because every instance belongs to a different namespace, they are all maintained separately and won't interfere with each other.

Imagine that you refer to the name a in your code. And the name a exists in several namespaces. The concept of scope helps Python to understand which one you mean.

**The scope of the name** is the program's scope in which this given specified name has a meaning.

The interpreter determines it during the runtime based on the name definition place and name referencing place in the code. So, in case you are referring to the variable a, the interpreter searches for a name a from the inside out, looking in the Local, Enclosing, Global, and finally in the Built-in scope, also known as a **LEGB rule**

### **Lesson Summary**

**A namespace** is a collection of unique names and information about the object each name references. Python uses namespaces to be able to track all symbolic names so that they don't interfere with one another.

In Python, there are four types of namespaces: built-in, global, enclosing, and local.

**The built-in namespace** contains the names of all of Python's built-in objects. The Python interpreter creates the built-in namespace when it starts and it remains in existence until the interpreter terminates it.

**The global namespaces** contain names at the level of the main program. This namespace is created when the main program body starts and remains until the interpreter terminates it.

**The local namespace and the enclosing namespace** remain until the corresponding function terminates.

Several instances of a particular symbolic variable name can exist simultaneously in different namespaces during the program execution.

**The scope of the name** – is the program's scope in which this given specified name has a meaning.

The interpreter searches for a name from the inside out, looking in the Local, Enclosing, Global, and finally in the Built-in scope – it is called the LEGB rule.

### ****L7: Scopes****

****Namespaces vs. Scopes****

A **namespace**
 is a dictionary for mapping symbolic names to their values. When you do any assignment, you are, in fact, updating a namespace dictionary. When you refer to an object by its name, Python looks through a list of several namespaces trying to find one with the name as a key.

A **scope**
, in comparison, defines which namespaces will be looked in and in what order. The scope of any reference always starts in the local namespace and moves outwards until it reaches the module's global namespace before moving on to the built-ins, which is the last level of namespaces.

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%204.png)

A namespace is a dictionary for mapping symbolic names to their values. A scope, in comparison, defines which namespaces will be looked in and in what order.

****Lesson Summary****

"Scope" is a rule for finding bindings (value with assigned name), while "namespaces" are a dictionary for storing all variables. The Python interpreter provides two built-in functions: globals() and locals() that allow you to access global and local namespace dictionaries.

**A hash table** is a data structure that stores a collection of key-value pairs.

### L8: Closures

### **Closure**

Let's talk about closures because you know the nested functions and how to modify variables outside the function's local scope.

The **closure** is a technique for implementing lexically scoped name binding. Operationally, a closure is a record storing a function together with an environment. The environment is a mapping associating each free variable of the function (variables that are used locally, but defined in an enclosing scope) with the value or reference to which the name was bound when the closure was created. Unlike a plain function, a closure allows the function to access those captured variables through the closure's copies of their values or references, even when the function is invoked outside their scope.

### ****L9: Decorators****

### **Design Patterns**

In software engineering, **design patterns** represent some of the best practices adopted by experienced software developers. Each pattern is like a blueprint that you can customize to solve a particular design problem in your code.

**A software design pattern** is a general, reusable solution to a commonly occurring problem within a given context in software design.

Decorators are a helpful tool in Python because they allow programmers to modify a function's behavior without modifying a function's code. The definition of a decorator is quite simple:

"**A decorator** is a function that takes in a function as an input argument and returns a supplemented copy of that function.

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%205.png)

```python
# decorator functions with decorator maker functions

def recipe_decorator_maker(recipe):
	def decorator(func):
			def wrapper(arg1):
				print(recipe)
				return func(arg1)
			return wrapper
	return decorator

@recipe_decorator_maker("milk")
@recipe_decorator_maker("sugar")
@recipe_decorator_maker("cacao")
def make_coffee(coffeetype):
	print(coffeetype)

make_coffee("Latte")

# => milk
# => sugar
# => cacao
# => Latte
```

### **Saving Values Between Decorated Function Calls**

There is one more interesting case of using decorators, to **save values between decorated function calls**. Let's create a decorator to save the number of calls for the decorated function.

### **Lesson Summary**

**A software design pattern** is a general, reusable solution to a commonly occurring problem within a given context in software design. **A decorator** is one pattern among an extensive library of design patterns already implemented in Python. **A decorator** is a function that takes in a function as an input argument and returns a supplemented copy of that function

Decorators can be nested and decorators allow you to increase/expand the already implemented functionality. You can also pass arguments to the decorated function or the decorator itself.

## M5: Modules and Packages

Modules and packages refer to modular programming. According to this concept, large tasks are broken into smaller manageable subtasks or modules. These small pieces can be combined to create complex applications. Splitting large applications into smaller parts brings the following benefits:

- Readability
- Maintainability
- Reusability
- Manageability

### ****L1: Modules****

### **What are Modules?**

It is essential to know that the modules as packages can be written not only in Python but also in C/C++ language (in the case of using CPython by default) or in Java (when using Jython). It depends on the Interpreter,as to which one you use. These modules are included in the standard library.

The module is just a program file without executed but callable code. Methods are not called inside modules like starting a web server or creating a file on the OS file system.

The advantages of storing code in modules are the ability to:

- reusability of code (DRY principle—Don't Repeat Yourself);
- easier debugging;
- readability;
- easier to avoid collisions between namespaces.

**1. Importing Whole Module**

You can import the whole module using the "import" statement. To do it, you should use the following formula:

`import [module name]`

Let's import the module time from Python's standard library:

`import time`

You have imported the time into your code in the above example, so now you can access all the time functions in your main program. Suppose you use the sleep() method in the time module. You can do so using the following code:

`time.sleep(3)  # method sleep() is used from Python's standard module time`

Also, you can use multiple imports:

`import time
import random`

You can use multiple imports in one line. But this option violates the [PEP8 standard](https://www.python.org/dev/peps/pep-0008/#imports) because imports should usually be on separate lines.

`import time, random # Wrong`

**2. Importing Only Some Methods**

You can import not just the whole module, but only some methods that you need. In this case, you should use the from statement:

`from [module name] import [function or value]`

Suppose you only want to import the sleep() function from the time module into your code. You can do so in the following way:

`from time import sleep`

Try to avoid the symbol * in imports because it can violate the program namespace in the same cases.

`from time import *  # Wrong`

Imagine you want to get the time in seconds because the epoch is a floating-point number. Python will call the method from the last import, and because the datetime module also has a time method, that method will be called.

**3. Importing With Module Aliases**

You can use imports with module aliases. To do it, you should use the following formula:

`from [module name] import [function or value] as [your module alias]`

or

`import [function or value] as [your module alias]`

Sometimes, the names of your methods, classes, or modules can be the same in a code. To not violate the program namespace, you can alias your imports:

`from time import time as t_time
from datetime import time as dt_time`

Or in this case, you can call these methods by using aliases.

`print(t_time())  # return ~1645494821.7695844
print(dt_time())  # return 00:00:00`

In addition, there are two types of imports. The first is **absolute**, when you write the full path to the module.

`from my_application.service.module1 import method1`

The second is **relative**, where the dot means current directory:

`from .module1 import method1  # import from module1, which is located in the same directory`

or

`from . import module1`

### **Lesson Summary**

The module is just a program file without executed but callable code. The methods are not called inside modules. In Python, there are three ways to import the code from modules. When you are only importing the whole module, in some methods, try to avoid the symbol * in imports because it can violate the program namespace in the same cases.

### ****L1: Packages****

This lesson will discover packages in Python. You will learn what they are and when you have to use the __init__ file in packages.

The file __init__.py can be empty but can also restrict which objects will be available from the package through an __all__ statement.

`# file __init__.py
from module1 import method1
from module2 import method2, method3

__all__ = (“method1”, “method2”)`

As a result, method3 won’t be available for import from another code that uses this method.

### **Lesson Summary**

A package in Python is a directory that includes other subpackages and modules but also contains an __init__.py file. This file helps the Python interpreter understand that this directory is a package. The file __init__.py can be empty but can also restrict which objects will be available from the package through an __all__ statement.

****Pitfalls  - Tuzoqlar****

### ****L3: Import Pitfalls****

### **Import Process**

It is worth noting that Python runs all codes when it reaches the import statement. Let’s follow the example below:

*Click the arrows to see more information.*

`# a.py
print("Hello from a.py")
def foo():
    pass`

First, let’s create a.py, which prints text and defines function foo().

`# b.py
from a import foo`

Then, let’s try to import the foo() function in the b.py file.

**Result**

`Hello from a.py`

If you run b.py, you will see that Hello from a.py is printed on the screen.

Any imported variable can be changed in the module. So it is impossible to guarantee you have the latest function state until you run all the modules.

### **Variable PYTHONPATH**

Let’s see what happens while importing a module in Python. For example, you want to import abc module. When Python sees an import abc statement, it searches abc.py in the working directory. If it does not find it, Python will throw ModuleNotFoundError:

`ModuleNotFoundError: No module named ‘xyz’`

A list of folders is specified in the PYTHONPATH environment variable. Sometimes you might see .pyc files. These files are compiled bytecodes of Python scripts. When you want to run a script, Python first translates a source code to byte code. However, if it is converted already, this process is skipped. It will help to speed up the execution.

PYTHONPATH is an environment variable you can set to add additional directories where Python will look for modules and packages.

An installation-dependent list of directories configured at the time Python is installed.

The search path can be accessed through the Python variable sys.path, which is obtained from a module sys.

**Code**

`import sys
print(sys.path)`

**Result**

`['/home/file.py, '/usr/lib/python38.zip', '/usr/lib/python3.8', '/usr/lib/python3.8/lib-dynload',
'/usr/local/lib/python3.8/dist-packages', '/usr/lib/python3/dist-packages']`

This path may differ. The above example is used for the OS Linux.

### **Variable __name__**

As you saw earlier, Python runs all the code before importing it. If you have print statements and import the module, they will be printed, but this may not be the desired result. So, let’s learn how to prevent it.

The solution is a **magic variable** __name__. Python sets the __name__ variable to module name when importing a module. But, when executing this module, __name__ is equal to __main__. Using this fact, you can distinguish between them.

*Click on the arrows to navigate through the items below.*

`# first.py 
def foo(): 
    pass 
print("printing inside first.py")`

When you run Python first.py, you will see the print statement works fine.

`# second.py 
from first import foo 
foo()`

However, when you execute second.py, the same print statement will be executed. You need to use the __name__ magic variable to prevent this.

`# first.py 
def foo(): 
    pass 
if __name__ == "__main__": 
    print("printing inside first.py")`

Let’s modify this code to work as desired. When you run Python second.py, the print statement is not printing.

### **Importing Modules With the Same Functions**

There are some problems when you use from the module import * statement. The reason is you have to avoid implicitly loading all of the Python module’s locals into and over our current module’s namespace. This can produce unpredictable results.

Let’s suppose you have the following situation:

`# first.py 
def foo(): 
    print("inside first.py")`

`# second.py 
def foo(): 
    print("inside second.py")`

`# third.py 
from first import * 
from second import * 
foo()`

Sometimes, you might have two functions with the same name and you want to use them in third module. If you run third.py, you will always see theinside second.py statement. There is no way to access foo(), that is in first.py. Moreover, if you declare another foo() function inside third.py, you will overwrite other functions.

It is bad practice to use thefrom module import * style of importing. A better approach is to import the module if you have two functions with the same name and import, but only the functions and classes needed.

### **Cyclic Imports**

Suppose you have the following two files: a.py and b.py. Each file tries to import functions from one another.

`# a.py 
from b import func1 
def func2(): 
    pass`

`# b.py 
from a import func2 
def func1(): 
    pass`

If you run b.py, you will get the error ImportError: cannot import name 'func2' from partially initialized module 'a' (most likely due to a circular import).

What happens is that when Python sees a statement from a import func2, it tries to import func2 from a.py. However, in a.py, there is also a statement from b import func1, which creates a cyclic loop.

You can import the module and use the module .func notation to solve this problem.

Another possible solution is to put imports inside functions so that imports will occur whenever functions are called.

`# a.py 
def func2(): 
    from b import func1 
    pass`

`# b.py 
def func1(): 
    from a import func2 
    pass`

### **Execution of __init__ Files When Importing a Package**

The __init__.py file is used to mark directories where it is located as Python packages. Let’s suppose you have the following structure: If you want to import x.py, you can type import folder.x or from folder import x. However, if you remove __init__.py and try to import it, you will get an error.

![https://elearn.epam.com/assets/courseware/v1/415255a5d1241b3491b9df2aee3b584c/asset-v1:EPAM+PC+0122+type@asset+block/Module_4_Lesson_3_002_image.svg](https://elearn.epam.com/assets/courseware/v1/415255a5d1241b3491b9df2aee3b584c/asset-v1:EPAM+PC+0122+type@asset+block/Module_4_Lesson_3_002_image.svg)

One interesting thing about __init__.py is that all the code written in it will be executed during the import.

`# folder/__init__.py 
print("inside __init__.py")`

`# y.py 
from folder import x`

If you run y.py, you will see the printed message inside of __init__.py. It can be advantageous when you need to run some piece of code when something is imported. For example, one can put tests in __init__.py so that tests will be executed whenever functions or classes are imported.

### **Changing Names**

You already know that everything is an object in Python, and you use names to reach these objects. So, you can change these names:

`import datetime 
my_time_method = datetime.time 
print(my_time_method())  # 00:00:00`

### **Lesson Summary**

Remember, Python runs all the codes when it reaches the import statement. Any imported variable can be changed in the module. So it is impossible to guarantee you have the latest function state until you run all the modules.

PYTHONPATH is an environment variable you can set to add additional directories where Python will look for modules and packages. The search path can be accessed through the Python variable sys.path, obtained from a module sys.

Python sets the __name__ variable to a module name when importing a module. But, when executing this module, __name__ is equal to __main__. Using this fact, you can distinguish between them.

It is bad practice to use the from module import * style of importing. A better approach is to import the module if you have two functions with the same name, but only import the functions and classes needed.

Also, remember about cyclic imports. The occur when you have the two files, and each file tries to import functions from the other.

The __init__.py file is used to mark directories where it is located as Python packages.

Sort your imports for an easy read. isort is a Python package that sorts imports alphabetically and automatically separats them into sections and by type.

## M6: OOP in Python

- *polymorphism*
- *encapsulation*
- *inheritance*
- *abstraction*

### **Programming Paradigms**

To understand **object-oriented programming (OOP)**, you need to understand what programming paradigms are. The word **paradigm** can be defined as a specific set of concepts and techniques as a way to solve a problem.

**A programming paradigm** is a way to classify programming languages based on their features.

**Object-oriented programming (OOP)**
 is the programming paradigm that allows using object-oriented analysis and design (OOAD) to model software design around objects rather than logic or functions.

Objects are real-world entities that you can feel, manipulate and sense. For example, an object can represent a person with the following properties: age, name, gender, and behaviors like eating, sleeping, walking, etc.

### **OOP Principles**

OOP design is based on several concepts called **OOP principles**. These are Abstraction, Encapsulation, Polymorphism, and Inheritance. These are also called the **four pillars of object-oriented programming**.

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%206.png)

### **Abstraction**

Abstraction is one of the core concepts of OOP, which enables the user to implement even more complex logic on top of the provided abstraction without the need to understand or think about all the hidden background complexity.

**Abstraction** is a process of removing or generalizing physical, spatial, or temporal details or attributes in the study of objects or systems to focus attention on details of greater importance. Also, it is the creation of abstract concept objects by mirroring common features or attributes of various nonabstract objects or systems of study – the result of the process of abstraction.

[Wikipedia](https://en.wikipedia.org/wiki/Abstraction_(computer_science))

### **Encapsulation**

**Encapsulation** refers to the bundling of data with the methods that operate on that data or restricting the direct access to some of an object's components.

[Wikipedia](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming))

When a class is created, it means that encapsulation is automatically implemented. This is because class binds instance variables and methods into a single unit.

Note that there is another concept of **data/information hiding** that most people confuse with encapsulation.

### **Polymorphism**

**Polymorphism** is the provision of a single interface for entities of the different types or the use of a single symbol to represent the several different types.

[Wikipedia](https://en.wikipedia.org/wiki/Polymorphism_(computer_science))

Polymorphism is a Greek word that means "poly" - many and "morph" - form. There are two significant classes of polymorphism: parametric and ad-hoc polymorphism.

**Parametric Polymorphism**

**Parametric polymorphism** is a data type or function that can be written generically to handle values differently without depending on their type.

[Wikipedia](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)%22_/l_%22Parametric_polymorphism)

**Ad-hoc polymorphism** 

**Ad-hoc polymorphism** refers to functions that can be applied to arguments of various types. It behaves differently depending on the type of arguments they are applied to. There is no ad-hoc polymorphism in Python.

[Wikipedia](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)%22_/l_%22Ad_hoc_polymorphism)

### **Inheritance**

Inheritance is one of the most critical concepts in OOP, which simulates the real-world concept of inheritance.

In terms of programming, **inheritance** is the mechanism of basing an object or class upon another object or class, retaining a similar implementation.

[Wikipedia](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming))

You probably heard that someone looks like his/her father or mother. For example, they say that the child has mother/father hair color or has the same eye color as the father/mother. The class which inherits the properties is called **derived** or the **child class**. At the same time, the class from which it inherits is called the **base** or the **parent class**.

```python
class Base:
   def call(self):
     print("Base Class")

class Left(Base):
   def call(self):
     print("Left Class")

class Right(Base):
   def call(self):
     print("Right Class")

class Child(Left, Right):
pass

obj = Child()
obj.call() # => Left Class
```

There is not an ideal algorithm for choosing Right or Left. This question is called the **diamond problem**.

Quite interesting. How does Python know which class call() method to invoke? The answer is **method resolution order (MRO)**.

In Python, both built-in and user-defined classes are inherited from the object class. And all the objects are instances of the object class. So, if you try to access an attribute or call method, Python will search for it in the current class. If it's not found, it's searched in the parent classes. The parent classes are searched from left to right order, and each class is searched once. So looking at our example, if you want to access an attribute in the child class, the order will be the following:

## ****L2: Class-Related Decorators****

In Python, there are three decorators to change the behavior of class methods:

- @classmethod
- @staticmethod
- @abstractmethod

### **Class Methods**

Unlike instance methods, class methods are not bound to a specific object. Instead, they take the first argument cls, which points to the class, not the object instance. For this reason, they can't modify the state of the object instance. But they can modify the class state using cls that will apply to all class instances.

```python
class Person:
    origin_country = "USA"

    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

    def speak(self, words):
        print(f"{self.name} speaks: {words}")

    @classmethod
    def change_origin_country(cls, new_country):
        cls.origin_country = new_country
        print(cls.origin_country)
```

### **Static Methods**

Static methods don't take a self or cls parameter, although they can take any other arbitrary parameters. They can't modify either the object or class state. The advantage of static methods is that they don't require object instantiation before a call.

```python
class Person:
    origin_country = "USA"

    def __init__(self, name, age, gender):
        self.name = name
        self.age = age
        self.gender = gender

    @classmethod
    def change_origin_country(cls, new_country):
        cls.origin_country = new_country
        print(cls.origin_country)

    @staticmethod
    def is_adult(age):
        return age > 18
```

### **Abstract Base Classes (ABC)**

An abstract class, or abstract base class (ABC), is a class that cannot be instantiated because it is either labeled as abstract or it simply specifies abstract methods (["Class (computer programming)" (2022) Wikipedia](https://en.wikipedia.org/wiki/Class_(computer_programming)%22_/l_%22Abstract_and_concrete)). The previous lesson highlighted what a method is. So, an [abstract method](https://en.wikipedia.org/wiki/Method_(computer_programming)#Abstract_methods) means a method without implementation. There is the [Abstract Base Class (ABC)](https://docs.python.org/3/library/abc.html#abc.ABC) in Python for creating abstract classes.

**Abstract classes** are supposed to be inherited but avoid implementing methods, leaving only method signatures that subclasses must implement.

## ****L3: Exceptions****

Errors can be broadly classified into two classes:

- Syntax errors
- Logical Errors (exceptions)

**Syntax Errors**

A syntax error occurs when the interpreter translates the source code into byte code. It provides the error's actual description and traces it back and points to the actual line where the error is corrected.

`>>> print "demonstrate syntax errors"
  File "<stdin>", line 1
  print "demonstrate syntax errors"
       ^
SyntaxError: Missing parentheses in call to 'print'. Did you mean print ("demonstrate syntax
errors")?
>>>`

**Logical Errors (Exceptions)**

An exception object describes an exception and traces it back to where the problem occurred.

For example, if you are trying to read a file that does not exist, it disrupts the flow of the program and raises a FileNotFoundError.

`>>> open("file.txt",'rb')
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
FileNotFoundError: [Errno 2] No such file or directory: 'file.txt'
>>>`

### **Handling Exceptions**

Exception handling ensures the program doesn't break when the unhandled error occurs. In Python, exceptions can be handled using a try/except statement. Let's review the structure of this statement:

### **try**

The operation which can cause an exception is placed inside the try clause.

### **except**

The code that handles the exceptions is written in the except clause. You can choose what operations to perform once you have caught the exception.

### **else**

In the else statement, you can only instruct a program to execute a specific code block if there are no exceptions.

### **finally**

You can use finally to make sure files or resources are closed or released regardless of whether an exception occurs, even if you don't catch the exception.

### **Handling Specific Exceptions**

Built-in or custom exceptions are raised for specific errors and can be specified in multiple except clauses to distinguish the specific exception.

**Built-In or Custom Exceptions**

Follow good programming practice instead of handling every case in the same way. For example, you can specify which exceptions an except clause should catch.

`try:
    # do something
    pass

except ValueError:
    # handle ValueError exception
    pass

except (TypeError, ZeroDivisionError):
    # handle multiple exceptions
    # TypeError and ZeroDivisionError
    pass

except:
    # handle all other exceptions
    pass`

The **raise** statement forces a specified exception to occur. In addition, you can optionally pass arguments to the exception to clarify why that exception was raised.

`>>> try:
    a = int(input("Enter a positive integer: "))
    if a <= 0:
raise ValueError("That is not a positive number!")
    except ValueError as ve:
    print(ve)
    
Enter a positive integer: -2
That is not a positive number!`

**User-Defined Exceptions**

Python has various built-in exceptions that force your program to raise an error when something goes wrong.

However, sometimes you may need to create custom exceptions that serve your needs.

Users can define custom exceptions by creating a new class from the built-in Exception class. Most of the built-in exceptions are also derived from the Base Exception class.

You have created a user-defined exception called InputError, inheriting from the Exception class. Like other exceptions, this new exception class can be raised using the raise statement with an optional error message.

`# Create and raise Custom exception 'InputError'
class InputError(Exception):
    pass
    
raise InputError('Custom exception')
# Output:
# Traceback (most recent call last):
# File "<stdin>", line 4, in <module>
InputError: Custom exception`

Suppose you have Exception1 and Exception2. Exception2 is a subclass of Exception1. So let's try to catch Exception2 in the above situation.

You will always get the "Exception1 is caught" output when running this code snippet. It happens because Exception1, the superclass of the exception class Exception2, has already been caught. Order matters.

`class Exception1(Exception):
   pass

class Exception2(Exception1):
   pass

try:
   if isinstance(2, int):
       raise Exception2
except Exception1:
   print("Exception1 is caught")
except Exception2:
   print("Exception2 is caught")`

### **Lesson Summary**

All errors in Python can be broadly classified into two classes: syntax and logic. Syntax errors are caused when the programmer does not follow the proper structure/syntax of the language. Logical errors or exceptions are events raised when Python encounters the error while executing the code. They stop the execution and raise exception objects.

Exceptions can be handled using a try/except statement in Python. Exception handling ensures the program doesn't break when the unhandled error occurs. Built-in or custom exceptions are raised for specific errors and can be specified in multiple except clauses to distinguish the specific exception. The raise statement forces a specified exception to occur.

Users can define custom exceptions by creating a new class from the built-in Exception class. Most of the built-in exceptions are also derived from the Base Exception class.

## ****L4: Magic Methods****

### **Magic Methods**

In Python, there is a function called dir(), which lists all the attributes of the given object, and if you use the dir() function for your object or object class, you will discover attributes like __class__, __doc__, __str__, etc. These are called magic methods because they implicitly call when some action happens.

**Magic methods** in Python are the special methods that start and end with the double underscores. Magic methods are not meant to be invoked directly by you, but the invocation happens internally from the class after a certain action.

![Untitled](EPAM(Pyth0n)%20391d560cd7484f5691e9bcba22107113/Untitled%207.png)

### **Callable Objects**

As you know, everything in Python is an object, including functions. In general, any object can be callable, like functions are. You have to only define the __call__ magic method in this object. This means that you can write your own callable objects.

**__call__() magic method**

```python
class Callable:
def __call__(self, *args, **kwargs):
     print("__call__ method is called")
```

```python
>>> obj = Callable()
>>> obj()
__call__ method is called
```

Here, you create a simple Callable class with the **call**() magic method. Inside this method, you are printing a message.

When you instantiate an object and call that object, a message will be printed.

### **Iterator Pattern**

Iterable is an object with __iter__() magic method. It can be iterated over. An example of an iterable is a list or tuple. The iterator is the object which iterates over the sequence (or some non-sequence object like dict or file objects) in the correct order. It is returned by an __iter__() method of the iterable object. In addition, iterators have the __next__() method, which returns the next item of the object.

### **Finite Iterator**

Let's create an iterator object that will be printed a finite number of times and proceed with it step-by-step again.

### **Context Managers**

Different programming languages have the tools to work with files, databases, or network connections. Managing these resources is correctly quite tricky. You must release these resources after usage, not lock them from other programs or users. The improper usee of these resources can lead to memory leaks because modern operating systems limit resource use. Cases of exceeding these limits using files, databases, or network connections can be stopped by the operating system or any other resource management system.

```python
class ContextManager:
    def __init__(self):
        print('__init__ method called')

    def __enter__(self):
        print('__enter__ method called')
        return self

    def __exit__(self, exc_type,
                 exc_value, exc_traceback):
        print('__exit___ method called')

with ContextManager() as manager:
    print('inside with statement block')

class FileManager:
    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode
        self.file = None

    def __enter__(self):
        self.file = open(self.filename,
                         self.mode)
        return self.file

    def __exit__(self, exc_type,
                 exc_value, exc_traceback):
        self.file.close()

with FileManager('data.txt', 'w') as f:
    f.write("First Line\n")
    f.write("Second Line")
```

Connections are not the only way to use context managers. For example, you can use them for benchmarking, logging, and other cases.

### **Lesson Summary**

Magic methods in Python are **special methods that start and end with the double underscores**. Magic methods are not meant to be invoked directly by you, but the invocation happens internally from the class after a certain action.

## RSS
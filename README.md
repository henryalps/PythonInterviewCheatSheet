# Python Interview Cheat Sheet

This repository contains a comprehensive Cheat Sheet particularly useful for those preparing for a Python-related job interview. Our goal is to provide a handy reference guide and capitalize on your Python knowledge during interviews.

## Content

[中文](README-zh.md)

### Common Constants

Here are some built-in constants in Python as well as common constants in `sys`/`math` modules, along with their explanations and usage examples:

| Constant Name | Description | Usage Example |
| ----------- | ----------- | ----------- |
| `None` | Represents a null or no value | `a = None` |
| `True` | The True value of a Boolean data type | `is_ok = True` |
| `False` | The False value of a Boolean data type | `is_ok = False` |
| `math.pi` | The constant pi, usually used for calculations involving circles | `import math; print(math.pi)` |
| `math.e` | The base of the natural logarithm, called Euler's number | `import math; print(math.e)` |
| `math.tau` | Tau constant, equal to 2π. This is a constant in mathematics representing circles or periodic things | `import math; print(math.tau)` |
| `math.inf` | Positive infinity | `import math; print(math.inf)` |
| `math.nan` | "Not a Number" representation in floating point. Represents undefined or unrepresentable values | `import math; print(math.nan)` |
| `sys.maxsize` | The maximum "natural" integer in Python. **To use the minimum value, use -sys.maxsize-1** | `import sys; print(sys.maxsize);print(-sys.maxsize-1)` |
| `sys.int_info` | Information about Python integers | `import sys; print(sys.int_info)` |
| `sys.float_info` | Information about Python floating-point values | `import sys; print(sys.float_info)` |
| `sys.long_info` | Information about Python long integers | `import sys; print(sys.long_info)` |
| `sys.path` | The module lookup path in Python | `import sys; print(sys.path)` |
| `sys.version_info` | Version information of the Python interpreter | `import sys; print(sys.version_info)` |
| `sys.modules` | All modules imported in Python | `import sys; print(sys.modules)` |
| `sys.platform` | The name of the platform on which Python runs | `import sys; print(sys.platform)` |

### Common Operators

| Operator | Name | Description | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: |
| `**` | Exponentiation Operator | Returns the result of raising the left-hand operand to the power of the right-hand operand | `2 ** 3` | 8 |
| `~` | Bitwise NOT Operator | Inverts the bits of the number's binary representation | `~2` | -3 |
| `/` | Division Operator | Divides the left-hand operand by the right-hand operand and returns a floating-point number | `10 / 3` | 3.3333333333333335 |
| `//` | Floor Division Operator | Divides the left-hand operand by the right-hand operand and returns the largest integer less than or equal to the division | `10 // 3` | 3 |
| `%` | Modulus Operator | Returns the remainder of dividing the left-hand operand by the right-hand operand | `10 % 3` | 1 |
| `!=` | Not Equal Operator | Compares two operands for inequality. Returns `True` if they are not equal, and `False` otherwise | `2 != 3` | True |
| `is not` | Identity Operator | Compares the identity of two objects. Returns `True` if they are not the same object (i.e., do not occupy the same memory space) | `[] is not []` | True |

### Common Data Structures and Operations

#### Built-in Data Structures (no import required)

##### List

| Operation | Name | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `append()` | Add Element | Adds an element to the end of the list | None (the original list is modified) | `my_list = [1, 2, 3]; my_list.append(4); print(my_list)` | `[1, 2, 3, 4]` |
| `+` | List Concatenation | Connects two lists to form a new list | A new list | `my_list = [1, 2, 3]; my_new_list = my_list + [4, 5]; print(my_new_list)` | `[1, 2, 3, 4, 5]` |
| `extend()` | Extend List | Adds multiple values from another list to the end of the list | None (the original list is modified) | `my_list = [1, 2, 3]; my_list.extend([4, 5]); print(my_list)` | `[1, 2, 3, 4, 5]` |
| `remove()` | Remove Element | Removes a specified element from the list | None (the original list is modified) | `my_list = [1, 2, 3]; my_list.remove(2); print(my_list)` | `[1, 3]` |
| `pop()` | Pop Element | Removes and returns the element at a specified position in the list. If no index is specified, it removes the last element | The removed element | `my_list = [1, 2, 3]; popped_value = my_list.pop(1); print(my_list, popped_value)` | `[1, 3], 2` |
| `insert()` | Insert Element | Inserts an element at the specified position in the list | None (the original list is modified) | `my_list = [1, 2, 3]; my_list.insert(1, 'a'); print(my_list)` | `[1, 'a', 2, 3]` |
| `count()` | Count | Counts the occurrences of a particular element in the list | The number of occurrences of the element | `my_list = [1, 1, 2, 2, 2, 3, 3, 3, 3]; num_twos = my_list.count(2); print(num_twos)` | `3` |
| `sort()` | Sort | Sorts the elements of the list | None (the original list is modified) | `my_list = [3, 1, 4, 1, 5, 9, 2]; my_list.sort(); print(my_list)` | `[1, 1, 2, 3, 4, 5, 9]` |
| `reverse()` | Reverse | Reverses the order of the elements in the list | None (the original list is modified) | `my_list = [1, 2, 3, 4, 5]; my_list.reverse(); print(my_list)` | `[5, 4, 3, 2, 1]` |

Other than the `+` and `pop()` operators, all other list operations directly modify the list and do not return any value. `+` creates a new list, while `pop()` returns the removed element.

##### Tuple

Tuples in Python are immutable data structures, which means that once a tuple is created, its elements cannot be added, modified, or removed. However, the contents of mutable objects within a tuple, such as lists, can be changed. Here are various tuple operations:

| Operation | Name | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :--- | :---: | :---: |
| `t[1]` | Access Element | Returns the element at the index | Element in the tuple | `t = (1, 2, 3); print(t[1])` | `2` |
| `t[1:3]` | Slice Tuple | Returns a part of the tuple | A new tuple | `t = (1, 2, 3, 4, 5); print(t[1:3])` | `(2, 3)` |
| `t + t2` | Concatenate Tuples | Connects two tuples to create a new tuple | A new tuple | `t = (1, 2, 3); t2 = (4, 5, 6); print(t + t2)` | `(1, 2, 3, 4, 5, 6)` |
| `count()` | Count | Counts the occurrences of a particular element in the tuple | The number of occurrences of the element | `t = (1, 2, 2, 3, 3, 3); print(t.count(2))` | `2` |
| `index()` | Index | Returns the index of the first occurrence of a specific element | Index | `t = (1, 2, 3, 2, 3, 3); print(t.index(2))` | `1` |

Additional information about tuples:

- Since tuples are immutable, methods like `append()` or `extend()` that modify lists are not available.
- Tuples are ordered, so they support indexing and slicing operations.
- Because tuples are immutable, they can be used as keys in dictionaries, whereas lists cannot.

##### Set

| Operation | Name | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `add()` | Add Element | Adds an element to the set | None (the original set is modified) | `s = {1, 2, 3}; s.add(4); print(s)` | `{1, 2, 3, 4}` |
| `remove()` | Remove Element | Removes an element from the set. Raises a KeyError if the element is not found. | None (the original set is modified) | `s = {1, 2, 3}; s.remove(2); print(s)` | `{1, 3}` |
| `discard()` | Discard Element | Removes an element from the set. Does nothing if the element is not found. | None (the original set is modified) | `s = {1, 2, 3}; s.discard(2); print(s)` | `{1, 3}` |
| `pop()` | Pop Element | Removes and returns an element from the set. Raises a KeyError if the set is empty. | The removed element | `s = {1, 2, 3}; ele = s.pop(); print(s, ele)` | `{2, 3}, 1` (Result may vary as sets are unordered) |
| `clear()` | Clear Set | Removes all elements from the set | None (the original set is modified) | `s = {1, 2, 3}; s.clear(); print(s)` | `set()` |
| `union()` | Union | Returns a new set with all elements from both sets | A new set | `s1 = {1, 2, 3}; s2 = {3, 4, 5}; print(s1.union(s2))` | `{1, 2, 3, 4, 5}` |
| `intersection()` | Intersection | Returns a new set with elements common to both sets | A new set | `s1 = {1, 2, 3}; s2 = {2, 3, 4}; print(s1.intersection(s2))` | `{2, 3}` |
| `difference()` | Difference | Returns a new set with elements in the first set not in the second | A new set | `s1 = {1, 2, 3}; s2 = {2, 3, 4}; print(s1.difference(s2))` | `{1}` |
| `symmetric_difference()` | Symmetric Difference | Returns a new set with elements in either the first or second set but not in both | A new set | `s1 = {1, 2, 3}; s2 = {2, 3, 4}; print(s1.symmetric_difference(s2))` | `{1, 4}` |

##### Dictionary

| Operation | Name | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `d[key]` | Access Element | Retrieves the value associated with the key | Value corresponding to the key | `d = {'a': 1, 'b': 2}; print(d['a'])` | `1` |
| `d.get(key)` | Get Element | Retrieves the value associated with the key; returns `None` if the key does not exist | Value corresponding to the key or `None` | `d = {'a': 1, 'b': 2}; print(d.get('c'))` | `None` |
| `d[key] = value` | Modify/Add Element | Adds or modifies an element with the key | None (the original dictionary is modified) | `d = {'a': 1, 'b': 2}; d['c'] = 3; print(d)` | `{'a': 1, 'b': 2, 'c': 3}` |
| `del d[key]` | Delete Element | Removes an element with the key | None (the original dictionary is modified) | `d = {'a': 1, 'b': 2}; del d['a']; print(d)` | `{'b': 2}` |
| `d.keys()` | Get All Keys | Returns a view object with all the keys | View object | `d = {'a': 1, 'b': 2}; print(d.keys())` | `dict_keys(['a', 'b'])` |
| `d.values()` | Get All Values | Returns a view object with all the values | View object | `d = {'a': 1, 'b': 2}; print(d.values())` | `dict_values([1, 2])` |
| `d.items()` | Get All Key-Value Pairs | Returns a view object with all key-value pairs | View object | `d = {'a': 1, 'b': 2}; print(d.items())` | `dict_items([('a', 1), ('b', 2)])` |
| `d.pop(key)` | Remove Element | Removes and returns the value associated with the key. Raises a KeyError if the key does not exist. | Value corresponding to the key | `d = {'a': 1, 'b': 2}; print(d.pop('b'))` | `2` |
| `d.clear()` | Clear Dictionary | Removes all elements from the dictionary | None (the original dictionary is modified) | `d = {'a': 1, 'b': 2}; d.clear(); print(d)` | `{}` |

#### Non-Built-In Data Structures (import required)

##### Collections Module

The Python `collections` module provides various specialized container data types as alternatives to Python's general-purpose built-ins such as `list, set, dict`, etc. Here are operations for some of the common `collections` data structures:

###### namedtuple
> from collections import namedtuple

Create a subclass of tuples with named fields.

| Operation | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: |
| Named Tuple Creation | Creates a named tuple subclass with named fields | A named tuple | `Point = namedtuple('Point', ['x', 'y'])` | `Point(x=11, y=22)` |

###### deque
> from collections import deque

A thread-safe `deque` is used to create a double-ended queue.

| Operation | Description | Return Value | Example | Example Result |
| :--- | :--- | :--- | :--- | :--- |
| Creation | Creates a new `deque` object. Deque length can be fixed with `maxlen`. | `deque` object | `d = deque([1,2,3,4], maxlen=3)` | `deque([2, 3, 4], maxlen=3)` |
| Append | Adds an element to the right side. If `deque` is full, it discards an element from the left side. | None (deque is modified) | `d.append(5)` | `deque([3, 4, 5], maxlen=3)` |

Benefits of using `deque`:
- Efficient insertions and deletions: Deque allows constant time O(1) operations for insertion or deletion from its endpoints, unlike lists, which require O(n) for insertions or deletions at the beginning.
- Thread safety: Deques are designed to be thread-safe for appending and popping from the ends, which is not the case with lists.
- Length restriction: Setting `maxlen` lets you create deques with bounded lengths which automatically discard the oldest elements when full.

###### Counter
> from collections import Counter

Thread-safe `Counter` is a subclass of dictionary for counting hashable objects.

| Operation | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: |
| Counter Creation | Creates a `Counter` object based on an iterable or mapping | `Counter` object | `c = Counter('abcda')` | `Counter({'a': 2, 'b': 1, 'c': 1, 'd': 1})` |

##### OrderedDict
> from collections import OrderedDict

An `OrderedDict` is a dictionary subclass that remembers the order entries were added.

| Operation | Description | Return Value | Example | Example Result |
| :--- | :--- | :--- | :--- | :--- |
| Creation | Creates an ordered dictionary | `OrderedDict` object | `od = OrderedDict()` | `OrderedDict()` |

###### heapq
> import heapq

`heapq` module provides heap-based (binary trees): heap queue algorithm.

| Operation | Description | Return Value | Example | Example Result |
| :---: | :---: | :---: | :---: | :---: |
| `heappush()` | Adds an element to the heap while maintaining the heap property | None (heap is modified) | `heappush(heap, 3)` | `[2, 3]` |

##### Queue Module
> import queue

`Queue`, `PriorityQueue`, and `LifoQueue` are part of the `queue` module in Python.

| Operation | Description | Return Value | Example | Example Result |
| :--- | :--- | :--- | :--- | :--- |
| `Queue(maxsize)` | Creates a FIFO queue. `maxsize` determines the max number of items in the queue. | `Queue` object | `q = Queue()` | `Queue()` |

The `put()` and `get()` methods in `Queue`, `PriorityQueue`, and `LifoQueue` are blocking by default, which means if the queue is full (empty), the `put()` (`get()`) operation will wait until a spot is available (an item is available). If non-blocking behavior is desired, `block` can be set to `False`, but this will raise `Full` (`Empty`) exceptions when the queue is full (empty).

### Common Built-in Functions

Here's a table of common built-in functions in Python, their descriptions, return values, examples, and example outputs:

| Name | Description | Return Value | Example | Example Output |
| :--- | :--- | :--- | :--- | :--- |
| `map()` | Applies a function to every element in an iterable | An iterator containing the results after applying the function | `result = map(lambda x: x**2, [1,2,3,4]); print(list(result))` | `[1, 4, 9, 16]` |
| `zip()` | Creates an iterator that aggregates elements from each of the iterables | An iterator whose elements are tuples | `result = zip(['a', 'b'], [1, 2]); print(list(result))` | `[('a', 1), ('b', 2)]` |
| `any()` | Checks if any element of an iterable is True | Boolean | `result = any([False, 0, None, [], {}, '']); print(result)` | `False` |
| `enumerate()` | Pairs an index value with each element in an iterable | An iterator whose elements are tuples (index, element) | `result = enumerate(['a', 'b'], start=1); print(list(result))` | `[(1, 'a'), (2, 'b')]` |
| `filter()` | Filters elements in an iterable using a function | An iterator containing elements for which the function returns True | `result = filter(lambda x: x%2==0, [1,2,3,4]); print(list(result))` | `[2, 4]` |
| `ord()` | Returns the Unicode code point for a one-character string | Integer | `result = ord('a'); print(result)` | `97` |
| `chr()` | Returns the character that represents the specified Unicode | String | `result = chr(97); print(result)` | `a` |
| `sorted()` | Returns a new list sorted according to the specified comparison function | List | `result = sorted([3, 1, 4, 1, 5, 9], reverse=True); print(result)` | `[9, 5, 4, 3, 1, 1]` |
| `round()` | Rounds a number to a specified precision | Number | `result = round(10.6783, 2); print(result)` | `10.68` |
| `all()` | Returns True if all values in an iterable are True | Boolean | `result = all([True, 1, 's']); print(result)` | `True` |
| `reversed()` | Returns a reverse iterator | Iterator | `result = reversed([1, 2, 3, 4]); print(list(result))` | `[4, 3, 2, 1]` |

All the above functions are executed immediately upon invocation. In Python 3.x, `map()` and `filter()` return iterators, and results should be converted to a list or other form to view all the results. Although `map()`, `zip()`, and `filter()` return iterators, these functions are still executed immediately without lazy evaluation.

## Common Package Functions
| Package Name | Name | Description | Return Value | Example | Example Output |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `itertools` | `zip_longest()` | Creates an iterator that aggregates elements from each of the iterables. If one of the iterable objects ends early, it is filled in with None | An iterator, whose elements are tuples, which may contain None | `from itertools import zip_longest; result = zip_longest([1, 2, 3, 4], ['a', 'b']); print(list(result))` | `[(1, 'a'), (2, 'b'), (3, None), (4, None)]` |

## Contribution

Please feel free to open an issue or pull request if you think something can be improved or added.

I hope this information can give you a helpful insight, and the related references provide you the necessary directions to dive deeper into Python. 

## Reference
This Cheat Sheet is curated and condensed from various reliable Python references. Full credit to the original source materials.

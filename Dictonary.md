#  Python Dictionary  

##  1. What is a Dictionary ?

A **dictionary** in Python is a built-in data type used to store data in **key–value pairs**.

* Each **key** is unique.
* Each key maps to a **value**.
* Dictionaries are **mutable** (can be changed).
* Written using `{}` (curly braces).

###  Syntax

```python
dictionary_name = {
    key1: value1,
    key2: value2
}
```

###  Example

```python
student = {
    "name": "Sairam",
    "age": 21,
    "course": "Data Science"
}
```

 Here:

* `"name"`, `"age"`, `"course"` → keys
* `"Sairam"`, `21`, `"Data Science"` → values

---

##  2. Why Use Dictionaries?

* Fast data access using keys (O(1) time complexity)
* Used in:

  * JSON data
  * APIs
  * Database-like storage
  * Configuration settings
  * Counting frequency problems (very common in Data Science & ML)

---

##  3. Creating Dictionaries

###  Empty Dictionary

```python
d = {}
```

or

```python
d = dict()
```

---

###  Dictionary with Values

```python
employee = {
    "id": 101,
    "name": "Ravi",
    "salary": 50000
}
```

---

###  Using `dict()` Constructor

```python
person = dict(name="Anu", age=25, city="Hyderabad")
```

---

##  4. Accessing Values

###  Using Key

```python
student["name"]
```



* If key doesn’t exist → Error

---

###  Using `get()` Method (Safe Method)

```python
student.get("name")
student.get("marks", 0)
```

* Returns `None` if key not found
* Can give default value

---

##  5. Adding & Updating Values

###  Add New Key

```python
student["marks"] = 95
```

###  Update Existing Key

```python
student["age"] = 22
```

---

##  6. Deleting Items

###  Using `del`

```python
del student["age"]
```

###  Using `pop()`

```python
student.pop("marks")
```

###  Using `popitem()` (removes last inserted item)

```python
student.popitem()
```

###  Clear Entire Dictionary

```python
student.clear()
```

---

#  7. Popular Dictionary Operations

---

## 1. Length of Dictionary

```python
len(student)
```

Returns number of key-value pairs.

---



## 2. Loop Through Dictionary

###  Loop Through Keys

```python
for key in student:
    print(key)
```

###  Loop Through Values

```python
for value in student.values():
    print(value)
```

###  Loop Through Key-Value Pairs

```python
for key, value in student.items():
    print(key, value)
```

---

#  Important Dictionary Methods

---

##  1. `keys()`

Returns all keys.

```python
student.keys()
```

Output:

```
dict_keys(['name', 'age', 'course'])
```

---

##  2. `values()`

Returns all values.

```python
student.values()
```

---

##  3. `items()`

Returns key-value pairs as tuples.

```python
student.items()
```

Output:

```
dict_items([('name', 'Sairam'), ('age', 21)])
```

---

##  4. `update()`

Updates dictionary with another dictionary.

```python
student.update({"age": 23, "city": "Delhi"})
```

---

##  5. `setdefault()`

Returns value if key exists.
If not, inserts key with default value.

```python
student.setdefault("grade", "A")
```

---

##  6. `copy()`

Creates shallow copy.

```python
new_student = student.copy()
```

---



#   Nested Dictionary

Dictionary inside dictionary.

```python
students = {
    "student1": {
        "name": "Ravi",
        "marks": 90
    },
    "student2": {
        "name": "Anu",
        "marks": 85
    }
}
```

Accessing nested values:

```python
students["student1"]["name"]
```

---





#   Difference Between List and Dictionary

| Feature | List      | Dictionary            |
| ------- | --------- | --------------------- |
| Access  | By index  | By key                |
| Order   | Ordered   | Ordered (Python 3.7+) |
| Syntax  | []        | {}                    |
| Example | `[1,2,3]` | `{"a":1}`             |

---


#  Conclusion

A **dictionary** is one of the most powerful and commonly used data structures in Python.
It is mainly used when we need to store and retrieve data using meaningful keys instead of numeric indexes.

In Data Science, Machine Learning, Web Development, and APIs — dictionaries are everywhere.

---


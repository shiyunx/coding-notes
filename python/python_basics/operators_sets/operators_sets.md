## Operators and Sets

### Arithmetic operators

```python
result = value1 operator value2
```

| Operator | Meaning           | Formula  |
| -------- | ----------------- | -------- |
| `+`      | Addition          | `a + b`  |
| `-`      | Subtraction       | `a - b`  |
| `*`      | Multiplication    | `a * b`  |
| `/`      | Division          | `a / b`  |
| `//`     | Floor division    | `a // b` |
| `%`      | Modulus/remainder | `a % b`  |
| `**`     | Power             | `a ** b` |

### Assignment operators

```python
variable = value
```

### Logical operators

```python
condition1 and condition2
```

| Operator | Meaning                        |
| -------- | ------------------------------ |
| `and`    | Both conditions must be True   |
| `or`     | At least one condition is True |
| `not`    | Reverses True/False            |

### Membership operators

```python
value in collection
```

| Operator | Meaning               |
| -------- | --------------------- |
| `in`     | Exists inside         |
| `not in` | Does not exist inside |

### Identity operators

| Operator | Meaning           |
| -------- | ----------------- |
| `is`     | Same object       |
| `is not` | Different objects |

### Basic set

```python
set_name = {value1, value2, value3}
```

### Create a set

```python
# method 1: {}
fruits = {"apple", "banana", "orange"}

# method 2: set()
numbers = set([1, 2, 3, 4])
```

### Add to a set

```python
set_name.add(value)
```

### Remove from a set

```python
# remove
set_name.remove(value)
```

```python
# discard
set_name.discard(value)
```

### Set union

```python
# Combine everything from both sets.
# A.union(B)

A | B
```

### Set intersection

```python
# Find values that exist in both sets.
# A.intersection(B)

A & B
```

### Set Difference

```python
# Values in A that are NOT in B.

A - B
```

### Symmetric difference

```python
# Values that are in either set, but NOT in both.

A ^ B
```

### Set comparison

```python
# One set is contained inside another.
# A.issubset(B)
A <= B
```

### Superset

```python
# A.issuperset(B)

A >= B
```

### Set membership

```python
value in set_name
```

## Dictionaries

### Create a dictionary

```python
dictionary = {
    "key": value,
    "key": value
}
```

### Access dictionary

```python
dictionary[key]              # Access one value
dictionary.keys()            # Access all keys
dictionary.values()          # Access all values
dictionary.items()           # Access all key-value pairs
```

### Access a value

```python
dictionary["key"]
```

### Add a new key-value pair

```python
dictionary["new_key"] = value
```

### Change a value

```python
dictionary["existing_key"] = new_value
```

### Delete an item

```python
# del
del dictionary["key"]
```

```python
# pop
dictionary.pop("key")
```

### Check if a key exists

```python
if "key" in dictionary:
    print("Exists")
```

### Get a value

```python
 # Get the value for the key; returns None if key doesn't exist
dict.get(key)             
```

```python
# Get the value for the key; returns default_value if key doesn't exist
dict.get(key, default_value)       
```

### Loop through keys

```python
for key in dictionary:
    print(key)
```

### Loop through values

```python
for value in dictionary.values():
    print(value)
```

### Loop through key-value pairs

```python
for key, value in dictionary.items():
    print(key, value)
```

### Nested dictionary

```python
dictionary = {
    "key": {
        "key": value
    }
}
```

### Dictionary containing a list

```python
dictionary = {
    "key": [value1, value2, value3]
}
```

### List containing dictionaries

```python
list = [
    {"key": value},
    {"key": value}
]
```

### Loop through a list of dictionaries

```python
for item in list:
    print(item["key"])
```

### Update multiple values

```python
dictionary.update({
    "key1": value1,
    "key2": value2
})
```

### Copy a dictionary

```python
new_dictionary = dictionary.copy()
```

### Get all keys as a list

```python
list(dictionary.keys())
```

### Get all values as a list

```python
list(dictionary.values())
```

### Clear a dictionary

```python
dictionary.clear()
```

### Dictionary integer Keys

```python
dictionary = {
    integer_key: value,
    integer_key: value
}
```

### Dictionary mapping

```python
dictionary = {
    key: value,
    key: value,
    key: value
}
```

### Dictionary comprehension

```python
dictionary = {
    key_expression: value_expression
    for item in iterable
}
```

### Dictionary comprehension with condition

```python
dictionary = {
    key_expression: value_expression
    for item in iterable
    if condition
}
```

### Dictionaries

```python
# Dictionaries

# Create Dictionaries
dictionary1 = {
    "key": value,
    "key": value
}

dictionary2 = {
    "key": value,
    "key": value
}

# Access Values
print(dictionary1["key"])
print(dictionary2["key"])

# Check Data Types
print(type(dictionary1["key"]))
print(type(dictionary2["key"]))
```
## List

### Create a list

```python
list_name = [item1, item2, item3]
```

### Access an item

```python
list_name[index]
```

### Change an item

```python
list_name[index] = new_value
```

### `len()`

```python
len(list_name)
```

### `append()`: add to end

```python
list_name.append(value)
```

### `insert()`: add at position

```python
list_name.insert(index, value)
```

### `extend()`: add multiple items

```python
list_name.extend(other_list)
```

### `remove()`: remove by value

```python
list_name.remove(value)
```

### `pop()`: remove by index

```python
list_name.pop(index)
```

### `del`: delete by index

```python
del list_name[index]
```

### `clear()`: remove everything

```python
list_name.clear()
```

### Index

```python
list_name[-1]
```

- -1 = last item

### Slice

```python
list_name[start:end]
```

- start = included
- end = excluded

### Slice from start

```python
list_name[start:]
```

### Slice to end
```python
list_name[:end]
```

### Slice with step
```python
list_name[start:end:step]
```

### Check length/empty list

```python
if list_name:
```

### Check if item exists

```python
value in list_name
```

### Loop through a list

```python
for item in list_name:
    # code
```

### Loop with index

```python
for index, item in enumerate(list_name):
    # code
```

### Sort (ascending)

```python
numbers.sort()
```

### Sort (descending)

```python
numbers.sort(reverse=True)
```

### `sorted()`: create a new sorted list

```python
new_numbers = sorted(numbers)
```

### Reverse a list

```python
numbers.reverse()
```

### Reverse using slicing

```python
numbers[::-1]
```

### Count an item

```python
list_name.count(value)
```

### Find position

```python
list_name.index(value)
```

### Combine lists

```python
list3 = list1 + list2
```

### Copy a list

```python
new_list = list_name.copy()
```

```python
new_list = list_name[:]
```

### List comprehension

```python
new_list = [expression for item in old_list]
```

### List comprehension with condition

```python
new_list = [expression for item in list if condition]
```




## Loops

### For loop through items

```python
list = [item1, item2, item3]

for variable in list:
    print(variable)
```

### For loop through a string

```python
variable = "string"

for item in variable:
    print(item)
```

### For loop: range

```python
for variable in range(start, stop):
    print(variable)
```

```python
range(start, stop, step)
       ↓      ↓      ↓
     begin  exclude  change
```

```python
for variable in range(start, stop, step):
    print(variable)
```

```python
# countdown with range
for variable in range(start, stop, step):
    print(variable)
```

### For loop: list indexes

```python
for index in range(len(list)):
    print(index, list[index])
```

### For loop: list slice

```python
for variable in list[start:stop]:
    print(variable)
```

### For loop: tuple

```python
tuple_name = (item1, item2, item3)

for variable in tuple_name:
    print(variable)
```

### For loop: tuple slice

```python
for variable in tuple[start:stop]:
    print(variable)
```

### While loop

```python
variable = starting_value

while condition:
    do_something
    variable += change
```

### While loop: count backwards

```python
count = starting_value

while count >= ending_value:
    print(count)
    count -= 1
```

### While loop: even numbers

```python
number = first_even_number

while number <= limit:
    print(number)
    number += 2
```

### While loop: odd numbers

```python
number = first_odd_number

while number <= limit:
    print(number)
    number += 2
```

### While loop: sum

```python
number = starting_value
total = 0

while condition:
    total += number
    number += 1

print(total)
```

### While loop: loop through a list

```python
index = 0

while index < len(list):
    print(list[index])
    index += 1
```

### Break: stop the loop

```python
while condition:

    if stop_condition:
        break
```

### Continue: skip current iteration

```python
while condition:

    if skip_condition:
        continue

    do_something
```

### Infinite loop
```python
while True:
    do_something

    if exit_condition:
        break
```

### Nested loops

```python
while outer_condition:

    while inner_condition:
        do_something

    update_outer
```

### While loop and user input

```python
value = input("Enter something: ")

while condition:

    do_something

    value = input("Enter something: ")
```

### User input validation

```python
value = ""

while value != correct_value:
    value = input("Enter value: ")

print("Valid")
```
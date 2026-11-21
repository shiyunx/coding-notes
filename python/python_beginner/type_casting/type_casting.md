## Type Casting

- Convert a value from one data type to another.

### Basic type casting

```python
new_variable = target_type(value)
```

### String to integer

```python
int(string_value)
```

### String to float

```python
float(string_value)
```

### Integer to string

```python
str(integer_value)
```

### Integer to float

```python
float(integer_value)
```

### Float to integer

```python
int(float_value)
```

### Integer to boolean

```python
bool(integer_value)
```

### String to boolean

```python
bool(string_value)
```

### Multiple type conversions

```python
number = "10"

number = int(number)
number = float(number)
number = str(number)

print(number)
print(type(number))
```

### Type casting in calculations

```python
num1 = input("Enter first number: ")
num2 = input("Enter second number: ")

print(num1 + num2)
```

### Type casting with variables

```python
variable = type(value)
```

### Type casting with variables and input

```python
variable = type(input("message"))
```

### Type casting with f-strings

```python
variable = type(value)

print(f"text {variable}")
```

### Number calculation with f-string

```python
variable = type(input("message"))
result = calculation

print(f"text {result}")
```
## Functions

### Basic function

```python
def function_name():
    # processing

function_name()
```

### Function with no parameter

```python
# no return
def function_name():
    # processing

function_name()
```

```python
# with return
def function_name():
    # processing
    return output

result = function_name()
print(result)
```

### Function with one parameter

```python
# return
def function_name(input):
    # processing

function_name(argument)
```

```python
# with return
def function_name(input):
    # processing
    return output

result = function_name(argument)
print(result)
```

### Function with multiple parameters

```python
# return
def function_name(input1, input2):
    # processing
    return output

result = function_name(argument1, argument2)
print(result)
```

```python
# with return
def function_name(input1, input2):
    # processing
    return output

result = function_name(argument1, argument2)
print(result)
```

### Function with default parameter

```python
def function_name(input="default_value"):
    # processing
    return output

result = function_name()
print(result)
```

### Function with multiple parameters + default value

```python
def function_name(input1, input2="default_value"):
    # processing
    return output

result = function_name(argument1)
print(result)
```

### Function with multiple return values

```python
def function_name(input):
    # processing
    output1 = ...
    output2 = ...

    return output1, output2

result1, result2 = function_name(argument)

print(result1)
print(result2)
```

### Function with conditions

```python
def function_name(input):

    if condition:
        return output1
    else:
        return output2
```

### Function with a loop

```python
def function_name(input):

    for item in input:
        # processing

    return output
```

### Function calling another function

```python
def add(a, b):
    return a + b


def multiply(a, b):
    return a * b


total = add(10, 20)
answer = multiply(total, 2)

print(answer)
```

### Function with a list

```python
def function_name(list_name):

    for item in list_name:
        # processing

    return result
```

### Function with a dictionary

```python
def get_name(person):
    return person["name"]
```

### Main function

```python
def function_name(input):

    # processing

    return output


# Call function
result = function_name(input)

print(result)
```

### Function using keyword arguments

```python
def function_name(parameter1, parameter2):
    # processing


function_name(parameter1=value1, parameter2=value2)
```

### Function with local variable

```python
def function_name():
    local_variable = value

    # processing
```

### Function with lambda

```python
lambda parameter: expression
```

### Function with lambda map
```python
result = list(map(lambda parameter: expression, list_name))
```

### Function with lambda filter

```python
result = list(filter(lambda parameter: condition, list_name))
```

### Docstring

```python
def function_name(parameters):
    """Description of the function."""
    
    # processing
    
    return output
```

### Function with type hints

```python
def function_name(
    parameter: data_type
) -> return_type:

    # processing

    return output
```

### Nested function

```python
def outer_function():

    def inner_function():
        # processing

    inner_function()


outer_function()
```

### Function with if elif else

```python
# Define function
def function_name(parameter1, parameter2):

    # processing
    variable1 = ...

    # processing
    variable2 = ...

    # condition
    if condition:
        result = ...

    elif condition:
        result = ...

    else:
        result = ...

    # Return multiple values
    return output1, output2


# Get user input
input1 = input(...)

input2 = input(...)

# Call function
result1, result2 = function_name(input1, input2)

# Display results
print(result1)
print(result2)
```

|               | No Parameter                         | Has Parameter                             |
| ------------- | ------------------------------------ | ----------------------------------------- |
| **No Return** | `def function_name():`               | `def function_name(input):`               |
| **Return**    | `def function_name(): return output` | `def function_name(input): return output` |


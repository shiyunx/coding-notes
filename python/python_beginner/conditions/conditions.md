## Conditions
### if

- one condition

```python
if condition:
    code_to_run
```

### if else

- two outcomes

```python
if condition:
    code_if_true
else:
    code_if_false
```

### if elif else

- multiple outcomes

```python
if condition1:
    code_for_condition1
elif condition2:
    code_for_condition2
else:
    code_if_nothing_above_is_true
```

### nested if

- if inside if

```python
if condition1:
    if condition2:
        code_to_run
```

### nested if else

- if else inside another condition

```python
if condition1:
    if condition2:
        code
    else:
        code
else:
    code
```

### nested if elif else

- if elif else inside another condition

```python
if condition_1:
    
    if condition_2:
        action_2
    elif condition_3:
        action_3
    else:
        action_4

elif condition_4:
    
    if condition_5:
        action_5
    elif condition_6:
        action_6
    else:
        action_7

else:
    action_8
```

### Combine conditions: and

- both conditions must be True

```python
if condition_1 and condition_2:
    action
```

### Combine conditions: or

- at least one condition must be True

```python
if condition_1 or condition_2:
    action
```

### Combine conditions: not

- Reverses True/False

```python
if not condition:
    action
```

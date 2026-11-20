## Json

### Import Json

```python
import json
```

### Create python dictionary

```python
dictionary = {
    "key": value,
    "key": value
}
```

### Python dictionary to json string

```python
json_string = json.dumps(python_dictionary)
```

### Json string to python dictionary

```python
python_dictionary = json.loads(json_string)
```

### Python dictionary to json file

```python
with open("file.json", "w") as file:
    json.dump(data, file)
```

### Python dictionary to formatted json file

```python
json.dump(data, file, indent=4)
```

### Json file to python dictionary

```python
with open("file.json", "r") as file:
    data = json.load(file)
```

| Function  | Formula                 | Result               |
| --------- | ----------------------- | -------------------- |
| `dumps()` | `json.dumps(data)`      | Python → JSON string |
| `loads()` | `json.loads(text)`      | JSON string → Python |
| `dump()`  | `json.dump(data, file)` | Python → JSON file   |
| `load()`  | `json.load(file)`       | JSON file → Python   |

### Access json data

```python
dictionary["key"]
```

### Access nested json data

```python
dictionary["key"]["nested_key"]
```

### Json list/array

```python
dictionary["list_key"][index]
```

### Loop through json list

```python
for item in dictionary["list"]:
    do_something
```

### Access with get

```python
dictionary.get("key")
```

### Get with default value

```python
dictionary.get("key", "default value")
```

### Check if key exists

```python
if "key" in dictionary:
    # key exists
else:
    # key does not exist
```

### Handle missing key with try/except

```python
try:
    code that may cause error
except KeyError:
    handle error
```

### Delete a key

```python
dictionary.pop("key", None)
```

### Delete key and save json file

```python
del dictionary["key"]
```

### Handle invalid json

```python
try:
    json.loads()
except json.JSONDecodeError:
    handle invalid JSON
```

### Print json

```python
json.dumps(data, indent=4)
```
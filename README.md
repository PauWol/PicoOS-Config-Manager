# PicoOS Config Manager

A lightweight and flexible configuration manager for PicoOS, supporting a TOML-like structure with inline dictionaries, lists, and automatic type conversion.

## Features
- Reads and parses configuration files with class and subclass hierarchy.
- Supports inline dictionaries, lists, booleans, and numerical values.
- Provides getter and setter methods for easy access to configuration values.
- Automatically saves changes to the configuration file.
- Handles missing or malformed entries gracefully.

## Installation
```bash
# Clone the repository
git clone https://github.com/pauwol/PicoOS-Config-Manager.git
cd PicoOS-Config-Manager
```

## Usage
### Creating a Configuration Instance
```python
from config import Config

config = Config("test.toml")
```

### Retrieving Configuration Values
```python
# Get the entire configuration
data = config.get("*")

# Get a specific value
unit_test_value = config.get("unit.test.value")
```

### Setting Configuration Values
```python
config.set("unit.test.dict", {"a": 7, "b": 0})
```

### Example Configuration File (`test.toml`)
```toml
[unit]
test_value = 42
test_bool = true

[unit.test]
dict = { "a" = 1, "b" = 2 }
```

## Contributions
Feel free to fork, modify, and submit pull requests!

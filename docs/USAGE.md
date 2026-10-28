# Usage Guide & Examples

This guide demonstrates how to use the utility modules provided in this repository.

## 1. Timing Decorators

Measure execution time of functions easily:

```python
import time
from utils.timing import timeit

@timeit
def heavy_computation():
    time.sleep(1)
    return "done"

heavy_computation()
```

## 2. File Utilities

Safe file reading and structured JSON handling:

```python
from utils.file_ops import read_json, write_json

# Read JSON configuration
data = read_json("config.json")

# Write output JSON safely
write_json("output.json", {"status": "success", "count": 42})
```

## 3. String Helpers

String formatting and cleaning tools:

```python
from utils.string_ops import slugify, truncate

slug = slugify("Hello World! Python Utils")  # "hello-world-python-utils"
short_text = truncate("Long text string...", length=10)
```

## 4. Logger Setup

Standardized logging configuration:

```python
from utils.logger import get_logger

logger = get_logger("my_app")
logger.info("Application started successfully")
```

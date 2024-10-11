
---

## Curriculum

**Short Specializations**  

### 0x00. Python - Variable Annotations

### Concepts

- Advanced Python

### Resources

- [Python 3 typing documentation](https://docs.python.org/3/library/typing.html)
- [MyPy cheat sheet](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html)

### Learning Objectives

- Type annotations in Python 3
- Specifying function signatures and variable types
- Duck typing
- Validating code with mypy

### Requirements

- Editors: `vi`, `vim`, `emacs`
- Python version: 3.7 (Ubuntu 18.04 LTS)
- Code style: `pycodestyle` (version 2.5)
- All files executable, ending with a new line
- Documentation for modules, classes, and functions

### Tasks

1. **Basic annotations - add**
   - `0-add.py`
   ```python
   def add(a: float, b: float) -> float:
       return a + b
   ```

2. **Basic annotations - concat**
   - `1-concat.py`
   ```python
   def concat(str1: str, str2: str) -> str:
       return str1 + str2
   ```

3. **Basic annotations - floor**
   - `2-floor.py`
   ```python
   def floor(n: float) -> int:
       import math
       return math.floor(n)
   ```

4. **Basic annotations - to string**
   - `3-to_str.py`
   ```python
   def to_str(n: float) -> str:
       return str(n)
   ```

5. **Define variables**
   - `4-define_variables.py`
   ```python
   a: int = 1
   pi: float = 3.14
   i_understand_annotations: bool = True
   school: str = "Holberton"
   ```

6. **Complex types - list of floats**
   - `5-sum_list.py`
   ```python
   from typing import List

   def sum_list(input_list: List[float]) -> float:
       return sum(input_list)
   ```

7. **Complex types - mixed list**
   - `6-sum_mixed_list.py`
   ```python
   from typing import List, Union

   def sum_mixed_list(mxd_lst: List[Union[int, float]]) -> float:
       return sum(mxd_lst)
   ```

8. **Complex types - string and int/float to tuple**
   - `7-to_kv.py`
   ```python
   from typing import Union, Tuple

   def to_kv(k: str, v: Union[int, float]) -> Tuple[str, float]:
       return (k, float(v ** 2))
   ```

9. **Complex types - functions**
   - `8-make_multiplier.py`
   ```python
   from typing import Callable

   def make_multiplier(multiplier: float) -> Callable[[float], float]:
       def multiply(n: float) -> float:
           return n * multiplier
       return multiply
   ```

10. **Let's duck type an iterable object**
    - `9-element_length.py`
    ```python
    from typing import Iterable, Sequence, List, Tuple

    def element_length(lst: Iterable[Sequence]) -> List[Tuple[Sequence, int]]:
        return [(i, len(i)) for i in lst]
    ```

**Repo:**  
GitHub repository: `alx-backend-python`  
Directory: `0x00-python_variable_annotations`

---

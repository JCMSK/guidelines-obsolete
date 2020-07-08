# Coding Guidelines
The following guidelines are higly-recommended suggestions to make our code compatible withing the various pipelines

## General python guidelines

“Code is read much more often than it is written.” - Guido van Rossum (founder of Python)

Here is a summary of the guidelines used by the whole python community. Find the official guidelines [here](https://www.python.org/dev/peps/pep-0008/) 

*Simplicity* is the main principle when writing code.

### Naming Style
- Variables, functions, methods, packages, modules  
  `lower_case_with_underscores`
- Classes and Exceptions
  `CapWords`
- Constants
  `ALL_CAPS_WITH_UNDERSCORES`

### Indentation
- 4 spaces

### Empty Space
- Leave space between operators in case of assignment and arithmetic operations.
  ```var = 4
  result = var * 5```
- Leave space after a comma.
  `var1, var2 = get_values(num1, num2)`
Documentation
Follow PEP 257’s docstring guidelines learn how to document your python program.
Use one-line docstrings for obvious functions.
"""Return the pathname of ``foo``."""
2. Multiline docstrings should include
Summary line
Use case, if appropriate
Args
Return type and semantics, unless None is returned
Example
class Car:
    """A simple representation of a car.

    :param brand: A string, car's brand.
    :param model: A string, car's model.
    """
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model


## JCMSK guidelines 

### Images
**File formats**
**Orientation** 

### Point clouds
**File formats**

### Mesh
**File formats**

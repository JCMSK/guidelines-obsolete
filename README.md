# Coding Guidelines
The following guidelines are higly-recommended suggestions to make our code consistent across various pipelines

“Code is read much more often than it is written.” - Guido van Rossum (founder of Python)
*Simplicity* is the main principle when writing code.


## General python guidelines
Here is a summary of the guidelines used by the whole python community. Find the official guidelines [here](https://www.python.org/dev/peps/pep-0008/) 

**Naming Style**
- Variables, functions, methods, packages, modules:   
  `lower_case_with_underscores`
- Classes and exceptions:  
  `CapWords`
- Constants:  
  `ALL_CAPS_WITH_UNDERSCORES`

**Indentation**
- 4 spaces

**Empty Space**
- Leave space between operators in case of assignment and arithmetic operations:  
  ```
  var = 4
  result = var * 5
  ```
- Leave space after a comma:  
  `var1, var2 = get_values(num1, num2)`


## JCMSK guidelines 

**! The following guidelines are still work in progress and under discussion**

### Comments  
Commenting code is fundamental as it allow others to understand it (and ourselves at a later time as well!)

**General comments**
- General comments are introduced by `#` and are above the code they refer to:
  ```
  # assign variable
  a = 5
  ```
  
**Functions**
Each function is documented right below its definition:    
```
def my_function (input1, input2):
    """
    This functions does ... .
    Inputs:
    - input1: contains... (type: python list)
    - input2: contains... (type: SimpleITK image)
    Outputs:
    - output1: contains... (type: int)
    """
    
    function body
    
    return output1 
```
- The function documentation is in between three opening and three closing double quotes: `"""`
- Outline:  
  - Description of what the function does (First word starts with capital letter. Last sentence finishes with a dot)
  - Keyword `Inputs:` followed by a list of inputs. For each input, description of what it is, followed by the type `(type: type_of_input)`
  - Keyword `Outputs:` followed by a list of outputs. For each output, description of what it is, followed by the type `(type: type_of_output)`
- *Why is this important?*   
  These comments decleared using triple double quotes (`"""`) are called *docstrings*. And they are used:  
  - By users to know what the function does by typing `help (my_function)`. For example:  
    `help(my_function)`  
    returns:
    ```
    def my_function (input1, input2):
    This functions does ...
        Inputs:
        - input1: contains... (type: python list)
        - input2: contains... (type: SimpleITK image)
        Outputs:
        - output1: contains... (type: int)
    ```
   - To create whole code documentation using, for example, `pydoc`.  
    

### Images
**File formats**
**Orientation** 

### Point clouds
**File formats**

### Mesh
**File formats**

---
---
**!!! You are looking at an old document. The most updated version is on our [website](https://jcmsk.github.io/for_contributors.html) !!!**

---
---


# Coding Guidelines

**-- page under construction --**

The following guidelines are highly-recommended suggestions to make our code consistent across various pipelines

“Code is read much more often than it is written.” - Guido van Rossum (founder of Python)  
*Simplicity* is the main principle when writing code


[General python guidelines](#General-python-guidelines)  
&nbsp; [Naming style](#Naming-style)  
&nbsp; [Indentation](#Indentation)  
&nbsp; [Empty space](#Empty-space)  

[JCMSK guidelines](#JCMSK-guidelines)  
&nbsp; [Comments](#Comments)  
&nbsp; &nbsp; &nbsp; [General comments](#General-comments)  
&nbsp; &nbsp; &nbsp; [Functions](#Functions)  
&nbsp; &nbsp; &nbsp; [Classes](#Classes)  
&nbsp; &nbsp; &nbsp; [Modules](#Modules)  
&nbsp; &nbsp; &nbsp; [Packages](#Packages)  
&nbsp; [Data types](#data-types)  
&nbsp; &nbsp; &nbsp; [Image](#Image)  
&nbsp; &nbsp; &nbsp; [Mesh](#Mesh)  
&nbsp; &nbsp; &nbsp; [Points](#Point)   
   


## General python guidelines
Here is a summary of the guidelines used by the whole python community. Find the official guidelines [here](https://www.python.org/dev/peps/pep-0008/) 

**Naming Style**
- Variables, functions, methods, modules, packages:   
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

--- 

## JCMSK guidelines 

**>>> ! The following guidelines are still work in progress and under discussion <<<**

### Comments  
Commenting code is fundamental as it allow others to understand it (and ourselves at a later time as well!)

#### General comments
- General comments are introduced by `#` and are above the code they refer to:
  ```
  # assign variable
  a = 5
  ```
  
#### Functions  
We follow the numpy style guide (see [here](https://numpydoc.readthedocs.io/en/latest/format.html)
Each function is documented right below its definition:    
```
def my_function (input1, input2):
    
    """This functions does ... .
    
    Parameters
    ----------
    x : type
        Description of parameter `x`.
    y
        Description of parameter `y` (with type not specified).
    
    Returns
    -------
    int
        Description of anonymous integer return value.
    """
    
    function body
    
    return output1 
```
- The function documentation is in between three opening and three closing double quotes: `"""`
- Outline:  
  - Description of what the function does
  - Keyword `Parameters:` followed by a list of parameters. For each parameter, type on the same line, and indented description on the following line
  - Keyword `Returns:` followed by a list of returned variables. For each variable, type on the same line, and indented description on the following line
- *Why is this important?*   
  These comments decleared in between triple double quotes (`"""`) are called *docstrings*. And they are used:  
  - By users to know what the function does by typing `help (my_function)`  
  - To create whole code documentation using, for example, `pydoc` or `Sphinx`, where you get a list of all the functions in a package, and their documentation
    
#### Classes
Coming soon!

#### Modules
Coming soon!  

#### Packages 
Coming soon!


### Data types  
In our pipelines, we mainly use: 3D image volumes, meshes, and point clouds.  
Here are our conventions:

| data type | data representation      | file format  |
| :---------| :----------------------- | :----------- |
| Image     | SimpleITK / VTK?         | .mha? /.vtk? |
| Mesh      | VTK?                     | .vtk?        | 
| Points    | VTKPoints / Numpy array? | .vtk? / .txt?|


#### Image   
##### Data representation 
##### File format    

#### Mesh  
##### Data representation 
##### File format    

#### Point  
##### Data representation
##### File format   







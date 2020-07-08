# Coding Guidelines
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
&nbsp; &nbsp; &nbsp; [Point](#Point)   
&nbsp; &nbsp; &nbsp; [Mesh](#Mesh)   


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
   - To create whole code documentation using, for example, `pydoc` or `Sphinx`, where you get a list of all the functions in a package, and their documentation
    
#### Classes
Coming soon!

#### Modules
Coming soon!  

#### Packages 
Coming soon!


### Data types  
In our pipelines, we mainly use: 3D image volumes, point clouds, and meshes. Here is a summary of their characteristics:

| data type | data representation | orientation                | file format |
| :---------| :------------------ | :------------------------- | :-----------|
| Image     | SimpleITK image     | RAI?                       | .mha?       |
| Point     | Numpy array         | point coordinates x points | .txt        |
| Mesh      | ?                   | ?                          | ?           | 


#### Image   

##### Data representation 
SimpleITK image?

##### Orientation
We have to choose one radiological orientation (e.g. RAI) so that we have for example:  
x -> axial  
y -> sagittal  
z -> frontal  
(Add here a figure)  

##### File format    
We save images in xxx.  
If our images are in another file format, we can convert them to xxx using these functions (link to `pyMSK`'s `image_file_conversions.py`)


#### Point  
##### Data representation and orientation
Points are represented in numpy arrays, where:  
- Each row corresponds to a point
- The first column is the x-coordinate  
- The second column is the y-coordinate  
- The third column is the z-coordinate 

*Example*: We have four points. Point 1 has coordinates x = 1, y = 1, z = 1, point 2 has coordinates x = 2, y = 2, z = 2, etc.   
We create a numpy array with 4 rows (= number of points) and 3 columns (= number of coordinates):        
`points = np.array ([ (1, 1, 1), (2, 2, 2), (3, 3, 3), (4, 4, 4) ])`.  
When we print it out (`print (points)`), it looks like this: 
```
[[1 1 1]
 [2 2 2]
 [3 3 3]
 [4 4 4]]
 ```
 
##### File format   
We save the points in `.txt` files.
Similarly to the numpy representation, in the file: 
- Each row corresponds to one point 
- For each point, we write `x y z` coordinates, separated by one space

*Example*: The array declared above would be saved in a .txt file that looks like this:
```
1 1 1
2 2 2
3 3 3
4 4 4
```

#### Mesh  
##### Data representation 
##### Orientation
##### File format    
Our preferred mesh format is xxx (STL?)




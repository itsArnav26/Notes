## Table of Contents

- [NumPy](#what-is-numpy)
- [UseCase](#why-use-numpy)
- [Diffrence Between List and NumPy](#list-vs-numpy)
- [First Array](#created-out-first-array)
- [ndim,shape,size,dtype](#array-attributes)
- [zeros,ones,linspace,arange](#create-basic-array)

## What is NumPy

- NumPy (Numerical Python) is an open source Python library that’s widely used in science and engineering.
- he NumPy library contains multidimensional array data structures, such as the `homogeneous`(same data type), N-dimensional ndarray, and a large library of functions that operate efficiently on these data structures.

## Why use NumPy

- NumPy shines when there are large quantities of “homogeneous” (same-type) data to be processed on the CPU.
- improve speed, reduce memory consumption, and offer a high-level syntax for performing a variety of common processing tasks.(for `homogeneos` data)

## LIST VS NUMPY

<table border="1" cellpadding="8" cellspacing="0">
    <tr>
        <th>Feature</th>
        <th>Python List</th>
        <th>NumPy Array</th>
    </tr>
    <tr>
        <td>Library</td>
        <td>Built-in Python</td>
        <td>Requires NumPy library</td>
    </tr>
    <tr>
        <td>Data Type</td>
        <td>Can store different data types</td>
        <td>Stores same data type (homogeneous)</td>
    </tr>
    <tr>
        <td>Performance</td>
        <td>Slower for numerical operations</td>
        <td>Faster due to vectorization</td>
    </tr>
    <tr>
        <td>Memory Usage</td>
        <td>More memory consumption</td>
        <td>Less memory consumption</td>
    </tr>
    <tr>
        <td>Mathematical Operations</td>
        <td>Needs loops for element-wise operations</td>
        <td>Supports direct element-wise operations</td>
    </tr>
    <tr>
        <td>Multi-dimensional Support</td>
        <td>Possible but less efficient</td>
        <td>Efficient multi-dimensional arrays</td>
    </tr>
    <tr>
        <td>Built-in Functions</td>
        <td>Limited numerical functions</td>
        <td>Many built-in mathematical/statistical functions</td>
    </tr>
    <tr>
        <td>Use Case</td>
        <td>General-purpose programming</td>
        <td>Scientific computing & data analysis</td>
    </tr>
</table>

### Created out first array

```py
import numpy as np
a = np.array([1,2,3,4],[5,6,7,8])
```

## Array Attributes

- **ndim**
  - The `number of dimensions` of an array is contained in the ndim attribute,whether is 2D,1D or 3D
  - Output: 2
- **shape**
  - The `shape of an array is a tuple` of non-negative integers that specify the number of elements along each dimension.
  - Output : (2,4)
- **size**
  - The fixed, total number of elements in array is contained in the size attribute.basically `count` the total elements
  - Output: 8

- **dtype**
  - The data type is recorded in the dtype attribute.
  - Since array is `homogeneous`,so we can find out the data type of the elements
  - Output : dtype('int64')

## Create Basic Array

- **np.zeros**
  - create an array filled with 0’s
  - EX: np.zeros(2) -> create an array filled with 0’s
  - array([0., 0.]) (`in float- bydefault`)
- **np.ones**
  - create an array filled with 1’s
  - EX: np.zeros(2) -> create an array filled with 1’s
  - array([1., 1.])
- **np.linspace**
  - create an array with values that are spaced linearly in a specified interval
  - EX: np.linspace(0,10,5)
  - array([ 0. , 2.5, 5. , 7.5, 10. ])
- **np.arange**
  - create an array with a range of elements
  - Ex:np.arange(0,4)
  - array([0,1,2,3]) (`4 is excluded`)
  - also can specify the `first number, last number, and the step size`.
  - Ex: np.arange(0,10,2)
  - array([0,2,4,6,8])
  ### Specifying your data type
  - can explicitly `specify` which `data type` you want using the `dtype` keyword.
  - Ex: a = np.ones(3,`dtype = np.int64`)
  - [1,1,1]

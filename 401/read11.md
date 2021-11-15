# JupyterLab 
JupyterLab is a next-generation web-based user interface for Project Jupyter.JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner (show the output immediatily)(tutotrial porpuses)
### JupyterLab provides a high level of integration between notebooks, documents, and activities:
* Drag-and-drop to reorder notebook cells and copy them between notebooks.
* Run code blocks interactively from text files (.py, .R, .md, .tex, etc.).
* Link a code console to a notebook kernel to explore code interactively without cluttering up the notebook with temporary scratch work.
* Edit popular file formats with live preview, such as Markdown, JSON, CSV, Vega, VegaLite, and more.

### difference between JupyterLab شىي Jupyter Notebook  ?


* JupyterLab is the next-generation user interface including notebooks. It has a modular structure, where you can open several notebooks or files (e.g. HTML, Text, Markdowns etc) as tabs in the same window. It offers more of an IDE-like experience.

* Jupyter Notebook is a web-based interactive computational environment for creating Jupyter notebook documents. It supports several languages like Python (IPython), Julia, R etc. and is largely used for data analysis, data visualization and further interactive, exploratory computing.


# NumPy

NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.


NumPy’s main object is the homogeneous multidimensional array. It is a table of elements (usually numbers), all of the same type, indexed by a tuple of non-negative integers. In NumPy dimensions are called axes.

For example, the coordinates of a point in 3D space [1, 2, 1] has one axis. That axis has 3 elements in it, so we say it has a length of 3. In the example pictured below, the array has 2 axes. The first axis has a length of 2, the second axis has a length of 3.
```
[[1., 0., 0.],
 [0., 1., 2.]]
 ```

 NumPy’s array class is called ndarray. It is also known by the alias array. Note that numpy.array is not the same as the Standard Python Library class array.array, which only handles one-dimensional arrays and offers less functionality. The more important attributes of an ndarray object are:

* ndarray.ndim
the number of axes (dimensions) of the array.

* ndarray.shape
the dimensions of the array. This is a tuple of integers indicating the size of the array in each dimension. For a matrix with n rows and m columns, shape will be (n,m). The length of the shape tuple is therefore the number of axes, ndim.

* ndarray.size
the total number of elements of the array. This is equal to the product of the elements of shape.

* ndarray.dtype
an object describing the type of the elements in the array. One can create or specify dtype’s using standard Python types. Additionally NumPy provides types of its own. numpy.int32, numpy.int16, and numpy.float64 are some examples.

* ndarray.itemsize
the size in bytes of each element of the array. For example, an array of elements of type float64 has itemsize 8 (=64/8), while one of type complex32 has itemsize 4 (=32/8). It is equivalent to ndarray.dtype.itemsize.

* ndarray.data
the buffer containing the actual elements of the array. Normally, we won’t need to use this attribute because we will access the elements in an array using indexing facilities.

An example
```
import numpy as np
a = np.arange(15).reshape(3, 5)
a
array([[ 0,  1,  2,  3,  4],
       [ 5,  6,  7,  8,  9],
       [10, 11, 12, 13, 14]])
a.shape
(3, 5)
a.ndim
2
a.dtype.name
'int64'
a.itemsize
8
a.size
15
type(a)
<class 'numpy.ndarray'>
b = np.array([6, 7, 8])
b
array([6, 7, 8])
type(b)
<class 'numpy.ndarray'>
```
### Array Creation
```
>>> import numpy as np
>>> a = np.array([2, 3, 4])
>>> a
array([2, 3, 4])
>>> a.dtype
dtype('int64')
>>> b = np.array([1.2, 3.5, 5.1])
>>> b.dtype
dtype('float64')
```

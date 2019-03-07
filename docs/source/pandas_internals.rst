Internals of Pandas
===================

Data structures in pandas
-------------------------

There are three main data structures in pandas:

* Series
* DataFrame
* Panel

Series
''''''

Series is one-dimensional array-like object containing a sequence of values 
(of similar types to NumPy types) and an associated array of data labels, 
called its *index*. The Series extends the functionality of the NumPy ndarray 
by adding an associated set of labels that are used to index the elements of the 
array. A Series can hold zero or more instances of any single data type.

A Series data structure can be created using the data as below:

* An ndarray (`numpy.ndarray`_)
* A python iterable or dictionary
* A scalar value

.. code-block:: python

   In [11]: import pandas as pd
   In [12]: obj = pd.Series(['a', 'b', 'c'])
   In [13]: obj
   Out[13]:
   0    a
   1    b
   2    c
   dtype: object

You can think about a Series is as a fixed-length, ordered dict, as it is a 
mapping of index values to data values. Here is an example that creates a 
Series from a dictionary.

.. code-block:: python

   In [1]: import pandas as pd
   In [3]: sd = {'beijing': 9000, 'shanghai': 8500, 'chengdu': 8400, 'hangzhou': 8000}
   In [4]: pd_obj = pd.Series(sd)
   In [5]: pd_obj
   Out[5]:
   beijing     9000
   shanghai    8500
   chengdu     8400
   hangzhou    8000
   dtype: int64
   In [6]: cites = ['beijing', 'chengdu', 'hangzhou', 'nanjing', 'shanghai']
   In [7]: pd_obj1 = pd.Series(pd_obj, cites)
   In [8]: pd_obj1
   Out[8]:
   beijing     9000.0
   chengdu     8400.0
   hangzhou    8000.0
   nanjing        NaN
   shanghai    8500.0
   dtype: float64

.. _`numpy.ndarray`: https://docs.scipy.org/doc/numpy/reference/arrays.ndarray.html
.. _`NumFOCUS`: https://numfocus.org
.. _`Cython`: https://cython.org

Pandas
======

.. image:: http://pandas.pydata.org/_static/pandas_logo.png
   :align: center

Pandas is a data wrangling platform for Python widely adopted in the 
scientific computing community. Pandas provides easy-to-use data 
ingestion, transformation, and export functions. Pandas project is 
`NumFOCUS`_ sponsored project since 2015.


Overview
--------

Basic Information
'''''''''''''''''

+----------------------------------------+
| |pandas_logo|                          |
+====================+===================+
| Original author(s) | Wes McKinney      |
+--------------------+-------------------+
| Developer(s)       | Community         |
+--------------------+-------------------+
| Write in           | Python, Cython, C |
+--------------------+-------------------+
| Initial release    | 11 January 2008   |
+--------------------+-------------------+
| Stable release     | 0.24.1            |
+--------------------+-------------------+

.. |pandas_logo| image:: /_static/pandas/pandas_logo.png

History
'''''''

Wes McKinney developed pandas in 2008 at AQR Capital Management with the need for a 
high performance, flexible tool to perform quantitative analysis on financial data.
Before leaving AQR he was able to convince management to allow him to open source 
the library. Another AQR employee, Chang She, joined the effort in 2012 as the second 
major contributor to the library.  In 2015, pandas signed on as a fiscally sponsored 
project of `NumFOCUS`_.

Technical details
'''''''''''''''''

Pandas is an open source library providing high-performance, easy-to-use data 
structures and data analysis tools for the Python programming language. Pandas’ 
data analysis and modeling features enable users to carry out their entire data 
analysis workflow in Python without having to switch to a more domain-specific 
language like R. The library is highly optimized for performance, with critical 
code paths written in `Cython`_ or C.

Applications
''''''''''''

As a foundational data wrangling tool, Pandas is used in virtually every large 
company in tech and finance and at every major university.

Features
''''''''

* DataFrame object for data manipulation with integrated indexing.
* Tools for reading and writing data between in-memory data structures and different file formats.
* Data alignment and integrated handling of missing data.
* Reshaping and pivoting of data sets.
* Label-based slicing, fancy indexing, and subsetting of large data sets.
* Data structure column insertion and deletion.
* Group by engine allowing split-apply-combine operations on data sets.
* Data set merging and joining.
* Hierarchical axis indexing to work with high-dimensional data in a lower-dimensional data structure.
* Time series-functionality: Date range generation and frequency conversion, moving window statistics, moving window linear regressions, date shifting and lagging.
* Provides data filtration.

Internals of Pandas
-------------------

Data structures in pandas
'''''''''''''''''''''''''

There are three main data structures in pandas:

* Series
* DataFrame
* Panel

Series
~~~~~~

Series is one-dimensional array-like object containing a sequence of values 
(of similar types to NumPy types) and an associated array of data labels, 
called its *index*. The Series extends the functionality of the NumPy ndarray 
by adding an associated set of labels that are used to index the elements of the 
array. A Series can hold zero or more instances of any single data type.


.. _`NumFOCUS`: https://numfocus.org
.. _`Cython`: https://cython.org

History of SciPy
================

This page sketches the history of SciPy and should clarify 
the differences/relations between ``SciPy``, ``Numeric``, ``numarray``, 
``NumPy`` and other related packages/projects.

The birth of Numeric
--------------------

In the beginning there was ``Numeric``. It was originally written in 1995 largely 
by Jim Hugunin with the help of many people including Jim Fulton, David Ascher, 
Paul DuBois, and Konrad Hinsen. Unfortunately, ``Numeric`` acquired several nicknames: 
``Numerical Python``, ``Numerical``, ``NumPy``. For example, the SourceForge project name for 
it is ``numpy``, the old CVS module is ``Numerical``, Konrad Hinsen named his package 
ScientificPython in reference to Numerical Python.

Quoting Paul DuBois on the history behind the various names of the project:

    Here's the true story about why the various names for the original: numpy, Numeric, Numerical.
    At the time Source Forge was pretty young, and I decided to put the project there. We all said 
    'numpy' informally not Numerical Python but the module name was Numeric. I created the project 
    as numpy. I have no memory of why I didn't call it Numeric, but if it wasn't a conflict, probably 
    I was focused on making it clear it was for Python and/or easy to type. (the FTP's etc. all had to 
    go through a long directory path that involved the name). The documentation for the CVS stuff was 
    confusing, and I made a mistake with my first submit of 'Numeric' (I think it was ending up with 
    everything in Numeric/Numeric) and then discovered I could not delete it; you had to ask the Source 
    Forge staff. Impatient, I did a second submit as Numerical. In short, all my fault, but then again, 
    SF was so security-minded that it was hard to do anything. That's why I soon gave up on their website 
    and hosted it at my own site for so long. 

The birth of SciPy
------------------

Several people used Numeric as a base for their scientific code and developed 
their own modules. Around 2001, Travis Oliphant, Eric Jones and Pearu Peterson 
merged their modules in one scientific super package: SciPy was born.

The birth of numarray
---------------------

Development on Numeric slowed down and people wanted to extend it in ways that 
the then-current codebase did not really allow. Furthermore, there was a desire 
to get Numeric or something like it into the standard library, but Guido van 
Rossum (the father of Python) was quite clear that the code was not maintainable 
in its state then.

As a result, numarray was created by Perry Greenﬁeld, Todd Miller and Rick White 
at the Space Science Telescope Institute as a replacement for Numeric. The new 
numarray pushed some of the code up into the Python level, which gave numarray 
a lot of flexibility and allowed it to experiment with a number of alternatives 
that have proven their usefulness. It also was quite fast for very large arrays 
because the people working on it were at the Space Telescope Science Institute 
and were intending to use it for astronomical image processing.

The split: Numeric vs. numarray
-------------------------------

Unfortunately, as fast as it was for large arrays, numarray was too slow for 
small arrays. Furthermore, the C API of numarray for creating ufuncs was not 
as convenient as that of Numeric. This made it difficult to convert the SciPy 
codebase to use numarray instead of Numeric. This split fractured the community 
quite a bit: some people wrote code only for numarray, seeing it as the next 
Numeric, while other people wrote code for Numeric, because they needed SciPy.

The reunion, aka the birth of NumPy
-----------------------------------

In early 2005, Travis Oliphant wanted to reunify the community around a single 
array package. He refactored the code of Numeric to make it more maintainable 
and flexible enough to implement the novel features of numarray. He named this 
new multi dimensional array project SciPy core and intended to use this in the 
bigger scientific package SciPy.

The problem with this approach was that people were mistakenly thinking that 
Numeric had been subsumed into SciPy and that they would have to install SciPy 
as a whole just to get an array object. There was a long discussion about a 
better name for this new multidimensional array package. The winning name was 
numerix, but this name turned out to be trademarked by a company that does DSP. 
In order to avoid trademark infringement, another name was picked: 'NumPy'.

Inclusion of a Numpy in Python's standard library
-------------------------------------------------

In the opinion of many involved in the Numpy development, an N-dimensional array 
interface should be part of the Python standard libraries. Hence, a PEP was 
started to describe what exactly is meant by an array interface, and a webpage 
was set up with useful information. At the SciPy conference in 2006, Guido and 
Travis discussed which parts of NumPy should go into Python. They decided that 
the best course to pursue is to write a series of PEPs to get

1. the data-type object into Python
2. extend the buffer interface with the array interface.

Anyone interested in helping with these PEPs should contact Travis Oliphant. 


**Reference**: `History of SciPy`_


.. _`History of SciPy`: https://scipy.github.io/old-wiki/pages/History_of_SciPy.html

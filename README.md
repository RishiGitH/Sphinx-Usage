# Sphinx-Usage
A documentation on how to use sphinx

## View Doc
To just view the doc 
1) Download Build folder
2) Open html/result.html

## Build Sphinx
Download pckg1 folder and keep it  inside the sphinx folder
Installing Sphinx 

1)Create a virtual env
```
mdir sphinx
virtualenv sphinx
source <name of virtualenv>/bin/activate
cd sphinx
```
2)Install dependecies
```
pip install Sphinx
pip install sphinx_rtd_theme
```

3)Setup Sphinx
```
sphinx-quickstart
```
set autodoc to true,
automatically insert doc strings to true,
set todo to true,
makefile to true,
view code to true,

4)Add these lines to conf.py
```
import sys
import os 
sys.path.insert(0, os.path.join(os.path.abspath('..'),'pckg1'))
html_theme = "sphinx_rtd_theme"
```
5)Add result to index.rst
```
Welcome to Rishi's documentation!
=============================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   result
```
6)run the apido command to create .rst files
```
 sphinx-apidoc pckg1 -o source
```
7)Build your documentation by changing directory to the directory that contains the Makefile and then running 
```
make html
```
8)You can view the documentation by navigating into the _build/html directory


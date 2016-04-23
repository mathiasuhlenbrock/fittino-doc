.. _style-guide:

Style guide
===========

General remarks
---------------

Most of the overall style definitions are enforced by running the astyle command as the last step of
the development process of your class. However, the code has to satisfy a few more style conventions
used throughout Fittino that astyle cannot account for (e.g. sorting). This page is intended to
serve as a guidline.

Header files style
^^^^^^^^^^^^^^^^^^

**Include file order**

- Standard C++ include libraries
- ROOT include files
- Fittino include files

Seperate each block with a newline. Within each block sort the items alphabetically.

**Class member order**

Sort all class members according to their visibility:

- public static data members
- public data members
- public static function members
- public function members
- protected static data members
- protected data members
- protected static function members
- protected function members
- private static data members
- private data members
- private static function members
- private function members

Include operators after functions. Seperate each block with a newline. Within each block sort the
items alphabetically starting with the data type. 

- built-in types
- STL types
- ROOT classes
- Fittino classes

The only exeptions are the constructor and the destructor members which should be always the first
items in their respective block. Add virtual functions after all regular functions. Apart from that,
sort them like regular functions.

Source files style
^^^^^^^^^^^^^^^^^^

Sort the include files in the same way as in the header files. Arrange the implementation of the
functions in the same order as in the header file.  Seperate the functions with a newline.

After writing your code make sure everything is fine by using the astyle command: ::

   $ astyle –options=devel/astyle-header-options <filename.h>
   $ astyle –options=devel/astyle-options <filename.cpp>

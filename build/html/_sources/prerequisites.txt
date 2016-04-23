Prerequisites
=============

The following external programs/libraries are mandatory in order to compile Fittino

 - | The build system generator `CMake <http://www.cmake.org>`_ (version 3.2 or higher)
 - | A build tool supported by CMake, e.g. GNU `make <https://www.gnu.org/software/make/>`_ or
     `Xcode <https://developer.apple.com/xcode/>`_
 - | A C++ compiler, e.g. provided by the `GNU Compiler Collection <http://gcc.gnu.org>`_ (gcc) or
     the `Clang project <http://clang.llvm.org>`_
 - | The `Boost C++ libraries <http://www.boost.org>`_ (version 1.47.0 or higher)
 - | The data analysis framework `ROOT <http://root.cern.ch/>`_ (version 5.20.00 or higher)

A number of optional tools is used to simplify working with Fittino. Fittino can be built without
these but in that case some functionality is restricted. These include

  - | The source code formatter `astyle <http://astyle.sourceforge.net/>`_ (needed to ensure that
      the code is in accordance with the Fittino coding style, which is specified in the
      :ref:`style-guide`)
  - | The documentation generation system `doxygen <http://www.stack.nl/~dimitri/doxygen/>`_ (used
      to automatically generate a Fittino code reference)
  - | The XML C parser `Libxml2 <http://xmlsoft.org/>`_ (needed to validate Fittino input files)

For information on how to install and setup these programs/libraries, please consult the
documentation at the individual project's websites. If a program is installed on your system but
cannot be found nevertheless, you should check if the corresponding CMake variables are correctly
set as described in the :ref:`troubleshooting` section.

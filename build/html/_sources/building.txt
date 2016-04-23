Building and installing Fittino
===============================

The setup of the installation process is managed by CMake. Its main task is to identify and find the
installed required and optional software packages so that the Fittino code can be linked to the
corresponding libraries. For that, CMake consults dedicated :file:`CMakeList.txt` files in which the
dependencies of the individual Fittino modules are specified.

The system paths pointing to the installation of the external software packages are set by CMake's
``Find*.cmake`` modules. CMake comes already with a number of ``Find*.cmake`` modules for many
widely used programs and libraries (a list of available CMake modules can be obtained by typing
``cmake --help-module-list``). The ``Find*.cmake`` modules that come with Fittino can be found in
the ``CMakeModules/`` directory.  How to write a custom ``Find*.cmake`` module to link Fittino to
yet unsupported code is explained in the :ref:`developer-guide`.

It is recommended to build Fittino in a dedicated directory. This helps keeping a clean separation
between the source code and the built objects. So e.g. from Fittino’s root directory change to ::

    $ cd <build_directory/>

In order to configure the build process type ::

    $ cmake ..

To build Fittino type ::

    $ make

If the compilation is successful, an executable called "fittino" is produced in
``<build_directory>/sources/kernel``.

To install Fittino type ::

    $ make install

This copies the executable to ``bin/fittino`` and the example input files to ``share/fittino/input``
in the Fittino installation directory. The default installation directory is ``/usr/local/``, which
can be changed by setting the ``CMAKE_INSTALL_PREFIX`` variable (see the :ref:`troubleshooting`
section).

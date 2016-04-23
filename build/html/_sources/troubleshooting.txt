.. _troubleshooting:

CMake variables
===============
 
The behavior of CMake can be influenced by setting dedicated CMake variables. CMake variables can
be set using CMake arguments in two ways:

- Definition of the variables on the command line (``-D<VARIABLE_NAME>=<VARIABLE_VALUE>``)
- Specifying an initial cache file (``-C<PATH_TO_FILE>``) in which the variables are set

Many of the available CMake variables such as e.g. software installation paths are set automatically
when invoking CMake, without the need of user interaction. If this fails, however, the user might be
urged to set the variables by hand (see next section). On the other hand, the user might want to
install Fittino at a location different from the default. This can be achieved by setting
``CMAKE_INSTALL_PREFIX`` to the desired location, e.g. by typing ::

   cmake -DCMAKE_INSTALL_PREFIX=/custom/installation/path ..

Troubleshooting
===============

If the installation of Fittino fails, it is most likely due to a mandatory library which is not
found by CMake. In this case, it might be imperative to manually modify the CMake search paths. The
CMake search paths for external software can be influenced by setting the following dedicated CMake
variables

- BOOST_ROOT
- ROOT_CONFIG_DIR
- GSL_CONFIG_DIR
- HIGGSBOUNDS_INSTALLATION_PATH
- HIGGSSIGNALS_INSTALLATION_PATH
- FEYNHIGGS_INSTALLATION_PATH
- SLHAEA_INSTALLATION_PATH
- LHAPDF_INSTALLATION_PATH

and/or via the usual general CMake and environmental variables.

Outlook
=======

Things

- Even more modular installation
- Fittino SuperBuild

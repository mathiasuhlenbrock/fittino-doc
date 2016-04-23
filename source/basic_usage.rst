Basic usage
===========

The basic command structure of Fittino is ::

    $ ./fittino [OPTION(S)]

If Fittino is run without options, a help text providing short information about all available
options is shown.

The individual options are

.. option:: -h, --help

   A help text providing short information about all available options is shown

.. option:: -i FILE, --input-file=FILE

   Fittino uses the input file :file:`FILE`

   This is probably the most important option, since without specifying an input file, Fittino does
   not do anything useful. A Fittino input file is an XML file, which allows the detailed
   configuration of the program's behavior. For further information on input files, have a look at
   :ref:`input-files`. To help you getting started, a number of annotated example input files can be
   found in the ``input/`` directory

.. option:: -l FILE, --lock-file=FILE

   Fittino uses the file :file:`FILE` for inter process locking

.. option:: -v, --validate

   Fittino validates the input file using the libxml2 library

   This option is supposed to help you identifying possible issues with your custom input file.
   A warning or even an error is produced if you have specified an unsupported configuration item
   or if a required option is missing or incorrectly set

**Example:**

The command ::

    $ ./fittino -v -i ../input/Example.Rosenbrock.Simple.in.xml

runs Fittino using the input file :file:`Example.Rosenbrock.Simple.in.xml`. In addition the input
file is validated.

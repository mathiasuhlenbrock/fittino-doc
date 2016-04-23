.. _user-guide:

User guide
==========

In the following, the usage of Fittino is explained. It is assumed at this point that Fittino is
already successfully built and installed on your system. If this is not the case, you might have a
look at the :ref:`installation-guide` first.

It is not assumed that you have added the directory containing the built executable to your system
search :envvar:`PATH` (if you want to do this and do not know how, please check the documentation of
your operating system). So, in order to use Fittino, simply change to the directory containing the
built executable (e.g.  ``bin/``).

In the first section of this document the invocation of Fittino from the command line and the
available command line options are explained. The majority of configuration options, however, is
specified in so-called Fittino input files, which are covered thoroughly in the second section. At
last, a final section walks through a simple working example, explaining all the details of its
configuration and encourages the reader to experiment and manipulate some of the configuration
options on his or her own.

**Note:** The main purpose of Fittino is to provide tools to analyze highly complex and specialized
physics models. If you are about to fully exploit the capabilities of Fittino, you probably want to
write your own extensions to the program in addition to what is described here. If this is the case,
you also might have a look at the :ref:`developer-guide`.

.. toctree::
   :maxdepth: 1

   basic_usage
   input_files
   getting_started

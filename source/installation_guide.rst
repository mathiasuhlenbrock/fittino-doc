.. _installation-guide:

Installation guide
==================

At the time of the writing of this guide, no precompiled versions of Fittino are available. With
other words, in order to make use of the framework, it has to be built from its sources in advance.

This document provides instructions on how to obtain the Fittino source code from its repository and
how to build and install the program. Whereas the core functionality of Fittino depends only on
relatively few external packages, one of the framework's main functions is to provide simple and
flexible interfaces to a number of third-party theoretical physics programs and make these work
together seamlessly. A list of third-party software which is already supported to run with Fittino
can be found in a dedicated section. This list is by no means exhaustive and people are encouraged
to write custom extensions in order to include their own favorite code. More information on how this
is done is compiled in the :ref:`developer-guide`. Lastly, a final section deals with common issues
the reader might be faced with in the course of the installation process and provides some
troubleshooting guidance.

Fittino is being developed in a Unix-like environment, therefore a certain familiarity with this
class of operating systems and the usage of a command line shell is assumed in the following.

.. toctree::
   :maxdepth: 1

   source_code
   prerequisites
   building
   third_party_software
   troubleshooting

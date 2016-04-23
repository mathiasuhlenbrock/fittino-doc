Introduction
============

Fittino is a software framework written in C++, whose main focus is to extract information about
physical model parameters that are not directly accessible through experimental observation. The
underlying working principle is to find the set of parameters for which the model makes the "best"
predictions about the outcome of a number of physics experiments. For that, the model parameters are
varied and the model predictions are compared with the measured values repeatedly, until at some
point the optimal matching set can be derived. To this end, Fittino offers various powerful
optimization and sampling algorithms, next to a number of tools to assist with the statistical
interpretation. The main task of the framework, however, is to provide simple and flexible
interfaces in order to allow the user to include a great number of third-party theory packages in
his or her analysis.

The code is largely developed by a team at Bonn University, but has ever since benefited from
contributions by members of other universities and institutes as well. Historically, the physics
program of Fittino has concentrated on determining the parameters of supersymmetric models such as
the constrained Minimal Supersymmetric Standard Model (cMSSM). In recent times, however, detailed
studies of the parameters of the Higgs boson sector have been performed in addition.

Since its first release, the software has been subjected to major adoptions and expansions which
altogether justify the assignment of a new version number. It is the purpose of this document to
outline the most relevant changes to the experienced user and at the same time provide newcomers
with enough information to get quickly acquainted.

The document's body is divided into three main parts. The :ref:`installation-guide` informs the
reader about how to obtain the Fittino source code and which additional programs and libraries are
necessarily required in order to build and link the individual software components. It also contains
a list of third-party software which is already supported to work together with Fittino. The
:ref:`user-guide` gives instructions on the configuration and the basic usage of the program.
Finally, the :ref:`developer-guide` is intended to describe the software architecture of Fittino and
discusses the most important design decisions in order to help the reader to integrate his or her
own custom extension into the framework.

For more information, e.g. about the most recent developments in connection with Fittino, it is
recommended to subscribe to one of the available mailing lists. If, for example, you would like to
be notified about new code commits, subscribe to the `fittino-dev mailing list
<https://lists.desy.de/sympa/subscribe/fittino-dev>`_. In case you are more interested about the
physics aspects of Fittino, you can subscribe to the `fittino mailing list
<https://lists.desy.de/sympa/subscribe/fittino>`_.

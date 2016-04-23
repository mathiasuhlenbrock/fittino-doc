Tools
=====

Now that Fittino models are established and the desired predictions can be calculated from a set of
model parameters it is time to ask how to analyze these. Tools are algorithms. Analysis such as
optimization and sampling algorithms. There are also plotting devices.  As usual, the descripition
of the available tools starts with an overview of the configuration options common to all tools:

``Name``

   The tool's name.

``OutputFile``

   The name of the output file. All data produced by the tool is stored in this file. The default
   output file name is ``Fittino.out.root``.

``WriteAllModelQuantities``

   If set to ``true`` all quantities are written to the output file.

``Chi2Name``

   The name of the total :math:`\chi^2` value.

``InitialChi2Value``

   The total :math:`\chi^2` is initialized with this value.

``IterationCounterName``

   The name of the iteration counter.

``InitialIterationCounterValue``

   The iteration counter is initialized with this value.

``OutputTreeName``

   The name of the output data tree.

``MetaDataTreeName``

   The name of the meta data tree. Meta data such as error codes.

In the following sections the available (classes of) tools are described in full detail.

.. toctree::
   :maxdepth: 1

   histogrammakers
   optimizers
   plotters
   samplers

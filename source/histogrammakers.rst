HistogramMakers
===============

``HistogramMakers`` are supposed to help the user to convert the data produced by Fittino into
histograms. Among other things, histogrammed data has the advantage of requiring fewer storage space
and being easier to process. This is the reason why many ``Plotters`` operate only on histogrammed
data.

The configuration options common to all ``HistogramMakers`` are:

``AxisMaxDigits``

   Specifies the nuber of digits of the numeric tic labels.

``Histogram``

   ``Name``

      The name of the histogram.

   ``PlotName``

      The name of the plot.

   ``LogScale``

      Calculates and fills logarithmic bins.

   ``NumberOfBins``

      The number of histogram bins.

   ``LowerBound``

      The lower bound of the histogram.

   ``UpperBound``

      The upper bound of the histogram.

``Plotter``

   The ``Plotter`` used to render a graphic representation of the histogram. The available plotters
   and their configuration options are described in more detail in the section.

   They have a separate section because they also can be used standalone.

.. toctree::
   :maxdepth: 1

   contour_histogrammaker
   profile_histogrammaker
   simple1D_histogrammaker
   simple2D_histogrammaker
   simple3D_histogrammaker
   summary_histogrammaker

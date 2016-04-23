Plotters
========

Plotters can be used to produce graphic representations of the data created by Fittino. Hereby, the
various plotters aim to faciliate daily work standard plots to quickly obtain nicely rendered plots
without putting too much thougtht into it. A number of configruation options exist to accomodated
the user's needs as as possible.

Configuration options common to all plotters:

``LogScaleX``

   Sets the labels of the x-axis to logscale. To work properly with histograms, make sure that
   logarithmic bins have been filled.

``LogScaleY``

   Sets the labels of the y-axis to logscale. To work properly with histograms, make sure that
   logarithmic bins have been filled.

``LogScaleZ``

   Sets the labels of the z-axis to logscale. To work properly with histograms, make sure that
   logarithmic bins have been filled.

``FileFormat``

   Specifies the output file format. All output file formats that are supported by ROOT are likewise
   valid in Fittino.

``PageFormat``

   Currently there are two possible options: ``Landscape`` and ``Square``. ``Landscape`` is a
   rectangular 8:6 format, which is usually best suited if an even number of plots should be
   displayed in one row next to each other. ``Square`` is a quadratic format and should be used for
   an odd number of plots, respectively.

``Version``

   Specifies the release version of Fittino.

``LogoPath``

   An image whose location is specified by this option is placed at the top right corner of the
   plot.

The following plotters are available:

.. toctree::
   :maxdepth: 1

   contour_plotter
   profile_plotter
   simple_plotter
   summary_plotter
   toyfit_plotter

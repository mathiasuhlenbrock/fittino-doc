ContourHistogramMaker
=====================

Prepares the histograms for the contour plots. It should be used together with ``ContourPlotter``.
The execution of ``ContourHistogramMaker`` may take some time, depending on the number of data
points that have been sampled. It is therefore recommended to separate the histogram filling from
the actual plotting, in order not to have to re-run ``ContourHistogramMaker`` if only changes to the
graphical representation need to be applied.

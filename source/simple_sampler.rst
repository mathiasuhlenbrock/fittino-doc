SimpleSampler
=============

The ``SimpleSampler`` simply samples every point (incremented by the parameter error) within the
specified parameter bounds. For that, it loops recursively over the dimensions of the parameter
space. Understandably, this simple, brute-force approach is suited only for parameter spaces with
low dimensionality, since the computational costs raise with the power of the number of parameters.
Nevertheless, the ``SimpleSampler`` has its applications, e.g. if one wants to do a quick scan of a
sub-space (while keeping the other parameters fixed). More importantly, the ``SimpleSampler`` can be
used to produce a (coarse) grid of a parameter (sub-) space, where the computation of individual
points takes too much time. The points of the interpolated grid can then be sampled easily, which is
in some situations the only way to extract information about the parameter space of interest.

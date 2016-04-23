Optimizers
==========

The Fittino ``Optimizers`` are algorithms that try to find the best matching set of model parameters
based on a criterion that is usually a measure of agreement between the model predictions and the
corresponding experimental measurements.

The following configuration options are common to all Fittino ``Optimizers``:

``MaxNumberOfIterations``

    The maximal number of iterations to be processed.

``AbortCriterion``

    If the quantity that serves as a measure of agreement between the model predictions and the
    corresponding experimental measurements becomes smaller than that number, the algorithm aborts.

.. toctree::
   :maxdepth: 1

   genetic_algorithm_optimizer
   minuit_optimizer
   particle_swarm_optimizer
   simple_optimizer
   simulated_annealing_optimizer

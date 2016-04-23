Global configuration options 
============================

Find below a list of all input file configuration options which affect the global behavior of
Fittino.

``<VerbosityLevel>``

   The verbosity level configuration option specifies the amount of output that is produced in the
   course of the execution of Fittino. Three levels are available, ``ALWAYS``, ``INFO`` and
   ``DEBUG``. In this manner, ``ALWAYS`` produces only minimal output while ``DEBUG`` provides the
   most detailed information about the current status of the active tool and the model being
   analyzed. The default verbosity level is ``ALWAYS``.

**Example:** ::

   <VerbosityLevel>INFO</VerbosityLevel>

sets the verbosity level to ``INFO``, which produces a bit more output than the default ``ALWAYS``.

``<RandomSeed>``

   The random seed configuration option specifies the seed for the random number generators used
   within Fittino. The choice of a fixed random seed ensures that the result of consecutive Fittino
   runs is reproduced. If, however, statistically independent results are intended, the random seed
   has to be changed for each individual run. The random seed configuration option takes an integer
   number as an argument and defaults to 0.

**Example:** ::

   <RandomSeed>3141</RandomSeed>

sets the random seed to 3141.

In the next section the configuration of :ref:`models` for Fittino is explained in full detail.

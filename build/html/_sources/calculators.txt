.. _calculators:

Calculators
===========

``Calculators`` play a central role within the Fittino framework. They can be thought of as
computing units which transform a set of input variables into a set of output variables. As such,
the ``Calculators`` are ultimately responsible to calculate the model predictions from a given set
of input parameters.

There exist already a number of theory programs, calculating predictions for physics experiments,
which are developed and maintained by experts of their respective fields. These programs, however,
are usually highly specialized and concentrate solely on the calculation of a single aspect of more
comprehensive models. In High Energy Physics, for example, separate programs for the computation of
the masses of Supersymmetric Particles, the Dark Matter Relic Density and the outcome of Flavor
Physics experiments are available. The reason for this separation is that the relationships between
the different kinds of phenomena are unclear. To shed light on the possible connections within a
more comprehensive model, however, is exactly among the tasks of programs such as Fittino, which
provide common interfaces in order to combine the output of codes from very different sources. The
``Calculators`` can now be understood as wrapper classes around third party software, implementing
the interfaces. Furthermore, Fittio comes with a number of built-in ``Calculators`` serving various
purposes. Apart from calculating additional physical model predictions, these ``Calculators`` may
be applied to very general (intermediate) processing tasks, such as the calculation of a formula or
the interpolation of a parameter grid.

To conclude, instead of defining a single ``Calculator``, a physics model usually constitutes a
chain of ``Calculators``, meaning a set of ``Calculators`` which are executed successively. This
approach allows for a flexible combination of ``Calculators`` and enables more sophisticated use
cases such as the parallel execution of the same ``Calculator`` with different configurations.

The various available ``Calculators`` and their configuration options are described in the
following. One configuration option is common to all calculators:

``Tag``

   The tag of the calculator. If specified, the tag is appended to all quantities that are computed
   by the ``Calculator``. This is especially useful if the same quantity should be computed multiple
   times by different ``Calculators`` or by several instances of the same ``Calculator`` with
   different configuration options.

**Example**

By specifying ::

   <Tag>MyCalculatorTag<Tag>

any ``Quantity`` is renamed to ``MyCalculatorTag_Quantity``. 

.. toctree::
   :maxdepth: 1

   chi2_calculator
   formula_calculator
   linearinterpolation_calculator
   regression_calculator
   rosenbrock_calculator
   tree_calculator

.. astro_calculator 
   astrofit_calculator 
   checkmate_calculator
   checkvacuum_calculator
   feynhiggs_calculator
   feynhiggs_rescaling_calculator
   gm2calc_calculator
   hdim6_calculator
   hec_calculator
   hepmcsplit_calculator
   herwigpp_calculator
   higgsbounds_calculator
   higgssignals_calculator
   lhcchi2_calculator
   lhclimit_calculator
   madgraph_calculator
   micromegas_calculator
   nllfast_calculator
   smodels_calculator
   spheno_calculator
   superiso_calculator

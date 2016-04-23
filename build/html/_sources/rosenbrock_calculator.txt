RosenbrockCalculator
====================

The ``RosenbrockCalculator`` evaluates the Rosenbrock function

.. math::

   f(\mathbf{x})=\sum_{i=1}^{N}\left(1-x_{i-1}\right)^2+100\cdot\left(x_{i}-x_{i-1}^2\right)^2

for an arbitrary number of arguments :math:`N`. The Rosenbrock function is a simple but not trivial
optimization problem which can be used as a test model for the validation of Fittino's
functionality, especially for the optimization and sampling algorithms. For low dimensionality, the
Rosenbrock function can also be computed by the ``FormulaCalculator`` but at some point the explicit
notation becomes tedious. In addition, the ``RosenbrockCalculator`` might be a helpful simplistic
example for developers who want to implement their own custom ``Calculator`` class.

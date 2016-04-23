FormulaCalculator
=================

The ``FormulaCalculator`` can be used to calculate a novel quantity from existing quantities using a
mathematical formula. Since Fittino uses the ROOT class ``TFormula`` for formulas, the ROOT
conventions for formula strings are simply adapted. Within the formulas, existing quantities are
referenced by name. For more information on how formula strings are written in ROOT and which
mathematical expressions are available, please have a look at the documentation at the ROOT
homepage.

The ``FormulaCalculator`` can be configured using the following options:

``Name``

   The name of the calculated quantity.

``Formula``

   The ROOT markup string of the formula.

**Example:** ::

  <ModelParameter>
    <Name>X1</Name>
    <Error>0.01</Error>
    <LowerBound>-2</LowerBound>
    <UpperBound>2</UpperBound>
  </ModelParameter>

  <ModelParameter>
    <Name>X2</Name>
    <Error>0.01</Error>
    <LowerBound>-2</LowerBound>
    <UpperBound>2</UpperBound>
  </ModelParameter>

  <FormulaCalculator>
    <Name>Parabola</Name>
    <Formula>[X1]^2+[X2]^2</Formula>
  </FormulaCalculator>

calculates a two-dimensional parabola from the model parameters ``X1`` and ``X2``.

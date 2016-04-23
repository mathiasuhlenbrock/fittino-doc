.. _models:

Models
======

The ``<Model>`` element specifies the (physical) model being analyzed by Fittino. In physics, a
model is understood as a collection of mathematical prescriptions ("formulas") which map a set of
parameters onto a set of predictions about the outcome of a set of experimental measurements. By
finding models where the adaption of a few parameters lead to accurate predictions about a wealth of
experimental measurements one hopes to gain deeper insight into the underlying principles of Nature.
Often, however, one is faced with the situation that the model parameters themselves are not directly
accessible by experiments. Fittino has been developed to obtain information about the model
parameters in this case, nevertheless.

The level of accuracy between a theoretical prediction and a measurement is quantified as the
so-called :math:`\chi^2` value, which is the error-weighted squared difference between prediction
and measurement. A number of tools in Fittino try to minimize the :math:`\chi^2` value which is
equivalent to finding the set of parameters that provides the best description of Nature (within the
limits of the model). The determination of the :math:`\chi^2` value from a set of model parameters
is accomplished by a collection of dedicated so-called ``Calculators``. With other words, in order
to configure a model, the user mainly has to specify the list of model parameters and choose a
collection of ``Calculators``. In the following, the list of all model configuration options is
presented.

``<Name>``

   The name of the model. This name appears at various locations in the output of the program and
   hereby helps with the organization of output files.

**Example:** ::

   <Name>CMSSM</Name>

sets the model name to ``CMSSM``.

``<Tag>`` 

   The tag of the model.

**Example:** ::

   <Tag>CMSSM</Tag>

sets the model tag to ``CMSSM``.

``<ModelParameter>``

   Specifies a new model parameter. A model parameter can further be configured with the following
   options:

   ``<Name>``

      The name of the parameter.

   ``<PlotName>``

      The ROOT markup string for the name of the parameter. Since Fittino uses ROOT to make plots,
      the ROOT markup conventions for formatted labels are simply adapted. For more information on
      how formatted labels are marked in ROOT, please have a look at the documentation at the ROOT
      homepage.

   ``<Value>``

      The initial value of the parameter. This option is ignored if an analysis tool calculates the
      starting value of the parameter on its own.

   ``<Error>``

      This value serves as a measure for the scale on which the parameter is allowed to vary.
      Depending on the used analysis tool this value is interpreted differently. Possible
      interpretations are e.g. a step width or a standard deviation in a Gaussian smearing.

   ``<Unit>``

      The physical unit of the parameter.

   ``<PlotUnit>``

      The ROOT markup string for the physical unit of the parameter.

   ``<LowerBound>``

      A parameter cannot assume a value below this limit.

   ``<UpperBound>``

      A parameter cannot assume a value above this limit.

   ``<Fixed>``

      If set to ``true`` the parameter is kept fixed on its starting value specified by the
      ``<Value>`` element. The default value for this option is ``false``.

**Example:** ::

   <ModelParameter>
     <Name>Mass_h</Name>
     <PlotName>M_{h}</PlotName>
     <Value>125.5</Value>
     <Error>0.3</Error>
     <Unit>GeV</Unit>
     <PlotUnit>GeV</PlotUnit>
     <LowerBound>120</LowerBound>
     <UpperBound>130</UpperBound>
     <Fixed>false</Fixed>
   </ModelParameter>

specifies a new model parameter named ``Mass_h``. The parameter can be varied between 120 and 130
GeV, with step width 0.3 GeV starting at 125.5 GeV.

``<Calculator>``

   One or more calculators can be specified with this element. Detailed information about the
   available calculators and their individual configuration options can be found in the
   :ref:`calculators` section.

   **Note:** The calculators are executed in the same order as they are specified, which means that
   **order matters**!

``<Chi2Contribution>``

   The ``<Chi2Contribution>`` takes the name of a quantity as an argument. The value of this
   quantity is added to the global :math:`\chi^2` value.

**Example:** ::

   <Chi2Contribution>Penalty</Chi2Contribution>

adds the value of ``Penalty`` to the global :math:`\chi^2` value. ``Penalty`` needs to be calculated
by a dedicated calculator.

In conclusion, the overall structure of a model looks like this ::

   <Model>
     <Name>ModelName</Name>
     <Tag>ModelTag</Tag>
     <ModelParameter>
       ...
     </ModelParameter>
     ...
     <Calculator>
       ...
     </Calculator>
     ...
     <Chi2Contribution>
       ...
     </Chi2Contribution>
     ...
   </Model>

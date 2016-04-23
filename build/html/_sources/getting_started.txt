.. _getting-started:

Getting started
===============

In this section, the functionality of Fittino is discussed in detail with the help of a simple but
not trivial example optimization problem. It is assumed at this point, that Fittino is successfully
built and installed on the reader's system and that he or she is equipped with a working knowledge
of the basic usage of the software framework. If this is not the case it is recommmended to consult
the Installation guide and/or the previous sections of this guide beforehand.

The optimization problem is the 2-dimensional Rosenbrock function.

At first, let's have a look at input file ``Example.Rosenbrock.Simple.in.root`` which can be found
in the ``input/`` subdirectory ::

   <?xml version="1.0" encoding='UTF-8'?>
   <?xml-stylesheet type="text/xsl" href="style/InputFile.xsl"?>

   <InputFile>

     <VerbosityLevel>ALWAYS</VerbosityLevel>

     <Model>
       <Name>2D Parabola</Name>

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
         <Formula>[X1]**2+[X2]**2</Formula>
       </FormulaCalculator>
     </Model>

     <Tool>
       <SimpleSampler></SimpleSampler>
     </Tool>

   </InputFile>

The first line indicates XML file. Second line is a reference to the style sheet files. Input file
can be opend with browser the properties are into tables better for overview of complicated files.

The verbosity level is set to always which means that only the most important information is printed
out. Then the model is defined. The model consists of two parameters x_1 and x_2.

Output ::

   ---------------------------------------------------------------------------------------

     Welcome to Fittino

   ---------------------------------------------------------------------------------------

     Initializing the Rosenbrock model

     Initializing the list of model parameters

   ---------------------------------------------------------------------------------------
   
     Initializing the Simple parameter sampler
   
      Configuration
   
       Name                                               Simple parameter sampler
       OutputFileName                                     Fittino.out.root
       WriteAllModelQuantities                            1
       Chi2Name                                           Chi2
       InitialChi2Value                                   inf
       IterationCounterName                               IterationCounter
       InitialIterationCounterValue                       0
       OutputTreeName                                     Tree
       MetaDataTreeName                                   MetaDataTree
   
   ---------------------------------------------------------------------------------------
   
     Running the Simple parameter sampler
   
   ---------------------------------------------------------------------------------------
   
     Terminating the Simple parameter sampler
   
   ---------------------------------------------------------------------------------------

After displaying a short welcome logo, Fittino initializes the model and its individual components.
Then, the analysis tool is initialized which is the ``SimpleSampler``. One can see that all data is
written out to a ROOT file called ``Fittino.out.root``. The data tree is called ``Tree`` and the
meta data tree is called ``MetaDataTree``.

If the verbosity level is changed Detailed Output ::

   ---------------------------------------------------------------------------------------

     Welcome to Fittino

   ---------------------------------------------------------------------------------------

     Initializing the Rosenbrock model

      Initializing the list of model parameters

       X1                                                 0.00e+00
       X2                                                 0.00e+00

   ---------------------------------------------------------------------------------------
   
     Initializing the Simple parameter sampler
   
      Configuration
   
       Name                                               Simple parameter sampler
       OutputFileName                                     Fittino.out.root
       WriteAllModelQuantities                            1
       Chi2Name                                           Chi2
       InitialChi2Value                                   inf
       IterationCounterName                               IterationCounter
       InitialIterationCounterValue                       0
       OutputTreeName                                     Tree
       MetaDataTreeName                                   MetaDataTree
   
   ---------------------------------------------------------------------------------------
   
     Running the Simple parameter sampler
   
   ---------------------------------------------------------------------------------------
   
     Iteration step 1
   
     Set of Rosenbrock model parameters:
   
       X1                                                -2.00e+00
       X2                                                -2.00e+00
   
       -----------------------------------------------------------
   
       Total chi2                                         3.61e+03

   ---------------------------------------------------------------------------------------

   ...

   ---------------------------------------------------------------------------------------
   
     Terminating the Simple parameter sampler
   
   ---------------------------------------------------------------------------------------

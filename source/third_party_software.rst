Third-party software
====================

The following list contains a number of theoretical physics programs which are supported by Fittino.
Within the framework, each program corresponds to a (set of) so-called ``Calculator`` (``s``), which
can be understood as (a) wrapper class(es) allowing for a unified integration of the different codes
and presenting a unified interface. If a user wants to make a program not on this list work together
with Fittino, all he or she has to do is to write a ``Find*.cmake`` module and a corresponding
``Calculator`` class.

- | `FeynHiggs <http://www.feynhiggs.de/>`_: Fortran code for the diagrammatic calculation of the
    masses, mixings and much more of Higgs bosons in the MSSM at the two-loop level
  | **Requires:**

    - The Fortran compilers `gfortran <https://gcc.gnu.org/wiki/GFortran>`_ or `ifort
      <https://software.intel.com/en-us/fortran-compilers>`_

- | `GM2Calc <http://gm2calc.hepforge.org/>`_: Precise calculation of the muon anomalous magnetic
    moment in the MSSM
  | **Requires:**

    - `Eigen <http://eigen.tuxfamily.org/index.php?title=Main_Page>`_: A C++ template library for
      linear algebra

- | `HepMC <http://lcgapp.cern.ch/project/simu/HepMC/>`_: A C++ Event Record for Monte Carlo
    Generators
- | `HiggsBounds <http://higgsbounds.hepforge.org/>`_: HiggsBounds takes a selection of Higgs
    sector predictions for any particular model as input and then uses the experimental topological
    cross section limits from Higgs searches at LEP, the Tevatron and the LHC to determine if this
    parameter point has been excluded at 95% C.L.
  | **Requires:**

    - The Fortran compilers `gfortran <https://gcc.gnu.org/wiki/GFortran>`_ or `ifort
      <https://software.intel.com/en-us/fortran-compilers>`_

- | `HiggsSignals <http://higgsbounds.hepforge.org/>`_: HiggsSignals performs a statistical test of
    the Higgs sector predictions of arbitrary models (using the HiggsBounds input routines) with
    the measurements of Higgs boson signal rates and masses from the Tevatron and the LHC
  | **Requires:**

    - The Fortran compilers `gfortran <https://gcc.gnu.org/wiki/GFortran>`_ or `ifort
      <https://software.intel.com/en-us/fortran-compilers>`_

- | `Micromegas <https://lapth.cnrs.fr/micromegas/>`_: A code for the calculation of Dark Matter
    Properties including the relic density, direct and indirect rates in a general supersymmetric
    model and other models of New Physics
  | **Requires:**

    - `X11 <http://www.x.org/wiki/>`_: The X Window System

- | `SuperIso <http://superiso.in2p3.fr/>`_: Calculation of flavour physics observables
 
The following programs need not to be present at compile-time in order to build Fittino. However,
Fittino needs the individually required packages to be present at compile-time. For example, in
order to build Fittino with support for SPheno, SLHAea is mandatory. In order to use one of these
program at run-time, it needs to be installed and (a pointer to) the executable must exit in the
directory from where Fittino is invoked.

- | `CheckMATE <http://checkmate.hepforge.org/>`_: A tool to easily test simulated event files
    against LHC results
- | `Herwig++ <http://herwig.hepforge.org/>`_: Herwig++ is a particle physics event generator,
    written in C++
- | `MadGraph <https://cp3.irmp.ucl.ac.be/projects/madgraph/>`_: A framework that aims at providing
    all the elements necessary for SM and BSM phenomenology, such as the computations of cross
    sections, the generation of hard events and their matching with event generators, and the use
    of a variety of tools relevant to event manipulation and analysis
- | `NLLFast <http://pauli.uni-muenster.de/~akule_01/nllwiki/index.php/NLL-fast>`_: A computer
    program which computes the squark and gluino hadroproduction cross sections including
    next-to-leading order (NLO) supersymmetric QCD corrections and the resummation of soft gluon
    emission at next-to-leading-logarithmic (NLL) accuracy
- | `SmodelS <http://smodels.hephy.at/wiki>`_: A tool for interpreting simplified-model results
    from the LHC
  | **Requires:**

    - The `Python <https://www.python.org/>`_ programming language

- | `SPheno <https://spheno.hepforge.org/>`_: SPheno stands for S(upersymmetric) Pheno(menology).
    The code calculates the SUSY spectrum using low energy data and a user supplied high scale
    model as input
  | **Requires:**

    - `SLHAea <http://fthomas.github.io/slhaea/>`_: An easy to use C++ library for input, output,
      and manipulation of data in the SUSY Les Houches Accord (SLHA)

A number of smaller projects, to which also members of the Fittino development team are
contributing, is hosted in the same repository as Fittino and can be found in the ``external/``
directory. These are

- | CheckVacuum
- | HDim6
  | **Requires:**

    - | `LHAPDF <https://lhapdf.hepforge.org/>`_: A general purpose C++ interpolator, used for
        evaluating PDFs from discretised data files
    - | `GSL <http://www.gnu.org/software/gsl/>`_: The GNU Scientific Library

.. - | Astro
   - | AstroFit
   - | LHCLimit

Again, for information on how to install and setup these programs/libraries, it is recommended to
consult the documentation at the individual project's websites.

---
layout: default
title: Coupled Codes
permalink: /codes/
---

# Coupled Codes

There are various codes - free and proprietary ones - currently coupled with preCICE. If you want to add your code here, please let us know.

**Official adapters:** [CalculiX](#calculix), [OpenFOAM](#openfoam), [SU2](#su2), [Code_Aster](#code_aster), [FEniCS](#fenics), [Fluent](#fluent), [COMSOL Multiphysics](#comsol-multiphysics)

**Third-party adapters:** [Ateles (APES)](#ateles-apes), [Alya System](#alya-system), [FASTEST](#fastest), [FEAP](#feap)

**Legacy adapters:** [Carat++](#carat), [EFD](#efd), [foam-extend](#foam-extend), [Peano](#peano)

## Official adapters

These adapters are hosted on [GitHub](https://github.com/precice/) and
are maintained by us. We try to keep these adapters up-to-date and we constantly
strive to improve their quality, compatibility, and feature coverage.
If you would like to contribute to these adapters, please [contact us](../resources/#contact)!

### CalculiX

[CalculiX](http://www.calculix.de/) is a free/open-source (GPL) Finite Element solver, developed at the [MTU Aero Engines](http://www.mtu.de/).

* **Adapter's repository:** [precice/calculix-adapter](https://github.com/precice/calculix-adapter) (C/Fortran)
* **Status:** <span style="color:green">up-to-date</span>
* **CalculiX versions:** 2.10, 2.12, 2.13 (2.14 coming soon)
* **Typical applications:** Fluid-Structure Interaction (structure part), Conjugate Heat Transfer (solid part), Structure-Structure Coupling
* **Can write:** Force, Displacement, Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient
* **Can read:** Force, Displacement, Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient
* **Tutorials:**
   * [FSI with SU2 and CalculiX](https://github.com/precice/precice/wiki/FSI-tutorial) (also [in your browser](http://run.precice.org/))
   * [CHT with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-CHT-with-OpenFOAM-and-CalculiX)
   * [SSI with CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-SSI-with-CalculiX)

### OpenFOAM

OpenFOAM is a free/open-source (GPL) collection of free/open-source Finite Volume solvers mainly for CFD.
Today, there are two major "flavors" of OpenFOAM, one developed by the OpenFOAM Foundation ([openfoam.org](https://openfoam.org/), [GitHub](https://github.com/OpenFOAM)) and one developed by the [ESI Group](https://www.esi-group.com/) ([openfoam.com](https://www.openfoam.com/), [GitLab](https://develop.openfoam.com/)).

* **Adapter's repository:** [precice/openfoam-adapter](https://github.com/precice/openfoam-adapter) (C++)
* **Status:** <span style="color:green">up-to-date</span>
* **OpenFOAM versions:** 4.0-dev (.org), v1706-? (.com)
* **Typical applications:** Conjugate Heat Transfer (fluid and solid parts), Fluid-Structure Interaction (fluid part).
* **Can write:** Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient, Force
* **Can read:** Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient, Displacement
* **Tutorials:**
  * [CHT with OpenFOAM](https://github.com/precice/openfoam-adapter/wiki/Tutorial-for-CHT:-Flow-over-a-heated-plate)
  * [CHT with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-CHT-with-OpenFOAM-and-CalculiX)
  * [FSI with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-FSI-with-OpenFOAM-and-CalculiX)

### SU2

[SU2](https://su2code.github.io/) is a free/open-source (LGPL) solver for CFD, hosted on [GitHub](https://github.com/su2code).

* **Adapter's repository:** [precice/su2-adapter](https://github.com/precice/su2-adapter) (C++)
* **Status:** <span style="color:green">up-to-date</span>
* **SU2 versions:** 4.0.x-6.0.x
* **Typical applications:** Fluid-Structure Interaction (fluid part)
* **Can write:** Force
* **Can read:** Displacement
* **Tutorials:**
  * [FSI with SU2 and CalculiX](https://github.com/precice/precice/wiki/FSI-tutorial) (also [in your browser](http://run.precice.org/))

### Code_Aster

[Code_Aster](https://code-aster.org/) is a free/open-source (GPL) Finite Element solver, developed at the [Electricite De France](https://www.edf.fr/).

* **Adapter's repository:** [precice/code_aster-adapter](https://github.com/precice/code_aster-adapter) (Python)
* **Status:** <span style="color:orange">needs small updates</span>
* **Code_Aster versions:** 12 (currently not actively maintained)
* **Typical applications:** Conjugate Heat Transfer (solid part)
* **Can write:** Sink Temperature, Heat Transfer Coefficient
* **Can read:** Sink Temperature, Heat Transfer Coefficient
* **Tutorials:** No step-by-step tutorials are available at the moment. However,
you may like to have a look at Section 4.4 of [Lucia Cheung Yau's master's thesis](https://www5.in.tum.de/pub/Cheung2016_Thesis.pdf).

### FEniCS

[FEniCS](https://fenicsproject.org/) is an open-source (LGPLv3) computing platform for solving partial differential equations (PDEs), developed by the [FEniCS Community](https://fenicsproject.org/community/).

* **Adapter's repository:** [precice/fenics-adapter](https://github.com/precice/fenics-adapter) (Python)
* **Status:** <span style="color:red">experimental</span>
* **FEniCS versions:** 2017.2.0
* **Tutorials:** No step-by-step tutorials are available at the moment. However,
you may like to have a look at the tutorials in the adapter repository.

### Fluent

[Fluent](https://www.ansys.com/products/fluids/ansys-fluent) is a commercial Finite Volume solver for CFD, developed by [ANSYS](https://www.ansys.com/).

* **Adapter's repository:** [precice/fluent-adapter](https://github.com/precice/fluent-adapter) (C)
* **Status:** <span style="color:red">out-of-date</span> (a new version is coming soon)
* **Typical applications:** Fluid-Structure Interaction (fluid part)
* **Notes:** Only incompressible flow simulations are supported.

### COMSOL Multiphysics

[COMSOL Multiphysics](https://www.comsol.com/comsol-multiphysics) is a commercial Finite Element solver developed by [COMSOL](https://www.comsol.com/).

* **Adapter's repository:** [precice/comsol-adapter](https://github.com/precice/comsol-adapter) (C)
* **Status:** <span style="color:red">out-of-date</span>
* **Typical applications:** Fluid-Structure Interaction (structure part)

## Third-party adapters

These adapters have been developed by the preCICE community. For more information
on these adapters, you may contact the respective developers.
If you have written any other adapter, please [let us know](../resources/#contact)!

### Ateles (APES)

Ateles is an in-house acoustics far-field solver, developed at the [University of Siegen](http://www.uni-siegen.de/).

* **Contact:** University of Siegen, [Simulationstechnik und Wissenschaftliches Rechnen](https://www.mb.uni-siegen.de/sts/index.html).
* **Typical applications:** Fluid-Acoustics, Fluid-Fluid coupling.

### Alya System

[Alya](https://www.bsc.es/research-development/research-areas/engineering-simulations/alya-high-performance-computational) is an in-house Computational Mechanics solver developed at the [Barcelona Supercomputing Center](https://www.bsc.es/).

* **Contact:** An in-house adapter has been developed at the [Chair of Scientific Computing of the Technical University of Munich](https://www5.in.tum.de/).
* **Typical applications:** Fluid-Structure Interaction (flow and structure part)
* **Notes:** This adapter is currently not actively maintained, but it is also not abandoned.

### FASTEST

[FASTEST](https://www.fnb.tu-darmstadt.de/forschung_fnb/software_fnb/software_fnb.en.jsp) is an in-house CFD code, developed at the [FNB institute, Technical University of Darmstadt](https://www.fnb.tu-darmstadt.de/).

* **Contact:** [FNB institute, Technical University of Darmstadt](https://www.fnb.tu-darmstadt.de/)
* **Typical applications:** Fluid-Structure-Acoustics Interaction (fluid part)
* **Notes:** The adapter can send the acoustics source terms, it cannot receive (uni-directional coupling).

### FEAP

[FEAP](http://projects.ce.berkeley.edu/feap/) is a commercial Finite Element code, developed at the [University of California, Berkeley](https://www.ce.berkeley.edu/).

* **Contact:** An in-house adapter has been developed at the [FNB institute, Technical University of Darmstadt](https://www.fnb.tu-darmstadt.de/).
* **Typical applications:** Fluid-Structure Interaction (structure part)


## Legacy adapters

These adapters and/or the respective solvers are not maintained and might not work anymore, but are
listed here as an example of what other projects have used preCICE in the past.

### Carat++

[Carat++](http://carat.st.bv.tum.de/) is a Finite Element code developed at the [Chair of Structural Analysis of the Technical University of Munich](http://www.st.bv.tum.de/).

* **Contact:** An in-house adapter for preCICE has been developed at the [Chair of Structural Analysis of the Technical University of Munich](http://www.st.bgu.tum.de/en/software/research/carat/). To the best of our knowledge, this adapter is not maintained anymore.
* **Typical applications:** Fluid-Structure Interaction (structure part)

### EFD

[EFD](https://github.com/precice/efd) was a free/open-source "Eulerian finite difference (EFD) fluid solver", which was coupled to preCICE. It was developed at the [Chair of Scientific Computing of the Technical University of Munich](https://www5.in.tum.de/). This solver is not maintained anymore and does not work with the current version of preCICE.

* **Contact:** The solver is hosted on [GitHub](https://github.com/precice/efd).
* **Typical applications:** Fluid-Structure Interaction (fluid part).

### foam-extend

[foam-extend](https://sourceforge.net/projects/foam-extend/) is a free/open-source (GPL) collection of free/open-source Finite Volume solvers mainly for CFD. It is one of earliest and most popular forks of OpenFOAM.

* **Contact:** The project [FOAM-FSI](https://github.com/davidsblom/FOAM-FSI), part of  the dissertation of [David Blom](https://www.researchgate.net/profile/David_Blom2) at the [Aerodynamics group of TU-Delft](https://www.tudelft.nl/index.php?id=4542&L=1) coupled foam-extend solvers using preCICE.
* **Typical applications:** Fluid-Structure Interaction (fluid and structure parts), Fluid-Fluid coupling.
* **Notes:** This project is not actively maintained anymore.

### Peano

[Peano](http://www.peano-framework.org/) is a free/open-source (GPL) "Framework for Solvers on Spacetree Grids", developed from 2009-2012 at the [Chair of Scientific Computing at the Technical University of Munich](https://www5.in.tum.de/) and today at the [Durham University](https://community.dur.ac.uk/tobias.weinzierl/home.html).

* **Contact:** A preCICE adapter has been developed in the past at the [Chair of Scientific Computing at the Technical University of Munich](https://www5.in.tum.de/). This adapter is not maintained anymore and does not work with the current version of preCICE.
* **Typical applications:** Fluid-Structure Interaction (flow part)

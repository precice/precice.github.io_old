---
name: OpenFoam
ID: openfoam
category: official
order: 1
repository: https://github.com/precice/openfoam-adapter
language: C++
status: up-to-date
application: Conjugate Heat Transfer (fluid and solid parts), Fluid-Structure Interaction (fluid part).
can-write: Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient, Force
can-read: Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient, Displacement
versions: 4.0-dev (.org), v1706-v1812 (.com)
---

OpenFOAM is a free/open-source (GPL) collection of free/open-source Finite Volume solvers mainly for CFD.
Today, there are two major "flavors" of OpenFOAM, one developed by the OpenFOAM Foundation ([openfoam.org](https://openfoam.org/), [GitHub](https://github.com/OpenFOAM)) and one developed by the [ESI Group](https://www.esi-group.com/) ([openfoam.com](https://www.openfoam.com/), [GitLab](https://develop.openfoam.com/)).

Build/tests status: <a style="text-decoration: none" href="https://travis-ci.org/precice/openfoam-adapter" target="_blank"><img src="https://travis-ci.org/precice/openfoam-adapter.svg?branch=master" alt="Build status"></a>

#### Tutorials:
  * [CHT with OpenFOAM](https://github.com/precice/openfoam-adapter/wiki/Tutorial-for-CHT:-Flow-over-a-heated-plate)
  * [CHT with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-CHT-with-OpenFOAM-and-CalculiX)
  * [FSI with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-FSI-with-OpenFOAM-and-CalculiX)

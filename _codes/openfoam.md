---
name: OpenFOAM
ID: openfoam
category: official
order: 1
repository: https://github.com/precice/openfoam-adapter
language: C++
status: up-to-date
application: Conjugate Heat Transfer (fluid and solid parts), Fluid-Structure Interaction (fluid part), Fluid-Fluid Coupling (currently in develop branch).
can-write: Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient, Force, Stress, Pressure, Pressure Gradient, Velocity, Velocity Gradient
can-read: Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient, Displacement, Pressure, Pressure Gradient, Velocity, Velocity Gradient
versions: v1706-v2006 (.com), 4.0-7 (.org)
notes: This adapter can work either as 3D or 2D and it also supports nearest-projection mapping.
---

OpenFOAM is a free/open-source (GPL) collection of free/open-source Finite Volume solvers mainly for CFD.
We constantly update the adapter and try to support recent versions of both the [ESI Group](https://www.esi-group.com/) ([openfoam.com](https://www.openfoam.com/), [GitLab](https://develop.openfoam.com/)) flavor, as well as the OpenFOAM Foundation ([openfoam.org](https://openfoam.org/), [GitHub](https://github.com/OpenFOAM)) flavor.

Build / system tests status: <a style="text-decoration: none" href="https://travis-ci.org/precice/openfoam-adapter" target="_blank"><img src="https://travis-ci.org/precice/openfoam-adapter.svg?branch=master" alt="Build status"></a>

#### Tutorials:
  * [CHT with OpenFOAM](https://github.com/precice/openfoam-adapter/wiki/Tutorial-for-CHT:-Flow-over-a-heated-plate)
  * [CHT with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-CHT-with-OpenFOAM-and-CalculiX)
  * [CHT with OpenFOAM and Code_Aster](https://github.com/precice/code_aster-adapter/wiki/Flow-over-plate-Code_Aster-Tutorial)
  * [FSI with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-FSI-with-OpenFOAM-and-CalculiX)
  * [FSI with OpenFOAM and deal.II](https://github.com/precice/precice/wiki/Tutorial-for-FSI-with-deal.II-and-OpenFOAM)
  * [FF with OpenFOAM](https://github.com/precice/openfoam-adapter/tree/develop/tutorials/FF/pipe-pipe) (currently in develop, more documentation soon)
  * and [more](https://github.com/precice/openfoam-adapter/wiki)

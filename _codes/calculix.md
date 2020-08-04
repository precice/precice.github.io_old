---
name: CalculiX
ID: calculix
category: official
order: 4
repository: https://github.com/precice/calculix-adapter
language: C/Fortran
status: up-to-date
application: Fluid-Structure Interaction (structure part), Conjugate Heat Transfer (solid part), Structure-Structure Coupling
can-write: Force, Displacement, Displacement Delta, Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient
can-read: Force, Displacement, Temperature, Heat Flux, Sink Temperature, Heat Transfer Coefficient
versions: 2.15, 2.16 (different adapter version for each). 2.17 coming soon.
notes: This adapter also supports nearest-projection mapping.
---
[CalculiX](http://www.calculix.de/) is a free/open-source (GPL) Finite Element solver, developed at the [MTU Aero Engines](http://www.mtu.de/).

Build / system tests status: <a style="text-decoration: none" href="https://travis-ci.org/precice/calculix-adapter" target="_blank"><img src="https://travis-ci.org/precice/calculix-adapter.svg?branch=master" alt="Build status"></a>

#### Tutorials:
   * [FSI with SU2 and CalculiX](https://github.com/precice/precice/wiki/FSI-tutorial) (also [in your browser](http://run.precice.org/))
   * [CHT with OpenFOAM and CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-CHT-with-OpenFOAM-and-CalculiX)
   * [SSI with CalculiX](https://github.com/precice/precice/wiki/Tutorial-for-SSI-with-CalculiX)
   * and [more](https://github.com/precice/calculix-adapter/wiki)

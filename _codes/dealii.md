---
name: deal.II
ID: dealii
category: official
order: 3
repository: https://github.com/precice/dealii-adapter
language: C++
status: up-to-date
application: Finite element method, in this case fluid-structure interaction (solid part)
can-write: Displacement
can-read: Forces
versions: Developed in deal.II 9.1.0, newer versions should also work.
notes: Example with linear elastic solid mechanics. This adapter can work either as 2D or 3D.
---

[deal.II](https://www.dealii.org/) is an open source software library supporting the creation of finite element codes. It uses state-of-the-art programming techniques to offer a modern interface to the complex data structures and algorithms required.

Build status: <a style="text-decoration: none" href="https://travis-ci.org/precice/dealii-adapter" target="_blank"><img src="https://travis-ci.org/precice/dealii-adapter.svg?branch=master" alt="Build status">
</a> 

#### Tutorials:
  * [FSI with OpenFOAM and deal.II](https://github.com/precice/precice/wiki/Tutorial-for-FSI-with-deal.II-and-OpenFOAM) 
  * [Build your own adapter](https://github.com/precice/dealii-adapter/wiki/Build-your-own-adapter)
  * and [more](https://github.com/precice/dealii-adapter/wiki)

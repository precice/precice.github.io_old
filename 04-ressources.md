---
layout: default
title: Ressources
permalink: /ressources/
---

## Downloads
The source is available via our [GitHub repository](https://github.com/precice/precice). Development takes place in the ```develop``` branch. You can download the source using git:

    git clone -b develop git@github.com:precice/precice.git

## Documentation & Support
The [Wiki](https://github.com/precice/precice/wiki) contains generell information, e.g. about building, parallization, coding conventions, ...

[Source Code documentation](https://ipvs.informatik.uni-stuttgart.de/sgs/precice/doc/) is auto-generated for some branches from time to time.

For asking questions there is a [mailing list](https://mailman.informatik.uni-stuttgart.de/mailman/listinfo/precice), you should subscribe when using preCICE.

## Tutorial
There is a tutorial that uses a simple one-dimensional example case. It can be [found in the Wiki](https://github.com/precice/precice/wiki/1D-Example).

The tutorial explains the basic concepts of using PreCICE to couple two functionally independent solvers to compute the solution to a fluid-structure interaction problem. The test case is a simple one-dimensional flow through a deformable artery.

## Associated Projects

There are a number of projects that are associated of preCICE though they are not part of the core and not necessary of compilation and executing.

### fem-shell
fem-shell is a finite-element code using shell elements. It is coupled with preCICE and was developed by Stephan Herb as part of his master thesis. See [https://github.com/precice/fem-shell](https://github.com/precice/fem-shell).

### efd
Eulerian finite difference (EFD) fluid solver, which is coupled to preCICE. This solver is still in alpha testing. It is a fork of [WscriChy/navier-stokes-equations-for-fluid-structure-interaction](https://bitbucket.org/WscriChy/navier-stokes-equations-for-fluid-structure-interaction/src). See [https://github.com/precice/efd](https://github.com/precice/efd).

---
layout: default
title:
permalink: /
---

[![Build Status](https://travis-ci.org/precice/precice.svg?branch=develop)](https://travis-ci.org/precice/precice)

# Welcome to preCICE
preCICE (Precise Code Interaction Coupling Environment) is a coupling tool for partitioned simulations of multi-physics scenarios. Partitioned means, that preCICE couples existing programs, capable of simulating a subpart of the complete physics involved in the complete simulation. This allows for a high flexibility, needed to keep a decent time-to-solution for complex multi-physics scenarios (e.g. fluid-structure-acoustics interactions). The conceptual ideas of preCICE are not completely new, preCICE is basically an advancement of FSI*ce which has been developed by Markus Brenk. preCICE offers a high-level programming environment for all basic tasks appearing in the development of partitioned coupling simulation tools, encompassing communication, data mapping, and transient coupling schemes. We are currently working on an efficient parallelization of preCICE for massively parallel systems.

preCICE is Open Source Software and available on [GitHub](https://github.com/precice/precice). It is developed as part of the [SPPEXA ExaFSA](https://ipvs.informatik.uni-stuttgart.de/SGS/EXAFSA/index.php) Project.
To reference preCICE please cite "Gatzhammer, Efficient and Flexible Partitioned Simulation of Fluid-Structure Interactions, PhD Thesis, Institut für Informatik, Technische Universität München, 2015" or "Bungartz et al., preCICE -- A Fully Parallel Library for Multi-Physics Surface Coupling, submitted to Computers and Fluids., Elsevier, 2015."



## Features

### Steering
+ Minimal invasive high-level API in C, C++, Fortran90/95, and Fortran2003
+ Parallel or sequential coupling between 2 or more coupling participants, configurable at run-time
+ Timestep size can be set by either participant or by preCICE
+ Subcycling

### Communication
+ Fully parallel point-to-point communication based on either TCP/IP or MPI ports

### Data Mapping
+ Projection-based mapping: nearest neighbor or nearest projection
+ Black-box mapping based on radial-basis functions

### Fix-Point Acceleration
+ Static or dynamic (Aitken) underrelaxation
+ Anderson or generalized Broyden acceleration techniques (also known as interface quasi-Newton schemes) extrapolation in time

### Other Features
+ Geometry interface for fixed-grid solvers, import via STL
+ Python action interface to modify coupling data at run-time
+ Restart mechanism for coupling schemes
+ Coupling mesh export to VTK
+ Automatic XML reference generation
+ Open Source using the LGPL3 license



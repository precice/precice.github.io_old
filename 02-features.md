---
layout: default
title: Features
permalink: /features/
---

# Features

### General
+ preCICE is cross-plattform. While we mostly test on Linux, preCICE has also been succesfully used on Windows and macOS.
+ Scalability for most features has been shown up to 10,000 cores.

### Steering
+ Minimally-invasive, high-level API in C, C++, Fortran 90/95, Fortran 2003, and Python
+ Parallel or sequential coupling between 2 or more coupling participants, configurable at run-time
+ Timestep size can be set by either participant or by preCICE.
+ Subcycling

### Communication
+ Fully parallel point-to-point communication, no central instance
+ Based on either TCP/IP or MPI ports.

### Data Mapping
+ Projection-based mapping: nearest neighbor or nearest projection
+ Black-box mapping based on radial-basis functions
+ All data mappings either in a consistent or in a conservative variant

### Fix-Point Acceleration
+ Static or dynamic (Aitken) underrelaxation
+ Anderson or generalized Broyden acceleration techniques (also known as interface quasi-Newton schemes)
+ Extrapolation in time

### Other Features
+ Geometry interface for fixed-grid solvers, import via STL
+ Python action interface to modify coupling data at run-time
+ Restart mechanism for coupling schemes
+ Coupling mesh export to VTK
+ Automatic XML reference generation

### Missing a feature?
We describe our plans for the future in our [Roadmap](https://github.com/precice/precice/wiki/Roadmap). If you don't see what you need there, [let us know](../resources/#contact)!

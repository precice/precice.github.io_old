---
layout: default
title: Features
permalink: /codes/
---

# Features

### General
+ preCICE is cross-plattform. While we mostly test on Linux, preCICE has also been succesfully used on Windowns and MAC
+ Scalability for most features has been shown up to 10,000 cores

### Steering
+ Minimally-invasive high-level API in C, C++, Fortran90/95, Fortran2003, and Python
+ Parallel or sequential coupling between 2 or more coupling participants, configurable at run-time
+ Timestep size can be set by either participant or by preCICE
+ Subcycling

### Communication
+ Fully parallel point-to-point communication, no central instance
+ Based on either TCP/IP or MPI ports

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


## Coupled Codes

There are various codes - free and proprietary ones - currently coupled with preCICE. If you want to add your code here, please let us know. 

[Ateles (APES)](http://www.mb.uni-siegen.de/sts/departmentmainmenu_de/software/?lang=de) |	Compressible Flow and Acoustics	| in-house (Universität Siegen) | in-house adapter
[Alya System](http://www.bsc.es/computer-applications/alya-system) |	Incompressible Flow and Structure | in-house (Barcelona Supercomputing Center) | in-house adapter
[CalculiX](http://www.calculix.de/) |	Structure | open-source | [official adapter](https://github.com/precice/calculix-adapter)
[Carat++](http://carat.st.bv.tum.de/) |	Structure | in-house (STATIK, Technical University of Munich) | in-house adapter
[Code_Aster](http://www.code-aster.org) |	Structure | open-source | [official adapter](https://github.com/precice/code_aster-adapter)
[COMSOL](http://www.comsol.com/) | Structure | commercial | [official adapter](https://github.com/precice/comsol-adapter)
[EFD](https://github.com/precice/efd) | Incompressible Flow | open-source (SCCS, Technical University of Munich) | built-in adapter
[FASTEST](http://www.fnb.tu-darmstadt.de/forschung_fnb/software_fnb/software_fnb.en.jsp) | Incompressible Flow | in-house (TU Darmstadt) | in-house adapter 
[FEAP](http://www.ce.berkeley.edu/projects/feap/)| Structure | commercial | in-house adapter at TU Darmstadt 
[Fluent](http://www.ansys.com/Products/Simulation+Technology/Fluid+Dynamics/Fluid+Dynamics+Products/ANSYS+Fluent) | Incompressible Flow | commercial | [official adapter](https://github.com/precice/fluent-adapter)
[OpenFOAM](http://www.openfoam.com/) |Compressible Flow, Incompressible Flow, and Structure | open-source | [third-party-adapter](https://github.com/davidsblom/FOAM-FSI), official adapter under development
[Peano](http://www5.in.tum.de/peano/releases/index.html) | Incompressible Flow | in-house (SCCS, Technical University of Munich) | in-house adapter
[SU2](http://su2.stanford.edu/) | Compressible Flow | open-source | [official adapter](https://github.com/precice/su2-adapter)

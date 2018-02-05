---
layout: default
title:
permalink: /
---


# Welcome to <img src="../assets/precice.png" height="60px" style="margin-bottom: -16px;">

<p id="latest-release">
    <!-- This will be replaced by the handleResponse() when the page is loaded -->
    <strong>News:</strong> (looking for the <a href="https://github.com/precice/precice/releases/latest">latest release on GitHub</a>...)
</p>

preCICE (Precise Code Interaction Coupling Environment) is a coupling library for partitioned multi-physics simulations, including, but not restricted to fluid-structure interaction and conjugate heat transfer simulations. Partitioned means that preCICE couples existing programs (solvers) capable of simulating a subpart of the complete physics involved in a simulation. This allows for the high flexibility that is needed to keep a decent time-to-solution for complex multi-physics scenarios.

The software offers methods for transient equation coupling, communication means, and data mapping schemes. [Ready-to-use adapters](codes) for well-known commercial and open-source solvers, such as OpenFOAM, SU2, or CalculiX, are available. Adapters for in-house codes can be implemented and validated in only a few weeks.

preCICE is an open-source software under the LGPL3 license and available on [GitHub](https://github.com/precice/precice).

<div align="center" style="margin-bottom:10px">
<img src="../assets/plugandplay.png" style="max-height: 100%; max-width: 100%">
</div>

## Unique Features

In contrast to other coupling software, preCICE is prepared for the next generation of multi-physics simulations thanks to the following features:

+ **Fully parallel peer-to-peer concept:** Coupled solvers directly communicate with each other without requiring a central instance. All coupling operations are executed directly on the solvers' compute resources. This enables massively parallel simulations without the coupling being the bottleneck of the overall simulation.

+ **Pure library approach:** In contrast to a framework approach, the solvers call preCICE instead of being called by the framework. This makes coupling minimally-invasive and thus easy to set up and to maintain. The preCICE API operates on a generic level, allowing highest flexibility and the implementation of new adapters in as little as approximately 30 lines of code.

+ **Sophisticated and robust quasi-Newton coupling algorithms:** They enable the partitioned realization of strongly-coupled problems, such as those  observed in hemodynamic applications.

+ **Multi coupling:** preCICE allows the robust coupling of an arbitrary number of solvers to one overall simulation.

## To cite preCICE, please use:  
> H.-J. Bungartz, F. Lindner, B. Gatzhammer, M. Mehl, K. Scheufele, A. Shukaev, and B. Uekermann: preCICE - A Fully Parallel Library for Multi-Physics Surface Coupling. *Computers and Fluids*, [Elsevier](http://www.sciencedirect.com/science/article/pii/S0045793016300974), **141**, 250--258, 2016. [bibtex](https://www5.in.tum.de/cgi-bin/publikationen/bibtex.py?pubid=2434)

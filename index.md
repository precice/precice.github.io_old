---
layout: default
title: "Home"
permalink: /
---


# Welcome to <img src="../assets/precice.png" alt="preCICE">

<p id="latest-release">
    <!-- This will be replaced by the handleResponse() when the page is loaded -->
    <strong>News:</strong> (looking for the <a href="https://github.com/precice/precice/releases/latest">latest release on GitHub</a>...)
</p>

**preCICE Workshop 2020**: Early registration extended until November 29. [Read more...](preCICE2020/)

**preCICE in xSDK**: preCICE is now part of the [xSDK](https://xsdk.info/packages/) framework. [Read the compatibility policies...](https://github.com/xsdk-project/xsdk-policy-compatibility/blob/master/precice-policy-compatibility.md)

**Give us your feedback**: [please use this form](https://precice.typeform.com/to/IeiyKF), it's important for us!

preCICE (Precise Code Interaction Coupling Environment) is a coupling library for partitioned multi-physics simulations, including, but not restricted to fluid-structure interaction and conjugate heat transfer simulations. Partitioned means that preCICE couples existing programs (solvers) capable of simulating a subpart of the complete physics involved in a simulation. This allows for the high flexibility that is needed to keep a decent time-to-solution for complex multi-physics scenarios. preCICE runs efficiently on a wide spectrum of systems, from low-end workstations up to complete compute clusters and has proven scalability on 10000s of MPI Ranks.

The software offers methods for transient equation coupling, communication means, and data mapping schemes. preCICE is written in C++ and offers bindings for C, Fortran, Matlab, and Python. [Ready-to-use adapters](codes) for well-known commercial and open-source solvers, such as OpenFOAM, deal.II, FEniCS, SU2, or CalculiX, are available. Due to the minimally-invasive approach of preCICE, adapters for in-house codes can be implemented and validated in only a few weeks.

preCICE is an open-source software under the LGPL3 license and available on [GitHub](https://github.com/precice/precice).

<figure class="text-center">
  <img src="../assets/precice_overview.png">
</figure>

## Unique Features

In contrast to other coupling software, preCICE is prepared for the next generation of multi-physics simulations thanks to the following features:

+ **Fully parallel peer-to-peer concept:** Coupled solvers directly communicate with each other without requiring a central instance. All coupling operations are executed directly on the solvers' compute resources. This enables massively parallel simulations without the coupling being the bottleneck of the overall simulation.

+ **Pure library approach:** In contrast to a framework approach, the solvers call preCICE instead of being called by the framework. This makes coupling minimally-invasive and thus easy to set up and to maintain. The preCICE API operates on a generic level, allowing highest flexibility and the implementation of new adapters in as little as approximately 30 lines of code.

+ **Sophisticated and robust quasi-Newton coupling algorithms:** They enable the partitioned realization of strongly-coupled problems, such as those  observed in hemodynamic applications.

+ **Multi coupling:** preCICE allows the robust coupling of an arbitrary number of solvers to one overall simulation.

Download overview slides: [preCICE_Slides.pdf](https://github.com/precice/precice.github.io/tree/master/material/slides/preCICE_Slides.pdf) 

## To cite preCICE, please use:  
<div class="publications">
<article class="publication">
  <header>
    <a href="http://www.sciencedirect.com/science/article/pii/S0045793016300974">preCICE -- A Fully Parallel Library for Multi-Physics Surface Coupling</a>
  </header>
  <section>
    <span class="authors">Hans-Joachim Bungartz, Bernhard Gatzhammer, Florian Lindner, Miriam Mehl, Klaudius Scheufele, Alexander Shukaev, Benjamin Uekermann</span>,
    <span class="year">2016</span>
    <p>In Computers and Fluids, Volume 141, p. 250––258. Elsevier.</p>
  </section>
  <footer>
    <a class="button" href="../assets/precice.bib">BibTeX</a>
  </footer>
</article>
</div>

---
layout: default
title: FAQ
permalink: /faq/
---

# Frequently Asked Questions

## How do I start a coupled simulation with preCICE?

In order to start a coupled simulation, you can execute the (adapted)
participants normally, as you would execute them for a non-coupled simulation.
"Adapted" means either that the solver is modified to call the preCICE library,
or that it loads a separate "preCICE adapter" at runtime. Often it is helpful
to just start the simulations in different terminals.

Please note that that the solvers call preCICE (as it is a library) and not the
opposite. There is no "preCICE executable" required to start the simulation.

## Is there any separate mesh defined for the coupling?

No. The user specifies one of the participants' meshes to be used for the coupling.

The interface meshes are given names in the preCICE configuration file and each adapter
specifies the locations of each node that lies on its side of the interface.

## How does preCICE treat non-conforming meshes?

preCICE supports several methods to map the interface values from the one mesh
to the other. The simplest method uses the nearest-neighbor's value, while
more advanced methods like the nearest-projection mapping or the Radial-Basis
Function mapping include contributions from neighboring nodes.

## Does partitioned coupling introduce error?

Partitioned coupling can indeed lead to errors such as the Added-Mass Effect. However, preCICE provides implicit coupling algorithms to treat the error introduced.

## Does preCICE use files for the communication?

No. Using files would be very slow. The preCICE participants communicate either
through TCP/IP sockets or through MPI ports.

Additionally, any processes that need to communicate, do so directly (Peer-to-Peer),
without needing to go through any central instance ("server").

## Can the individual solvers run on two different platforms on two different machines in/out of a network?

Yes, at least as long as communication over TCP/IP is possible. The solvers find each other using a network address, which is written in a file and read once in the beginning of the simulation. For this reason, all solvers need to be able to at least access a common file system.

## Can preCICE couple more than two participants?

Yes! [Here is an example](https://github.com/precice/precice/wiki/Tutorial-for-CHT-with-OpenFOAM-and-CalculiX).

## Can preCICE be used for volume coupling?

Yes, but it will be computationally expensive. preCICE is mainly designed to
couple simulations that share a common surface boundary. In this case, all the
coupled volume nodes should be specified in the coupling mesh.

preCICE only knows about points and their connectivity, so it doesn't make much of a difference if the points are on a surface or on a volume. However, in the case of volume coupling, nearest-projection mapping would not be available. You may still use the nearest-neighbor or RBF mapping, however.

## Can preCICE be used for one-way coupling?

Yes! Several people are doing this already.

Even though there may be simpler ways to do one-way coupling, it may still be beneficial to use preCICE here: flexible data mapping methods and parallel communication (your coupling data might be too large to write to disk).

## Can preCICE be used with adaptive meshes?

Or: "Is it correct that preCICE cannot support couplings when the interface mesh is changing its connectivity during the simulation?"

Currently, the mapping setup only occurs once during the initialization of preCICE. Thus, in order to modify the mapping one must restart the simulation. It depends on a case-by-case basis whether this costly method is acceptable or not.
A dissertation in progress studies this issue and preCICE will have such a feature in the future.

## Which code drives the coupled simulation in preCICE?
Or: "Which code is executing the coupling iterations given that preCICE does not really have a centralized engine to orchestrate the simulation?"

It is the preCICE library! Every participant loads the library and works on its own part of the mesh. Of course, there needs to be some cooperation between the different processes, but this does not need to be blocking or through a central process. If you want to know more details about the implementation of specific features, you may look into our [literature guide](https://github.com/precice/precice/wiki/Literature-guide), in particular in the dissertation of Benjamin Uekermann. And of course, the code is open!

## Where can I find more details for the methods involved?

Have a look into our [literature guide](https://github.com/precice/precice/wiki/Literature-guide).

## What are the advantages of preCICE in comparison to other coupling software?

Such a list would be difficult to maintain, however you can have a look at the
introductory section of our [reference paper](../publications).

When comparing preCICE to other software, look for the following key points:

Library approach
: preCICE is _not_ a framework which is used to call the
participating solvers, but a library which the solvers call.
This allows for great flexibility: you can easily make
your own in-house solvers use the preCICE library and you can allocate different
computational resources for each participant, using the same tools that you
may already use.

Performance
: preCICE is designed especially for massively parallel simulations.
For this reason, each process of each participant communicates directly with
any other processes of other participants, without passing through a
central bottleneck. Additionally, all the communication happens using either
the network TCP/IP sockets or MPI ports, methods much faster than exchanging
files through the filesystem. Last but not least, advanced numerical methods
can accelerate the coupling already in the algorithmic level.

Coupling algorithms
: preCICE supports fully implicit (strong) coupling,
accelerated by sophisticated and robust quasi-Newton algorithms. These stabilize
and accelerate the solution.

Data mapping techniques
: preCICE offers several first and second order
methods to map the interface values between non-matching meshes,
including Radial-Basis Functions.

Multi-coupling
: preCICE can easily be used to couple more than two simulations.

License
: preCICE is free software, distributed under the GNU LGPL3 license
and actively maintained on [GitHub](https://github.com/precice/). Of course, as
with any free software, the documentation of a commercial alternative may be
more extended. However, we constantly improve our [documentation](https://github.com/precice/precice/wiki), based on the
feedback we get from preCICE users.

## How is preCICE funded?

preCICE is orginally an academic software. We have received public funding from several projects that use and develop preCICE. This applies currently, e.g., to the DFG-funded [ExaFSA project](http://ipvs.informatik.uni-stuttgart.de/SGS/EXAFSA/index.php), part of [SPPEXA](http://www.sppexa.de/). Recently, DFG had also a specific call on [research software sustainability](http://www.dfg.de/en/research_funding/programmes/infrastructure/lis/funding_opportunities/call_proposal_software), in which we were succesful: The project preDOM should take preCICE to the next level, from a prototype to a wide-spread sustainable scientific software. Specific funding for basic un-academic things such as tutorials, outreach, or documentation has been granted. Besides this public funding, both active academic developer groups, [SCCS](https://www5.in.tum.de/wiki/index.php/Home) at the Technical University of Munich and [SGS](https://www.ipvs.uni-stuttgart.de/abteilungen/sgs) at the University of Stuttgart, also invest own internal funding.  

Since 2017, the spin-off [COPLON](http://coplon.de/) provides support, training, and software solutions for industrials users of preCICE. 

Last, as any open-source project, preCICE could only survive through its user's and developer's  passionate commitment also in their after-work hours.       

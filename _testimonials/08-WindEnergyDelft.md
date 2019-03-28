---
title: "Fluid-Structure Interaction of Inflatable Wing Sections"
authors: "<a href=\"https://www.tudelft.nl/staff/m.a.m.folkersma/\">Mikko Folkersma</a>, Wind Energy, Faculty of Aerospace Engineering, TU Delft, The Netherlands"
img-url: ../assets/testimonial_windenergy.png
---
Airborne wind energy is a novel renewable energy technology using tethered wings to harness wind energy at higher altitudes and with less material. At TU Delft, we are investigating the aerodynamics of inflatable membrane wings which are highly flexible and therefore exhibit a strong coupling between fluid and structure. In our fluid-structure interaction (FSI) simulation framework, we use OpenFOAM to calculate the aerodynamic load distribution on the wing and mem4py or, alternatively, MBDyn to calculate the structural deformation. We use preCICE to couple the solvers and implemented the preCICE adapters in Python for mem4py and MBDyn. Thanks to preCICE, we achieved accurate, stable and efficient fluid-structure coupling with a small piece of code (less than 100 lines).

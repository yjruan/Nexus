# Nexus
A program for analyzing properties of polymer systems.
This program is designed to analyze instantaneous configurations generated from LAMMPS simulations. 
It provides tools for characterizing polymer systems, including entanglement analysis (FT-PPA), structural analysis (radius of gyration, chain orientation etc.), as well as several additional utilities for post-processing simulation data.

FT-PPA is an analysis of primitive paths for entangled polymers based on combining energy minimization with the Frenet trihedron
geometric analysis. More details about this method can be found in Macromolecules 2024, 57, 2792.

## Features Overview

- [1. FT-PPA: Entanglement Analysis](docs/FT-PPA.md)
  - [1.1 Entanglement statistics](docs/FT-PPA_Stat.md)
  - [1.2 Entanglement visualization](docs/FT-PPA_Dump.md)
- [Property: Chain Analysis]
  - [2.1 Radius of Gyration]
  - [2.2 End-to-End Distance]

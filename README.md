# Nexus
## Preface
A program for analyzing properties of polymer systems.
The program uses modern Fortran standards (2003 or later) with modules, and is designed to analyze instantaneous configurations generated from LAMMPS simulations.

The current version can process orthogonal, monoclinic, and triclinic simulation boxes. 
These box types correspond to equilibrium simulations, shear simulations using the `fix deform` command, and uniaxial extensional simulations using the `fix nvt/uef` command in LAMMPS, respectively.
It provides tools for characterizing polymer systems, including entanglement analysis (FT-PPA), structural analysis (radius of gyration, chain orientation etc.), tube theory calculation, as well as several additional utilities for post-processing simulation data.


**FT-PPA** is an important module of this program.
FT-PPA is an analysis of primitive paths for entangled polymers based on combining energy minimization with the Frenet trihedron
geometric analysis. 
More details about this method can be found in Macromolecules 2024, 57, 2792.

However, I have no time to add all **Error** or **WARNING** message in program.
Users are welcome to try this program and provide feedback. 
Any comments or suggestions will be greatly appreciated, and the program will be continuously improved in future updates.
If possible, please cite Macromolecules 2024, 57, 2792.



## Features Overview
- [1. FT-PPA: Entanglement Analysis](docs/FT-PPA.md)
  - [1.1 Statistics](docs/FT-PPA_Stat.md)
  - [1.2 Visualization](docs/FT-PPA_Dump.md)
- [2. Property: Chain Analysis]
  - [2.1 Radius of Gyration]
  - [2.2 End-to-End Distance]

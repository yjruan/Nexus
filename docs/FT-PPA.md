# `FTPPA` Styles

## Description
This module performs the `FT-PPA` algorithm to analyze the primitive paths of polymer chains and calculate entanglement properties. 
More details about this method can be found in Ref [1](https://doi.org/10.1021/acs.macromol.3c02054). This method consists of two steps: 1) obtaining a smooth primitive path; 2) conducting primitive path analysis using the Frenet trihedron.
Briefly, FT-PPA identifies local high-curvature segments, termed kinks, along the primitive chain path. 
An entanglement (Ent) is then assigned when two kinks are spatially close and exhibit opposite curvature directions.
At the current stage, FTPPA only processes energy minimization configurations of Kremer–Grest model.<sup>2</sup>
Users need to prepare and provide these configurations as input files.


The FTPPA styles include two main commands: 
- the [`FTPPA Stat`](FT-PPA_Stat.md), statistical properties of entanglements

- the [`FTPPA Dump`](FT-PPA_Dump.md), visualization conformations of entanglements.



 <!-- or *KMax* or *Del* or *Diff* or *Angle* or *Dis* or *Ori*
    - *format* values = data, dump, cfg
    - *NC*  values = chain length
    - *extend* values = value
    - *KMax* values = threshold curvature
    - *Del* values =
    - *Diff* values = threshold between contour length and end-to-end length
    - *Angle* values = 
    - *Dis* values = 
    - *Ori* values = -->




## References

[1] Ruan, Y.; Lu, Y.; An, L.; Wang, Z.-G. *Macromolecules* **2024**, *57(6)*, 2792–2800. https://doi.org/10.1021/acs.macromol.3c02054

[2] Sukumaran, S. K.; Grest, G. S.; Kremer, K.; Everaers, R. *J. Polym. Sci. B: Polym. Phys.* **2005**, *43(8)*, 917–933. https://doi.org/10.1002/polb.20384
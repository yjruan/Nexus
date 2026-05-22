# `FTPPA Dump` command

## Syntax

`FTPPA Dump filename Keyword value Args`

- filename = file name

- Keyword = *AInfo* or *TChain* or *TAtom* or *TwoChain*
     
    - *AInfo*  values = none
     
    - *TChain* values = mol_ID
    
    - *TAtom*   values = mol_ID Astart Astop r_cut

    - *TwoChain* values = mol_ID1, mol_ID2, mol_ID3...

- Args = *format* or *NC* or *extend* or *CenMove*
    - *format* values = data, dump, cfg
    - *NC*    values = chain length
    - *extend* values = value
    - *CenMove* values = none

## Examples
```text
FTPPA Dump -h
FTPPA Dump AInfo NC 300
FTPPA Dump dump.PPA_0 TChain 1
FTPPA Dump dump.PPA_0 TAtom  1 94 99 1.11246  NC 300
FTPPA Dump dump.PPA_* TwoChain 1 471
```
## Description

The `FTPPA Dump` command performs FT-PPA analysis on primitive chain conformations and outputs entanglement-related configurations.
This command dumps molecular information in the LAMMPS data format (`full` style), which can be used for visualization and further analysis.
Such files can be recognized by visualization software such as OVITO, making it convenient for users to analyze entanglement configurations.

---

`filename` is name of the input coordinate file to be processed. 
If the `filename` does not end with the wildcard character, the command processes only this file. 
If the filename ends with `*`, the command processes all matching files. 
For wildcard processing, the matched filenames must end with non-zero-padded numerical indices, such as `0`, `1`, `2`, ..., instead of `01`, `02`, ...
For example, `dump.PPA_*` can match files such as:
`dump.PPA_0`, `dump.PPA_1`, `dump.PPA_2`, but not filenames with zero-padded indices such as: `dump.PPA_01`, `dump.PPA_02`.

---
`AInfo` outputs the atom ID, molecular ID, atom type, curvature value, and the `x`, `y`, and `z` coordinates of each monomer.
The output file is written in the LAMMPS `full` data format. 
In this file, the `charge` field is used to represent the curvature value. 
Atom type `1` represents a monomer that does not form a kink, while atom type `2` represents a monomer belonging to a kink segment.

---
`TChain` outputs the configuration of chain *mol_ID* together with the entangled segments from other chains.
The output file is written in the LAMMPS `full` data format. 
In this file, the `charge` field is used to represent the curvature value. 
Atom types `1` and `2` represent non-kink and kink monomers in chain *mol_ID*, respectively. 
Atom type `3` represents an entangled segment from another chain. 
If the *extend* argument is not `0`, the entangled segment is further extended by the specified number of monomers, and these additional monomers are assigned atom type `4`.
The output file can be loaded into visualization software such as OVITO, allowing users to conveniently identify which polymer chains are entangled with chain *mol_ID*.

---
`TwoChain` outputs the configurations of multiple selected chains, such as *mol_ID1*, *mol_ID2*, and so on. 
The output file is written in the LAMMPS `full` data format, where the `charge` field represents the curvature value. 
Atom types are assigned sequentially: types `1` and `2` represent non-kink and kink monomers in chain *mol_ID1*, types `3` and `4` represent non-kink and kink monomers in chain *mol_ID2*, and so forth. 
The file can be loaded into visualization software such as OVITO to inspect the spatial relationships among multiple polymer chains.

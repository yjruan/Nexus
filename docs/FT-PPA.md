This module performs the `FT-PPA` algorithm to analyze the primitive paths of polymer chains and calculate entanglement properties. 
Depending on the selected options, it can output the number of entanglements, the entanglement distribution, and the spatial positions of entanglement points.

# `FTPPA Dump` command

## Syntax


`FTPPA Dump filename Keyword value Args`

- filename = file name
- one or more keyword/value pairs may be appended
 
  Keyword = AInfo/TChain/TAtom/TwoChain

    TChain values = mol_ID
    
    TAtom  values = mol_ID atom_ID r_cut

## Examples
```text
A
```
## Description

AInfo     : Dump \kappa and x,y,z of all monomer'&

TChain    : Dump Target chain, and around kinks'&

TAtom     : Dump Targer Atom, and around monomers'&

TwoChain  : Dump two or more chains',&
This module performs the `FT-PPA` algorithm to analyze the primitive paths of polymer chains and calculate entanglement properties. 
Depending on the selected options, it can output the number of entanglements, the entanglement distribution, and the spatial positions of entanglement points.

# `FTPPA Dump` command

## Syntax


`FTPPA Dump filename Keyword value Args`

- filename = file name

- Keyword = *AInfo* or *TChain* or *TAtom* or *TwoChain*
     
    - *AInfo*  values = none
     
    - *TChain* values = mol_ID
    
    - *TAtom*   values = mol_ID Astart Astop r_cut

    - *TwoChain* values = mol_ID1, mol_ID2, mol_ID3

- Args = *NC* or *extend* or *format*
    - *NC*  values = chain length
    - *extend* values = mol_ID
    - *format* values = data, dump, cfg
## Examples
```text
FTPPA Dump -h
FTPPA Dump AInfo NC 300
FTPPA Dump dump.PPA_0 TChain 1
FTPPA Dump dump.PPA_0 TAtom  1 94 99 1.11246  NC 300
FTPPA Dump dump.PPA_* TwoChain 1 471
```
## Description

AInfo     : Dump \kappa and x,y,z of all monomer'&

TChain    : Dump Target chain, and around kinks'&

TAtom     : Dump Targer Atom, and around monomers'&

TwoChain  : Dump two or more chains',&
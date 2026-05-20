This module performs the `FT-PPA` algorithm to analyze the primitive paths of polymer chains and calculate entanglement properties. 
Depending on the selected options, it can output the number of entanglements, the entanglement distribution, and the spatial positions of entanglement points.

# `FTPPA Dump` command

## Syntax


`FTPPA Dump filename Keyword value Args`

- filename = file name
- one or more keyword/value pairs may be appended

<div style="background-color:#f6f8fa; padding:12px; border:1px solid #d0d7de;">
keyword = AInfo/TChain/TAtom/TwoChain
</div>


## Examples
```text
A
```
## Description

AInfo     : Dump \kappa and x,y,z of all monomer'&

TChain    : Dump Target chain, and around kinks'&

TAtom     : Dump Targer Atom, and around monomers'&

TwoChain  : Dump two or more chains',&
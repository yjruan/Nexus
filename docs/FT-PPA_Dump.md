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

Doing...
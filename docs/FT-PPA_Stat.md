# `FTPPA Stat` command

## Syntax

`FTPPA Dump filename Keyword Args`

- filename = file name

- Keyword = *EnNum* or *EnPos* or *EnDis* or *EnID*
     
    - *EnNum* = Kink Number and Ent Number per chain
     
    - *EnPos* = Ent wrapped position (center of two kinks) in space
    
    - *EnDis* = Ent Distribution along target direction

    - *EnID*  = Atom IDs of the two entangled chain segments

- Args = *format* or *NC*

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
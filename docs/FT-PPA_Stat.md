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
FTPPA Stat dump.PPA_0 EnNum NC  300"
FTPPA Stat dump.PPA_* EnPos
```
## Description

Doing...
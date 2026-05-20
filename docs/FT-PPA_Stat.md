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
    - *format* values = data, dump, cfg
    - *NC*    values = chain length

## Examples
```text
FTPPA Stat dump.PPA_0 EnNum NC  300"
FTPPA Stat dump.PPA_* EnPos
```
## Description
The `FTPPA Stat` command performs FT-PPA on primitive chain conformations and outputs statistical information of entanglements, such as the entanglement number per chain and the spatial distribution of entanglement.
Since primitive paths (PPs) cannot pass through each other, sharp bends, that is, kinks, naturally occur at the points where two PPs come into contact. 
Therefore, a PP can be seen as a sequence of straight segments connected by these sharp kinks. 
An entanglement is associated with a pair of kinks which arise due to the topological constraint.




`filename` is name of the input coordinate file to be processed. 
If the `filename` does not end with the wildcard character, the command processes only this file. 
If the filename ends with `*`, the command processes all matching files. 
For wildcard processing, the matched filenames must end with non-zero-padded numerical indices, such as `0`, `1`, `2`, ..., instead of `01`, `02`, ...
For example, `dump.PPA_*` can match files such as:
`dump.PPA_0`, `dump.PPA_1`, `dump.PPA_2`, but not filenames with zero-padded indices such as: `dump.PPA_01`, `dump.PPA_02`.

`EnNum` will output the kink number per chain and entanglement number per chain to a file named `EnNum.DAT`.
An entanglement is associated with a pair of kinks, 
Note that an entanglement is generally defined by a pair of kinks. However,
due to the multiple chain entanglements, one kink may be paired with two different kinks, and thus contribute to two entanglements. 
As a result, the kink number per chain and the entanglement number per chain are not identical.

`EnPos` will output the wrapped position of all entanglements, defined as the centers of mass of the corresponding kink pairs, to a file named `EnPos.DAT`.
Users can further analyze the spatial distribution of entanglements using their own post-processing scripts.





## Default
format = dump, NC = 0
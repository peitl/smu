# smu
A collection of *saturated minimally unsatisfiable* (SMU) formulas with up to 10 clauses, split into *singular* (SSMU) formulas (which contain a singular variable) and *regular* (RSMU) formulas (which contain no singular variables).

The file `genf.c` is a modification of `genbg.c` provided by Brendan McKay to generate these formulas.
A modified makefile for Nauty to include `genf` in the compilation is provided.
If the makefile doesn't work, try compiling with something like (after having compiled Nauty)

```
gcc -o genf -O4 -march=native -DMAXN=WORDSIZE -DWORDSIZE=32 genf.c gtoolsW.o schreierW.o nautyW1.o nautilW1.o naugraphW1.o naurng.o
```

`genf.c` was created for Nauty 2.7r1.

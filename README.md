# Co-Ni-Ru

## Foreword

The purpose of this project is to calculate the basic structural parameters (including lattice parameter and elastic constants), generalized stacking fault energies (GSFE), and local slip resistances (LSR) in three alloy systems that consist of equal or non-equal molar Co, Ni, and Ru.

The effect of chemical short-range order (CSRO) will be considered. One scientific question: Is the CSRO the same, or similar, in alloys containing the same elements but different concentrations?

## LAMMPS

Following [another project](https://github.com/shuozhixu/Modelling_2024), we can build LAMMPS with MANYBODY, EXTRA-COMPUTE, and MC packages and submit jobs on [OSCER](http://www.ou.edu/oscer.html).

Six universal machine learning-based interatomic potentials will be applied: MACE, CHGNet, DeepMD, SevenNet, M3GNet, MEGNet. Most of them can be found on either [Matbench Discovery](https://matbench-discovery.materialsproject.org) or [Materials Graph Library](https://matbench-discovery.materialsproject.org).

## CoNiRu

Build the random structure in an FCC lattice. Calculate the lattice parameter, elastic constants, and GSFE at 0 K. Compare results with [DFT](http://dx.doi.org/10.1088/1361-651X/ab3b62).

## Co<sub>2</sub>Ni<sub>2</sub>Ru

It has an FCC lattice, according to [this paper](https://doi.org/10.1016/j.actamat.2020.05.003).

Build the random and CSRO structures annealed at 300 K. Calculate the lattice parameters and elastic constants of both structures at 0 K and 300 K, following [a previous GitHub repository](https://github.com/shuozhixu/Modelling_2024).

Calculate the [GSFE](https://github.com/shuozhixu/FLAM2020-GSFE) and [LSR](https://github.com/shuozhixu/FLAM2020-LSR) in both random and CSRO structures at 0 K, following [this paper](http://dx.doi.org/10.1016/j.ijplas.2021.103157).

Note: unpublished DFT calculations show that, _a_<sub>0</sub> = 3.58 nm, effective _C_<sub>11</sub> = 401.078 GPa, effective _C_<sub>12</sub> = 168.944 GPa, effective _C_<sub>44</sub> = 148.554 GPa, and mean ISFE = -43.11 mJ/m<sup>2</sup>.

## CoNiRu<sub>2</sub>

It has an HCP lattice, according to [this paper](https://doi.org/10.1016/j.actamat.2020.05.003).

Build the random and CSRO structures annealed at 300 K. Calculate the lattice parameters and elastic constants of both structures at 0 K and 300 K.

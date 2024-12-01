# Co-Ni-Ru

## Foreword

The purpose of this project is to calculate the basic structural parameters (including lattice parameter and elastic constants), generalized stacking fault energies (GSFE), and local slip resistances (LSR) in three alloy systems that consist of equal or non-equal molar Co, Ni, and Ru. The alloys have either a face-centered cubic (FCC) or a hexagonal close-packed (HCP) lattice.

The effect of chemical short-range order (CSRO) will be considered. One scientific question: Is the CSRO the same, or similar, in alloys containing the same elements but different concentrations?

## LAMMPS

Following [another project](https://github.com/shuozhixu/Modelling_2024), we can build LAMMPS with MANYBODY, EXTRA-COMPUTE, and MC packages and submit jobs on [OSCER](http://www.ou.edu/oscer.html).

Six universal machine learning-based interatomic potentials will be applied: MACE, CHGNet, DeePMD, SevenNet, M3GNet, MEGNet. More information can be found on [Matbench Discovery](https://matbench-discovery.materialsproject.org) [Materials Graph Library](https://matbench-discovery.materialsproject.org), and [DeePMD-kit](https://github.com/deepmodeling/deepmd-kit).

## Calculations

### CSRO

The CSRO structure of an alloy can be generated following [a previous project](https://github.com/shuozhixu/CMS-EAM_2025). Here, all CSRO structures are annealed at 300 K.

### Basic structural parameters

Lattice parameter and elastic constants of an alloy at 0 K can be calculated following [a previous project](https://github.com/shuozhixu/Modelling_2024). Both random and CSRO structures are considered.

### GSFE

The GSFE curve on the {111} plane in an FCC crystal or on the basal plane in an HCP crystal can be calculated following [a previous project](https://github.com/shuozhixu/Modelling_2024).

Both random and CSRO structures are considered. In addition, 20 slip planes are considered in each structure.

### LSR

LSR of an edge dislocation or of a screw dislocation in an alloy can be calculated following [a previous project](https://github.com/shuozhixu/Metals_2025).

Both random and CSRO structures are considered. In addition, 20 LSR are calculated for each dislocation type.

## Alloys

### CoNiRu

Build the FCC structure. Compare results of basic structural parameters and GSFE with [DFT](http://dx.doi.org/10.1088/1361-651X/ab3b62).

### Co<sub>2</sub>Ni<sub>2</sub>Ru

It has an FCC lattice, according to [this paper](https://doi.org/10.1016/j.actamat.2020.05.003).

Unpublished DFT calculations show that, for random Co<sub>2</sub>Ni<sub>2</sub>Ru, _a_<sub>0</sub> = 3.58 nm, effective _C_<sub>11</sub> = 401.078 GPa, effective _C_<sub>12</sub> = 168.944 GPa, effective _C_<sub>44</sub> = 148.554 GPa, and mean ISFE = -43.11 mJ/m<sup>2</sup>.

### CoNiRu<sub>2</sub>

It has an HCP lattice, according to [this paper](https://doi.org/10.1016/j.actamat.2020.05.003).

No DFT data exist for comparison.
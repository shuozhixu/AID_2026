# Co-Ni-Ru

## Foreword

The purpose of this project is to calculate the basic structural parameters (including lattice parameter and elastic constants) and generalized stacking fault energies (GSFE) in three alloy systems that consist of equal or non-equal molar Co, Ni, and Ru. The alloys have either a single face-centered cubic (FCC) phase, a single hexagonal close-packed (HCP) phase, or an FCC/HCP biphase, according to [experiments](https://doi.org/10.1016/j.actamat.2020.05.003).

## LAMMPS

Following [another project](https://github.com/shuozhixu/Modelling_2024), we can build LAMMPS with the EXTRA-COMPUTE package and submit jobs on [OSCER](http://www.ou.edu/oscer.html).

Four universal machine learning-based interatomic potentials will be applied: SevenNet, Orb, MACE, and DeePMD. More information can be found on [Matbench Discovery](https://matbench-discovery.materialsproject.org), [Materials Graph Library](https://github.com/materialsvirtuallab/matgl), and [DeePMD-kit](https://github.com/deepmodeling/deepmd-kit).

## Calculations

Only random structures are considered in this project and can be generated using [atomsk](https://atomsk.univ-lille.fr).

### Basic structural parameters

Lattice parameter and elastic constants at 0 K and 300 K can be calculated following [a previous project](https://github.com/shuozhixu/Modelling_2024). 

### GSFE

The GSFE curve on the {111} plane in an FCC lattice or on the basal plane in an HCP lattice at 0 K can be calculated following [a previous project](https://github.com/shuozhixu/Modelling_2024).

10 slip planes are considered in each alloy.

## Materials

### CoNiRu

It is a bi-phase material. One phase has an FCC lattice while another an HCP lattice. Hence, we will consider here both FCC CoNiRu and HCP CoNiRu. For the FCC phase, we can compare results of basic structural parameters and GSFE with [DFT](http://dx.doi.org/10.1088/1361-651X/ab3b62).

### Co<sub>2</sub>Ni<sub>2</sub>Ru

It has an FCC lattice. [This paper](https://doi.org/10.1016/j.actamat.2020.05.003) reported an experimental measurement of its lattice parameter, _a_<sub>0</sub> = 3.59 &#8491;.

Unpublished DFT calculations show that, for random Co<sub>2</sub>Ni<sub>2</sub>Ru, _a_<sub>0</sub> = 3.58 &#8491;, effective _C_<sub>11</sub> = 401.078 GPa, effective _C_<sub>12</sub> = 168.944 GPa, effective _C_<sub>44</sub> = 148.554 GPa, and mean ISFE = -43.11 mJ/m<sup>2</sup>. 60 ISFE values can be found in `Co2Ni2Ru-DFT-ISFE.txt` in this GitHub repository.

### CoNiRu<sub>2</sub>

It has an HCP lattice.

No DFT or experimental data exist for comparison, to our best knowledge.

### Ni

It has an FCC lattice. Compare results of basic structural parameters and GSFE with [DFT](http://dx.doi.org/10.1063/1.5115282).

## Reference

If you use any files from this GitHub repository, please cite

- Subah Mubassira, Wu-Rong Jian, Shuozhi Xu, [Effects of chemical short‑range order and temperature on basic structure parameters and stacking fault energies in multi‑principal element alloys](https://doi.org/10.3390/modelling5010019), Modelling 5 (2024) 352--366

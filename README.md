# Non-equal molar multi-principal element materials

## Foreword

The purpose of this project is to calculate the basic structural parameters (including lattice parameter and elastic constants), generalized stacking fault energies (GSFE), and local slip resistances (LSR) in several non-equal molar multi-principal element materials (MPEMs) including three alloys and four ceramics. One equal-molar MPEA will also be considered, but mainly as a validation of the interatomic potential. The effects of chemical short-range order (CSRO) and temperature will be considered.

## LAMMPS

LAMMPS on [OSCER](http://www.ou.edu/oscer.html) likely does not come with many packages. To build more packages into LAMMPS, please visit [this page](https://docs.lammps.org/Build_package.html).

To finish this project, at least four packages are needed. The first three come with the official LAMMPS source code, and so it should be straightforward to install them:

- MANYBODY package. This is to use the manybody potential such as the embedded-atom method potential.
- EXTRA-COMPUTE package. This is to calculate the elastic constants at finite temperatures using the Born matrix method. To learn more, please visit [this page](https://docs.lammps.org/Howto_elastic.html
) and [this page](https://docs.lammps.org/compute_born_matrix.html). [This paper](https://doi.org/10.1063/1.447221) should be cited for the Born matrix method.
- MC package. This is to generate materials with chemical short-range order at a given temperature. [This paper](http://dx.doi.org/10.1103/PhysRevB.85.184203) should be cited if one uses this package.

The last package does not come with the official LAMMPS source code, and so it is not straightforward to install it:

- [M3GNet package](https://www.linkedin.com/posts/ongsp_github-advancesoftcorplammps-compiled-activity-7008842815757586432-BaWR). This is to help use the M3GNet potential. [Here](https://www.nature.com/articles/s43588-022-00349-3) is the paper for M3GNet and [here](https://doi.org/10.1038/s41524-024-01227-4) is an improved version; it should be cited if one uses this package. This potential will be used in all materials in this project.

Note: if you use sbatch files from [LAMMPSatOU](https://github.com/ANSHURAJ11/LAMMPSatOU), you may need to change the walltime (default: 12 hours) and/or number of cores (default: 16). For this project, I recommend

	#SBATCH --time=200:00:00
	#SBATCH --ntasks=32
	
## Alloys

One scientific question: Is the CSRO the same, or similar, in alloys containing the same elements but different concentrations?

### CoNiRu

Build the random structure in an FCC lattice. Calculate the lattice parameter, elastic constants, and GSFE at 0 K. Compare results with [DFT](http://dx.doi.org/10.1088/1361-651X/ab3b62). The purpose is to validate the interatomic potential. Results of this equal-molar MPEA can be put in the Appendix of the paper.

### Co<sub>2</sub>Ni<sub>2</sub>Ru

It has an FCC lattice, according to [this paper](https://doi.org/10.1016/j.actamat.2020.05.003).

Build the random and CSRO structures annealed at 300 K. Calculate the lattice parameters and elastic constants of both structures at 0 K and 300 K, following [a previous GitHub repository](https://github.com/shuozhixu/Modelling_2024).

Calculate the [GSFE](https://github.com/shuozhixu/FLAM2020-GSFE) and [LSR](https://github.com/shuozhixu/FLAM2020-LSR) in both random and CSRO structures at 0 K, following [this paper](http://dx.doi.org/10.1016/j.ijplas.2021.103157).

Note: DFT calculations show that, _a_<sub>0</sub> = 3.58 nm, effective _C_<sub>11</sub> = 401.078 GPa, effective _C_<sub>12</sub> = 168.944 GPa, effective _C_<sub>44</sub> = 148.554 GPa, and mean ISFE = -43.11 mJ/m<sup>2</sup>.

### CoNiRu<sub>2</sub>

It has an HCP lattice, according to [this paper](https://doi.org/10.1016/j.actamat.2020.05.003).

Build the random and CSRO structures annealed at 300 K. Calculate the lattice parameters and elastic constants of both structures at 0 K and 300 K.

## Ceramics

Four ceramics will be considered. I will send you Sooraj's data for their structures.

### BaCe<sub>0.5</sub>Zr<sub>0.5</sub>O<sub>3</sub>

It is the simplification of BaCe<sub>0.4</sub>Zr<sub>0.4</sub>Y<sub>0.1</sub>Yb<sub>0.1</sub>O<sub>$3-\delta$</sub>, which is a proton conducting electrolyte in one type of protonic ceramics fuel cell (PCFC).

Build the random structure and the CSRO structure annealed at 823 K.

Calculate the lattice parameters and elastic constants of both random and CSRO structures at 0 K and 823 K.

Calculate the GSFE and LSR in both random and CSRO structures at 0 K.

### BaCo<sub>0.5</sub>Fe<sub>0.5</sub>O<sub>3</sub> 

It is the simplification of BaCo<sub>0.4</sub>Fe<sub>0.4</sub>Zr<sub>0.1</sub>Y<sub>0.1</sub>O<sub>$3-\delta$</sub>, which is a positive electrode (i.e., cathode) in one type of PCFC.

Build the random structure and the CSRO structure annealed at 823 K.

Calculate the lattice parameters and elastic constants of both random and CSRO structures at 0 K and 823 K.

### La<sub>0.8</sub>Sr<sub>0.2</sub>Ga<sub>0.8</sub>Mg<sub>0.2</sub>O<sub>2.8</sub>

It is an oxygen-ion conducting electrolyte in one type of solid oxygen fuel cell (SOFC).

Build the random structure and the CSRO structure annealed at 1073 K.

Calculate the lattice parameters and elastic constants of both random and CSRO structures at 0 K and 1073 K.

Calculate the GSFE and LSR in both random and CSRO structures at 0 K.

### La<sub>0.6</sub>Sr<sub>0.4</sub>CoO<sub>3</sub> 

It is the simplification of La<sub>0.6</sub>Sr<sub>0.4</sub>CoO<sub>$3-\delta$</sub>, which is a cathode in one type of SOFC.

Build the random structure and the CSRO structure annealed at 1073 K.

Calculate the lattice parameters and elastic constants of both random and CSRO structures at 0 K and 1073 K.

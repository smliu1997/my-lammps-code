# Manual for improper style dihedral/fourier

## Introduction

Here we develop an improper style potential called dihedral/fourier. This potential has the form: $E=\sum_{1, \cdots, m} K_i[1.0 + \cos(n_i \phi - d_i)]$, where $\phi$ is the improper dihedral angle. This improper style potential has identical function form as lammps dihedral style fourier. Note the improper dihedral angle has similar definition as the normal dihedral angle, while the only difference is, to define a normal dihedral angle with four atoms $i, j, k, l$, the four atoms have to be directly and sequentically connected by chemical bonds, while for the improper dihedral angle, the four atoms $i, j, k, l$ do not have to be directly or sequentially connected. 

Note lammps already has an improper style called fourier, and this potential is very different from improper style dihedral/fourier. 

## Notes for development

Some template codes are saved in directory template-code. The templates are from the code contained in lammps-7Aug2019.tar.gz. The code improper_dihedral_fourier.cpp is modified mainly from template-code/dihedral_fourier.cpp. 

## Instruction

Examples:
```
improper_style dihedral/fourier
improper_coeff 1 1 3.0 1 20.0
```

The input parameters are the same as dihedral_style fourier, the only difference is, improper_style dihedral/fourier is applied on impropers, while dihedral_style fourier is applied on dihedrals. 

## Tests

Two sets of tests are performed in directories test-4mer-dihedral-fourier and test-4mer-improper-dihedral-fourier. In these two tests, there is a molecule composed of 4 identical atoms (the structure data file is data.homopolymer). In the two tests, the only difference is, a dihedral_style fourier is performed in test-4mer-dihedral-fourier, while in test-4mer-improper-dihedral-fourier, all the dihedrals are defined as impropers (check data.homopolymer file for the difference) and improper_style dihedral/fourier is applied with the same parameters for dihedral_style fourier in the other simulation, and all the other parameters are the same in both simulations. The same random seed is used in both simulations, so the two simulations should give identical performance, such as identical potential energy at each step. 


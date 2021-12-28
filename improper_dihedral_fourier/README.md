# Manual for improper style dihedral/fourier

## Introduction

Here we develop an improper style potential called dihedral/fourier. This potential has the form: $E=\sum_{1, \cdots, m} K_i[1.0 + \cos(n_i \phi - d_i)]$, where $\phi$ is the improper dihedral angle. This improper style potential has identical function form as lammps dihedral style fourier. Note the improper dihedral angle has similar definition as the normal dihedral angle, while the only difference is, to define a normal dihedral angle with four atoms $i, j, k, l$, the four atoms have to be directly and sequentically connected by chemical bonds, while for the improper dihedral angle, the four atoms $i, j, k, l$ do not have to be directly or sequentially connected. 

Note lammps already has an improper style called fourier, and this potential is very different from improper style dihedral/fourier. 

## Notes for development
Some template codes are saved in directory template-code. The templates are from the code contained in lammps-7Aug2019.tar.gz. The code improper_dihedral_fourier.cpp is modified mainly from template-code/dihedral_fourier.cpp. 





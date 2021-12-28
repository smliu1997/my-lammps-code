# Manual for improper style cvff_shift

## Introduction

Here we extend lammps improper style cvff to cvff_shift. Improper style cvff has such a form: $E=K[1+d\cos(n\phi)]$, where $\phi$ is the improper dihedral and has a similar definition as dihedral angle, though the 4 atoms for improper dihedral may not be connected by chemical bonds sequentially. 

Improper style cvff_shift has such a form $E=K[1+d\cos(n\phi - \phi_0)]$, and this form is more generalized than improper style cvff. Notably, cvff_shift has a function form similar to dihedral_style fourier.

## Notes for development
Some template codes are saved in directory template-code. The templates are from the code contained in lammps-7Aug2019.tar.gz. 





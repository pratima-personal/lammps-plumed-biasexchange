Adding functionality to PLUMED to perform replica exchange umbrella sampling MD simulations, as described in doi:10.1063/1.1308516.

We achieve this by adding actions to PLUMED to obtain current values of the order parameter and adding new fixes to LAMMPS to perform replica exchange on the biased order parameter values with the appropriate acceptance probabilities. This accelerates equilibration of molecular structure and free energies when parallel simulations at different order parameter bias values are performed.

LAMMPS files: fix_plumed.cpp and fix_plumed.h
Both to be placed in the LAMMPS src directory

PLUMED files: Action.h, PlumedMain.cpp, PlumedMain.h, Restraint.cpp
Action.h, PlumedMain.cpp and PlumedMain.h in the PLUMED src/core directory
Restraint.cpp in the PLUMED src/bias directory

# VASP
Vienna Ab-initio Simulation Packages is a common tools for DFT calculation. It comes with commercial version mostly used by professional engineer, scientists and academic researcher. This repo will cover basic knowledge to VASP codes. You can use it for your references. Happy computing !!!

# Packages requirements
1. VASP 
2. VASPkit
3. VESTA
4. gnuplot/xmgrace

# Inputs files
1. INCAR : contains specific parameters/tags that control the calculation.
2. POSCAR : contains position/geometry of the system.
3. POTCAR : contains PseudoPotential (PP) and XC functional.
4. KPOINTS : contains kpoints mesh.

# Create input files
1. At first create INCAR file with necessary tags for your system.
2. Use VESTA to open CIF file and export data into POSCAR file.
3. To create POTCAR file run: $ cat /home/.../VASP/vasp.6.x.x/PBE_pot/Mg/POTCAR > POTCAR
4. To create KPOINTS file run: $ vaspkit
and select:
- (1) VASP Input-Files Kit
- (102) Generate KPOINTS File for SCF Calculation

# command 
$ mpirun -np 8 vasp_std

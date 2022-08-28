# For INCAR file
copy INCAR file of Scf and change ISTART = 1 & ICHARG=11 for DOS calculation
also add LORBIT = 11 tags

# For KPOINTS : To generate K POINTS in gamma-centered for tetrahedra method
In terminal run vaspkit and select 
	(1) VASP Input-Files Kit
	(102) Generate KPOINTS File for SCF Calculation
	and select options as necessary
	
# For POSCAR file
copy the CONTCAR file of Scf and rename into POSCAR
&
copy all necessary CHGCAR, POTCAR ...

# run calculation
mpirun -np 8 /home/.../vasp.6.x.x/bin/vasp_std

# For DOS structure 
run vaspkit from terminal and select
	  (11) Density-of-States
	  (111) Total Density-of-States
and plot the TDOS.dat file 





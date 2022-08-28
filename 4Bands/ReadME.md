# For INCAR file
copy INCAR file of Scf and change ISTART = 1 & ICHARG=11 for Band calculation
also add LORBIT = 11 tags

# To generate high symmetry K POINTS
In terminal run vaspkit and select 
	(3) K-Path for Band-Structure
	(302) 2D Structure
	and select options as necessary
and rename the KPATH.in file into KPOINTS

# For POSCAR file
copy the CONTCAR file of Scf and rename into POSCAR
&
copy all necessary CHGCAR, POTCAR ...

# run the calculation 
mpirun -np 8 /home/.../vasp.6.x.x/bin/vasp_std

# For Band structure
run vaspkit from terminal and select
	(21) DFT Band-Structure
	(211) Band-Structure	
then plot the BAND.dat file
	
		





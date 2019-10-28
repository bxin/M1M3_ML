The final bending mode forces after the scaling is found at
\url{https://github.com/bxin/M1M3_ML/blob/master/data/M1M3_1um_156_force.txt}.
Each row is for an actuator. There are 156 rows in total.
The first column is the actuator ID. The 2nd and 3rd columns are the x
and y coordinates of the actuators. The rest of the columns are forces
for individual bending modes in Newton.
The bending mode shapes are at
\url{https://github.com/bxin/M1M3_ML/blob/master/data/M1M3_1um_156_grid.txt}
Each row is for a surface node. There are 5256 rows in total. The
first column is the node ID. The 2nd and 3rd columns are the x and y
coordinates in meter for that node. The rest of the columns are for
individual bending modes. Note that these are surface normal
displacements in meter, which need to be projected to surface sag if
used in raytrace programs.

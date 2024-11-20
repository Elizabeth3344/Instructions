All modeling projects are done in folder "modeling".

1) Create a file named "in.<file_name>" with your Lammps script. If you mention another auxiliary code files in your main one, adress them as "../../modelling/<file_name>". ../../ helps you to get out of lmp, which runs your script.
2) To run your script in terminal change your current folder to "lammps/build" and go "./lmp -in ../../modeling/in.<file_name>".

There may be some problems during the first launches:
1) "ERROR: Unrecognized fix style 'rigid/small' is part of the RIGID package which is not enabled in this LAMMPS binary"
This error means that you need to install the rigid package for your lammps.

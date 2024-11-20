All modeling projects are done in folder "modeling".

1) Create a file named `in.<file_name>` with your Lammps script. If you mention another auxiliary code files in your main one, adress them as `../../modelling/<file_name>`. `../../` helps you to get out of lmp, which runs your script.
2) To run your script in terminal change your current folder to "lammps/build" and go `./lmp -in ../../modeling/in.<file_name>`. You may find "lmp" in the "build" folder. You can do `lmp` from only this location in "lammps".

There may be some problems during the first launches:
1) "ERROR: Unrecognized fix style 'rigid/small' is part of the RIGID package which is not enabled in this LAMMPS binary".
This error means that you need to install the rigid package for your lammps. To install the package from "lammps/build" go `cmake -D PKG_RIGID=yes ../cmake` and then `cmake --build .`.
2) Rigid may also need mpi-cxx package for parallel computing. The error "No package 'mpi-cxx' found" may appear during the trying to go `cmake ../cmake`. To solve the problem go `sudo apt install mpich` from your any current path. Now mpi is located in "lammps/src". You may check it's presents by command `ls | grep lmp_mpi` in "src".
3) You may not to pay your attention on the messages such as "Could NOT find ClangFormat". This tool is needed for formatting and doesn't affect your codework.

Congrats! All other errors may appear because your script sucks and is not working:)

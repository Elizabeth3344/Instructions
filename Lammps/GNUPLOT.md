Gnuplot is used to plot the graphics using the table with data after calculation in Lammps. <br />

To run GNUPLOT :<br />
``gnuplot`` <br />
``plot 'log.lammps' using Xcolumn:Ycolumn``<br />
<br />
Here Xcolumn and Ycolumn are the numbers of columns which you want to include to plot the dependence of the value corresponding to the second selected column on the value of the first selected column.<br />
<br />
You may also write: ``plot 'log.lammps' using Xcolumn:Ycolumn with lines`` to build a plot with lines.

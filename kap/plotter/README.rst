These plotting programs and scripts aim to make it simple to plot opacities.

To use them, first compile the kap plotter program::

  ./clean
  ./mk

The options that control what data is output by the program are
documented in the file ``inlist_plotter``.  This inlist contains two
namelists: the ``kap`` namelist that controls the MESA ``kap`` module
and the ``plotter`` namelist that controls the plotter program (see
source in ``src/kap_plotter.f90``).  Edit these namelists so that the
plotter will output the desired quantities.

Then, run the plotter::

  ./plotter

This will create an output data file ``kap_plotter.dat``.

A python script that knows how to read this file and plot it using
matplotlib is provided.  You can invoke it via::

  ./plotter.py

This will produce a plot file ``kap_plotter.png`` that you can then
view.  You may need to edit the python file to manually adjust various
aspects of the plotting (e.g., colorbar limits).

As well, you can plot which tables are used in the plotted parameter
space by setting plot_regions to true. To plot those regions call
the following script as::

  ./regions.py

This will produce the plot ``kap_regions.png`` that you can then
view.



  



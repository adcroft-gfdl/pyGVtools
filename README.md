About
=====

pyGVtools is a python replacement for the matlab "gtools" scipts and provides a single-step solution for rapid visualization of netCDF output from the numerical ocean models MOM6 and GOLD. The tools will work on most netCDF files but are specifically designed to understand the general vertical (and curvilinear-horizontal) coordinates of the MOM6 and GOLD codes.

Pre-requisites
==============
python             - version 2.7 or higher  
netCDF4 for python - https://code.google.com/p/netcdf4-python/  
matplotlib         - http://matplotlib.org/

How to obtain the tools
=======================

In the location where you would like the directory "pyGVtools" to appear type:  

    git clone https://github.com/Adcroft/pyGVtools.git  
Thereafter, you can invoke the tools with <path-you-chose>/pyGVtools/tool. For instance if you were in your home directory (~) when you cloned the repository you could invoke gplot.py with ~/pyGVtools/gplot.py. You can also add pyGVtools to your PATH environment variable which would allow you to invoke without the explcit path, e.g. gplot.py.

How to use
==========

    gplot.py --help for more extensive information

Simple examples:

    gplot.py dat.nc,depth  
    gplot.py surf.nc,sst,5
    gplot.py surf.nc,sst,5,201:300,150:
    gplot.py surf.nc,sst,5,=0:,:

Complex examples:

    gplot.py surf.nc,sss,: --clim 33 38 --supergrid ocean_hgrid.nc -output sss.%4.4i.png --animate
    gplot.py prog.nc,temp,1,:,:,=-170 --elevation prog.nc,e

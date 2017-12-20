# PyCCD-Plotting-Tool

#### Abstract:

This plotting tool is being developed to provide visualization and
analysis support of LCMAP products generated with PyCCD.  Multispectral
time-series models and calculated indices at a specified point location
are available for plotting.  The
plots by default include all ARD observations, PyCCD time-segment
model-fits, time-segment attributes including start, end, and break
dates, and datelines representing annual increments on day 1 of each
year.  The tool generates an interactive figure that contains the
specified bands and indices, with each of these being drawn on its
own subplot within the figure.   Interactive capabilities of the figure
include zooming-in to an area of interest, returning to the default
zoom level, adjusting subplot-specific x and y axis ranges, adjusting
subplot sizes, and saving the current figure.  For each subplot the
x-axis represents the dates of the time series, and the y-axis
represents that subplot’s band values.  Both axes are rescaled and
relabeled on zoom events allowing for finer resolution at smaller
scales.  Each subplot has interactive picking within the plotting area
and within the legend.  Left-clicking on observation points
in the subplot displays the information associated with that
observation in a window on the GUI.  Left-clicking on items in the
legend turns on/off those items in the subplot.  Button controls on
the GUI allow for generating and displaying the plot, clearing the
list of clicked observations, saving the figure in its current state
to a .PNG image file, and exiting out of the tool.

## Installing

System Requirements:

pyccd_plotter is known to work on Win32 and Win64 systems
##### Note:
It is recommended to use conda for installing gdal

* Install Anaconda or Miniconda
  * Download link: https://www.anaconda.com/download/
* Create a virtual environment with python 3.5 and install matplotlib
    ```bash
    $conda create -n <env-name> python=3.5 matplotlib
    ```
    * Alternatively, you can use the spec-file.txt if on Win-64
    ```bash
    $conda create -n <env-name> --file spec-file.txt
* Activate the virtual environment and install gdal from conda-forge
    ```bash
    $activate <env-name>
    (env-name)$conda install gdal -c conda-forge
    ```
* Clone or download the GitHub repository
    ```bash
    $cd \<working-dir>
    $git clone https://github.com/danzelenak-usgs/PyCCD-Plotting-Tool.git
    $cd PyCCD-Plotting-Tool\
    ```
* Install the plotting tool using setup.py with the virtual env activated
    ```bash
    $activate <env-name>
    (env-name)$ python setup.py install
    ```


## Run the Tool

* Activate the conda environment if not already

* Option A - From the console
    ```bash
    (env-name)$pyccd_plotter
    ```
* Option B - Use the pyccd_plotter.exe
    * located in <python_path>/Scripts/pyccd_plotter.exe



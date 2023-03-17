Installation
++++++++++++

This installation works under the assumption that the user is 
familiar with the installation and implementation of the SLEUTH model. 
For basic tutorials and installation, refer to 
the `Project Gigalopolis <http://www.ncgia.ucsb.edu/projects/gig/>`_ website.
The procedure for installing the SLEUTsH is as follows.


Step 1: Downloading the original SLEUTH source code
===============================================================

The source codes for the SLEUTH models are available `here <http://www.ncgia.ucsb.edu/projects/gig/Dnload/download.htm>`_.
There are currently two versions listed that vary mainly on how model calibration is done.

* **SLEUTHGA** (`SLEUTH GA <http://www.ncgia.ucsb.edu/projects/gig/Dnload/SLEUTHGA.zip>`_; version released in April 2017)
* **SLEUTH** (`SLEUTH3.0beta_p01 <http://www.ncgia.ucsb.edu/projects/gig/Dnload/SLEUTH3.0beta_p01_linux.tar.gz>`_; released 6/2005)

The choice of the model will depend on the user. The `SLEUTH GA` will implement
the calibration faster than the second one, which uses brute force calibrations using Monte Carlo simulation.

Step 2: Downloading the patch files to represent SLEUTsH
========================================================================

The source codes of the original SLEUTH have to be updated in order to reflect the growth rules of railway-induced urban growth.
The patches to reflect this can be downloaded through the links below.

* For SLEUTHGA, download the files through the repository `here <https://github.com/TokyoTechGUC/SLEUTsH_code/archive/refs/heads/main.zip>`_.
* For the SLEUTH, download the files through the repository `here <https://github.com/TokyoTechGUC/SLEUTsHGA_code/archive/refs/heads/main.zip>`_.

Step 3: Replacing the original source codes with the patch
===============================================================

#. Create a folder where the SLEUTsH is to be installed.
#. Copy the contents of the original SLEUTH folder (either SLEUTHGA or SLEUTH) into the SLEUTsH folder.
#. Move the patch files into the SLEUTH folder.

While the patch files are intended to introduce railway-induced urban growth,
additional patches are added for efficiency, such as:

* Increasing the allowed number of input files
* Removing the years in the predicted images (useful when post-processing the outputs with GIS tools)
* Increasing the character lengths of files

Step 4: Installing the SLEUTsH model
====================================

Inside the SLEUTsH folder, the common procedure
used to install all SLEUTH models must be followed. For details,
visit the `Project Gigalopolis <http://www.ncgia.ucsb.edu/projects/gig/Imp/implement.htm>`_ site.
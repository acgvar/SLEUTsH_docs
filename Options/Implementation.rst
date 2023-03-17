Implementation
++++++++++++++++++++

.. note::
    Instructions are only for the additional steps and inputs
    needed to run the SLEUTsH model. The usual process 
    of running the SLEUTH models can be conducted.

Implementation of SLEUTsH is the same as the default SLEUTH models
except in the inclusion of an input file and a necessary modification in the scenario file.

Additional input (stations)
====================================

To run the SLEUTsH model, at leaast one gif file is needed to represent
the locations of the station. The year it represent must at least match the
latest year of the other inputs. This file is represented by an array
of 1's and 0's, such that locations where stations are absent
are assigned a value of 0. Furthermore, SLEUTsH represents
stations with buffers (or a certain circular area centered at the station). A buffer radius
of around 600-m should be set.

The gif must have the format ``<domain>.station.<year>.gif``. 
Examples are as follows where ``QC`` refers to the domain to stand for Quezon City, Manila::
 
    QC.station.2000.gif
    QC.station.2005.gif
    QC.station.2010.gif

At the current SLEUTsH version,
the year must match at least the latest available year of the land cover
or urban cover input.

A sample file can be downloaded :download:`here <../images/QC.station.2010.gif>`. A few visualization softwares may not be able to
visualize the file properly because of the values set in the gif.
Try visualizing with QGIS and assigning colors to the 1 and 0 values.

Modifications in the scenario file
====================================

In order for SLEUTsH to recognize the input station files,
slight modifications in the scenario file are necessary. For example,
to consider the gifs above as inputs, the following has 
to be included (e.g. below the ``URBAN_DATA`` files) in the scenario files.

.. code-block::

    ...
    URBAN_DATA= QC.urban.2010.gif

    STATION_DATA= QC.station.2000.gif
    STATION_DATA= QC.station.2005.gif
    STATION_DATA= QC.station.2010.gif
    ...

Running the model
==================

Once the above is set, you may run the model as in the 
default method. If an error is encountered, there is a possibility
that it has something to do with the system settings. Hence, before
running the SLEUTsH model, ensure that SLEUTH could run
smoothly in your system.
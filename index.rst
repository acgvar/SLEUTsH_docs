.. SLEUTsH: Railway-induced urban growth for SLEUTH documentation master file, created by
   sphinx-quickstart on Thu Mar 16 09:52:03 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to SLEUTsH: Railway-induced urban growth for SLEUTH's documentation!
============================================================================

.. note:: 
   This page is designed only for users who are already familiar
   with the SLEUTH model and have experienced implementing them smoothly
   in their system.

Introduction
-------------

The `SLEUTH <http://www.ncgia.ucsb.edu/projects/gig/About/bkOverview.html>`_ model 
is a cellular-automata model widely used to model and predict changes in land cover and urban cover.
The model was developed (`Clarke et al., 1997 <http://www.ncgia.ucsb.edu/projects/gig/Pub/SLEUTHPapers_Nov24/Clarke_Hoppen_Gaydos_1996.pdf>`_) by Dr. Keith C. Clarke, who continues advancing the model at the University of California, Santa Barbara, Department of Geography. 
Dr. Clarke's group has developed its latest version of SLEUTH that can speed up
the calibration phase through a widely known machine-learning algorithm called genetic algorithm (GA).

SLEUTsH (`Varquez et al., 2020 <https://www.mdpi.com/2071-1050/12/17/6801>`_; `Varquez et al., 2023 <https://www.sciencedirect.com/science/article/pii/S2210670723000537>`_) is a version of the original SLEUTH model, expanded to contain railway-induced urban growth.
This version is represented by a patch file of the original source code to include a growth rule, which considers urban growth at surrounding railway stations 
that are represented as one of the standard inputs (.gif format) of the model.

This page is designed for users to follow the work 
and motivate advancement of railway transport representation in 
urban growth models, not limited to the SLEUTH model.

Disclaimer
-------------

The real world is a complex system. There is no guarantee
that the predictions will reflect the actual future. Hence, 
users are advised to conduct sensitivity experiments and implement
other urban growth models to increase plausibility of the forecasts. 
With this, the developers are not held responsible for any decisions
based on the model

.. toctree::
   :maxdepth: 2
   :hidden:

   Options/Installation
   Options/Implementation
   Options/References
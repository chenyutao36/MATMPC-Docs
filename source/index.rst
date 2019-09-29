.. MATMPC documentation master file, created by
   sphinx-quickstart on Sun Sep 29 20:26:10 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to MATMPC's documentation!
==================================

MATMPC: MATLAB based nonlinear MPC tool

MATMPC is an open source software built in MATLAB for nonlinear model predictive control (NMPC). It is designed to facilitate modelling, controller design and simulation for a wide class of NMPC applications. MATMPC has a number of algorithmic modules, including automatic differentiation, direct multiple shooting, condensing, linear quadratic program (QP) solver and globalization. It also supports a unique Curvature-like Measure of Nonlinearity (CMoN) MPC algorithm. MATMPC has been designed to provide state-of-the-art performance while making the prototyping easy, also with limited programming knowledge. This is achieved by writing each module directly in MATLAB API for C. As a result, MATMPC modules can be compiled into MEX functions with performance comparable to plain C/C++ solvers. MATMPC has been successfully used in operating systems including WINDOWS, LINUX AND OS X.

.. toctree::
    :maxdepth: 3

    license
    contact
    cite

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

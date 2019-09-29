========================
Quick start instruction:
========================

Basic installation:
===================

MATMPC requires two fundamental software and toolboxes

* MATLAB (R2014b or above) 

* CaADi 3.3.0

CaADi is the state-of-art automatic differentiation (AD) tool for computing derivatives of functions. 
For how to download and install CaADi, please visit https://github.com/casadi/casadi/wiki/InstallationInstructions.

Advanced features:
==================

For basic use, you don't need to install anything else. However, if you want to use the QP solver *HPIPM* and *IPOPT*, you need to follow the following steps.

Comipler on Windows
-------------------

For Windows users who want to use *HPIPM*, a linux-like C compiler *MinGW* is necessary. To install it, follow the steps below:

1. start with no mingw or msys on your system (otherwise, please uninstall them)

2. download msys2 at https://www.msys2.org/ (choose x86_64 for 64-bit system)

3. run the MSYS2 installer, install MSYS2 at default path (e.g. C:\msys64)

4. open MSYS2 at C:\msys64\msys2_shell.bat

5. type "pacman -Syuu" (may take a while, if get stucked at end, then just close this window)

6. close and reopen msys2_shell.bat, type "pacman -S base-devel mingw-w64-x86_64-toolchain" (take some time)

7. add "C:\msys64\usr\bin" and "C:\msys64\mingw64\bin" into system environment path (not user path)

8. open a windows command window by using "cmd", type "gcc -v", if you get information about your gcc version, then you have installed MINGW successfully.


Linear algebra library *BLASFEO*
--------------------------------

*HPIPM* is built on *BLASFEO*. To install *BLASFEO*, follow the steps below:

Now we can install BLASFEO and HPIPM.

1. download *BLASFEO* from https://github.com/chenyutao36/blasfeo and 

2. go to *BLASFEO* directory, open Makefile.rule using a text editor

3. select target architecture according to your CPU type (if not sure, use X64_INTEL_CORE if you have a INTEL CPU)

4. uncomment OS=WINDOWS **if you use WINDOWS**

5. choose C Compiler as CC=x86_64-w64-mingw32-gcc instead of CC=gcc **if you use WINDOWS**

6. open a command window

7. type "make" (take a while)

8. type "make install_static"

QP solver *HPIPM*
-----------------

1. download *HPIPM* from https://github.com/chenyutao36/hpipm

2. go to *HPIPM* directory, open Makefile.rule using a text editor

3. select target architecture according to your CPU type (if not sure, use X64_INTEL_CORE if you have a INTEL CPU)

4. uncomment OS=WINDOWS when choosing operating system **if you use WINDOWS**

5. choose C Compiler as CC=x86_64-w64-mingw32-gcc instead of CC=gcc **if you use WINDOWS**

6. open a command window

7. type "make" (take a while)

8. type "make install_static"

Generate HPIPM MEX files
------------------------

Finally, we generate MEX files for *HPIPM*.

1. Open MATLAB and go to MATMPC/mex_core

2. open compile_hpipm.m

3. Click Run and you should have hpipm_sparse.mexw64, hpipm_pcond.mexw64 and Condensing_Blasfeo.mexw64 (e.g. Win 64)

Install *IPOPT* (Windows only)
------------------------------

Install *OPTI Toolbox* from https://www.inverseproblem.co.nz/OPTI/. You are done!




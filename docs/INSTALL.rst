Installation
------------

Requirements:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Python >= 3.9

Step 1: Create a virtual environment
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

``conda create -n venv_chronix2grid python=3.9``

``conda activate venv_chronix2grid``



Step 2 (first option): Install from source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

``mkdir c2g_test``

``cd c2g_test``

``git clone https://github.com/Grid2op/chronix2grid.git``

``cd chronix2grid``

``pip install -U .``


Step 2 (second option): Install from pypi
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
``source venv_chronix2grid/bin/activate``

``pip install Chronix2Grid==1.0.2``

or if you want to install optional dependencies (e.g. tensorflow if you want to use GAN generation for solar and wind)

``pip install Chronix2Grid[optional]==1.0.2``

Step 3: Install library requirements
^^^^^^^^^^^^^^^^^^^^^^^^^^^

``pip install -r requirements_test.txt``


Additional install required for dispatch
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A backend for dispatch has been implemented with PyPSA 

``pip install -U pypsa``

Note: Currently, HIGHS is used as the Optimal Power Flow (OPF) solver due to its fast computation. If you prefer the CBC solver, please install it from: [https://projects.coin-or.org/Cbc](https://github.com/coin-or/Cbc/releases]

[Optional] Compile and output the sphinx doc (this documentation)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Run
``./docs/make.bat html``

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mlund/SI-asynuclein-protonation/HEAD?urlpath=lab)

# Supporting information for _Charge compensation during amyloid formation of alpha-synuclein_

This repository contains electronic notebooks for reproducing the simulation results presented
in the above manuscript.

## Layout

Each of the three folders below contains simulations of alpha-synuclein as a monomer and as a decamer
for the (1) the wildtype and for (2) a mutant. The salt concentrations can be 0 mM or 15 mM as indicated.
Also, in each folder you will find Jupyter notebooks for either running Monte Carlo simulations and for
simply plotting and analysing. You will most likely want to run the latter as running all simulations
is a lengthy procedure.

- `wildtype-0mM/`
- `wildtype-15mM/`
- `mutant_5Q-0mM/`

In addition to simulations, the folder `extract-nmr-data` contains a notebook for extracting
data from a previously published experimental work.

## Requirements

To run the Notebooks, simply click on the _launch binder_ logo above. Alternatively,
install python via [Miniconda](https://conda.io/miniconda.html) and
make sure all required packages are loaded by issuing the following terminal commands

``` bash
    conda env create -f environment.yml
    source activate asyntitr
    jupyter-notebook
```

For re-running simulations, [Faunus](https://github.com/mlund/faunus) git revision 075bf8de (2020-07-13)
must be build using a C++ compiler. An archive of the source code is included.



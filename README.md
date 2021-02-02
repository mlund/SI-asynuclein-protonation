[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mlund/SI-asynuclein-protonation/HEAD?urlpath=lab)

# Supporting information for _Charge Compensation During Amyloid Formation of α-synuclein_

This repository contains electronic notebooks for reproducing the simulation results presented
in the above manuscript.

## Layout

Each directory listed below contains simulation output of α-synuclein as a monomer and as a decamer,
together with Jupyter Notebooks (`*.ipynb`) for reproducing analysis and figures presented in the publication.

- `wildtype-0mM/` - α-synuclein wildtype, no salt
- `wildtype-15mM/` - α-synuclein wildtype, 15 mM salt
- `mutant_5Q-0mM/` - α-synuclein 5Q mutant, no salt
- `extract-nmr-data/` - Notebook for extracting data NMR data
- `faunus-source/` - C++ source of the MC simulation software (Faunus 2.4.1, git patch 075bf8de)

## Requirements

To run the Notebooks online, click on the "launch binder" logo above. Alternatively,
install python via [Miniconda](https://conda.io/miniconda.html) and
make sure all required packages are loaded by issuing the following terminal commands

``` bash
    conda env create -f environment.yml
    source activate asyntitr
    jupyter-notebook
```

### Monte Carlo Simulation Software

For optionally running simulations, [Faunus](https://github.com/mlund/faunus) must be build using a C++ compiler:

``` bash
    cd faunus-source/
    unzip faunus-075bf8de.zip 
    patch CMakeLists.txt patch1-eigen.diff # apply patch due to URL change of dependency
    cmake . -DCMAKE_BUILD_TYPE=Release
    make faunus -j
```

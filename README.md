[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mlund/SI-asynuclein-protonation/HEAD?urlpath=lab)

# Electronic Notebook: _Charge Regulation During Amyloid Formation of α-synuclein_

This repository contains electronic notebooks for reproducing the simulation results presented
in the above manuscript, published in [Journal of the American Chemical Society, 2021](https://dx.doi.org/10.1021/jacs.1c01925).

## Layout

Each directory listed below contains simulation output of α-synuclein as a monomer and as a decamer,
together with Jupyter Notebooks (`*.ipynb`) for reproducing analysis and figures presented in the publication.

- `wildtype-0mM/` - α-synuclein wildtype, no salt
- `wildtype-15mM/` - α-synuclein wildtype, 15 mM salt
- `mutant_5Q-0mM/` - α-synuclein 5Q mutant, no salt
- `extract-nmr-data/` - Notebook for extracting data NMR data
- `faunus-source/` - C++ source of the MC simulation software (Faunus 2.4.1, git patch 075bf8de)

## Requirements

To run the Notebooks online, click on the _Launch Binder_ logo above. Alternatively, if you want
to run on your own computer,
install python via e.g. [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://docs.conda.io)
and make sure all required packages are loaded by issuing the following terminal commands

``` bash
    conda env create -f environment.yml
    source activate asyntitr
    jupyter-notebook
```

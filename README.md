# Analysis of insertions in genomic and protein sequences of coronaviruses

## Motivation

...

## Collaborators

- Etienne Decroly
- Jacques van Helden
- Erwan Sallard
- José Halloy

## Files

## Usage

### Installing the software environment

The whole software environment required to reproduce these analyses can be easily installed with miniconda.


```
## List the targets
make -f scripts/makefiles/01_software-environment.mk

## Install the environment
make -f scripts/makefiles/01_software-environment.mk install_env

## See the list of targets for the other steps

```

### Analysis of the spike protein sequences

The aim of this program is to retrieve from uniprot all the available sequences of spike proteins belonging to the specified taxa, to align them and to identify the insertions in one of these proteins (by default the spike of SARS-CoV-2).

The commands are specified in the make file `make -f scripts/makefiles/03_protein-alignments.mk`. 

The list of targets can be obtained with the following command.

```
make -f scripts/makefiles/03_protein-alignments.mk
```

You should first run one of the "uniprot_" functions, then "align_muscle" and finally "identify_insertion". For example:

```
make -f scripts/makefiles/03_protein-alignments.mk uniprot_sarbecovirus
make -f scripts/makefiles/03_protein-alignments.mk align_muscle
make -f scripts/makefiles/03_protein-alignments.mk identify_insertion
```

Results will be found in the "results/spike_protein" folder (namely the multiple alignment file in several formats, and a .csv file describing the position of the insertions in the reference protein).

#### Colorizing the inserts on the 3D structural model

bla bla bla

1. Open pymol
2. Open the script `scripts/pymol/colorize-inserts.pml`
3. ....





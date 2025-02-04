# COFI-2023

This repo usese the CMS ML HATS tutorial as a base for examples shown at the ML Basic Tools and Resources sessions of the COFI 2023 Winter School

To run locally, run commands like these from your terminal:

## Streamlined environment for the COFI days 1 and 2 notebook demonstrations
This environment focuses on having pytorch, torchvision, pytorch_lightning, wandb, tritonclient, jupyter, and a few other niceties installed.

This will be slightly easier to solve with the old conda installer
```bash
# Download the setup bash file for your machine from here https://github.com/conda-forge/miniforge#mambaforge
# e.g. wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh
# Install: (the mamba directory can end up taking O(1-10GB) so make sure the directory you're using allows that quota)
chmod u+x Mambaforge-Linux-x86_64.sh
./Mambaforge-Linux-x86_64.sh  # follow instructions in the installation

git clone https://github.com/nickmanganelli-sr/cofi-2023.git
cd cofi-2023
mamba env create -f environment.yml
conda activate cofi-2023
jupyter lab # this will create a JupyterLab instance from which you can run all the notebooks.
```

## Extended environment
This environment focuses on installing as much as possible, capable of running pytorch, keras, tensorflow, pytorch_geometric,
and many other packages (in addition to the ones in the streamlined environment). The yaml file and environment name differ.

WARNING: This is a very heavy installation, and solving dependencies on different OS's may take unreasonably long with
an old installation of conda. Please ensure you use one with the mamba solver (e.g. with the directed miniforge installation below)
```bash
# Download the setup bash file for your machine from here https://github.com/conda-forge/miniforge#mambaforge
# e.g. wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh
# Install: (the mamba directory can end up taking O(1-10GB) so make sure the directory you're using allows that quota)
chmod u+x Mambaforge-Linux-x86_64.sh
./Mambaforge-Linux-x86_64.sh  # follow instructions in the installation

git clone https://github.com/nickmanganelli-sr/cofi-2023.git
cd cofi-2023
mamba env create -f environment-ext.yml
conda activate cofi-2023-ext
jupyter lab # this will create a JupyterLab instance from which you can run all the notebooks.
```


# CMS Machine Learning Hands-on Advanced Tutorial Session (HATS)


## Introduction

This is a set of tutorials for the CMS Machine Learning Hands-on Advanced Tutorial Session (HATS). 
They are intended to show you how to build machine learning models in python, using `Keras`, `TensorFlow`, and `PyTorch`, and use them in your `ROOT`-based analyses. 
We will build event-level classifiers for differentiating VBF Higgs and standard model background 4 muon events and jet-level classifiers for differentiating boosted W boson jets from QCD jets using dense and convolutional neural networks.
We will also explore more advanced models such as graph neural networks (GNNs), variational autoencoders (VAEs), and generative adversarial networks (GANs) on simple datasets.

## Setup

### Vanderbilt Jupyterhub (Recommended!)

The recommended method for running the tutorials live is the Vanderbilt Jupyterhub, follow the instructions [here](https://fnallpc.github.io/machine-learning-hats/setup/vanderbilt-jupyterhub/vanderbilt.html).

### FNAL LPC

Not as well supported, but instructions are [here](https://fnallpc.github.io/machine-learning-hats/setup/lpc.html).

### Locally

All these notebooks can be run on your local machine as well. 
It can often be useful to test your models and pipelines locally, but it is not recommended to run full trainings as these can be resource-intensive.

To run locally, run these commands from your terminal:

```bash
# Download the setup bash file for your machine from here https://github.com/conda-forge/miniforge#mambaforge
# e.g. wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh
# Install: (the mamba directory can end up taking O(1-10GB) so make sure the directory you're using allows that quota)
chmod u+x Mambaforge-Linux-x86_64.sh
./Mambaforge-Linux-x86_64.sh  # follow instructions in the installation

git clone https://github.com/FNALLPC/machine-learning-hats/
cd machine-learning-hats
mamba create -f environment.yml
mamba activate machine-learning-hats
jupyter lab  # this will create a JupyterLab instance from which you can run all the notebooks.
```

### Binder

You can launch this repository in a "Binder" instance using: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FNALLPC/machine-learning-hats/HEAD),
or for a specific notebook by navigating to the rocket icon on the website and clicking on the Binder option.

![launch_notebooks](figures/launch_notebooks.png)

This may be a more convenient, but it has not been well tested and the set-up time can be slow.


### Google Colab

Each notebook can also be launched in a Google Colab instance by clicking "Google Colab" option in the menu bar above. 
To use this, you will have to install any extra libraries needed for the tutorial yourself and re-download the relevant datasets each time.


## Links

The indico page is: [https://indico.cern.ch/event/1311559/](https://indico.cern.ch/event/1311559/)

The Mattermost for live support is: [https://mattermost.web.cern.ch/cms-exp/channels/hatslpc-2023](https://mattermost.web.cern.ch/cms-exp/channels/hatslpc-2023)

The datasets we will use are located here: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3901869.svg)](https://doi.org/10.5281/zenodo.3901869)


## Credits

This project is created using the excellent open source [Jupyter Book project](https://jupyterbook.org/) and the [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).

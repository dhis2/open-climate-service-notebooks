# open-climate-service-notebooks

This repository contains example notebooks demonstrating how to use and interact with a local instance of Open Climate Service (OCS). 

## Setup

The following steps shows how to get started running the notebooks in this repository. The results will differ depending on which country and administrative units are available in your OCS instance. 

### Prerequisites

Before you get started, make sure you have the following installed:

- [Open Climate Service (OCS)](https://open-climate-service.dhis2.org/setup_guide/) - A local configured instance of OCS.
- [Git](https://git-scm.com/) – for cloning repositories and managing updates.
- [Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main) for managing a reproducible Python environment.
    - Follow the [installation instructions](https://www.anaconda.com/docs/getting-started/miniconda/install).
    - Run `conda init --all` in your terminal.
    - Restart your terminal for the changes to take effect.

### Download the repository

To download these notebooks to your local machine, clone the repository:

    git clone https://github.com/dhis2/open-climate-service-notebooks

### Setup the environment

First, use `conda` to create and activate the Python environment:

    conda create -y -n open-climate-service-notebooks python=3.13
    conda activate open-climate-service-notebooks

Install the dependencies in this order:

    conda install -y -c conda-forge pymeeus jupyterlab ipywidgets jupyterlab_widgets
    pip install -r requirements.txt

### Register the environment as a Jupyter kernel

To make sure the notebooks are run in the environment you just installed, register it as a Jupyter kernel:

```bash
python -m ipykernel install --user --name open-climate-service-notebooks
```

Verify that the `open-climate-service-notebooks` environment shows up in the list of kernels:

```bash
jupyter kernelspec list
```

### Running the notebooks

You’re now ready to explore and run the notebooks. We recommend doing this directly in VS Code, using the [VSCode Jupyter notebook extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter). 

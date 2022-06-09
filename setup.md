---
title: Setup
---

# Software Packages Required

You will need to have a functioning installation of Python 3 with
```
matplotlib
pandas
numpy
scikit-learn
tensorflow
pytorch
jax
```

> List under contruction
{: .keypoints}

## Install Python Packages

We recommend creating a new environment for your project. This will allow you to track dependencies a lot easier. There are several different ways to do this (virtualenv, pipenv).

you can copy the list of packages above into a file (e.g. `requirements.txt`) to install them with `pip`
```bash
python3 -m pip install -r requirements.txt
```
{: .language-bash}

If you have issues, we recommend using [mamba](https://mamba.readthedocs.io/en/latest/), which is faster and more robust than `conda` for this.
### Creating a virtual environment
#### using venv (built-in Python 3.8+)

> it’s the officially recommended way to create virtual environments since Python 3.5.
>
> See [Documentation > The Python Tutorial > 12. Virtual Environments and Packages](https://docs.python.org/3/tutorial/venv.html) for more information and a complete tutorial on `venv`.
{: .callout}

The module used to create and manage virtual environments is called `venv`. `venv` will usually install the most recent version of Python that you have available. If you have multiple versions of Python on your system, you can select a specific Python version by running `python3` or whichever version you want.

To create a virtual environment, decide upon a directory where you want to place it, and run the venv module as a script with the directory path:

```bash
python3 -m venv tutorial-env
source tutorial-env/bin/activate
```
{: .language-bash}

This will create the `tutorial-env` directory if it doesn’t exist, and also create directories inside it containing a copy of the Python interpreter and various supporting files. The last line activates the environment.

Activating the virtual environment will change your shell’s prompt to indicate what virtual environment is active. It will also modify the environment to run the python version and libraries from that environment. For example:
```bash
$ source ~/envs/tutorial-env/bin/activate
(tutorial-env) $ python
Python 3.5.1 (default, May  6 2016, 10:59:36)
  ...
>>> import sys
>>> sys.path
['', '/usr/local/lib/python35.zip', ...,
'~/envs/tutorial-env/lib/python3.5/site-packages']
>>>
```
{: .language-bash}
#### using conda

Here we show an example with conda:
```bash
conda create --name new_environment python
conda activate new_environment
```
{: .language-bash}
## Hosted solutions

* [Google Colab](colab.research.google.com)

* [Deepnote](deepnote.com)

* [Jupyter-docker-stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html), Docker images
    * See [Image list](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html) to find the appripriate image (e.g. `jupyter/tensorflow-notebook`)


{% include links.md %}

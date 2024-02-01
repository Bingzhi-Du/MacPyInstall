# PyInstall Guide

This guide provides instructions for setting up a local machine learning test environment on macOS. It includes steps for installing Python through Homebrew and setting up a Conda environment optimized for Apple Silicon.

## Prerequisites

- macOS (Mx core)
- Terminal access

## Installing Homebrew

Homebrew is a package manager for macOS. Execute the following command to install Homebrew:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## install of python (optional, conda will instead)

```
brew install python
```
### check version (optional, conda will instead)
```
python3 --version
pip3 --version
```
### download conda modifed version for apple silicon
https://github.com/conda-forge/miniforge?tab=readme-ov-file

### to the file located
```
cd ~/Donwloads
```
### activate conda env (temporarily, **path not set**)
```
source ~/miniforge3/bin/activate
```
### check version
```
conda --version
```
## set the path of conda, so mac can invoke the conda
### open path terminal
```
nano ~/.zshrc
```
### in **nano**
```
export PATH="$HOME/miniforge3/bin:$PATH"    ###"/miniforge3/bin" is your conda bin path modify it to your path
```
### save change (terminal)
**Ctrl + O**
### activate change (terminal)
```
source ~/.zshrc
```
### restart your mac

### check conda env default (can invoke conda xxx at terminal since then)
```
conda --version
```
# Python env
```
conda create -n myenv python=3.9    ###"myenv" is your environment name
```


## activate Python env
```
conda activate myenv
```

## install packages
```
conda install
pip install
```
## test mac gpu - in env ():
```
python
import torch
print(torch.backends.mps.is_available())
```






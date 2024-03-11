# A.MAC PyInstall Guide

This guide provides instructions for setting up a local machine learning test environment on macOS. It includes steps for installing Python through Homebrew and setting up a Conda environment optimized for Apple Silicon.

## a.Prerequisites

- macOS (Mx core)
- Terminal access

## b.Installing Homebrew

Homebrew is a package manager for macOS. Execute the following command to install Homebrew:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## c.install of python (optional, conda will instead)

```
brew install python
```
### 1.check version (optional, conda will instead)
```
python3 --version
pip3 --version
```
### 2.download conda modifed version for apple silicon
https://github.com/conda-forge/miniforge?tab=readme-ov-file

### 3.to the file located
```
cd ~/Donwloads
```
### 4.activate conda env (temporarily, *path not set*)
```
source ~/miniforge3/bin/activate
```
### 5.check version
```
conda --version
```
## c.set the path of conda, so mac can invoke the conda
### 1.open path terminal
```
nano ~/.zshrc
```
### 2.in *nano*
```
export PATH="$HOME/miniforge3/bin:$PATH"    ###"/miniforge3/bin" is your conda bin path modify it to your path
```
### 3.save change (in *nano*)
*Ctrl + O*
### 4.activate change (terminal)
```
source ~/.zshrc
```
### 5.restart your mac

### 6.check conda env default (can invoke conda xxx at terminal since then)
```
conda --version
```
# B.Python env
```
conda create -n myenv python=3.9    ###"myenv" is your environment name
```


## a.activate Python env
```
conda activate myenv
```

## b.install packages
```
conda install
pip install
```
## c.test mac gpu - in env ():
```
python
import torch
print(torch.backends.mps.is_available())
```
# C.Jupyter notebook 

## a.install notebook for python
```
conda install jupyter
```
## b.ipykernel for env
```
install ipykernel
```
```
python -m ipykernel install --user --name=your_environment_name    ###replace 'your_environment_name' by your env name
```
## c.check the env at ipkernel(@terminal)
```
jupyter notebook
```



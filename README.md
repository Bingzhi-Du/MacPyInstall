# PyInstall Guide

This guide provides instructions for setting up a local machine learning test environment on macOS. It includes steps for installing Python through Homebrew and setting up a Conda environment optimized for Apple Silicon.

## Prerequisites

- macOS (Mx core)
- Terminal access

## Installing Homebrew

Homebrew is a package manager for macOS. Execute the following command to install Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"


##install of python

```bash
brew install python

##check version
```bash
python3 --version
pip3 --version

##download conda modifed version for apple silicon
https://github.com/conda-forge/miniforge?tab=readme-ov-file

##to the file located
```bash
cd ~/Donwloads

##activate conda env
```bash
source ~/miniforge3/bin/activate

##check version
```bash
conda --version

##set the path of conda, so mac can invoke the conda
###open path terminal
```bash
nano ~/.zshrc

###in nano
```bash
export PATH="$HOME/miniforge3/bin:$PATH"    ###"/miniforge3/bin" is your conda bin path modify it to your path

###save change (terminal)
Ctrl + O
###activate change (terminal)
```bash 
source ~/.zshrc

###restart your mac

###check conda env default (can invoke conda xxx at terminal since then)
```bash
conda --version

#Python env
```bash
conda create -n myenv python=3.9    ###"myenv" is your environment name

#activate Python env
```bash
conda activate myenv

in env:
python
import torch
print(torch.backends.mps.is_available())






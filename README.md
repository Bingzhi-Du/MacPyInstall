# PyInstall

mac python installation for ml local test

##install of homebrew

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

##install of python

brew install python

##check version

python3 --version
pip3 --version

##download conda modifed version for apple silicon
https://github.com/conda-forge/miniforge?tab=readme-ov-file

##to the file located
cd ~/Donwloads

##activate conda env
source ~/miniforge3/bin/activate

##check version
conda --version

##set the path of conda, so mac can invoke the conda
###open path terminal
nano ~/.zshrc
###in nano 
export PATH="$HOME/miniforge3/bin:$PATH"    ###"/miniforge3/bin" is your conda bin path modify it to your path
###save change (terminal)
Ctrl + O
###activate change (terminal)
source ~/.zshrc
###check conda env default (can invoke conda xxx at terminal since then)
conda --version

#Python env

conda create -n myenv python=3.9    ###"myenv" is your environment name

#activate Python env






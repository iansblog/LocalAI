# Foundational areas to setup

Setting up the different componenets that we will need, including.
- Miniconda
- Python 3.12
- PIP
- Poetry

**Note** *If you are not running the MS ARM OS then look at the note at the bottom of this page to install the X86_64 rather then the ARM install.*

**Note:** *The miniconda install instructions have been taken from: [miniconda documentation](https://docs.anaconda.com/free/miniconda/) and issues please look at the latest install process.*

----

Double click on the created shortcut. 

Run the following commands

- mkdir -p ~/miniconda3
- wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-aarch64.sh -O ~/miniconda3/miniconda.sh
- bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
- rm -rf ~/miniconda3/miniconda.sh
- Initialize the  newly installed Miniconda install
    - ~/miniconda3/bin/conda init bash
    - ~/miniconda3/bin/conda init zsh
- sudo apt update
- sudo apt upgrade 
- sudo apt install python3.12
- sudo apt install python3-pip
- curl -sSL https://install.python-poetry.org | python3 -
- export PATH="/root/.local/bin:$PATH"

Return back to the main [README](./../README.md)

----

**Note** If you are not running the MS ARM OS but at standard x86 chip set then run the following. 

- mkdir -p ~/miniconda3
- wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
- bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
- rm -rf ~/miniconda3/miniconda.sh
- Initialize the  newly installed Miniconda install
    - ~/miniconda3/bin/conda init bash
    - ~/miniconda3/bin/conda init zsh
- sudo apt update
- sudo apt upgrade 
- sudo apt install python3.12
- sudo apt install python3-pip

Return back to the main [README](./../README.md)
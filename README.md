[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/luchem/KEMM30.git/master)
<a target="_blank" href="https://colab.research.google.com/github/luchem/KEMM30/blob/master/lectures/01-introduction.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

# KEMM30

Course files for Python in Biochemistry. 

## Running

Here are three ways you can run this:
1. Log into Google Colab and navigate to _Github_ and search for `luchem`. Open the first notebook.
2. Run using the free _My Binder_ server by clicking _launch binder_ above.
3. On local Jupyter server. Download and unzip the code. Then launch a local server by typing `jupyter lab` or `jupyter notebook` on a command line 
(the adress field in any windows browser window is a command line).
    - if this fails with "can not find command" it means that anaconda is not in the 
    search path. You can then either start a specified server/command line by starting 
    anaconda command prompt or by starting a server and navigating to the folder with your notebooks
    - add the python script folder to your environment variables. This folder can be 
    in different location but is usually easy to find. You search for the `Anaconda3` folder either at: 
    `C:\Anaconda3`, at `C:\Programs\Anaconda3`, `C:\Users\my_name\Anaconda3`,... or using the search function. 
    At the university computers in Lund/chemistry the folder you need to add is `c:\Anaconda3\Scripts`.
    For windows there is a small bat file in the main directory called `add_anaconda_scripts_to_path.bat` that 
    will do that for you (so simply double click on it).
    
## Usage without environment

The first (lecture) notebooks only use the standard scientific packages and you can start working directly. 
only for the last notebook you will need an additional package that you can install from within any notebook
with `!pip install lmfit` (and then restart the kernel to use it)

For the project notebooks you will need a number of extra packages. If you run from within any notebook this 
command you will install the in one go your installation folder (or the user folder in case of lacking rights)

`!pip install lmfit ipympl lxml nglview ipywidgets brewer2mpl rdkit ffmpeg nmrglue`.

## Usage with environment

At Lund installing an environement is very slow. So we recommend to install only the minimum using conda and then
install the rest via pip. To do this run the following commands:

``` bash
conda env create -f environment_mini.yml
conda activate KEMM30
pip install lmfit ipympl lxml nglview ipywidgets brewer2mpl rdkit ffmpeg nmrglue
jupyter nbextension enable rubberband/main
jupyter nbextension enable exercise2/main
jupyter nbextension enable --py widgetsnbextension
jupyter-notebook
```

At home you can install all packages automatically. Install python via [Miniconda](https://conda.io/miniconda.html) 
or the full anaconda from [Anaconda](https://www.anaconda.com/download) and 
then make sure all required packages are loaded by issuing the following terminal commands:

``` bash
conda env create -f environment.yml
conda activate KEMM30
jupyter nbextension enable rubberband/main
jupyter nbextension enable exercise2/main
jupyter nbextension enable --py widgetsnbextension
jupyter-notebook
```

The before each usage you must "activate" the environment by typing `activate KEMM30`.

# ResBaz19_Perth
Research Bazaar 2019 Perth (Intro to Machine Learning)

### Setup
To create a virtual environment for data visualisation.
```
$ conda env create -f environment.yml
$ conda activate resbaz
```



# Machine Learning Stream Software Requirements

## Requirements
For this workshop, you are required to **bring a computer (not a tablet, Chromebook, etc.) with a working version of Python installed.** It is recommended that you have administrative privileges on your computer — the lessons require specific software packages installed.

We will be using **Scikit Learn** and **fast.ai** for this workshop, please make sure you have installed Anaconda Distribution, and Jupyter Notebook (a programming environment that runs in a web browser) and also other relevant packages listed as below:

## Prerequisites:
- Pytorch >= v1.0
- fast.ai v1 for PyTorch https://github.com/fastai/fastai
- A dataset from Kaggle competition. You can download all of them here[].
- **Signup and apply for access Google Colab** https://colab.research.google.com/ – anyone with a Google Drive account can sign up for Colab by heading to colab website.

Please ensure you have a reasonably up-to-date Web browser. The current versions of Chrome, Safari and Firefox are all supported, but some older browsers, including Internet Explorer version 9 are not.

## Windows
Install Anaconda Python 3.x distribution https://www.anaconda.com/distribution/
Make sure you have defined the PATH system variable.

1.  Find your current Python and Conda path:
Open Windows command prompt (Press <kbd>win</kbd> and type `cmd`)
Type `where python` and `where conda`

Example: Note! your path may differ from the instruction
```
C:\>where python
C:\Users\ResBaz\AppData\Local\Continuum\anaconda3\python.exe
C:\>where conda
C:\Users\ResBaz\AppData\Local\Continuum\anaconda3\condabin\conda.bat
C:\Users\ResBaz\AppData\Local\Continuum\anaconda3\Library\bin\conda.bat
C:\Users\ResBaz\AppData\Local\Continuum\anaconda3\Scripts\conda.exe
```

2. Press  +  R together to get a command prompt. Type sysdm.cpl → go to Advanced tab → select Environment Variables

In the System variables section, choose Path → select Edit → click New

Add the path → press OK

 - using command line to verify Python has been successfully installed. Open terminal console (i.e. Anaconda Prompt,  Git Bash, Cmder, etc.) → type `python` then press Enter

Example:

Type `exit()` then Enter or <kbd>Ctrl</kbd> + <kbd>D</kbd> to exit.

 - Download a dataset from Kaggle competition to your working directory. You can download all of them here.

```
# In terminal, create a directory called 'rossmann'
$ mkdir rossmann
# Change to 'rossmann' directory:
$ cd rossmann
# Run the following command to untar rossmann.tgz file
$ tar xvzf rossmann.tgz
```

3. Create a virtual environment called **resbazml**

> Note: By creating the virtual environment via Anaconda distribution, you will be working on an isolated working copy of Python with specific versions of libraries or Python itself without affecting the base Anaconda or other projects.

Make sure the conda will be the latest version (conda install will also do the update)
```
$ conda install conda
```

Create a virtual environment from YAML file which you can download from here

> Note: download YAML file and place to any directory (i.e. /Desktop). Browse to the folder that YAML file exists before running the following command.
>

```
$ conda env create -f resbazml_environment.yml
```

Close your Anaconda Prompt terminal (or others) and relaunch it

Activate the environment
```
$ conda activate resbazml
```

4. Check the fastai installation and Pytorch version

```
$ python -m fastai.utils.show_install
```


If you can see the details as example above, your fastai installation should be working fine.

5. Fastai and Pytorch packages verification

Type the command line as below for the verification


To check if your CUDA is available or not



If the result is True, your CUDA is available for use. Otherwise, it will be False.

## MacOS and Linux
Install the Anaconda Python 3.x distribution (recommended if you’re new to conda): https://www.anaconda.com/distribution/
or the Miniconda Python 3.x distribution:	https://docs.conda.io/en/latest/miniconda.html

Load (or reload) the terminal. Make sure you have defined the PATH system variable and have conda activated by testing the command conda-env list:

If you don’t get an output similar to the one above, adjust the following commands to reflect your installation path and either run them interactively or add them to your .bashrc:
```
$ export PATH="$HOME/miniconda3/bin:$PATH"
$ source $HOME/miniconda3/bin/activate
```

Create and activate a virtual environment called resbazml
```
$ conda create --name resbazml python=3.7 -c conda-forge -c fastai python=3.7 pytorch fastai jupyter nb_conda_kernels xgboost pandas-profiling seaborn plotly python-cufflinks
$ conda activate resbazml
```

## Optional Settings
* Create a Jupyter Notebook Kernel for the Python Environment so you can switch to different kernel.

Create the Jupyter kernel and install ipywidgets
$ python -m ipykernel install --user --name resbazml --display-name "resbazml"

Sometimes there will be ‘autopep8’ error once you start Jupyter Notebook. So you can reinstall ‘autopep8’ package using conda
$ conda install -c conda-forge autopep8

(Optional) Some extensions would be helpful for using the notebook (i.e. code folding, collapsible heading, etc.) The original GitHub repository which contains a source code is here

Install Nbextensions using Conda
$ conda install -c conda-forge jupyter_contrib_nbextensions

Install Nbextensions Configurator using Conda
$ conda install -c conda-forge jupyter_nbextensions_configurator

(Optional) Nbextensions tab will also appear right next to Clusters tab

Example of configuration


(Optional) Increase cell width in a web browser
This solution will not change your default settings. All you need to do is add this following code into any cell of your current notebook and run the cell.

from IPython.core.display import display, HTML
display(HTML("<style>.container { width:100% !important; }</style>"))



# Intro to Jupyter
`jupyter` is an application that provides a simple, browser-based development environment called a "notebook". Notebooks allow you to intersperse markdown/LaTex/images/HTML with executable code and they are extremely popular in the data science community for exploratory analyis and model development. Jupyter also has a set of powerful user-contributed extensions that expand the basic notebook functionality. 

More recently jupyter developed a slightly more full-featured development environment called `jupyter lab` which includes file system navigation and system and python shells within the same browser-based user interface. This tool is gaining in popularity but for this workshop we will stick with the simple notebooks application which is still widely used. 


## Installation and Setup
Let's create a new `conda` virtual environment for running jupyter. First navigate to your project folder in Anaconda Prompt. Now we can create the environment, install jupyer and the extensions package, and then run jupyter with:

```
conda create --name jupyter_server python=3.8
conda activate jupyter_server
conda install -c conda-forge notebook
conda install -c conda-forge jupyter_contrib_nbextensions
jupyter notebook
```

The last line will launch a jupyter notebook "server" which will run until you kill the process in terminal with `Ctrl + C`. Your browser should automatically open a page communicating with this "server" - but if it doesn't you can copy/paste the URL from the printout in your terminal. You should see the "homepage" for jupyter notebook, also called the notebook "dashboard". From here you can navigate your file system and create/delete/rename notebooks.

## Setting Up Extensions for Jupyter
Before we create a notebook let's set up some extensions. From the homepage click on the "Nbextensions" tab in the top ribbon to see a list of all the extensions you can enable. We'll just enable two of them for now
- *Table of Contents (2)* - exposes a table of contents panel for navigating
- *Collapsible Headings* - allows you to collapse/hide sections

To enable these two extensions simply check the boxes. You may also need to kill (`Ctrl + C`) and restart the jupyter server in your terminal. 


## Setting Notebook Kernels (Environments)
In jupyter the virtal environment that will be used to execute your code cells is called a kernel, and you can set it from a simple dropdown in the notebook interface. By default the kernel will be whatever environment you launched the jupyter server from. It's best practice to have one environment you always use for launching/running the jupyter server, and then to set your notebook kernels to be the specific virtual environments for your project. 

In order for jupyter to recognize conda environments as potential kernels we need the `nb_conda_kernels` package installed in our project environments. Let's install it in our data science environment now. Open a new instance of Anaconda Prompt and do

```
conda activate <envname>
conda install -c conda-forge nb_conda_kernels
conda deactivate
```

# Basics of Using Notebooks
Now we're ready to start developing in notebooks. From your jupyter homepage navigate into the `/notebooks` folder and click on the `Intro_to_Jupyter_Notebooks.ipynb` notebook. It will open in a new window. The first thing we'll do is change the kernel that is set for this notebook - from the ribbon along the top choose *Kernel > Change Kernel* and select our data science environment. Now when we execute code within this notebook it will execute using that environment. Next, in the ribbon of graphic icons at the top, find and click the icon for the Table of Contents. This will create a new window displaying a hyperlinked table of contents. Walk through the notebook for an overview of the jupyter development environment.






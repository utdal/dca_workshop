# DCA Workshop

This is the almost-entirely python version of the DCA Workshop, done in a platform agnostic way.

## Installation

You will need to install a few things before starting:
1. Anaconda3/Miniconda3
2. python-mfdca
3. HMMER

**If you are on Windows, you will also need to download the Ubuntu filesystem from the App Store to use HMMER.**

1. Installing Anaconda3 and the dca environment.
    * Use [this link](https://www.anaconda.com/products/individual) for Anaconda3. You will be using the Anaconda3 terminal that gets installed if you are in Windows, and just a terminal otherwise.
    * Then, download this github repo using the green button towards the top or 
      * ```git clone git@github.com:utdal/dca_workshop.git```
    * You will use the yaml file to install the dca conda environment. Use this command to install: 
      * ```conda env create --file dca.yaml```
    * then this command to activate the environment 
      * ```conda activate dca```
    * If you have code editing software which can handle ipynb files like VS Code or Spyder, then you should be good to go. Otherwise you can run the command 
      * ```conda install jupyter``` 
    * to install the Jupyter software which will let you edit and run Jupyter notebooks by running ```jupyter``` in the terminal.
2. Installing python-mfdca
    * Download it from [this link](https://github.com/utdal/src-python-mfdca/). You can use ```git clone git@github.com:utdal/src-python-mfdca.git``` if you have git installed or just download the zip using the green button on the page.
    * In the downloaded directory, you can use the command ```pip install -e .``` to install the package.
3. Installing HMMER
    * Installation guide [is here](http://hmmer.org/documentation.html). 
    * If you are on Windows, this must be done in the Ubuntu filesystem from the App Store. 
      * This command ```sudo apt install hmmer``` should work.

Now that you have the necessary files, you should be able to run the notebook. Make sure to edit the path to your HMMER installation; if it is installed so you can run it from any folder then no changes are needed. Otherwise, point the hmmer_path variable to the install hmmer/bin directory.

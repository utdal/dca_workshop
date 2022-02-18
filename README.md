# DCA Workshop

This is the almost-entirely python version of the DCA Workshop, done in a platform agnostic way.

## Installation

You will need to install a few things before starting:
1. Anaconda3/Miniconda3
2. python-mfdca
3. HMMER

**If you are on Windows, you will also need to download the Ubuntu filesystem from the App Store to use HMMER.**

To install Ubuntu on Windows:
   * You must install Windows Subsystem Linux. 
      * For Windows 10+ : https://docs.microsoft.com/en-us/windows/wsl/install
      * Full Guide for Windows 7-: https://docs.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package 
      * Troubleshooting installation: https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#installation-issues 
      * Once you have this, you should be able to install Ubuntu through the App Store.

**Main Installation**

1. Installing Anaconda3 and the dca environment.
    * Use [this link](https://www.anaconda.com/products/individual) for Anaconda3. You will be using the Anaconda3 terminal that gets installed if you are in Windows, and just a terminal otherwise.
    * Then, download this github repo using the green button towards the top or 
      * ```git clone git@github.com:utdal/dca_workshop.git```
   * **The easy way** to install the conda environment is to open the Anaconda Navigator application, then click on the Environment Tab. There, you can find buttons towards the bottom like "Create", "Clone"... Click the import button, then open the file dca.yml from the dca_workshop directory. This should create an environment called "dca" and install the required packages.
    * **The command line way**, will also use the yaml file to install the dca conda environment. Use this command to install: 
      * ```conda env create --file dca.yaml```
      * You enter this command in Anaconda3. Below are instructions on how to reach the command bar.
      * Search for Anaconda in the computer
      * Click Anaconda-navigator
      * Open CMD.exe Prompt
    * then this command to activate the environment 
      * ```conda activate dca```
      * This is also done in the CMD.exe window.
    * **To use notebooks,** you need code editing software which can handle ipynb files like VS Code or Spyder, or you need to install the Jupyter package. 
      * **To install Jupyter the easy way**, open the Anaconda Navigator application and find the Tile labeled Jupyter, then click the Install button. Then, hit launch, and it should open a page in your web browser which will let you navigate your hard drive and open the jupyter notebook file from the DCA Workshop.
      * **the command line way**, is to use the command ```conda install jupyter``` in the command line after you've activated the dca environment. 
      * Then you can use the command ```jupyter notebook``` in the terminal to open the Jupyter browser.
2. Installing python-mfdca
    * Download it from [this link](https://github.com/utdal/src-python-mfdca/). You can use ```git clone git@github.com:utdal/src-python-mfdca.git``` if you have git installed or just download the zip using the green button on the linked page.
    * In the downloaded directory, you can use the command ```pip install -e .``` to install the package.
3. Installing HMMER
    * Installation guide [is here](http://hmmer.org/documentation.html). 
    * If you are on Windows, this must be done in the Ubuntu filesystem from the App Store. 
      * Open the Windows Ubuntu application, and it should open a text terminal.
      * Enter this command ```sudo apt install hmmer``` into the terminal and hit enter. Troubleshoot help should be in the installation guide.
      * Now you should be able to run the command hmmscan by typing the command ```hmmscan``` and hitting enter. If you see the help text for the software, then installation was successful.
      
Now that you have the necessary files, you should be able to run the notebook. Make sure to edit the path to your HMMER installation; if it is installed so you can run it from any folder then no changes are needed. Otherwise, point the hmmer_path variable to the install hmmer/bin directory.

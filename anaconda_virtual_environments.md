# Setting up Virtual Environments in Anaconda

### Step 1: Open a Terminal
Open a terminal window. On Windows, choose either Anaconda Prompt or Command Prompt from the start menu. On Mac select Terminal. Alternatively, choose 'New' and 'Terminal' from your Jupyter Notebook window.

### Step 2: Create virtual environment
In the terminal, enter the command below to create a new virtual environment. In this example, MyEnv is the name used for the environment, you should change this to whatever you like.

`conda create - n MyEnv python = 3.6`

Press 'y' and return when asked to proceed. All packages will be downloaded and installed.

### Step 3: Activate virtual environment
Run source active MyEnv to activate your virtual environment. Again, you should substitute the name you used in place of MyEnv. You should now see a prompt with the name of your environment in parentheses. On some computers, substitute conda activate MyEnv instead of source activate MyEnv.

### Step 4: Install packages
Now that you're in your virtual environment, install packages using conda install or pip install. For example, to install Seaborn type:

`conda install seaborn`

Hint 1: you can append -y to your statement to automatically proceed without being prompted to tap 'y' for yes.

Hint 2: for some packages, you may need to use a different Conda statement, eg. if installing for a different Conda channel. Search for package-specific help if needed or consult this Conda Cheatsheet.

### Step 5: Install ipykernel
For your environment to work on Jupyter notebooks, you need to install ipykernel as follows:

`conda install ipykernel`

### Step 6: Create the kernel
Now create the kernel for your environment by running:
`python -m ipykernel install --user --name MyEnv --display-name MyEnd`

### Step 7: Open a notebook with the kernel
Navigate back to the Home tab on Jupyter Notebooks in your browser. Make sure to refresh the page. Now click the New button and select the name of your kernel, which is MyEnv in this example.

### Step 8: Import packages
You can now import and use the packages from your kernel. Notice the Seaborn package imports successfully.

While writing data science code on your local machine, you'll want to use a range of different libraries. But code libraries have dependencies: one library may need Numpy version 1.16 but an older library may still understand the commands in Numpy version 1.05. This is why you need Virtual Environments. If you change the whole of your base installation of Python each time, you will be forever changing the libraries installed on your machine. Instead, create a different Virtual Environment for each major set of tasks. The Virtual Environment provides an installation of Python and whichever libraries you choose to add to it. You could create an environment called 'machine_learning' and one called 'geospatial', for instance. To run your code, you then activate the virtual environment in Jupyter Notebooks.
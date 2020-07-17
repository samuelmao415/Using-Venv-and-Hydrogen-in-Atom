# Using Venv and Hydrogen in Atom
 
Step by step tutorial to create a new virtual environment (virtualenv) and use them in ATOM with your favorite Hydrogen (macOS version)

### 1) [Install virtualenv](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)

`python3 -m pip install --user virtualenv`


### 2) Create a virtual environment

`python3 -m venv yourenvname` 


### 3) Activate your virtual environment name

`source yourenvname/bin/activate`


### 4) [Create a jupyter kernel for this particular environment so you could use hydrogen in this specific environment:](https://ipython.readthedocs.io/en/stable/install/kernel_install.html)

- in your activated virtual environment: `python3 -m pip install ipykernel --user --name yourenvname --display-name "yourenvname kernel"`
- The `--name` value is used by Jupyter internally. These commands will overwrite any existing kernel with the same name. `--display-name` is what you see in the notebook menus.


### 5) `cd` to your repository and run `atom .`:

- this will open atom in your activate virtual environment and you can select the kernel you want in this environment--the one you just created


### 6) [If you want to delete the kernel from the virtual environment you just created:](https://stackoverflow.com/questions/42635310/remove-kernel-on-jupyter-notebook)

- run in your terminal `jupyter kernelspec list` you will see a list of kernels

- run `jupyter kernelspec uninstall unwanted-kernel` will delete the kernel you typed


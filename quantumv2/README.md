# Setting up a Virtual Environment to Use Qiskit

Summary from [Python Packaging Docs](https://packaging.python.org/guides/installing-using-pip-and-virtualenv/).

(1) Install `virtualenv` if it is not already installed. (Note: There are different directions for Python 2.)

`python3 -m pip install --user --upgrade pip`
`python3 -m pip install --user virtualenv`

(2) Create a virtual environment.

Create a new directory and cd into it. Execute:

```python3 -m virtualenv envname```

(3) Activate the environment.

`source env/bin/activate`

In the virtual environment, use `pip` to install packages as you would do normally.

`pip install qiskit==0.7.0`

You may need to handle other dependencies.

To leave the environment `envname`, run `deactivate` in the terminal.

# Enabling the Virtual Environment for Jupyter Notebooks

Summary from [this article](https://anbasile.github.io/programming/2017/06/25/jupyter-venv/).

(1) In the virtual environment, install `ipykernel`:

`pip install ipykernel`

(2) Install a new kernel:

`ipython kernel install --user --name=projectname`

Now, a jupyter notebook can be started as is normally done. Inside the notebook, select the Kernel tab at the top, and under "Change kernel," select the kernel that was just installed. (Will be named whatever was put for `projectname`.)


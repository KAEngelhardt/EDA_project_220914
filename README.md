# EDA-project

In this repository, an exploratory data analysis was performed on data collected from houses in King County, Washington USA, in order to recommend suitable houses to the stakeholder Larry Sanders based on his housing criteria. A description of the stakeholder and his criteria as well as limiting factors can be found in the associated [Jupyter notebook](Larry_Sanders_EDA.ipynb).

In addition to that, the repository contains [task assignment](assignment.md), information on [house features](column_names.md), a [presentation](eda_presentation.pdf) containing main findings and conclusions, as well as [requirements file](requirements.txt) containing information on the used Python libaries.

Below are further information to reproduce this project.

## Configuring Python virtual environment
```sh
pyenv local 3.9.8
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

## Add-information for setting up Python virtual environment

One of the first steps for any data science project is to create a virtual environment. The general workflow for creating a virtual environment is as follows:
* setting the python version locally 
* creating a virtual environment using the `venv` module
* activating newly created environment 
* upgrading `pip` (This step is not absolutely necessary, but will save you trouble when installing some packages.)
* installing the required packages via `pip`

At the end, you want to make sure that people who are interested in your project can create an identical environment on their own computer in order to be able to run your code without running into errors. Therefore you can create a `requirements file` and add it to your repository. You can create such a file by running the following command: 

```bash
pip freeze > requirements.txt
```

*Note: In rare case such a requirements file created with `pip freeze` might not ensure that another (especially M1 chip) user can install and execute it properly. This can happen if libraries need to be compiled (e.g. SciPy). Then it also depends on environment variables and the actual system libraries.*

### Add-on information on unit testing (Optional)

If you write python scripts for your data processing methods, you can also write unit tests. In order to run the tests execute in terminal:

```bash
pytest
```

This command will execute all the functions in your project that start with the word **test**.

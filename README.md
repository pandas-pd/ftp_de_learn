# FTP DeLearn - Graded labs

## Setup

### Requirements:

- Python 3.12 or greater

### Setup process for VSCode:

#### VS Code:

- Install the following extenseions:
    - Jupyter
    - Jupyter PowerToys

#### Setup env and jupyter kernel (Microslop Windows):

```shell
py -m venv env
```

```shell
.\env\Scripts\activate
```

```shell
pip install -r requirements.txt
```

```shell
py -m ipykernel install --user --name=env --display-name "Python (env nlp)"
```

#### Setup env and jupyter kernel (Linux / Mac):

```shell
python3 -m venv env
```

```shell
source env/bin/activate
```

```shell
pip install -r requirements.txt
```

```shell
python3 -m ipykernel install --user --name=env --display-name "Python (env)"
```

#### Notebook:

- Select the kernel called <i>Python (env)</i>

## Setup GPU based tensorflow

tbd

# Predict-final-grade
Doing a machine learning proyect using Python with Numpy, Pandas, Matplotlib, seaborn and scikitlearn.

This proyect use a [Social, gender and study data from secondary school students]https://www.kaggle.com/uciml/student-alcohol-consumption), taken from [Kaggle](https://www.kaggle.com/).
**Features**
* school - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
* sex - student's sex (binary: 'F' - female or 'M' - male)
* age - student's age (numeric: from 15 to 22)
* address - student's home address type (binary: 'U' - urban or 'R' - rural)
* famsize - family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)
* Pstatus - parent's cohabitation status (binary: 'T' - living together or 'A' - apart)
* Medu - mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 – 5th to 9th grade, 3 – secondary education or 4 – higher education)
* Fedu - father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 – 5th to 9th grade, 3 – secondary education or 4 – higher education)
* Mjob - mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
* Fjob - father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
* reason - reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')
* guardian - student's guardian (nominal: 'mother', 'father' or 'other')
* traveltime - home to school travel time (numeric: 1 - 1 hour)
* studytime - weekly study time (numeric: 1 - 10 hours)
* failures - number of past class failures (numeric: n if 1<=n<3, else 4)
* schoolsup - extra educational support (binary: yes or no)
* famsup - family educational support (binary: yes or no)
* paid - extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)
* activities - extra-curricular activities (binary: yes or no)
* nursery - attended nursery school (binary: yes or no)
* higher - wants to take higher education (binary: yes or no)
* internet - Internet access at home (binary: yes or no)
* romantic - with a romantic relationship (binary: yes or no)
* famrel - quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
* freetime - free time after school (numeric: from 1 - very low to 5 - very high)
* goout - going out with friends (numeric: from 1 - very low to 5 - very high)
* Dalc - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
* Walc - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
* health - current health status (numeric: from 1 - very bad to 5 - very good)
* absences - number of school absences (numeric: from 0 to 93)

These grades are related with the course subject, Math or Portuguese:

* G1 - first period grade (numeric: from 0 to 20)
* G2 - second period grade (numeric: from 0 to 20)
* G3 - final grade (numeric: from 0 to 20, output target)

Entry and see the workflow that i used for the [project](https://github.com/renzoo123t/Predict-final-grade/blob/main/Predict%20final%20grade%20notebook.ipynb)

## Installation 

This project uses conda as a environment/package manager. To easily run this project in your machine, you should have ananconda or miniconda installed (You might want to refer to [Conda documentation](https://docs.conda.io/en/latest/index.html)). Alternatively, you can use your preferred method to install the required dependencies (`jupyter`, `NumPy`, `Pandas`, `Matplotlib`, `seaborn` and `scikitlearn`); use the versions stated in the environment.yml file to reproduce the same environment used for this project..

First, clone this repository to your machine:

```bash
gh repo clone renzoo123t/Predict-final-grade
```
### Using conda

Then, create the environment folder with the dependencies within the project directory:

```bash
conda env create --prefix ./env -f ./environment.yml
```

Activate the environment, with:

```bash
conda activate ./env
```

And finally, if dependencies are correctly installed, you should be able to run:

```bash
jupyter notebook
```
### Troubleshooting

When creating the enviroment, you may encounter `ResolvePackageNotFound` problem:

```bash
ResolvePackageNotFound:
  - dependencies not found
```
To solve the problem, move the problematic dependecies under pip section in the .yml file, like:

```yml
dependencies:
  - appnope=0.1.0=py38_0
  - attrs=19.3.0=py_0
  - backcall=0.1.0=py38_0
  - blas=1.0=mkl
  - bleach=3.1.4=py_0
  - ca-certificates=2020.6.24=0
  - certifi=2020.6.20=py38_0
  - cycler=0.10.0=py38_0
  - dbus=1.13.14=h517e14e_0
  - decorator=4.4.2=py_0
  - defusedxml=0.6.0=py_0
  ** all dependencies, except those not found **
  - pip:
    - jedi=0.17.0=py38_0
    - jinja2=2.11.2=py_0
    - joblib=0.15.1=py_0
    - jpeg=9b=he5867d9_2
    - jsonschema=3.2.0=py38_0
    - jupyter=1.0.0=py38_7
    - jupyter_client=6.1.3=py_0
    - jupyter_console=6.1.0=py_0
    - jupyter_core=4.6.3=py38_0
    - kiwisolver=1.2.0=py38h04f5b5a_0
    - libcxx=10.0.0=1
    - libedit=3.1.20181209=hb402a30_0
    - libffi=3.3=h0a44026_1
    - libgfortran=3.0.1=h93005f0_2
    - libiconv=1.16=h1de35cc_0
    - libpng=1.6.37=ha441bb4_0
    *** All dependencies not found ***
```

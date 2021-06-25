![PTQ](https://i.imgur.com/0D4Qvkt.png)

# :snake: PyToQlik

PyToQlik is a library that allows you to integrate Qlik Desktop with Jupyter notebooks. With it you can:

* Open and edit a Qlik app inside a Jupyter notebook;
* Create a Qlik object with data from a pandas DataFrame data structure and/or;
* Import data from a Qlik object and create a pandas DataFrame to work with in Python.

# :sparkles: Latest Updates 


## 24/jun/2021
:star2: Just added some basic Qlik Cloud SaaS functionalities! :star2:


Be a more powerful :bar_chart: **data scientist** by importing and extracting data from Qlik objects in Cloud applications inside your (:cloud:) tenant! 

## 25/jun/2021
:exclamation: Major revamp in verbose results and class hierarchy. PyToQlik should be way more stable and reliable! :exclamation:

# Getting Started

For this library to work you might want to have a functioning Qlik Desktop App installed and running on your local machine, or, if using the Cloud version, you will need an API Key to your tenant. There are tutorials on here and on Qlik's website about API Keys. You will also find having the *pandas* library useful, and either a [Jupyter Notebook local server](https://jupyter.readthedocs.io/en/latest/running.html) or use something like [Google Colaboratory](https://colab.research.google.com/).


You can then download and install PyToQlik using:

**Installation**
```
pip install pytoqlik 
```

## Usage

### Example 1

**Creating a Qlik app and feeding it data**
```
from pytoqlik import Pytoqlik
import seaborn

df = seaborn.load_dataset('tips')  # df is just some example data provided by the seaborn library

p2q = Pytoqlik()
app = p2q.toQlik(df)
```

### Example 2

**Importing data from a Qlik object to Python**
```
from pytoqlik import Pytoqlik
import seaborn

df = seaborn.load_dataset('tips')  # df is just some example data provided by the seaborn library

p2q = Pytoqlik()
app = p2q.toQlik(df)
app.toPy('your ObjectID')
```

## :feet: Step-by-step example
<img src="toPy.gif" />

# :books: Documentation

PyToQlik current documentation can be found [HERE](docs/Documentation.md).



# :notebook: Comprehensive Qlik Cloud tutorial

A case-study based tutorial has been developed and is available [HERE](docs/PyToQlik%20Cloud%20Tutorial.md).



# :computer: Features in development

## :earth_americas: Connectivity
- Qlik Enterprise authentication via *.pem* files
- Qlik Cloud robustness (easy-to-use embedding, more global functionality)

## :bulb: Planned Functionality
- Data fetching based on dimension and measure names
- More robust embedding objects and sheets
- Object creation and manipulation via Python
- Task creation and managing

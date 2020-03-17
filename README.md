[![Build Status](https://travis-ci.org/EISy-as-Py/eisy.svg?branch=master)](https://travis-ci.org/EISy-as-Py/eisy)
[![Documentation Status](https://readthedocs.org/projects/eisy-as-py/badge/?version=latest)](https://eisy-as-py.readthedocs.io/en/latest/?badge=latest)
[![Coverage Status](https://coveralls.io/repos/github/EISy-as-Py/eisy/badge.svg?branch=master)](https://coveralls.io/github/EISy-as-Py/eisy?branch=master)

# eisy
UW DIRECT DataScience Project, to Import/Process/Store/Report Data related to electrochemical impedance measurements. 

`eisy` is a Python module for simulating and classifying impedance data.

<img src=https://github.com/EISy-as-Py/eisy/blob/master/doc/project_management/misc_design/Logo3_square.PNG width=400 p align="right"> 

Using different combinations of circuit elements and their expression for impedance, the simulation module is able to reproduce the overall impedance response of the selected circuit. Look into the `circuit.py` page to see which configurations are already supported.
The `data_simulation.py` module allows to simulate the impedance response  in the frequency domain and saves the result as a `pandas.DataFrame` . The impedance response is  presented both in its complex form, as well as separated in its real and imaginary parts. Additionally, the `data_simulation.py` module allows for the creation of a .csv file containing metadata of the simuation just performed (i.e. circuit used, circuit elements values, etc.), as well as appending the raw data of the simulation. Finally, the simulation module provides option of generating a plot of the impdance respose. This can be generated for immediate inspection of the data trend, or saved automaticallyin a .png file having the same file name as the raw `.csv` file. 

An SQL database was created to preserv the simuation files produced and to allow for long term storage of electrochemical impedance spectroscopy data, as well as any data generate from future freatures added to the package. [ ## add more info on the database here ##]

Finally, `eisy` allows for a electrochemical impedance fingerprinting throught he euse of a *Convolutional Neural Network(CNN)*. Through the generation of simulated data, the network was trained and abtain ana ccuracy of ## Add number here!!##. The classification for now allows to differentialte between single semicircle responses, double semicircle response, impedance respone with a tail end. Addionally, noisy data can be classified and flagged as such. 


.. note::
  `eisy` is a new Python model and will be continuously updated as more feature are developed.

For any suggestions or request for specific features, plese visit the `eisy` [issue page](https://github.com/EISy-as-Py/eisy/issues) Otherwise, there is always the ooption of submitting a pull request `eisy` [pull request page](https://github.com/EISy-as-Py/eisy/pulls)

How to install `eisy`
--------------------------------

The package can be easiliy installed by executing the following commands: 

```
   pip install eisy
   
   conda install eisy (maybe?)
   
```

Dependencies
-------------------------

The following packages are required for using `eisy` 

- Python (>=3.5)
- SciPy (>=1.0)
- NumPy (>=1.14)
- Matplotlib (>=3.0)

Some notebooks are available in the `examples/` directory. In order to make use of them, `jupyter notebook` or alternatively `jupyter lab` will also be requred. 

More requirements can be found in the *requirements.txt* file. 

Future features
----------------------

The folloowing are implemetations that are planned for the `eisy` package:

* Expand the `plotting.py` module to include *bode plots*, as well as *DRT*
* Expand the `alterations.py` module to allow the simulation of *missing data points* and *interrupted data collection*. 
* Train the Neural Network to being able to cathegorize the above mentioned fetures. 
* Add a model fitting module to allow to predict the equivalent electrcal circuit fr experimental data
* Rewrite some of the modules to broaden their scope and be more inclusive in functionalities 

Suggestions of modifications or additions are welcomed and incoraged. File an issue [here](https://github.com/EISy-as-Py/eisy/issues)


## GIT Folder Structure
 * eisy
     * cnn
     * configuration
     * data
     * simulation
     * test
 * doc
     * project management     
 * examples
 
    LICENSE
    README.md
    requirements.txt
    setup.py
    .travis.yml
    environment.yml
 
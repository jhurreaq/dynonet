# dynoNet: a neural network architecture for learning of dynamical systems 

This repository contains the Python code to reproduce the results of the paper "dynoNet: a neural network architecture for learning of dynamical systems"

# Folders:
* [torchid](torchid):  PyTorch implementation of the linear dynamical operator (aka G-block in the paper) used in dynoNet
* [examples](examples): examples using dynoNet for system identification 
* [util](util): definition of metrics R-square, RMSE, fit index 

Three [examples](examples) discussed in the paper are:

* [WH2009](examples/WH2009): A circuit with Wiener-Hammerstein behavior. Experimental dataset from http://www.nonlinearbenchmark.org
* [BW](examples/BW): Bouc-Wen. A nonlinear dynamical system describing hysteretic effects in mechanical engineering. Experimental dataset from http://www.nonlinearbenchmark.org
* [EMPS](examples/EMPS): A controlled prismatic joint (Electro Mechanical Positioning System). Experimental dataset from http://www.nonlinearbenchmark.org

For the [WH2009](examples/WH2009) example, the main scripts are:

 *  ``WH2009_train.py``: Training of the dynoNet model on the training dataset
 *  ``WH2009_test.py``: Testing of the dynoNet model on the test dataset, computation of metrics.
  
Similar scripts are provided for the other examples.

NOTE: the original data sets are not included in this project. They have to be manually downloaded from
http://www.nonlinearbenchmark.org and copied in the data sub-folder of the example.
# Software requirements:
Simulations were performed on a Python 3.7 conda environment with

 * numpy
 * scipy
 * matplotlib
 * pandas
 * pytorch (version 1.4)
 
These dependencies may be installed through the commands:

```
conda install numpy scipy pandas matplotlib
conda install pytorch torchvision cudatoolkit=10.2 -c pytorch
```
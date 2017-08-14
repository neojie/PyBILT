# PyBILT
------
![Python version badge](https://img.shields.io/badge/python-2.7-blue.svg)
[![GitHub license](https://img.shields.io/github/license/Day8/re-frame.svg)](LICENSE)
[![Code Health](https://landscape.io/github/blakeaw/PyBILT/master/landscape.svg?style=flat)](https://landscape.io/github/blakeaw/PyBILT/master)
[![docstring-coverage badge](https://img.shields.io/badge/docstring--coverage-38.9%25-orange.svg)](.docstring-coverage_report.txt)
------
## *Py*thon based lipid *BIL*ayer analysis *T*oolkit
------
![alt text](./_images/7percentCL_sideview_b.jpg "Lipid Bilayer")
#### PyBILT is a Python toolkit developed to analyze molecular simulation trajectories of lipid bilayers systems. The toolkit includes a variety of analyses from various lipid bilayer molecular simulation publications.

The analyses include:
   * Mean Squared Displacement (MSD)
   * Diffusion coefficent estimators (from MSD curves) - includes Einstein relation, linear fit, and anomalous diffusion fit.
   * Area per lipid estimators
   * Bilayer thickness
   * Displacement Vector (flow) maps and correlations
   * Deuterium order parameter
   * Orientation parameters
   * Mass and Electron Density Estimators
   * and more!

------

### Install

#### Warning: PyBILT is still under heavy development and may rapidly change.

Download PyBILT from the github repo (https://github.com/blakeaw/PyBILT.git)
and then add the path to the PyBILT directory to your PYTHONPATH. From a
terminal you can type
```
export PYTHONPATH="path_to/PyBILT:$PYTHONPATH
```
to add it to the current shell environment. For persistence add the line to your
.bashrc file.

PyBILT has the following major dependencies:
   * MDAnalysis 0.16.0
   * NumPy  1.11.3
   * SciPy 0.18.1,
   * Matplotlib 2.0.0
   * Seaborn 0.7.1


In addition, it is highly recommended that you install
[Anaconda Python](https://www.continuum.io/)
version 4.3.1 Python 2.7 before installing PyBILT. PyBILT
has yet to be tested outside of an Anaconda environment.

------

#### Setup using Anaconda's conda tool
The file environment.yml has been provided to allow for easy setup of a new
environment with all the appropriate dependencies using the conda tool. Run
```
conda env create -f environment.yml
```
which will create a new conda environment named *pybilt* with the appropriate
dependencies. Then activate the environment
```
source activate pybilt
```
before running PyBILT modules.

------

#### Quick overview of PyBILT
**PyBILT** is composed of 5 major modules:
  * bilayer_analyzer -- The bilayer_analyzer is the primary analysis module.
                        This object has the most comprehensive set of built-in
                        features (types of analyses and use of different bilayer
                        representations) and makes use of much of the
                        functionality from proceeding modules.  
  * mda_tools -- This module has various sets of functions for directly
                 analyzing and operating on MDAnalysis trajectories and objects.
                 e.g. functions to compute density profiles.
  * lipid_grid -- The lipid grid module can be used construct "lipid grid" grid
                  representations of lipid bilayers, which can be used to
                  accurately estimate quantities such as area per lipid.
  * com_trajectory -- This module can be used to construct a center of mass
                      trajectory (COMTraj) out of an MDAnalysis trajectory,
                      which is useful for computing quantities like mean squared
                      displacement.
  * plot_generation -- This module has several pre-written plotting functions
                       (using matplotlib and seaborn) for some of the properties
                       that can be computed from functions in the other modules.
                       e.g. mean squared displacement and area per lipid.

## Documentation

Detailed documentation for PyBILT is in the pipeline. There are currently a
few Jupyter IPython [notebooks](jupyter_notebooks) that provide some examples and show some basic usage. More of these are also in the pipeline. Although they are also not fully extensive, the [tests](tests) can serve as a useful place to examine some basic usage and functionality.

## Authors

* **Blake A Wilson** - *Initial work* - Currently a Postdoctoral Fellow at Vanderbilt University
  * Vandy e-mail: blake.a.wilson@vanderbilt.edu
  * Gmail: blakeaw1102@gmail.com
  * [Blake's VU Website]( https://my.vanderbilt.edu/blakeaw/)
  * Also find me on [LinkedIn](https://www.linkedin.com/in/blakewilson3/) and [Research Gate](https://www.researchgate.net/profile/Blake_Wilson3)

## Contact

If you have any comments, suggestions, or feature requests for PyBILT please feel free to open a GitHub Issue (https://github.com/blakeaw/PyBILT/issues) with those comments, suggestions, or feature requests. Or you can contact Blake directly via e-mail at either blake.a.wilson@vanderbilt.edu or blakeaw1102@gmail.com. You may also contact Blake with any questions about PyBILT use or implementation.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* A special thanks to James Pino (https://github.com/JamesPino) for his inciteful comments and suggestions that have helped improve the quality of this code, and thanks to him for pointing out some very useful coding tools.   
* Thanks to my advisors, Carlos F. Lopez and Arvind Ramanathan, for catalyzing this project and for providing me with the space and means to pursue it.    
* Thanks to the developers of Landscape (https://landscape.io/), which has proved to be a powerful tool for improving the quality of this projects code.

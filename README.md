# A Network Tour of Data Science, edition 2018

[![Binder](https://mybinder.org/badge.svg)][binder_lab]
&nbsp; (Jupyter [lab][binder_lab] or [notebook][binder_notebook])

[binder_lab]: https://mybinder.org/v2/gh/mdeff/ntds_2018/outputs?urlpath=lab
[binder_notebook]: https://mybinder.org/v2/gh/mdeff/ntds_2018/outputs?urlpath=tree

This repository contains the material for the labs associated with the EPFL
master course [EE-558 A Network Tour of Data Science][epfl] ([moodle]), taught
in fall 2018. The content is similar to the [2017 edition]. Compared to the
[2016 edition], the course has been refocused on graph and network sciences.
The course material revolves around the following topics:

1. [Network Science](https://en.wikipedia.org/wiki/Network_science),
1. [Spectral Graph Theory](https://en.wikipedia.org/wiki/Spectral_graph_theory),
1. [Graph Signal Processing](https://arxiv.org/abs/1211.0053),
1. [Machine Learning](https://en.wikipedia.org/wiki/Machine_learning).

[epfl]: http://edu.epfl.ch/coursebook/en/a-network-tour-of-data-science-EE-558
[moodle]: http://moodle.epfl.ch/course/view.php?id=15299
[2016 edition]: https://github.com/mdeff/ntds_2016
[2017 edition]: https://github.com/mdeff/ntds_2017

Below is the material you'll find in that repository:
1. Practical information
1. [Installation instructions](#usage)
1. Introduction: [conda] & [anaconda], [python], [jupyter], [git]
1. Numerical computation with [numpy] and [scipy]
1. Data visualization with [matplotlib]
1. Data exploration with [pandas]
1. Network science with [networkx]
1. Graph signal processing with [pygsp]
1. Concluding remarks

As a Data Science course, the above activities are realized on real networks,
e.g. a social network from Twitter, that students have to collect and clean
themselves.

[conda]: https://conda.io
[anaconda]: https://anaconda.org
[python]: https://www.python.org
[jupyter]: http://jupyter.org
[git]: https://git-scm.com
[numpy]: http://www.numpy.org
[scipy]: https://www.scipy.org
[matplotlib]: https://matplotlib.org
[pandas]: https://pandas.pydata.org
[networkx]: https://networkx.github.io
[pygsp]: http://pygsp.readthedocs.io

## Projects

This year, the whole course is evaluated by a project (see the description),
proposed and carried out by groups of three to four students. The students had
to deliver four milestones, following the theory seen in class:
1. Network properties: measure and interpret some properties of your network
1. Network models: fit some relevant network models and comment on their fitness
1. Spectral graph theory: visualize or cluster your graph using the spectrum of the graph Laplacian
1. Graph signal processing: analyze data on your graph

Below is their work.

## Usage

Click the [binder badge][binder_lab] to play with the notebooks from your
browser without installing anything.

For a local installation, you will need [git], [Python], and packages from the
[Python scientific stack][scipy]. If you don't know how to install those on
your platform, we recommend to install [Miniconda], a distribution of the
[conda] package and environment manager. Please follow the below instructions
to install it and create an environment for the course.

1. Download the Python 3.x installer for Windows, macOS, or Linux from
   <https://conda.io/miniconda.html> and install with default settings. Skip
   this step if you have conda already installed (from [Miniconda] or
   [Anaconda]). Linux users may prefer to use their package manager.
   * Windows: Double-click on the `.exe` file.
   * macOS: Run `bash Miniconda3-latest-MacOSX-x86_64.sh` in your terminal.
   * Linux: Run `bash Miniconda3-latest-Linux-x86_64.sh` in your terminal.
1. Open a terminal. Windows: open the Anaconda Prompt from the Start menu.
1. Install git with `conda install git`.
1. Download this repository by running
   `git clone https://github.com/mdeff/ntds_2018`.
1. Create an environment with the packages required for the course with
   `conda env create -f ntds_2018/environment.yml`.

Every time you want to work, do the following:

1. Open a terminal. Windows: open the Anaconda Prompt from the Start menu.
1. Activate the environment with `conda activate ntds_2018`
   (or `activate ntds_2018`, or `source activate ntds_2018`).
1. Start Jupyter with `jupyter notebook` or `jupyter lab`. The command should
   open a new tab in your web browser.
1. Edit and run the notebooks from your browser.

[git]: https://git-scm.com
[python]: https://www.python.org
[scipy]: https://www.scipy.org
[anaconda]: https://anaconda.org
[miniconda]: https://conda.io/miniconda.html
[conda]: https://conda.io
[conda-forge]: https://conda-forge.org

## Team

* Instructors:
[Pierre Vandergheynst](https://people.epfl.ch/pierre.vandergheynst),
[Pascal Frossard](https://people.epfl.ch/pascal.frossard).
* Assistants:
[Michaël Defferrard](http://deff.ch),
[Hermina Petric Maretic](https://people.epfl.ch/hermina.petricmaretic),
[Effrosyni Simou](https://people.epfl.ch/effrosyni.simou),
[Rodrigo Pena](https://rodrigo-pena.github.io),
[Benjamin Ricaud](https://people.epfl.ch/benjamin.ricaud),
[Eda Bayram](https://people.epfl.ch/eda.bayram).

## License

The content is released under the terms of the [MIT License](LICENSE.txt).

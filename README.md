# A Network Tour of Data Science, edition 2018

[![Binder](https://mybinder.org/badge_logo.svg)][binder_lab]
&nbsp; (Jupyter [lab][binder_lab] or [notebook][binder_notebook])

[binder_lab]: https://mybinder.org/v2/gh/mdeff/ntds_2018/outputs?urlpath=lab
[binder_notebook]: https://mybinder.org/v2/gh/mdeff/ntds_2018/outputs?urlpath=tree

This repository contains the material for the practical work associated with the EPFL
master course [EE-558 A Network Tour of Data Science][epfl] ([moodle]), taught
in fall 2018. The content is similar to the [2017 edition]. Compared to the
[2016 edition], the course has been refocused on graph and network sciences.
The course material revolves around the following topics:

1. [Network Science](https://en.wikipedia.org/wiki/Network_science),
1. [Spectral Graph Theory](https://en.wikipedia.org/wiki/Spectral_graph_theory),
1. [Graph Signal Processing](https://arxiv.org/abs/1211.0053),
1. [Data Science](https://en.wikipedia.org/wiki/Data_science),
1. [Machine Learning](https://en.wikipedia.org/wiki/Machine_learning).

Theoretical knowledge is taught during lectures.
Practical knowledge is taught through [tutorials](#tutorials).
Both are practiced and evaluated through a [semester project](#projects).
Below are slides about the organization of the course.

1. [Course organization][practical_info]
1. [Project expectations][projects]
1. Concluding remarks

[epfl]: http://edu.epfl.ch/coursebook/en/a-network-tour-of-data-science-EE-558
[moodle]: http://moodle.epfl.ch/course/view.php?id=15299
[2016 edition]: https://github.com/mdeff/ntds_2016
[2017 edition]: https://github.com/mdeff/ntds_2017

[practical_info]: https://github.com/mdeff/ntds_2018/blob/outputs/slides/ntds_info.pdf
[projects]: https://github.com/mdeff/ntds_2018/blob/outputs/slides/ntds_projects.pdf

## Tutorials

Below is the teaching material you'll find in this repository.

1. [Installation instructions](#installation)
1. [Introduction][t01]
1. [Building graphs from edge lists][t02a]
1. [Building graphs from features][t02b]
1. [Plotting with matplotlib][t03]
1. [Interactive graph visualization with gephi][t04]
1. [Sparse matrices with scipy][t05]
1. [Linear algebra for graphs and networkx][t06]
1. [Graph signal processing with pygsp][t07]

[t01]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/01_introduction.ipynb
[t02a]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/02a_graph_from_edge_list.ipynb
[t02b]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/02b_graph_from_features.ipynb
[t03]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/03_matplotlib.ipynb
[t04]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/04_graph_visualization.ipynb
[t05]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/05_scipy_sparse.ipynb
[t06]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/06_linalg_and_networkx.ipynb
[t07]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/tutorials/07_pygsp.ipynb

For this course, we'll introduce and use the following tools:
[conda] & [anaconda], [python], [jupyter], [git], [numpy], [scipy], [matplotlib], [pandas], [networkx], [graph-tool], [pygsp], [gephi].

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
[graph-tool]: https://graph-tool.skewed.de
[pygsp]: http://pygsp.readthedocs.io
[gephi]: https://gephi.org

## Projects

During the course of a semester project, students exercise the theory seen in class on real data and networks.
Projects are carried out by groups of four students, and are to be chosen in the list of [proposed projects](projects).
The students have to deliver four milestones, following the theory seen in class:

1. [Network properties][m1]: measure and interpret some properties of the network.
   [Best student solution][s1].
1. [Network models][m2]: fit some relevant network models and comment on their fitness.
   [Best student solution][s2].
1. [Spectral graph theory][m3]: visualize and cluster the network using the spectrum of the graph Laplacian.
   [Best student solution][s3].
1. [Graph signal processing][m4]: analyze data (signals, features) on the graph.
   [Best student solution][s4].

[m1]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/1_network_properties.ipynb
[s1]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/1_network_properties_student_solution.ipynb
[m2]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/2_network_models.ipynb
[s2]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/2_network_models_student_solution.ipynb
[m3]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/3_spectral_graph_theory.ipynb
[s3]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/3_spectral_graph_theory_student_solution.ipynb
[m4]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/4_graph_signal_processing.ipynb
[s4]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/milestones/4_graph_signal_processing_student_solution.ipynb

After completing those milestones, they are free to pursue any other direction of interest.
Those data projects are meant to jointly practice and evaluate their theoretical network analysis skills and practical Data Science skills.

Below is the work of the 180 students enrolled that year.

![projects](projects/projects.jpg)

* [[report][r01], [slides][s01], [code][c01]] A Network Analysis of Movie Popularity
* [[report][r02], [slides][s02], [code][c02]] Learning US Senate voting behavior from bill sponsorship profiles
* [[report][r03], [slides][s03], [code][c03]] Retrieving the continent labels from the air routes structure
* [[report][r04], [slides][s04], [code][c04]] Evolution of the movie industry
* [[report][r05], [slides][s05], [code][c05]] A network tour to flight delay in the US
* [[report][r06], [slides][s06], [code][c06]] Flight network and airline alliances
* [[report][r07], [slides][s07], [code][c07]] Vote prediction of US Senators from graph properties
* [[report][r08], [slides][s08], [code][c08]] Spreading disease through the air
* [[report][r09], [slides][s09], [code][c09]] A Network Analysis of the 2018 FIFA World Cup
* [[report][r10], [slides][s10], [code][c10]] History of Movie Success through GSP
* [[report][r11], [slides][s11], [code][c11]] Music Genre Recognition
* [[report][r12], [slides][s12], [code][c12]] Finding Continents from a Flight Routes Network
* [[report][r13], [slides][s13], [code][c13]] Conversation starter using Wikipedia
* [[report][r14], [slides][s14], [code][c14]] Smooth Radio: Automatic playlist generation using signal graph processing
* [[report][r15], [slides][s15], [code][c15]] Movie Grossing Success Prediction with Convolutional Neural Networks on Graphs
* [[report][r16], [slides][s16], [code][c16]] How to invest in movies?
* [[report][r17], [slides][s17], [code][c17]] A Netflix Tour of Data Science — Film suggestion by diffusion on graphs
* [[report][r18], [slides][s18], [code][c18]] U.S. Senators: A Voting Pattern Study
* [[report][r19], [slides][s19], [code][c19]] A Data Study of Terrorism and its Tendencies
* [[report][r20], [slides][s20], [code][c20]] Spammer… Catch me if you can
* [[report][r21], [slides][s21], [code][c21]] Exposing the True Terrorist Network
* [[report][r22], [slides][s22], [code][c22]] Small Components' Analysis and Flight Delay Prediction
* [[report][r23], [slides][s23], [code][c23]] Minipedia
* [[report][r24], [slides][s24], [code][c24]] Wikipedia Analysis Using Keyword Based Graphs
* [[report][r25], [slides][s25], [code][c25]] Finding the Authors of a Terrorist Attack
* [[report][r27], [slides][s27], [code][c27]] How to beat terrorism efficiently: identification of set of key players in terrorist networks
* [[report][r28], [slides][s28], [code][c28]] A Network Topology Analysis of the Airline Industry
* [[report][r29], [slides][s29], [code][c29]] Predicting Terror Attacks — A Data Story
* [[report][r30], [slides][s30], [code][c30]] Free Music Alternative Playlists
* [[report][r31], [slides][s31], [code][c31], [proposal][p31]] Feminism in Hollywood
* [[report][r32], [slides][s32], [code][c32]] Genre Classification: A Transductive, Inductive and Deep Approach
* [[report][r33], [slides][s33], [code][c33]] Friends Will Be Friends: A Network Tour of Musical Friendship
* [[report][r34], [slides][s34], [code][c34]] Predicting the nature of terrorist attacks
* [[report][r36], [slides][s36], [code][c36]] Transitional playlists for new musical discoveries
* [[report][r37], [slides][s37], [code][c37]] A Wikipedia Tour of Death — or how University College Boat Club became popular
* [[report][r38], [slides][s38], [code][c38]] Tempering the Spread of Epidemics on Aerial Networks
* [[report][r40], [slides][s40], [code][c40]] Can we estimate the earnings of a movie?
* [[report][r42], [slides][s42], [code][c42]] Re-balancing flight routes inequalities
* [[report][r44], [slides][s44], [code][c44], [proposal][p44]] Voting patterns in the Swiss National Council
* [[report][r47], [slides][s47], [code][c47]] An overviews of intercontinental flight route connections
* [[report][r49], [slides][s49], [code][c49]] A Network Tour of Millenial Movies
* [[report][r50], [slides][s50], [code][c50]] Identifying Spammers on Social Networks
* [[report][r51], [slides][s51], [code][c51], [proposal][p51]] An exploratory study on the brain dysconnectome
* [[report][r52], [slides][s52], [code][c52]] Mood Changing Playlist Generator
* [[report][r54], [slides][s54], [code][c54]] Fight Against Terrorism

As each team stored their code in a github repository, all their code can conveniently be downloaded with `git clone --recurse-submodules https://github.com/mdeff/ntds_2018`.
One folder per team will be populated in `projects/code`.

[p31]: projects/proposals/team_31.pdf
[p44]: projects/proposals/team_44.pdf
[p51]: projects/proposals/team_51.pdf

[r01]: projects/reports/team_01.pdf
[r02]: projects/reports/team_02.pdf
[r03]: projects/reports/team_03.pdf
[r04]: projects/reports/team_04.pdf
[r05]: projects/reports/team_05.pdf
[r06]: projects/reports/team_06.pdf
[r07]: projects/reports/team_07.pdf
[r08]: projects/reports/team_08.pdf
[r09]: projects/reports/team_09.pdf
[r10]: projects/reports/team_10.pdf
[r11]: projects/reports/team_11.pdf
[r12]: projects/reports/team_12.pdf
[r13]: projects/reports/team_13.pdf
[r14]: projects/reports/team_14.pdf
[r15]: projects/reports/team_15.pdf
[r16]: projects/reports/team_16.pdf
[r17]: projects/reports/team_17.pdf
[r18]: projects/reports/team_18.pdf
[r19]: projects/reports/team_19.pdf
[r20]: projects/reports/team_20.pdf
[r21]: projects/reports/team_21.pdf
[r22]: projects/reports/team_22.pdf
[r23]: projects/reports/team_23.pdf
[r24]: projects/reports/team_24.pdf
[r25]: projects/reports/team_25.pdf
[r27]: projects/reports/team_27.pdf
[r28]: projects/reports/team_28.pdf
[r29]: projects/reports/team_29.pdf
[r30]: projects/reports/team_30.pdf
[r31]: projects/reports/team_31.pdf
[r32]: projects/reports/team_32.pdf
[r33]: projects/reports/team_33.pdf
[r34]: projects/reports/team_34.pdf
[r36]: projects/reports/team_36.pdf
[r37]: projects/reports/team_37.pdf
[r38]: projects/reports/team_38.pdf
[r40]: projects/reports/team_40.pdf
[r42]: projects/reports/team_42.pdf
[r44]: projects/reports/team_44.pdf
[r47]: projects/reports/team_47.pdf
[r49]: projects/reports/team_49.pdf
[r50]: projects/reports/team_50.pdf
[r51]: projects/reports/team_51.pdf
[r52]: projects/reports/team_52.pdf
[r54]: projects/reports/team_54.pdf

[s01]: projects/slides/team_01.pdf
[s02]: projects/slides/team_02.pdf
[s03]: projects/slides/team_03.pdf
[s04]: projects/slides/team_04.pdf
[s05]: projects/slides/team_05.pdf
[s06]: projects/slides/team_06.pdf
[s07]: projects/slides/team_07.pdf
[s08]: projects/slides/team_08.pdf
[s09]: projects/slides/team_09.pdf
[s10]: projects/slides/team_10.pdf
[s11]: projects/slides/team_11.pdf
[s12]: projects/slides/team_12.pdf
[s13]: projects/slides/team_13.pdf
[s14]: projects/slides/team_14.pdf
[s15]: projects/slides/team_15.pdf
[s16]: projects/slides/team_16.pdf
[s17]: projects/slides/team_17.pdf
[s18]: projects/slides/team_18.pdf
[s19]: projects/slides/team_19.pdf
[s20]: projects/slides/team_20.pdf
[s21]: projects/slides/team_21.pdf
[s22]: projects/slides/team_22.pdf
[s23]: projects/slides/team_23.pdf
[s24]: projects/slides/team_24.pdf
[s25]: projects/slides/team_25.pdf
[s27]: projects/slides/team_27.pdf
[s28]: projects/slides/team_28.pdf
[s29]: projects/slides/team_29.pdf
[s30]: projects/slides/team_30.pdf
[s31]: projects/slides/team_31.pdf
[s32]: projects/slides/team_32.pdf
[s33]: projects/slides/team_33.pdf
[s34]: projects/slides/team_34.pdf
[s36]: projects/slides/team_36.pdf
[s37]: projects/slides/team_37.pdf
[s38]: projects/slides/team_38.pdf
[s40]: projects/slides/team_40.pdf
[s42]: projects/slides/team_42.pdf
[s44]: projects/slides/team_44.pdf
[s47]: projects/slides/team_47.pdf
[s49]: projects/slides/team_49.pdf
[s50]: projects/slides/team_50.pdf
[s51]: projects/slides/team_51.pdf
[s52]: projects/slides/team_52.pdf
[s54]: projects/slides/team_54.pdf

[c01]: https://github.com/illorens/Project_NTDS
[c02]: https://github.com/roman-bachmann/US-Senators
[c03]: https://github.com/AmauV/NTDS
[c04]: https://github.com/swouf/ntds_IMDb_team4
[c05]: https://github.com/yf0726/ntds_project
[c06]: https://github.com/nicolasFontbonne/Project_ntds
[c07]: https://github.com/magoncal/NTDS_Project
[c08]: https://github.com/dsalathe/group_ntds
[c09]: https://github.com/ProjectNTDS/Network_World_Cup_Analysis
[c10]: https://github.com/hugofluhr/Team10_ntds_2018
[c11]: https://github.com/angomez/ntds
[c12]: https://github.com/franckdess/NTDS_Project
[c13]: https://github.com/okhofsk/NTDS_Wikipedia
[c14]: https://github.com/padesplaces/ntds_project
[c15]: https://github.com/mcherep/ntds-epfl
[c16]: https://github.com/GentleDell/IMDb_movie_analysis
[c17]: https://github.com/PierreFourcade/A-Netflix-Tour-of-Data-Science---Film-suggestion-by-diffusion-on-graphs
[c18]: https://github.com/lkieliger/US-Senators
[c19]: https://github.com/AminMekacher/NTDS_Team19
[c20]: https://github.com/mfendri2/NTDS_Project_Team20
[c21]: https://github.com/sinyil/ntds_2018_Final_Project
[c22]: https://github.com/sami2310/NTDS_Project_team22
[c23]: https://github.com/Ivo-A/Team23_Wikipedia
[c24]: https://github.com/mattminder/wikilinks
[c25]: https://github.com/yusiZou/NTDS_project
[c27]: https://github.com/natbolon/terrorist_network_weaknesses
[c28]: https://github.com/rusucosmin/ntp
[c29]: https://github.com/Axeln78/TerrorAttacksNtds
[c30]: https://github.com/TTimTT/FMAP
[c31]: https://github.com/othmanbck/ntds_project_2018
[c32]: https://github.com/senakicir/ntds_project
[c33]: https://github.com/JCrobe/NTDS19_FWBF
[c34]: https://github.com/coencharles/NTDS_team34
[c36]: https://github.com/Team36-ntds2018/Project_free_music_archives_2018
[c37]: https://github.com/isabelaconstantin/wikinet
[c38]: https://github.com/montalex/NTDS_2018_Final_Project
[c40]: https://github.com/rocari96/NTDS-project
[c42]: https://github.com/VincentCoriou/Re-balancing-flight-routes-inequalities
[c44]: https://github.com/nikolaiorgland/conseil_national
[c47]: https://github.com/FrankSchmutz/NTDS2019FinalProject
[c49]: https://github.com/MilenaFilipovic/NTDS_Project_Team_49
[c50]: https://github.com/ilijagjorgjiev/project_ntds
[c51]: https://github.com/emullier/NTDS_team51_BrainNetworks
[c52]: https://github.com/rezaho/NetworkTour-of-DataScience
[c54]: https://github.com/mouadhhamdi/NTDS_Project

## Installation

Click the [binder badge][binder_lab] to play with the notebooks from your
browser without installing anything.

For a local installation, you will need [git], [Python], and packages from the [Python scientific stack][scipy].
If you don't know how to install those on your platform, we recommend to install [Miniconda] or [Anaconda], a distribution of the [conda] package and environment manager.
Follow the below instructions to install it and create an environment for the course.

1. Download the Python 3.x installer for Windows, macOS, or Linux from
   <https://conda.io/miniconda.html> and install with default settings. Skip
   this step if you have conda already installed (from [Miniconda] or
   [Anaconda]). Linux users may prefer to use their package manager.
   * Windows: Double-click on `Miniconda3-latest-Windows-x86_64.exe`.
   * macOS: Run `bash Miniconda3-latest-MacOSX-x86_64.sh` in your terminal.
   * Linux: Run `bash Miniconda3-latest-Linux-x86_64.sh` in your terminal.
1. Open a terminal. Windows: open the Anaconda Prompt from the Start menu.
1. Install git with `conda install git`.
1. Navigate to the folder where you want to store the course material with `cd path/to/ntds`.
   Windows users may need `\` instead of `/` as the path separator.
1. Download this repository with `git clone https://github.com/mdeff/ntds_2018`.
1. Enter the repository with `cd ntds_2018`.
1. Create an environment with the packages required for the course with
   `conda env create -f environment.yml`.
1. If everything went fine, you should be able to run the [`test_install.ipynb`][test_install] notebook after following the above steps.

[test_install]: https://nbviewer.jupyter.org/github/mdeff/ntds_2018/blob/outputs/test_install.ipynb

Every time you want to work, do the following:

1. Open a terminal. Windows: open the Anaconda Prompt from the Start menu.
1. Activate the environment with `conda activate ntds_2018`
   (or `activate ntds_2018`, or `source activate ntds_2018`).
1. Navigate to the folder where you stored the course material with `cd path/to/ntds_2018`.
1. Start Jupyter with `jupyter notebook` or `jupyter lab`. The command should
   open a new tab in your web browser.
1. Edit and run the notebooks from your browser.

[git]: https://git-scm.com
[python]: https://www.python.org
[scipy]: https://www.scipy.org
[anaconda]: https://www.anaconda.com/download
[miniconda]: https://conda.io/miniconda.html
[conda]: https://conda.io
[conda-forge]: https://conda-forge.org

## Team

* Instructors:
[Pierre Vandergheynst](https://people.epfl.ch/pierre.vandergheynst),
[Pascal Frossard](https://people.epfl.ch/pascal.frossard).
* Assistants:
[Michaël Defferrard](http://deff.ch),
[Hermina Petric Maretić](https://people.epfl.ch/hermina.petricmaretic),
[Effrosyni Simou](https://people.epfl.ch/effrosyni.simou),
[Rodrigo Pena](https://rodrigo-pena.github.io),
[Benjamin Ricaud](https://github.com/bricaud),
[Eda Bayram](https://people.epfl.ch/eda.bayram).
* Invited lecturers:
[Kirell Benzi](https://www.kirellbenzi.com),
[Dorina Thanou](https://people.epfl.ch/dorina.thanou),
[Michaël Defferrard](http://deff.ch).

## License

The content is released under the terms of the [MIT License](LICENSE.txt).

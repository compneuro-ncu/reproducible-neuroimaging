================
Code management 
================

Neuroimaging data analysis involves a code that allows interpretation and validation of the results as well as solving new research questions. 
That is why you should think about code in case of reproducibility either. 
Most researchers are not trained in software engineering which often causes undocumented code, but still sharing undocumented code is much better 
than not sharing at all. (Gorgolewski et al. 2016) 

Although, we aim to provide the most optimal scientific practices in which data science code quality is about correctness and reproducibility. 
Starting with a fairly standardized setup provides a clean, logical structure of the code.

Version control system
-----------------------

Version control system (VSC) is a class of systems responsible for managing changes to any collections 
of information such as computer programs or documentation over time. 

`Git <https://git-scm.com/>`_ is the most popular version control system which allows efficient source code management. There are its basic features:

  * **saving the history of changes**, where each of them have a title, comment, contributor information and the date of change; it allows direct insight into the changes that have occurred in the source files; 

  * **code branching** that is the ability to developing new program functions independently of each other; the main branch allows to have a stable version of the program, and the independent remaining branches allow to test new solutions; changes taking place in branches can be removed or implemented directly into the source;

  * **Git remote repository** allows to work on a project backup that forms the basis of teamwork; each contributor has a local version on their device, which can be linked to its remote version;

  * the ability of **offline working** on personal device.

.. image:: img/git.png
  :height: 535
  :width: 1280
  :scale: 10%
  :align: center
  :alt: Alternative text

Git in conjunction with services such as `GitHub.com <https://github.com/>`_ allows the entire community of developers to engage in the development of shared software and help eliminate unnoticed errors. So what exactly is GitHub? Basically, it is a platform providing free hosting for open source programs and private repositories for sharing code. 

.. image:: img/github.png
  :height: 465
  :width: 1150
  :scale: 10%
  :align: center
  :alt: Alternative text

.. note:: Every developer (both professional and non-professional) should be able to work with version control systems!

Makefiles
-----------

Automation with scripts improves processing when parameters are modified in the course of the project and time-consuming processing steps have to be repeated.

The created program of neuroimaging data analysis will consist of several source files. 
If you want to show the program to other users, we have to create an elegant way to compile our program. 
**Make** enables you to express your workflow backwards as dependencies between files.

**Makefiles** are machine-readable documentation capturing your workflow in a machine-readable format with 100 % chances to pass the effectiveness tests. 
**Make** is a rigorous way of recording each step in the process, enabling you (and your coworkers) to reproduce the entire process later. 

Code folder structure
----------------------

Even written and organized code is of no reuse, unless others have access to proper documentation and information describing what and where something is 
actually stored in the repository. Clear folder structure and documentation within a repository are needed to make use of information. 

A form of self-documentation differs among each researcher and to simplify the whole process we managed to create our own code folder structure with
proper description which may solve the problem. 

│   .gitignore
│   Dockerfile
│   environment.yml
│   LICENSE
│   README.rst
│
├───analysis
│   │   requirements.md
│   │
│   ├───01-behavioral
│   │       README-behavioral.rst
│   │
│   ├───02-preprocessing
│   │       fmriprep_command.sh
│   │       README-preprocessing.rst
│   │
│   ├───03-modeling
│   │       predict_model.py
│   │       README-modeling.md
│   │
│   └───04-visualization
│       │   visualize.py
│       │
│       └───figures
│               Fig1-connectivity.png
│
├───data
│   │   README-data_description.md
│   │
│   ├───01-raw
│   ├───02-processed
│   └───03-cleaned
├───docs
│   │   make.bat
│   │   Makefile
│   │
│   └───source
│           conf.py
│           index.rst
│
├───notebooks
│       jupyter.ipynb
│
└───utils
        plotting.py

If you are interested in using our template, visit our `GitHub page <https://github.com/compneuro-ncu/project-name-template>`_. 

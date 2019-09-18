# State Species of Greatest Conservation Need

## Provisional Software Statement

Under USGS Software Release Policy, the software codes here are considered preliminary, not released officially, and posted to this repo for informal sharing among colleagues.

This software is preliminary or provisional and is subject to revision. It is being provided to meet the need for timely best science. The software has not received final approval by the U.S. Geological Survey (USGS). No warranty, expressed or implied, is made by the USGS or the U.S. Government as to the functionality of the software and related material nor shall the fact of release constitute any such warranty. The software is provided on the condition that neither the USGS nor the U.S. Government shall be held liable for any damages resulting from the authorized or unauthorized use of the software.

## Overview

After some recent work on other species lists, we are revisiting the process for working through the lists of Species of Greatest Conservation Need submitted by US States and Territories. This repository contains the thinking for how that process should run that we will adapt for live cyberinfrastructure as we get the system refined.

State SGCN lists are submitted to the USGS in partnership with the Association of Fish and Wildlife Agencies (AFWA). 2005 lists were assembled by parsing names from State Wildlife Action Plans with some inherent issues in accuracy. For 2015 and beyond, States and Territorries are submitting spreadsheets of their species lists with some variation in the format and contents. The lists are all stored in the ScienceBase Repository under a [single collection](https://www.sciencebase.gov/catalog/item/56d720ece4b015c306f442d5).

The process explored in this repository is based in Python code through Jupyter Notebooks. Data are sourced from the files in ScienceBase and are processed through logic in our provisional software package, [bispy](https://github.com/usgs-bcb/bispy). The codes are all based on open data and methods. If you want to run the code yourself, you will need to install the bispy package and other necessary dependencies. It is recommended that you run the system in a clean virtual environment. We use Anaconda, so that process looks something like the following:

conda create --name sgcn
conda install -c conda-forge jupyter pip
pip install git+git://github.com/usgs-bcb/bispy

This is not meant as an operational codebase but as a set of notes and processing logic we are exploring for how to conduct the work of synthesizing a common national list of SGCN species. The notebooks explain our thinking about the process and the decisions we are making about how to assemble the list.

The data files in the repository contain the processing results we have decided to cache as we continue exploration. The destination for this toolset is a cyberinfrastructure we run in the USGS for continuous processing of source data and reference sources that will keep up to date over time with changes in taxonomy, listing status, and other details from sources we are consulting. The data in this repo are simply a snapshot at a point in time indicated in the "processing_metadata" or other attributes in the files.


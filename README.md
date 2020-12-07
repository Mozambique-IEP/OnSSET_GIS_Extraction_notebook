# OnSSET GIS extraction
Jupyter notebook facilitated for extracting GIS data and generating the input file necessary for OnSSET. The notebook can be utilized when generating an OnSSET input file from scratch or when the user wants to change one specific dataset in an existing OnSSET-input file. The mandatory datasets are \n:
* Land Cover
* Elevation
* Slope
* Global horizontal irradiation
* Travel time
* Wind velocity
* Clusters (**Note** The clusters have to include the name of the study area, the amount of nighttime lights, population, population living in areas with nighttime light and an ID column)

Optional datasets that can be used for the extraction are: 

* Custom Demand - A layer that can be created by the users themselves. For the first round of GEP the methodlogy described here has been used.
* Substations
* Transformers
* Mini/Small hydro
* Existing and planned HV-lines
* Existing and planned MV-lines
* Road network

The output is in the form of a CSV file that can be directly put into OnSSET.

## Content
This repository contains:
* An environment .yml file needed for generating a fully functioning python 3.7 environment necessary for the clustering algorithm.
* The clustering code and related functions. These files also have instructions for how to run the code

## Installing and running the extraction notebook

**Requirements**

The extraction module (as well as all supporting scripts in this repo) have been developed in Python 3. You are recommended to install [Anaconda's free distribution](https://www.anaconda.com/distribution/) as suited for your operating system. 

**Install the extraction repository from GitHub**

After installing Anaconda you can download the repository directly or clone it to your designated local directory using:

```
> conda install git
> git clone https://github.com/babakkhavari/OnSSET-GIS-Extraction.git
```
Once installed, open anaconda prompt and move to your local "OnSSET-GIS-Extraction" directory using:
```
> cd ..\OnSSET-GIS-Extraction
```

In order to be able to run the tool (main.ipynb and funcs.ipynb) you have to install all necessary packages. "full_project.yml" contains all of these and can be easily set up by creating a new virtual environment using:

```
conda env create --name OnSSET_extraction --file full_project.yml
```

This might take some time. When complete, activate the virtual environment using:

```
conda activate OnSSET_extraction
```

With the environment activated, you can now move to the extraction directory and start a "jupyter notebook" session by simply typing:

```
..\OnSSET-GIS-Extraction> jupyter notebook 
```
## Changelog
**X-December-2020**: Original code base published


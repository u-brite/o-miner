# o-miner


## Table of Contents

- [o-miner](#o-miner)
    - [Background](#Background)
    - [Data](#data)
    - [Usage](#usage)
        - [Installation](#installation)
        - [Requirements](#requirements)
        - [Steps to run ](#steps-to-run)
            - [Step-1](#step-1)
            - [Step-2](#step-2)
    - [Results](#results)
    - [Team Members](#team-members)

## Background

Cancer patient stratification and molecular mechanism identification are essential in risk prediction and personalized therapy. We introduce an application integrated with our previous published tools, the metadata annotation tool called "Statistical Enrichment Analysis of Samples (SEAS)" and the functional genomics downstream analysis tool called "PAGER Web APP". The application enables the stratification of the cancer patients associated with molecular subtypes joined with clinotypes using the clinical feature weighted functional genomics embedding and allows users to identify sub-cohorts in densMAP. In the functional genomics downstream analysis, the application identifies molecular mechanisms driving the clinical feature and systematically reviews the critical insights of the pathway crosstalk and gene mechanisms among those molecular subtypes. The application provides a visual exploration of the sub-cohort's gene panels in each enriched pathway coupling with gene networks, and a comprehensive review of genes by topology-based and transcriptomics-based prioritization.

## Data



## Usage



### Installation

:exclamation: _If installation is required, please mention how to do so here._ :exclamation:

Installation simply requires fetching the source code. Following are required:

- Git

To fetch source code, change in to directory of your choice and run:

```sh
git clone -b main \
    git@github.com:u-brite/team-repo-template.git
```

### Requirements
:exclamation: _Note any software used (including Python or R packages), operating system requirements, etc. and its version so that your project is reproducible. It does not have to be in the below format_ :exclamation:


### Steps to run
:exclamation: _Optional: Depends on project._ :exclamation:

#### Step 1

```sh
python src/data_prep.py -i path/to/file.tsv -O path/to/output_directory
```

#### Step 2

```sh
python src/model.py -i path/to/parsed_file.tsv -O path/to/output_directory
```

Output from this step includes -

```directory
output_directory/
├── parsed_file.tsv               <--- used for model
├── plot.pdf- Plot to visualize data
└── columns.csv - columns before and after filtering step

```



## Results
 
 
 

## Team Members

Zongliang Yue (zongyue@uab.edu)

Yuwei Song (songyw@uab.edu)

Neda Ghohabi (nedaghohabi777@gmail.com)

Eric Zhang (ezhang1@g.ucla.edu)

# UAB 2022 Omics Hackathon O-miner team

Patient stratification and molecular mechanism identification using patient clinotypes and transcriptomics embeddings



![Screenshot (45)](https://user-images.githubusercontent.com/89701701/183282400-835f77a0-ec7d-4769-afd0-d3557973747b.png)




![Screenshot (46)](https://user-images.githubusercontent.com/89701701/183282500-e0568e81-413d-410e-9234-51e83a2500f7.png)



Requirements to use the cookiecutter template:

### Requirements to use the cookiecutter template:
-----------
 
 - Python 3.5+
 
 - PAGER API script downloaded from the website: http://discovery.informatics.uab.edu/PAGER/index.php/pages/help. We loaded a updated version 8/6/22 in the folder.
 
## Table of Contents
- [o-miner](#o-miner)
    - [Background](#background)
    - [Data](#data)
    - [Tools](#tools)
    - [Results](#results)
    - [Team Members](#team-members)
	
## Background

Cancer patient stratification and molecular mechanism identification are essential in risk prediction and personalized therapy. We introduce an application integrated with our previous published tools, the metadata annotation tool called "Statistical Enrichment Analysis of Samples (SEAS)" and the functional genomics downstream analysis tool called "PAGER Web APP". The application enables the stratification of the cancer patients associated with molecular subtypes joined with clinotypes using the clinical feature weighted functional genomics embeddings and allows users to identify sub-cohorts in densMAP. In the functional genomics downstream analysis, the application identifies molecular mechanisms driving the clinical feature and systematically reviews the critical insights of the pathway crosstalk and gene mechanisms among those molecular subtypes.

To enable the multi-Omics explortaion of the molecular subtype specific survival related mechansims, we developed three layers consist of genetics (copy number alteration, gene methylation and gene fusion), transcriptomics (RNA-seq), and microbiome (microbiome abundance). We aims to explore the driving molecules and those relationships between the three Omics layers reflected in the pathway level. Additionally, we aim to discover those molecular type specific panels correlated to survival.

We used SEAS software tool to stratify the cancer patients associated with molecular subtypes joined with survival. We generate the candidate gene lists that collect genetic mutation, differentially expressed genes from RNA-seq data, GBM drug targets from drugbank, and clinical data (GETC).
The project is critical in solving the problem of sub-cohort identification and molecular mechanism exploration using network modeling. 

## Data

GBM multi-Omics data: https://www.cbioportal.org/study/summary?id=gbm_tcga_pan_can_atlas_2018

Data availibility: https://drive.google.com/drive/folders/1-3KZ0NtVdO-mqFQOtSYXoi9D1o9JNO3R?usp=sharing

GBM related drug targes in DrugBank: 
https://go.drugbank.com/

### Tools:

1.SEAS: http://discovery.informatics.uab.edu/SEAS/

2.PAGER: http://discovery.informatics.uab.edu/PAGER/,  PAGER Web APP: https://aimed-lab.shinyapps.io/PAGERwebapp/

3.WINNER: http://discovery.informatics.uab.edu/WINNER/

4.WIPER: http://discovery.informatics.uab.edu/WIPER/

5.BEERE: http://discovery.informatics.uab.edu/BEERE/

## Results

We discovered 824 GBM candidate genes using the GETC frame. In the Disease-Specific Survival (DSS) weighted embedding of the 824 expressed genes, we position 108 TCGA RNA-seq samples with 3 distinct molecular subtypes, i.e., classical (N=35), mesenchymal (N=46) and proneural (N=27). The embedding space showed a clear pattern of three sample subtypes classifications joined with low to high survival trends. We selected high survival and low survival patient samples from each subtype cluster containing all survival high and survival low patient samples by embedding cutoff. This returned 6 final sub-cohorts making 3 intra-group contrast of high vs. low patient samples for downstream analysis. 

Using PAGER API, we retrieved 171 enriched PAGs in a union set of three molecular sub-cohorts pathway enrichment analyses. We found 12 shared pathways and 159 distinct pathways in our three contrast of high vs. low sub-cohorts.  

In the "glioblastoma signaling pathway", we discovered that the mesenchymal specific survival gene panel (9 genes) serving a good performce in survival curve with log rank test p-value = 0.76e-8; the proneural specific survival gene panel (5 genes) serving a good performce in survival curve with log rank test p-value = 0.84e-7; and the classical specific survival gene panel (5 genes) serving a good performce in survival curve with log rank test p-value = 0.67e-11.

In the microbiome layer, we found that the Lymphocryptovirus is negatively associated with CDKN1B gene in the mesenchymal specific survival related sub-cohort with correlation coeffecient = -0.69. 

In the genetic layer, we found that there are 190 gene copy number alterations related to the transciptomic changes in the proneural gene panel. Most events were related to FOXO4 gene. There are 55 gene copy number alterations related to  the transciptomic changes in the proneural gene panel. Most events were related to  MET gene.

In the methylation screening, we found that there were 95 events in the mesenchymal gene panel, 254 events in the proneural gene panel, and 65 events in the classical gene panel.

## Team Members

Zongliang Yue | zongyue@uab.edu | Team Leader  

Yuwei Song | songyw@uab.edu | Member

Neda Ghohabi | nedaghohabi777@gmail.com | Member

Eric Zhang | ezhang1@g.ucla.edu | Member

Yumi Kim | yumikim@uab.edu | Member


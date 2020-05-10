# Mortality Prediction on MIMIC-III Clinical Datasets Using RNN (GRU) and GNN
Project for BMIN-GA 3007 Deep Learning in Medicine Spring, 2020  
Poornima Haridas & Yuan Ding

## Abstract
Quantifying patient health by predicting the mortality is an important problem in critical care research. An accurate prediction of patient mortality can help with the assessment of severity of illness and guide decision making in terms of drastic measures required to save a patient. In this paper, we propose a simple Graph Neural Network based architecture for mortality prediction of patients in the ICU and compare it to a Recurrent Neural Network based benchmark model (GRU). GNNs are known to help extract information from data that can be inherently represented as a graph and this contributes to the explain-ability of the deep learning model which is becoming increasingly essential to all clinical prediction tasks. We find that, given enough time, GNNs perform equivalent to RNNs. We also find that in general, deep learning models perform better when raw features are used. 

## Data
We used the [MIMIC  III](https://mimic.physionet.org/gettingstarted/overview/), a  publicly available  critical  caredatabase  maintained  by  the  Massachusetts  Institute  of  Technology  (MIT)’s  Laboratoryfor  Computational  Physiology. It  integrates  de-identified,  comprehensive  clinical  data  ofpatients admitted to an Intensive Care Unit (ICU) at the Beth Israel Deaconess MedicalCenter (BIDMC) in Boston, Massachusetts during 2001 to 2012.  MIMIC-III contains dataassociated with 53,423 distinct hospital admissions for adult patients whose age is above 15and 7,870 admissions for neonates.  For easy benchmarking, we only included the recordsof the first ICU admission of the adult patients (36,093).  We built the relational databasemimicwith 26 raw tables using PostgreSQL (The instructions can be found [here](https://mimic.physionet.org/tutorials/install-mimic-locally-windows/)). You should request access before using MIMIC III datasets. 

The MIMIC III citation:  
> MIMIC-III, a freely accessible critical care database. Johnson AEW, Pollard TJ, Shen L, Lehman L, Feng M, Ghassemi M, Moody B, Szolovits P, Celi LA, and Mark RG. Scientific Data (2016). DOI: 10.1038/sdata.2016.35. Available at: http://www.nature.com/articles/sdata201635  

> Pollard, T. J. & Johnson, A. E. W. The MIMIC-III Clinical Database http://dx.doi.org/10.13026/C2XW26 (2016).



## Jupyter Notebooks
The `code` folder contains all the codes for our data preparation and modeling.
* The [data_prep](https://github.com/UTpH/dl_in_medicine/tree/master/code/data_prep) foler contains all the codes for data pre-processing and descriptive analysis
* The [GRU](https://github.com/UTpH/dl_in_medicine/tree/master/code/GRU) folder contains all the codes for training GRU models
* The [GCN](https://github.com/UTpH/dl_in_medicine/tree/master/code/GCN) folder contains all the codes for training GNN models  
Run the jupyter notebooks in a Google colab envrionment or download the notebooks as .py files and use the [sbatch script](https://github.com/UTpH/dl_in_medicine/blob/master/code/job_submit.sbatch) to submit the code to HPC clusters (please change the filename in the script).

Code reference: the data preparation for benchmarking
> Purushotham, Sanjay, et al. "Benchmark of deep learning models on large healthcare mimic datasets." arXiv preprint arXiv:1710.08531 (2017).

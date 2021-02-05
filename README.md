# Metadata
A reproduction of following paper as part of MSR course at MSR course 2020/21 at UniKo, CS department, SoftLang Team

AIMMX: Artificial Intelligence Model Metadata Extractor

DBLP: https://dblp.org/rec/conf/msr/TsayBHSM20.html?view=bibtex

[Paper at the Mining Software Repositories Conference 2020 describing AIMMX](http://www.jsntsay.com/publications/tsay-msr2020.pdf)

The paper presents a library AIMMX which extracts the AI model metadata from software repositories.The input data source is Github. 

## Requirements

Runs on Python3 environment with dependencies as mentined in `requirements.txt`

Required software can be installed by executing code

## Process

To avoid 'Access Denied' errors locally, We have used colab to execute code (https://colab.research.google.com/notebooks/intro.ipynb)

* File > Upload notebook > open aimmx.ipynb 

* To upload all files which are in Data folder,execute command mentioned in first cell

* Select runtime in menu > Run all (all required installations are done with pip install commands)

* Go to examples section at end of notebook. Generate GitHub API Key using below steps and then give a github repository link as input.

     * On [GitHub](https://github.com/), click your profile picture in the top-right

     * [Settings > Developer Settings > Personal access tokens > "Generate new token"](https://github.com/settings/tokens)

* Validate the output metadata with Readme file of corresponding input software repository link.Model name, dataset ,references , framework and domain 

can be verified with corresponding paper

## Data

* Provide a AI related model github repository link as input to AIMMX library. Example repository links are provided in notebook(end of AIMMX.ipynb).AIMMX library process the 

code and refereces of input github repository link and then fetch the metadata of AI model(model name, domain, framework, dataset and references used).

* Dataset used for extracting metadata information are uploaded in Data folder

* AIMMX library code is uploaded in Process folder

* Evaluation results and analysis on evaluation dataset is uploaded in Evaluation folder. Sample output can be checked in evaluation.xlsx


## Delta

## Process Delta

* We have taken complete code from original paper. We have faced 'access denied' and 'installation problems' while executing code locally.We tried to change permission settings 

and used different python IDE's to execute code locally. But still we faced issues.

* To avoid this errors and run code flexibly, we modified the structure of code and merged into a single file(aimmx.ipynb) after understanding the whole process. The merged file 

consists of process of five extractors and util classes.

* We also tried to change the way of extracting references using arxivID, as we still got the same output as original paper we used same logic for extraction.

## Data Delta

* The dataset used for evaluation in paper is very huge(7998 repositories). We have collected dataset of 24 AI model repositories for evaluation and analysis with respect to 

software repositories. We have five different extractors in AIMMX model,sample output can be seen in AIMMX file. 

* Output has been manually evaluated by examining corresponding  github repository code and related papers.

* Evaluation results are almost similiar to the results of original paper, except reference extraction. We got less accuracy for reference extraction compared to the original 

paper.

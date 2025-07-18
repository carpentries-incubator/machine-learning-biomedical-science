---
title: Setup
---

## Project organization

1. Start RStudio.

2. Create a new project in your Desktop called `ml-biomed`. 
- Click the `File` menu button, then `New Project`.
- Click `New Directory`. 
- Click `New Project`.
- Type `ml-biomed` as the directory name. Browse to your Desktop to create the project there.
- Click the `Create Project` button.

3. Use the `Files` tab to create  a `data` folder to hold the data, a `scripts` 
folder to hold your scripts, and a `results` folder to hold results. 
Alternatively, you can use the R console to run the following commands for step 
3 only. You still need to create a project with step 2.

   ~~~
   dir.create("./data")
   dir.create("./scripts")
   dir.create("./results")
   ~~~
   {: .r}
   
## Data Sets

Download the tissue gene expression 
[data directly from Github](https://github.com/genomicsclass/tissuesGeneExpression/blob/master/data/tissuesGeneExpression.rda) 
and place them in your new `data` directory.
   
The data represent RNA expression levels for eight tissues, each with several
individuals.

## Software Setup
 
1. Install R packages and load the libraries.

    ~~~
   install.packages("rafalib", "RColorBrewer", "gplots", "UsingR", "class", "caret", "UsingR")
   library(rafalib)
   library(RColorBrewer)
   library(gplots)
   library(UsingR)
   library(class)
   library(caret)
   library(UsingR)
   ~~~
   {: .r}

2. Install and load packages from Bioconductor.

   ~~~
   if (!require("BiocManager", quietly = TRUE))
        install.packages("BiocManager")
   
   BiocManager::install(c("genefilter", "Biobase", "SpikeIn", "hgu95acdf")
   library(genefilter)
   library(Biobase)
   library(SpikeIn)
   library(hgu95acdf)
   data(SpikeIn95)
   ~~~
   {: .r}

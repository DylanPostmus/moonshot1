# moonshot1
**MO**dular **O**perating **N**ode for **S**tatistical **H**elp **O**r **T**asks, version 1.0. A collection of web apps built using the Shiny framework from Rstudio, designed to perform useful functions and provide assistance with statistical analysis.

The moonshot tools have been created with the needs of the AIVE/Goffinet Lab group in mind, but can be used more generally as well. More information is available on request. Here follows an overview of each tool and some basic guidelines as to its usage:

## FetchGene

FetchGene is designed to retrieve alternative gene IDs to those that are available, e.g. to retrieve HGNC symbols when only ENSEMBL IDs are provided. It takes as input a spreadsheet file (csv or xlsx) with, importantly, a column named **gene** (all lower case letters). It then edits the file as it is uploaded to add (a) column(s) with the corresponding alternative gene IDs (e.g. UniProt, Refseq etc.). This file can be downloaded as a csv or xlsx (or copied to your clipboard). All other columns and their order is preserved.

Link to [FetchGene](https://dylanpostmus.shinyapps.io/FetchGene/) or go to  https://dylanpostmus.shinyapps.io/FetchGene/.

## MarkGene

MarkGene is designed to mark genes based on whether they belonging to one or multiple genesets, avoiding the need to check each gene individually. This is useful particularly for differential expression results dataframes from NGS experiments, e.g. RNA-seq. Currently, the Reactome Interferon Signalling pathway and a hand-picked set of NRF2 regulated genes are supported. It takes as input a spreadsheet file (csv or xlsx) with, importantly, a column named **gene** (all lower case letters). It then edits the file as it is uploaded to add (a) column(s) indicating whether the gene belongs to the selected geneset(s). This file can be downloaded as a csv or xlsx (or copied to your clipboard). All other columns and their order is preserved.

Link to [MarkGene](https://dylanpostmus.shinyapps.io/MarkGene/) or go to  https://dylanpostmus.shinyapps.io/MarkGene/.

## MEMbuilder

MEMbuilder is designed to allow for the building of linear mixed effects models and basic data exploration. This is useful for data with repeated measures, such as longitudinal studies with multiple observations per subject/patient/animal over time.  It takes as input a spreadsheet file (csv or xlsx) 
and reqires:
- Decimal **points**, NOT commas to be used
- Columns containing **numerical data** should *not* contain non-numerical entries, e.g. 5.16, 6.78. no detected, 7.56 -- BAD!
- Data should be in the long format (each row should be a single observation, with columns specifying all relevant information) e.g
**Patient** - **Treatment** - **CD4_count** : Patient1 - DEX - 456
It then builds a linear mixed effects model, outputting the summary, some QC statistics and allowing for some basic graphing of the data.

Link to [MEMbuilder](https://dylanpostmus.shinyapps.io/MEMbuilder/) or go to https://dylanpostmus.shinyapps.io/MEMbuilder/.


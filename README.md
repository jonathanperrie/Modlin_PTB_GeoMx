# TREM2 macrophages in PTB
This repo contains the code used to process our GeoMx and CosMx data and generate plots for the manuscript. Plots and data are not included here. 

## GeoMx
Like bulk RNA-seq but with coordinates. We take the data and filter out genes that are not expressed above background (see NanoString document on limit of quantification) and spots that do not have enough genes expressed. There are some other filters too. We start with the DCC files, an annotation file, and a configuration file. 

The annotation file has DCC filenames (**Sample_ID**) + tissue labels (**Scan name**) + sample annotations (**Segment tags**) + coordinates. It was constructed from the SegmentProperties sheet within the NanoString counts spreadsheets provided in the initial data dump for each sample. 

![Alt text](geomx_anno_all_batch_header.png)

Filtering and quality control: [NanoString workflow](https://www.bioconductor.org/packages/release/workflows/vignettes/GeoMxWorkflows/inst/doc/GeomxTools_RNA-NGS_Analysis.html)

Configuration file - [Hs_R_NGS_WTA_v1.0](https://nanostring.com/products/geomx-digital-spatial-profiler/geomx-dsp-configuration-files/)

Q3 - NanoString workflow

Median of ratios - [DESeq2](https://hbctraining.github.io/DGE_workshop/lessons/02_DGE_count_normalization.html) 

##



## CosMx
Like scRNA-seq but with coordinates

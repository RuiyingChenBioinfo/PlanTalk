# PlanTalk

<img src="https://github.com/RuiyingChenBioinfo/PlanTalk/blob/main/imgs/PlanTalk.logo.png" align="right" width="160" height="180">

### Cell-cell Communication Analysis Tool for Plants

The R package PlanTalk is designed to quantify the cell-cell communication intensity using spatial information, provide elegant visualization of inferred ligand-receptor pairs, and infer receptor-activated pathways in single-cell RNA sequencing (scRNA-seq) data in plants.




# Tutorial

### Inputs

When using this software, you need to prepare the input files as required, including three parts: the ligand-receptor pair database, the processed scRNA-seq data with Seurat structures, the pathway-related information of the corresponding species, and spatial information of corresponding plant tissues (optional). 

**1. The ligand-receptor pair database**

The database should contain ligand and receptor information respectively in the "Ligands" and "Receptors" columns of the R data frame. If you are using the PlantPhoneDB (https://jasonxu.shinyapps.io/PlantPhoneDB/) database, we suggest removing out the ligand-receptor pairs from the "homolog" source, since the orthologs were obtained only from human orthologs and are without experimental validations, making many inferred receptor-ligand pairs unreliable.

**2. The pathway information**

The pathway information should contain gene identifiers (consistent with the gene format in the Seurat data input), pathway number, pathway type and pathway description.

The ligand-receptor databases (for input file 1) modified from PlantPhoneDB, GO (Gene Ontology) information and KEGG (Kyoto Encyclopedia of Genes and Genomes) information (for input file 2) of *Arabidopsis thaliana* and *Solanum lycopersicum* have been configured and can be used directly in PlanTalk. In the future we will add more built-in databases for different species.

**3. Gene list representing plasmodesmata strength (optional)**

This file should be a one-column file with no row names and no column header. The plasmodesmata gene lists of *Arabidopsis thaliana* and its homologues in *Solanum lycopersicum* have been configured and can be used directly in PlanTalk.

**4. Spatial information of corresponding plant tissues (optional)**

The spatial information should be in data frame format, similar to ggPlantmap (https://github.com/leonardojo/ggPlantmap) provided examples.

PlanTalk currently contains built-in spatial information of longitudinal root tips of *Arabidopsis thaliana*, cross section roots of *Arabidopsis thaliana* and *Solanum lycopersicum*, and shoot apical meristems of *Arabidopsis thaliana*. If you wish to use custom spatial information, you can first follow the ggPlantmap workflows to process your original image, and then transform the outputs to data frame formats.

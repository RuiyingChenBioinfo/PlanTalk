# PlanTalk

<img src="https://github.com/RuiyingChenBioinfo/PlanTalk/blob/main/imgs/PlanTalk.logo.png" align="right" width="160" height="180">

*Cell-cell communication analysis tool for Plants*

The R package PlanTalk is designed to quantify the cell-cell communication intensity using spatial information, provide elegant visualization of inferred ligand-receptor pairs, and infer receptor-activated pathways in single-cell RNA sequencing (scRNA-seq) data in plants.



# Tutorial

*Inputs*

When using this software, you need to prepare the input files as required, including three parts: the ligand-receptor pair database, the processed scRNA-seq data with Seurat structures, the pathway-related information of the corresponding species, and spatial information of corresponding plant tissues (optional). 

The ligand-receptor pair databases should contain ligand and receptor information respectively in the "Ligands" and "Receptors" columns of the R data frame. We suggest removing out the "homolog" source genes in the PlantPhoneDB (https://jasonxu.shinyapps.io/PlantPhoneDB/) database, since the orthologs were obtained only from human orthologs and are without experimental validations, making many inferred receptor-ligand pairs unreliable.

The pathway information should contain gene identifiers (consistent with the gene format in the Seurat data input), pathway number, pathway type and pathway description.
The ligand-receptor databases modified from PlantPhoneDB, GO (Gene Ontology) information and KEGG (Kyoto Encyclopedia of Genes and Genomes) information of Arabidopsis thaliana and Solanum lycopersicum have been configured and can be used directly in PlanTalk. In the future we will add more built-in databases for different species.

Spatial information of corresponding plant tissues should be in data frame format, similar to ggPlantmap (https://github.com/leonardojo/ggPlantmap) provided examples. PlanTalk currently contains built-in spatial information of longitudinal root tips of Arabidopsis thaliana, cross section roots of Arabidopsis thaliana and Solanum lycopersicum, and shoot apical meristems of Arabidopsis thaliana. If you wish to use custom spatial information, you can first follow the ggPlantmap workflows to process your original image, and then transform the outputs to data frame formats.


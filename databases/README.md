### For PlantPhoneDB database correction:
1. We deleted the ligand-receptor pairs from human homologous genes with human and *Arabidopsis thaliana* (which are noted as "ortholog" in the "source" column) in the original PlantPhoneDB database.
2. We eliminated duplication of repeating ligand-receptor pairs and merged their sources in *Arabidopsis thaliana* databases.
3. We keeped ligand and receptor genes that are also included in the GO/KEGG terms following keywords: "ligand"/"secrete"/"signal" (for ligand genes) or "receptor"/"membrane"/"signal" (for receptor genes) in the *Arabidopsis thaliana* database.
4. We added recently published ligand-receptor pair information to the databases.

The strictly revised PlantPhoneDB databases for *Arabidopsis thaliana* (LR_pair_strictlyrevised.At.PlantPhoneDB.csv) and *Solanum lycopersicum* (LR_pair_strictlyrevised.Sl.PlantPhoneDB.csv) were used for PlanTalk inputs.

### Author contribution: 
R.C. collected GO and KEGG information of *Arabidopsis thaliana* and revised the original PlantPhoneDB database. S.H. collected GO and KEGG information of *Solanum lycopersicum*.

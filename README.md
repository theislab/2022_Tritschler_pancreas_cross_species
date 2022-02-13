# A transcriptional cross species map of pancreatic islet cells

This repository contains scripts to reproduce the results of the single-cell data from:
S. Tritschler et al., "A transcriptional cross species map of pancreatic islet cells", _submitted_, 2022


The notebooks contain code for the following analyses:

**scRNA-seq of human pancreatic islets:**  
- _human_islets_preprocessing.ipynb_ --> QC, preprocessing, batch correction (input data are raw count matrices)  
- _human_islets_new_clustering.ipynb_ --> Manifold, clustering and annotation steps for endocrine, beta and alpha cells (input data are preprocessed, filtered and annotated count matrices)  
- _human_islets_endocrine_analyses.ipynb_, _human_islets_beta_analyses.ipynb_, _human_islets_alpha_analyses.ipynb_ --> main analyses to reproduce results and plots of human endocrine cells (input data are preprocessed, filtered and annotated count matrices)  
- _human_patch_seq_Camunas_Soler_2020.ipynb_ --> Mapping of single-cell Patch-seq (Camunas-Soler, 2020) data to human reference
- _curate_fetal_Cao_2020.ipynb_ --> QC, preprocessing, manifold, clustering and annotation steps for human fetal pancreatic cells (Cao, 2020)

**scRNA-seq of pig pancreatic islets:**    
- _pig_islets_preprocessing.ipynb_ --> QC, preprocessing, batch correction (input data are raw count matrices) 
- _pig_islets_new_clustering.ipynb_ --> Manifold, clustering and annotation steps and analysis for endocrine cells (input data are preprocessed, filtered and annotated count matrices)  

**scRNA-seq of mouse pancreatic islets:**     
- _mouse_new_clustering.ipynb_ --> Preprocessing, manifold, clustering and annotation steps and analysis for endocrine cells (input data are preprocessed, filtered and annotated count matrices) (Sachs, 2020)
- _mouse_STZ_model.ipynb_ --> Analysis mouse STZ model (Sachs, 2020)

**Cross species mapping:**      
- _cross_species_mapping.ipynb_ --> main analyses to reproduce results and plots of cross-species comparisons and mapping    


The data has been deposited in GEO under accession number xxxx. The raw count matrices as well as preprocessed, filtered and annotated count matrices are provided as supplementary file as an Anndata object (h5ad-file).

For exploration visit the CellxGene data portal:  or load the anndata-files into a python-session for additional analyses using scanpy.

Note that most of the analysis was done with scanpy v1.4-v1.6. Some functions have changed in newer versions of scanpy. For other package versions please consult the notebook or the methods in the supplementary information of the manuscript. Numeric results can vary depending on package versions and e.g. affect clustering.

If the materials in this repo are of use to you, please consider citing the above publication.

If you have any questions about the data or analysis feel free to contact us. :)

# A transcriptional cross species map of pancreatic islet cells

This repository contains scripts to reproduce the results of the single-cell data from:
S. Tritschler et al., "A transcriptional cross species map of pancreatic islet cells", Molecular Metabolism, 2022


The notebooks contain code for the following analyses:

## scRNA-seq of human pancreatic islets 
- **human_islets_preprocessing.ipynb** --> QC, preprocessing, batch correction (input data are raw count matrices)  
- **human_islets_new_clustering.ipynb** --> Manifold, clustering and annotation steps for endocrine cells (input data are preprocessed, filtered and annotated count matrices)  
- **human_islets_endocrine_analyses.ipynb**, **human_islets_beta_analyses.ipynb**, **human_islets_alpha_analyses.ipynb** --> main analyses to reproduce results and plots of human endocrine cells (input data are preprocessed, filtered and annotated count matrices)
- **human_patch_seq_Camunas_Soler_2020.ipynb** --> Mapping of single-cell Patch-seq (Camunas-Soler et al, 2020) data to human reference
- **human_state_mapping_cross_study.ipynb** --> Cross-study mapping of human b cell states (9 public human datasets)
- **curate_9_human_public_studies.ipynb** --> QC, preprocessing, manifold, clustering and broad annotation steps for 9 available human scRNA-seq studies of pancreatic islets (Fasolino et al 2022, Shresta et al 2021, Fang et al 2019, Xin et al 2018, Enge et al 2017, Lawlor et al 2017, Baron et al 2016, Segerstolpe et al 2016, Muraro et al 2016)
- **curate_fetal_Cao_2020.ipynb** --> QC, preprocessing, manifold, clustering and annotation steps for human fetal pancreatic cells (Cao et al, 2020)
- **curate_fetal_Yu_2021.ipynb** --> QC, preprocessing, manifold, clustering and annotation steps for human fetal pancreatic cells (Yu et al, 2021)
- **human_beta_cell_velocity_all_donors** --> RNA velocity analysis for human beta cells (this requires to run velocyto on bam files to extract exonic/intronic read information. For details see M&M)

## scRNA-seq of pig pancreatic islets  
- **pig_islets_preprocessing.ipynb** --> QC, preprocessing, batch correction (input data are raw count matrices) 
- **pig_islets_new_clustering.ipynb** --> Manifold, clustering and annotation steps and analysis for endocrine cells (input data are preprocessed, filtered and annotated count matrices)  

## scRNA-seq of mouse pancreatic islets     
- **mouse_new_clustering.ipynb** --> Preprocessing, manifold, clustering and annotation steps and analysis for endocrine cells (input data are preprocessed, filtered and annotated count matrices) (Sachs et al, 2020)
- **mouse_STZ_model.ipynb** --> Analysis mouse STZ model (Sachs et al, 2020)
- **mouse_state_mapping_Pineros** --> Confirmation of cross-species mapping of human alpha and beta cell states to mouse cells (Pineros et al, 2020)

## Cross species mapping:      
- **cross_species_conservation.ipynb**, **cross_species_heterogeneity_mapping.ipynb** --> main analyses to reproduce results and plots of cross-species conservation and mapping   


The data has been deposited in GEO under accession number GSE198623. The raw count matrices as well as preprocessed, filtered and annotated count matrices are provided as supplementary file as an Anndata object (h5ad-file).

For exploration visit the CellxGene data portal:  or load the anndata-files into a python-session for additional analyses using scanpy.

Note that most of the analysis was done with scanpy v1.4-v1.6. Some functions have changed in newer versions of scanpy. For other package versions please consult the notebook or the methods in the supplementary information of the manuscript. Numeric results can vary depending on package versions and e.g. affect clustering.

If the materials in this repo are of use to you, please consider citing the above publication.

If you have any questions about the data or analysis feel free to contact us. :)

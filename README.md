# FVS-Apptainer
Find Viral Strains inside of an apptainer container

Steps to use: 
1. Clone the repository in your desired location.
2. Build your .sif file
   > apptainer build yourfilename.sif fvs.def
3. Run FindViralStrains
   > apptainer run --bind /your_repository_location --bind /your_data_location path_to/findviralstrains.sif snakemake -s findviralstrains.smk --configfile config_files/build_test.yaml --cores 2

Binding your repository ensures changes will persist after the apptainer has finished running.


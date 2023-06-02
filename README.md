# Exploring Genetic Variation
Comparison of genetic variation between populations in the 1000 Genomes Project using machine learning techniques such as PCA (currently implemented) and clustering (to be added)

process_genotypes.ipynb: 
- download VCF file for specified chromosome
- extract samples and variants, create genotype matrix
- save matrix as compressed numpy file (.npz)
- save samples list as numpy file (.npy)

sample_info.ipynb: 
- download file with sample information
- load saved samples list
- create and save dictionary of sample information
    - key = sample_id
    - value = [population, super_population, gender]
- create and save CSV files with count information
    - subpopulation (population) counts
    - superpopulation counts
    - gender counts
- create and save color dictionaries for superpopulations and subpopulations
- view table of subpopulation full names, their superpopulation, and chosen color

pca.ipynb:
- load saved genotypes matrix, samples list, dictionaries
- perform PCA on genotypes matrix to reduce dimensionality
- create and save plot of PCA results by superpopulation
- create and save plots of PCA results by subpopulation

Future work:
- combine data from multiple chromosomes
- implement clustering algorithm to compute clusters of populations
    - evaluate accuracy against actual populations
    - determine which populations cluster together/if there is a structure

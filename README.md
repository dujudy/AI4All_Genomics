# AI4All_Genomics

AI4All@Princeton is a summer camp that aims to promote diversity in computer science by teaching AI to young students of diverse backgrounds (https://ai4all.princeton.edu).  In this module, we will be investigating our genomic diversity by exploring natural genomic variation between world populations.

Relevant Links:
- IGSR home: Genohttp://www.internationalgenome.org/home
- Phase 3 1000 Genomes Results: https://www.nature.com/articles/nature15393#abstract
- Phase 3 1000 Genomes Data: https://ftp-trace.ncbi.nih.gov/1000genomes/ftp/release/20130502/
- Phase 3 1000 Genomes Processing Example: https://bitbucket.org/remills/1000gp_sv_phase3/src/master/
  - *** see gwas_sv_ld_filt_af.txt 
  
Data Preprocessing
- Run GATK software to subset SNPs: https://software.broadinstitute.org/gatk/documentation/tooldocs/4.0.0.0/org_broadinstitute_hellbender_tools_walkers_variantutils_SelectVariants.php
  - run ./gatk/gatk SelectVariants -V input.vcf -O output.vcf --keep-ids gwas_sv_ld_RSIDs.list 
    - example output.vcf: chrX_filtered.txt
 - concatenate vcf files using vcf-tools
  - https://vcftools.github.io/man_latest.html

To Do:
- merge data
- double check student histories to get an intuition for their academic level
- plan (and test) which ML algorithms to introduce to students (clustering, standard prediction, etc)
- revisit calendar to edit the syllabus
- brainstorm intro slides to SNPs
- explore with python and benchmark runtimes

Files:
- 1000genomes_dataExploration.ipynb: preliminary exploration of 1000 Genomes data (PCA, SVM, data cleanup and filtering)

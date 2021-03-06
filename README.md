# [SIP](https://github.com/chansigit/SIP) 
## Overall
Multiple steps of bioinformatics processing are needed to convert scRNA-seq data to information that can be used in downstream analyses. Dozens of software packages have been developed but different labs tend to have different preferences on the choices of the workflow. Such diversity can cause difficulties in future efforts of aggregating data from multiple labs, and also difficulties for new labs to start in this field. A few pipelines have been developed to help integrating multiple steps into a whole, but the fixed software architecture makes it hard for developers to add new features or exchange parts in the pipeline. 

SIP is a single-cell data processing pipeline whose components are interchangeable. It is a one-stop full-stack framework for the processing of scRNA-seq data from multiple platforms, and will also work for other types of single-cell sequencing data like dscRNA-seq data, and scATAC-seq data. SIP has the following major components: Read QC & preprocessing, Alignment & quasi-alignment, Transcript assembly, Expression Counting, Subpopulation finding, Trajectory analysis, DEG analysis. 

The pipeline is developed based on  a popular workflow framework [Nextflow](https://github.com/nextflow-io/nextflow), and uses container technology to solve the package dependency catastrophe and the deployment dilemma. SIP provides a very handy access to HPC resources, making it easy to process massive amount of data. The pipeline uses an open structure, allowing users to integrates new parts into this system.



## Quick start


1. Setting up the Nextflow environment. Simply run the following command to set up Nextflow environment. Nextflow requires JDK 1.8 and POSIX compatible operating systems (Max OS X, Linux, Unix, etc). Windows users can use cygwin or windows subsystem for linux to run Nextflow. 


   ```wget -qO- get.nextflow.io | bash  ```

2. Download the SIP with git clone

   ```git clone https://github.com/chansigit/SIP.git```

6. Run the SIP pipeline with your own data:

   ```nextflow run ./sipmain.groovy```


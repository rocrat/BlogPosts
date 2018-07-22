Normalization of High-throughput Data for Clinical Testing
========================================================
author: Dominic LaRoche 
date: 22-Jul-2018
autosize: true
css: ./CCC/bootstrap.css

Why do we need normalization?
========================================================

High-throughput measurements systems include a lot of technical variation.

- Uneven library sizes for RNA seq
- Batch effects
- etc.

Normalization attempts to remove tehcnical variation while preserving biological variation.

Normalization Methods Discussed Today
========================================================

There are many methods available:

- Counts per Million (CPM)
- Total Count (TC)
- Upper Quartile (UQ)
- Median Ratio (MR)
- Trimmed Mean of M-values (TMM)
- Quantile

Notation
========================================================
I will use the framework of RNA-Seq but the methods are translatable to other measurement systems.

We assume an experiment in which measurements for $P$ probes are made on a set of $K$ samples.

- $Y_{gk}$ refers to the count (measurment) for probe $g$ in sample $k$.
- $N_k$ is the total number of reads for sample $k$


Counts per Million and Total Count
========================================================

CPM and TC normalizations are really more accurately described as "Standardizations."

The goal of both methods is to standardize the individual probe counts by accounting for the total number of counts allocated to each sample.  

Upper Quartile
========================================================
Upper quartile normalization was proposed by Bullard et al. (2010) to



Median Ratio
========================================================
The median ratio method of normalization was proposed by Anders and Huber (2010) as part of their model for differential expression of RNA-Seq data.




Trimmed Mean of M-values
========================================================
Robinson and Oshlack (2010) proposed the TMM method using similar logic to Anders and Huber, i.e. most probes should not be different.



Quantile Normalization
========================================================
Quantile normalization was first introduced by Bolstad et al. (2003) in the context of microarray experiments but has been adapted to a number of other applications.



General Classes of Normalizations
========================================================
All of these normalization methods can be grouped into two categories:

1. Scaling normalizations
  - Generate a scale factor for each sample to re-scale the counts
  - May not adequately remove technical variation among samples
  
2. Constraining normalizations
  - Constrain the distribition of each sample to some reference distribution
  - May not be applicable if there a *biological* differences in the distributions among sample types
    - Diseased and healthy samples may have meaningful differences in distribution
  
  
  
Performance of Normalization Methods
========================================================



Applying Normalization in the Clinical Setting
========================================================
The ultimate goal of many analyses of high-thoughput data is to generate a clinical diagnostic.

- Applying normalizations to individual clinical samples can be difficult
  - CPM is an appealing option becuase it is applied at the sample level and no other information is required
  - Other scale factor normalizations are "batch-applied", making the normalization of new samples difficult
  
- Incorporating the normalization into the diagnostic prediction model is one possible solution
  - Must be capable of being applied to individual samples measured in a testing lab
  - Must be validated as part of the diagnostic procedure

  
Quantile Normalization for Clinical Testing
========================================================

Quantile normalization can be incorporated into the diagnostic model.

- Generate reference distribution with the same samples used to train the model







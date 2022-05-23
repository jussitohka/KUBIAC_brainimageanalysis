# Statistical group analyses
This largely follows *Handbook of functional MRI data analysis* by Russell Poldrack, Jeanette Mumford and Thomas Nichols
## The mixed effects model

**Fixed, random and mixed effects**

The terms of fixed, random, and mixed effects have variable meanings in statistics and thus one should be careful about how to interpret them. See Gelman 2004 about various definitions http://www.stat.columbia.edu/~gelman/research/published/AOS259.pdf . 

In brain imaging, the mixed effects models account for both within-subject and between subject variabilities, i.e., the model for (a single group) is

<img src="https://render.githubusercontent.com/render/math?math=y_{ij} = d \oplus z_i \oplus e_{ij}"> ,

where d is the population level parameter of actual interest, z_i is the subject specific mean (not interesting in its own right) and e_{ij} is the subject specific error term.  Note that the model can include additional mean terms modelling, e.g., the effects of gender. Typically, in statistics, this kind of mixed effects model can be easily written, however, since in brain imaging, there are typically an enormous number of voxels to be tested a 2-step summary statistics approach is used instead. 

In the simplest case, making a simplifying assumption of equal within subject variance, the 2-step strategy involves doing statistics on the first level estimates.     


## Inference and multiple comparisons correction

The result of the previous step is a group level statistical map describing the size of studied effect  

## Statistical power

Power analyses must be carried out prior to data collection to plan how many subjects are necessary for a study. You may see notions of the post-experiment power analyses, but these are usually useless and pointless (and wrong) exercises.  The power calculation is a function of the number of subjects in the study; the Type I error rate; the size of the effect that you wish to be able to detect; and the variance of this effect. The multiple comparsions problem makes the power calculation in neuroimaging data analysis more complicated than elsewhere and it should be included in the considerations.  

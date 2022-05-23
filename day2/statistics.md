# Statistical group analyses
This largely follows *Handbook of functional MRI data analysis* by Russell Poldrack, Jeanette Mumford and Thomas Nichols
## The mixed effects model

**Fixed, random and mixed effects**

The terms of fixed, random, and mixed effects have variable meanings in statistics and thus one should be careful about how to interpret them. See Geelman 2004 about various definitions http://www.stat.columbia.edu/~gelman/research/published/AOS259.pdf . 

In brain imaging, the mixed effects models account for both within-subject and between subject variabilities, i.e., the model for (a single group) is

<img src="https://render.githubusercontent.com/render/math?math=_{ij} = d_{population} \oplus z_i \oplus \epsilon_{ij}"> ,

where d is the population level parameter of actual interest. 


## Inference and multiple comparsions correction


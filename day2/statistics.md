# Statistical group analyses
This largely follows *Handbook of functional MRI data analysis* by Russell Poldrack, Jeanette Mumford and Thomas Nichols
## The mixed effects model

**Fixed, random and mixed effects**

The terms of fixed, random, and mixed effects have variable meanings in statistics and thus one should be careful about how to interpret them. See Gelman 2004 about various definitions http://www.stat.columbia.edu/~gelman/research/published/AOS259.pdf . 

In brain imaging, the mixed effects models account for both within-subject and between subject variabilities, i.e., the model for (a single group) is

<img src="https://render.githubusercontent.com/render/math?math=y_{ij} = d \oplus z_i \oplus e_{ij}"> ,

where d is the population level parameter of actual interest, z_i is the subject specific mean (not interesting in its own right) and e_{ij} is the subject specific error term.  Note that the model can include additional mean terms modeling, e.g., the effects of gender. Typically, in statistics, this kind of mixed effects model can be formed and solved using standard statistical packages such as SPSS, stata or packages for Python or R. (We do not go into details how these algorithms work here). In brain imaging, however, there are typically an enormous number of voxels to be tested and also the design matrices are large (especially in fMRI). Therefore, a 2-step summary statistics approach is used instead: 

![image](https://user-images.githubusercontent.com/6709791/169844800-b2aa9eed-2402-4871-a64b-554536afa1db.png) 
Figure from Maumet, Camille; Nichols, Thomas (2018): Validity of summary statistics-based mixed-effects group fMRI. figshare. Presentation. https://doi.org/10.6084/m9.figshare.6723851.v1  CC-BY-4.0. 

In the simplest case, making a simplifying assumption of equal within subject variance, the 2-step strategy involves doing statistics on the first level estimates. However, usually a more complex scheme involving iterative estimation such as in Worsley et al 2002 https://doi.org/10.1006/nimg.2001.0933 or Woolrich 2004 https://doi.org/10.1016/j.neuroimage.2003.12.023.        

You can also watch: https://www.youtube.com/watch?v=mzAMZtUAY-M

## Inference and multiple comparisons correction

The result of the previous step is a group level statistical map describing the size of studied effect. That is a lot of data to chew on. Typically, in the realm of the classical statistical analyses, we are interested in the questions like:  at which voxels patients response to the stimulus differs from that of controls or at which voxels controls have more gray matter than patients.  The statistical maps have to be thresholded to draw conclusions. But where to put a threshold?   An example follows: (See https://neurovault.org/images/13166/ , from Jääskeläinen et al 2016 http://doi.org/10.1038/srep27741 )

Unthresholded statistical map:  
![image](https://user-images.githubusercontent.com/6709791/169892655-131f26cb-c955-44c2-ba15-288d66354e7b.png) Statistical parametric maps of hemodynamic activity during first-time viewing of the movie clips as explained by self-rated humorousness in the GLM based analysis.  

Map thresholded at |Z| > 2:

![image](https://user-images.githubusercontent.com/6709791/169894379-eaed166d-7f4e-4e31-9478-3a4f03c5324d.png)

Map thresholded at |Z| > 4
![image](https://user-images.githubusercontent.com/6709791/169894715-f9a08cc8-8125-4bbf-8078-af21e6b842b6.png)

Which one is correct? 

We formulate a hypothesis test at each voxel, i.e., assign a p-value to a voxel. If our statistical maps are parametric (t, Z, or F typically), we can easily assign a p-value to each voxel.  But how the threshold the p-values? If we threshold at p < 0.05 when doing hundreds of thousand of hypothesis tests, a problem of multiple comparsions follows (Remember the dead salmon during the mental rotation task. )          

## Statistical power

Power analyses must be carried out prior to data collection to plan how many subjects are necessary for a study. You may see notions of the post-experiment power analyses, but these are usually useless and pointless (and wrong) exercises.  The power calculation is a function of the number of subjects in the study; the Type I error rate; the size of the effect that you wish to be able to detect; and the variance of this effect. The multiple comparsions problem makes the power calculation in neuroimaging data analysis more complicated than elsewhere and it should be included in the considerations.  

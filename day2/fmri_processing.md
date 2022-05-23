# fMRI processing into subject-specific statistical maps
follows fMRI Data analysis handbook
## The BOLD Signal

The goal of task-based fMRI data analysis is to analyze each voxel’s time series to see whether the BOLD (blood oxygenation level dependent) signal changes in response to some manipulation. In principle, we want to look how strongly the voxel time series correlates with the manipulation (task).  However, there are several issues to take into account such as  the BOLD signal arising from the interplay of blood ﬂow, blood volume, and blood oxygenation in response to changes in neuronal activity - i.e. being an indirect measure of neural activity. Therefore , the analysis tool is the general linear model (GLM), where the BOLD time series plays the role of dependent variable, and the independent variables in the model reﬂect the expected BOLD stimulus timecourses.


![z9j0010503411001](https://user-images.githubusercontent.com/6709791/169793057-1eceed36-68d8-4a7c-86df-45deb28ea4f5.jpeg) Figure from Demonet, Thierry and Cardebat. Physiological Reviews 2005 https://doi.org/10.1152/physrev.00049.2003 Copyright 2005 the American Physiological Society 

## Time series preprocessing 
1) The most obvious characteristic of noise in BOLD fMRI data is the presence of low-frequency drift, which is removed by high-pass filtering (in a voxel-by-voxel manner).
2) The GLM  assumes that the data are not temporally autocorrelated and that the variance of the data is constant over observations. When these assumptions are violated, the inferences based on the GLM are biased and can result in an elevated false positive rate. Thus, we estimate and undo the correlation structure of the data. The current standard approach is to prewhiten the data to remove the temporal autocorrelation.  

There are variations how different analysis packages implement these steps and what additional (time series) preprocessing there might be. 

## Statistical modeling

![image](https://user-images.githubusercontent.com/6709791/168901430-f996562c-e85a-4d9c-918f-e388e2b734ad.png)
*Figure from Monti 2011 https://doi.org/10.3389/fnhum.2011.00028*

We can write the GLM as
<img src="https://render.githubusercontent.com/render/math?math=Y = X\beta \oplus \epsilon"> , where Y is the BOLD time series, X is the design matrix,<img src="https://render.githubusercontent.com/render/math?math=\beta"> is the vector of parameter estimates, <img src="https://render.githubusercontent.com/render/math?math=\oplus"> is + (cannot write the ordinary + in Equations in here for some reason, looking into it), <img src="https://render.githubusercontent.com/render/math?math=\epsilon"> is the error term (normally distributed, zero mean, with and covariance sV). For GLM to be optimal/valid, V should be an identity matrix. The pre-whitening finds a matrix W so that WVW' = I and the model becomes  <img src="https://render.githubusercontent.com/render/math?math=WY = WX\beta \oplus W\epsilon">, with independent errors.  Writing Y* = WY, X* = VX*,  <img src="https://render.githubusercontent.com/render/math?math=\epsilon* = V\epsilon">, we get the parameter estimates <img src="https://render.githubusercontent.com/render/math?math=\hat{\beta} = (X*'X*)^{-1} X^*'Y*">  and the covariance <img src="https://render.githubusercontent.com/render/math?math=\hat{Cov}(\hat{\beta}) = (X*'X*)^{-1} s">.  This all is straight-forward statistics.  

**Statistical contrasts:** The term constrast in terms of the GLMs refers to linear combinations of the elements of the parameter vector <img src="https://render.githubusercontent.com/render/math?math=\beta">. Constrasts allow to specify the hypotheses we would like to address, such as: is <img src="https://render.githubusercontent.com/render/math?math=\beta_1"> different from zero, is <img src="https://render.githubusercontent.com/render/math?math=\beta_1"> larger than <img src="https://render.githubusercontent.com/render/math?math=\beta_2"> and soforth. Mathematically, a contrast is vector c of the same length as the parameter vector <img src="https://render.githubusercontent.com/render/math?math=\beta">.  The distribution of <img src="https://render.githubusercontent.com/render/math?math=c\hat{\beta}"> (under GLM assumptions) is normal, and thus we get t-statistic

<img src="https://render.githubusercontent.com/render/math?math=t=\frac{c\hat{\beta}}{\sqrt{c(X*'X*)^{-1}c's}}">.

This t-statistic map of each individual can be passed to the group level analyses. t-statistics are comparable between different subjects and different voxels.  Note that one an test simultaneously several contrasts using an F-test. 

## Resting state fMRI
This has been about task-based fMRI, where we study changes in the brain activity in response to some external manipulation. Resting state fMRI is a bit different - we will have a teaser about resting state fMRI analysis after the lunch break.    

## About registration

Note that we need to register the individual t-maps to common template to do group statistics. There are 1-step, 2-step,and 3-step strategies to this.  See Figure 4.3 from page 59 of fMRI data analysis handbook. 

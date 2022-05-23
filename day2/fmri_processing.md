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

We can write the GLM 
<img src="https://render.githubusercontent.com/render/math?math=Y = X\beta \oplus \epsilon">

## Resting state fMRI

## About registration

See Figure xx from yy

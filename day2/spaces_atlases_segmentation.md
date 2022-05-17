# Standard spaces and atlases 

The idea of using a three-dimensional Cartesian coordinate space as a common space for different brains was proposed by the neurosurgeon Jean Talairach. He suggested to use 3-D coordinate system of the human brain to map the location of brain structures independent from individual differences in the size and overall shape of the brain. The Talairach coordinate system is defined based on anatomical landmarks (the anterior commissure (AC), and posterior commissure (PC), the midline sagittal plane, and the exterior boundaries of the brain).  As Talairach space (and the coordinate system) was based on a single post-mortem brain, it is now largely replaced by MNI coordinate system and associated atlases. (See  xxx more information) 

## Definitions
(According to  fMRI handbook)

**Atlas** is a guide to the location of anatomical features in a coordinate space

**Template** is an image that is representative of the atlas and provides a target to which individual images can be aligned. 

Note that the template represents a specific MRI modality while an atlas is independent of the imaging modality.  

**Stereotactic coordinates** or **standard coordinates** are voxel coordinates (x,y,z) in a standard or stereotactic space. The location of (x,y,z) standard coordinates are expected to match between any two images (at least after Gaussian smoothing).

![registration](https://user-images.githubusercontent.com/6709791/168842588-2b1f08d1-863c-4408-990f-90c9ec3e6655.png) 
*Figure from Introduction to MRI by Jonathan Peelle,  licensed under a Creative Commons BY-NC-SA 3.0 License http://jpeelle.net/mri/index.html*

Be aware that there is a lot of fuzziness in the usage of the terminology related 

Registration of the functional MRI to a template (1-step,2-step or 3-step). [Picture]

# MRI segmentation

**Skull stripping or brain extraction** refers to the removal of the skull (and other non-brain tissue) usually from T1-weighted MRI. Lots of research has been done here.

[picture here]
![image](https://user-images.githubusercontent.com/6709791/168875044-e8882ed9-b0c8-4188-9103-0a667c0e7f60.png) 
*Figure from De Feo et al. 2021 https://www.sciencedirect.com/science/article/pii/S1053811921000112?via%3Dihub CC-BY 4.0. Example of MU-Net based skull-stripping.*

![image](https://user-images.githubusercontent.com/6709791/168876381-7284d144-fccd-452b-83fb-f8045ae83a76.png)
*Example of SynthStrip results. Figure from Hoopes et al, 2022 https://arxiv.org/abs/2203.09974 CC-BY-4.0*

**Tissue classification** refers to the classification of voxels to the three main tissue classes (white matter, gray matter, and cerebrospinal fluid).

![image](https://user-images.githubusercontent.com/6709791/168891576-47a1309a-1278-46b7-b307-b11bfc20bc68.png)
*Figure from Tohka 2014 https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4241492/. Used with permission.*

*Bias field correction* and *partial volume effect* are important considerations here. High-resolution T1-weighted images show broad variation in their intensity, due to inhomogeneities in the excitation of the head caused by a number of factors. It must be corrected before or jointly with tissue classification. Partial volume effect refers to the phenomenon that each voxel can contain (and typically does) multiple tissue types. There are numerous ways to take this into account during the segmentation.   

![image](https://user-images.githubusercontent.com/6709791/168880453-7a8e9717-c3a7-4de2-9115-3440d517cd25.png)
*Figure from Tohka 2014 https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4241492/. Used with permission.*

Tissue classified images (in the standard space) can be readily used for *voxel-based morphometry*. Tissue classification can be continued in the extraction of the cortical surfaces and to the measurement of cortical thickness. 

![image](https://user-images.githubusercontent.com/6709791/168894936-abaeb531-bf17-485f-b9df-0c4f817962fc.png) Figure from Hutton et al 2008 https://doi.org/10.1016/j.neuroimage.2008.01.027 CC-BY 3.0. 


**Region segmentation** refers to the segmentation of brain into a regions or volumes of interest. This can be done by probagating atlas labels into the image-to-be-segmented after (nonlinear) registration. However, it might well be that using a single template does not lead to a good enough segmentation, but a majority vote across several template registrations leads to improvements. Convolutional neural network approaches work well, even with a relatively small number of training examples.    

![image](https://user-images.githubusercontent.com/6709791/168890882-f2631eae-1e2e-42c3-8f46-3baa59ba6f05.png)
*Figure from De Feo et al. 2021 https://www.sciencedirect.com/science/article/pii/S1053811921000112?via%3Dihub CC-BY 4.0. Example of MU-Net based segmentation of mouse cortex (blue), ventricles (green), striati (red) , and hippocampi (yellow).*

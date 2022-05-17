# Standard spaces and atlases 

The idea of using a three-dimensional Cartesian coordinate space as a common space for different brains was proposed by the neurosurgeon Jean Talairach. He suggested to use 3-D coordinate system of the human brain to map the location of brain structures independent from individual differences in the size and overall shape of the brain. The Talairach coordinate system is defined based on anatomical landmarks (the anterior commissure (AC), and posterior commissure (PC), the midline sagittal plane, and the exterior boundaries of the brain).  As Talairach space (and the coordinate system) was based on a single post-mortem brain, it is now largely replaced by MNI coordinate system and associated atlases. (See  xxx more information) 

## Definitions
(According to  fMRI handbook)

**Atlas** is a guide to the location of anatomical features in a coordinate space

**Template** is an image that is representative of the atlas and provides a target to which individual images can be aligned. 

Note that the template represents a specific MRI modality while an atlas is independent of the imaging modality.  

**Stereotactic coordinates** or **standard coordinates** are voxel coordinates (x,y,z) in a standard or stereotactic space. The location of (x,y,z) standard coordinates are expected to match between any two images (at least after Gaussian smoothing).

![registration](https://user-images.githubusercontent.com/6709791/168842588-2b1f08d1-863c-4408-990f-90c9ec3e6655.png) From Introduction to MRI by Jonathan Peelle,  licensed under a Creative Commons BY-NC-SA 3.0 License http://jpeelle.net/mri/index.html

Be aware that there is a lot of fuzziness in the usage of the terminology related 

Registration of the functional MRI to a template (1-step,2-step or 3-step). [Picture]

# MRI segmentation

**Skull stripping or brain extraction** refers to the removal of the skull (and other non-brain tissue) usually from T1-weighted MRI. Lots of research has been done here.

[picture here]

**Tissue classification** refers to the classification of voxels to the three main tissue classes (white matter, gray matter, and cerebrospinal fluid).

[picture here]

**Region segmentation** refers to the 

# A short guide to neuroimaging resources

## Books, lecture notes and similar

Poldrack, Mumford, Nichols: Handbook of Functional MRI Data Analysis: [https://www.amazon.com/Handbook-Functional-MRI-Data-Analysis/dp/0521517664/ref=sr_1_1?ie=UTF8&qid=1307113870&sr=8-1] . This is a definite book about fMRI data analysis, very clear and useful also for other modalities. The book is easy to read.  

SPM documentation and books: https://www.fil.ion.ucl.ac.uk/spm/doc/ There are lots of great resources about, for example, statistical analyses. Some of the books are bit old but still very essentials reads.   

A very useful piece of lecture notes http://jpeelle.net/mri/ that nicely completements the previous ones oncentrating on structural MRI. 

FSL https://open.win.ox.ac.uk/pages/fslcourse/website/ and Freesurfer https://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial/ courses are great resources on these partcular packages but also more generally. 

## Software

### Main packages

| Name         | Link                                         | Excels at | License | Limitations |
|--------------|----------------------------------------------|-----------|---------|-------------|
| SPM          | https://www.fil.ion.ucl.ac.uk/spm/software/  | All around software toolbox with a GUI. Runs on top Matlab. Lots of toolboxes by various developers          | GNU GPL (open source, copyleft)        | Runs on top of Matlab    |
| FSL          | https://fsl.fmrib.ox.ac.uk/fsl/fslwiki       | All around software toolbox with a GUI. Geared towards fMRI and DTI. Written in C++.           |        Free for academic use, not free for commercial use https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/Licence |  Licence           |
| Freesurfer   | https://surfer.nmr.mgh.harvard.edu/          | Software toolbox build around the idea of surface based processing. Widely used for structural MRI analyses          | Open source (miscellanous licence)   |             |
| AFNI         | https://afni.nimh.nih.gov/                   | fMRI analysis          |  GNU GPL (open source, copyleft)      |             |
| Ants         | http://stnava.github.io/ANTs/                | Registration          |  Open soure       |             |

### Some other packages/tools

Nearly all software packages can be found here: https://www.nitrc.org/

Insight toolkit https://itk.org/  is an open-source, cross-platform library that provides developers with an extensive suite of software tools for image analysis. Not brain imaging specific. 

CAT12 http://www.neuro.uni-jena.de/cat/ A widely used SPM12 add-on for registration, segmentation, and analysis of structural MRI data (T1-weighted). Many favor this package over SPM12 native tools for the purpose.    

Volbrain https://www.volbrain.upv.es/ An online tool for robust segmentation and volumetry
 
Brainvoagager https://www.brainvoyager.com/ A commercial all around package

fMRIprep https://fmriprep.org/en/stable/ functional magnetic resonance imaging (fMRI) data preprocessing pipeline that is designed to provide an easily accessible, state-of-the-art interface that is robust to variations in scan acquisition protocols and that requires minimal user input, while providing easily interpretable and comprehensive error and output reporting


## Atlases
MNI atlases (human, monkey) http://nist.mni.mcgill.ca/atlases/

## (Open) Data

| Name       |     Link | Description             |      Access conditions |
|------------|----------|------------------------ |------------------------|

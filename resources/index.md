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
 
Brainvoyager https://www.brainvoyager.com/ A commercial all around package

fMRIprep https://fmriprep.org/en/stable/ functional magnetic resonance imaging (fMRI) data preprocessing pipeline that is designed to provide an easily accessible, state-of-the-art interface that is robust to variations in scan acquisition protocols and that requires minimal user input, while providing easily interpretable and comprehensive error and output reporting

BrkRaw https://github.com/BrkRaw/brkraw - a Python-based tool to converting Bruker ParaVision acquisitions to NIfTI format. A two-pass structure: 1) first pass produces an Excel file that the user can correct, 2) the second pass converts the data according to the corrected Excel file. The converted file structure follows BIDS (https://bids.neuroimaging.io/) format. - GNU GPL v3.0

Bruker2nifti https://github.com/SebastianoF/bruker2nifti - a Python-based tool to converting Bruker ParaVision acquisitions to NIfTI format. - MIT Licence

Dicom2nifti https://github.com/icometrix/dicom2nifti - a Python-based tool to converting DICOM to NIfTI format. - MIT Licence 

## Atlases
MNI atlases (human, monkey) http://nist.mni.mcgill.ca/atlases/
SIGMA atlas (rat) https://www.nitrc.org/projects/sigma_template
## (Open) Data

| Name       |     Link                      | Description             |      Access conditions |
|------------|-------------------------------|------------------------ |------------------------|
| ADNI       |https://adni.loni.usc.edu/     | Various kinds of imaging, biomarker, clinical, genetic data on dementia and people-at-risk. ~ 2000 subjects,long follow-up | Access to qualified scientists through an online application |
| AIBL       | https://aibl.csiro.au/        | Australian version of ADNI | Similar to ADNI |
| A4         | https://a4study.org/          | Anti-Amyloid Treatment in Asymptomatic Alzheimer's study, various kinds of imaging and cognitive data, over 4000 participants |   Access to qualified scientists through an online application |
| ADNIDOD    |  https://adni.loni.usc.edu/study-design/#collaborative-studies-container | Connections of TBI and PTSD and AD | Similar to ADNI |   
| PPMI       | https://www.ppmi-info.org/    | Parkinnson's progression markers,  imaging (MRI, DATscan), motor and cognitive testing |  Access to qualified scientists through an online application |
| ABIDE      | https://fcon_1000.projects.nitrc.org/indi/abide/ | Autism spectrum, anatomical and functional MRI| Registration and approval of terms of use |
| ABCD       | https://abcdstudy.org/           | Development, 10000 participants, MRI, cognition, behviour    | Access through NDA, requires university level approval |                 
| NIHPD      |                                  | Healthy development, multisequence MRI, cognition, behaviour | Access through NDA, requires university level approval |   
| HCP        | https://www.humanconnectome.org/ | High-quality MRI from healthy volunteers | 
| ATLAS (v2) | https://fcon_1000.projects.nitrc.org/indi/retro/atlas.html | Stroke lesion segmentation | Registration and approval of terms of use | 


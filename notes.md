### Ideas 

Siamese network can be used for single-particle cryo EM classfication.  

### Where SPI stands in structural biology method?

X-ray crystallographic method contributes significantly to structure
determination of biological samples.  X-ray imaging of non-crysalline biological
sample could be a viable option thanks to the X-ray free electron laser.  

#### roseSingleparticleImagingSymmetry2018

Single-particle imaging (SPI) performed using hard X-ray free-electron lasers
(XFELs) (Altarelli et al., 2006; Emma et al., 2010; Ishikawa et al., 2012) was
proposed more than a decade ago (Neutze et al., 2000; Miao et al., 2001; Gaffney
& Chapman, 2007) as a method of determining the structure of individual
biological samples from viruses to single molecules in their native environment.


#### sunCurrentStatusSingle2018

Soft X-ray FEL.  

<!-- Why SPI is still appealing? -->

However, the potential for studying dynamics at physiological conditions and
capturing ultrafast biological, chemical and physical processes represents a
tremendous potential application, attracting continued interest in pursuing
further method development. In this paper, we give a brief introduction of SPI
developments and look ahead to further method development.


#### shiEvaluationPerformanceClassification2019

<!--

!!! VERY IMPORTANT REFERENCE

This reference provides terminology and concepts in the so-called SPI
classification problem.  

It also reviews previous works as well.  

It also states what datasets are used.  Data preprocessing like normalization etc.  

Model, training strategy, etc.  

Single/multi hit, hit finiding


-->

It is also possible for XFEL pulses to intercept more than one particle during
one exposure, producing scattering patterns with inter- particle interference,
often referred to as ‘multiple hits’, as opposed to the ‘single hits’ that are
the scattering patterns from individual sample particles.

The procedure of identifying the scattering patterns is called ‘hit finding’.

but the challenges in excluding multiple hits remain along with other more
complicated cases.

the term 'pattern identification' is used for hit finding.  

while the term ‘pattern classification’ is used for sorting the patterns of
single sample particles or multiple particles.  

Single-hit diffraction patterns


<!-- Is log necessary? -->

The intensity values were then subjected to logarithm operations to enhance the
features in regions with weaker signals.

<!-- Ground truth -->

It is notable that mistakes in the manually selected training/vali- dation data
could not be completely avoided; thus, these values are not the comparison
results against the ground truth.

<!-- Real time classification capabilities -->

It is possible to manually label 200 single- particle scattering patterns with a
good signal-to-noise ratio within a few minutes, so these methods can
potentially be used for real-time data classification during experiments.

<!-- Accurary -->

A validation dataset containing 500 manually labelled patterns was used to
evaluate the accuracy of the trained models by computing the true positive rate
at a cutoff of 0.5. CNN has a prediction accuracy of 83.8%, and the accuracies
for GC and DM methods are 84.2 and 80.8%, respectively.

To improve: 

- We did not attempt to further classify the non-single- particle scattering
  patterns as the major goal was to distinguish the single-particle data from
  others.



### Work done to overcome the single particle image classification problem

#### bobkovSortingAlgorithmsSingleparticle2015

Image compression and feature extraction with PCA and SVM.  

Dataset consists of simulated images.  

However, this approaach is to distinguish sample types rather than single-hit
from multi-hit.  


#### ignatenkoClassificationDiffractionPatterns2021

YOLO based.

# Qualitative & Quantitative Analysis of Structural MRI Modalities & Segmentation of Tumor Regions

This project was conducted to make a qualitative comparison between T1CE and T2 brain scans, segmentation of tumor regions within the images, and a quantitative comparison of the tumor brain scans. 
The dataset consists of 1 T1CE image and 1 T2 image for the 2 visits to the hospital from 5 subjects each, adding up to a total of 20 images. The MRI images used are considered private and confidential, hence they will not be included in this repository.

## Qualitative Analysis

Qualitative analysis of the T1CE and T2 images was done by spotting the differences between the two modalities visually. Some notable differences are that regions of the brain filled with water appear dark in T1CE images while they appear bright in T2 images, while areas within the brain that contain fatty tissue appear bright in T1CE images but appear dark in T2 images. For instance, the ventricles that are filled with fluid appear dark in T1CE images but bright in T2 images, while brain tumors that contain higher fat content appear bright in T1CE images but dark in T2 images.

## Segmentation of Tumor Regions

Firstly, tumors within the images were identified. Tumors can be identified with the criteria of any irregularly appearing round object within the brain that should not be there are likely to be brain tumors. Then, tumor masks were made for each image using the ITK-SNAP program. Subsequently, The tumor masks were saved as binary masks.

## Quantitative Analysis

Quantitative analysis is performed using the histogram plots from the MRI_tumor_run.ipynb file in this repository. The relevant modules were imported, which are the os, Numpy, Matplotlib, and NiBaBel modules. The files were loaded with functions load_individual_data and load_joint_data. Two functions were created to plot two types of histograms for comparisons, which are plot_individual_histogram and plot_joint_histogram.

### Individual Histograms



### Joint Histograms

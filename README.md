# Qualitative & Quantitative Analysis of Structural MRI Modalities & Segmentation of Tumor Regions

This project was conducted to make a qualitative comparison between T1CE and T2 brain scans, segmentation of tumor regions within the images, and a quantitative comparison of the tumor brain scans. 
The dataset consists of 1 T1CE image and 1 T2 image (both .nii files)for the 2 visits to the hospital from 5 subjects each (labelled 01 to 05), adding up to a total of 20 images. The MRI images used are considered private and confidential, hence they will not be included in this repository.

## Qualitative Analysis

Qualitative analysis of the T1CE and T2 images was done by spotting the differences between the two modalities visually. Some notable differences are that regions of the brain filled with water appear dark in T1CE images while they appear bright in T2 images, while areas within the brain that contain fatty tissue appear bright in T1CE images but appear dark in T2 images. For instance, the ventricles that are filled with fluid appear dark in T1CE images but bright in T2 images, while brain tumors that contain higher fat content appear bright in T1CE images but dark in T2 images.

## Segmentation of Tumor Regions

Firstly, tumors within the images were identified. Tumors can be identified with the criteria of any irregularly appearing round object within the brain that should not be there are likely to be brain tumors. Then, tumor masks were made for each image using the ITK-SNAP program. Subsequently, The tumor masks were saved as binary masks (.nii.gz files).

## Quantitative Analysis

Quantitative analysis is performed using the histogram plots from the MRI_tumor_run.ipynb file in this repository. The relevant modules, which are the os, Numpy, Matplotlib, and NiBaBel modules, were imported. This analysis can be divided into two parts: plotting the individual histograms of each modality and the joint histograms for both modalities within the tumor region.

### Individual Histograms for T1CE and T2
The files were loaded with the function load_individual_data and the individual histograms were plotted with the function plot_individiual_histograms. The folder path that contains the T1CE and T2 images was entered as user input and taken as the argument for the load_individual_data function. After extracting the T1CE and T2 images, they were passed through the plot_individual_histogram function to be plotted. A total of 10 histograms of frequency to pixel intensity were plotted and analyzed for both T1CE and T2 respectively. Some notable observations are that the pixel intensities are more spread out for T1CE and less for T2. This is due to the contrast sensitivity of each modality, where T1CE is more sensitive than T2. Besides that, irregularities within the histogram such as spikes and gaps could be indicators of artifacts.

![Untitled](https://github.com/user-attachments/assets/b4433b90-55f8-45e1-b996-9081d876a200)


### Joint Histograms of T1CE and T2 in Tumor Regions
The files were loaded with functions load_joint_data and the individual histograms were plotted with the function plot_joint_histograms. The folder path that contains the T1CE, T2, and mask images was entered as user input and passed as the argument in the load_joint_data function. The files were grouped into groups that consist of one T1CE, one T2, and one mask image based on the subject label (01 to 05). After creating the datasets, they were passed through the plot_joint_histogram function to be plotted. A total of 10 joint histograms of T2 intensity to T1 intensity were plotted and analyzed.  Some notable observations are that there is a positive correlation between T1CE and T2 modalities. It can be seen that the tumor region in the histograms that possess high frequency of intensity (in bright colors) are of high-intensity values in both T1CE and T2 modalities. Moreover, the size of the tumor displays a correlation with the intensity distribution based on the joint histograms. The larger the size of the tumor, the more concentrated the intensity distribution of the joint histogram will be.

![Untitled-1](https://github.com/user-attachments/assets/b2e77c2a-000d-4dd4-a664-dccd6318fc6d)

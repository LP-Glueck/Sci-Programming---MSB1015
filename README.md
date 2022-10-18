# Sci-Programming README file

## Predicting tumour type from MRI image arrays

We're going to be using MRI scans to classify the tumour type based on the image arrays. 
Overall the script will include:
- General data loading and exploration
- cleaning the data
- Transforming the data
- PCA
- Upsampling
- Model training using:
  - K-Nearest Neighbours
  - Support Vector Machines


Please notice:
Since the entire analysis for review is contained within one script, there should not be any confusion in the order of methods to run. 
Just follow the jupyter notebook as it is and there shouldn't be any problems. 

## Data 
This data is organized in matlab data format (.mat file). Each file stores a structure containing the following fields for an image:

- cjdata.label: 1 for meningioma, 2 for glioma, 3 for pituitary tumor
- cjdata.PID: patient ID
- cjdata.image: image data (512 x 512 matrix)
- cjdata.tumorBorder: a vector storing the coordinates of discrete points on tumor border.
- cjdata.tumorMask: a binary image with 1s indicating tumor region

We will ignore the tumorBorder and Mask variables.


## Aim of analysis: 
Overall we aim to explore, clean and transform the data in such a way to obtain more informative variables within reduced dimensions. 
We then will upsample using the SMOTE algorithm. 
From these upsampled data variables, we will train and test classification models to predict the type of tumour from each sample based on these newly transformed and partly synthesized data.
As well, 
involving: 
- Removing patients with different image sizes
- Flattening the images to one-dimensional arrays
- Perform PCA on the original samples
- Upsample the training set 
- Train two classification models on the upsampled data. 

You need to perform the analysis in the order as it comes in the jupyter notebook. 

If you have any problems, or issues. 
Please let me know, you can contact me at the email: l.glueck@student.maastrichtunvirsity.nl

Enjoy! 








# Brain-Tumor-Segmentation-and-Survival-Prediction-using-Deep-Neural-Networks


## Dataset
BraTS 2017 and 2018 data can be found on Kaggle.


## Resources

- https://arxiv.org/pdf/1505.03540.pdf : Patch based Brain Tumor Segmentation
- https://www.biorxiv.org/content/10.1101/760157v1.full.pdf : Encoder Decoder network with dice loss
- https://arxiv.org/pdf/1802.10508v1.pdf : Unet 3D
- https://arxiv.org/abs/1606.04797 : VNet 3D
- https://arxiv.org/pdf/1903.11593.pdf : Survival Prediction Idea of extracting features
- https://link.springer.com/chapter/10.1007/978-3-319-75238-9_17 : Integrating results along the 3 axis and different models
- https://link.springer.com/chapter/10.1007/978-3-319-75238-9_30: Inception U-Net
- https://link.springer.com/chapter/10.1007/978-3-319-75238-9_15 : Pooling free DenseNet architecture



## Task
Task is of segmenting various parts of brain i.e. labeling all pixels in the multi-modal MRI images as one of the following classes:
- Necrosis
- Edema
- Non-enhancing tumor
- Enhancing tumor 
- Everything else

Brats 2015 dataset composed of labels 0,1,2,3,4 while Brats 2017 dataset consists of only 0,1,2,4.

## BRATS Dataset 
I have used BRATS 2017 training dataset for the analysis of the proposed methodology. It consists of real patient images as well as synthetic images created by MICCAI. Each of these folders are then subdivided into High Grade and Low Grade images. For each patient, four modalities(T1, T1-C, T2 and FLAIR) are provided. The fifth image has ground truth labels for each pixel. The dimensions of images are (240,240,155) in both.

![](Captures/Dataset.png)


## Dataset pre-processing 
Model has been trained on only those slices having all 4 labels(0,1,2,4) to tackle class imbalance and label 4 has been converted into label 3 (so that finally the one-hot encoding has size 4).

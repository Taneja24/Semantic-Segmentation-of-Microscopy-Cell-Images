# Semantic-Segmentation-of-Microscopy-Cell-Images
Identify microscopy cells in biomedical images using semantic segmenting with U-Net Architecture

TRAINING DATA
- 670 microscopic images
- 15-40 masks per each images
- Various type of images and cells

PRE PROCESSING  
- WHAT? New mask generation: Add cell boundaries.
- WHY? To improve prediction, get the exact mask of the images and prevent mistakes when there is cell superposition. 
- HOW? OpenCV.

Augmentation  
- WHAT? Data augmentation to create more images instead of hiring technicians to manually annotate 
- WHY? Increase in training images could lead to improvement in performance
- HOW? Using Albumentations package in Python

MODEL ARCHITECTURE  
U-Net is a fully convolutional network use for image segmentation adapted to medical imaging. 
It localise and distinguish borders by performing class prediction on each pixels.

MODEL PERFORMANCE
- IoU : We stop training after 20 epochs as Mean IoU improvement was saturated.
- Loss : Loss on Train and Validation data reduced consistently over 20 epochs without signs of overfitting

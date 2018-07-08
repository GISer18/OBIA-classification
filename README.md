# OBIA CLASSIFICATION

Implementation of OBIA algorithm for classification photo from unmanned aerial vehicle.  
The input data is the aerial image in 3 channels RGB (["ortho.png"](https://github.com/trojanskehesten/OBIA-classification/blob/master/ortho.png)) and digital model - DM (["dm.png"](https://github.com/trojanskehesten/OBIA-classification/blob/master/dm.png)).  
For training labeled image ["train_with_shadows.png"](https://github.com/trojanskehesten/OBIA-classification/blob/master/train_with_shadows.png) is used.
DM = Digital Terrain Model (DTM) - Digital Surface Model (DSM).  
Orthophoto, DTM and DSM are got from Agisoft PhotoScan software. Subtraction is implemented and labels are created in ArcMap software.  
In the example, I classified objects on the aerial image to 3 categories: trees, grassland and roads.
  
OBIA algorithm which is used here:  
  1. Upload 2 images (aerial photo and DM) and sum it to one 4-bands image.  
  2. Create segmentation (Quickshift and Felszenwalb segmentation are used).  
  3. Upload labels and train. Ensemble "Random Forest Tree" is used.
  4. Save classification to the file.

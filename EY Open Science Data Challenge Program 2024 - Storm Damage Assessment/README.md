# EY Open Science Data Challenge Program 2024
## Objective

The goal of the challenge is to develop a machine learning model to identify and detect “damaged” and “un-damaged” coastal infrastructure (residential and commercial buildings), which have been impacted by natural calamities such as hurricanes, cyclones, etc.

Participants will be given pre- and post-cyclone satellite images of a site impacted by Hurricane Maria in 2017 and build a machine learning model, designed to detect four different objects in a satellite image of a cyclone impacted area:
- Undamaged residential building
- Damaged residential building
- Undamaged commercial building
- Damaged commercial building

## Dataset Used

**Mandatory dataset**: High-resolution panchromatic satellite images before and after a tropical cyclone: Maxar GeoEye-1 (optical)
**Optional datasets**: Moderate-resolution satellite data: Sentinel-2 (optical), Sentinel-1 (radar)

## Method
- Convert the Pre_Event_San_Juan.tif files to jpg files
- Annotate the jpg files using LabelMe
- Download the annotated images in YOLOv8 required format
- Split the images into train, test and val dataset
- Finetune the YOLO model, then test and make inferences on submission data

In this competition, I have achieved an overall MAP50 score of 0.43, higher than the baseline models of 0.34. The strategies employed are:
1. Increasing data, especially damaged data: enriching the dataset with more examples, especially those that represent 'damaged' scenarios, likely improved the model's ability to generalize and detect nuanced features.
2. Experimenting with different YOLO Models: switching between different YOLO architectures (like YOLOv3, YOLOv4, etc.) might have helped in identifying a model structure that better fits the specific data tasks and characteristics. Some models also have a much higher number of parameters, which may perform better.
3. Hyperparameter search: optimizing hyperparameters can significantly influence the performance of deep learning models by fine-tuning their learning process and adaptation to the training data.
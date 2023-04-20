# Land Cover Classification of Satellite Images
**Aidan O'Keefe**

## Overview
A deep learning (neural network) land cover classification project using RGB satellite images (remote sensing) across 10 classes. This land cover classifier could be used by nature conservancies to monitor deforestation/land development using satellite images to observe if land starts changing from one class (forest, vegetation,etc) to another class (industrial, crop, etc). From a Baseline Model with a performance of 74.1% Test accuracy, I iterated until reaching my final model, a Fine Tuned VGG16 Model with additonal Dense and Dropout Layers with a 91.46% Test accuracy. 

<img width="730" alt="LandCoverClasses" src="https://user-images.githubusercontent.com/120589094/231884775-4add3081-b666-45d7-ac91-dd9b9c0cd501.png">
*Samples of each of the Land Cover Classes; from top left- Annual Crop, Forest, Herbaceous Vegetation, Highway, Industrial, Pasture, Permanent Crop, Residential, River, Sea or Lake*

## Business Understanding
The Nature Conservancy (TNC) is looking to help protect wildlife migration corridors from development/deforestation, but they can’t be everywhere at once.

In order to help them find where to focus their efforts, we want to build Land Cover Classifier so that TNC can monitor deforestation using satellite images to observe if land starts changing from forest or vegetation to another class.

## Data Understanding
For this project, I am using RGB satellite images from [EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification](https://zenodo.org/record/7711810#.ZD7rSezMJQL).

This dataset contains 27,000 RGB Satellite Images across 10 classes:

- Annual Crop
- Forest
- Herbaceous Vegetation
- Highway
- Industrial
- Pasture
- Permanent Crop
- Residential
- River
- Sea or Lake

There are about 2,500 images per class.

## Modeling and Evaluation
I used a variety of Convolutional Neural Networks to classify the image data. Compared to my Baseline Model's performance of 74.1% Test accuracy, my final model was Model 16 (a Fine Tuned VGG16 Model with additonal Dense and Dropout Layers) with a 91.46% Test accuracy.

**Structure of Final Model (Model 16)- a fine-tuned VGG16 model using augmented training data.** 
<img width="598" alt="FinalModelArch" src="https://user-images.githubusercontent.com/120589094/233229580-c0aa8d6f-4637-4bc0-a510-bced8f1411e7.png">

**Training/Validation Loss and Accuracy of Final Model**
<img width="637" alt="FinalModel_Loss" src="https://user-images.githubusercontent.com/120589094/232880527-70e5bae4-ab2d-4bbe-91f3-b7202b32ccfd.png">

<img width="612" alt="FinalModel_Accuracy" src="https://user-images.githubusercontent.com/120589094/232880554-8fdd7a58-2c36-4cde-912b-1b6dfe35d01a.png">

**Test Prediction Accuracy by Class**

![FinalModel_ConfusionMatrix](https://user-images.githubusercontent.com/120589094/232880674-9485bde3-eecd-478c-817b-a1349c86b3d6.png)

## Conclusion
I would recommend to use this land cover classifier tool on images of the same land area over time. By observing where an image’s class has changed over time, TNC could focus deforestation prevention efforts on areas where images are changing from a natural classification (Forest, Herbaceous Vegetation) to a developed classication (Crops, Highways, Industrial, Residential, etc).

Next, I would work to refine my model to better differientiate between confused classes (i.e. river and highway), possibly through preprocessing. Additionally, I would like to incorporate object detection into this project to help classify multiple areas of land cover within a singular image.

## References
[1] Eurosat: A novel dataset and deep learning benchmark for land use and land cover classification. Patrick Helber, Benjamin Bischke, Andreas Dengel, Damian Borth. IEEE Journal of Selected Topics in Applied Earth Observations and Remote Sensing, 2019.

[2] Introducing EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification. Patrick Helber, Benjamin Bischke, Andreas Dengel. 2018 IEEE International Geoscience and Remote Sensing Symposium, 2018.

## Repository Structure
├── [data](https://github.com/aokdata/Land_Cover_Classification/tree/main/data)<br>
├── [.gitignore](https://github.com/aokdata/Land_Cover_Classification/blob/main/.gitignore)<br>
├── [Land_Cover_Classification_Notebook.ipynb](https://github.com/aokdata/Land_Cover_Classification/blob/main/Land_Cover_Classification_Notebook.ipynb)<br>
├── [README.md](https://github.com/aokdata/Land_Cover_Classification)<br>
└── [presentation.pdf](https://github.com/aokdata/Land_Cover_Classification/blob/main/presentation.pdf)<br>


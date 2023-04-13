# Land Cover Classification of Satellite Images
**Aidan O'Keefe**

## Overview
A deep learning (neural network) land cover classification project using RGB satellite images (remote sensing) across 10 classes.

<img width="730" alt="LandCoverClasses" src="https://user-images.githubusercontent.com/120589094/231884775-4add3081-b666-45d7-ac91-dd9b9c0cd501.png">
*Samples of each of the Land Cover Classes; from top left- Annual Crop, Forest, Herbaceous Vegetation, Highway, Industrial, Pasture, Permanent Crop, Residential, River, Sea or Lake*

## Business Understanding
The Nature Conservancy (TNC) is looking to help protect wildlife migration corridors from development/deforestation, but they can’t be everywhere at once.

In order to help them find where to focus their efforts, we want to build Land Cover Classifier so that TNC can monitor deforestation using satellite images to observe if land starts changing from forest or vegetation to another class.

## Data Understanding
For this project, I am using RGB satellite images from EuroSAT: A Novel Dataset and Deep Learning Benchmark for Land Use and Land Cover Classification.

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
I used a variety of Convolutional Neural Networks to classify the image data. Compared to my Baseline Model's performance of 74.1% Test accuracy, my final model was Model 8 with a 78.01% Test accuracy.

## Conclusion
I would recommend to use this land cover classifier tool on images of the same land area over time. By observing where an image’s class has changed over time, TNC could focus deforestation prevention efforts on areas where images are changing from a natural classification (Forest, Herbaceous Vegetation) to a developed classication (Crops, Highways, Industrial, Residential, etc).

Next, I would like to incorporate object detection into this project to help classify multiple areas of land cover within a singular image.

## Repository Structure
<br>
├── [data](https://github.com/aokdata/Land_Cover_Classification/tree/main/data) <br>
├── [.gitignore](https://github.com/aokdata/Land_Cover_Classification/blob/main/.gitignore) <br>
├── [Land_Cover_Classification_Notebook.ipynb](https://github.com/aokdata/Land_Cover_Classification/blob/main/Land_Cover_Classification_Notebook.ipynb) <br>
├── [README.md](https://github.com/aokdata/Land_Cover_Classification) <br>
└── presentation.pdf (NOT YET UPLOADED) <br>


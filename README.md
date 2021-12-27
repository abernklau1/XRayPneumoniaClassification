# X-Ray Pneumonia Classification

**By**: Andrew Bernklau, Carlos McCrum, Jared Mitchell

## Overview
The goal of this project is to create an image classification model that can successfully classify between X-rays of uninfected and infected lungs. The data set we're using is a set of five and a half thousand X-ray images from Guangzhou Women and Children’s Medical Center. The data has around a four to one ratio between infected lung images and uninfected lung images. After testing a few models, the model that we chose to use was a Convolutional neural network (CNN).

## Business Problem
Death rate from Pneumonia has hit with an all time high. As of 2018 the cdc reported 1.5 mil ER visits, a 16% increase in total deaths in 2020, and among those deaths and more around the world the WHO reports ~2.5 mil deaths of children under five every year. Due to this large number of deaths, Pneumonia is consistently estimated as the leading cause of childhood mortality. The Guangzhou Women and Children's Medical Center recognizes the severity of this problem and has asked us to build an image classification model that correctly identifies between x-rays of lungs infected with Pneumonia and lungs that are healthy. 

## Data
Our data includes 5.5k X-ray images from the Guangzhou Women and Children’s Medical Center. Our data was also ethically obtained. The data did contain some significant class imbalance. We had four times as many images of infected lungs compared to images of uninfected lungs.

## Methods
![CNN image](https://user-images.githubusercontent.com/82346896/142509391-253d3584-9229-49d7-9fbb-fa67b224fcca.JPG)

Our model was a CNN model. The way this model works is by taking our input image, then running that image through the tuned layers of the model, and then outputs a classification for the image. Image classification models work better with more images, so we used image augmentation within our model to effectively train it on more images without actually collecting more X-rays. This ended up being very helpful with our models' accuracy. 

## Results
The final accuracy of our model was 91%. We're pretty confident in our model's outcome, and are confident that it could be used to help screen patients X-rays. That being said, it can't be used as a stand alone tool. The model would misdiagnose too many patients if used alone.  

## Conclusions
We recommend our model be used in tandem with a doctor's opinion. The model could act as a second check to support the doctor and even catch misdiagnoses from the doctor. If we wanted our model to get even closer to 100% accuracy then we would need more data. With the limited amount of images we did it was challenging to properly train the model. On top of that, getting some demographic info on each patient could be very helpful for our model as well. Things like pre-existing conditions and other possible risk factors for pneumonia. 
## For More Information

Please review our full analysis in our [Jupyter Notebook](./chest_xray_image_classification.ipynb) or our [presentation](./xray_image_classification_pres.pdf).

## Repository Structure

```
├── code
│   ├── __init__.py
│   ├── preparation.py
│   └── preparation.py
├── data/chest_xray
│   ├── test/
│   ├── train/
│   └── val/
├── .gitignore
├── README.md
├── chest_xray_image_classification.ipynb
└── xray_image_classification_pres.pdf
```

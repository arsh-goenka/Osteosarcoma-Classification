# Osteosarcoma-Classification
By: Arsh Goenka

Try out the web app: https://arsh-goenka-osteosarcoma-classification-web-app-3gwog2.streamlitapp.com/

## Problem
Osteosarcoma is a type of bone cancer in which early detection is critical in treatment efforts. Worldwide there is 3.4 million cases each year and it metastasizes incredibly quickly posing issues with treatment and recovery making osteosarcoma deadly. Current diagnoses is done through multiple test including blood tests, X-rays, CTs, histological imaging, and MRIs making diagnoses long and very expensive.

## Solution
To use deep learning to quickly and accurately diagnose osteosarcoma from histological images. Not only can the deep learning model diagnose osteosarcoma it can also tell clinicans wheter the tumor is viable (can be operated on) or necrotic (cannot be operated on). 

## Dataset
https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=52756935

1,144 images of size 1024 X 1024 with 536 (47%) non-tumor images, 263 (23%) necrotic tumor images, and 345 (30%) viable tumor images.

## Pre-Processing
1. CSV files had some annotations that were copies that had to be removed.
2. Annotations were not in the same order of the images given.
3. Image size of 1024 X 1024 was too large for running our model because of RAM constraints.
4. Data was split into Train (63%), Validation (18%), and Test (19%) sets.

## Binary Model
Two Classes: Osteosarcoma Positive, consists of viable and necrotic tumors; Osteosarcoma Negative, consists of non-tumors

DenseNet121:
98.6% Accuracy |
0.986 AUC

## Multiclass Model
Three Classes: Viable Tumor, tumor can be operated on; Necrotic Tumor, tumor cannot be operated on: Non-Tumor, no tumor

InceptionV3:
92.56% Accuracy | 
0.978 AUC

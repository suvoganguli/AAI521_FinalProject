


# Face Recognition using FaceNet and DeepFace

AAI-521 Final Team Project Report - Group 2

Authors: Mohammad Alkhawaldeh, Narendra Fadnavis, Subhabrata Ganguli (Project Lead)

Course: Advanced Computer Vision

University of California San Diego

---
## Introduction

Facial recognition has become a pivotal technology in modern computer vision, finding applications in security, authentication, and social networking platforms. The purpose of this project, titled Face Recognition using FaceNet and DeepFace, is to develop and evaluate a face recognition system leveraging two state-of-the-art deep learning models, FaceNet and DeepFace. This study aims to compare their performances on the widely used Labeled Faces in the Wild (LFW) dataset.

The LFW dataset, hosted by the University of Massachusetts Amherst, is a benchmark dataset for evaluating unconstrained face recognition models. It consists of 13,233 images of 5,749 individuals, collected from the web using the Viola-Jones face detection algorithm. Among the dataset, 1,680 individuals have two or more distinct images, making it ideal for evaluating facial recognition systems. The images in the dataset are pre-processed and centered, ensuring consistency across samples. This project utilizes this dataset to assess how effectively the FaceNet and DeepFace models can identify and differentiate faces under real-world, unconstrained conditions.

---

The main file to use in Final_Project.ipynb. It is expected that the notebook is uploaded to Google Drive is executed in Google Colab.

The code is written such that it extracts the tar zipped dataset in the user's Google Drive in a folder called lfw in: 
'/content/drive/MyDrive/AAI521_FinalProject'

The code is divided into three sections:
a) Data Preprocessing and EDA
b) Face Verification
c) Face Identification

The **Data preprocessing and EDA** step consists of loading the images from the dataset. Corresponding labels are created based on the subfolder name, which designates the name of the person. The data is split into training and test sets for image classification.

The EDA does the following:

- Folder Summary
- Image Size Analysis
- Treemap for top class
- Image Quality Assessment
- Duplicate Analysis

The **Face Verification** code focuses on implementing a face verification system using **DeepFace embeddings** and **cosine similarity** to determine whether two facial images belong to the same person. The system evaluates its performance across randomly selected image pairs, adjusting thresholds for different sensitivity levels.

The **Face Identification** code used **FaceNet and DeepFace embeddings** to design two classifiers - one based on Logistic Regression and another based on SVC. The goal is to classify a test image based on a model trained with training images. Further analysis is done to see why in certain cases, image classification fails. Also, additional code is written to analyze the effect of image resolution on image classification.







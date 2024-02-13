# Terrastack
Terrastack Satellite Agri-Modeling

# Crop Growth Stage Classification Using Machine Learning

## Introduction

This project aims to develop a machine learning model for classifying the growth stages of crops based on clipped raster data. The dataset consists of clipped rasters for 569 geographical grid cells (GIDs) across 12 agricultural months. The task involves creating a model that accurately classifies the growth stage of crops into the following categories: 'no_crop', 'growing', and 'lush'.

## Data Exploration

The initial step involved a thorough exploration of the dataset to understand its characteristics. This exploration included analyzing the distribution of data across different classes, visualizing sample images, and identifying any potential challenges or patterns in the data.

- After Data Analysis we noted that the all images in the dataset didn't have the same shape. So, we plotted the height and width of the images to analyse them 
- After analysis we got these results : Analysis of sample raster image ![image](https://github.com/skillingshark/Terrastack/assets/117962699/dd705c32-a884-42e3-bcc6-4f670acb0224)

![image](https://github.com/skillingshark/Terrastack/assets/117962699/03664676-4ed6-4e57-a85d-896e26a86cf9)


  ![image](https://github.com/skillingshark/Terrastack/assets/117962699/94dbaff7-c72b-49c2-85da-88d358263379)  ![image](https://github.com/skillingshark/Terrastack/assets/117962699/e123bca8-3b50-46f9-a8ca-6eebf416a529)

 

  ![image](https://github.com/skillingshark/Terrastack/assets/117962699/60e0dbee-a2e8-4b90-b9d6-007537bc378f)


## Feature Engineering

Preprocessing and feature engineering techniques were implemented to ensure optimal model performance. The data was preprocessed to determine the average size of images, which were then converted into tensors for further processing. Additionally, any necessary normalization or scaling was performed to prepare the data for model training.

## Model Selection

For crop growth stage classification, a Variational Autoencoder (VAE) using Convolutional Neural Network (CNN) layers was selected. The VAE encodes tensor images into a lower-dimensional latent space and decodes them back to their original dimensions. This model is effective for noise removal and obtaining a lower-dimensional latent vector, which was used for clustering.

## Clustering with Gaussian Mixture Model (GMM)

The latent vectors obtained from the VAE were used for clustering using a Gaussian Mixture Model (GMM). The GMM is a probabilistic model that assumes the data points are generated from a mixture of Gaussian distributions with unknown parameters. In this project, the GMM algorithm was employed to cluster the latent vectors into three classes: 'no_crop', 'growing', and 'lush'.

![image](https://github.com/skillingshark/Terrastack/assets/117962699/82382195-7a30-4417-8167-04f34294f845)

![image](https://github.com/skillingshark/Terrastack/assets/117962699/6b4153df-60ac-403c-860a-1262731a8380)

## Evaluation

As it was an unsupervised learning model so we could not evaluate the model for accuracy details.



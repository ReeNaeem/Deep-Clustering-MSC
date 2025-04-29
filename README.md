# Deep-Clustering-MSC
This repository contains the implementation for a Deep Clustering Embedded Convolutional Variational Autoencoder (DCEC) designed for the reconstruction and clustering of EEG topographic maps. EEG data were preprocessed into 40×40 spatially structured topographic representations using Azimuthal Equidistant Projection and cubic interpolation.

The model architecture integrates a Convolutional Variational Autoencoder (C-VAE) with a clustering layer, enabling simultaneous feature extraction and latent space clustering. Pretraining was conducted with a custom loss function combining Maximum Mean Discrepancy (MMD) and Negative Log Likelihood (NLL) to optimise latent space structure. Joint training was then performed with an additional Kullback-Leibler Divergence (KLD) loss, using dynamic loss weighting based on the Coefficient of Variation (CoV) to stabilise training.

Model evaluation included reconstruction metrics (SSIM, MSE, MAE) and clustering validation indices (Silhouette Score, Calinski-Harabasz Score, Davies-Bouldin Index). The implementation used TensorFlow and Keras, with experiments conducted in Google Colab utilising GPU acceleration.

This project contributes to unsupervised EEG representation learning, focusing on improving feature disentanglement and the clustering of spatial brain activity patterns.

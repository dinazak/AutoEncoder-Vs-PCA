# Autoencoders

This repository contains code for training an autoencoder (with CNN layers) to encode and decode images. The autoencoder is trained as a denoising autoencoder, where input images are corrupted with noise and then reconstructed by the autoencoder.

## Problem Description

The task is to train a denoising autoencoder that can encode and decode images. The autoencoder is trained using a dataset of colored images and is evaluated by comparing the reconstructed images with the original images. Additionally, the autoencoder is tested on custom images (outside the dataset) by adding noise to the images and reconstructing them.

## Dataset

The dataset used for training the autoencoder consists of colored images. The dataset include at least three different backgrounds or scenery and contain of 385 different images for training. The image size 256x256 pixels.

## Noise

The noise used in the denoising autoencoder is random noise sampled from any distribution. used the Gaussian (normal) distribution for generating the noise for both the image and the encoded vector. 

## Autoencoder

The autoencoder is implemented using CNN layers. It is trained to encode a vector of size between 8-16 for a small-sized autoencoder and 32-80 for a moderate-sized autoencoder. Two separate autoencoders should be trained for each size range. The autoencoders are saved after training for future use.

## Testing and Evaluation

The trained autoencoders are tested on custom images (outside the dataset) by adding noise to the images and passing them through the autoencoder for reconstruction. The reconstructed images are compared with the original images to evaluate the performance of the autoencoder. The process is repeated for three or more custom images, and the decoded images are shown and compared with the original images.

## Extra/Bonus

As an extra or bonus task, train multiple autoencoders to encode vectors of sizes 8, 16, 32, 64, or more. Additionally, apply PCA reduction and restoration on the same custom image using different numbers of components (e.g., top 8, 16, 32, 64 components). The restored images using PCA and the decoded images from the autoencoders are compared and analyzed to observe any differences or similarities.

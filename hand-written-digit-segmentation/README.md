# Handwritten Digit Segmentation using U-Net

## Overview
This learning-based project demonstrates how to segment handwritten digits from the MNIST dataset using a U-Net model.

## Steps:

1. **Load and Preprocess the MNIST Dataset:**
   - Load the MNIST dataset using `tf.keras.datasets.mnist.load_data()`.
   - Normalize pixel values to the range [0, 1].
   - Create segmentation masks by thresholding the images.
   - Reshape the data to add a channel dimension for U-Net.

2. **Build the U-Net Model:**
   - Define the U-Net architecture using `tensorflow.keras` layers.
   - The model consists of a contracting path for downsampling and feature extraction, an expanding path for upsampling and segmentation mask reconstruction, and skip connections to preserve details.

3. **Train the Model:**
   - Compile the model using the Adam optimizer, binary cross-entropy loss, and accuracy metric.
   - Train the model on the training data, validating on a separate validation set.

4. **Evaluate and Visualize:**
   - Evaluate the model's performance on the test data.
   - Visualize the original image, ground truth segmentation mask, and predicted segmentation mask for random samples.

## Results:

The U-Net model achieves high accuracy in segmenting handwritten digits, effectively separating them from the background. The predicted segmentation masks closely resemble the ground truth masks, demonstrating the model's ability to learn the underlying patterns of digit shapes.

## Conclusion:

U-Net is a powerful architecture for image segmentation tasks, including handwritten digit segmentation. Its ability to capture both local and global context makes it well-suited for accurately delineating objects within images. This project provides a starting point for further exploration of U-Net and its applications in image segmentation.
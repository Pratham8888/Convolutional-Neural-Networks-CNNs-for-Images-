# Convolutional-Neural-Networks-CNNs-for-Images:
# Fashion-MNIST Image Classification with CNNs

**Project Status:** Completed

## Objective
The goal of this project was to build and train a Convolutional Neural Network (CNN) to accurately classify 28x28 pixel grayscale images of clothing from the Fashion-MNIST dataset into 10 distinct categories.

## Dataset
This project uses the Fashion-MNIST dataset, which contains 70,000 images from 10 different clothing categories. The dataset is pre-split into a training set of 60,000 images and a testing set of 10,000 images.

## Process
1.  **Data Loading:** The dataset was loaded directly from the `keras.datasets` library.
2.  **Preprocessing:**
    * Pixel values were **normalized** from the original 0-255 range to a 0-1 range to help the model train more efficiently.
    * Images were **reshaped** to include a color channel dimension `(28, 28, 1)`, which is the format expected by the convolutional layers.
3.  **Model Architecture:** A sequential CNN was built using the following layers:
    * `Conv2D` (32 filters) -> `MaxPooling2D`
    * `Conv2D` (64 filters) -> `MaxPooling2D`
    * `Flatten`
    * `Dense` (128 neurons) -> `Dense` (10 neurons with `softmax`)
4.  **Training & Evaluation:** The model was compiled using the `adam` optimizer and `sparse_categorical_crossentropy` loss function. It was then trained for 10 epochs and evaluated on the unseen test set.

## Results
The CNN model achieved a final accuracy of approximately **90%** on the test set, demonstrating its effectiveness in classifying the clothing images.

## What I Learned
* How to build a complete CNN architecture from scratch using Keras.
* The importance of preprocessing image data, including normalization and reshaping.
* The role of `Conv2D`, `MaxPooling2D`, and `Flatten` layers in extracting features from images.
* How to apply deep learning to a real-world computer vision problem.

# Deep Learning Image Search

By [Christian Sada](https://www.linkedin.com/in/christian-sada-716426169/)

## Introduction

**Image search engines:** Generally, a search engine takes a query and returns results. An image search engine takes an input image as an image query, then finds "similar" images within its indexed database and returns them as the search result.

## Methodology

### Similarity Measurement
- **Pixel Space:** Measure the Euclidean distance between two images in the pixel space. However, this method may consider images with similar pixel values as similar, even if they are conceptually different.
- **Feature Space:** Use the feature space instead of pixel space when computing the Euclidean distance between two images. This approach projects images into a space where images with similar features are close to each other.

### Feature Extraction
- Utilize a pre-trained generic network like InceptionV3 to extract high-level features from images. By feeding an image into the network, we obtain a feature vector summarizing the content of the input image.

### Dataset
- Caltech 101 dataset is used in the examples, focusing on 9 classes: 'airplanes', 'Motorbikes', 'Faces', 'Faces_easy', 'Leopards', 'car_side', 'grand_piano', 'brain', 'butterfly'.

## Implementation Steps

1. **Data Preparation:** Download the data, preprocess it, and split it into training and testing sets.
2. **Feature Extraction:** Utilize the pre-trained InceptionV3 model to extract features from images.
3. **Image Search:** For a query image, compute its feature vector and find the nearest images in the dataset based on Euclidean distance.
4. **Visualization:** Visualize the results using t-SNE to reduce dimensionality and plot images.

## Code Overview

- Load and preprocess the Caltech 101 dataset.
- Utilize InceptionV3 for feature extraction.
- Implement image search using Euclidean distance.
- Visualize the results using t-SNE.

## Conclusion

This project demonstrates the implementation of a deep learning-based image search engine using pre-trained neural networks and feature extraction techniques. By following the provided steps, users can conduct image searches and visualize the results effectively.

Feel free to explore and modify the code according to your requirements!


# Generative Adversarial Network (GAN) for Generating MNIST-like Images

This repository contains the code for a simple GAN implementation using Keras to generate images similar to the MNIST dataset.
GANs are a class of machine learning models used for generative tasks, where they learn to generate 
data that is similar to a given training dataset. In this case, we're generating handwritten digit images.

## What is a GAN?

A Generative Adversarial Network (GAN) consists of two neural networks, a Generator, and a Discriminator, 
which are trained simultaneously through a competitive process. The main idea behind GANs is to have these 
two networks play a game against each other:

- **Generator**: This network takes random noise as input and tries to generate data (in our case, images)
 that is indistinguishable from real data (MNIST digits). It learns to create increasingly realistic images as it trains.

- **Discriminator**: This network, on the other hand, tries to distinguish between real data (from the MNIST
  dataset) and fake data generated by the Generator. It learns to become better at distinguishing real from fake images.

During training, the Generator aims to generate images that are so realistic that the Discriminator can't tell them apart
from real images. The Discriminator, in turn, aims to become better at distinguishing real from fake images. This adversarial 
process continues until the Generator produces high-quality fake data.

## How to Use This Code

### Prerequisites

Before running the code, make sure you have the following libraries installed:

- Keras
- NumPy
- Matplotlib
- TensorFlow (or another backend for Keras)

### Running the Code

- Clone this repository to your local machine:

```bash
git clone <repository-url>
cd <repository-directory>
```

- Run the `gan_mnist.py` script to train the GAN:

```bash
python gan_mnist.py
```

- This script will train the Generator and Discriminator for a specified number of epochs, generating MNIST-like images along the way.

### Model Evaluation

The model can be evaluated using a separate script or Jupyter Notebook to generate and visualize fake images produced by the Generator. 
The saved generator model can be loaded and used for this purpose.

## Model Architecture

### Generator

The Generator network consists of several fully connected (Dense) layers followed by Batch Normalization and LeakyReLU activation functions. 
It takes a random noise vector as input and produces an image.

### Discriminator

The Discriminator network is a binary classifier that takes an image as input and outputs a probability indicating whether the input image is real or fake.

### Training

The training process involves alternating between training the Generator to generate more realistic images and training the Discriminator 
to better distinguish real from fake images. This adversarial training continues for a specified number of epochs.

## Sample Images

During training, sample images are generated and saved at regular intervals. These images can be viewed in the `images/` directory.


By Alish Shrestha

# Autoencoder

This repository is developed for an Encoder - Decoder model which is connected to a Multilayer Perceptron in order to classify MNIST images. There are total of 10 classes in this dataset including handwritten digits from 0 to 9.

[MNIST](https://www.kaggle.com/datasets/hojjatk/mnist-dataset) dataset is called from torchvision.dataset.

***Some Image Samples From the Dataset***

<a href="url">
  <img src="https://github.com/ekaraali/Autoencoder/blob/main/images_/mnist_dataset.png?raw=true" height="250" width="400">
</a>
                                                                                                                     
# Introduction

This repo has an original Encoder - Decoder architecture consisting of Conv2D and Pooling layers, and a classifier that is solely multilayer perceptron. This model includes a total of **7000** images.

  - 6000 images are spared for training whereas the remaining 1000 images are utilized for testing the model.
  - This model is trained with the following parameters:
    - Loss function -> MSE Loss (Autoencoder) ve CrossEntropy Loss (Multilayer Perceptron)
    - Optimizer -> Adam
    - Learning rate -> 0.001
    - Batch size -> 100
    - Epoch number -> 20

All necessary codes can be found in [**google colab**](https://github.com/ekaraali/Autoencoder/blob/main/Encoder_Decoder_on_MNIST_Dataset.ipynb) folder, and parameters can be updated by editing related lines.

# Results

After the feature extraction model works appropriately, 2 different approaches are applied for the classification task:
  
  1 - The loss function only applies to the MLP model <br/>
  2 - The loss function applies to both Encoder and MLP models simultaneously.
  
For the first approach, accuracy result is obtained as **87.34%** while the second approach's result is **93.18%** as expected.

Training loss curve can be seen in below:

<a href="url">
  <img src="https://github.com/ekaraali/Autoencoder/blob/main/images_/loss_curve.png?raw=true" height="300" width="400">
</a>


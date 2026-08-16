# CNN Image Classification with PyTorch — FashionMNIST

## Student Information

- Student ID: 220129
- Framework: PyTorch
- Dataset: FashionMNIST
- Task: Image Classification

## Project Description

This project implements a Convolutional Neural Network (CNN) using PyTorch to classify images from the FashionMNIST dataset.

The model is trained on the standard FashionMNIST dataset and then tested on 10 real-world photographs taken using a smartphone.

The complete workflow is automated through Google Colab and GitHub.

## Dataset

FashionMNIST contains 10 clothing categories:

1. T-shirt/top
2. Trouser
3. Pullover
4. Dress
5. Coat
6. Sandal
7. Shirt
8. Sneaker
9. Bag
10. Ankle boot

The standard dataset is automatically downloaded using torchvision.

## CNN Architecture

The CNN consists of:

- Convolutional Layer 1
- ReLU Activation
- Max Pooling
- Convolutional Layer 2
- ReLU Activation
- Max Pooling
- Fully Connected Layer
- ReLU Activation
- Dropout
- Output Layer

Input image size: 28 × 28 grayscale

## Data Preprocessing

The images are processed using torchvision transforms:

- Resize to 28 × 28
- Convert to Tensor
- Normalize using FashionMNIST mean and standard deviation

Custom smartphone images are also converted to grayscale and processed using the same transformation pipeline.

## Training

- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 64
- Epochs: 8

## Results

The notebook generates:

- Training Loss vs Epochs
- Validation Loss vs Epochs
- Training Accuracy vs Epochs
- Validation Accuracy vs Epochs
- Confusion Matrix
- Custom Image Prediction Gallery
- Visual Error Analysis

## Custom Image Testing

10 real-world images were captured using a smartphone and stored in the `dataset/` folder.

The trained CNN predicts the class of each image and displays the prediction along with its confidence score.

Example:

Pred: Sneaker (98.5%)

## Model

The trained model state dictionary is stored in:

`model/220129.pth`

## Repository Structure

```text
220129_CNN/
├── dataset/
│   ├── custom_image_1.jpg
│   ├── custom_image_2.jpg
│   └── ...
├── model/
│   └── 220129.pth
├── 220129.ipynb
└── README.md

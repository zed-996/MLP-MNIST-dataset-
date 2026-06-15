# MNIST Digit Classification

A simple neural network built with TensorFlow/Keras to classify handwritten digits from the MNIST dataset.

## Overview

This notebook loads the MNIST dataset, preprocesses the images, visualizes sample digits, trains a feedforward neural network, and plots the training/validation performance.

## Requirements

- Python 3.12
- tensorflow
- numpy
- matplotlib

Install dependencies:
```bash
pip install tensorflow numpy matplotlib
```

## Dataset

The MNIST dataset is automatically downloaded via `tf.keras.datasets.mnist.load_data()`:
- Training set: 60,000 images (28x28 grayscale)
- Test set: 10,000 images (28x28 grayscale)

Pixel values are normalized to the range [0, 1] by dividing by 255.

## Model Architecture

A `Sequential` model with the following layers:

| Layer | Type | Units | Activation |
|-------|------|-------|------------|
| 1 | Flatten | - | - |
| 2 | Dense | 256 | sigmoid |
| 3 | Dense | 128 | sigmoid |
| 4 | Dense (output) | 10 | softmax |

**Compilation:**
- Optimizer: `adam`
- Loss: `sparse_categorical_crossentropy`
- Metric: `accuracy`

## Training

- Epochs: 25
- Batch size: 2000
- Validation split: 20%

## Evaluation

The model is evaluated on the test set, printing test loss and accuracy.

## Visualizations

- A 10x10 grid of sample training images
- Training vs. validation accuracy curve
- Training vs. validation loss curve

## Usage

Run all cells sequentially in Jupyter Notebook or JupyterLab to load data, train the model, and view results.

## License

This project is licensed under the MIT License.

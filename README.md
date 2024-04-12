# Machine-Learning-AudioRecognizer

## Description

Using the GTZAN audio set to create a classifier that can tell what genere a piece of music is.

Two models was used, a personally created and pretrained one for comparison.

## Models setup

Both models will use a dataset of 1000 audio files. 80% of that dataset is used for training, while 20% is used for testing. Stochastic Gradient Descent (SGD) was used for the optimizer, and Cross-Entropy for the loss function. At the same time, a Cosine Learning Rate scheduling was used for both models to train more effeciently as it adjusted the learning rate to keep the loss at a minimum.

### First Model (personal)

Uses a Convolutional Neural Network (CNN) for high-level feature extraction. It will use ReLU as its activation function, have normalization and max pooling.

The output of the CNN model will be transfered to an SVM model using the RBF Kernel for full classification of the genre. It will use gridsearch to hypertune its parameters.

### Second Model

A pretrained model used for transfer learning. It was tweaked by changing its classifier to fit for the dataset used.

## Instructions and Setup

1. This was done using [Google Colab](https://colab.research.google.com). Download the [MachineLearningAudioData.ipynb](MachineLearningAudioData.ipynb) file and upload it to google colab.

2. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification).

3. Extract the dataset. Zip the `genres_original` folder, and rename it to `GTZAN Genre Collection`

4. Upload the zipped folder into your google `My Drive`

On Google Colab

1. Set your runtime to the `T4 GPU` by going `Runtime -> change runtime type` and connect to runtime session.

2. Run the file by going `Runtime -> run all` and ensure you mount your google drive.

## Credit

Anthony Massaad

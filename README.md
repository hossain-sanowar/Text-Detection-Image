# Text-Detection-Image
The main goal is to build a CRNN network that can predict the single-line text in an image (e.g., vehicle number plate)

# Business Purpose:

Text detection refers to the technique of identifying text inside a picture. Several uses include answering captchas and scanning license plates to identify automobiles.

Convolutional neural networks are techniques for deep learning that are very effective for image analysis. Recurrent Neural Networks (RNNs), on the other hand, are used for sequential data like as text. RNNs are well suited for addressing situations where the sequence is more important than the individual components.

This project is utilized both CNN and RNN networks to conduct image processing and sequence prediction in our scenario. I have added convolutions to the photos, and then run the recurrent neural network model on these convolutions to predict the text in the image. The name of this model is Convolutional Recurrent Neural Network (CRNN).

This model works best with photographs containing a single line of text, thus we will create it with images containing one-line texts.

This project attempts to develop a convolutional recurrent neural network capable of text detection from an image.

# Data Description: 

I have used the TRSynth100K dataset. This dataset contains around, 100k images along with their labels in a text file.

Project Aim:

To build a CRNN network that can predict the single-line text in a given image.

# Technology Used:
- Language - Python
- Libraries – cv2, torch, numpy, pandas, albumentations, matplotlib, pickle

# Approach

1. Importing the required libraries
2. Download the required dataset
3. Pre-processing
  - Find null values and replace those missing values with string “null”
  - Create a data frame with image path and corresponding labels (save as csv file)
  - Create a mapping from characters to integer and save in pickle format(char2int.pkl)
  - Create a mapping from integer to character and save in pickle format (int2char.pkl)
4. Define configurations paths
5. Training the model
  - Split the data into train and validation
  - Create train and validation datasets
  - Define the loss function
  - Create the model object
  - Define the optimizer
  - Training loop
  - Save the trained model
6. Predictions
  - Select image for prediction
  - Apply augmentations
  - Take the model output
  - Apply softmax and take label predictions
  - Use the ‘ph’ string character and convert integer predictions to string
  - Display the output

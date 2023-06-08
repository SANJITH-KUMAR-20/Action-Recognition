# Action-Recognition
An action detection using Tensorflow and Mediapipe

This is an mediapipe, LSTM model that uses actions to classify between different classes.

---> Data preparation:

1. For this model we collect the data from camera live feed.
2. Once we collect the images, we use mediapipe to extract the landmarks and use it as the training data.
3. We create a set of folders to store the training data,Create 3 folders for the three classes, Create data folder containing 30 folders.
4. we collect 30 frames for each folder in each class.
5. We collect the landmarks concatenate and flatten it and save it as numpy file with .npy format.

---> Building the model:

1. We use tensorflow for creating the LSTM model that takes in the numpy files as input and train the model to classify
        
        1. Load in the data
        2. Build the model with 3 LSTM layers and 3 Dense layers 
        3. Train the model.

2. Evaluate the model

---> Prediction:

1. Load in the model.
2. Take live feed from camera as input and extract landmarks for 30 frames and preprocess it.
3. Use the model to predict the result

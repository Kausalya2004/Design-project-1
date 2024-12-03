1. Set Seed for Reproducibility
- Set seeds for random, numpy, and TensorFlow to ensure consistent results.
2. Setup Kaggle API for Dataset Download
- Load Kaggle credentials (kaggle.json) and set environment variables.
- Use the Kaggle API to download the dataset.
3. Extract Dataset
- Unzip the downloaded dataset.
- Explore the dataset structure by listing directories and files.
4. Load and Display an Example Image
- Specify an image path.
- Load the image using matplotlib and display it.
5. Data Preprocessing and Augmentation
- Define image size (224x224) and batch size (32).
- Use ImageDataGenerator for rescaling and splitting data into training and
validation sets:
- Training Generator: Load training images with rescaling and specified target
size.
- Validation Generator: Load validation images similarly.
6. Model Definition
- Build a convolutional neural network (CNN) using Keras Sequential API:
1. Conv2D Layer: 32 filters, 3x3 kernel, ReLU activation.
2. MaxPooling2D: 2x2 pooling.
3. Conv2D Layer: 64 filters, 3x3 kernel, ReLU activation.
4. MaxPooling2D: 2x2 pooling.
5. Flatten Layer: Converts the 2D matrix to a 1D vector.
6. Dense Layer: 256 neurons, ReLU activation.
7. Output Layer: Softmax activation for multi-class classification.
7. Model Training
- Compile and train the model using model.fit().
- Use the training and validation generators.
- Train for 5 epochs.
8. Model Evaluation
- Evaluate the model on the validation set.
- Print the validation accuracy and loss.
9. Visualize Training Results
- Plot training and validation accuracy over epochs.
- Plot training and validation loss over epochs.
10. Image Prediction
- Preprocessing Function: Resize, normalize, and expand image dimensions.
- Prediction Function:
1. Load and preprocess an input image.
2. Predict the class using the trained model.
3. Retrieve the predicted class name from class indices.
11. Save Class Indices
- Save the mapping of class indices to class names as a JSON file.
12. Predict and Display Result
- Use the prediction function to predict the class of a test image.
- Print the predicted class name.

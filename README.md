# Drone Chatbot -  Natural Language Processing Application

This project implements a drone chatbot using Natural Language Processing (NLP) techniques. It's designed to understand and respond to user queries related to drones.

## Functionality Overview

1. **Data Preprocessing:**
   - Loads intents and patterns from a JSON file (`drone.json`).
   - Performs tokenization, lemmatization (using WordNetLemmatizer), and removal of stop words to prepare the data for processing.
   - Creates bag-of-words representations and one-hot encoded output vectors for training data.

2. **Model Development:**
   - Builds a Sequential neural network model using Keras.
   - Defines layers with appropriate activation functions and dropout layers for regularization.
   - Compiles the model with categorical crossentropy loss function, SGD optimizer with decay and momentum, and accuracy metric.

3. **Training:**
   - Trains the model on the prepared training data for a specified number of epochs (default: 20000) and batch size (default: 8).
   - Monitors and displays training progress during fit process.

4. **Model Saving:**
   - Saves the trained model as `chatbot_model.h5`.

## Requirements

* Python 3.x
* nltk (install using `pip install nltk`)
* keras (install using `pip install keras`)
* tensorflow (install using `pip install tensorflow`)
* numpy (install using `pip install numpy`)
* json (built-in module)
* pickle (built-in module)

## Usage Instructions

**1. Setting Up:**

   - **Install Libraries:** Ensure you have all the necessary libraries installed as mentioned in the Requirements section.
   - **Prepare Data:** Make sure your `drone.json` file is present in the project directory. This file should contain the intents and patterns for the chatbot to understand.

**2. Running the Script:**

   Execute the Python script (e.g., `python chatbot_training.py`) to preprocess data, train the model, and save it as `chatbot_model.h5`.

**3. Using the Trained Model (Next Steps):**

   - **Load the Model:** In a separate script, load the saved model using `model = load_model('chatbot_model.h5')`.
   - **Implement Chatbot Logic:** Develop code to handle user input, pre-process the input with similar NLP techniques, and make predictions using the trained model.
   - **Generate Responses:** Based on the predicted class, generate appropriate responses for the user.

**Note:** This provided code focuses on the training aspect. You'll need to implement additional code to integrate the chatbot functionality and allow interaction with the user.

## Potential Enhancements

* Explore other NLP techniques for advanced text processing (e.g., stemming, stemming vs. lemmatization).
* Implement a user interface for interaction with the chatbot.
* Train the model on a larger dataset and explore different neural network architectures for potentially better performance.
* Integrate sentiment analysis capabilities to tailor chatbot responses based on user tone.
* Consider incorporating context awareness into the model for more natural dialogue.



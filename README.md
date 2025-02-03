# Chatbot using PyTorch and NLTK

This project implements a simple intent-based chatbot using PyTorch and NLTK. It includes natural language processing techniques like tokenization, stemming, and training a neural network to classify user intents.

## Features
- Tokenization using NLTK
- Word stemming with PorterStemmer
- Intent classification using a neural network
- JSON-based dataset for chatbot responses
- Training and inference with PyTorch

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/chatbot.git
   cd chatbot
   ```
2. Install dependencies:
   ```bash
   pip install numpy torch nltk
   ```
3. Download NLTK data (only if running for the first time):
   ```python
   import nltk
   nltk.download('punkt')
   ```

## Usage
1. **Data Preparation:** The chatbot uses `intents.json` as the dataset, which contains predefined categories of user inputs and corresponding responses.
2. **Preprocessing:**
   - Sentences are tokenized using `nltk.word_tokenize`.
   - Words are then stemmed using `PorterStemmer` to normalize them.
3. **Training the Model:**
   - The processed data is converted into numerical form for training.
   - A simple neural network is implemented using PyTorch for intent classification.
   - The trained model is saved as `model.pth`.
4. **Chatbot Inference:**
   - User input is tokenized and stemmed.
   - The trained model predicts the intent category.
   - A corresponding response is selected from `intents.json`.
5. **Modify the chatbot:** You can add or update intents in `intents.json` to customize chatbot responses.

## How It Works
1. **User Input Handling:**
   - The chatbot receives user input as text.
   - The input is tokenized into words and stemmed to reduce them to their root form.

2. **Intent Classification:**
   - The processed words are converted into a numerical format that the neural network can understand.
   - The trained model predicts which intent the user input belongs to.

3. **Response Selection:**
   - Based on the predicted intent, a suitable response is retrieved from `intents.json`.
   - The chatbot then returns this response to the user.

4. **Improving Accuracy:**
   - The model can be retrained with additional intents and responses to improve performance.
   - Modifying `intents.json` allows customization for different applications.

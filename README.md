# Next-Word-Predictor

---
# Next Word Predictor with PyTorch & LSTM

A deep learning-based Natural Language Processing (NLP) project designed to predict the next most likely word in a given sentence. Built using `PyTorch` and `LSTM` (Long Short-Term Memory) networks, this model demonstrates how sequence modeling techniques can be applied to language understanding and generation.

***

## Key Features

* **End-to-End NLP Pipeline**: From raw text preprocessing to real-time prediction.
* **Practical LSTM Implementation**: Demonstrates a clear and effective use of LSTMs in PyTorch for sequence modeling.
* **High Performance**: Achieves approximately **95% accuracy** on the training dataset.
* **Domain-Specific Training**: Trained on a realistic document (e.g., FAQs, course information) to provide context-aware predictions.
* **Educational & Interpretable**: The code is designed to be simple and easy to understand, making it a great learning resource.

***

## How It Works

This project takes a body of text, learns its sequential patterns, and uses this knowledge to generate context-aware predictions for the next word.

### 1. Text Preprocessing
* The raw document is cleaned and normalized to lowercase.
* Using `NLTK`, the text is tokenized into individual words.
* A vocabulary is created by assigning a unique index to each token.

### 2. Sequence Generation
* For each sentence, multiple training sequences are generated using a sliding window.
* Each sequence includes a partial sentence, with the last word serving as the prediction target.
* Sequences are padded to a uniform length and converted into `PyTorch` tensors.

### 3. Model Architecture
The model is designed to be simple, interpretable, and efficient.
* **Embedding Layer**: Converts word indices into dense vector representations.
* **LSTM Layer**: Learns long-range dependencies and patterns between words in a sequence.
* **Fully Connected (Linear) Layer**: Maps the LSTM outputs to scores for each word in the vocabulary, predicting the most likely next word.

### 4. Training & Performance
* The model is trained for **50 epochs** using `CrossEntropyLoss` and the `Adam` optimizer.
* Loss decreases steadily across epochs, indicating successful learning.
* The final model achieves approximately **95% accuracy** on the training dataset.

***

## Usage & Example

The model allows for dynamic input: you provide a partial sentence, and it predicts the next word. It can be run iteratively to generate multiple words and build entire sentences.

**Example:**
* **Input**: `"The course follows a monthly"`
* **Predicted Output**: `"subscription"`

***

## Applications

This model serves as a foundation for various real-world NLP applications, including:
* Chatbots and conversational assistants
* Smart typing and email autocompletion
* AI-powered writing assistants
* NLP education and research tools

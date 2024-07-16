# Tweet Emotion Recognition using Recurrent Neural Networks (RNN)

This project aims to classify emotions in tweets using a recurrent neural network (RNN) implemented with TensorFlow. The dataset consists of tweets labeled with one of six emotions: sadness, joy, surprise, love, anger, and fear.

## Project Overview

The goal of this project is to develop a machine learning model capable of accurately predicting the emotional content of tweets. Emotion classification in natural language processing (NLP) is crucial for various applications, including sentiment analysis and customer feedback analysis.

## Methodology

### Data Preparation

- **Importing and Cleaning Data:** The dataset (`tweeter_emo.csv`) was imported and cleaned to focus on relevant columns (`text` and `emotions`). Duplicate entries were removed to ensure data integrity.

### Model Development

- **Tokenization and Sequence Padding:** Text data was tokenized using TensorFlow's `Tokenizer` and sequences were padded/truncated to a fixed length of 50 for compatibility with the RNN model.

- **Recurrent Neural Network (RNN):** The model architecture includes an embedding layer followed by two bidirectional LSTM layers and a dense output layer with softmax activation for multi-class classification (six emotions).

### Training and Evaluation

- **Training:** The model was trained using the Adam optimizer and sparse categorical cross-entropy loss function. Training was stopped early if validation accuracy did not improve for three consecutive epochs (`EarlyStopping` callback).

- **Evaluation:** Model performance was evaluated on a separate test set using metrics such as accuracy and loss. The test loss was 0.82657, indicating the average loss per sample during testing. The model achieved a precision of 76%, demonstrating its ability to correctly classify tweets into the correct emotion categories.

- **Confusion Matrix:** Confusion matrices and visualizations were used to analyze model predictions and identify any patterns or biases.

## Observations

- **Model Performance:** The trained RNN achieved 76% precision on the test set, demonstrating effective classification of tweets into one of six emotions.
  
- **Word Cloud Visualization:** Word clouds were generated for each emotion category to visualize the most frequent words associated with different emotions in the dataset.

## Conclusion

This project showcases the application of recurrent neural networks for tweet emotion recognition. The model successfully learns to classify tweets based on emotional content, highlighting its potential for sentiment analysis and related tasks in NLP.

# Tweet Emotion Recognition using Recurrent Neural Networks (RNN)

This project aims to classify emotions in tweets using a recurrent neural network (RNN) implemented with TensorFlow. The dataset consists of tweets labeled with one of six emotions: sadness, joy, surprise, love, anger, and fear.

## Project Overview

The goal of this project is to develop a machine learning model capable of accurately predicting the emotional content of tweets. Emotion classification in natural language processing (NLP) is crucial for various applications, including sentiment analysis and customer feedback analysis.

![download (1)](https://github.com/user-attachments/assets/f6bbc5ab-6b88-44f7-afa7-66b003a5a056)


## Methodology

### Data Preparation

- **Importing and Cleaning Data:** The dataset (`tweeter_emo.csv`) was imported and cleaned to focus on relevant columns (`text` and `emotions`). Duplicate entries were removed to ensure data integrity.

![download (2)](https://github.com/user-attachments/assets/135c75fb-a28b-49b6-9ecf-18fedc937216)

### Model Development

- **Tokenization and Sequence Padding:** Text data was tokenized using TensorFlow's `Tokenizer` and sequences were padded/truncated to a fixed length of 50 for compatibility with the RNN model.

- **Recurrent Neural Network (RNN):** The model architecture includes an embedding layer followed by two bidirectional LSTM layers and a dense output layer with softmax activation for multi-class classification (six emotions).

### Training and Evaluation

- **Training:** The model was trained using the Adam optimizer and sparse categorical cross-entropy loss function. Training was stopped early if validation accuracy did not improve for three consecutive epochs (`EarlyStopping` callback).

- **Evaluation:** Model performance was evaluated on a separate test set using metrics such as accuracy and loss. The test loss was 0.82657, indicating the average loss per sample during testing. The model achieved a precision of 76%, demonstrating its ability to correctly classify tweets into the correct emotion categories.

![download (3)](https://github.com/user-attachments/assets/2d0c5ded-6623-45b2-a45f-e8dbb25c3d94)

- **Confusion Matrix:** Confusion matrices and visualizations were used to analyze model predictions and identify any patterns or biases.

![download (4)](https://github.com/user-attachments/assets/8fb39a5a-533c-470b-9768-a74a212357d2)

## Observations

- **Model Performance:** The trained RNN achieved 76% precision on the test set, demonstrating effective classification of tweets into one of six emotions.
  
- **Word Cloud Visualization:** Word clouds were generated for each emotion category to visualize the most frequent words associated with different emotions in the dataset.

## Conclusion

This project showcases the application of recurrent neural networks for tweet emotion recognition. The model successfully learns to classify tweets based on emotional content, highlighting its potential for sentiment analysis and related tasks in NLP.

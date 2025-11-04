# Spam Detection Project

## Overview  
This project builds a spam-detection model using the SMS Spam Collection dataset and pre-trained word embeddings (GloVe). The goal is to classify SMS messages into “spam” or “ham” (non-spam) and to leverage word embeddings for improved text representation before model training.

## Datasets

### 1. SMS Spam Collection  
- Source: [SMS Spam Collection Dataset on Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset/data)  
- Description: A collection of ~5,574 SMS messages, each labeled as *spam* or *ham*. It was originally collected for mobile SMS spam research.  
- Usage in this project: The dataset is used for building and evaluating the classification model.  
- Key attributes:  
  - `label`: Indicates whether the message is *spam* or *ham*.  
  - `message`: The text content of the SMS.

### 2. GloVe Embeddings (100 dimensional)  
- Source: [glove.6B.100d.txt on Hugging Face](https://huggingface.co/datasets/SLU-CSCI4750/glove.6B.100d.txt)  
- Description: Pre-trained word vectors from the GloVe (Global Vectors for Word Representation) project, trained on a large English corpus. The 100-dimensional version provides fixed-length embeddings for words.  
- Usage in this project: We use the embeddings file to map words in SMS messages to dense vector representations, thereby improving text feature representation before feeding into the model.

## Project Workflow
1. **Data Loading:** Import the SMS dataset and inspect basic statistics.  
2. **Preprocessing:**  
   - Clean text (remove punctuation, stopwords, lowercase text)  
   - Tokenize and pad sequences  
3. **Embedding Integration:**  
   - Load `glove.6B.100d.txt`  
   - Create an embedding matrix matching the tokenizer vocabulary  
4. **Model Design:**  
   - Use a neural network (e.g., LSTM, or Dense layers) for classification  
5. **Training & Evaluation:**  
   - Train model on the processed dataset  
   - Evaluate using accuracy, precision, recall, F1-score, and confusion matrix  

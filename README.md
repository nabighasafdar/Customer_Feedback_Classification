# Customer_Feedback_Classification

# Overview

In this assignment, I worked on **Task 1: Encoder-Only (BERT)** to perform **sentiment classification** on customer feedback data. The goal was to determine whether a given piece of feedback expressed a **positive**, **negative**, or **neutral** sentiment.

# Objective

The main objective was to fine-tune a **BERT-based model** (encoder-only architecture) to classify textual feedback according to customer sentiment.

# Dataset

I used the dataset from Kaggle: [Customer Feedback Dataset](https://www.kaggle.com/datasets/vishweshsalodkar/customer-feedback-dataset?select=sentiment-analysis.csv). It contains text feedback along with sentiment labels.

# Steps Performed

1. **Data Preprocessing & Tokenization**

   * Loaded the dataset and cleaned the text (lowercasing, removing unwanted symbols).
   * Tokenized the text using the `BERT tokenizer` from the Hugging Face Transformers library.
   * Encoded the labels (Positive, Neutral, Negative) into numerical form.

2. **Model Fine-tuning (Training & Validation)**

   * Used a pretrained `bert-base-uncased` model.
   * Added a classification head for three sentiment classes.
   * Split the dataset into training and validation sets.
   * Trained the model using the AdamW optimizer and a suitable learning rate.

3. **Evaluation**

   * Evaluated the model using **Accuracy**, **F1-score**, and a **Confusion Matrix**.
   * Observed that the model was able to classify sentiments effectively after fine-tuning.

4. **Example Predictions**

   * Tested the model with new sample customer feedback texts.
   * The model correctly predicted sentiments such as:

     * “The product was amazing!” → **Positive**
     * “Very disappointed with the service.” → **Negative**

## Conclusion

This task demonstrated how an encoder-only transformer model like **BERT** can be fine-tuned for text classification tasks such as sentiment analysis. By performing preprocessing, tokenization, training, evaluation, and testing, I successfully implemented a pipeline to classify customer feedback based on sentiment.

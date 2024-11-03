# Emotion_TextClassification_with_Bert

This project implements an emotion classification model using the BERT base uncased model. The model is fine-tuned on a dataset of textual data to classify six different emotions: anger, fear, love, happiness, sadness, and surprise. Additionally, the project enhances the emotion classification by integrating emojis corresponding to each emotion and utilizing color coding for better visualization.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Emotion Classification](#emotion-classification)
- [Emoji Integration](#emoji-integration)

## Introduction

The goal of this project is to classify emotions expressed in text using BERT. Emotion classification can be beneficial in various applications, including sentiment analysis, user feedback interpretation, and social media monitoring.

## Dataset

The dataset used for training the emotion classification model is sourced from the `datasets` package, which contains labeled text data for various emotions. The dataset includes the following emotions:
- Anger
- Fear
- Love
- Happiness
- Sadness
- Surprise

**Dataset Info**:
  train: Dataset({
        features: ['text', 'label'],
        num_rows: 16000
    })
    validation: Dataset({
        features: ['text', 'label'],
        num_rows: 2000
    })
    test: Dataset({
        features: ['text', 'label'],
        num_rows: 2000
    })


## Model Training

1. **Model Selection**: BERT base uncased was selected for its performance on NLP tasks.
2. **Fine-Tuning**: The BERT model was fine-tuned for **5 epochs** on the emotion dataset.
3. **Model Saving**: After training, the model was saved as a `.pkl` file for future use.

![image](https://github.com/user-attachments/assets/351d1a75-fe49-4b7d-a65b-63a6c5a45ada)

## Emotion Classification

The fine-tuned BERT model is used to classify input sentences into one of the six emotion categories. The classification results can be further processed for visualization and user interaction.

## Emoji Integration

To enhance the emotion classification output, emojis corresponding to each emotion are integrated using the `emoji` package. Each emotion is also associated with a specific color for better representation:
- **Anger**: 🔴 (Red)
- **Fear**: 🟡 (Yellow)
- **Love**: 💖 (Pink)
- **Happiness**: 🟢 (Green)
- **Sadness**: 🔵 (Blue)
- **Surprise**: 🟣 (Purple)

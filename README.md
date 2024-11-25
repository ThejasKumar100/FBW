# Feelings Behind Words: Detecting Persuasive Techniques in Media

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![BERT](https://img.shields.io/badge/BERT-FF5722?style=for-the-badge&logo=apache&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

## Overview

**Feelings Behind Words** is an AI-driven project designed to analyze online media and provide insights into persuasive, manipulative, and potentially harmful content. By leveraging multimodal analysis of both text and image data, our model identifies manipulative rhetoric, helping users become more aware of how media may influence their thoughts and actions.

The model is particularly useful in identifying harmful propaganda in political ads, election campaigns, or any media with the potential to manipulate public opinion. Ultimately, this project aims to increase media literacy by allowing users to recognize emotional manipulation in the content they consume.

## Key Features

- **Multimodal Rhetoric Detection**: Analyzes both text and images to identify persuasive techniques such as *appeal to authority*, *fear-mongering*, *name-calling*, and *loaded language*.
- **Sentiment Analysis**: Uses **BERT** to analyze the emotional tone of text and classify persuasive sentiment.
- **Image Classification**: Applies **Convolutional Neural Networks (CNNs)** to recognize patterns and symbols in images that may contribute to persuasion.
- **Real-time Propaganda Detection**: Flag harmful rhetoric and manipulative content in real time.

## Technologies Used

- **TensorFlow**: For training the sentiment analysis model (BERT) and image classification (CNN).
- **BERT**: Pretrained model for natural language processing and sentiment analysis.
- **ResNet 18**: For image pattern recognition.

## How It Works

The model combines two models:

1. **Model 1: Sentiment Analysis (Text)**  
   - Text is processed using **BERT**, which tokenizes and converts the input text into vectors.  
   - These vectors are then classified into different emotional tones (e.g., fear, anger, trust) using **TensorFlow**.
   
2. **Model 2: Image Classification (Visual Content)**  
   - Images are preprocessed and passed through **ResNet18** to detect patterns, symbols, and visual rhetoric (e.g., authority figures, flags, etc.).

3. **Late Fusion**:  
   - The outputs from both the sentiment analysis and image classification models are merged using late fusion, improving overall accuracy.

## Results

- **Overall Accuracy**: 89.2% across 20 persuasion techniques.
- **High Accuracy Techniques**: *Appeal to authority*, *repetition*, and *bandwagon* were detected with high accuracy (>90%).
- **Lower Accuracy Techniques**: *Flag-waving*, *name-calling*, and *loaded language* had accuracy <60%, showing the difficulty in detecting more subtle manipulations.

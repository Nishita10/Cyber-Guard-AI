# Cyber-Guard-AI
This NLP project categorizes complaints based on parameters like victim, fraud type, and other relevant factors. The goal is to build a precise text classification model to aid in identifying and organizing complaint data, supporting effective analysis and response to various fraud cases.

This project develops an NLP model that categorizes complaints based on relevant parameters, including the victim, type of fraud, and additional specific attributes. By training a text classification model using complaint data, we aim to automate and streamline the categorization of complaint information, aiding in effective analysis and response to various fraud cases.

<h1>Problem Statement</h1>
With a high volume of complaint data, manually categorizing each case based on parameters such as victim involvement, fraud type, and other unique details is challenging and time-consuming. This project provides a solution by building an NLP model that classifies complaints based on these factors, allowing for efficient organization and prioritization in fraud investigations.

<h2>Solution Approach</h2>
The project leverages a hybrid approach that combines data preprocessing, Exploratory Data Analysis (EDA), and a fine-tuned DistilBERT model for classification.

<h3>Key Steps in the Code: </h3>
<ol>
<li><b>Loading and Preprocessing Data: </b>
The script begins by loading the training and testing datasets. Basic EDA is conducted to visualize the distribution of categories in each dataset, helping us understand the class balance.</li>

<li><b>Exploratory Data Analysis: (EDA)</b>
The eda function visualizes the count of each complaint category in both the training and testing datasets, aiding in understanding class distributions.</li>

<li><b>Text Preprocessing: </b>
The complaints text undergoes preprocessing for normalization, tokenization, and removal of stopwords. The preprocess_text function applies these techniques, while clean_and_stem further processes the text using stemming.</li>

<li><b>Dataset Creation for Model Training: </b>
TensorFlow datasets are created from the encoded complaint data, enabling efficient batching and shuffling during model training.</li>

<li><b>Building the Hybrid Model: </b>
A custom model is built using a pre-trained DistilBERT model from Hugging Face’s Transformers library. The model architecture includes:

<ul><li>Input layers for input_ids and attention_mask to handle tokenized text inputs.</li>
<li>A DistilBERT layer (encapsulated within a Lambda function) to process input sequences.</li>
<li>Dense layers with dropout for classification, where the final layer uses softmax activation to output probabilities for each complaint category.</li>
</ul></li>
<li><b>Training and Evaluating the Model: </b>
The model can be trained using the TensorFlow fit function, and its performance can be evaluated on the test dataset.</li>
</ol>
<h5>Requirements</h5>
<ul>
<li>pandas</li>
<li>tensorflow</li>
<li>transformers</li>
<li>matplotlib</li>
<li>seaborn</li>
<li>nltk</li>
</ul>




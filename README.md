## ConstructivIQ
# Material Similarity Project

This project aims to calculate similarities between materials based on their descriptions and predict similarity scores for test pairs.

## Table of Contents
1. [Data Preparation](#data-preparation)
2. [Text Preprocessing](#text-preprocessing)
3. [Feature Extraction](#feature-extraction)
4. [Similarity Calculation](#similarity-calculation)
5. [Evaluation](#evaluation)




## Data Preparation

1. Load the required datasets:
   - `materials.csv`: Contains material descriptions
   - `submission.csv`: Ground truth data
   - `test_pairs.csv`: Test pairs for prediction

## Text Preprocessing

1. Define a `preprocess_text` function that:
   - Converts text to lowercase
   - Removes special characters
   - Tokenizes the text
   - Removes stopwords
   - Lemmatizes the tokens

2. Apply the preprocessing to the material descriptions

## Feature Extraction

1. Use TF-IDF (Term Frequency-Inverse Document Frequency) vectorization:
   

2. Create TF-IDF matrix from preprocessed descriptions

## Similarity Calculation

1. Define a `calculate_similarity` function using cosine similarity
2. Calculate similarities for ground truth data
<h3>How Cosine Similarity works? : </h3>
<p>Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.</p>
<p align='center'><img src ='https://user-images.githubusercontent.com/31500911/143417796-8602832b-aac9-4f4f-b930-b753dc050981.png'></p>

## Evaluation

1. Implement MAP@K (Mean Average Precision at K) metric
2. Calculate MAP@K for K values of 1, 3, 5, and 10

<h3>How to calculate MAP?</h3>
<p>Mean Average Precision (MAP) at K is a quality metric that helps evaluate the ability of the recommender or ranking system to return relevant items in the top-K results while placing more relevant items at the top. We can express it as the following:
</p>
<p align='center'>
    <img src='https://cdn.prod.website-files.com/660ef16a9e0687d9cc27474a/662c432c08687cce06cf3df4_6577811c2a405c8d26605bd4_precision_recall_k6.png' width='500' height='auto'>
</p>


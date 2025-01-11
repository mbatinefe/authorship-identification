# Song Lyrics Artist Classification

A machine learning project that classifies song lyrics to predict their artists using three different approaches:

## Models Implemented
1. Custom Naive Bayes Classifier (from scratch)
2. K-Nearest Neighbors with TF-IDF 
3. Neural Network with Word Embeddings

## Project Structure
- Data preprocessing and cleaning
- Feature engineering
- Model implementation and training
- Performance evaluation and comparison

## Key Features
- Custom implementation of Naive Bayes classifier using Maximum Likelihood Estimation
- TF-IDF vectorization with n-grams (1-3)
- Neural network with word embeddings
- Confusion matrix visualization for all models
- Performance metrics including accuracy and F1 scores

## Results

### Model Performance Analysis

#### Naive Bayes Classifier
- Accuracy: 61.7%
- F1-Score: 0.613
- Strong performance on distinctive artists (Drake, Eminem, BTS)
- Limitations with stylistically similar artists
- Simple but effective baseline model

#### K-Nearest Neighbors (Best Performer)
- Accuracy: 63.0%
- F1-Score: 0.624
- Best overall performance
- Excellent results for Eminem, Drake, and Lady Gaga
- Strong handling of medium-sized samples
- TF-IDF with n-grams (1-3) proved highly effective
- Optimization through:
  - Increased max_features to 10000
  - Adjusted min_df to 3

#### Neural Network
- Accuracy: 60.0%
- F1-Score: 0.589
- Good performance on high-frequency artists
- Struggles with less represented artists
- Improved through:
  - Vocabulary size increase to 10000
  - 20 training epochs
  - Architecture optimization

### Key Findings
1. Feature Engineering Impact:
   - TF-IDF with n-grams proved most effective
   - Word embeddings showed potential but limited by random initialization
   - Bag-of-Words provided solid baseline performance

2. Model Strengths:
   - KNN: Best for balanced classification across all artists
   - Naive Bayes: Strong baseline with good generalization
   - Neural Network: Effective for frequently represented artists

3. Common Challenges:
   - Artist-specific pattern recognition
   - Handling imbalanced artist representations
   - Capturing subtle stylistic differences

### Final Ranking
1. K-Nearest Neighbors (63.0%)
2. Naive Bayes (61.7%)
3. Neural Network (60.0%)


## Dataset
Uses a lyrics dataset with train/dev/test split of 70/15/15 proportions.
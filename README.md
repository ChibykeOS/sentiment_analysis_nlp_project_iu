# Sentiment Analysis on Movie Reviews
## Background
With the advent of social media, movie reviews have become a popular means of expressing opinions about films. This project develops a natural language processing (NLP) system to analyze movie reviews and determine overall sentiment (positive or negative), as outlined in the assignment.

**Task Overview**

## Collect Data 
Used the publicly available Stanford Large Movie Review Dataset (IMDB) from https://ai.stanford.edu/~amaas/data/sentiment/.
Preprocess Data: Remove stop words, lemmatize, and encode using TF-IDF.
**Train Model**: Supervised learning with Multinomial Naive Bayes on labeled positive/negative reviews.
**Evaluate Model**: Assessed accuracy and generalization on a separate test dataset.
**Analyze Reviews**: Binary classification for new reviews (positive/negative).
**Evaluation Scenarios**: Tested on small (e.g., 100 reviews), medium (1,000), large (10,000), and full (50,000) datasets.

## Dataset Details

Source: https://ai.stanford.edu/~amaas/data/sentiment/
Structure: 50,000 reviews total (25,000 train: 12,500 pos/12,500 neg; 25,000 test similarly). Each review is in a .txt file within pos/neg folders.
Labels: Binary (positive/negative based on folder).

## System Implementation
The system is implemented in sentiment_analysis_nlp_iu.py using Python with NLTK for preprocessing and scikit-learn for vectorization and modeling. Key steps:

## Download and extract the dataset.
Load and preprocess reviews (lowercase, remove stop words, lemmatize).
Encode text with TF-IDF (limited to 5,000 features for efficiency).
Train Multinomial Naive Bayes on train data.
Evaluate on test data with accuracy and classification report.
Analyze new reviews via a dedicated function.

Performance Metrics on the Test Dataset
The model was evaluated on the full test dataset (25,000 reviews). Results:

**Accuracy**: 0.8265


Classification Report:
<img width="436" height="133" alt="image" src="https://github.com/user-attachments/assets/9e81423d-3ab0-4ee0-a3af-4c4a7434c5b1" />


These metrics indicate balanced performance across classes, with good generalization. For smaller datasets:

Small (100 reviews): Accuracy ~0.70-0.80 (higher variance due to limited data).
Medium (1,000 reviews): Accuracy ~0.82-0.85.
Large (10,000 reviews): Accuracy ~0.85-0.87.

Example Usage
After training, the system can analyze new reviews. For the example "This movie was absolutely fantastic! I loved every minute of it.": Sentiment: Positive
Dependencies

Python 3.x
NLTK
scikit-learn

Install via: pip install nltk scikit-learn

## How to Run

Clone the repo: git clone https://github.com/user/sentiment_analysis_nlp_project_iu

Run python sentiment_analysis_nlp_iu.py (adjust limit for different scenarios).

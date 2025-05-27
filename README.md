# Fake-News Text Classifier

A classic case of "don't believe everything you read". This project dives into the fascinating world of fake vs. real news. We build and evaluate various machine learning models that classify whether a piece of news is fake or real, and even dig into the parts of speech that give misinformation away.

Using a labeled dataset of real and fake news articles, this project applies a comprehensive NLP pipeline to:
- Clean the text (stopword removal, lemmatization, and POS-tagging)
- Explore linguistic patterns (word clouds, frequency tables)
- Build classifiers using three kinds of text features: TF (Term Frequency), TF-IDF (Term Frequency-Inverse Document Frequency), and Bag of Words (BoW)
- Compare traditional models (Logistic Regression, Naive Bayes, Random Forest) with advanced ones (XGBoost)
- Test whether parts of speech (nouns, verbs, adjectives) alone can identify fake news

## Contents 

`data/`   
- `dataset.md`: Contains the dataset source link

`notebooks/`  
- `fake-news-text-classifier.ipynb`: Notebook with the entire NLP pipeline and our analysis        

## Results  

| Model                      | Feature Type | Accuracy |
|----------------------------|--------------|----------|
| Logistic Regression        | TF           | 99.31%   |
| Random Forest              | TF           | 99.05%   |
| XGBoost                    | TF           | **99.47%** |
| Logistic Regression        | TF-IDF       | 98.02%   |
| XGBoost (POS: Nouns)       | TF           | 92.19%   |
| XGBoost (POS: Adjectives)  | TF           | 91.56%   |

XGBoost with raw term frequencies crushed it with a near-perfect score.

## Highlights  

- Clean data makes a world of difference.
- TF features worked surprisingly better than TF-IDF or even n-gram BoW.
- POS-specific models show there's signal even in just nouns and adjectives!  

# Fake News Detection System

## Overview
This project implements a machine learning solution to detect fake news articles using NLP techniques and various classification algorithms. The system analyzes text content to determine the likelihood of an article being fake or legitimate news.

## Problem Statement
In today's digital age, misinformation spreads rapidly through social media and various online platforms. This project aims to tackle this issue by providing an automated system that can help identify potentially fake news articles based on their content.

## Related Work
This implementation draws inspiration from several key research papers in the field:

1. Conroy, N. J., Rubin, V. L., & Chen, Y. (2015). "Automatic deception detection: Methods for finding fake news." Proceedings of the Association for Information Science and Technology, 52(1), 1-4.
   - Utilized their textual feature extraction approach

2. Shu, K., Sliva, A., Wang, S., Tang, J., & Liu, H. (2017). "Fake news detection on social media: A data mining perspective." ACM SIGKDD Explorations Newsletter, 19(1), 22-36.
   - Adapted their stance detection methodology

## Dataset
The project uses the [Fake and Real News Dataset](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset) from Kaggle, which contains:
- 21,417 real news articles
- 23,481 fake news articles
- Features include article titles, text, subject, and date

## Methodology

### Data Preprocessing
1. Text cleaning (removing special characters, numbers)
2. Lowercasing and tokenization
3. Stop words removal
4. Stemming/Lemmatization
5. TF-IDF Vectorization

### Exploratory Data Analysis
- Distribution of articles by category
- Word frequency analysis
- Text length analysis
- Temporal analysis of publication dates

### Models Implemented
1. Passive Aggressive Classifier
2. Multinomial Naive Bayes
3. Random Forest
4. Logistic Regression
5. Support Vector Machine

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix

## Results
| Model | Accuracy | Precision | Recall | F1-Score | AUC |
|-------|----------|-----------|--------|----------|-----|
| Passive Aggressive | 0.92 | 0.94 | 0.90 | 0.92 | 0.91 |
| Naive Bayes | 0.89 | 0.88 | 0.90 | 0.89 | 0.88 |
| Random Forest | 0.93 | 0.95 | 0.91 | 0.93 | 0.92 |
| Logistic Regression | 0.91 | 0.93 | 0.89 | 0.91 | 0.90 |
| SVM | 0.92 | 0.93 | 0.91 | 0.92 | 0.91 |

## Deployment
The system is deployed as a web application using Streamlit. Users can input news articles to get predictions on their authenticity.

- Live Demo: https://cfyvffu33x4px9cxc8tuw4.streamlit.app/

## Installation and Usage
```bash
# Clone the repository
git clone https://github.com/mango-mocha/fake-news-detection.git

# Navigate to the project directory
cd fake-news-detection

# Install dependencies
pip install -r requirements.txt

# Run the application locally
streamlit run app.py

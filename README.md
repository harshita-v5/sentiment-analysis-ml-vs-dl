# sentiment-analysis-ml-vs-dl

#Sentiment Analysis: ML vs Deep Learning (Experimental Study)

This project is an experimental NLP study that compares traditional ML and DL approaches for sentiment analysis on IMDB movie reviews.
The focus is on understanding how preprocessing strategies and models affect performance, rather than chasing maximum accuracy.

#Problem Statement
Given IMDB movie review, predict whether the sentiment is:
Positive
Negative

📂 Dataset
IMDB Movie Reviews Dataset
50,000 labeled reviews
Binary sentiment classification (positive / negative)

🛠️ Tech Stack
Python
Scikit-learn
TensorFlow / Keras
NLTK
Pandas, Matplotlib

🔬 Experiment Pipelines
🔹 Pipeline 1: Traditional ML
Text Cleaning: Light
Feature Extraction: TF-IDF
Model: Logistic Regression

Pipeline 2: Deep Learning (Light Cleaning)
Text Cleaning: Light
Text Representation: Tokenizer + Padding
Model: Bidirectional LSTM

Pipeline 3: Deep Learning (Heavy Cleaning)
Text Cleaning: Stopword removal + Lemmatization
Text Representation: Tokenizer + Padding
Model: Bidirectional LSTM

⚠️ All Deep Learning models were trained with the same architecture and training parameters to ensure a fair comparison.

📊 Results Comparison
Pipeline	Cleaning	Model	Accuracy
TF-IDF + LR	Light	Logistic Regression	  89.70%
BiLSTM (Light Clean)	Light	BiLSTM	    86.90%
BiLSTM (Heavy Clean)	Heavy	BiLSTM	    86.69%

🔍 Key Observations
1.TF-IDF with Logistic Regression provides a strong baseline for sentiment analysis.
2.Bidirectional LSTM benefits from contextual learning but did not outperform the ML baseline in this setup.
3.Heavy text preprocessing did not improve Deep Learning performance.
4.Deep Learning models are robust to minimal preprocessing, and excessive cleaning may remove useful context.
5.Preprocessing strategies should be model-dependent, not one-size-fits-all.

🧠 Conclusion
This project highlights that:
Traditional ML models with TF-IDF remain highly competitive for sentiment analysis.
Deep Learning models do not always require heavy text preprocessing.
Fair experimentation and controlled comparisons are essential for drawing meaningful conclusions.

Acknowledgements:-
IMDB Dataset
Scikit-learn & TensorFlow documentation

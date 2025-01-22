*Aspect-Based Sentiment Analysis (ABSA)*
This project implements an Aspect-Based Sentiment Analysis (ABSA) system, leveraging various Natural Language Processing (NLP) techniques and models. The system analyzes user reviews of laptops to identify sentiment associated with specific aspects such as performance, display, or durability.

**Dataset Overview**
Dataset: SemEval-2014 ABSA
Number of records: 2,313 rows
**Approach and Techniques**
1. Data Pre-Processing
Converting text to lowercase
Tokenization and lemmatization
Removing stopwords and applying regular expressions
Preparing cleaned sentences for feature extraction
2. Machine Learning Models
Count-Vectorizer with:
Sentence-level features (ngram_range=(2,3))
Aspect-level features (ngram_range=(1,4))
Models:
DecisionTreeClassifier
Support Vector Classifier (SVC)
3. Embedding-Based Approaches
Word2Vec (W2V) embeddings combined with:
DecisionTreeClassifier: 44% accuracy
SVM: 35% accuracy
4. Transformer Models
MobileBERT: Fine-tuning resulted in 40% accuracy
ALBERT Base v2:
Fine-tuning resulted in 77% accuracy
Twitter-RoBERTa-base:
Accuracy improved from 67% to 79% after 4 epochs
DeBERTa-v3-base (Powered by PyABSA):
Accuracy before fine-tuning: 95%
Accuracy after fine-tuning: 96%
**Results**
Fine-tuning transformer-based models significantly improved performance, with DeBERTa-v3 achieving the highest accuracy of 96%.

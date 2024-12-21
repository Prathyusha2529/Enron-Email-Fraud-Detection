# Enron-Email-Fraud-Detection

This project leverages text mining and machine learning techniques to analyze the Enron email dataset for detecting fraudulent emails. The project encompasses comprehensive data preprocessing, advanced modeling approaches, and business insights that contribute to combating phishing attacks and enhancing cybersecurity.

**1. Introduction**
Phishing emails are a persistent cybersecurity threat, resulting in financial and reputational losses for organizations worldwide. By analyzing the Enron email dataset, this project demonstrates the application of text mining techniques to identify fraudulent emails. The findings aim to aid organizations in improving their security protocols and safeguarding sensitive information.

**2. Dataset Details**

**Source:** The dataset was obtained from Kaggle's Enron Email Dataset.
**Features:**
Body: Contains the main content of the emails.

Subject: Contains the subject lines of the emails.

Label: Binary target column indicating whether an email is fraudulent (1) or non-fraudulent (0).

**Challenges:**

Highly imbalanced data: Only 0.5% of emails are labeled as fraudulent.
Presence of noise and irrelevant characters in the text data.

**3. Key Processes**
**Data Preprocessing** 
- Removed special characters, excessive whitespace, and null values from the dataset.
- Stratified sampling was applied to address the imbalance in the target variable.
- Concatenated Subject and Body fields for combined analysis.

**Feature Engineering**
Term Weighting: Applied techniques such as IDF (Inverse Document Frequency), Entropy, and Mutual Information (MI).

Dimensionality Reduction: Used Singular Value Decomposition (SVD) to reduce dimensionality and computational overhead.

**Model Building**

Explored various machine learning techniques with text mining to identify the best-performing model:

**Algorithms:**
- Regression
- Neural Networks
- Decision Trees
**Stoplists:**
Custom stoplists were created to improve accuracy by excluding irrelevant or frequently occurring terms.

**4. Model Comparison and Results**
**Body Text Analysis**
Model	Technique	Dimensions	Accuracy
Body Log & IDF	Neural Network	120	89.89%
Body Log & Entropy	Regression	150	87.53%
Body Log & MI	Neural Network	80	89.70%

**Subject Text Analysis**
Model	Technique	Dimensions	Accuracy
Subject Log & IDF	Regression	150	82.89%
Subject Log & Entropy	Regression	150	82.56%
Subject Log & MI	Regression	120	82.81%

**Combined (Body + Subject)**
Model	Technique	Accuracy
Concat Log & IDF	Regression	89.46%
Concat Log & Entropy	Regression	89.72%

The Body Text Neural Network (Log & IDF) model emerged as the best, achieving an accuracy of 89.89%.

**5. Business Insights**
Fraud Indicators: Common keywords in phishing emails included "account," "confirm," "delivery," and "request."

**Organizational Benefits:**
-Improved email security measures.
- Enhanced trust among customers and stakeholders.
- Reduced financial losses from phishing scams.

**Actionable Steps:**
- Integrate the best-performing model into email systems for real-time fraud detection.
- Train staff to recognize phishing patterns highlighted by the analysis.

**6. Technical Architecture** 
Preprocessing: Python (Pandas, NumPy) on Google Colab.
Modeling: SAS Enterprise Miner for text analytics.
Visualization: Matplotlib for data exploration and result presentation.

# Email Spam Detection
## Overview
This project focuses on developing a robust SPAM email detection system using a Random Forest (RF) classifier. By leveraging Natural Language Processing (NLP) techniques, the system analyzes the textual content of emails to identify and classify them as Spam or Not Spam (Ham).
![image alt](https://github.com/adeyie/Email-Spam-Detection/blob/4ac767a78cb37040241a5a437becd4598a43adec/Email%20SPAM.PNG)

## Python version: 3.7.4
## Packages used
* numpy
* pandas
* sklearn
* nltk
* re
* matplotlib

## Key Highlights
* Checked for missing values
* Data Preprocessing and Cleaning
* Feature Extraction
* Checking feature correlation to the target (Spam or Ham)
* Model training using Random Forest Classifier
* Model evaluation using accuracy, precision, recall, and F1-score


## Dataset
The dataset consists of email messages labeled as either "spam" or "ham" (non-spam). It exhibits a significant class imbalance:
* Ham: 4822 emails
* Spam: 746 emails

## Data Preprocessing and Cleaning
Used isna() to check for missing values, and no missing values were found in the dataset.

Created two features: one representing the number of characters excluding spaces, and another representing the proportion of punctuation in the body text of an email.

Point-Biserial Correlation was applied to determine the relationship between the binary target variable and the newly created features. In addition, histograms were drawn to visualize both features for 'spam' and 'ham' categories. The analysis indicated that the first feature is significant and will be used as an input for training the Random Forest (RF) model.

![image alt](https://github.com/adeyie/Email-Spam-Detection/blob/b6119bb3010486fe20cc763a7f248070d3aeaa22/word_count.png)
![image alt](https://github.com/adeyie/Email-Spam-Detection/blob/28d77c73cefa444a7b10090652f0d79b37cc144a/punc_prop.png)

For data cleaning, the following steps were performed on the body text of email data for classification:

- Lowercasing: Convert all text to lowercase to ensure consistency.
- Number Removal: Remove all numerical characters from the email body.
- Removed Punctuation: To eliminate unnecessary symbols.
- Removed Stop Words: To reduce noise and focus on meaningful words.
- Stemming: To reduce words to their root forms for better classification.

After data cleaning, CountVectorizer with ngram_range=(2,2) was applied to extract bigrams from the email body text. The generated bigrams provide valuable insights into common word pairings.

The dataset is split into training and testing sets using stratified sampling. Stratified sampling ensures that the proportion of spam and ham emails is maintained in both the training and testing sets. This is crucial for preventing biased evaluation for the imbalanced dataset. A test set size of 20% is used to evaluate the model's performance.

We employ a Random Forest (RF) classifier, known for its robustness and ability to handle complex datasets. 

The Random Forest model's performance is evaluated on the test set. Metrics used: 
* Precision: Measures the proportion of correctly predicted spam emails out of all emails predicted as spam. 
* Recall: Measures the proportion of correctly predicted spam emails out of all actual spam emails. 
* F1-score: Harmonic mean of precision and recall, providing a balanced measure. 
* Accuracy: Overall proportion of correctly classified emails.


## Acknowledgements
* Thanks to the creators of the datasets used.
* Special thanks to the open-source community for maintaining libraries and resources.



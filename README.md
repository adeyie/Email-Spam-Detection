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

## Data Preprocessing and Cleaning
Used isna() to check for missing values, and no missing values were found in the dataset.

Created two features: one representing the number of characters excluding spaces, and another representing the proportion of punctuation in the body text of an email.

Point-Biserial Correlation was applied to determine the relationship between the binary target variable and the newly created features. In addition, histograms were drawn to visualize both features for 'spam' and 'ham' categories. The analysis indicated that the first feature is significant and will be used as an input for training the Random Forest (RF) model.

![image alt](https://github.com/adeyie/Email-Spam-Detection/blob/b6119bb3010486fe20cc763a7f248070d3aeaa22/word_count.png)
![image alt](https://github.com/adeyie/Email-Spam-Detection/blob/28d77c73cefa444a7b10090652f0d79b37cc144a/punc_prop.png)

For data cleaning, the following steps were performed on the body text of email data for classification:

Removed Punctuation: To eliminate unnecessary symbols.

Removed Stop Words: To reduce noise and focus on meaningful words.

Stemming: To reduce words to their root forms for better classification.

## Acknowledgements
* Thanks to the creators of the datasets used.
* Special thanks to the open-source community for maintaining libraries and resources.



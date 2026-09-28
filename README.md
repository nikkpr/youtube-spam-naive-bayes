# youtube-spam-naive-bayes
YouTube spam classification using Multinomial Naive Bayes implemented from scratch.
# YouTube Spam Classification with Naive Bayes

Binary classification of YouTube comments using Multinomial Naive Bayes.

The main goal of this project is to implement Multinomial Naive Bayes
from scratch and compare the implementation with scikit-learn.

## Dataset

YouTube Spam Collection from the UCI Machine Learning Repository.

## Approach

1. Data exploration
2. Bag-of-Words representation
3. sklearn MultinomialNB baseline
4. Multinomial Naive Bayes implementation from scratch
5. Hyperparameter tuning
6. Error analysis

## Results

| Metric | Score |
|---|---:|
| Accuracy | 0.935 |
| Spam Precision | 0.896 |
| Spam Recall | 0.976 |
| Spam F1 | 0.934 |

The final model detected 164 out of 168 spam comments in the test set.

## Key findings

The custom implementation produced the same predictions as
scikit-learn's MultinomialNB when using the same hyperparameters.

Error analysis showed several limitations of the Bag-of-Words approach:

- different forms of the same word are treated as separate features;
- rare tokens may receive disproportionately high spam likelihood ratios;
- the model does not capture semantic context;
- patterns such as phone numbers are treated as individual tokens.

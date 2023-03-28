# VietnameseNLP_sentimentAnalysis
Sentiment Analysis from Shopee ecommerce platform comments

comments from the Shopee ecommerce platform, using the underthesea library for text cleaning.
$ pip install underthesea
https://github.com/undertheseanlp/underthesea 

The project consists of 6 steps:

- Preprocessing: Exploratory Data Analysis and text cleaning
- Model Pre-selection: Using Lazy Predict to identify potential machine learning models
- Model selection with Machine Learning (for 3 classes): Applying selected machine learning models from Lazy  Predict, choosing the best model, and tuning hyperparameters
- Model selection with Machine Learning (for 2 classes): Using SMOTE as a resampling technique, applying selected machine learning models from Lazy Predict, choosing the best model, and tuning hyperparameters- 
- Model selection with Pyspark (for 3 classes): Comparing Naive Bayes and Logistic Regression models
- Model selection with Pyspark (for 2 classes): Comparing Naive Bayes and Logistic Regression models


The results of the project show that:

The dataset can be divided into 3 classes based on customer ratings: 1-2 (negative), 3 (neutral), and 4-5 (positive)
However, ratings 1-3 can be seen as areas that require improvement
For 3 classes, applying resampling did not improve results, while for 2 classes, resampling using SMOTE improved results
The final metrics show that normal processing for 3 classes resulted in poor performance, while processing for 2 classes performed better.

  3 class:       precision    recall  f1-score   support

    negative       0.49      0.61      0.55     41218
     neutral       0.36      0.01      0.03     24557
    positive       0.73      0.83      0.78     94234

    accuracy                           0.65    160009
   macro avg       0.53      0.49      0.45    160009
weighted avg       0.61      0.65      0.60    160009
####

   2 class:       precision    recall  f1-score   support

           0       0.66      0.69      0.67     43312
           1       0.78      0.76      0.77     62798

    accuracy                           0.73    106110
   macro avg       0.72      0.72      0.72    106110
weighted avg       0.73      0.73      0.73    106110

### Process with Pyspark: given a faster proceeding
the best result is Naive Bayes Model with 3 classes
Accuracy of model: 0.750074693228309
[[149839.   8994.  25417.]
 [  6893.  32254.  14556.]
 [  8628.   8397.  15062.]]

### with 2 class, best model is Logistic Regression
Accuracy of model: 0.8536307313470617
[[78556. 13699.]
 [12464. 73996.]]
 




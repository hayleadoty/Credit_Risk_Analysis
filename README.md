# Credit Risk Analysis

## Overview of the Analysis

The purpose of this analysis was to employ different machine learning techniques to train and evaluate models to solve the real-world challenge of credit risk. Our dataset comes from LendingClub, a peer-to-peer lending services company. We over-sampled the data using RandomOverSampler and SMOTE algorithms, and under-sampled the data using the ClusterCentroids algorithm. We combined over- and under-sampling using SMOTEENN, then compared BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms to compare models that reduce bias.

## Results

Below are the balanced accuracy, precision, and recall scores of our six machine learning models:

- For our RandomOverSampler model, our balanced accuracy score was 0.65. Precision was 0.99, and recall was 0.68:

![Over-Sampling Classification Report](/images/oversample.png)

- For our SMOTE model, our balanced accuracy score was 0.64. Precision was 0.99, and recall was 0.66:

![SMOTE Classification Report](/images/smote.png)

- For our ClusterCentroids model, our balanced accuracy score was 0.51. Precision was 0.99, and recall was 0.44:

![ClusterCentroids Classification Report](/images/undersample.png)

- For our SMOTEENN model, our balanced accuracy score was 0.64. Precision was 0.99, and recall was 0.57:

![SMOTEENN Classification Report](/images/smoteenn.png)

- For our BalancedRandomForestClassifier model, our balanced accuracy score was 0.79. Precision was 0.99, and recall was 0.91:

![BalancedRandomForestClassifier Classification Report](/images/brfc.png)

- For our EasyEnsembleClassifier model, our balanced accuracy score was 0.93. Precision was 0.99, and recall was 0.94:

![EasyEnsembleClassifier Classification Report](/images/eec.png)

## Summary

As far as balanced accuracy scores, RandomOverSampler, SMOTE, and SMOTEENN models all performed very similarly. RandomOverSampler and SMOTE had similar recall scores. The ClusterCentroids model performed the worst, with the lowest balanced accuracy and recall scores. The two best performing models were the ensemble models: BalancedRandomForestClassifier and EasyEnsembleClassifier.

Our precision score for each machine learning model is very close to 1.00, at 0.99. This means that the models' reliability in detecting credit risk was high, but also over-sensitive to the data. The high number of false positives in most of our models help to show this. The ensemble models performed much better than other models, but were still over-sensitive to the data. This would result in the lender missing out on potentially low-risk customers who were falsely labeled as high-risk. Therefore, in conclusion, we would not recommend using any of the tested models to predict credit risk.
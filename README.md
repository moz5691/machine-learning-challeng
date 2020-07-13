## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, create machine learning models capable of classifying candidate exoplanets from the raw dataset.

## Two different classifications are used.

* RandomForest
```

                precision    recall  f1-score   support

     CANDIDATE       0.83      0.73      0.78       157
     CONFIRMED       0.84      0.83      0.83       190
FALSE POSITIVE       0.95      1.00      0.97       353

      accuracy                           0.89       700
     macro avg       0.87      0.85      0.86       700
  weighted avg       0.89      0.89      0.89       700
```
![](img/randomforest.png)

* SVC
```

               precision    recall  f1-score   support

     CANDIDATE       0.79      0.66      0.72       157
     CONFIRMED       0.76      0.83      0.79       190
FALSE POSITIVE       0.97      0.99      0.98       353

      accuracy                           0.87       700
     macro avg       0.84      0.83      0.83       700
  weighted avg       0.87      0.87      0.87       700
```

![](img/svc.png)

* Neural Network (Tensorflow)

```
                precision    recall  f1-score   support

           0       0.77      0.78      0.77       177
           1       0.79      0.73      0.76       179
           2       0.97      1.00      0.98       344

    accuracy                           0.87       700
   macro avg       0.84      0.84      0.84       700
weighted avg       0.87      0.87      0.87       700

```

![](img/ann.png)

## Conclusion
RandomForest performance is slightly better than SVC.  However, its model size of RandomForest is 50MB while SVC model size is about 1MB.  RamdomForest takes a lot more computation power and storage size for its model.   
ANN model shows similar performance as RamdomForest and SVC.  



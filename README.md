# Credit_Risk_Analysis



## Purpose 

The purpose of this analysis was to determine credit card risk through the use of supervised machine learning algorithms. Specifically, a large, unbalanced data set of over 50,000 credit applications was used to train a range of machine learning algorithms in order to determine which if any could successfully predict low and high-risk credit applications.  Methods utilized and evaluated included over and under sampling models, as well as a combination of the 2. In addition, two newer algorithms were employed: Balanced Random Forest, and Easy Ensemble Classifier. The analysis below will detail the balanced accuracy score as well as precision and recall scores for each model, and then provide a recommendation on which if any of the models would be sufficient for predicting credit risk. 



## Results 

### Random Over Sampler Model
![OversamplingReport](https://user-images.githubusercontent.com/81761879/130283920-3b9fa990-2d7c-45e3-ad25-197b0337c873.PNG)

* Model had a mediocre balanced accuracy score of 64.7%
* Very high precision (100%) for detecting low-risk applicants, but extremely low precision (1%) of predicting high-risk applicants 
* Fairly mediocre sensitivity for predicting both low-risk applicants (60%) and high -risk applicants (69%)



### SMOTE Model 
![SMOTEreport](https://user-images.githubusercontent.com/81761879/130284782-62288bac-669d-4e47-8b3c-b74ccd1d5573.PNG)

* Model had a mediocre balanced accuracy score of 66.2%
* Very high precision (100%) for detecting low-risk applicants, but extremely low precision (1%) of predicting high-risk applicants 
* Fairly mediocre sensitivity for predicting both low-risk applicants (69%) and high -risk applicants (63%)



### Cluster Centroids Undersampling Model 
![CCUndersamplingReport](https://user-images.githubusercontent.com/81761879/130285032-c85647c8-6ebf-4c7a-943d-b0cf271c52b9.PNG)

* Model had a low balanced accuracy score of 54.4%
* Very high precision (100%) for detecting low-risk applicants, but extremely low precision (1%) of predicting high-risk applicants 
* Low sensitivity for predicting low-risk applicants (40%), and mediocre sensitivity for high -risk applicants (69%)



### SMOTEENN combination Model
![CombinationSamplingReport](https://user-images.githubusercontent.com/81761879/130285522-d88a08eb-646c-4c62-beb2-71a29e14f041.PNG)

* Model had a mediocre balanced accuracy score of 67.7%
* Very high precision (100%) for detecting low-risk applicants, but extremely low precision (1%) of predicting high-risk applicants 
* Low sensitivity for predicting low-risk applicants (57%), but decent sensitivity for high-risk applicants (78%)



### Balanced Random Forest Model
![RandomForestReport](https://user-images.githubusercontent.com/81761879/130285832-6b2c59df-d9e6-4566-a315-a952f4070376.PNG)

* Model had a decent balanced accuracy score of 78.8%
* Very high precision (100%) for detecting low-risk applicants, but extremely low precision (3%) of predicting high-risk applicants 
* Relatively high sensitivity for predicting low-risk applicants (87%), and decent sensitivity for high-risk applicants (70%)



### Easy Ensemble Model 
![EasyEnsemble](https://user-images.githubusercontent.com/81761879/130286049-51139577-ee7f-431c-b185-1a0c3ecbaf43.PNG)

* Model had a high balanced accuracy score of 93.2%
* Very high precision (100%) for detecting low-risk applicants, but low precision (9%) of predicting high-risk applicants 
* High sensitivity for predicting both low-risk applicants (94%)and high-risk applicants (92%)



 ## Summary

Overall, many of the models struggled to accurately predict future credit risk, with only the Balanced Random Forest and Easy Ensemble models having accuracy scores above 70%. Due to the nature of credit risk, it would seem having high sensitivty would be more important than precision relative to detecting high-risk applicants. Therefore, I would recommend using the Easy Ensemble Model for predicting future credit risk, as it had sensitvity above 90% for both groups. While the model may be overly aggresive with predicting high-credit risk as evident by it's low precision score for this group, due to the low volume of these types of applicants, it would be much easier to then individually evaluate these on a case by case basis if needed. In addition, the model could likely be further improved by focusing on specific variables most relevant to credit risk and dropping those features that are not (there were over 90 columns of features in the data set).




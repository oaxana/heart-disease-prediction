## Heart Disease Prediction
***Oaxana Sri***

### Executive summary

This project aims to develop a predictive model for assessing heart disease risk using data from the CDC's 2022 telephone interviews, which includes 445,000 responses. The model is designed to provide actionable insights for both individuals and medical practitioners. For individuals, it offers a user-friendly dashboard to assess their risk level based on health factors, lifestyle choices, and medical history, empowering them to make informed decisions about their health. For medical practitioners, it enhances patient care by providing accurate risk assessments and optimizing resource allocation for high-risk patients.

The dataset is highly imbalanced, with only 6% of respondents classified as having heart disease. To address this, several machine learning models were developed, including Logistic Regression, Decision Trees, Random Forests, XGBoost. These models were evaluated primarily on recall and F1 score to ensure effective identification of positive cases.

The XGBoost model demonstrated the best performance with a recall score of 0.7951, an F1 score of 0.3020, an accuracy of 0.8025, and an ROC AUC score of 0.7990. These results indicate somewhat good performance, particularly in identifying positive cases, though there is room for improvement, especially in the F1 score. This highlights the need for further refinement.

### Research Question
Based on a person’s health factors, lifestyle choices and demographics, what is the likely risk of heart disease?

### Rationale: Why is this important?

1. For Individuals:
- Staying Informed: A user-friendly dashboard will allow individuals to input their health factors, lifestyle choices, and medical history to determine their risk level for heart disease.
- Empowered to Change: By understanding their risk level, individuals can make informed decisions to adjust modifiable risk factors such as smoking or physical activity to improve their heart health.
- Proactive Health Management: Knowledge of their risk allows individuals to be proactive, seeking timely medical advice and interventions, thus enhancing their quality of life and improving survival chances.
2. For Medical Practitioners:
- Enhanced Patient Care: Practitioners can use the model to assess patient risk more accurately, providing targeted advice and interventions to mitigate heart disease risk.
- Resource Optimization: Risk assessments enable healthcare facilities to allocate resources more efficiently, prioritizing high-risk patients for more intensive monitoring and care, thereby improving overall healthcare delivery.

### Data Sources
[Indicators of Heart Disease Dataset from Kaggle](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease/data)
- 2022 data collected by CDC via telephone interviews
- 445k responses with 40 variables
- 2020 data is also available for reference
- Includes both categorical and numerical features

### Methodology
Given the imbalanced nature of the dataset (only 6% of the patients classify as having had heart disease), it will be essential to choose techniques that can handle such imbalance effectively. 
Below are a few models I'm building to create a first draft of this project:

1. Logistic Regression:
- To understand the relationship between individual health factors, lifestyle choices, and demographics with the binary outcome of heart disease presence.
- Use class weighting or SMOTE to address imbalance.
2. Decision Trees:
- To identify the most significant health and lifestyle factors that influence heart disease risk.
- Use techniques like class weighting or boosting (i.e. AdaBoost) to improve performance on imbalanced data.
3. Random Forests:
- To improve prediction accuracy and handle the imbalance in the dataset by aggregating the results of multiple decision trees.
- Use class weighting or balancing techniques during training.
4. Gradient Boosting Machines (GBM):
- To enhance predictive performance by sequentially correcting the errors of a series of weak learners (decision trees).
- Implement XGBoost with appropriate parameters to handle imbalances in the data.


### Results
1. To evaluate prediction models, I focus on the following metrics:
- Primary Metric: Recall – Ensure that you identify as many actual positive cases as possible, minimizing the number of false negatives (FN)
- Secondary Metric: F1 Score – Balance precision and recall to have a more balanced evaluation of model performance.

2. The model with the best Recall score was XGBoost.  Below are evaluation metrics for this model:
- Recall: 0.7951
- F1 Score: 0.3020
- Accuracy: 0.8025
- ROC AUC Score: 0.7990

3. The Top Features of Importance, listed in descending order, from the XGBoost model:
- Had_Angina_YES
- ChestScan_YES
- AgeCategory (ordered oldest to youngest)
- DifficultyWalking_YES
- GeneralHealth (ordered from worst to best)

### Next steps
- Review initial draft with learning instructor and brainstorm ways to improve the prediction model
- Re-examine feature list and remove any features that are not adding value
- Examine data from 2020 to see if it can be used to augment the 2022 dataset
- Reasearcha and test other techniques for dealing with class imbalance
- Try building a Neural Networks model to capture complex, non-linear relationships in the dataset

### Outline of project

- [Link to Jupyter Notebook](https://github.com/oaxana/heart-disease-prediction/blob/main/Heart_Disease_Prediction_03.ipynb)


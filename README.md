### Heart Disease Prediction
***Oaxana Sri***

#### Executive summary


#### Rationale

1. For Individuals:
- Staying Informed: A user-friendly dashboard will allow individuals to input their health factors, lifestyle choices, and medical history to determine their risk level for heart disease.
- Empowered to Change: By understanding their risk level, individuals can make informed decisions to adjust modifiable risk factors such as smoking or physical activity to improve their heart health.
- Proactive Health Management: Knowledge of their risk allows individuals to be proactive, seeking timely medical advice and interventions, thus enhancing their quality of life and improving survival chances.
2. For Medical Practitioners:
- Enhanced Patient Care: Practitioners can use the model to assess patient risk more accurately, providing targeted advice and interventions to mitigate heart disease risk.
- Resource Optimization: Risk assessments enable healthcare facilities to allocate resources more efficiently, prioritizing high-risk patients for more intensive monitoring and care, thereby improving overall healthcare delivery.

#### Research Question
Based on a person’s health factors, lifestyle choices and demographics, what is the likely risk of heart disease?

#### Data Sources
Indicators of Heart Disease Dataset from Kaggle: https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease/data
- 2022 data collected by CDC via telephone interviews
- 445k responses with 40 variables
- 2020 data is also available for reference
- Includes both categorical and numerical features

#### Methodology
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


#### Results
What did your research find?


#### Next steps
What suggestions do you have for next steps?

Neural Networks:
To capture complex, non-linear relationships between health factors, lifestyle choices, and heart disease risk.
Use techniques like class weighting, oversampling, or undersampling to address imbalances.


#### Outline of project

- [Link to notebook 1]()



G

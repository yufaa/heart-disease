# Heart Disease Classification 

## Technical Report


#### Problem Statement

Heart disease is a leading cause of death worldwide. Early detection and diagnosis are crucial for effective treatment and prevention. The goal of this project is to develop a machine learning model that can predict the presence of heart disease in patients based on various medical attributes.

#### Goals

- **Predictive Modeling:** Develop a reliable machine learning model to classify whether a patient has heart disease.
- **Web Deployment:** Deploy the model as a web application to allow easy access and interaction for medical professionals and researchers.
- **Insights Generation:** Provide actionable insights based on data analysis to help understand key factors contributing to heart disease.

#### Solution Statement

Using the UCI Heart Disease dataset, this project involves preprocessing the data, exploratory data analysis (EDA), building and evaluating multiple classification models, and deploying the best-performing model using Streamlit. The solution will enable users to input patient data and get a prediction of heart disease likelihood, along with confidence levels.

### Data Understanding
[UCI Heart Disease dataset](https://archive.ics.uci.edu/dataset/45/heart+disease) contains 76 attributes, but all published experiments refer to using a subset of 14 of them.  In particular, the Cleveland database is the only one that has been used by ML researchers to date.  The "goal" field refers to the presence of heart disease in the patient.  It is integer valued from 0 (no presence) to 4. Experiments with the Cleveland database have concentrated on simply attempting to distinguish presence (values 1,2,3,4) from absence (value 0).  
 
#### Overview Data

Only 14 attributes used:
      1. #3  (age)       
      2. #4  (sex)       
      3. #9  (cp)        
      4. #10 (trestbps)  
      5. #12 (chol)      
      6. #16 (fbs)       
      7. #19 (restecg)   
      8. #32 (thalach)   
      9. #38 (exang)     
      10. #40 (oldpeak)   
      11. #41 (slope)     
      12. #44 (ca)        
      13. #51 (thal)      
      14. #58 (num)

### Methodology

1. **Data Collection:** Gather the dataset from the UCI repository.
2. **Data Preprocessing:** Handle missing values, encode categorical variables, imbalance handling, normalize features.
3. **Exploratory Data Analysis (EDA):** Visualize and summarize the data to gain insights.
4. **Model Building:** Train multiple classification models.
5. **Model Evaluation:** Compare models using accuracy, precision, recall, F1 score.
6. **Model Deployment:** Deploy the best model using Streamlit for real-time prediction.

### Data Preparation

- **Missing Values:** Imputed using the mean for numerical features and the mode for categorical features.
- **Duplicate Data:** Check and Delete Duplicate data 
- **Normalization:** Applied Standard Scaler to scale features.
- **Imbalance Handling** Applied SMOTE to handling imbalance between data.
- **Splitting Data:** Divided the data into training (80%) and testing (20%) sets to evaluate the models.

### Modeling

- **K-Nearest Neighbors (KNN):** Simple and intuitive but sensitive to the choice of k and feature scaling.
- **Random Forest:** An ensemble method that improves accuracy and reduces overfitting.
- **XG-Boost** is a fast, high-performance gradient boosting algorithm for accurate predictions. 


### Evaluation & Result


**Best result in SMOTE + Normalization Data**
- **Accuracy:** The model achieved the highest accuracy of 92%.
- **Precision:** The model showed a precision of 92%.
- **Recall:** The model had a recall of 98%.
- **F1 Score:** The model had the highest F1-score of 92%.


### Conclution

From the experiment above, it can be concluded that the average accuracy of the machine learning model for the heart disease dataset is 92%.
For the KNN algorithm, the highest accuracy is 92% using data that has been SMOTEed, normalized and tuned to the model.
while the lowest accuracy was 75% using SMOTE data, without normalization and tuning in the model.

For the Random Forest algorithm, the highest accuracy is 92% using SMOTE data without norm & tuning and on SMOTE Norm data without tuning,
while the accuracy of the tuned model decreased to 89%. This indicates that the tuning process carried out is less than optimal.

For the XGBoost algorithm, the first 2 experiments obtained 90% accuracy. while in the third experiment the accuracy was 92%. 

Overall, the use of SMOTE to handle imbalance data can be said to be effective and the tuning process uses grid search
can improve model accuracy.


------

Feel free to adjust the content to better fit the specifics and achievements of your project.

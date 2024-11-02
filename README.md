**Project Overview**
This project aims to leverage machine learning techniques to enhance medical diagnosis by classifying medical conditions and uncovering associations between various health attributes. Using the XGBoost Classifier for classification tasks and applying association rule mining methods such as FP-Growth and ECLAT, this project provides insights that could inform better health management and treatment strategies.

**Data Preprocessing**
**Library Imports and Data Loading:** I began by importing the necessary libraries and loading the dataset into a pandas DataFrame.
**Exploratory Data Analysis (EDA):** Conducted EDA to understand the dataset's structure, including dimensions, column names, the first ten rows, data types, general statistics, and checks for missing values, duplicates, and unique values.
**Data Cleaning:** Replaced unusual values ('?') in the BMI column with the mode and converted the data type of BMI from object to float.
**Data Visualization:** Plotted histograms for numerical variables to visualize their distributions and generated bar graphs for categorical variables such as 'RETINOPATHY.'
**Correlation Analysis:** Created a correlation matrix to assess the relationships between variables, and split the dataset into training and testing sets.
**Model Building**
**Pipeline Construction:** Developed a robust pipeline for training the XGBoost Classifier, ensuring a streamlined process from data preprocessing to model evaluation.
**Hyperparameter Tuning:** Implemented BayesSearchCV for hyperparameter tuning to optimize model performance.
**Model Training:** Trained the XGBoost model using the prepared training set.
**Model Evaluation**
**Performance Metrics:** Evaluated the classifier using accuracy scores, confusion matrix, and classification reports.
Confusion Matrix Insights: The confusion matrix indicated:
True Positives (TP): 113
True Negatives (TN): 83
False Positives (FP): 7
False Negatives (FN): 7
**Feature Importance:** Calculated feature importance to identify the most impactful variables in the model's predictions.
**Results**
**Accuracy Achievements:** The XGBoost Classifier achieved a test accuracy of approximately 84.81%.
Top Features Identified: The top five important features included:
Diabetic Macular Edema
Maculopathy
Duration in years
Hypertension
HBA1C
**Feature Selection Methods
Correlation-Based Feature Selection:**

Top 10 Features: Mean accuracy of 86.47%; Mean F1 score of 86.23%.
Top 5 Features: Mean accuracy improved to 88.75%; Mean F1 score of 88.58%.
Information Gain-Based Feature Selection:

Top 10 Features: Achieved mean accuracy of 87.49%; Mean F1 score of 87.28%.
Top 5 Features: Mean accuracy increased to 89.00%; Mean F1 score of 88.78%.
Learner-Based Feature Selection:

Top 10 Features: Mean accuracy of 89.54%; Mean F1 score of 89.38%.
Top 5 Features: Mean accuracy remained at 89.00%; Mean F1 score of 88.78%.
Comparison with Full Dataset: Training with the full dataset yielded a mean accuracy of 85.00%, demonstrating the benefit of feature selection for model performance.

**Association Rule Mining**
FP-Growth Algorithm:

Frequent Itemsets: Identified frequent conditions, including hypertension and dyslipidemia, with support values ranging from 0.56 to 0.80.
Association Rules: Found strong relationships between conditions, indicating that the presence of hypertension often suggests dyslipidemia, with high confidence values.
**ECLAT Algorithm:**

Frequent Itemsets: Highlighted co-occurrences of conditions such as "Cardiovascular No" and "No Neuropathy."
Significant Association Rules: Notably, the rule indicating that having no cardiovascular issues and no neuropathy strongly correlates with having retinopathy.
Comparative Analysis of Algorithms
Efficiency: FP-Growth was efficient in generating frequent itemsets, while ECLAT exhibited longer processing times for larger datasets.
Memory Usage: FP-Growth consumed less memory due to its compact structure, making it suitable for memory-constrained environments.
Ease of Implementation: Both algorithms have their advantages, with FP-Growth providing efficient library implementations and ECLAT being easier to understand due to its counting approach.
Conclusion
This project underscores the significance of feature selection and association rule mining in enhancing predictive performance and deriving actionable insights in healthcare. The findings reveal that strategic feature selection can significantly boost model accuracy while also shedding light on the relationships between various medical conditions. I'm excited to engage with the community on this project and explore further collaboration opportunities!

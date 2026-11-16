# Medical-Insurance-Cost-Prediction

Problem statement: Predict medical insurance cost given features like age, BMI, smoking status, sex, number of children, and region (Regression Problem)

Source of dataset (with link/reference): Kaggle – Medical Insurance Cost Dataset by Varisha Batool.
https://www.kaggle.com/datasets/varishabatool/data-set/data

Description of key variables/features:

1. Age- Age of primary beneficiary of the insurance (integer value)
2. Sex- Gender of beneficiary- male, female
3. BMI- Body Mass Index
4. Children- Number of children covered by health insurance (integer value)
5. Smoker- Smoking status of the beneficiary- yes, no
6. Region- Residential region in the US- northeast, northwest, southeast, southwest
7. Charges- Medical insurance cost billed to the beneficiary (float value)
   
Summary of preprocessing steps taken:

The dataset was first inspected to check its structure, column types, and any missing values.
Duplicate records were removed and categorical strings were standardized (lowercased and
stripped of spaces) for consistency. Binary variables like sex and smoker were mapped into
numeric form, while the multi-category variable region was later one-hot encoded. For
numerical features such as age, BMI, and children, outliers were identified using the IQR
method and capped to reduce their influence. Missing values, though minimal, were handled
using median imputation for numeric features and mode imputation for categorical ones. New
derived features, such as the interaction between BMI and smoking status, were added to
capture potential risk effects. Finally, a preprocessing pipeline was built using scaling for
numeric features and encoding for categorical ones, ensuring that all transformations were
applied consistently. The clean dataset was then split into training and testing sets (80:20) and
saved as ready-to-use CSV files for model building.

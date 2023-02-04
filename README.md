# Dimensionality-reduction_using_PCA

## Principal Component Analysis helps with dimensionality reduction of highly dimensional datasets.

![image](https://user-images.githubusercontent.com/106458239/216755053-968e8f80-a88f-4d77-b615-add3474dab8c.png)

# Problem Statement

- The need for identifying breast cancer in it's early stages has been increasing.

- The Wisconsin Diagnostic Laboratories have a good record of diagnosing patients with cancer in their early stages.

- But it is a time critical process to generate, analyze and predict if a particular nucleus can be malignant or benign.


> Checking Target Variable

**Benign    357**

**Malignant    212**

![image](https://user-images.githubusercontent.com/106458239/216755234-8cbdedeb-fa6c-42ad-99c3-ee9668e4687c.png)

>**Benign tumors tend to grow slowly and do not spread. Malignant tumors can grow rapidly, invade and destroy nearby normal tissues, and spread throughout the body**.

>In our dataset more number of patients diagonsed with Benign tumors as compared to deadly Malignant tumors.

![image](https://user-images.githubusercontent.com/106458239/216756086-b1efcab6-53c7-47ab-82cb-0edbb360a11f.png)

![image](https://user-images.githubusercontent.com/106458239/216756090-01c8611b-1e33-4fdf-93bb-78a41e39f9b6.png)

**observation:**

- We can see that radius mean & area mean is on higher side for Benign as compared to Malignant.

![image](https://user-images.githubusercontent.com/106458239/216755277-4aad2c20-58de-4fca-a062-d093ee03b36c.png)
**Observations:**

- radius_mean and area_mean are highly correlated.
- radius, texture, prerimeter and area features are highly correlated in all categories.

 >Modelling Development & Evaluation without PCA
 
- In this section, we will develop some baseline models using RandomForestClassifier and a LogisticRegression

- Scores obtained using RandomForestClassifier and a LogisticRegression

>Test_Accuracy_Score: 1.0
>Train_Accuracy_Score:0.9649122807017544

## Dimensionality Reduction using PCA

![newplot (1)](https://user-images.githubusercontent.com/106458239/216755700-af9bf989-639f-4abc-b558-fb7a60092b0b.png)

**Observations:**
- **With only 2 principal components 100% variance can be achieved**

## Modelling Development & Evaluation after PCA

- In this section, we will develop new models using the PCA reduced train and test set.

## Model 1

> Scores obtained using PCA (n_components=2, random_state=0)

>Train_Accuracy_Score: 0.1
>Test_Accuracy_Score:0.90

## Model 2

> Scores obtained using PCA (n_components=6, random_state=42)

>Train_Accuracy_Score: 0.1
>Test_Accuracy_Score:0.96

**Observations:**

- In Model 1 with no of components 2 Logistic Regression model is overfitting.

- In Model 2 with no of components 6 Logistic Score is balanced.

- These models seem to be fitted well on the reduced data in Model 2.




# Sonar-rock-vs-mine

The SONAR Rock Vs Mine Prediction falls under a Classification Machine Learning Problem. The project aims to develop a machine learning model capable of accurately distinguishing between metal cylinders(mines) and rocks based on SONAR return data.

The project is based on SONAR return data. Each data point consists of a set of 60 numerical values ranging from 0 to 1 representing the energy within specific frequency bands over time. The labels are 'M' for mines and 'R' for rock. The numbers in the labels are in increasing order of aspect angle, but they do not encode the angle directly.


##  Models Used
### 1. Logistic Regression
- A linear model that estimates the probability of class membership using the logistic (sigmoid) function.  
- Works well on smaller datasets with linear decision boundaries.  
- Includes **L2 regularization** to prevent overfitting.

### 2. Support Vector Machine (SVM)
- A linear margin-based classifier that finds the optimal separating hyperplane between classes.  
- Uses the **regularization parameter `C`** to control the balance between margin width and training error.  
- Does not output probabilities directly but focuses on maximizing the classification margin.
  
## Methodology
1. The dataset consists of **numeric features (≈60)** and **210 samples**.  
2. Data was split into training and test sets (typically 80/20).  
3. Features were scaled using `StandardScaler`.  
4. Both models were evaluated using:
   - **Training accuracy**
   - **Test accuracy**
   - **Cross-validation (5-fold)** for reliable performance estimation.

## Results Summary
- **Logistic Regression** performed consistently and was easier to interpret.  
- **Linear SVM** showed slightly lower training accuracy but **higher test accuracy**, suggesting better generalization and stronger regularization.  
- Since both models are linear, differences mainly arise from how each optimizes its decision boundary (SVM focuses on margins, Logistic Regression on probabilities).

| Model | Training Accuracy | Test Accuracy | Notes |
|--------|------------------:|---------------:|-------|
| Logistic Regression | 0.8072289156626506 | 0.8095238095238095 | Simple, linear decision boundary |
| SVM (Linear) | 0.7951807228915663 | 0.9285714285714286 | Better generalization, flexible boundary |



## Conclusion
- **Linear SVM** showed slightly lower training accuracy but **higher test accuracy**, suggesting better generalization and stronger regularization.  
- Since both models are linear, differences mainly arise from how each optimizes its decision boundary (SVM focuses on margins, Logistic Regression on probabilities).

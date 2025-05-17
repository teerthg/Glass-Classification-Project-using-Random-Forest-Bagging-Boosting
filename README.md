# Glass Classification Project using Random Forest, Bagging & Boosting

This project applies multiple ensemble learning techniques to the **Glass Identification dataset** to classify different types of glass based on their chemical properties.

---

## 📁 Dataset Description
- **Source:** UCI Machine Learning Repository
- **Features:** 9 numerical features (e.g., RI, Na, Mg, etc.)
- **Target:** Glass Type (multi-class)
- **File Used:** `glass (1).xlsx`, sheet name: `glass`

---

## 🧭 Why Each Step and Skill Was Used

### 1. **Exploratory Data Analysis (EDA)**
- To **understand the structure** and nature of the data
- Detect **missing values**, **anomalies**, or **outliers** early
- Gain insight into the **distribution** and **relationships** between features

### 2. **Data Visualization**
- **Pairplots** were used to visualize the relationship between features and their ability to distinguish glass types
- **Boxplots** helped identify **outliers** that could distort model performance

### 3. **Data Preprocessing**
- **StandardScaler** was applied to ensure all features are on the same scale, as tree-based models can sometimes benefit from balanced input ranges
- **Train-test split** allowed fair evaluation of model generalization

### 4. **Random Forest**
- Used as a **baseline ensemble model** that performs well with minimal tuning
- Helps reduce overfitting by averaging multiple decision trees

### 5. **Bagging**
- Introduced to compare with Random Forest by training multiple estimators on different bootstrapped samples
- Helps reduce **model variance**

### 6. **Boosting (AdaBoost)**
- Implemented to explore performance improvements by focusing on **hard-to-classify instances**
- Boosting sequentially improves weak learners to reduce **bias**

### 7. **Evaluation Metrics**
- Used **confusion matrix**, **precision**, **recall**, and **F1-score** for a well-rounded evaluation, especially in a **multi-class setting**

### 8. **Handling Imbalanced Data**
- Class imbalance can mislead accuracy — hence we addressed it using:
  - **Class weights**
  - Evaluation metrics that are robust to imbalance
  - Recommendation of techniques like **SMOTE** or **resampling**

---

## 🔍 Project Workflow

### 1. Exploratory Data Analysis (EDA)
- Checked data shape, structure, and missing values
- Identified outliers using **boxplots**
- Explored variable relationships using **pairplots**

### 2. Data Preprocessing
- Applied **standardization** using `StandardScaler`
- Performed a **train-test split** (80:20)
- No missing values or categorical variables present

### 3. Model Building

#### ✅ Random Forest Classifier
- Applied as a baseline ensemble method
- Evaluated using **confusion matrix**, **precision**, **recall**, **F1-score**

#### ✅ Bagging (Bootstrap Aggregating)
- Implemented using `BaggingClassifier`
- Aggregates predictions of multiple base estimators trained independently

#### ✅ Boosting (AdaBoost)
- Implemented using `AdaBoostClassifier`
- Sequentially trains weak models focusing on misclassified instances

### 4. Performance Evaluation
- All models evaluated on the **test set**
- Key metrics: Accuracy, Precision, Recall, F1-Score

---

## 🧠 Bagging vs. Boosting: Key Differences

| Feature        | Bagging                       | Boosting                          |
|----------------|-------------------------------|------------------------------------|
| Goal           | Reduce variance               | Reduce bias                        |
| Training       | Parallel                      | Sequential                         |
| Examples       | Random Forest                 | AdaBoost, Gradient Boosting        |
| Risk of Overfit| Lower                         | Higher (needs tuning)              |
| Handling Noise | More robust                   | Less robust                        |

---

## ⚖️ Handling Imbalanced Data

- Checked class distribution in target variable
- Suggested strategies:
  - **Oversampling minority classes**
  - **Undersampling majority classes**
  - Using **class weights** (e.g., `class_weight='balanced'`)
  - Choosing proper **metrics**: Precision, Recall, F1-score
  - Using **Boosting** to focus on difficult samples

---

## ✅ Technologies Used
- Python, Pandas, Seaborn, Matplotlib
- Scikit-learn (Random Forest, Bagging, AdaBoost)
- Jupyter Notebook / Google Colab

---

## 📊 Sample Visualizations
- Pairplots colored by `Type`
- Boxplots for outlier detection

---

## 👤 Author
**Teerth Gupta**  
Master’s Student – Statistics and Data Science  
Uppsala University, Sweden  
GitHub: [https://github.com/teerthg](https://github.com/teerthg)

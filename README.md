# 🔥 Fire Alarm Prediction System using Machine Learning

This project builds a **fire detection system** using **machine learning** based on **electrical device and sensor readings**.  
The goal is to accurately predict whether a **fire occurs (1)** or **not (0)**, with a strong focus on **safety-critical performance**.

---

## 📌 Problem Statement

Fire incidents are **rare but extremely dangerous**.  
Missing a fire event can lead to severe damage, while false alarms are comparatively acceptable.

This makes fire detection a **highly imbalanced classification problem**, where **recall for fire events is more important than accuracy or precision**.

---

## 📊 Dataset Overview

- **Features**: Sensor and electrical device readings  
- **Target Variable**:
  - `0` → No Fire  
  - `1` → Fire  
- **Class Imbalance**:
  - No Fire: ~313,000 samples  
  - Fire: ~2,800 samples  

---

## 🧪 Project Workflow

1. **Loading the Dataset**
2. **Exploratory Data Analysis (EDA)**
   - Distribution of features
   - Missing and duplicate value checks
3. **Feature Engineering**
   - Date handling
   - Removal of low-importance features
4. **Correlation Analysis**
   - Feature vs target relationship
5. **Model Building**
   - Decision Tree Classifier
6. **Pre-Pruning**
   - Controlling tree depth to reduce overfitting
7. **Model Evaluation**
   - Confusion Matrix
   - Classification Report
   - ROC-AUC Score

---

## 🌲 Model Used

- **Decision Tree Classifier**
- Pre-pruning applied to:
  - Improve generalization
  - Reduce overfitting
- Threshold tuning performed to improve fire detection

---

## 📈 Model Performance

### 🔹 ROC-AUC Score
ROC-AUC = 0.9789

- Indicates **excellent separation** between fire and non-fire events
- Suitable for **imbalanced datasets**

---

### 🔹 Confusion Matrix

[[291625 21990]
[ 177 2630]]

- **False Negatives (Fire Missed): 177**
- **True Positives (Fire Detected): 2630**

---

### 🔹 Classification Report (Key Insight)

- **Fire Recall = 0.94**
  - The model detects **94% of all fire events**
- **Precision is low**
  - Many false alarms, which is acceptable for fire alarm systems
- **Accuracy is misleading**
  - Due to heavy class imbalance

---

## 🔥 Why Recall Matters More Than Accuracy

- Missing a fire → **dangerous**
- False alarm → **acceptable inconvenience**

This model intentionally prioritizes **high recall for fire detection**, making it suitable for **real-world safety systems**.

---

## 🧠 Key Conclusion

✔ Strong fire detection capability  
✔ Very low missed fire events  
✔ High ROC-AUC confirms model reliability  
✔ Trade-off between false alarms and safety is acceptable  

> This system is designed to **maximize safety**, not convenience.

---

## 🚀 Future Improvements

- Two-stage fire confirmation system
- Temporal analysis (consecutive alarms)
- Cost-sensitive learning
- Ensemble models (Random Forest, Gradient Boosting)

---

## 📁 Repository Structure

├── Fire_Alarm_Prediction_Decision_Tree.ipynb
├── test.parquet
├── README.md
├── requirements.txt

---

## 🧑‍🎓 Ideal Use Cases

- College Mini / Major Project
- Fire Detection Research
- Safety-Critical ML Demonstration
- Interview / Viva Explanation

---

## ✨ Final Note

This project demonstrates how **machine learning can be applied responsibly** in safety-critical domains by prioritizing **human safety over raw accuracy metrics**.

# Manufacturing Defect Detection using Machine Learning

## 📌 Problem Statement

In manufacturing environments, quality inspection typically occurs at the final stage of production. Detecting defects late increases cost due to material waste, rework, and delayed delivery.

This project builds a predictive quality inspection system that identifies potential machine failures using operational sensor data before final inspection.

---

## 🏭 Business Context

In industrial systems, missing a defective unit (false negative) is significantly more costly than conducting additional inspections (false positive).

Therefore, the model is optimized to maximize **Recall for failure detection** rather than overall accuracy.

---

## 📊 Dataset

AI4I 2020 Predictive Maintenance Dataset

Features include:
- Air Temperature
- Process Temperature
- Rotational Speed
- Torque
- Tool Wear
- Machine Type

Target:
- Machine Failure (0 = Pass, 1 = Fail)

---

## ⚙️ Approach

1. Removed data leakage columns (failure type indicators)
2. One-hot encoded categorical machine types
3. Stratified train-test split
4. Applied SMOTE to handle class imbalance
5. Trained Random Forest and XGBoost models
6. Tuned classification threshold to improve recall

---

## 📈 Results

Initial Recall: 0.69  
After threshold tuning: 0.82  

The model successfully identifies 82% of defective cases.

---

## 🔍 Feature Importance

Top contributing features:
- Torque
- Rotational Speed
- Tool Wear

These align with mechanical stress behavior in rotating equipment.

---

## 🚀 Future Improvements

- Hyperparameter optimization
- Real-time deployment using Azure ML
- Integration with IoT sensor pipelines

---

## 🛠 Technologies Used

- Python
- Pandas
- Scikit-learn
- XGBoost
- Imbalanced-learn
- Google Colab

# 📱 Mobile Phone Price Range Prediction

This project predicts the **price range of mobile phones** based on their hardware and technical specifications.
It demonstrates a complete **end-to-end machine learning pipeline**, from data analysis and preprocessing to model training, evaluation, and prediction.

The goal is to classify mobile phones into one of four categories:
**Low, Medium, High, or Very High** price range.

---

## 📌 Project Overview

- **Problem Type:** Multi-class classification  
- **Domain:** Consumer Electronics / Data Science  
- **Target Variable:** `price_range` (0, 1, 2, 3)  
- **Model Used:** Random Forest Classifier  
- **Framework:** Scikit-learn  

---

## 📊 Dataset

- **Source:** Mobile Phone Pricing Dataset  
- **File Used:** `dataset.csv`  
- **Total Records:** 2,000  
- **Total Features:** 20 (excluding target)  
- **Target Classes:** 4 (evenly distributed)

### Key Features
- `ram`
- `battery_power`
- `px_height`, `px_width`
- `mobile_wt`
- `clock_speed`
- Connectivity & hardware indicators (`wifi`, `blue`, `four_g`, `three_g`, etc.)

✔ No missing values  
✔ Combination of integer and float features  

---

## 🔍 Exploratory Data Analysis (EDA)

The following EDA steps were performed:

- Inspected data structure and data types
- Verified absence of missing values
- Visualized target class distribution
- Generated correlation heatmap
- Analyzed relationships between key features and price range

### Key Insights
- **RAM** has the strongest correlation with price range
- **Battery power** and **pixel resolution** significantly impact pricing
- Connectivity features show relatively low influence

---

## 🔧 Data Preprocessing

- Separated features (`X`) and target (`y`)
- Split dataset into:
  - **Training set:** 80%
  - **Testing set:** 20%
- Applied **StandardScaler** to numerical features
- Prevented data leakage by fitting scaler only on training data

---

## 🧠 Model Selection & Training

### Model Used: Random Forest Classifier

The Random Forest model was chosen due to:
- Strong performance on tabular data
- Ability to capture non-linear feature relationships
- Robustness without heavy feature engineering

```python
RandomForestClassifier(random_state=42)
The model was trained using the scaled training dataset.
```
---

## 📈 Model Evaluation

### Test Set Performance
- **Accuracy:** ~89.25%
- **Precision (weighted):** ~89.61%
- **Recall (weighted):** ~89.25%
- **F1-score (weighted):** ~89.33%

These results indicate **strong and balanced performance across all price categories**.

---

## 🔍 Model Prediction

The trained model was used to predict price ranges on unseen test data.

### Example Predictions

[0 2 1 3 1 2 2 0 3 1]


### Price Range Mapping
- 0 → Low  
- 1 → Medium  
- 2 → High  
- 3 → Very High  

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|--------|
| Python | Programming |
| Pandas / NumPy | Data processing |
| Scikit-learn | Machine learning |
| Matplotlib / Seaborn | Data visualization |
| Jupyter Notebook | Experimentation |

---

## 🚀 How to Run

```bash
git clone https://github.com/SyedHussain23/Mobile_Phone_Pricing.git
cd Mobile_Phone_Pricing
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook Mobile_Phone_Pricing.ipynb
```

---

## 🔮 Future Improvements
- Hyperparameter tuning for Random Forest
- Feature importance analysis
- Try advanced models (XGBoost, LightGBM)
- Add confusion matrix visualization
- Include real-world features (brand, camera specs)

---

👨‍💻 Author

**Syed Hussain Abdul Hakeem**

- LinkedIn: https://www.linkedin.com/in/syed-hussain-abdul-hakeem
- GitHub: https://github.com/SyedHussain23

---

📄 License

This project is open source and available under the MIT License.

---

⭐ Show Your Support

If you found this project useful, consider giving it a ⭐.

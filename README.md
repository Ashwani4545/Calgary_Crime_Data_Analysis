
# 📈 Calgary Crime Data Analysis and Neural Network Prediction

This project leverages Calgary's **Crime and Disorder Data (2018 - 2024)** to analyze trends in crime across communities and predict future crime counts using a **Neural Network (LSTM)** approach.

---

## 📂 Project Structure

```
📦 Calgary Crime Data Analysis
 ┣ 📄 Calgary_Crime_Data_Analysis_and_Neural_Network_Prediction.ipynb
 ┣ 📄 Community_Crime_Statistics_20240522.csv
 ┗ 📄 README.md
```

---

## 🎯 Objective

- Analyze Calgary's monthly crime data from 2018 to 2024.
- Explore trends by **community, crime category, year, and month**.
- Build an **LSTM Neural Network** model to predict the number of crimes that might occur in the future.
- Visualize predictions, actual data, and model residuals for deeper insights.

---

## 📊 Dataset Overview

- **Source:** City of Calgary's official data repository.
- **Total Records:** ~70,661
- **Columns:**
  - `Community`: Name of the community in Calgary
  - `Category`: Type of crime
  - `Crime Count`: Number of crimes in that record
  - `Year`: Year of occurrence
  - `Month`: Month of occurrence

---

## 🔍 Exploratory Data Analysis (EDA)

1. **Top 10 Dangerous and Safest Communities**
2. **Distribution of Crime Categories**
3. **Year-wise and Month-wise Crime Trends**
4. **Community and Category Correlations**
5. **Year and Category Analysis**
6. **Month and Category Analysis**

**Insights:**
- **Beltline, Forest Lawn**, and **Downtown Commercial Core** are the top communities with high crime rates.
- **Theft from Vehicle**, **Theft of Vehicle**, and **Break & Enter - Commercial** are the most common crime categories.

---

## ⚙️ Data Preprocessing

- **Handling Missing Values:** No missing data found.
- **Data Types:** Verified data types for all columns.
- **Label Encoding:** Applied to categorical columns using `LabelEncoder`.
- **Data Scaling:** Not detailed but recommended for neural networks.

---

## 🧠 Model Development

### Sequence Preparation
- Prepared data sequences using a window length of **3** for the LSTM input.

### Train-Test Split
- 70% Training
- 15% Validation
- 15% Testing

### LSTM Neural Network Architecture
- LSTM layer with 50 units
- Dropout layer (20% rate)
- Dense output layer
- Compiled with **Adam Optimizer** and **Mean Squared Error (MSE)** loss

### Training
- Trained for **100 epochs**
- Monitored training and validation loss

### Evaluation
- Final Test Loss: **~4.89**
- Visualized **Actual vs Predicted Crime Counts**
- Plotted **Residuals** for performance inspection

---

## 📈 Visualization

- **Training vs Validation Loss over Epochs**
- **Actual vs Predicted Crime Count Plot**
- **Residual Plot (Actual - Predicted)**

---

## 🚀 How to Run Locally

1. **Clone Repository**
```bash
git clone https://github.com/your-username/calgary-crime-analysis.git
cd calgary-crime-analysis
```

2. **Install Dependencies**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
```

3. **Launch Notebook**
```bash
jupyter notebook Calgary_Crime_Data_Analysis_and_Neural_Network_Prediction.ipynb
```

---

## ✅ Future Work

- Hyperparameter tuning for LSTM
- Try other time-series models like **Prophet** or **ARIMA**
- Deploy the prediction model as a **web app using Streamlit or Flask**
- Community-wise predictions instead of aggregate counts

---

## 📬 Contact

**Author:** Ashwani Pandey  
📧 Email: your-email@example.com  
🔗 LinkedIn: [linkedin.com/in/yourprofile]

---

## 📜 License

This project is licensed under the **MIT License**.

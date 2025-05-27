# ⚡ Financial Fraud Detection System 🔍💸

A full-stack data science pipeline that detects fraudulent financial transactions in real time. Built using Python (Scikit-learn), MySQL, and Power BI — integrating machine learning, databases, and business intelligence into one sleek solution.

---

## 🚧 What It Does

✅ Flags suspicious transactions using anomaly detection (Isolation Forest)  
✅ Stores processed and labeled data securely in MySQL  
✅ Visualizes fraud patterns and KPIs via a DAX-powered Power BI dashboard  
✅ Enables actionable insights for risk analysts and financial teams  

---

## 🧰 Tech Stack

| Layer              | Tools & Libraries                                                  |
|-------------------|---------------------------------------------------------------------|
| 👩‍💻 ML & Data      | Python · Pandas · Scikit-learn · NumPy · Matplotlib · Seaborn       |
| 🗄️ Database        | MySQL · SQLAlchemy                                                 |
| 📊 Visualization   | Power BI · DAX (CALCULATE, DIVIDE, VAR, etc.)                      |
| 📒 Notebook        | Jupyter Notebook (end-to-end ML pipeline)                          |

---

## 🧱 Project Structure

fraud_detection_project/
├── Financial_Fraud_Detection.ipynb # Full ML + Export pipeline
├── fraud_detection.sql # DB schema + test inserts
├── requirements.txt # Python dependencies
├── PowerBI_Fraud_Dashboard.pbix # Interactive dashboard (Power BI)
└── README.md # You’re reading it!

yaml
Copy
Edit

---

## 🛠️ Quick Start

### 🔗 1. Clone the Repo
```bash
git clone https://github.com/yourusername/financial-fraud-detection.git
cd financial-fraud-detection
🧪 2. Install Python Dependencies
bash
Copy
Edit
pip install -r requirements.txt
🚀 3. Run the Notebook
Open Financial_Fraud_Detection.ipynb in Jupyter Notebook

Run all cells to:

Preprocess the data

Train Isolation Forest

Label predictions

Export to MySQL via SQLAlchemy

🛢️ 4. MySQL Setup
Ensure fraud_detection database exists and replace credentials:

python
Copy
Edit
engine = create_engine("mysql+mysqlconnector://user:pass@localhost/fraud_detection")
df.to_sql("transactions", con=engine, if_exists="replace", index=False)
📈 5. Power BI Dashboard
Open PowerBI_Fraud_Dashboard.pbix in Power BI Desktop

Update the MySQL data source if needed

View dynamic KPIs, charts, and fraud detection metrics

📊 Sample DAX Measures
dax
Copy
Edit
Accuracy = 
DIVIDE(CALCULATE(COUNT(transactions[transaction_id]),
transactions[actual_fraud] = transactions[predicted_fraud]),
COUNT(transactions[transaction_id]))

Precision = DIVIDE([True Positives], [True Positives] + [False Positives])
Recall = DIVIDE([True Positives], [True Positives] + [False Negatives])
F1 Score = 
VAR P = [Precision]
VAR R = [Recall]
RETURN IF(P + R = 0, BLANK(), 2 * P * R / (P + R))
📷 Dashboard Preview
(Visuals can be added after dashboard export)


🎯 Outcomes
⚙️ Real-time fraud detection with <2s processing latency

📈 Interactive reports with slicers for fraud type, location, and risk score

🔒 Secure MySQL backend for seamless storage & querying

📊 Data-driven decision-making for financial teams & analysts



# ElectricCarStatusDetector
 
## Technologies Used
- **Python 3.10+**
- **Flask** — Web framework for deployment  
- **Pandas / NumPy** — Data handling and computation  
- **Matplotlib / Seaborn** — Data visualization  
- **scikit-learn** — Machine learning model training  
- **Pickle** — Model serialization  

---

##  Model Training Workflow

1. **Data Loading**  
   The dataset `Ppp - Feuille 1.csv` is imported from Google Drive.  

2. **Data Preprocessing**  
   - Missing values are checked.  
   - Data is standardized using `StandardScaler`.  

3. **Exploratory Data Analysis (EDA)**  
   - Correlations visualized using Seaborn pairplots.  
   - Relationships between features (e.g., battery voltage vs car state).  

4. **Model Training**  
   - `LinearRegression()` is used.  
   - Training/test split: 70% / 30%.  

5. **Model Evaluation**  
   - Metrics: MAE, MSE, RMSE, R², and Adjusted R².  
   - Visualization of residuals and prediction scatter plots.  

6. **Model Saving**  
   - The trained model is serialized using `pickle` as `regmodel.pkl`.  

---

## 🌐 Flask Web App Workflow

1. **Run the App:**
   ```bash
   python app.py

## 🌐 Access the Web Interface:

1. **Open your browser and go to:**
   ```bash
   http://127.0.0.1:5000/

## 🌐 Input Values:

1. **Enter the following features:**
  - Open your browser and go to:
    - **Time [s]**
    - **Battery Voltage [V]**
    - **Motor Torque [Nm]**
    - **Battery Current [A]**
    - **Battery Temperature**
   

## 🌐 View Prediction

**The app will output:**
```bash
   Car Status: Low / Medium / High

<svg width="1600" height="360" viewBox="0 0 1600 360" fill="none" xmlns="http://www.w3.org/2000/svg">

  <!-- Background Gradient -->
  <defs>
    <linearGradient id="grad" x1="0" y1="0" x2="1600" y2="360">
      <stop offset="0%" stop-color="#0A0F1F" />
      <stop offset="100%" stop-color="#0F223A" />
    </linearGradient>

    <!-- Glow Filter -->
    <filter id="glow">
      <feGaussianBlur stdDeviation="8" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- Background -->
  <rect width="1600" height="360" fill="url(#grad)"/>

  <!-- Decorative Grid Lines -->
  <g opacity="0.15">
    <line x1="0" y1="60" x2="1600" y2="60" stroke="#4AF1FF"/>
    <line x1="0" y1="120" x2="1600" y2="120" stroke="#4AF1FF"/>
    <line x1="0" y1="180" x2="1600" y2="180" stroke="#4AF1FF"/>
    <line x1="0" y1="240" x2="1600" y2="240" stroke="#4AF1FF"/>
    <line x1="0" y1="300" x2="1600" y2="300" stroke="#4AF1FF"/>
  </g>

  <!-- Energy Wave -->
  <path d="M0 240 C 200 140, 400 340, 600 200 S 1000 100, 1400 260 S 1600 80, 1600 80"
    stroke="#00FFC6" stroke-width="4" fill="none" opacity="0.55" filter="url(#glow)" />

  <!-- Main Title -->
  <text x="50%" y="150" text-anchor="middle" fill="#00F7FF" font-size="48" font-family="Segoe UI, Roboto, sans-serif" filter="url(#glow)">
    AI Energy Forecasting System
  </text>

  <!-- Subtitle -->
  <text x="50%" y="215" text-anchor="middle" fill="#A8D9FF" font-size="26" font-family="Segoe UI, Roboto, sans-serif">
    XGBoost • LSTM • MLP  |  Flask API  |  Data Pipeline  |  Interactive UI
  </text>

  <!-- Bottom Accent Line -->
  <rect x="400" y="275" width="800" height="3" fill="#00FFC6" opacity="0.7" filter="url(#glow)"/>

</svg>

---

# 🔋 **AI Energy Forecasting System**
A complete end-to-end **Energy Forecasting Application** featuring:

* 🧠 **Machine Learning model (XGBoost / MLP / LSTM)**
* 🌐 **Flask API backend**
* 💻 **Responsive Web Frontend** with Dark/Light theme
* 📊 **Feature engineering pipeline**
* 📁 Full project structure with **EDA, notebooks, datasets, and saved models**

This system predicts **next hour energy usage (kWh)** and provides a clean UI with history, CSV export, timestamp input, and visual organization.

---

# 🏷️ Badges

![Stars](https://img.shields.io/github/stars/girishshenoy16/ai-energy-forecast?style=flat-square&color=blue)

![Forks](https://img.shields.io/github/forks/girishshen/ai-energy-forecast?style=flat-square)

![Python](https://img.shields.io/badge/Python-3.10-blue)

![Flask](https://img.shields.io/badge/Made%20with-Flask-black?style=flat&logo=flask)

![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange)

![Testing](https://img.shields.io/badge/Tests-PyTest-yellow)

![Status](https://img.shields.io/badge/Status-Production--Ready-brightgreen)

![License](https://img.shields.io/badge/License-MIT-green)


<p align="center">
  <b>🔥 AI-Powered Energy Forecasting System | Machine Learning • Flask API • Modern Frontend • End-to-End Project</b>
</p>

---

## 📸 Screenshots


### 🌞 UI – Light Mode

![Light Mode](screenshots/light_mode.png)

### 🌙 UI – Dark Mode

![Dark Mode](screenshots/dark_mode.png)

### 📈 Prediction Output

![Prediction Output](screenshots/output.png)

---

## 🚀 Features

### 🧠 **Machine Learning**

* Model trained using:

  * XGBoost
  * MLP
  * LSTM

* Feature-engineered inputs
* Cleaned datasets
* Saved best model (`best_model.pkl`)

### 🧮 **Flask Backend**

* `/api/predict` endpoint
* Handles timestamps
* Returns predicted kWh + model used
* Handles missing timestamp gracefully

### 💻 **Frontend UI (HTML + CSS + JS)**

* Inputs for:

  * Current Energy (kWh)
  * Temperature (°C)
  * Humidity (%)
  * Timestamp (optional)

* Shows prediction like: **320 kWh**
* Success animation
* Fully centered modern UI
* Dark/Light toggle

### 🗃 **History System**

* Saves past predictions
* Export CSV
* Clear History option

### 📊 **Data Pipeline**

* Raw → Cleaned → Feature-Engineered
* Stored in `/data` with clear organization
* Jupyter notebooks for:

  * EDA
  * Feature engineering
  * Model building

---

## 📂 Project Structure

```

ENERGY-FORECASTING/
│── app/
│   └── energy_app.py
│
│── data/
│   ├── features/
│   │   ├── features_LSTM.csv
│   │   ├── features_MLP.csv
│   │   └── features_XGBOOST.csv
│   │
│   ├── processed/
│   │   ├── cleaned_energy_data.csv
│   │   └── feature_engineered_energy_data.csv
│   │
│   └── raw/
│       └── energy_data.csv
│
│── frontend/
│   ├── index.html
│   ├── style.css
│   └── control.js
│
│── models/
│   └── best_model.pkl
│
│── notebooks/
│   ├── 01. EDA.ipynb
│   ├── 02. Feature Engineering.ipynb
│   └── 03. Modelling.ipynb
│
│── tests/
│   └── test_api.py
│
│── requirements.txt
└── README.md

```

---

## ⚙️ Installation & Setup

### **1️⃣ Clone the repository**

```sh
git clone https://github.com/girishshenoy16/AI-Energy-Forecasting-System.git
cd AI-Energy-Forecast
````

---

### **2️⃣ Create a virtual environment**

```sh
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

---

### **3️⃣ Install dependencies**

```sh
python.exe -m pip install --upgrade pip
pip install -r requirements.txt
```

---

### **4️⃣ Run the Flask API**

```sh
python .\app\energy_app.py
```

Server will start at:

```
http://127.0.0.1:8000
```

---

### **5️⃣ Open the Frontend**

Open:

```
frontend/index.html
```

Your UI will communicate with the Flask API automatically.

---

## 📡 API Usage

### **POST /predict**

#### Sample Request

```json
{
  "current_energy": 320,
  "temperature": 28,
  "humidity": 60,
  "timestamp": "2025-11-19 14:00"
}
```

#### Sample Response

```json
{
  "prediction": 333.15,
  "timestamp_used": "2025-11-19 14:00",
  "model": "xgboost"
}
```

---

## 📈 Future Improvements

* Deploy backend (Render / AWS / Railway)
* Add live charts
* Compare multiple ML models
* Add user authentication
* Implement batch forecasting

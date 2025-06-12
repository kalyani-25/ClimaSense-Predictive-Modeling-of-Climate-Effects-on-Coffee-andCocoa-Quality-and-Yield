# 🌱 EcoBeanAI – Predictive Modeling of Climate Effects on Cocoa & Coffee Quality

ClimaSense is a machine learning-powered project designed to predict the **quality** and **yield** of coffee and cocoa crops under changing climate conditions. The system integrates real and synthetic datasets, deep learning, and tree-based models, and presents predictions via an interactive web dashboard.

## 🔍 Project Objectives

- Analyze the impact of climate variables (temperature, rainfall, altitude) on coffee and cocoa.
- Predict both **yield** and **sensory quality** using supervised ML techniques.
- Use **synthetic data augmentation** (GANs, CTGAN, CVAE) to improve model performance.
- Build an intuitive **React web interface** to deliver results in real-time.

---

## 🧠 Models Used

- **GRU / LSTM**: For time-series modeling of climate patterns
- **XGBoost / Random Forest**: For robust tabular prediction
- **TabNet**: For interpretable deep learning with attention
- **CTGAN / CVAE**: For synthetic data generation
- **PyTorch-Wrapped XGBoost**: Multi-target optimized predictor

---

## 📁 Project Structure

```bash
ClimaSense/
│
├── 📂 data/                      # Cleaned and merged climate + crop datasets
├── 📂 models/                    # Trained model files (.pkl / .joblib)
├── 📂 notebooks/
│   ├── Clean_coffee_*.ipynb     # Coffee data cleaning
│   ├── Coffee_bot_scrapper/     # CQI scraper scripts
│   ├── LSTM.ipynb               # Deep learning for coffee
│   ├── Wrapper.ipynb            # PyTorch-wrapped XGBoost
│   ├── Coca_Quality_Prediction_Final.ipynb
│   └── Cocoa_Yeild_Prediction_Final.ipynb
├── 📂 src/frontend/              # React + Vite dashboard interface
├── 📄 Final_Report.pdf           # Full IEEE-style research paper
├── 📄 0_Appendix.pdf             # File descriptions
└── 📄 README.md                  # This file


## 📊 Evaluation Results

### Cocoa Quality (Real + Synthetic)

| Model                        | R² Score | MAE (out of 10) |
|-----------------------------|----------|-----------------|
| TabNet (Real)               | 0.9579   | 9.91            |
| TabNet + GAN                | 0.9559   | 9.90            |
| XGBoost + Conditional GAN   | 0.5280   | 9.41            |
| TabNet + CVAE               | 0.4520   | 9.45            |
| Optuna TabNet + CVAE        | 0.4030   | 9.40            |

---

### Cocoa Yield (Real + Synthetic)

| Model                | R² Score | MAE (kg/ha) | MAE Score (out of 10) |
|---------------------|----------|-------------|------------------------|
| TabNet + Real Data  | 0.9997   | 267.28      | 9.11                   |
| TabNet + VAE        | 0.9991   | 382.03      | 8.73                   |
| Deep Neural Network | 0.9991   | 507.21      | 8.31                   |
| Complex TabNet      | 0.9900   | 995.02      | 6.68                   |
| Simple TabNet       | 0.9880   | 1067.51     | 6.44                   |

---


## 🌍 Web Dashboard

Built using **React + Vite**, the dashboard provides:

- Intuitive input sliders for temperature, rainfall, and altitude
- Predictions for yield and quality based on real or projected data
- Local model inference (no server required)
- Fast and lightweight deployment for rural access

## 📈 Visualizations
- Confusion Matrices
- Horizontal Bar Chart: Model Accuracy Comparison
---

## ⚙️ Installation
pip install -r requirements.txt

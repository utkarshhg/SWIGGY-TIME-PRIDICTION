

# Swiggy Delivery Time Prediction 🚀

## 📌 Project Overview
This project predicts **food delivery times** for Swiggy orders using machine learning. It integrates:
- **Data preprocessing & feature engineering**
- **Model training & evaluation**
- **MLOps pipeline with DVC**
- **Deployment using FastAPI/Streamlit/Docker**

The goal is to build a reproducible, scalable, and production-ready ML system.

---

## 📂 Repository Structure
```
swiggy-time-prediction/
│── data/                  # Raw and processed datasets
│── notebooks/             # Jupyter notebooks for exploration
│── src/                   # Source code (training, preprocessing, utils)
│── models/                # Saved models
│── dvc.yaml               # DVC pipeline definition
│── requirements.txt       # Python dependencies
│── Dockerfile             # Containerization setup
│── README.md              # Project documentation
```

---

## ⚙️ Tech Stack
- **Languages**: Python (pandas, scikit-learn, numpy)
- **MLOps Tools**: DVC (Data Version Control), Git
- **Deployment**: FastAPI, Docker, Streamlit (optional UI)
- **Experiment Tracking**: DVC metrics, Git commits

---

## 🔄 Workflow
1. **Data Preprocessing**  
   - Handle missing values, categorical encoding, feature scaling  
   - Save processed dataset with DVC  

2. **Model Training**  
   - Train ML models (Random Forest, XGBoost, etc.)  
   - Evaluate using metrics (MAE, RMSE, R²)  
   - Save trained model with DVC  

3. **MLOps with DVC**  
   - Track datasets, models, and experiments  
   - Reproduce pipelines with `dvc repro`  

4. **Deployment**  
   - Expose prediction API with FastAPI  
   - Containerize with Docker  
   - Optional: Streamlit dashboard for visualization  

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/swiggy-time-prediction.git
cd swiggy-time-prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Initialize DVC
```bash
dvc init
dvc repro
```

### 4. Run FastAPI server
```bash
uvicorn src.app:app --reload
```

### 5. Docker Deployment
```bash
docker build -t swiggy-prediction .
docker run -p 8000:8000 swiggy-prediction
```

---

## 📊 Example API Usage
```bash
POST /predict
{
  "order_id": 12345,
  "restaurant_lat": 25.43,
  "restaurant_long": 81.77,
  "delivery_distance": 5.2,
  "traffic_level": "High"
}
```

Response:
```json
{
  "predicted_delivery_time": "32 minutes"
}
```

---

## 🛠️ Future Improvements
- Integrate CI/CD pipeline (GitHub Actions)  
- Add real-time monitoring with Prometheus/Grafana  
- Deploy on cloud (AWS/GCP/Azure)  

---

## 👨‍💻 Author
- **Utkarsh Gupta**  
- Freelancer | Competitive Programmer | ML Enthusiast  


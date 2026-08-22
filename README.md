# 🍷 Wine Quality Prediction

A machine learning web application that predicts whether a wine is of **Good Quality** or **Bad Quality** based on its physicochemical properties. The project covers the full ML workflow — data exploration, model training, and deployment — and ships with a Flask web app for real-time predictions.

## 📌 Overview

Wine quality is traditionally assessed through sensory evaluation by human tasters, which is subjective and time-consuming. This project uses a supervised machine learning model trained on physicochemical test data (acidity, sugar, sulphates, alcohol content, etc.) to predict wine quality objectively and instantly.

## ✨ Features

- End-to-end ML pipeline: data preprocessing, EDA, and model training (see the Jupyter notebook)
- Trained classification model serialized as `model.pkl`
- Flask-based web interface for entering wine attributes and getting instant predictions
- Clean, simple HTML templates for input and result display
- Dockerfile included for containerized deployment

## 🛠️ Tech Stack

- **Language:** Python
- **Web Framework:** Flask
- **ML & Data:** scikit-learn, NumPy, pandas
- **Visualization:** Matplotlib, Seaborn
- **Prototyping:** Streamlit
- **Deployment:** Docker

## 📁 Project Structure

```
Wine-Quality-Prediction/
│
├── Raw_Data/                          # Dataset used for training
├── templates/                         # HTML templates for the Flask app
├── Wine_Quality_Prediction_Notebook.ipynb   # EDA + model training notebook
├── app.py                             # Flask application entry point
├── model.pkl                          # Serialized trained model
├── requirements.txt                   # Project dependencies
├── Dockerfile                         # Container configuration
└── README.md
```

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/Wine-Quality-Prediction.git
   cd Wine-Quality-Prediction
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

Run the Flask application locally:

```bash
python app.py
```

Then open your browser and navigate to:

```
http://127.0.0.1:5000/
```

Enter the wine's physicochemical attributes in the form (fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, and alcohol) to get an instant quality prediction — **Good Quality Wine** or **Bad Quality Wine**.

### 🐳 Running with Docker

```bash
docker build -t wine-quality-prediction .
docker run -p 5000:5000 wine-quality-prediction
```

## 🧠 Model

The model is trained on a wine quality dataset containing 11 physicochemical input features:

| Feature | Description |
|---|---|
| Fixed Acidity | Non-volatile acids in wine |
| Volatile Acidity | Acetic acid content |
| Citric Acid | Adds freshness and flavor |
| Residual Sugar | Sugar remaining after fermentation |
| Chlorides | Salt content |
| Free Sulfur Dioxide | Prevents microbial growth |
| Total Sulfur Dioxide | Total SO₂ present |
| Density | Density of the wine |
| pH | Acidity/alkalinity level |
| Sulphates | Wine additive contributing to SO₂ levels |
| Alcohol | Alcohol percentage |

Model training, evaluation, and comparison steps are documented in `Wine_Quality_Prediction_Notebook.ipynb`.

## 📊 Dataset

The dataset used is located in the `Raw_Data/` folder and is based on the publicly available **Wine Quality Dataset** (physicochemical tests and quality ratings of red/white wine samples).

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository, open an issue, or submit a pull request with improvements.

## 📄 License

This project is open-sourced for educational and learning purposes.

## 👤 Author

**Kashish Gangwar**

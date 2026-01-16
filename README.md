# Student Math Score Prediction

This project predicts **Math scores** of students based on multiple demographic and academic factors. It demonstrates a complete **end-to-end Machine Learning pipeline**, from data analysis to model deployment using **Docker** and **Flask**.

---

## Problem Statement

Student performance is influenced by several factors beyond academic ability. This project aims to understand and model how a student's **Math score** is affected by:

* Gender
* Ethnicity
* Parental level of education
* Lunch type
* Test preparation course

The final goal is to build a robust regression model that can accurately predict Math scores and deploy it as a web application.

---

## Machine Learning Approach

* **Type:** Supervised Learning (Regression)
* **Target Variable:** Math Score
* **Evaluation Metric:** R² Score
* **Model Selection Strategy:**

  * Multiple regression algorithms are trained
  * Hyperparameter tuning using Grid Search (via a custom `evaluate_model` utility)
  * Best model selected based on highest R² score on test data

### Models Trained

The following models are trained and evaluated:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor
* AdaBoost Regressor
* K-Neighbors Regressor
* XGBoost Regressor
* CatBoost Regressor

Each model is trained with a predefined hyperparameter grid, and the best-performing model is automatically selected and saved.

---

## Project Workflow

1. **Data Ingestion**

   * Load raw student performance dataset

2. **Exploratory Data Analysis (EDA)**

   * Univariate & multivariate analysis
   * Correlation analysis
   * Visualizations using Seaborn & Matplotlib

3. **Data Transformation**

   * Handling categorical features
   * Feature scaling
   * Train-test split

4. **Model Training & Evaluation**

   * Multiple models trained
   * Performance comparison using metrics like RMSE and R²

5. **Model Serialization**

   * Best model saved using `dill`

6. **Web Application**

   * Flask-based web interface for predictions

7. **Dockerization**

   * Application containerized and pushed to Docker Hub

---

## Tech Stack

* **Programming Language:** Python
* **Data Analysis:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn, CatBoost, XGBoost
* **Backend:** Flask
* **Serialization:** Dill
* **Environment:** Docker

---

## Requirements

Create a virtual environment and install dependencies using:

```bash
pip install -r requirements.txt
```

### `requirements.txt`

```txt
ipykernel
pandas
numpy
seaborn
matplotlib
scikit-learn
catboost
xgboost
Flask
dill

# -e .
```

---

## Running the Project Locally

### 1️. Clone the Repository

```bash
git clone https://github.com/kirtanmandaviya/MLProject.git
cd MLProject
```

### 2️. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3️. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️. Run Flask App

```bash
python app.py
```

Open browser and go to:

```
http://localhost:8080/
```

---

## Docker Usage

The Docker image for this project is **publicly available on Docker Hub**.

### Pull the Image

```bash
docker pull kirtanpatel007/student-math-score:latest
```

### Run the Container

```bash
docker run -p 8080:8080 kirtanpatel007/student-math-score:latest
```

Then open:

```
http://localhost:8080
```

---

## Example Use Case

* Educational institutions analyzing student performance
* Predicting outcomes based on socio-economic factors
* Learning end-to-end ML deployment for real-world projects

---

## Project Structure (High Level)

```
├── src/
│   ├── components/
│   ├── pipeline/
│   ├── exception.py
│   ├── logger.py
|   ├── utils.py
├── artifacts/
├── templates/
├── app.py
├── requirements.txt
├── Dockerfile
├── README.md
```

---

## Key Highlights

* End-to-end ML pipeline
* Clean modular code structure
* Model comparison & selection
* Flask web app
* Dockerized deployment

---

## Author

**Kirtan Patel**

---

#### If you like this project, don’t forget to give it a star!

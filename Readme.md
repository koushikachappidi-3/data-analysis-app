
# Data Analysis App

## Table of Contents
- [Purpose](#purpose)  
- [System Requirements](#system-requirements)  
- [Installation Guide](#installation-guide)  
- [Features and Walkthrough](#features-and-walkthrough)  
- [Design Decisions](#design-decisions)  



## Purpose
The **Data Analysis App** is a Flask-based dashboard that analyzes **donation** and **consumer** datasets. It provides **interactive data visualizations** and **forecasting models** to identify patterns and predict future needs.  

Built with **Flask**, **Matplotlib**, and **XGBoost**, this project demonstrates skills in web development, data preprocessing, machine learning, and visualization.  



## System Requirements

**Prerequisites:**  
Before running the project locally, install:  

- **Python (3.9 or later)** – Required to run the Flask backend.  
- **pip** – Comes with Python, used to install dependencies.  
- **Git** – Required to clone the repository and manage version control.  



## Installation Guide

1. **Clone the Repository**
```bash
git clone git@github.com:koushikachappidi-3/data-analysis-app.git
cd data-analysis-app
```

2. **Create Virtual Environment (Optional but Recommended)**
```bash
python3 -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Add Datasets**  
Place the following files in the project root:  
- `Consumer_Dataset.csv`  
- `Donation_Dataset.csv`  

*(These are ignored in Git for privacy but required for running the app.)*

5. **Run Locally**
```bash
python app.py
```
Access at: [http://127.0.0.1:5000](http://127.0.0.1:5000)  

## Features and Walkthrough

### 1. Home Page
- Provides a clean dashboard landing page with navigation links to **Visualization**, **Forecasting**, and **About**.  
<img width="1470" height="575" alt="homepage" src="https://github.com/user-attachments/assets/87803ab3-8d05-4f75-8cc6-f8f126ec960d" />

### 2. Visualization
- Displays **Monthly Trends** for donations and consumption in subplots.
<img width="1457" height="690" alt="dv 1" src="https://github.com/user-attachments/assets/17464ae3-d661-48a4-9af0-c208a848ee64" />

<img width="1407" height="616" alt="image" src="https://github.com/user-attachments/assets/a09354c2-ef38-4540-8061-78c9972fbe4d" />

- Provides **EDA charts** for deeper insights:  

####  Distribution of Donation Quantities 
<img width="1348" height="634" alt="1" src="https://github.com/user-attachments/assets/7c64e8e9-b411-4718-969e-dee4442a664c" />


#### Box Plot of Quantities Taken by Consumers 
<img width="1214" height="609" alt="image" src="https://github.com/user-attachments/assets/d5677496-d2e0-491b-8aab-d830af8ec078" />


#### Top Donated Items
<img width="1292" height="643" alt="image" src="https://github.com/user-attachments/assets/48372b0f-6c24-4758-b937-4984c43352fb" />


#### Top Requested Items
<img width="1355" height="629" alt="image" src="https://github.com/user-attachments/assets/96636ad1-86e0-45d9-9cdd-8fb1ed0d760f" />

### 3. Forecasting
- Interactive dropdown to choose lag periods (**12, 18, 24, 30 months**).  
- Uses **XGBoost** to forecast donations and consumption for the next 24 months.  
- Displays two plots: **Donation Forecast** and **Consumer Forecast**.

  <img width="1469" height="448" alt="image" src="https://github.com/user-attachments/assets/a9aa2548-5201-406a-aebf-be416fb61930" />


#### Donation Forecast
<img width="1343" height="702" alt="image" src="https://github.com/user-attachments/assets/31d961c7-889f-4b8a-86f3-0dc770a4b960" />

#### Consumer Forecast
<img width="1300" height="671" alt="image" src="https://github.com/user-attachments/assets/c2d5317a-a339-494b-9bff-b529b568d577" />

### 4. About
- Explains the purpose and methodology of the project.  
- Lists key technologies: Flask, Python, Pandas, NumPy, Matplotlib, XGBoost.  
<img width="1470" height="343" alt="image" src="https://github.com/user-attachments/assets/bd4f073e-37ea-4b6b-af7b-c7ec4274249f" />

## Design Decisions

### Technology Stack
- **Backend**: Flask (Python) for routing and template rendering.  
- **Frontend**: HTML , Bootstrap, and custom CSS.  
- **Data Analysis**: Pandas, NumPy for preprocessing.  
- **Visualization**: Matplotlib with base64 encoding for embedding plots.  
- **Forecasting**: XGBoost + scikit-learn.  

### Data Handling
- Monthly aggregation ensures clear time-series trends.  
- Base64 encoding allows plots to render dynamically in HTML without saving static images.  
- `.gitignore` excludes CSV datasets from version control.  

### Deployment
- Runs locally with Python.  
- Can be containerized with Docker or deployed to cloud (Heroku/AWS) if needed.  

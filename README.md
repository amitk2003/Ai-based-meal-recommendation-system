<h1 align="center">AI-Powered Meal Recommendation System</h1>

<div align="center">
<img src="Assets/logo_img1.jpg" width="200"/>

### Personalized Nutrition Recommendation using Machine Learning
A web-based system that recommends healthy meals based on user attributes such as **age, height, weight, dietary preferences, and nutritional requirements**.

Built using **Scikit-learn, FastAPI, and Streamlit**.
</div>

---

# Project Overview

Maintaining a balanced diet is essential for a healthy lifestyle. However, many people struggle to choose meals that meet their nutritional requirements.

This project builds an **AI-powered meal recommendation system** that analyzes nutritional information and user health parameters to suggest **personalized meal plans**.

The system uses a **content-based recommendation approach** that matches user preferences and nutritional needs with similar recipes from a large dataset.

---

# Features

- Personalized meal recommendations based on user inputs
- Content-based recommendation engine
- Nutrition-based filtering of recipes
- Fast API backend for ML model serving
- Interactive Streamlit web interface
- Docker containerized deployment
- Large-scale recipe dataset integration

---

# Dataset

The system uses the **Food.com Recipes Dataset** from Kaggle.

Dataset details:

- **500,000+ recipes**
- **1.4 million user reviews**
- Nutritional attributes including:
  - Calories
  - Protein
  - Fat
  - Carbohydrates

Dataset Link:

https://www.kaggle.com/datasets/irkaal/foodcom-recipes-and-reviews

---

# Machine Learning Approach

The recommendation engine uses a **content-based filtering technique**.

It analyzes the **nutritional attributes of recipes** and recommends similar meals using **cosine similarity**.

### Algorithm Used

**Nearest Neighbors Algorithm (Scikit-Learn)**

The model identifies recipes with similar nutritional characteristics using cosine similarity.

Formula:  cos(θ) = (A · B) / (||A|| ||B||)

This approach helps match user nutritional requirements with suitable meals.

---

# System Architecture
deployment architecture diagram
User
  ↓
Streamlit UI (Docker container)
  ↓
FastAPI Backend (Docker container)
  ↓
ML Recommendation Engine
  ↓
Food Dataset
<div align="center">
<img src="Assets/Architecture_diagram.png" width="600"/>
</div>

The system consists of three main components:

### Backend (FastAPI)

- Handles API requests
- Processes user inputs
- Runs the recommendation model

### Machine Learning Model

- Nearest Neighbors model
- Content-based similarity search

### Frontend (Streamlit)

- Interactive web interface
- User inputs health parameters
- Displays recommended meals

---

# Technologies Used

| Category | Tools |
|--------|--------|
| Programming | Python |
| Machine Learning | Scikit-learn |
| Data Processing | Pandas, NumPy |
| Backend API | FastAPI |
| Frontend | Streamlit |
| Deployment | Docker, Docker Compose |
| Visualization | Streamlit ECharts |

---
## Containerized Deployment

The application is fully containerized using **Docker** and **Docker Compose** to ensure consistent environments and simplified deployment.

### Docker Image

The machine learning application is packaged inside a Docker container including:

- FastAPI backend
- Streamlit frontend
- Machine learning model
- Python dependencies

This ensures the project runs identically across different systems.

### Docker Compose

Docker Compose is used to orchestrate multiple services in the system.

Services include:

- **Frontend (Streamlit)** – User interface for meal recommendations  
- **Backend (FastAPI)** – API that processes user inputs and runs the recommendation model  

The `docker-compose.yml` file allows the entire application to start with a single command.

```bash
docker-compose up --build

# Running the Project Locally

### Clone the Repository

```bash
git clone https://github.com/amitk2003/Ai-based-meal-recommendation-system

Run using Docker
docker-compose up -d --build
http://localhost:8501
https://diet-recommendation-system.streamlit.app/
'''
5. Example output
## Example Recommendation

Input:

Age: 25  
Weight: 70kg  
Height: 175cm  
Goal: Weight Loss  

Output:

Recommended Meals:

• Grilled Chicken Salad  
• Avocado Toast  
• Quinoa Vegetable Bowl  
• Greek Yogurt with Berries

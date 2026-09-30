# 🧠 Mansik Santulan Score

<p align="center">

  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange?style=for-the-badge&logo=scikit-learn" />
  <img src="https://img.shields.io/badge/Frontend-HTML%20%7C%20CSS%20%7C%20JavaScript-E34F26?style=for-the-badge&logo=html5" />

</p>

<p align="center">
  <b>An AI-powered mental wellness scoring application that analyzes lifestyle, academic, social-media, sleep, physical activity, and stress-related factors to generate a personalized mental-health score.</b>
</p>

---

## 🌱 About The Project

**Mansik Santulan Score** is a Machine Learning-powered application designed to analyze multiple lifestyle and behavioral factors that may be associated with a student's mental-health score.

The application collects information such as:

- 👤 Age and gender
- 🌍 Country
- 🎓 Academic level
- 📱 Most-used social media platform
- 🎯 Purpose of social media usage
- ⏱️ Average daily social media usage
- 🔓 Daily phone/social-media unlocks
- 📚 Study hours
- 🏃 Physical activity
- 😴 Sleep duration
- 🧠 Self-reported stress level

These inputs are processed by a trained Machine Learning model through a **FastAPI backend**, which returns a predicted mental-health score.

The result is displayed through a modern, interactive frontend.

---

# ✨ Key Features

### 🧠 Machine Learning Prediction

Uses a trained Machine Learning model to generate a predicted mental-health score from multiple lifestyle and behavioral features.

### 🌐 FastAPI Backend

A REST API handles:

- Input validation
- Data preparation
- Model inference
- Prediction response

### 🎨 Modern Frontend

The project includes a responsive frontend built using:

- HTML
- CSS
- JavaScript
- Interactive form components
- Animated score visualization
- Dynamic prediction states

### 📊 Mental Health Score

The application returns a numerical predicted mental-health score and presents it through an interactive visual gauge.

### ✅ Input Validation

The API uses **Pydantic** validation to restrict invalid values and maintain consistent input formats.

### ⚡ Real-Time Prediction

User inputs are sent from the frontend to the FastAPI backend and the prediction is displayed without reloading the page.

---

# 🏗️ System Architecture

```text
                  ┌─────────────────────────┐
                  │       User Input         │
                  │                         │
                  │ Age                     │
                  │ Gender                  │
                  │ Academic Level          │
                  │ Social Media Usage      │
                  │ Study Hours             │
                  │ Physical Activity       │
                  │ Sleep Hours             │
                  │ Stress Level            │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │       Frontend          │
                  │                         │
                  │ HTML + CSS + JavaScript │
                  └────────────┬────────────┘
                               │
                         POST /predict
                               │
                               ▼
                  ┌─────────────────────────┐
                  │       FastAPI           │
                  │        Backend          │
                  │                         │
                  │ Pydantic Validation     │
                  │ Data Preparation        │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Machine Learning      │
                  │         Model           │
                  │                         │
                  │ Mental_Health_Model.pkl │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │ Predicted Mental Health │
                  │        Score            │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │ Interactive Score Gauge │
                  │       & Result          │
                  └─────────────────────────┘

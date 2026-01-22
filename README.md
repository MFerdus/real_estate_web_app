
---

## 📂 Application Modules Overview

This project is a **multi-page Streamlit application** for real estate analytics that combines **price prediction**, **data visualization**, and **apartment recommendation** into a single interactive system.

---

## 🏠 1. Price Prediction Module

**File:** `1_Price Predictor.py` 

This module enables users to **estimate property prices** based on structural and location attributes.

### Key Functionality

* Loads a **pretrained machine learning pipeline** (`pipeline.pkl`) and cleaned dataset (`df.pkl`)
* Collects user inputs such as:

  * Property type (flat/house)
  * Sector (location)
  * Bedrooms, bathrooms, balconies
  * Built-up area
  * Furnishing type, luxury category, floor category
  * Servant room and store room availability
* Transforms inputs into a structured DataFrame compatible with the trained model
* Predicts property price using a **log-transformed regression pipeline**
* Displays a **price range estimate** (lower and upper bound) to account for market variability

### Outcome

Provides an intuitive, data-driven **price estimation tool** for residential properties.

---

## 📊 2. Analytics & Visualization Module

**File:** `2_Analysis App.py` 

This module focuses on **exploratory data analysis and visual insights** for the real estate dataset.

### Visualizations Included

* **Sector-wise price per square foot geo-map** using Plotly Mapbox
* **Word cloud** highlighting important real estate features
* **Area vs Price scatter plots** segmented by property type
* **BHK distribution pie charts** (overall and sector-wise)
* **Price distribution comparisons** between houses and flats
* **Box plots** showing BHK-wise price ranges

### Outcome

Helps users and analysts understand **market trends, spatial patterns, and pricing distributions** across sectors.

---

## 🏢 3. Apartment Recommendation Module

**File:** `3_Recommend Appartments.py` 

This module provides **location-based and similarity-based apartment recommendations**.

### Recommendation Logic

* Loads:

  * Location distance matrix (`location_distance.pkl`)
  * Multiple cosine similarity matrices (`cosine_sim1.pkl`, `cosine_sim2.pkl`, `cosine_sim3.pkl`)
* Combines similarity matrices using weighted averaging
* Uses **cosine similarity** to identify apartments similar to a selected property
* Supports:

  * Radius-based location search (distance filtering)
  * Top-N apartment recommendations with similarity scores

### Outcome

Delivers personalized apartment recommendations based on **geographic proximity and feature similarity**.

---

## 🧭 4. Application Entry Point

**File:** `Home.py` 

This file acts as the **main landing page** for the Streamlit application.

### Responsibilities

* Configures global app settings (title, icon)
* Provides a welcoming interface
* Enables sidebar navigation to different modules:

  * Price Predictor
  * Analytics Dashboard
  * Apartment Recommendation System

---

## 🔗 End-to-End System Flow

1. **Home Page** initializes the application and navigation
2. Users can:

   * Predict property prices
   * Explore market analytics
   * Receive apartment recommendations
3. Each module operates independently while sharing common datasets and design principles

---

## ✅ Key Highlights

* Modular Streamlit architecture
* Machine learning–based price prediction
* Interactive geospatial and statistical visualizations
* Hybrid recommendation system (distance + similarity)
* Production-ready structure suitable for deployment

---


# Loyalty-Tiers-Prediction-in-Hospitality
📌 Project Overview

This project focuses on building a Loyalty Tier Prediction System for the hospitality domain using booking behavior data.
The goal is to analyze customer stay patterns and predict their next loyalty tier (Copper, Silver, Gold, or Platinum) based on historical booking information.

The project follows a step-by-step data science workflow, starting from raw data exploration to machine learning–based prediction.

📂 Dataset Used
Source: https://www.kaggle.com/datasets/mojtaba142/hotel-booking

Initial Format: hotel_bookings.csv

Type: Structured tabular data

Key Information Includes:

Length of stay (week & weekend nights)

Average Daily Rate (ADR)

Previous cancellations

Booking and customer details

🔁 Project Workflow

1️⃣ Data Exploration & Cleaning

Loaded and inspected the raw dataset

Handled missing values (children, babies, agent, company, country)

Removed invalid records (zero guests, negative ADR)

Converted data types and processed date fields

Performed exploratory data analysis (EDA) using visualizations

Saved the cleaned dataset as:

hotel_bookings_cleaned.csv

2️⃣ Feature Engineering & Rule-Based Tier Assignment

Created a new feature TotalSpend using:

TotalSpend = (week nights + weekend nights) × ADR


Assigned a Current Loyalty Tier using business rules:

Copper

Silver

Gold

Platinum

Defined logical rules to generate a NextTier based on:

Spending behavior

Previous cancellations

Saved the updated dataset as:

hotel_bookings_with_tiers.csv

3️⃣ Machine Learning Model
Converted the problem into a multi-class classification task

Target Variable: NextTier

Features Used:

Week nights stay

Weekend nights stay

ADR

Previous cancellations

Current Tier

Encoded categorical data using Label Encoding

Trained a Random Forest Classifier

Evaluated model performance using accuracy and classification metrics

4️⃣ Model Persistence
Saved trained components for reuse:

tier_model.pkl → trained ML model

tier_encoder.pkl → label encoder

Enables instant predictions without retraining

5️⃣ Prediction Capability
Supports predictions even for new or unseen user inputs

Model generalizes patterns learned from historical data

Ready for future UI or API integration

🧠 Key Highlights
End-to-end machine learning pipeline

Combination of business logic + ML

Handles unseen inputs gracefully

Modular and production-ready structure

Clear separation between data processing, logic, and modeling

🛠️ Tech Stack
Language: Python

Libraries:
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Pickle

Environment: Google Colab

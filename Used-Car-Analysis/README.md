# Used Car Regression Analysis

## Overview
This repository contains the full analysis and modeling work for **Required Assignment 11.1: What Drives the Price of a Car?**  
The goal of this project is to identify the key factors influencing used‑car prices and build regression models to support dealership pricing decisions.

The project follows a structured CRISP‑DM workflow, including data preparation, exploratory data analysis, modeling, evaluation, and business recommendations.

---

## Notebook
**Main Notebook:**  
`Used_Car_Regression_Analysis.ipynb`

The notebook includes:
- Clean, well‑structured headings  
- Markdown explanations for each step  
- Visualizations and model diagnostics  
- Linear, Ridge, and Lasso regression models  
- Cross‑validation and hyperparameter tuning  
- Final model comparison  
- Business insights and recommendations  

---

## Summary of Findings

### What Increases Price
Models consistently identified the following as strong positive predictors:
- Luxury manufacturers (Porsche, Ferrari, Tesla, Lexus)
- Diesel fuel type
- Off‑road vehicle types
- Newer model years

These features reliably increase predicted price and represent high‑value inventory segments.

### What Decreases Price
The strongest negative predictors were:
- condition_salvage (largest negative impact)
- condition_fair
- High mileage (odometer)
- Older vehicles (vehicle_age)

Condition and mileage remain the most powerful downward pricing forces.

### Model Performance
All tuned models converged to nearly identical performance:

| Model                     | RMSE     | MAE      | R²       |
|---------------------------|----------|----------|----------|
| Linear Regression         | 0.5460   | 0.3460   | 0.6270   |
| Ridge Regression (Tuned)  | 0.5462   | 0.3459   | 0.6274   |
| Lasso Regression (Tuned)  | 0.5463   | 0.3459   | 0.6272   |

This indicates a strong linear structure in the dataset.

### Final Recommendation
Use **Linear Regression or Tuned Ridge Regression** as the final model.  
Both are accurate, interpretable, and stable, making them ideal for dealership pricing decisions.

---

## Repository Structure
Used-Car-Analysis/ 
│ 
├── Used_Car_Regression_Analysis.ipynb   # Main notebook 
├── README.md                            # Project summary and documentation 
└── data/ 
└── vehicles.csv.zip               # Compressed dataset (>50MB)


- The dataset is stored as a **zip file** due to GitHub’s file size limits.

---

## How to Run the Notebook

1. Clone the repository  
2. Extract `vehicles.csv.zip` inside the `data/` folder  
3. Open the notebook in Jupyter, Google Colab, or VS Code  
4. Install required Python libraries:  
pandas
numpy
seaborn
matplotlib
scikit-learn
5. Run all cells in order  

---

## Business Value

This project provides:
- A clear ranking of the most important pricing features  
- Visualizations for non‑technical stakeholders  
- Reliable regression models for pricing decisions  
- Actionable recommendations for inventory and reconditioning strategy  

The dealership can use these insights to improve pricing accuracy, reduce underpricing risk, and increase profitability.

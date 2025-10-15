# Operations Performance Analytics Project

This repository contains a **synthetic analytics project** designed to showcase skills relevant to roles such as **Business Analyst**, **Program Manager**, and **Data Analyst**.  
It includes a generated dataset, exploratory analysis with data visualizations, and predictive modelling using Python. The goal is to provide an out‑of‑the‑box project that demonstrates your ability to work with data from end to end — from generating/understanding data through to building models and interpreting results.

## Project Structure

```
├── data/
│   └── operations_performance_synthetic.csv
├── notebooks/
│   └── operations_performance_analysis.ipynb
├── README.md
└── requirements.txt
```

- **data/** – Contains the synthetic dataset (`operations_performance_synthetic.csv`).
- **notebooks/** – Jupyter notebook with exploratory data analysis (EDA), visualizations, and predictive models.
- **requirements.txt** – List of Python dependencies used in the project.

## Dataset

The dataset simulates daily operational performance metrics for various departments within a company. Each row represents aggregated metrics for a department on a specific date.

| Column | Description |
|------|-------------|
| `date` | Date of observation (daily). |
| `department` | Department name (Sales, Marketing, IT, HR, Finance, Operations, R&D). |
| `project_count` | Number of active projects. |
| `avg_project_duration` | Average duration of projects (days). |
| `budget_k` | Budget allocated (in thousand dollars). |
| `employee_count` | Number of employees in the department. |
| `actual_spend_k` | Actual spend (in thousand dollars). |
| `revenue_k` | Revenue generated (in thousand dollars). |
| `customer_satisfaction` | Customer satisfaction score (0–100). |
| `project_success_rate` | Percentage of projects delivered on time and within budget (0–100). |
| `risk_level` | Categorical risk level (`low`, `medium`, `high`) derived from spending patterns and project volume. |

The data is entirely synthetic, generated with realistic distributions and relationships between variables (e.g., higher project counts and overspend increase risk, revenue depends on budget and department). It is safe to publish publicly.

## Analysis Notebook

The Jupyter notebook performs:

1. **Exploratory Data Analysis (EDA)** – Summary statistics and visualizations such as histograms, scatter plots, and correlation heatmaps to understand distributions and relationships between variables.
2. **Predictive Modelling** –
   - **Regression**: A Random Forest Regressor predicts `project_success_rate` based on operational metrics and department information.
   - **Classification**: A Random Forest Classifier predicts the categorical `risk_level` based on the same features.

Evaluation metrics (Mean Squared Error, R², accuracy, classification report) are displayed to assess model performance.

## Getting Started

1. **Clone or download** this repository.
2. Create a Python environment (optional but recommended) using `venv` or `conda`.

   ```bash
   # using venv
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   venv\Scripts\activate    # Windows
   ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter Notebook**:

   ```bash
   jupyter notebook notebooks/operations_performance_analysis.ipynb
   ```

   Or use JupyterLab for an enhanced interface:

   ```bash
   jupyter lab
   ```

## Extending the Project

- **Add new features**: Introduce additional variables such as quality metrics, resource utilization, or external factors (economy, market trends).
- **Try other algorithms**: Experiment with different models (e.g., Gradient Boosting, XGBoost, Neural Networks) and compare performance.
- **Deploy as an app**: Build a simple dashboard using Streamlit or Dash to allow stakeholders to interact with data and predictions.
- **Incorporate time‑series forecasting**: Extend the analysis to forecast future performance using ARIMA, Prophet, or LSTM models.

## Purpose

This project demonstrates how to:

- Generate and document a synthetic dataset with business relevance.
- Perform data cleaning, visualization, and feature engineering.
- Build and evaluate machine learning models for both regression and classification tasks.
- Communicate insights clearly through visualizations and narrative in a notebook and README.

Use this repository as a **portfolio piece** or as a starting point for more complex analytics projects.

## Contributing

Contributions are welcome! If you encounter issues or have suggestions for improvements, please open an issue or submit a pull request. For pull requests, fork the repository, create a new branch for your changes, and ensure your code is well-documented and tested before proposing a merge.

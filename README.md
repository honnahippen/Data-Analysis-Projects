# Predictive Maintenance Analytics for Turbofan Engine Fleet

## Project Overview
This project uses NASA’s CMAPSS turbofan engine degradation dataset to build a predictive maintenance analytics solution for a simulated aircraft engine fleet. The objective was to forecast Remaining Useful Life (RUL) of engines using machine learning and transform model outputs into actionable maintenance insights through Power BI dashboards.
The project demonstrates an end-to-end analytics workflow including:
- Data cleaning and transformation
- Feature engineering
- Predictive modeling with XGBoost
- Model evaluation
- Fleet risk classification
- Business intelligence dashboarding

## Business Problem
Unexpected engine failures can create significant operational downtime, maintenance delays, and increased costs. Predictive maintenance helps organizations move from reactive repairs to proactive scheduling.
This project answers:
- Which engines are most likely to fail soon?
- How many cycles remain before maintenance is needed?
- Which assets should be prioritized first?
- What sensor signals are most associated with degradation?

## Dataset
Source: NASA CMAPSS Turbofan Engine Degradation Simulation Dataset

The dataset simulates a fleet of turbofan engines operating under varying conditions and records sensor measurements across lifecycle degradation until failure.
## Data Structure
unit_number = individual engine ID

cycles = operating cycle / mission count

operational settings = environmental / control variables

sensor values = engine telemetry data

RUL = Remaining Useful Life target variable

## Tools & Technologies
- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Power BI
- GitHub

## Methodology
1. Data Preparation
- Imported raw NASA text datasets
- Removed blank columns and formatting artifacts
- Applied column naming conventions
- Generated Remaining Useful Life (RUL) targets
- Combined original operational data with model outputs
2. Feature Engineering
Created additional variables including:
- Engine lifecycle progression
- Risk thresholds
3. Modeling
Used XGBoost Regressor to predict Remaining Useful Life.
4. Evaluation Metrics
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

## Model Results
Results on FD001 dataset:
- MAE: 31.44 cycles
- RMSE: 41.67 cycles
- R²: 0.501
These results demonstrate strong baseline predictive capability on simulated engine degradation data.

## Power BI Dashboard
The dashboard was built to convert technical model outputs into operational decisions.
## Dashboard Features
- Fleet health overview
- High-risk engines requiring maintenance
- Actual vs Predicted RUL comparison
- Sensor importance analysis
- Maintenance prioritization queue

## Key Insights
- Predictive analytics can identify engines at elevated failure risk before breakdown.
- Sensor telemetry provides measurable indicators of degradation trends.
- Maintenance teams can prioritize inspections based on predicted RUL instead of fixed schedules.
- Combining ML with BI tools creates executive-ready decision systems.

# TerraSight — UK Regional Insight Web App

**Live Demo:** https://terrasight-six.vercel.app  
**Project Report:** https://terrasight-six.vercel.app/TerraSight_Final_Year_Report.pdf

## Project Overview

TerraSight is a full-stack web application that forecasts five socioeconomic 
indicators across 9 English regions from 2025 to 2035. It uses machine learning 
models trained on UK government open data to generate predictions with confidence 
intervals and plain-English insights.

## Indicators Predicted

- Population Estimates (ONS)
- Employment Rate (ONS / NOMIS)
- Average House Price (HM Land Registry)
- Rental Price Index (ONS / VOA)
- Housing Completions (DLUHC)

## Regions Covered

East Midlands, East of England, London, North East, North West, 
South East, South West, West Midlands, Yorkshire and The Humber.

## Technology Stack

- Backend: Python, FastAPI, scikit-learn, pandas
- Frontend: React 19, TypeScript, Vite, Recharts, Tailwind CSS
- ML Models: Linear Regression, Random Forest, Gradient Boosting
- Deployment: Render (backend) + Vercel (frontend)

## Project Structure

- data_pipeline.py - Data cleaning and merging (435 lines)
- train.py - Model training and evaluation (354 lines)
- backend/ - FastAPI REST API (5 Python files, 13 endpoints)
- frontend/ - React dashboard (4 pages)
- data/processed/ - Cleaned dataset (master_dataset.csv)
- models/ - Trained model (model.pkl)

## Setup

### Backend

    cd backend
    python -m venv venv
    source venv/bin/activate
    pip install -r requirements.txt
    uvicorn main:app --reload

### Frontend

    cd frontend
    npm install
    npm run dev

For local frontend setup, create a .env file in frontend/ with:

    VITE_API_URL=http://localhost:8000

## Results

Linear Regression was the best performing model with 1.81% average MAPE 
on the test set (2020-2023), well below the 8% target.

## Author

Bera Aksoy  
BSc Computer Science, Nottingham Trent University  
2026

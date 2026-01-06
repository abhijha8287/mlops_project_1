# mlops_project_1

A comprehensive end-to-end **MLOps** project demonstrating machine learning pipeline development, containerization, CI/CD automation, and model serving via FastAPI.

## 📋 Project Overview

This is a learning project focused on implementing MLOps best practices including:
- **ML Pipeline**: Complete workflow from data ingestion to model training and evaluation
- **Model Serving**: FastAPI web application with interactive UI for predictions
- **Containerization**: Docker support for seamless deployment
- **CI/CD**: GitHub Actions workflows for automated testing and deployment
- **Configuration Management**: YAML-based configuration for reproducibility
- **Experiment Tracking**: Structure for tracking and logging experiments

##  Repository Structure

mlops_project_1/
├── .github/workflows/ # CI/CD pipeline workflows (GitHub Actions)
├── artifact/ # Generated artifacts (models, processed data, logs)
├── config/ # Configuration files (YAML/JSON)
├── notebook/ # Jupyter notebooks (EDA, experimentation)
├── src/ # Core Python package
│ ├── ingestion/ # Data ingestion components
│ ├── transformation/ # Data preprocessing and feature engineering
│ ├── training/ # Model training logic
│ ├── evaluation/ # Model evaluation metrics
│ └── prediction/ # Inference and prediction service
├── static/css/ # CSS styling for web UI
├── templates/ # Jinja2 HTML templates
├── app.py # FastAPI application entry point
├── demo.py # Pipeline demonstration script
├── dockerfile # Docker configuration
├── projectflow.txt # Project structure notes
├── requirements.txt # Python dependencies
├── pyproject.toml # Project metadata and configuration
├── setup.py # Package setup script
└── README.md # This file

##  Getting Started

### Prerequisites

- **Python 3.8+** (check `pyproject.toml` for specific version)
- **pip** or **conda** package manager
- **Docker** (optional, for containerized deployment)
- **Git** (for version control)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/abhijha8287/mlops_project_1.git
cd mlops_project_1
Create virtual environment (recommended)

bash
python -m venv venv

# Activate on Linux/Mac
source venv/bin/activate

# Activate on Windows
venv\Scripts\activate
Install dependencies

bash
pip install -r requirements.txt
 Usage
Run the ML Pipeline
Execute the complete ML pipeline including data ingestion, transformation, training, and evaluation:

bash
python demo.py
Outputs and artifacts will be saved to the artifact/ directory.

Run FastAPI Web Application
Start the FastAPI server for serving predictions:

bash
uvicorn app:app --reload
Access the application at: http://127.0.0.1:8000

Features:

Interactive web UI for model predictions

REST API endpoints for programmatic access

Styled interface using CSS from static/css/

HTML templates served via Jinja2

API Endpoints
GET / - Home page / UI

POST /predict - Get predictions from the model

(Additional endpoints as implemented in app.py)

 Docker Deployment
Build Docker Image
bash
docker build -t mlops_project_1:latest .
Run Container
bash
docker run -p 8000:8000 mlops_project_1:latest
The application will be available at: http://localhost:8000

Configuration
Configuration files are located in the config/ directory. Modify these to:

Set data paths and file locations

Adjust model hyperparameters

Configure pipeline parameters

Set logging levels and artifact storage paths

Example configuration structure:

text
data:
  path: "data/"
  train_split: 0.8

model:
  type: "linear_regression"
  hyperparameters:
    learning_rate: 0.01
    epochs: 100
MLOps Concepts Covered
✅ Modular Architecture: Clean separation of concerns with src/ package

✅ Configuration as Code: YAML/JSON based configurations for reproducibility

✅ Experiment Tracking: Artifact storage and logging infrastructure

✅ CI/CD Pipeline: Automated workflows in .github/workflows/

✅ Containerization: Docker support for production deployments

✅ Model Serving: FastAPI for REST API and web interface

✅ Data Pipeline: Structured ingestion, transformation, and validation

✅ Version Control: Git-based development workflow

🧪 Project Workflow
Data Ingestion - Load and validate raw data

Data Transformation - Clean, preprocess, and engineer features

Model Training - Train ML model with configured hyperparameters

Model Evaluation - Evaluate performance on test set

Model Serving - Deploy via FastAPI web application

Monitoring - Track metrics and artifacts in artifact/

Notebooks
Exploratory analysis and experimentation notebooks are available in the notebook/ directory:

Data exploration and visualization

Feature engineering experiments

Model prototyping and tuning

CI/CD Workflows
GitHub Actions workflows in .github/workflows/ automate:

Testing and validation

Model training and evaluation

Docker image building

Deployment to production

Dependencies
All project dependencies are listed in requirements.txt. Key packages include:

FastAPI - Web framework for API and UI

Pandas - Data manipulation and analysis

Scikit-learn - Machine learning algorithms

Uvicorn - ASGI server for FastAPI

Jupyter - Interactive notebooks

Install all dependencies:

bash
pip install -r requirements.txt
🎓 Learning Resources
This project covers:

MLOps fundamentals and best practices

Python package structure and setup

REST API development with FastAPI

Docker containerization

GitHub Actions CI/CD

Configuration management

Model deployment and serving

Troubleshooting
Port 8000 already in use?

bash
uvicorn app:app --reload --port 8001
Dependencies installation issues?

bash
pip install --upgrade pip
pip install -r requirements.txt --force-reinstall
Docker build fails?

bash
docker build --no-cache -t mlops_project_1:latest .
License
This project is licensed under the MIT License - see the LICENSE file for details.

Last Updated: January 2026

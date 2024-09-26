# Chest Cancer Classification using CNN

This project is focused on building a **Convolutional Neural Network (CNN)** to classify chest cancer images. It uses a modular and scalable approach with tools for experiment tracking, data versioning, and model deployment.

## Project Overview

The goal of this project is to develop a deep learning model capable of detecting chest cancer from images. The model architecture is built using TensorFlow, and a Flask web interface is provided for easy interaction with the model.

### Tech Stack

- TensorFlow 2.12.0: For building and training the CNN model.
- Pandas and NumPy: For data manipulation and preprocessing.
- DVC: For data version control and model tracking.
- MLflow: To track experiments and manage models.
- Flask & Flask-Cors: For deploying a web-based inference interface.
- Matplotlib and Seaborn: For visualizations.
- Scipy: For scientific computing.

### Folder Structure

``` bash
cnnClassifier/
├── src/                      # Source code folder
│   ├── cnnClassifier/        # Main package for CNN and other components
├── config/                   # Configuration and parameter files
├── research/                 # Jupyter Notebooks for experimentation
├── templates/                # HTML templates for web interface
├── requirements.txt          # Project dependencies
├── setup.py                  # Package setup script
```

### Installation
1. Clone the repository:
``` bash
git clone https://github.com/harsha0603/chest-cancer-classification.git
cd chest-cancer-classification
```
2. Create a virtual environment and install dependencies:
``` bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
pip install -r requirements.txt
```


``` bash
import dagshub
dagshub.init(repo_owner='harsha0603', repo_name='chest-cancer-classification', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)
``` 
```
aef88c752cc97330feef4eb05e7e608bc939cecf
```
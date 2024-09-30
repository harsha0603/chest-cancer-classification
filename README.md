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

## DVC Commands

``` bash 
dvc init
```
```bash
dvc repro
```

## User interface 
![image](https://github.com/user-attachments/assets/57f13415-9ac0-4407-8bfc-ef6596b8b397)



![image](https://github.com/user-attachments/assets/0f924305-ea54-427c-af66-e7a5669f2dcb)






# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

## 3. Create ECR repo to store/save docker image
    - Save the URI: Your ECR URI


## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = ENTER YOUR URI

    ECR_REPOSITORY_NAME = 

    
    
## Here you can see CICD status
![image](https://github.com/user-attachments/assets/7a81fa0b-6e74-4dec-97e9-abbd2ec26beb)

![image](https://github.com/user-attachments/assets/686bf3d2-373a-4c13-ad4c-23a99db91300)



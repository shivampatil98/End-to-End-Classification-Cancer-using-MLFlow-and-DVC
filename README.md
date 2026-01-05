# Project Overview

This project focuses on building a robust, end-to-end cancer classification system using Convolutional Neural Networks (CNNs). The pipeline leverages MLFlow for experiment tracking, DVC for data versioning, and utilizes Docker and AWS for containerization and cloud deployment, ensuring scalability and efficient model management.

## Project Structure

End-to-End-Classification-Cancer-using-MLFlow-and-DVC/
│
├── app.py                # Main application file to serve predictions
├── main.py               # The main script for pipeline execution and model training
├── Dockerfile            # For containerizing the app
├── dvc.yaml              # DVC pipeline configuration file
├── params.yaml           # Hyperparameters and settings
├── requirements.txt      # List of Python dependencies
├── src/
│   └── cnnClassifier/    # CNN model definition and training logic
│       ├── model.py      # Defines the CNN architecture
│       ├── train.py      # Script to train the model
│       └── utils.py      # Utility functions for training
├── scores.json           # JSON file to store evaluation metrics
└── README.md             # Project documentation


## How to run

1. Clone this repository to your local machine:

```bash
- git clone https://github.com/shivampatil98/End-to-End-Classification-Cancer-using-MLFlow-and-DVC.git
- cd End-to-End-Classification-Cancer-using-MLFlow-and-DVC
```

2. Install Python dependencies:

```bash
pip install -r requirements.txt
```

3. Set up MLFlow

```bash
pip install mlflow
```

4. Train the Model

```bash
python main.py --train
```

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=[https://dagshub.com/shivampatil98/End-to-End-Classification-Cancer-using-MLFlow-and-DVC.mlflow]
MLFLOW_TRACKING_USERNAME=shivampatil98 \
MLFLOW_TRACKING_PASSWORD=2f958127c828fc1267dfbe2ea45a0d187469ae56  \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=[https://dagshub.com/shivampatil98/End-to-End-Classification-Cancer-using-MLFlow-and-DVC.mlflow]

export MLFLOW_TRACKING_USERNAME=shivampatil98 

export MLFLOW_TRACKING_PASSWORD=2f958127c828fc1267dfbe2ea45a0d187469ae56  

```
5. Run the Application

```bash
python app.py
```

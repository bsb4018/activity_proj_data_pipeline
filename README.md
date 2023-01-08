# Activity Prediction - Data Collection Pipeline

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)<space><space>![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka)<space><space>![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)


This repository imitates the data collection for Human Activity 
Prediction like SITTING, STANDING, WALKING, RUNNING etc. The data 
consists of sensors data from embedded accelerometer and gyroscope
in a smartphone, capturing 3-axial linear acceleration and 3-axial 
angular velocity at a constant rate of 50Hz. A vector of features 
is obtained by calculating variables from the time and frequency 
domain.
Each record in the dataset consists of -
• Triaxial acceleration from the accelerometer 
  (total acceleration) and the estimated body acceleration.
• Triaxial Angular velocity from the gyroscope.
• A 561-feature vector with time and frequency domain variables.
• An identifier of the subject who carried out the experiment
• Its activity label.


The data is streaming data hence a streaming platform Apache Kafka 
is used to collect data in a streaming fashion and store it inside 
collections defined in MongoDB. This whole process is written 
using Python.


# confluent-kafka-python


This repo help us to know how to publish and consume data to and from kafka confluent in json format.

Step 1: Create a conda environment
```
conda --version
```

Step2: Create  a conda environment
```
conda create -p venv python==3.8 -y
```

Step3:
```
conda activate venv/
```
Step4:
```
pip install -r requirements.txt
```


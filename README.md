# Activity Prediction - Data Collection Pipeline

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)<space><space>![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka)<space><space>![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)


This repository imitates the data collection for Human Activity 
Prediction like SITTING, STANDING, WALKING, RUNNING etc. The data 
consists of sensors data from embedded accelerometer and gyroscope
in a smartphone, capturing 3-axial linear acceleration and 3-axial 
angular velocity at a constant rate of 50Hz.<br>

A vector of features  is obtained by calculating variables from 
the time and frequency domain. <br>
Each record in the dataset consists of - <br>
• Triaxial acceleration from the accelerometer 
  (total acceleration) and the estimated body acceleration.<br>
• Triaxial Angular velocity from the gyroscope.<br>
• A 561-feature vector with time and frequency domain variables.<br>
• An identifier of the subject who carried out the experiment.<br>
• Its activity label.<br>


The data is streaming data hence a streaming platform Apache Kafka 
is used to collect data in a streaming fashion in json format and 
store it inside collections defined in MongoDB. This whole process 
is written using Python.<br>

![Data Pipeline Diagram](https://github.com/bsb4018/activity_proj_data_pipeline/blob/main/screenshots/data_pipeline_diagram.png)

<br>

## Pre Requisites

The main pre-requisites for this project are - <br>
Confluence Kafka Account With a Setup Cluster and Schema<br>
MongoDB Cloud Atlas Database and Collection<br>
Python v3.8.13 <br>

## Environment Variables

To run this project, you will need to add the 
following environment variables to your system <br>

`SECURITY_PROTOCOL` = Denotes the default security Protocol ("SASL_SSL") <br>
`SSL_MACHENISM`= Denotes the SSL Mechanism to use ("PLAIN") <br>
`API_KEY` = Confluence Kafka Cluster Api Key <br>
`API_SECRET_KEY` = Confluence Kafka Cluster Api Secret Key <br>
`BOOTSTRAP_SERVER` = Confluence Kafka Cluster Bootstrap Server Url <br>
`ENDPOINT_SCHEMA_URL`  = Confluence Kafka Cluster Schema Endpoint <br>
`SCHEMA_REGISTRY_API_KEY` = Confluence Kafka Cluster Schema Registry Api Key <br>
`SCHEMA_REGISTRY_API_SECRET` = Confluence Kafka Cluster Schema Registry Api Secret Key <br>
`MONGO_DB_URL` =  Mongo DB Atlast Database Url <br>




## Run 

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
Step5:
```
python consumer.py
```
Step6:
```
python producer.py
```

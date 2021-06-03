# Azure-ML-Engineer-Udacity-2

This is the repository for the Second Project for the Udacity Azure ML Engineer Nanodegree.

# Overview 

This project contains following steps: 

- Creating a automated ML Experiment
- Deploying the best model
- Enable logging
- Creating Swagger Documentation 
- Consume Model Endpoint
- Create, Publish and Consume a Pipeline
- Documentation including a screencast

Note: As it was not possible to create a Service principal in the Udacity lab environment, this step was skipped

## Auto ML Experiment
In this step a Auto ML Model is created using the same bankmarket dataset from course 1. 
This dataset gives us the opportunity to create a model to make a binary classification.

For compute resource a Standard_DS12_v2 is used. 

![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2_RegisteredDatasets.PNG)
## Deploy the best Model
The Auto ML Run resulted into a best model, which used the voting ensemble algorithm. (0.91520 presicion)
This model got deployed using a Azure Container instance.

## Enable logging
Logging got enabled using the Python sdk inside the logs.py script located inside the /starter_files folder

## Swagger documentation
Swagger documentation was downloaded via a json file and the swagger documentation website was locally deployed using both scripts in the starter_files/swagger/ folder

## Consume Model Endpoint
The endpoint got consumed using the endpoint.py script, which is located in the starter_files folder

## Create, Publish and Consume a Pipeline
Using the python SDK to create a ML Pipeline

## Documentation
link for the screencast
https://youtu.be/9LoBYsp6kfs


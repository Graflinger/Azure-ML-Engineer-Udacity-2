# Azure-ML-Engineer-Udacity-2

This is the repository for the Second Project for the Udacity Azure ML Engineer Nanodegree.

# Overview 

This project contains following steps: 

- Architecture
- Creating a automated ML Experiment
- Deploying the best model
- Enable logging
- Creating Swagger Documentation 
- Consume Model Endpoint
- Create, Publish and Consume a Pipeline
- Documentation including a screencast

Note: As it was not possible to create a Service principal in the Udacity lab environment, this step was skipped


## Architecture
![Architecture](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/4ba78b432cc405043f40bd557c27fc770c7151ee/Screenshots/Diagram%202021-06-03%2021-24-09.png)

## Auto ML Experiment
In this step a Auto ML Model is created using the same bankmarket dataset from course 1. 
This dataset gives us the opportunity to create a model to make a binary classification.

For compute resource a Standard_DS12_v2 is used. 

Here ist the used dataset registered.
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2_RegisteredDatasets.PNG)

Here is the completed experiment
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2experimentcompleted.PNG)

Best Model
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2bestmodel.PNG)

## Deploy the best Model
The Auto ML Run resulted into a best model, which used the voting ensemble algorithm. (0.91520 presicion)
This model got deployed using a Azure Container instance.

## Enable logging
Logging got enabled using the Python sdk inside the logs.py script located inside the /starter_files folder

Enabled logging
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/ApplicationInsightTrue.PNG)

logs provided by log.py
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/logs.PNG)

## Swagger documentation
Swagger documentation was downloaded via a json file and the swagger documentation website was locally deployed using both scripts in the starter_files/swagger/ folder

Swagger API
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/swagger.PNG)

Swagger payload Content
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/swaggerContents.PNG)

## Consume Model Endpoint
The endpoint got consumed using the endpoint.py script, which is located in the starter_files folder

Output running against the API using the endpoint.py
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/endpointResult.PNG)

## Create, Publish and Consume a Pipeline
Using the python SDK to create a ML Pipeline

Created Pipeline
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/pipelineCreated.PNG)


Pipeline Endpoint
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/pipelinerest.PNG)

Pipeline Detail
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/BankmarketingwithautomlRun.PNG)

Run Details
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/pipelinerundetail.PNG)

## Documentation
link for the screencast
https://youtu.be/9LoBYsp6kfs


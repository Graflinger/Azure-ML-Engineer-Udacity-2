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
- Further Improvements for the future
- Documentation including a screencast


Note: As it was not possible to create a Service principal in the Udacity lab environment, this step was skipped


## Architecture
Here you can see how the project is implemented step by step. First the dataset got registered, then a compute cluster got created to run auto ml classification. Afterwards the best model is deployed using a Azure Container Instance, which got logging enabled. Finally the endpoint provides a REST API so you can use the deployed model for a prediction.

![Architecture](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/4ba78b432cc405043f40bd557c27fc770c7151ee/Screenshots/Diagram%202021-06-03%2021-24-09.png)

## Auto ML Experiment
In this step a Auto ML Model is created using the same bankmarket dataset from course 1. 
This dataset gives us the opportunity to create a model to make a binary classification.

For compute resource a Standard_DS12_v2 is used. 

After completion of the experiment, you can clearly see a list of all models tried and the best one at the top.

Here ist the used dataset registered.
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2_RegisteredDatasets.PNG)

Here is the completed experiment
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2experimentcompleted.PNG)

List of Models
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/2bestmodel.PNG)

## Deploy the best Model
The Auto ML Run resulted into a best model, which used the voting ensemble algorithm. (0.91520 presicion)
This model got deployed using a Azure Container instance.

## Enable logging
As you cann see in the "Enabled logging", logging is enabled, so you can use the log.py script to view these logs, as shown under "logs provides by log.py"

Enabled logging
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/c5b13c398b7acaf8ee57a5c596fe9c7d5ccdcbac/Screenshots/ApplicationInsightTrue.PNG)

logs provided by log.py
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/logs.PNG)

## Swagger documentation
Swagger documentation was downloaded via a json file and the swagger documentation website was locally deployed using both scripts in the starter_files/swagger/ folder.
This resulted in a overview of the api, as shown in "Swagger API" picture. The detailed payload content is visible under "Swagger payload content"

Swagger API
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/swagger.PNG)

Swagger payload Content
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/swaggerContents.PNG)

## Consume Model Endpoint
The endpoint got consumed using the endpoint.py script, which is located in the starter_files folder. This consumption results in a return message, which can be seen in the next screenshot.

Output running against the API using the endpoint.py
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/endpointResult.PNG)

## Create, Publish and Consume a Pipeline
Using the python SDK to create a ML Pipeline. First the pipelines gets created "Created Pipeline" and is completed shown at "Completed Pipelines". Afterwards it got published and is therefore shown as active in "Active published pipeline". The created Endpoint can be seen at "Pipeline Endpoint" and further pipeline and run details are includes at the "Pipeline Detail" and "Run Details" screenshots 

Created Pipeline
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/pipelineCreated.PNG)

Compelted Pipelines
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/8495c285f7f144024848ba28c704683aa6fd04df/Screenshots/pipelineoverview.PNG)

Active published pipeline
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/8495c285f7f144024848ba28c704683aa6fd04df/Screenshots/Actibe.PNG)

Pipeline Endpoint
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/pipelinerest.PNG)

Pipeline Detail
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/BankmarketingwithautomlRun.PNG)

Run Details
![Registered Datasets](https://github.com/Graflinger/Azure-ML-Engineer-Udacity-2/blob/d2b21350ca3d342efddf8bf79b42dcbb2bd6ccf0/Screenshots/pipelinerundetail.PNG)

## Further improvements for the future

1. The Banking dataset could get more prepared for better results (e.g. feature engineering, if imbalanced classes balancing them, gathering more data...)
2. The training time and performance of the underlying compute cluster of the auto ml function could be increased to get better results
3. Furthermore deep learning could get activated (if GPU is activated on the cluster) to achieve possibly even better results 

## Documentation
link for the screencast
https://youtu.be/dELenE_Si3U


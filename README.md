# End-to-end-Machine-Learning-Project-with-MLflow

1. **CI/CD Implementation using AWS Github Action**
![CICD Implementation using AWS Github Action](/images/CICD%20Implementation.png)

2. **User Interactive App deployed in AWS ECR**
![User Interactive app](/images/UserEndpoint%20using%20Flask.png)


## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

```
import dagshub
dagshub.init(repo_owner='ashleshuk', repo_name='End-to-end-Machine-Learning-Project-with-MLflow', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)
```

Run this to export as env variables:

```bash
export MLFLOW_TRACKING_URI=https://dagshub.com/ashleshuk/End-to-end-Machine-Learning-Project-with-MLflow.mlflow
export MLFLOW_TRACKING_USERNAME=ashleshuk 
export MLFLOW_TRACKING_PASSWORD=a86163024f0fc3112229ff0f628c80dbde7d2452

```


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
    - Save the URI: 394423337255.dkr.ecr.us-east-1.amazonaws.com/mlproj

	
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
	
## 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


## 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app




## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model



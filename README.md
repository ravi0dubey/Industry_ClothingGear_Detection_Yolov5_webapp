# Industry Clothing Gear Detection

## How to Run

1. conda create -n clothgear python=3.8 -y
2. conda activate clothgear
3. pip install -r requirements.txt
4. python ClientApp.py
5. open in browser: http://localhost:8080/



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
    - Save the URI: 066474313952.dkr.ecr.us-east-1.amazonaws.com/dogcat

	
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

    AWS_ECR_LOGIN_URI = 066474313952.dkr.ecr.us-east-1.amazonaws.com

    ECR_REPOSITORY_NAME = dogcat
    
    
#### CI-CD Pipeline
##### ECR Image
![image](https://user-images.githubusercontent.com/38419795/229327985-a5e4690e-d134-4285-b62c-e13d8ee0747e.png)


![image](https://user-images.githubusercontent.com/38419795/229327478-759ff3e3-fea5-4ada-ac4e-c7a51692ee45.png)

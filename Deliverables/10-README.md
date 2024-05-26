# README.md file
in your solution that serves as documentation for your user to detail how your deployment process works and how the user can deploy changes. 
The details should not simply rehash what you have done on a step-by-step basis. Instead, 
it should help an experienced software developer understand the technologies and tools in the build and deploy process as well as provide them insight into how they would release new builds.

## Getting Started

### Setup
#### 1. Create a Docker File
create a docker file that contain a step by step build process for the python app.
test the docker file by building it to ensure the image is produced successfully. 

#### 2. Create Buildspec.yaml
create an ecr private repo
create a codebuild project with a compatable linux image as the cluster
create a postbuild, build , prebuild stages to run on codebuild to login to ECR, build the docker file , tag it and push it to the ECR repository 

#### 3. Create an EKS cluster 
Creating an EKS cluster with the needed number of nodes inside a nodegroup , then update the kubeconfig file with your newly created cludter 

#### 4. Create the Database and fill it with data 
Create a pv.yaml , pvc.yaml , deployment and service configuration files to establish the database pods 
portforward to the pod and run the seeds files that will populate the database with the data 

#### 5. Create Deployment files to deploy the python app
Create a configmap , secrets , deployment , service yaml file to deploy the python app to the cluster 
Run a curl that will call the api after it has been deployed successfully

#### 6. Connect to cloud watch and see the logs live
Create an attach role policy to add the cloud watch policy to the cluster nodegroup iam role 
Create addon to see the logs happening 




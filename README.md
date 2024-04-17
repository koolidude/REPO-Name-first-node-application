# REPO-Name-first-node-application

step-by-step how to create an image until it will be deployed to AWS ECR

create repository in AWS ECR

Use the following steps to authenticate and push an image to your repository. For additional registry authentication methods, including the Amazon ECR credential helper, see Registry Authentication .
Retrieve an authentication token and authenticate your Docker client to your registry.
Use the AWS CLI:

aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 255945442255.dkr.ecr.us-east-1.amazonaws.com
Note: If you receive an error using the AWS CLI, make sure that you have the latest version of the AWS CLI and Docker installed.
Build your Docker image using the following command. For information on building a Docker file from scratch see the instructions here . You can skip this step if your image is already built:

docker build -t node-docker-norshukri-170424 .
After the build completes, tag your image so you can push the image to this repository:

docker tag node-docker-norshukri-170424:latest 255945442255.dkr.ecr.us-east-1.amazonaws.com/node-docker-norshukri-170424:latest
Run the following command to push this image to your newly created AWS repository:

docker push 255945442255.dkr.ecr.us-east-1.amazonaws.com/node-docker-norshukri-170424:latest


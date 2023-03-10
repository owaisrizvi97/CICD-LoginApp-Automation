# CICD-LoginApp-Automation
CI/CD pipeline for static login app using github (as SCM), Jenkins, Docker, Ansible and Kubernetes on AWS cloud.

![Screenshot 2023-01-17 182430](https://user-images.githubusercontent.com/68285890/212910850-c7522deb-7ad1-4e61-9d33-d422dc36a27d.png)


In this project, I am going to automate the deployment of simple static web application on Git. In the first part, I have deployed the application on tom-cat server by manually using the Jenkins build and deploy tool. Next, to expand the project and creating the CI/CD pipeline, we use maven build tool to create artifacts upon successfull unit testing including the syntax checks and configuration tests. Finally, those artifacts have been deployed on docker host on AWS to create the docker image and push that image to dockerhub for continuous integration process. Now, I have the option to create the docker container on singel VM or creating multiple VMs using cluster and container management tool. I tried both to check the performance, reliability and security. 

The EKS service and Ansible is used as the part of Continuous Deployment process to automate the pipeline whenever there is a change in code on git. This allows jenkins to trigger the job based on Poll SCM, build it through Maven and deploy on the Kubernetes cluster with min POD 2, max POD 3 over AP-south-region-1. 

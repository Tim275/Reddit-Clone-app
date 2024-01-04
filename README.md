## Overview


This project aims to deploy a Reddit clone application in a cloud-native environment while incorporating monitoring and logging functionalities. The implementation will leverage the following tools:

1. Terraform: An Infrastructure as Code (IAC) tool for automating the deployment of the application’s infrastructure on AWS. 

2. AWS: A cloud platform providing essential services and resources for hosting the application.

3. EKS (Elastic Kubernetes Service): A managed Kubernetes service on AWS designed for container orchestration, established using the IAC tool Terraform.

4. Jenkins: A Continuous Integration/Continuous Deployment (CI/CD) tool automating the build, test, and deployment processes.

5. SonarQube: A static code analysis tool ensuring code quality and identifying potential issues.

6. Trivy: A container image vulnerability scanner used to detect and mitigate security risks in the application’s containers.

7. OWASP: The Open Web Application Security Project, offering a set of best practices for web application security.

8. ArgoCD: A Continuous Deployment tool managing and automating deployments to the EKS cluster.

9. Prometheus: A monitoring and alerting system collecting metrics and generating alerts based on predefined rules.

10. Grafana: A visualization and dashboard tool displaying monitoring data in a user-friendly manner.

11. Kibana: A distributed search and analytics engine for storing and indexing logs.

# Documentation
 ## First Pipeline Check after pool adjustment with Jenkins
![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/2abb2d95-1e75-4706-bdb1-856155c3635b)

## SonarQube

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/27efec43-743b-4ba0-be9c-be652d3439f3)

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/4d5453a0-cdf2-4fa8-990d-4a7d171733f6)

## Dependency check with QWASP
![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/807e9dbb-627a-4724-ae27-1f612fc03238)

## docker image included into the Pipeline
![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/93718570-1dc9-4f21-820c-f506eca6b1a8)


## Argo CD

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/bf6fc73c-9593-4c7f-bee6-a3ff84b37b3e)

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/327dbefe-6510-4b48-986a-73c19b67d72f)


# Application deployment
![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/9720bbfa-9370-4936-b3fa-e190dbd2cb36)






## Monitoring Pods and Clusters
![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/e4ce0c66-7e24-4567-ac2a-002b98fb2615)

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/5662bc18-46f0-4fe4-9eb8-06b4a1a65a74)

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/1f10b94a-fc64-403f-8a62-fdd8d7dcb796)

## Kibana logs

![image](https://github.com/Tim275/Reddit-Clone-app/assets/117520669/4bf1017a-58c9-4144-98f1-dca8fd5fdc5f)

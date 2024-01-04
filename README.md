## Overview

Overview:

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

11. Elasticsearch: A distributed search and analytics engine for storing and indexing logs.



# Summer Internship Project: SECOPS 360

## About the Project
Automation of deployments for an application called **Minitrello**, developed with **NodeJS**, **React**, and **MongoDB**.

## Project Framework
- Dockerization of the Minitrello application with **Docker** and **Docker compose**
- **Automation of deployment with **Jenkins**
- **Management of requests and traffic with **Nginx Proxy Manager**
- **Adoption of Infrastructure as Code (IaC) with **terrafrom**
- **Establishment of an IT automation platform with **Ansible**
- **Deployment of the application on **an Azure virtual machine**
- Use of **Agile Scrum** methodology for project management**
-- Use **Git** and a platform like**GitLab** to manage  source code.

## Project Architecture

![Project Architecture](architecture.png) <!-- Replace with the link to your architecture image -->

## CI/CD Pipeline
Our pipeline includes both a CI (Continuous Integration) part and a CD (Continuous Deployment) part.

![CI/CD Pipeline](CICD-pipeline-frontendbackend.png)

## Preparation for the Adoption of Infrastructure as Code (IaC) with Terraform

After setting up the Terraform environment, we can run the **`terraform apply`** command to deploy the infrastructure. After executing this command, we find the following results:

![terraform apply ](terraform-apply.png)
## configuration our vm with ansible 
![Ansible Execution  ](Ansible-Execution-Screenshot.jpg)

After preparing the infrastructure and configuring the server, and executing our frontend and backend pipeline located in Jenkins, we find:
## Deployed application is accessible via public IP address.
![Application deployed ](Application.png)



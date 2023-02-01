Lab 08 - Deploy Azure Container instance
# Student lab manual

## Lab scenario

Contoso is looking for a new platform to host its virtualized workloads. You identified a number of container images that can be used to achieve this goal. Because you want to reduce container management, you intend to investigate the use of Azure Container Instances for Docker image deployment. You have been tasked with following functionalities

- Creating an Azure Container instance. Azure Container Instances is a Microsoft Azure public cloud service that allows developers to deploy containers without having to provision or manage any underlying infrastructure. The service, which supports both Linux and Windows containers, eliminates the need for a developer to provision virtual machines or implement a container orchestration platform like Kubernetes in order to deploy and run containers. Instead, with Azure Container Instances (ACI), an organization can spin up a new container through the Azure portal or command-line interface (CLI), and Microsoft will provision and scale the underlying compute resources automatically. ACI also supports standard Docker images that a developer can get from a container registry like Docker Hub or Azure Container Registry.

- Reviewing the functionalities of Azure container instance. After deploying the container, start by viewing its logs with az container logs, and stream its standard out and standard error with az container attach. You can also view logs and events for container instances in the Azure portal, or send log and event data for container groups to Azure Monitor logs.

## Objectives

In this lab, you will have:

+ Exercise 1: Create an Azure Container instance and reviewing it. 


## Estimated timing: 60 minutes
## Solution Architecture


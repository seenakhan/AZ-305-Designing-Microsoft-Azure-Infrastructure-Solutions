---
Lab:
    Title: '01 - Design a Governance Solution'
    Module: 'Microsoft Azure Architect Design Prerequisites'
---

# Lab 01 - Design a Governance Solution
# Student lab manual
## Lab scenario

In order to improve management of Azure resources in Contoso, you have been tasked with implementing the following functionality:

- Management Groups in Azure to manage access, policy, and compliance across multiple subscriptions.

- Assign subscriptions to the management groups to separate billing environments, such as development, test, and production.

- Assign Policies to enforce different rules over your resource configurations so the configurations stay compliant with corporate standards.
- Cost Analysis - Microsoft Cost Management is a suite of tools that help organizations monitor, allocate, and optimize the cost of their Microsoft Cloud workloads. 

## Objectives

In this lab, we will:

+ Task 1: Create Management Groups
+ Task 2: Create Child Management Groups
+ Task 3: Assign Subscriptions to management groups
+ Task 4: Assign Policies and Governance to management groups
+ Task 5: Review the cost data and explore the cost manager

## Estimated timing: 30 minutes
## Architecture diagram

![image](media/manarch.png)

## Instructions

### Exercise 1

#### Task 1: Create Management Groups

#### Pre-requisites for this task
If you don't have an Azure subscription, create a free account before you begin by clicking [here](https://azure.microsoft.com/en-us/free/).

Any Azure AD user in the tenant can create a management group without the management group write permission assigned to that user if hierarchy protection isn't enabled. This new management group becomes a child of the Root Management Group or the default management group and the creator is given an "Owner" role assignment. Management group service allows this ability so that role assignments aren't needed at the root level. No users have access to the Root Management Group when it's created. To avoid the hurdle of finding the Azure AD Global Admins to start using management groups, we allow the creation of the initial management groups at the root level.

#### Steps:

1. Log into the Azure portal.

2. Select All services > Management + governance.

3. Select Management Groups.

4. Select + Add management group.


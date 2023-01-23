# Instructions

## Exercise 1: Add a user and provide the accessibility of the resources.

Each Azure server (which hosts SQL Database or Azure Synapse) starts with a single server administrator account that serves as the server's administrator. As an Azure AD account, create a second administrator account. This principal is created as a contained database user in the server's master database. Administrator accounts are members of the db owner role in all user databases and log in as the dbo user. If a server does not have an Azure Active Directory administrator, then Azure Active Directory logins and users receive a Cannot connect to server error.

In this Exercise, you will grant Azure AD admin role to access your SQL server.

### Task 1: Set the current user as Admin and Query the data by using Azure Active Directory Authentication

In this task you are going to grant permission to SQL server created on previous exercise through Azure Active Directory.

#### Pre-requisites for this task

Complete Exercise 1 & Exercise 2.

#### Steps:

# Instructions

## Exercise 2: Deploy a multi-container group using a YAML file

In this exercise, you are going to deploy a multi container group by using YAML file and review the functionalities of it.

In this Exercise, you will have:

  + Task 1: Create a Storage account.
  + Task 2: Review the functionality of the Azure Container Instance.

### Task 1: Create a Storage account

In this task, you will create a new storage account.

#### Pre-requisites for this task



#### Steps:

1. Go to Azure portal, from the top please select **Cloud shell**. Then select **Bash**

![img](../media/yml3.png)

2. Please select **Show advanced settings**.

![img](../media/yml4a.png)



3. On the **Create a Storage account** page please enter the following details and select **Review**.
    
    | Setting | Action |
    | -- | -- |
    | **Subscription** drop-down list | Retain the default value |
    | **Resource group** section | PLease click on **Use existing** then Select **ODL-AZ-305M05C - XXXXX** |
    | **Storage account name** text box | Enter **contosostor** |
    | **Region** drop-down list | Select **(US) East US** |
    | **File share** section | Enter **contosofile1** option |
    
    The following screenshot displays the configured settings in the **Create a storage account** blade.

![img](../media/yml5.png)
 
4. Please wait for sometime and let the **Bash** terminal open.

5. Please enter the command **code deploy-aci.yaml** to create an empty YAML file to write the scripts.

6. You can see an empty YAML file created in the name of **deploy-aci.yaml**.

![img](../media/yml6.png)

7. Please copy the following YAML script to the **deploy-aci.yaml** file.

    ```YAML
    apiVersion: 2019-12-01
    location: eastus
    name: securetest
    properties:
    containers:
    - name: mycontainer
    properties:
    environmentVariables:
    - name: 'ACCEPT_EULA'
    value: 'Y'
    - name: 'MSSQL_SA_PASSWORD'
    value: 'India@123'
    image: mcr.microsoft.com/mssql/server:2019-CU12-ubuntu-20.04
    ports:
    - port: 1433
    resources:
    requests:
    cpu: 2
    memoryInGB: 2
    osType: Linux
    restartPolicy: Always
    tags: null
    type: Microsoft.ContainerInstance/containerGroups
    ```
8. 











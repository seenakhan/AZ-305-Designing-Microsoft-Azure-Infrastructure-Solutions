# Instructions

## Exercise 1: Deploy a Quickstart template on Azure 

In this exercise, you are going to deploy a quickstart template on Azure and deploy a traffic manager profile.

In this exercise, you will:

+ Task 1: Deploy a quickstart template on Azure.
+ Task 2: Deploy an App service to another region.
+ Task 3: Deploy a Traffic Manager Profile.

### Estimated Timing: 60 minutes

### Task 1: Deploy a quickstart template on Azure.

In this task, you will learn how to use Azur portal to deploy a template by using Deploy a custom template.

#### Pre-requisites for this task

An Azure account

#### Steps

1. Go to Azure Portal, enter **Custom deployment** on search bar, then select **Deploy a custom template**.

    ![img](../media/depl1.png)

2. On the **Custom deployment** page please select template source as **Quickstart templates**, Select **web-app-regional-vnet-private-endpoint-sql-storage** from the Quickstart templates dropdown, then select **Select template**, then select **Basics** tab.

    ![img](../media/depl2a.png)

3. Under **Basics** tab please enter the following details:

    | Section | Values |
    | ------- | ------ |
    | Resource group | Select **Create new**, then enter the name **newres123**, then click **Ok**. |
    | Region |  **West US** |
    | Sql Administrator Login Name | **contososqladmin** |
    | Sql Administrator Login Password | **Pa$$w0rd123!** |
    | V Nets | Enter **[{"name":"hub-vnet","addressPrefixes":["10.1.0.0/16"],"subnets":[{"name":"PrivateLinkSubnet","addressPrefix":"10.1.1.0/24","udrName":null,"nsgName":null,"delegations":null,"privateEndpointNetworkPolicies":"Disabled","privateLinkServiceNetworkPolicies":"Enabled"}]},{"name":"spoke-vnet","addressPrefixes":["10.2.0.0/16"],"subnets":[{"name":"AppSvcSubnet","addressPrefix":"10.2.1.0/24","udrName":null,"nsgName":null,"privateEndpointNetworkPolicies":"Enabled","privateLinkServiceNetworkPolicies":"Enabled","delegations":[{"name":"appservice","properties":{"serviceName":"Microsoft.Web/serverFarms"}}]}]}]** |
    
    
 4. After entering all the informations please select **Review + create**.    
    
    ![img](../media/depl4a.png)      

5. After passing validation, please select **Create**.

6. The deployment will take 10 minutes to complete. After completing the deployment, please select **Go to resource group**

7. Please review all the resources deployed on the resource group **newres123**.

8. On the **Overview** section of the resource group, please select the **App service** named **web-app-XXXXXXXX-XXXXXXXX**.

    ![img](../media/depl5a.png)

9. On the **Overview** section of the  resource group, please copy the Url of the App service.

    ![img](../media/depl6a.png)

10. Take another tab of browser and paste the url of app service. You will get the default page of the App.

    ![img](../media/depl7.png)

The application is running successfully.

### Task 2: Deploy an App service to another region

1. Search for **Web Apps** on the **search** box of the **Home** page, then select **App services** from the list below.

2. On the **App services** page, please select **+ Create**.

3. On the **Create Web App** page please enter the following details on the **Basics** tab and then select **Next: Deployment>** at the bottom.

    | Section | Values |
    | ------- | ------ |
    | Subscription | **Default** Select the default subscription |
    | Resource group | Select **newres123** |
    | Name | **web-app-EastUS** |
    | Publish | **Code** |
    | Runtime stack | Select **.Net 6 (LTS)** |
    | Operating System | Select **Windows** |
    | Region | Select **East US**. |
    | Windows Plan | Select **Create new** and enter **contosoappplanEastUS1** in the text box |
    | Pricing plan | Select **Standard S1 (100 total ACU, 1.75 GB memory, 1 vCPU)** |

    ![img](../media/webap1.png)

4. On the **Deployment** tab review the default settings and select **Next: Networking>** at the bottom.

5. On the **Networking** tab, please review the default settings and select **Next: Monitoring>** at the bottom.

6. On the **Monitoring** tab, set **Enable Application Insights** to **No** and then select **Review + create**.

    ![img](../media/webap2.png)

7. After completing the validation, please select **Create**. After completing the deployment please select **Go to resource**.

You have successfully deployed another web app.

### Task 3: Deploy a Traffic Manager Profile

#### Steps:

1. Go to Home page, and search for **Traffic Manager Profile**, then select **Traffice Manager Profile** from the list.

2. On the **Load balancing | Traffic Manager** page, please select **+ Create**.

    ![img](../media/trafp1.png)

3. On the **Create Traffic Manager Profile** page, please enter the following informations and then select **Create**. 

    | Section | Values |
    | ------- | ------ |
    | Name | **contosotrafficmanager-1**  |
    | Routing method | Select **Priority** |
    | Subscription | **Default** Select the default subscription |
    | Resource group | **newres123** |

    ![img](../media/trafp2.png)

After completing the deployment, you can see the **contosotrafficmanager-1**.

    ![img](../media/trafp3.png)

### Clean up resources

>**Please do not delete resources you deployed in this lab. You will reference them in the next lab of this module.**

### Review

In this lab, you have:

   - Deployed a quickstart template.
   - Verified the application is running.
    

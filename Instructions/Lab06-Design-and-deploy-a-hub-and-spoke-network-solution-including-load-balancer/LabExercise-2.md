# Instructions

## Exercise 2: Create a hub and spoke network

In this exercise, you will use Azure Virtual Network Manager to create a hub and spoke network topology. The hub virtual network will then have a virtual network gateway installed to allow resources in the spoke virtual networks to communicate with remote networks via VPN. 

In this Exercise, you will have:

  + Task 1: Create virtual networks.
  + Task 2: Deploy a virtual network gateway.
  + Task 3: Create a dynamic network group.
  + Task 4: Create a hub and spoke connectivity configuration.
  + Task 5: Deploy the connectivity configuration.

### Task 1: Create virtual networks

In this task you are going to create three virtual networks. One will be in the West US region and the other two will be in the East US region.

#### Pre-requisites for this task

Complete Exercise 1.

#### Steps:

1. Search for **Virtual networks** on the **search** box of the **Home** page, then select **Virtual networks** from the list below.

2. Please select the **+ Create** on the **Virtual network** page.

  ![img](/../media/vnt1.png)
  
3. On the **Create Virtual Network** page, please enter the following details on Basics tab:

  | Section | Values |
  | ------- | ------ |
  | Subscription | **Default** Select the default subscription |
  | Resource group | Select or create a new resource group to store the virtual network, here we will use a resource group named **contosovnet** |
  | Name | **Contoso-Vnet-WestUS** |
  | Region | **West US** |
  
  ![img](/../media/vnt2.png)
  
4. Go to **Next: IP Addresses**, then on the **IP Addresses** tab, please review the default IP addresses and subnet given.
  
  ![img](/../media/vnt3.png)
  
5. Once the validation passed successfully, please click on **Create**.

 ![img](/../media/vnt4.png)
 
6. After completing the deployment, please select **Go to resource**.

7. Repeat steps 2-5 to create two more virtual networks into the same resource group with the following information:

  **Second Virtual Network:**
  
  | Section | Values |
  | ------- | ------ |
  | Name | **Contoso-Vnet-EastUS** | 
  | Resource group | **contosovnet** |
  | Region | **East US** |
  
  
  For the **IP Addresses** tab keep the default settings.
  
  **Third Virtual Network:**
  
  | Section | Values |
  | ------- | ------ |
  | Name | **Contoso-Vnet-EastUS-A** |
  | Resource group | **contosovnet** |
  | Region | **East US** |
  
 After completing this task, you deployed three virtual networks.
 
 ### Task 2: Deploy a virtual network gateway

Deploy a virtual network gateway into the hub virtual network. This virtual network gateway is required for the spokes to be able to use the hub as a gateway setting.

In this task you are going to a virtual network gateway.

#### Pre-requisites for this task

Complete Exercise 1 & Exercise 2 - Task 1.

#### Steps:

1. Search for **Virtual network gateways** on the **search** box of the **Home** page, then select **Virtual network gateways** from the list below.

2. Please select **+ Create** on the **Virtual Network gateways**.

 ![img](/../media/vnt5.png)

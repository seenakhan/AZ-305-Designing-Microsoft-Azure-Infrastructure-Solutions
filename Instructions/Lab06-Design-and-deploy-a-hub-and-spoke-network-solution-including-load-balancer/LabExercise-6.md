# Instructions

## Exercise 6: Verify deployment of configurations


In this Exercise, you will have:

  + Task 1: Verify from a Virtual network.
  + Task 2: Verify from a Virtual machine.
   
### Task 1: Verify from a Virtual network

#### Pre-requisites for this task

Complete Exercise 1 & Exercise 2 & Exercise 3 & Exercise 4 & Exercise 5

#### Steps:

1. Go to **Contoso-Vnet-EastUS** virtual network and select **Network Manager** under **Settings**. You'll see the **HubA** connectivity configuration applied.

![img](../media/ver1.png)

2. Go to **Contoso-Vnet-WestUS** virtual network and select **Peerings** under **Settings**. You'll see virtual network peerings created by Virtual Network Manager with ANM in the name.

![img](../media/ver2.png)

3. Go to **Contoso-Vnet-EastUS** virtual network and select **Network Manager** under **Settings** and select the **SecurityAdmin** tab to see the security admin rules applied to this virtual network.

![img](../media/VER3.png)

### Task 2: Verify from a Virtual machine

In this task you are going to dpeloy a test virtual machine into **Contoso-Vnet-EastUS** virtual network and then verify the connection configurations.

#### Pre-requisites for this task

Complete Exercise 1 & Exercise 2 & Exercise 3 & Exercise 4 & Exercise 5

#### Steps:

1. Go to home page and search for virtual machines in the search box, then select **Virtual machines** from the below list.

2. On the Virtual machines page, please select **+ Create** and then select **Azure virtual machine**.

![img](../media/ver4.png)

3. On the **Basics** tab of the **Create a virtual machine** page, please enter the following details, then select **Next:Disk>** from the bottom.

    | Section | Values |
    | ------- | ------ |
    | Subscription | Select the default subscription |
    | Resource group | **contosovnet** |
    | Region | **East US** |
    | Image | **Windows Server 2019 Datacenter - x64 Gen2** |
    | VM Architecture | **X64** |
    | Size | **Standard_DS1_v2 - 1 vcpu, 3.5 GiB memory** |
    | User | **azureuser** |
    | Password | **Passw0rd123!** |
    | Confirm password | **Passw0rd123!** |
    
  ![img](../media/ver5.png)  
  ![img](../media/ver6.png)
  
4. On the **Disks** tab, for **OS disk type** please select **Standard SSD (Locally-redundant storage), then select **Next:Networking>**.

![img](../media/ver7.png)

5. On the **Networking** tab for **Virtual network** please select **Contoso-Vnet-EastUS** virtual network, keep the default values of other settings as it is, then select **Review + Create**.

![img](../media/ver8.png)  

6. After Validation passed successfully, please select **create**.


  
  
  
    
    



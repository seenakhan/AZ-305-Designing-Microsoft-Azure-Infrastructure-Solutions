# Instructions

## Exercise 4: Create a hub and spoke connectivity configuration and Deploy the connectivity configuration

In this Exercise, you will have:

  + Task 1: Create a hub and spoke connectivity configuration
  + Task 2: Deploy the connectivity configuration

### Task 1: Create a hub and spoke connectivity configuration

Before deploying the connectivity configuration, ensure that the virtual network gateway has been successfully deployed. The deployment will fail if you deploy a hub and spoke configuration with Use the hub as a gateway enabled and there is no gateway.

#### Pre-requisites for this task

Complete Exercise 1 & Exercise 2 & Exercise 3

#### Steps:

1. Go to Network manager named **contosonetmanager**, please select **Configuration** under Settings, then select **+ Create**, then select **Connectivity configuration** from the drop-down menu.

2. On the Basics tab, enter and select the following information for the connectivity configuration:

  | Section | Values |
  | ------- | ------ |
  | Name| Enter **HubA** for the name of the configuration |
  | Description | **This configuration contains a hub virtual network in the West US region**. |
  
3. Select Next: Topology >. Select Hub and Spoke under the Topology setting. This will reveal other settings.

4. Select Select a hub under Hub setting. Then, select VNet-A-WestUS to serve as your network hub and select Select.

5. Under Spoke network groups, select + add. Then, select **contosonetworkgrp** for the network group and select Select.

6. 


## Instructions

### Exercise 2

#### Task 1: Assign policies and governance to management groups

The first step in enforcing Azure Policy compliance is to assign a policy definition. A policy definition specifies how a policy is enforced and what effect it has. In this task, use the built-in policy definition Inherit a tag from the resource group if missing to add the specified tag and its value from the parent resource group to new or updated resources that are missing the tag.

#### Pre-requisites for this task

Complete Exercise 1

#### Steps:

1. Go to search box and enter policy, then select **Policy** from the list.

![image](../media/pol1.png)

2. Select **Assignments** on the left side of the Azure Policy page and then select **Assign Policy**.
      
      **Note: An assignment is a policy that has been assigned to take place within a specific scope.**

![image](../media/pol2.png)

3. On the **Assign Policy** page under **Basic** tab for **Scope** section you can see the default subscription selected or else please select the default subscription. 

4. Please click on **Exclusions** elipsis **(...)** towards the right side of the exclusions.

5. On the Exclusions side screen Select the Resource group **ODL-AZ-305M02-838938** and then select **Add to selected scope** and then **Save**.

![image](../media/pol6a.png)

6. Please click on **Policy Definitions** elipsis **(...)**.

7. On the **Available Definitions** sidescreen take a moment to browse through the list of built-in policy definitions that are available for you to use.

8. On the search box please type **tag** and select **Require a tag and its value on resources** built in definition, then click **Save**.

![image](../media/pol7.png)

9. By selecting the policy definition, the assignment name also filled automatically.

10. Click on **Next** at the bottom, review the **Advanced** tab and leave the default settings as it is.

11. Click on **Next** at the bottom, under the **Parameters** tab please enter the following details:

    | Tag name | **Role** |
    | -------- | ----------------- |
    | Tag value | **Owner** |
    
![image](../media/pol9a.png)    

12. Leave the default settings of other options as it is.

13. Please select **Review + Create**.

![image](../media/pol10.png) 

14. After the validation, please select **Create**.

15. On the Assignments section, you can see the newly created **Assignment**.

#### Task 2: Create a Storage account


#### Pre-requisites for this task

Complete Exercise 1

#### Steps:

1. On the Azure portal, please select **All Services** and select **Storage accounts**.

![image](../media/pol11.png)

2. On the **Storage accounts** page, please select **+Create**.

![image](../media/pol12.png)

3. On the Storage account page, keep the default subscription selected, then please select a resource group included in the policy assignment from the resource group list.

4. Please enter a name of the storage account on the **storage account name** and then click **Review**.

    | Setting | Value |
    | --- | --- |
    | Storage account name | any globally unique combination of between 3 and 24 lower case letters and digits, starting with a letter |

![image](../media/pol13.png)

5. You can see the validation failed, and there is a validation error. Please click on the **validation error**, a side screen of error details will open. It shows the error happens due to the policy.

![image](../media/pol14.png)

6. On the same page, please select **Tags** tab and enter the following details and click **Review**:

      | Name | **Role** |
      | ---- | -------- |
      | Value | **Owner** |
 
 ![image](../media/pol15.png)
      
7. Now you can see the validation passed successfully.

8. Please click **Create**.

![image](../media/pol16.png)

9. You have successfully created the storage account now.

     



  

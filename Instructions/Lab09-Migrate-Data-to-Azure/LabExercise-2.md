# Instructions

## Exercise 1: Migrate SQL Server database to Azure

In this exercise, you will:

+ Task 1: Create an Azure SQL database
+ Task 1: Install the Data Migration Assistant (DMA) on Windows
+ Task 2: Use the Data Migration Assistant to prepare for migration from SQL Server to Azure SQL Database
+ Task 3: Use Data Migration Assistant to migrate a sample schema
+ Task 4: Create Azure Database Migration Service instance

### Estimated Timing:  minutes

### Task 1: Create an Azure SQL database

In this task, you will learn how to create an Azure SQl database by using Azure portal.

#### Pre-requisites for this task

An Azure account

#### Steps

1. In the home page of Azure portal, please enter **SQL database** on the search bar and select **SQL database** from the list.

2. On the SQL databases page, please select **+ Create**.

![img](../media/datas1.png)

3. On the **Create SQL Database** please enter the following informations.

    | Settings | Values |
    |  -- | -- |
    | Subscription | **Use default supplied** |
    | Resource group | **ODL-AZ-305M05D-XXXXX-AZ-305M05D** |
    | Database name | **contosodb1** |

![img](../media/datas2.png)

4. 4. For server, click **Create new**.

5. On **Create SQL Database Server** page, please enter the following details, then click **Ok**.

    | Settings | Values |
    |  -- | -- |      
    | Server name | **contososerv** |
    | Location | **East US** |
    | Authentication method | **Use SQL authentication** |
    | Server admin login | **contosoadmin** 
    | Password |  **Contoso@123** 
    | Confirm password | **Contoso@123** |    

![img](../media/datas3.png)

6. After creating the database server, please enter the following, then select **Review + create**. 

    | Settings | Values |
    |  -- | -- |      
    | Server name | **contososerv** |
    | Want to use SQL elastic pool? | **No** |    |
    | Compute + storage | **General Purpose (Standard-series (Gen5), 2 vCores, 32 GB storage, zone redundant disabled)** |
    | Backup storage redundancy |  **Locally-redundant backup storage** |

![img](../media/datas4.png)

7. After the validation, please select **Create**.

### Task 2: Set up server-level firewall rules using Azure Portal

In this task you will configure Server firewall. Azure SQL Server is protected by server-level firewall rules. As a result, it applies to all underlying Azure SQL Databases. Before reaching the Azure server or database, each connection must pass through the firewall.

#### Pre-requisites for this task

An Azure account, a resource group and an Azure SQL Database 

#### Steps:

1. Please select the database you have created on the previous task. Select **Set Server Firewall** on the **Overview** section.

![img](../media/datas5.png)

2. On the Networkinmg page, Please select **Selected Networks**. To add your current IP address to a new server-level firewall rule, select **+ Add your client IP**. This rule has the ability to open Port 1433 for a single IP address or a range of IP addresses, then select **Save**.

3. Go to **contosodb1** database, select **Query Editor** provide the login as **contosoadmin** and Password **Contoso@123** then click **Ok**.

![img](../media/datas6.png)

You have successfully logged into the contosodb1 database.

### Task 2: Install the Data Migration Assistant (DMA) on Windows

In this task, you will learn how to install and configure Data Migration Assistant (DMA) on Windows.

#### Pre-requisites for this task

An Azure account

#### Steps
  

1. Open up your web browser, and go to the download page for Microsoft Data Migration Assistant, please click [here](https://www.microsoft.com/en-us/download/details.aspx?id=53595).
    
    > [!NOTE]
    > Follow the steps in this task even if DMA is already installed, to ensure that you are using the latest version of the tool.

2. Confirm that your environment supports the software by checking the requirements list. If its ask for installing .Net Framework 4.8 please click [here](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48) to download. After downloading it, please go to the download folder and double click on the .Net installer file named **ndp48-web** to install it.

3. To download **DataMigrationAssistant.msi**, select **Download**, and then select **Run**.

4. On the **Welcome** screen, select **Next**.

5. Select **I accept the terms in the License Agreement**, and then select **Next**.

6. Read the **Privacy Statement**, and then select **Install**.

7. If prompted, allow UAC control for this application.

8. To complete install, select **Finish**.

### Task 2: Use the Data Migration Assistant to prepare for migration from SQL Server to Azure SQL Database

1. Select the **Start** button, type **Data Migration**, and then select **Microsoft Data Migration Assistant**.

2. To create a new project, on the left, select **+**.

![img](../media/datam1.png)

3. On the **New** page, enter these values, and then select **Create**:

    | Property | Value |
    | --- | --- |
    | Project type | **Assessment** |
    | Project name | **Migration Assessment SQL DB** |
    | Assessment type | Database Engine |
    | Source server type | SQL Server |
    | Target server type | Azure SQL Database |
    
  ![img](../media/datam2.png)  

4. On the **Options** page, leave the default values, and then select **Next**.

5. On the **Connect to a server** page, enter these values, and then select **Connect**:

    | Property | Value |
    | --- | --- |
    | Server name | **labvm-XXXXXX\SQLEXPRESS** (Please go to SSMS and take the server name from there). |
    | Authentication type | **Windows Authentication** |
    | Encrypt connection | Deselected |
    | Trust server certificate | Selected |

![img](../media/datam3a.png) 

6. On the **Add sources** page, select the **AdventureWorks** database, and then select **Add**.

![img](../media/datam4.png) 

7. On the **Select sources** page, select **Start Assessment**.

8. Review the SQL Server feature parity and compatibility issues found. Note how many feature parity issue there are.

![img](../media/datam5.png) 

9. Go to SSMS, right click on the server name, then select **Properties**.

![img](../media/datam6.png)

10. On the **Server properties** window, select **Security**, then select **SQL Server and Windows Authentication** mode.

![img](../media/datam7.png)

### Task 3: Use Data Migration Assistant to migrate a sample schema

#### Steps

1. Run **Microsoft Data Migration Assistant** tool, select the **+** New (+) icon, and enter the following details and then select **Create**.

    | Property | Value |
    | --- | --- |
    | Project type | **Migration** |
    | Project name | **Migration schema only SQL DB** |
    | Source server type | Select **SQL Server** |
    | Target server type | Select **Azure SQL Database** |
    | Migration scope | Select **Schema only** |

![img](../media/datam8.png)

2. On the Select Source tab, Select the server name **labvm-XXXXX\SQLEXPRESS**, then select **Windows Authentication** as Authentication type, then select **connect**. 

![img](../media/datam9.png)

3. Select **Adventureworks2019**, then select **Next**.

4. Go to **contosodb1** database on azure portal, then on the **Overview** section, please copy the server name **contososerv.database.windows.net**.

5. Go to **Microsoft Data Migration Assistant** tool and on the **Connect to target server** tab on the server name section, paste the contosdb1 server name copied.

6. For the **Authentication type** please select **SQL Server Authentication**, then enter username as **contosoadmin**, and password as **Contoso@123**.

7. Select **Connect**.

![img](../media/datam10.png)

8. Select **contosodb1** and then click on **Next**

9. On the **Select Object** tab, please select the **Schema** (By default all the objects are selected, please unselect all other objects except schema).

10. To create the SQL scripts, select **Generate SQL scripts option**.

![img](../media/datam11.png)

11. On the **Script & Deploy schema** tab please select **Deploy schema**.

![img](../media/datam12.png)

12. You have successfully migrated the schema, you can see the execution of all the schema queries are successfully completed.

![img](../media/datam13.png)

